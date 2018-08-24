= Milestone 2 =

Documents and ideas: [[Milestone 2]] esp. [[World 2]]

== Notes ==

{{Attention|s=Only developers should edit this page. Please add [[User ideas]] and [[Bugs]] to the end of their pages}}

Apart from issues listed here, [[:Category:Needs Code]], [[:Category:Needs Sound]] and [[:Category:Needs Graphics]] list articles that describe content which still lacks one of the three. Bugs can be found in our [http://supertux.lethargik.org/bugs bug tracker].


== Game Tasks ==

=== Current ===

==== Integration/Organisation ====
* integrate new bomb sprite, remove the old
* integrate new green pipe
* make list of ugly titles that need replacement
* remove the helper-tiles in levels where enemies should be stay-on-platform

==== Graphics ====
* repaint dead-iceblock
* redraw underground ice tileset
* design a new ice-castle titleset
* design enemies that fit into a ice-castle

==== Coding ====
* make submenus look different then clickable menu items
* implement threading in netbrush-server (needed so that new users don't bring the session to a crawl)
* make lisp reader get(name, bool) handle 0/1 as bool instead of fail
* getting stuck under a tile as large-tux shouldn't harm you, just unstuck you

==== Input ====
* implement wiimote support (easily done with cwiid), should be #ifdef'ed out if library doesn't exit or better dlopen the library at runtime
* check that joystick code works with analogsticks properly and fix where necessary

==== Bugs ====
* german umlauts seem to be broken when switching the language in game
* In special levels, such as ones were tux walks upside down or levels where the camera moves at a constant speed, spawning at a checkpoint causes tux to die immediately. (Mac OS X Version)

=== Future ===

* add paralax scrolling to all levels
* remove old water from levels (bridge levels)

== Editor ==
(The editor is not release critical therefore no ratings for these TODOS)
* Scroll TileList with middle mouse, Get different Tilegroups
*:Isn't that the way it is atm? --[[User:WolfgangB|WolfgangB]] 18:23, 7 Aug 2006 (BST)
*::Only if one tilegroup is selected, with default group (empty string) you can't scroll, once you have set it to "All" or anything else you can. Should be bug (or feature) in GTK, it's not controlled by program.
* Create an overview widget (where to place this in the GUI?)
*: Overview for what? -- [[User:Penma|Penguinmaster]] 15:46, 4 Oct 2006 (CEST)
*::The sector. Like a minimap.
* Grab Mouse Pointer when scrolling so that we can scroll as much as we want (and the mouse is still where it was before scrolling)
*:I don't think that would be a good idea. I at least found that applications that does that are hard to use. --[[User:AnMaster|AnMaster]] 10:46, 13 Nov 2006 (CET)
* More custom property editors:
** Texts
** Scripts (we had a very good gtksourceview based editor which is disabled at the moment, maybe split the editor to a separate dll and load different editors on demand?)
**:Why was it disabled? --[[User:WolfgangB|WolfgangB]] 16:45, 13 Jul 2006 (BST)
**::Because it crash the editor on Windows, and because it add lots of extra deps. --[[User:AnMaster|AnMaster]] 23:27, 20 Jul 2006 (BST)
**:::"lots of extra deps" anything that is not part of every serious distro? Why not fix the crash instead of removing features?
* Layer switching on keys 1,2,3,...,0 CTRL+1,2,3,...,0 to switch visibility, key 0 for objects
* Editor has strange behaviour when you select a tile in the middle, right-click select and move the mouse too much to the right
* Tool not working after loading new level
*:Added a workaround for this by resetting to the Select tool when loading new level. --[[User:AnMaster|AnMaster]] 20:25, 8 Sep 2006 (BST)
* Windows builds seem to silently crash when loading huge levels
*:huge as in 100x100 or more like 10000x10000?
*::the level old world2/airkey.stl crashed both editor and the game itself on windows. --[[User:AnMaster|AnMaster]] 17:56, 30 Jun 2006 (BST)
*:::the old airkey was 300x300. It makes the editor slow on my Linux box but it's working--[[User:WolfgangB|WolfgangB]] 00:14, 6 Jul 2006 (BST)
*::::The editor crashes on windows certainly. It stops also responding very often. I think it's partly windows, wich causes the crash. --[[User:Yaniel|Yaniel]]
* Make the right click menu from sector tab a normal menu so that users can easily find it
*:Maybe add them to a toolbar? that could be useful. --[[User:AnMaster|AnMaster]] 23:27, 20 Jul 2006 (BST)
* Add a new way to copy parts of one level to another.

[[Category:Development]]