{{PD Help Page}}
'''Range blocks''' are technical restrictions applied through [[Special:Blockip]] to a group of [http://en.wikipedia.org/wiki/IP_addresses IP addresses] that prevent them from editing, creating new accounts, sending email through the wiki interface, et cetera. Registered accounts editing from these IP addresses will also be blocked, unless you check the box to only block anonymous editors.

Range blocking is enabled on all [http://en.wikipedia.org/wiki/Wikimedia_Foundation Wikimedia] wikis; to enable it on other wikis, add "<code>{{mediawiki|Manual:$wgSysopRangeBans|$wgSysopRangeBans}} = true;</code>" in <tt>{{mediawiki|Manual:LocalSettings.php|LocalSettings.php}}</tt>.

To block an IP range from [[Special:Blockip]], enter the first IP address in the range followed by a forward slash and a [http://en.wikipedia.org/wiki/Classless_inter-domain_routing Classless inter-domain routing] (CIDR) suffix. '''You should avoid performing range blocks unless you understand what you are doing, or you may end up blocking tens of thousands of people who are not the problem!'''

==Technical explanation==
CIDR notation is written as the IP address, a slash, and the CIDR affix (for example, the IPv4 "<code>10.2.3.41/24</code>" or IPv6 "<code>a3:b:c1:d:e:f:1:21/24</code>"). The CIDR affix is the number of starting digits every IP address in the range have in common when written in binary. 

For example: "<code>10.10.1.32</code>" is binary "<code>00001010.00001010.00000001.00100000</code>", so <code>10.10.1.32/27</code> will match the first 27 digits ("<code><u>00001010</u>.<u>00001010</u>.<u>00000001</u>.<u>001</u>00000</code>"). The IP addresses <code>10.10.1.32</code>–<code>10.10.1.63</code>, when converted to binary, all have the same 27 first digits and will be blocked if <code>10.10.1.32/27</code> is blocked.

As the CIDR affix increases, the block affects fewer IP addresses (see [[#Table|table of example ranges]]). CIDR affixes are not the same for IPv4 addresses as they are for IPv6 addresses.

==Calculating the CIDR affix==
You can use the [[#Table|table of sample ranges]] below to guess the range, use a computer script, or manually calculate the range.

===Conversion to binary===
The first step in manually calculating a range is to convert the first and last IP address to binary representation. (This assumes you're not using a computer script, which can probably calculate the range for you anyway.) An IP address is composed of four groups of eight ones and zeros. Each group represents a number from 0 to 255. To convert a number to binary, you can use a [http://www.ccci.com/tools/subcalc/binary.html reference table] or know the value of each binary digit:
{| class="prettytable" style="text-align:center;"
|-
| 1
| 1
| 1
| 1
| 1
| 1
| 1
| 1
|-
| 128
| 64
| 32
| 16
| 8
| 4
| 2
| 1
|}

Proceeding from left to right, fill in '1' if the number is at least that value, and subtract that value (if it's not, fill in '0' and don't subtract). For example, to calculate 240:
# 240 is at least 128, so place 1 and subtract 128.
# 112 (240-128) is at least 64, so place 1 and subtract 64.
# 48 (112-64) is at least 32, so place 1 and subtract 48.
# 16 (48-32) is at least 16, so place 1 and subtract 16.
# Since the remaining value is zero, all the remaining places are '0'.
Thus, 240 is 1111 0000 because it can be represented as 128+64+32+16+0+0+0+0.

===Calculate range===
# Place both IP addresses one atop the other, and count how many starting digits are exactly alike. This is the CIDR affix.
# Double-check! Being off by one digit could extend your block by thousands of addresses.

The example below calculates the CIDR range between 69.208.0.0 and 69.208.0.255. Note that this is a simple example; some groups of IP addresses do not so neatly fit CIDR affixes, and need multiple different-sized blocks to block the exact range.
 IP addresses:
   69.208.0.0
   69.208.0.255
 &nbsp;
 Convert to binary:
   0100 0101.1101 0000.0000 0000.0000 0000
   0100 0101.1101 0000.0000 0000.1111 1111
 &nbsp;
 Count identical first numbers:
   '''0100 0101.1101 0000.0000 0000'''.0000 0000
   '''0100 0101.1101 0000.0000 0000'''.1111 1111
   |____________________________|
             24 digits
  &nbsp;
 CIDR range:
   69.208.0.0/24
</pre>

===<span id="Table">Table of sample ranges</span>===
The table below shows the IP blocks each CIDR suffix affects. Note that MediaWiki only supports blocking CIDR suffixes 16&ndash;32.

{| class="prettytable"
! CIDR
! Start Range
! End Range
! Total addresses
! Bits selected in IP address
|- style="color:gray;"
| 69.208.0.0'''/0'''
| 0.0.0.0
| 255.255.255.255
| 4,294,967,296
| ********.********.********.********
|- style="color:gray;"
| 69.208.0.0'''/1'''
| 0.0.0.0
| 127.255.255.255
| 2,147,483,648
| 0*******.********.********.********
|- style="color:gray;"
| 69.208.0.0'''/4'''
| 65.0.0.0
| 79.255.255.255
| 268,435,456
| 0100****.********.********.********
|- style="color:gray;"
| 69.208.0.0'''/8'''
| 69.0.0.0
| 69.255.255.255
| 67,108,864
| 01000101.********.********.********
|- style="color:gray;"
| 69.208.0.0'''/11'''
| 69.208.0.0
| 69.238.255.255
| 2,197,152
| 01000101.110*****.********.********
|- style="color:gray;"
| 69.208.0.0'''/12'''
| 69.208.0.0
| 69.223.255.255
| 1,048,576
| 01000101.1101****.********.********
|- style="color:gray;"
| 69.208.0.0'''/13'''
| 69.208.0.0
| 69.215.255.255
| 524,288
| 01000101.11010***.********.********
|- style="color:gray;"
| 69.208.0.0'''/14'''
| 69.208.0.0
| 69.211.255.255
| 262,144
| 01000101.110100**.********.********
|- style="color:gray;"
| 69.208.0.0'''/15'''
| 69.208.0.0
| 69.209.255.255
| 131,072
| 01000101.1101000*.********.********
|-
| 69.208.0.0'''/16'''
| 69.208.0.0
| 69.208.255.255
| 65,536
| 01000101.11010000.********.********
|-
| 69.208.0.0'''/17'''
| 69.208.0.0
| 69.208.127.255
| 32,768
| 01000101.11010000.0*******.********
|-
| 69.208.0.0'''/18'''
| 69.208.0.0
| 69.208.63.255
| 16,384
| 01000101.11010000.00******.********
|-
| 69.208.0.0'''/19'''
| 69.208.0.0
| 69.208.31.255
| 8,192
| 01000101.11010000.000*****.********
|-
| 69.208.0.0'''/20'''
| 69.208.0.0
| 69.208.15.255
| 4,096
| 01000101.11010000.0000****.********
|-
| 69.208.0.0'''/21'''
| 69.208.0.0
| 69.208.7.255
| 2,048
| 01000101.11010000.00000***.********
|-
| 69.208.0.0'''/22'''
| 69.208.0.0
| 69.208.3.255
| 1,024
| 01000101.11010000.000000**.********
|-
| 69.208.0.0'''/23'''
| 69.208.0.0
| 69.208.1.255
| 512
| 01000101.11010000.0000000*.********
|-
| 69.208.0.0'''/24'''
| 69.208.0.0
| 69.208.0.255
| 256
| 01000101.11010000.00000000.********
|-
| 69.208.0.0'''/25'''
| 69.208.0.0
| 69.208.0.127
| 128
| 01000101.11010000.00000000.0*******
|-
| 69.208.0.0'''/26'''
| 69.208.0.0
| 69.208.0.63
| 64
| 01000101.11010000.00000000.00******
|-
| 69.208.0.0'''/27'''
| 69.208.0.0
| 69.208.0.31
| 32
| 01000101.11010000.00000000.000*****
|-
| 69.208.0.0'''/28'''
| 69.208.0.0
| 69.208.0.15
| 16
| 01000101.11010000.00000000.0000****
|-
| 69.208.0.0'''/29'''
| 69.208.0.0
| 69.208.0.7
| 8
| 01000101.11010000.00000000.00000***
|-
| 69.208.0.0'''/30'''
| 69.208.0.0
| 69.208.0.3
| 4
| 01000101.11010000.00000000.000000**
|-
| 69.208.0.0'''/31'''
| 69.208.0.0
| 69.208.0.1
| 2
| 01000101.11010000.00000000.0000000*
|-
| 69.208.0.0'''/32'''
| 69.208.0.0
| 69.208.0.0
| 1
| 01000101.11010000.00000000.00000000
|}

==References==
* [[wikipedia:Classless Inter-Domain Routing|Classless Inter-Domain Routing]]
* [http://www.ccci.com/tools/subcalc/binary.html Converting IP addresses to binary]

==External links==
* [http://www.find-ip-address.org/ip-country/ IP Address Ranges Block] gives you complete IP ranges for certain country.
* [http://apps.csc.fi/laskin2.html Netmask calculator] which helps in making the correct decision for range blocks.
* [http://tools.wikimedia.de/~chm/blockcalc.php Rangeblock-Calculator] gives you the range you should use when blocking.

{{Languages|Help:Range blocks}}

[[Category:Help|Range blocks]]
[[Category:Imported help]]