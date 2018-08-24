{{PD Help Page}}

MediaWiki allows you to categorize pages by adding one or more category tags to the text.  Adding these tags create links at the bottom of the article which take you to the list of all pages in that category, which makes it easy to browse related articles.

== How to add categories ==

To add an article to a category put the following at the end of the page you are editing...

 <nowiki>[[Category:NAME]]</nowiki>

where NAME is the name of the category you want to add it to.  Any number of category tags may be added to the page - the page will be listed in all of them.

You can also specify an additional SORT parameter that dictates where the page will appear, alphabetically, within the category. This is achieved by using the following markup:

 <nowiki>[[Category:NAME|SORT]]</nowiki>

So for example, to add this page to the 'Help' category, you would use:

 <nowiki>[[Category:Help|Categories]]</nowiki>

Note that we used 'Categories' as the sort parameter.  Without this the page would be listed under 'H' for 'Help:Categories',  instead of under 'C', which is more useful.  Other situations where you might want to use the sort parameter is when you have articles about people that are titled as <code>FirstName LastName</code> but within the category you want them listed as <code>LastName, FirstName</code>.

Another way to sort the article in the correct letter without the namespace is

 <nowiki>[[Category:Help|{{SUBPAGENAME}}]]</nowiki>

This is extremely helpful when using templates which include a category tag. ...

''Note: the SORT parameter does '''not''' affect how the page title is displayed within the category listing, just how it is ordered.  In the above example, the link to this page will still be 'Help:Categories', and not 'Categories' as you might expect!''

== Linking to Category Pages ==

To create a link to a category page:

 <nowiki>[[:Category:NAME]]</nowiki>

If you were linking to the Category Page for Help on MediaWiki, the link would look like this: [[:Category:Help]]

If you want to display alternate text for the link:

 <nowiki>[[:Category:NAME|TEXT]]</nowiki>

Here is an example of the same link to the Category Page for Help on MediaWiki as above, but with alternative text: [[:Category:Help|MediaWiki Help Index]]

== Categorize Categories==

Categories themselves and other uploaded files like Pictures can be categorized exactly like normal pages. It is useful to connect the article-categories with categories already in place to establish connections and hierarchies. To this end, after saving the article, follow the category links at the end of the page to see, if the category is already in place and if not, categorize them until you connect them with an existing category.

==Moving categories==
Categories cannot be easily moved [[Help:Moving a page|like other pages]]. For this reason, category names should be chosen carefully.

The easiest way (for those with admin privileges) is to create the new page, delete the old one, and then change the tags in each member of the category (manually or with a bot). However, this loses the page history - not a huge problem when categories are used only for navigation, but when a wiki is structured differently and the category pages contain significant amounts of text, this is undesirable.

=== Moving with revision history ===
However, category pages ''can'' be moved together with the full revision history, with some effort, by using the [[Special:Export]] and [[Special:Import]] functions.

{{Languages|Help:Categories}}
[[Category:Help|Categories]]
[[Category:Imported help]]