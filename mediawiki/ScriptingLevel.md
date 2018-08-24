__NOTOC__

== Summary ==
The <tt>Level</tt> class provides basic controlling functions for the current level.

== Instances ==
An instance named <tt>Level</tt> is available from scripts and the console. ''(Note: class and eponymous instance might create potential conflicts – the name of one might be changed eventually)''

== Methods ==
{| class="objectlist"
! class="method" style="vertical-align: top"| finish(bool win)
| Ends the current level. If you set <tt>win</tt> to <tt>true</tt>, the level is marked as completed if launched from a worldmap.<br />Tip: Very useful if you have created a frustrating level and want to, at some point, save the player from agony.
|-
! class="method" style="vertical-align: top"| spawn(string sectorname, string spawnpointname)
| Respawns Tux in the sector <tt>sectorname</tt> at the <tt>spawnpointname</tt> spawnpoint.<br />''Exceptions'': If <tt>sectorname</tt> or <tt>spawnpointname</tt> are empty or the specified sector does not exist, the function will bail out first chance it gets. If the specified spawnpoint doesn't exist, Tux will be spawned at the spawnpoint named <tt>main</tt>. If this spawnpoint doesn't exist either, Tux will simply end up at the origin (top-left 0, 0).
|-
! class="method" style="vertical-align: top"| flip_vertically()
| Flips the level vertically (i.e. top is now bottom and vice versa). Call again to revert the effect.<br />Tip: Make sure the player can land on something after the level is flipped!
|-
! class="method" style="vertical-align: top"| toggle_pause()
| Toggle pause
|-
! class="method" style="vertical-align: top"| Level_edit(bool editing)
| Change to/from edit mode
|}

== Constants ==

None

== Example code ==

=== Teleportation ===

The following code teleports the player to [[spawnpoint]] "main" in [[sector]] "underground".

 (scripttrigger
   (script "Level.spawn(\"underground\", \"main\");]]")
   (button #f)
   ...
 )

{{Navbox Scripting reference}}
[[Category:Scripting Reference]]