__NOTOC__

== Summary ==

A Wind object that was given a name can be controlled by scripts.

== Instances ==
A <tt>Wind</tt> is instantiated by a definition in the level file. It can be accessed by scripts using its <tt>name</tt> and from the console as <tt>sector.''name''</tt>.

=== Example ===

Example of a definition:
<pre>
(wind
  (name "WIND1")
  (blowing #f)
  (speed-x 0)
  (speed-y -600)
  (acceleration 3)
  (width 32)
  (height 64)
  (x 783)
  (y 768)
)
</pre>

The above object will be exposed under the name WIND1 in the scripting engine. Example usage:

<pre>
WIND1.start();
</pre>

Console access:
<pre>
sector.WIND1.stop()
</pre>

== Methods ==
{| class="objectlist"
! class="method"| start()
| start blowing
|-
! class="method"| stop()
| stop blowing
|}

== Constants ==

None

{{Navbox Scripting reference}}
[[Category:Scripting Reference]]