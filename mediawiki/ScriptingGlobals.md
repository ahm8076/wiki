= Summary =
This module contains global constants and methods.

= Methods =
{| class="objectlist"
! class="method"| display(*** object)
| Displays the string value of <tt>object</tt> in the [[Console]]. Object can be of any data type.
|-
! class="method"| print_stacktrace()
| Displays contents of the current stack.
|-
! class="method"| load_worldmap(string filename)
| Loads and runs the worldmap specified in <tt>filename</tt>. (The path is relative to the data root.)
|-
! class="method"| load_level(string filename)
| Loads and runs the level specified in <tt>filename</tt>. (The path is relative to the data root.)
|-
! class="method"| get_current_thread()
| Returns the currently running thread.
|-
! class="method"| display_text_file(string filename)
| Displays the SuperTux text file named <tt>filename</tt>. (The path is relative to the data root, e.g. "/home/joe/src/supertux-trunk/data") See also: SuperTux file format reference, SuperTux texts
|-
! class="method"| wait(float time)
| Pauses execution of the Squirrel code for <tt>time</tt> seconds.
|-
! class="method"| wait_for_screenswitch()
| Pauses execution of the Squirrel code until a new screen is displayed (e.g. menu &rarr; worldmap or worldmap &rarr; level).
|-
! class="method"| exit_screen()
| Exits the current screen, returning to the previous one or, if the active screen is the last one, exiting SuperTux.
|-
! class="method"| fadeout_screen(float seconds)
| Does a fadeout for the specified number of seconds before next screenchange.
|-
! class="method"| shrink_screen(float dest_x, float dest_y, float seconds)
| Does a shrinking fade towards the destposition for the specified number of seconds before next screenchange.
|-
! class="method"| translate(string text)
| Returns: translated <tt>string</tt>. Translates <tt>text</tt> into the user's locale. Note: This construct is unfortunately not yet recognized by XGetText, so translation files have to be written manually.
|-
! class="method"| import(string filename)
| Imports and runs the Squirrel script <tt>filename</tt>. (The path is relative to the data root.)
|-
! class="method"| save_state()
| Dumps the current state into the user's save game file.
|-
! class="method"| update_worldmap()
| Update worldmap from worldmap state (state.world variable)
|-
! class="method"| play_music(string musicfile)
| Changes music to musicfile
|-
! class="method"| play_sound(string soundfile)
| Plays a soundfile
|-
! class="method"| debug_collrects(bool enable)
| Enables or disables drawing of collision rectangles.
|-
! class="method"| debug_show_fps(bool enable)
| Enables or disables drawing of the FPS. (Also affects config file)
|-
! class="method"| debug_draw_solids_only(bool enable)
| When enabled, only draws solid tilemaps. (No background/foreground tiles)
|-
! class="method"| set_game_speed(float speed)
| Set speed to run the game at. (Doesn't affect menus/gui)
|-
! class="method"| grease()
| Speeds Tux's horizontal velocity by a factor of 3.
|-
! class="method"| ghost()
| Makes Tux a ghost, letting him float around and through objects.
|-
! class="method"| invincible()
| Make Tux invincible for 10000 units of game time.
|-
! class="method"| mortal()
| Recall Tux's invincibility or ghost status. (Even when not given with above 2 commands)
|-
! class="method"| restart()
| Reinitialize and respawn Tux at the beginning of the current level.
|-
! class="method"| whereami()
| Print out Tux's coordinates to the console.
|-
! class="method"| gotoend()
| Moves Tux horizontally 2 screens away from the end.
|-
! class="method"| camera()
| Display the current camera's coordinates. (top-left corner)
|-
! class="method"| quit()
| Exits the game. (Not recommended for use in levels!)
|-
! class="method"| int rand()
| Returns a random evenly-distributed integer between 0 and 2147483647, inclusive.
|-
! class="method"| record_demo(string filename)
| Record a demo to the given file.
|-
! class="method"| play_demo(string filename)
| Play back a demo from the given file.
|}

= Constants =

{| class="objectlist"
! class="method"| ANCHOR_TOP
| represents the top center anchor point of a rectangle
|-
! class="method"| ANCHOR_BOTTOM
| represents the bottom center anchor point of a rectangle
|-
! class="method"| ANCHOR_LEFT
| represents the left anchor point of a rectangle
|-
! class="method"| ANCHOR_RIGHT
| represents the right anchor point of a rectangle
|-
! class="method"| ANCHOR_MIDDLE
| represents the middle anchor point of a rectangle
|-
! class="method"| ANCHOR_TOP_LEFT
| represents the top left anchor point of a rectangle
|-
! class="method"| ANCHOR_TOP_RIGHT
| represents the top right anchor point of a rectangle
|-
! class="method"| ANCHOR_BOTTOM_LEFT
| represents the bottom left anchor point of a rectangle
|-
! class="method"| ANCHOR_BOTTOM_RIGHT
| represents the bottom right anchor point of a rectangle
|}

{{Navbox Scripting reference}}
[[Category:Scripting Reference]]