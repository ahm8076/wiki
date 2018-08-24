{{Navbox Milestone 2 Design Document}}
__TOC__

This document is meant to give a reasonably detailed guide on what shall and shall not happen in Milestone&nbsp;2. It is also intended as a complete replacement of other, incomplete or otherwise flawed, Milestone&nbsp;2 documents floating around in this Wiki. This design document is written by [[User:Grumbel|Grumbel]], question and comments are welcome, use the [[Talk:Milestone 2 Design Document|talk page]] or the [[IRC]] channel for that. At the moment this document is a work-in-progress, meaning goals might change as time progresses. This document has not yet been approved by any other member of the ''SuperTux'' [[Team|development staff]].

= Motivation = 

Development of the forest world hasn't made much progress over the last few years. Milestone&nbsp;2 is a try to bring development back up to speed by setting more reasonable goals and by cutting out a lot of allocated cruft, reducing the game back to a maintainable state that allows further development. This means the [[Forest|forest world]] will be cut out completely and focus will be given to the [[Iceworld]] of [[Milestone 1]]. The core goals of Milestone 2 are:

* cleanup the engine and fix long standing issues (broken OpenGL texturing, broken collision detection, etc)
* enhance and adopt the levels of [[Milestone 1]] to use new engine features
* stabilize the engine to the point that new stable released can be rolled out much faster
* create a polished boss fight

Optional goals (might wait for [[Milestone 3]]):

* create new levels, tile sets and enemies

The Milestone 2 Design Document lists a lot of additional features for the iceworld, which should maybe wait till the next release.

= General =

* uni-solid tiles shall be provided for all tilesets
*: Should the graphics of unisolid tiles differ from those of solid tiles? If not, using invisible unisolid tiles in the interactive tilemap and solid tiles in a non-solid background tilemap works just as well and doesn't duplicate tiles a hundredfold. --[[User:Octo|octo]] 07:06, 2 March 2010 (UTC)
* multi-layer parallax scrolling background tilemaps shall be used in all levels
* menu system should be replaced/reworked
* save system could need a rework as well
* language shall be changeable via the option menu, LANG environment variable shall only be used as default setting
*: I think this is how it is currently behaving, isn't it? --[[User:Octo|octo]] 07:06, 2 March 2010 (UTC)
* worldmap Tux sprite should get animations for left, right, up, down directions, not just a single one as now

= Levels = 

The levels of Milestone1 lack verticality as well as unisolid tiles, Milestone2 should fix that by adding those elements. Also the levels should be shortened/split to avoid the need for reset points. Another important point is that each level should try follow a clear design premise instead of being more or less random collection of tiles and enemies. The levels from Milestone1 should be taken as a point of inspiration and starting point, not as something that is verbatim copied over to Milestone2. 

The ''worldmap'' should be rolled back to that of [[Milestone 1]], i.e. a mostly linear map, but additional optional paths shall be added.
: This has been done in {{Revision|6424}} and is included in this form in ''version 0.3.3''. The only additional path is to the bonus level, though. --[[User:Octo|octo]] 07:12, 2 March 2010 (UTC)

See [[Milestone 2 Design Document/Levels]] for a more detailed analysis of the current levels.

== Cleanup ==

The test/ levels are currently quite a big mess, there needs to be cleanup to reduce them to those that are really needed otherwise its to easy to miss the ones that are important.
: [[User:Mathnerd314|Mathnerd314]] has cleaned up test levels a bit in {{Revision|6477}}. --[[User:Octo|octo]] 07:09, 2 March 2010 (UTC)

= World 1 - Icyisland =

World 1, the icyisland, was released with Milestone 1, the intend of Milestone 2 is to adapt it to the new engine features as well as improving it by adding new enemies and new gameplay elements. While level structure might be recyclable in many places, it will often need structural improvements to provide real use of vertical and horizontal scrolling, instead of just locking the player in a horizontal-only scrolling level. Things that need to be done:
[[Image:Newpipe_blue.png|thumbnail|right|New Pipe Variations]]
* Jumpy shall be replaced with an enemy that fits better into the snow landscape, Jumpy himself shall be reused in a lava-like setting or in the bosses castle
*: Are you referring to the old ''Milestone 1'' jumpy? The current snowball-with-a-spring look fits the snowy landscape well, IMHO. --[[User:Octo|octo]] 07:18, 2 March 2010 (UTC)
* the walrus salesmen shall be added to the island
* some levels shall be separated out into optional paths, to provide a less linear path
* iceblocks which will melt on contact with fire shall allow to lock paths in a level or lock secrets
*: Code is there, see [[weak block]]s. Needs graphics to fit into [[Icy Island]]. --[[User:Octo|octo]] 07:18, 2 March 2010 (UTC)
* balanced platforms that start to rotate or move when Tux stands on them shall be provided
* water, in its simplistic tile form, shall be removed from all levels
* uni-solid/half-tiles shall be used to enhance the levels and provide optional paths
* bottom-less pits shall be either replaced by pits with spike at the bottom or allow Tux to climb back out of the pit

* there shall be auto-scrolling levels that force Tux to run by having a avalanche coming down behind him, the avalanche might either be simple snow or a large group of enemies
* the castle tileset shall be replaced with something that looks colder and features both snow and ice
* cave tileset shall be replaced with something that has a larger pattern, thus looks less ugly when tiled
* tiles picturing deadly spikes build out of ice shall be created

<br clear="all" />

= Intro/Credits =
[[Image:Introcutscene.png|thumbnail|left|Intro Storyboard]]
The text based intro and credits shall be replaced with cutscenes, showing the events that are described in the text. Instead of auto-scrolling text the game shall provide text that doesn't scroll, but instead only continues up on user interaction (i.e. press action button to see the next page of text). Text in cutscenes shall get printed letter by letter to the screen to provide a sense of 'motion'. Voice over from a story-teller might be consideration, while Tux, Penny and Nolok itself shall remain without speech.

'''Later in the development of Milestone2'''

<br clear="all"/>

= Things to know =

* {{SvnFile|data/levels/test/unisolid.stl}} shows a few new features of Milestone&nbsp;2 (parallax scrolling, unisolid snow tiles, new water)
* [[News]] is there to be used, so if something interesting happens, write it down there

[[Category:Development]]