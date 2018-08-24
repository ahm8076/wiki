<includeonly>|-
| {{#if: {{{Screenshot|}}}
    | [[Image:{{{Screenshot}}}|100px|Screenshot of level {{{Name}}}]]
    | {{#ifexist: Image:{{{Name}}}.png
        | [[Image:{{{Name}}}.png|100px|Screenshot of level {{{Name}}}]]
        | ''Not available''<br /><small>[[Media:{{{Name}}}.png|(Add&nbsp;…)]]</small>
    }}
  }}
| '''{{{Name}}}'''<br /><!--
-->{{#if: {{{Description|}}}
     | {{{Description}}}
     | ''No description available.''
   }}
| {{#if: {{{Difficulty|}}}
    | {{Difficulty | {{{Difficulty}}} }}
    | ''unknown''
  }}
| {{#if: {{{Length|}}}
    | {{Level length | 1={{{Length}}} }} <!-- hack: only strings to named arguments are trimmed (leading and trailing whitespace is removed. -->
    | ''unknown''
  }}
| {{#if: {{{Contributor|}}} | {{{Contributor}}} | [[Team|''SuperTux'' team]] }}</includeonly><noinclude>The '''Level list entry''' template inserts information about a level into a level listing.

== Usage ==

 <nowiki>{{</nowiki>Level list entry
   | Name=''name_of_level''
   | Description=''description''
   | Contributor=''name_of_contributor''  &lt;!-- (optional; default: ''SuperTux'' team) --&gt;
   | Screenshot=''screenshot.png''        &lt;!-- (optional; default: ''Name''.png) --&gt;
   | Difficulty=easy|medium|hard      &lt;!-- (optional) --&gt;
   | Length=''n tiles''                   &lt;!-- (optional) --&gt;
 <nowiki>}}</nowiki>

== See also ==

* [[Template:Level list begin]]
* [[Template:Level list end]]

[[Category:Templates]]
</noinclude>