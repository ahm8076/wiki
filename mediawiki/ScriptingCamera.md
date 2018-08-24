__NOTOC__

== Summary ==
<tt>Camera</tt> is an interface to manipulate the camera.

== Instances ==
An instance named <tt>Camera</tt> (<tt>sector.Camera</tt> in the console) is available. ''(Note: doesn't having a class and an eponymous instance create a potential for conflicts? We should probably rename the instance or the class.)''

The ''mode'' of the camera is either '''normal''' (the camera is following the player) or '''autoscroll'''. In the latter mode the camera is forced along a specified [[ScriptingPath|path]]. The left and right borders of the screen are solid. If the player fails to hold up with the moving camera, [[Tux]] is pushed forward according to the camera movement, possibly squishing him when he is between the border of the screen and other solid objects.

=== Example ===

 (camera
   (mode "autoscroll")
   (path
     (node
       (x 0)
       (y 0)
       (time 250)
     )
     (node
       (x 19072)
       (y 0)
     )
   )
 )

== Methods ==
{| class="objectlist"
! class="method"| shake(float time, float x, float y)
| Shakes camera in the vector specified by x and y.
|-
! class="method"| set_pos(float x, float y)
| Moves the camera to the specified position. Warning: This function has not yet been implemented.
|-
! class="method"| set_mode(string modestring)
| This function sets the camera mode. Valid values for <tt>modestring</tt> are <tt>"normal"</tt> and <tt>"manual"</tt>.
|-
! class="method" style="vertical-align: top"| scroll_to(float x, float y, float time)
| Scrolls the camera to (<tt>x</tt>, <tt>y</tt>) within <tt>time</tt> seconds.
|}

== Constants ==

None

{{Navbox Scripting reference}}
[[Category:Scripting Reference]]