{{PD Help Page}}
==Introduction==
Sometimes it becomes necessary to have certain links in your wiki to be opened in an external windows leaving the current window as is. This help is for such special situation only. If your wiki is completely locked for editing , and you need complete freedom for embedding html use [$wgRawHtml = true;] in your Localsettings.php!
Note: This might is a very simple process, have been inspired by 
# {{mediawiki|Manual:Opening_external_links_in_a_new_window}}

==Method==
# Follow {{mediawiki|Extension:Secure_HTML}} to install Secure_HTML extension
# go to http://www.yoursite.org/yourwiki/index.php/Special:SecureHTMLInput in your site
# paste the following html code.
 <html>
 <body>
 <a href="http://www.yoursite.com" target="_blank">title</a>
 </body>
 </html>
 Note: Please replace the address with link, file or external site address.
# Submit to get the hashed code.(Please refer the extension page given above for instruction for this)
# Paste this into a seperate page in your wiki, This page can be embedded into any other page.

There you have it, A specific link that opens in another page.

 Note: This is just a process, just mixed and matched data.
 Hope i have not infringed on any license
 If i have please feel free to delete this page.
 I had created this page, as i found it hard to do this
 in one of our internal sites. This help might help some one, someday.

[[Category:Help|{{PAGENAME}}]]
[[Category:Imported help]]