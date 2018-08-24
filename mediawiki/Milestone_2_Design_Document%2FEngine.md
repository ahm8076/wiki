{{Navbox Milestone 2 Design Document}}
= Screensize/Aspect-Ratio =

Milestone2 will allow near total freedom in setting the screensize and the size of the projected area:

 ./supertux -g 1280x1024:1680x1050

This command for example will give a Window of 1280x1024, but with the visible area of a level being 1680x1050.

This means that level design must not focus on 800x600, but should be flexible enough even when the user has a much larger visible area. However all levels should remain playable even as low as 640x480.

The maximum resolution to deal with is 1920x1200 (HD-TV Monitor), 2560x1600 (Apple 30" Cinema Display) can't be handled since that would cause issues with enemy respawning, the respawn distance is currently 1600x1200, relative to Tux.

Maximum resolution might be limited to 1280x800, with everything larger getting upscaled.

* with a windows larger then 1280x800 the content will be scaled up, letter boxes will be used where useful
* with a window between 640x480-1280x800 the visible playfield will resize
* with a window smaller then 640x480 the content will be scaled down

== Questions ==

Might 1280x1024 be a better choice then 1280x800, as its a common LCD resolution?
: Maybe, if levels would have build in verticallity, at the moment they are just scaled to 25 tiles, which isn't enough for 1024, thus letterboxing. -- [[User:Grumbel|Grumbel]] 11:11, 26 February 2010 (UTC)

[[Category:Development]]