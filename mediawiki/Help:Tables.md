{{PD Help Page}}

Tables may be authored in wiki pages using either HTML table elements directly, or using wikicode formatting to define the table. HTML table elements and their use are well described on various web pages and will not be discussed here. The benefit of wikicode is that the table is constructed of character symbols which tend to make it easier to perceive the table structure in the article editing view compared to HTML table elements.

As a general rule, it is best to avoid using a table unless you need one. Table markup often complicates page editing.

== Wiki table markup summary ==

{|cellpadding="5" cellspacing="0" border="1" width="600"
|<nowiki>{|</nowiki> || '''table start'''
|-
|<nowiki>|+</nowiki> || table '''caption,''' ''optional;'' only between '''table start''' and first '''table row'''
|-
|<nowiki>|-</nowiki> || '''table row,''' ''optional on first row'' -- wiki engine assumes the first row
|-
|<nowiki>!</nowiki>  || '''table header''' cell, ''optional.'' Consecutive '''table header''' cells may be added on same line separated by double marks (!!) or start on new lines, each with its own single mark (!).
|- 
|<nowiki>|</nowiki>  || '''table data''' cell, ''required!'' Consecutive '''table data''' cells may be added on same line separated by double marks (<nowiki>||</nowiki>) or start on new lines, each with its own single mark (<nowiki>|</nowiki>).
|-
|<nowiki>|}</nowiki> || '''table end'''
|}
*The above marks must '''start on a new line''' except the double || and !! for optionally adding consecutive cells to a line.
*'''XHTML attributes.''' Each mark, except table end, optionally accepts one or more XHTML attributes. Attributes must be on the same line as the mark. Separate attributes from each other with a single space. 
**Cells and caption (<nowiki>| or ||, ! or !!, and |+</nowiki>) hold content. So separate any attributes from content with a single pipe (|). Cell content may follow on same line or on following lines.
**Table and row marks (<nowiki>{| and |-</nowiki>) do not directly hold content. Do ''not'' add pipe (|) after their optional attributes. If you erroneously add a pipe after attributes for the table mark or row mark the parser will delete it ''and'' your final attribute if it was touching the erroneous pipe!
*'''Content''' may (a) follow its cell mark on the same line after any optional XHTML attributes or (b) on lines below the cell mark. Content that uses wiki markup that itself needs to start on a new line, such as lists, headers, or nested tables, must of course be on its own new line.

==Simple table==

===Plain===
The following table lacks borders and good spacing but shows the simplest wiki markup table structure
{| width="100%"
|width="50%"|
{|
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{|
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

===Alternative===
For more table-ish looking wiki markup cells can be listed on one line separated by ||. This does not scale well for longer cell content such as paragraphs. It works well for short bits of content however, such as our example table.

Extra spaces within cells in the wiki markup can be added, as I have done in the wiki markup below, to make the wiki markup itself look better but they do not affect the actual table rendering.

HTML attributes can be added to tables on this page but have been left out of the following example for simplicity.
{| width="100%"
|width="50%"|
{|
|  Orange    ||   Apple   ||   more
|-
|   Bread    ||   Pie     ||   more
|-
|   Butter   || Ice cream ||  and more
|}
|width="50%"|
<pre>
{|
|  Orange    ||   Apple   ||   more
|-
|   Bread    ||   Pie     ||   more
|-
|   Butter   || Ice cream ||  and more
|}
</pre>
|}

===With HTML attributes===
You can add HTML attributes to make your table look better
====border="1"====
{| width="100%"
|width="50%"|
{| border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

====align="center" border="1"====
{| width="100%"
|width="50%"|
{| align="center" border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| align="center" border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

====Attributes on cells ====
You can put attributes on individual '''cells.''' Numbers for example may look better aligned right
{| width="100%"
|width="50%"|
{| border="1"
|Orange
|Apple
|align="right"|12,333.00
|-
|Bread
|Pie
|align="right"|500.00
|-
|Butter
|Ice cream
|align="right"|1.00
|}
|width="50%"|
<pre>
{| border="1"
|Orange
|Apple
|align="right"|12,333.00
|-
|Bread
|Pie
|align="right"|500.00
|-
|Butter
|Ice cream
|align="right"|1.00
|}
</pre>
|}

====Attributes on rows====
You can put attributes on individual '''rows,''' too.
{| width="100%"
|width="50%"|
{| border="1"
|Orange
|Apple
|align="right"|12,333.00
|-
|Bread
|Pie
|align="right"|500.00
|- style="font-style:italic;color:green;"
|Butter
|Ice cream
|align="right"|1.00
|}
|width="50%"|
<pre>
{| border="1"
|Orange
|Apple
|align="right"|12,333.00
|-
|Bread
|Pie
|align="right"|500.00
|- style="font-style:italic;color:green;"
|Butter
|Ice cream
|align="right"|1.00
|}
</pre>
|}

====cellspacing="0" border="1"====
{| width="100%"
|width="50%"|
{| cellspacing="0" border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| cellspacing="0" border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

====cellpadding="20" cellspacing="0" border="1"====
{| width="100%"
|width="50%"|
{| cellpadding="20" cellspacing="0" border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| cellpadding="20" cellspacing="0" border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

===With HTML attributes and CSS styles===
CSS style attributes can be added with or without other HTML attributes
====style="color:green;background-color:#ffffcc;" cellpadding="20" cellspacing="0" border="1"====
{| width="100%"
|width="50%"|
{| style="color:green;background-color:#ffffcc;" cellpadding="20" cellspacing="0" border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| style="color:green;background-color:#ffffcc;" cellpadding="20" cellspacing="0" border="1"
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

==Table with TH headings==

TH (HTML table headings) can be created by using ! instead of |. Headings usually show up bold and centered by default.

===Top headings===
====Each column====
{| width="100%"
|width="50%"|
{| border="1" cellpadding="20" cellspacing="0"
!Yummy
!Yummier
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| border="1" cellpadding="20" cellspacing="0"
!Yummy
!Yummier
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

====Colspan="2"====
{| width="100%"
|width="50%"|
{| border="1" cellpadding="20" cellspacing="0"
!colspan="2"|Yummies
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| border="1" cellpadding="20" cellspacing="0"
! colspan="2"|Yummies
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

===Side headings===
====Default====
{| width="100%"
|width="50%"|
{| border="1" cellpadding="20" cellspacing="0"
!Fruit
|Orange
|Apple
|-
!Dish
|Bread
|Pie
|-
!Complement
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| border="1" cellpadding="20" cellspacing="0"
!Fruit
|Orange
|Apple
|-
!Dish
|Bread
|Pie
|-
!Complement
|Butter
|Ice cream 
|}
</pre>
|}

====Right justify====
Right justified side headings can be done as follows
{| width="100%"
|width="50%"|
{| border="1" cellpadding="20" cellspacing="0"
!align="right" |Fruit
|Orange
|Apple
|-
!align="right" |Dish
|Bread
|Pie
|-
!align="right" |Complement
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| border="1" cellpadding="20" cellspacing="0"
!align="right" |Fruit
|Orange
|Apple
|-
!align="right" |Dish
|Bread
|Pie
|-
!align="right" |Complement
|Butter
|Ice cream 
|}
</pre>
|}

==Caption==
A '''table caption''' can be added to the top of any table as follows
{| width="100%"
|width="50%"|
{| border="1" cellpadding="20" cellspacing="0"
|+Food complements
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| border="1" cellpadding="20" cellspacing="0"
|+Food complements
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

'''Attributes''' can be added to the caption as follows

{| width="100%"
|width="50%"|
{| border="1" cellpadding="20" cellspacing="0"
|+align="bottom" style="color:#e76700;"|''Food complements''
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| border="1" cellpadding="20" cellspacing="0"
|+align="bottom" style="color:#e76700;"|''Food complements''
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

==Table with H1, H2, H3 etc. headings==

HTML H1, H2, H3, H4 etc. headings can be created the standard wiki markup way with ==equal== signs and '''must be on a line all by themselves''' to work.

'''Preview the whole table.''' If you click on an edit tab for a heading ''within'' a table, edit, and preview, the parent table will display erroneously broken because part of it will be missing.

Keep the heading hierarchy consistent with the rest of the page so that the table of contents at page top works correctly.

{| width="100%"
|width="50%"|
{| border="1" cellpadding="20" cellspacing="0"
|colspan="2"|
===Yummiest===
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
|width="50%"|
<pre>
{| border="3"  cellpadding="20" cellspacing="0"
|colspan="2"|
===Yummiest===
|-
|Orange
|Apple
|-
|Bread
|Pie
|-
|Butter
|Ice cream 
|}
</pre>
|}

==Caveat==
===Negative numbers===
Negative value minus sign can break your table (it may display missing some values) if you start a cell on a new line with a negative number or a parameter that evaluates to a negative number (|-6) because that is the wiki markup for table row, not table cell. To avoid this, insert a space before the value (| -6) or use in-line cell markup (||-6).

{{Languages|Help:Tables}}
[[Category:Help|Tables]]
[[Category:Imported help]]