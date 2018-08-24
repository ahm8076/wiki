__NOTOC__

== Summary ==

A [[Thunderstorm]] object that was given a name can be controlled by scripts.

== Instances ==
A <tt>Thunderstorm</tt> is initialised by a definition in the level. It can be accessed via its <tt>name</tt> in scripts and <tt>sector.''name''</tt> in the console.

=== Example ===

Example of a definition:
<pre>
(thunderstorm
  (name "ELIZA")
  (running #f)
)
</pre>

The above object will be exposed under the name ELIZA in the scripting engine. Example usage:

<pre>
ELIZA.thunder();
wait(2);
ELIZA.lightning();
</pre>

In the console:
<pre>
sector.ELIZA.electrify()
</pre>

== Methods ==
{| class="objectlist"
! class="method"| start()
| Start playing thunder and lightning at configured interval
|-
! class="method"| stop()
| Stop playing thunder and lightning at configured interval
|-
! class="method"| thunder()
| Play thunder
|-
! class="method"| lightning()
| Play lightning, i.e. call flash() and electrify()
|-
! class="method"| flash()
| Display a nice flash
|-
! class="method"| electrify()
| Electrify water throughout the whole sector for a short time
|}

== Constants ==

None

{{Navbox Scripting reference}}
[[Category:Scripting Reference]]