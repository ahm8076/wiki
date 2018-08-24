{{PD Help Page}}
If you have standard texts you want to include on several pages, the MediaWiki template feature comes into play.

==Creating a template==
Templates are standard wiki pages, only the template names are prefixed with "<code>Template:</code>". Therefore you can [[Help:Starting a new page|create them like any other wiki page]].

==Using a template==
Templates are wiki pages which can be used in other pages in three ways:
*<code><nowiki>{{Name}}</nowiki></code> 'transcludes' (i.e. includes a copy) the content of the template (stored in the page <nowiki>[[Template:Name]]</nowiki>) whenever the page containing the template transclusion is fetched and displayed; i.e. if the template is later changed, the displayed transcluding page will automatically change too
*<code><nowiki>{{subst:Name}}</nowiki></code> replaces that string with the contents of the template, in the source of the transcluding page, when you save that page; the copy of the template contents can then be edited normally (and separately from the original in the template page). '''''Note''''': don't use this if you are looking to continually propagate changes from the source template to the page(s) that references it.
*<code><nowiki>{{msgnw:Name}}</nowiki></code> includes the template in a form that displays it as raw wiki syntax (the way <code><nowiki>&lt;nowiki&gt;</nowiki></code> does) when the page containing it is fetched

==Using parameters in templates==
<div style="float:right; margin:8px;">
{| {{Prettytable}} 
|-
|{{Hl2}} colspan="2" align="center" |'''Template with numbered parameters'''	
|-
| colspan="2" |
<pre><nowiki> 
'''A little thank you...'''<br>
<small>for {{{1}}}.<br>
hugs, {{{2}}}</small>
</nowiki></pre> 
|-
|{{Hl2}}|'''You type'''	
|{{Hl2}}|'''You get'''
|-
|<code><nowiki>{{Thankyou|all your hard work|Joe}}</nowiki></code>
|
{{Thankyou|all your hard work|Joe}}
|-
|{{Hl2}} colspan="2" align="center" |'''with named parameters'''	
|-
| colspan="2" |
<pre><nowiki> 
'''A little thank you...'''<br>
<small>for {{{reason}}}.<br>
hugs, {{{signature}}}</small>
</nowiki></pre> 
|-
|{{Hl2}}|'''You type'''	
|{{Hl2}}|'''You get'''
|-
|<pre><nowiki>{{Thankyou
|reason=all your hard work
|signature=Joe}}</nowiki></pre>
|
{{Thankyou|all your hard work|Joe}}
|}
</div>
You can define parameters in templates either numbered as <code><nowiki>{{{1}}}</nowiki></code> or named <code><nowiki>{{{param}}}</nowiki></code>.  

'''Example:''' You want a little thank you note you can put on the talk page of other users. It will contain a reason and your signature. You could create [[Template:Thankyou]] to enter your text, as in the example in the table.

When using the template on a page, you fill in the parameter values, separated by a pipe char (|): <code><nowiki>{{Thankyou|all your hard work|Joe}}</nowiki></code>.  For named parameters use "name=value" pairs separated by a pipe char:   <code><nowiki>{{Thankyou|reason=all your hard work|signature=Joe}}</nowiki></code>. The advantage of using named parameters in your template is that they are flexible in order. It also makes the template easier to understand if you have many parameters. If you want to change the order of numbered parameters, you have to mention them explicitly: <code><nowiki>{{Thankyou|2=Joe|1=all your hard work}}</nowiki></code>.

You can also provide default values for parameters, i.e. values that are going to be used if no value is provided for a parameter. For example, <code><nowiki>{{{reason|all your hard work}}}</nowiki></code> would result in ''"all your hard work"'' if no value was provided for the parameter <tt>reason</tt>.

==Control template inclusion==
You can control template inclusion by the use of <code><nowiki><noinclude></nowiki></code> and
<code><nowiki><includeonly></nowiki></code> tags.

Anything between <code><nowiki><noinclude></nowiki></code> and <code><nowiki></noinclude></nowiki></code> will be processed and
displayed only when the page is being viewed directly, not included.

Possible applications are:
* Categorising templates
* Interlanguage links to similar templates in other languages
* Explanatory text about how to use the template

The converse is <code><nowiki><includeonly></nowiki></code>. Text between <code><nowiki><includeonly></nowiki></code> and
<code><nowiki></includeonly></nowiki></code> will be processed and displayed only when the page is
being included. The obvious application is to add all pages containing a given template to a [[Help:Categories|category]], without putting the template itself into that category.

'''Note:''' when you change the categories applied by a template, the categorization of the pages that use that template may not be updated until some time later: this is handled by the {{mediawiki|Manual:Job_queue|job queue}}.

==Organizing templates==
For templates to be effective users need to find them and be able to use them. A simple technique is to include an example on the template page.
For example:
<div style="display:table; width:auto;"><pre>
<noinclude>
==Usage==
Allows to establish a link to a subject:
{{NameOfTemplate|Term1+Term2+Term3}}
</noinclude>
</pre></div>

Then, an editor can simply copy and paste the example to create a similar page.

==See Also==
*[[Help:External searches]] -- a template special use case example
*[[Help:Magic words]] -- fancy stuff you may find in some templates
*{{mediawiki|meta:Help:Embed page}} -- embedding pages from {{mediawiki|namespace|namespaces}} other than <code>Template:</code>.

[[Category:Help|{{PAGENAME}}]]
[[Category:Template]]
{{Languages|Help:Templates}}
[[Category:Imported help]]