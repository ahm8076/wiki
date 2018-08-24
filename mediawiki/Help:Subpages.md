{{PD Help Page}}
'''Subpages''' introduce some hierarchical organisation into wiki page names, with levels of the hierarchy separated by slashes '/'.

=== Namespaces ===
MediaWiki's '''subpage''' feature is turned '''off by default''' in the main namespace, but can be used on [[Help:Talk pages|talk pages]] and [[Help:User page|user pages]]. See [[Help:namespaces]]. In namespaces where the feature is switched off, any slashes (/) within a page name are simply part of the page name and do nothing special.

=== Slashes within a page name ===
Slashes (/) within a page name break the page into parent and subpages, recursively, eg:

:[[Example page]]
:[[Example page/Some sub-page]]
:[[Example page/Some sub-page/Some sub-sub-page]]

A '''link back to parent''' will automatically appear at the top of each subpage. In the case of sub-sub-pages, a set of breadcrumb navigation links will automatically be presented. Note that these links do not appear, however, if the parent page has not yet been created.

=== Using (and over-using) sub pages ===
There are various uses for the subpage mechanism. The main two intended uses are:
* On a [[Help:Talk pages|talk page]] create a subpage (or several) for an archiving of old discussions
* On a [[Help:User page|user page]] create a subpage (or several) to use as a scratchpad editing space.

People instinctively think hierarchically when trying to organise information, so it may be tempting use subpages all the time, however, subpages can be over-used. Remember that having a page name with a slash will generally make the name longer, harder to remember, and thus more difficult to link to. Some people find it more elegant to keep page naming simple. By sticking to a flat naming structure, with a manually maintained web of wiki links, a structure will emerge organically (and this can include a pseudo-hierarchy)

{{Admin tip|tip=Subpages can be activated within the 'main' namespace by adding to the {{mediawiki|Manual:$wgNamespacesWithSubpages|$wgNamespacesWithSubpages}} array.}}

==See also==
* [[Meta:Help:Link#Subpage feature]]
* [[Help:Variables#Page names]]
* {{mediawiki|Manual:$wgNamespacesWithSubpages}}

[[Category:Help|{{PAGENAME}}]]
[[Category:Subpage|{{PAGENAME}}]]

{{languages|Help:Subpages}}
[[Category:Imported help]]