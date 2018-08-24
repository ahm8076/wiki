<includeonly>{{#ifeq: {{{Value|}}} | yes
 | style="background: #e0ffe0; color: #006000;" {{!}} {{#if: {{{Text|}}} | {{{Text}}} | yes}}
   {{#if: {{{YesCategory}}} | [[Category:{{{YesCategory}}}]]}}
 | {{#ifeq: {{{Value|}}} | no
    | style="background: #ffe0e0; color: #600000;" {{!}} {{#if: {{{Text|}}} | {{{Text}}} | no}}
      {{#if: {{{NoCategory}}} | [[Category:{{{NoCategory}}}]]}}
    | style="background: #e0e0e0; color: #000000;" {{!}} {{#if: {{{Value|}}} | {{{Value}}} | ''unknown''}}
      {{#if: {{{UnknownCategory}}} | [[Category:{{{UnknownCategory}}}]]}}
   }}
}}</includeonly><noinclude>Adds a colored table cell. The color of the cell depends on the ''Value'' argument which can be either "yes" or "no". If it is neither, "unknown" is assumed. This template is meant to be used in more specialized templates.

== Usage ==

 <nowiki>{{TableCell YesNoUnknown</nowiki>
 | Value=yes
 | Text=this is true
 | YesCategory=Pages which are true
 | NoCategory=Pages which are false
 | UnknownCategory=Schroedinger's pages
 <nowiki>}}</nowiki>
</noinclude>