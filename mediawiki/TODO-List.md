This is a list of tasks and issues that might be worth to implement or
fix. This list is however not an authorative list of things that must
be done, its a collection of random things that pop up during
development, therefore not everything in here might be well thought
out or worth to implement. Use your brain before implementing anything
on this list and always think about how useful a new feature would be
in the context of the whole game or if a potential performance
enhanchment, actually enhanchmes anything at all.

==TODO List as of March of 2015==

===Translation Related Stuff===
*http://supertux.lethargik.org/bugs/view.php?id=106

===Graphic Related Stuff===
*make "downer" lava tiles for the newer lava graphics. WIP by Sydney.
*Iced Cherry bomb graphics are ugly. http://supertux.lethargik.org/bugs/view.php?id=1036 WIP by Sydney
* Stone Tux graphics would be nice. Tobbi and Sydney tried but didn't get far. contact them if you want to see what they have so far. http://supertux.lethargik.org/bugs/view.php?id=1072
* Tree Boss need Graphics improvement.

===Code Related Stuff===
*https://github.com/SuperTuxTeam/supertux/issues/14
*http://supertux.lethargik.org/bugs/view.php?id=1052
*https://github.com/SuperTuxTeam/supertux/issues/24

===Level Related Stuff===
*On going task, always WIP it seems. Mostly fixed though. http://supertux.lethargik.org/bugs/view.php?id=1016
*Add ghost tree level: http://supertux.lethargik.org/bugs/view.php?id=1037


===Editor related Stuff===
*http://supertux.lethargik.org/bugs/view.php?id=1066
*http://supertux.lethargik.org/bugs/view.php?id=1056
*http://supertux.lethargik.org/bugs/view.php?id=1055

===Mailing List stuff===
*http://supertux.lethargik.org/bugs/view.php?id=1073

==OLD TODO LIST==
[[Category:Development]]
==Major Issue==
* Memory leaks : Assigned to Tobbi, fixed soon 
* See if anything is usefull in [[Editor_Ideas]]
* Make any editor working correctly

==Minor Issue==
===Internationalisation===
**Translation  of menu and worlds [https://www.transifex.com/projects/p/supertux/]
**Font improve (needs feed back: arabic and cyrillic) 

===Graphic Tasks===

* make downer tiles of lava flow
* Frozen enemies
* Consolidate/cleanup/organize image files and tilesets
* Find a way to make the menu border work
* A waterfall to match the new water look
* Fix tiling issues
:crystal cave tiles
:brown castle tiles
:some blue castle tiles
:ghostly word
* Fill out some of the new tilesets or remove (e.g. blue mtn.)
* Animate some badguy deaths
* LiveFire final sprite
* Alternative candle sprites (animated background torches, glowing crystals, maybe a brazier/open flame, maybe a light bulb)
* Need parallax versions of backgrounds (in forest)
* Visual effects for willowisp warp and level flip
* Fix Tux graphics ugliness (floating debris outside of Tux and transparent holes inside)
* Replace airarrow with one that is both visible and isn't confusing (maybe a glowing sprite w/o Tux)
* General icons for jump and action buttons, can be used on billboards and in keybinding menu

===Coding Task ===
* Internationalization of add-on
* Improve font support for diacritics 
* Code buttjumpable when frozen for spiky and jumpy
* Code effect of Iceflower on forest badguys 
* Improve fish
:it also looks weird when fish disappears in transparent water
:start of the jump should depend on top of water- i.e. be dynamic for moving water tiles
*the backflip billboard doesn't work if "jump with up" is not selected


===Sound effect===
*Splash effect when falling in water

==Misc.==

From previous TODO list, some point should be rethink, or may have been corrected … 

===Coding Standard Stuff===

* remove overuse of multi-inheritance 
* remove overuse of friend'ship
* maybe mark interfaces as interfaces (ISerializable or SerializableInterface)
* split files with multiple classes into multiple files with one class each
* Decide what to do with magic constants of objects (static vs anonymous namespace vs lisp property)
* check the code with Valgrind and profilers
* use Vector in Physics for 'a' and 'v'
* replace random generator with C++11 stuff
* md5.hpp and random_generator.hpp could go to external/
* write/finish scripts to automatically:
** make all includes relative to top level dir
** sort includes (.hpp file, then system includes, then other project files)
** include guards proper and of the form HEADER_SUPERTUX_${PATH_TO_FILE}_HPP
** remove trailing whitespace

===Suggesions===

* more moving directories around?
**addon/
**audio/	
**control/
**gui/	
**lisp/	
**math/
**physfs/	
**sprite/	
**util/
**video/
**squirrel/ - for generic squirrel code
**supertux/
***worldmap/
***trigger/
***scripting/ - for scripting wrapper code
***badguy/
***object/
* implement a system that allows to attach comments to specific regions in a level
* implement a tool to "screenshot" a complete level
* GameObject::RemoveListenerListEntry: Ughs, somebody trying to implement a list class within in the GameObject?!
* add --datadir DIR (data/) and --userdir DIR (~/.supertux/), allow multiple --datadir's
* make gravity constant-> To be discussed…
* rename Vector -> Vector2f
* get rid of SCREEN_WIDTH/SCREEN_HEIGHT overuse, give them a proper name at least -> to think when upgrading to SDL2
* resolution menu entry moves the wrong way around
* having dictionary_manager in Lisp is extremely ugly
* enforce proper naming of files to match their class (SomeClass -> some_class.?pp or so)
* file naming is inconsistent: some times we use '_' to separate words, sometimes we don't
* implement PNG screenshot
* having hitbox in Sprite is fugly
* add code that compares the last Log line with the current, if they are the same reject them and just output something like:
  ** last line has been repeated X times
* implement: http://standards.freedesktop.org/basedir-spec/basedir-spec-0.6.html
* peaking up/down doesn't work properly
* peaking left/right should make Tux look into that direction (up/down to, needs new sprites)
* cleanup scripting interface
* replace cloud tiles with decals
* add support for automatic scrolling backgrounds
* add direct reading of Vector2f to Reader/lisp
* refactor Camera code, break ugly long functions into pieces and such
* allow fully custom magnification levels from command line (maybe GUI to if there is a proper/easy way to let the user enter numbers)  (--magnification or -g WIDTHxHEIGHT:ASPECTX:ASPECTY@MAGNIFICATION)
* use AnchorPoint in Background instead of Alignment
* allow gradients to parallax scroll like Background (make it optional)
* add multicolored gradients (see Windstille source code, which can deal with Gimp gradients)
* fix alpha blending in the SDL renderer, currently all sprites (Tux, etc.) appear transparent
* shadow font glyphs bleed into other glyphs
* sprite/sprite.cpp: frame should never get out of range:
  if((int)frame >= get_frames() || (int)frame < 0)
    log_warning << "frame out of range: " << (int)frame << "/" << get_frames() << " at " << get_name() << "/" << get_action() << std::endl;
* Surface::hflip() is used exactly once, should probally be part of the constructor

===Scenegraph and Physics Engine Restructuring===

* random idea to restructure engine stuff (might lead to nicer code and easier scriptability (and a need to rewrite lots of stuff...):

    class SomeBadGuy : public PhysicsCallbackListener // or use boost::function
    {
    private:
          PhysicsPtr box;
          SpritePtr sprite;
            
    public:
          SomeBadGuy(Engine& engine)  
          {
             box    = engine.physics().create_box(Rectf(0,0,32,32));
             box->register_listener(this);
             sprite = engine.graphics().create_and_add_sprite("Foobar");
          }
    
          void update(float delta)
          {
             // not much to do, as most stuff is done internally in the engine
             if (dead)
             {
                      sprite->replace_with("Foobar_dead");
             }
             else
             {
                    sprite->hide();
                    sprite->set_pos(box->get_pos());
            }
          }
    
          // no more draw(), done by the scene graph
    
          void on_collision(CollisionData data)
          {
            // respond
          }
    };

==Random Notes==

* calculate the size of an background image that should fill the screen:

  image_size = (1 - parallax_speed) * screen_size + level_size * parallax_speed

 def calc(parallax, screen, tiles):
    return (1 - parallax) * screen + parallax * tiles * 32

Whats the point in adding new features while the existing features and badguys can't be used due to lack of images or animations?

As long as all these points haven't been fixed, Milestone 2 will not be considered as Stable, so won't be released.

== Supported Resolutions ==

SuperTux shall support resolutions from 640x480 to 1280x800 at a magnification of 1x.
For resolutions higher, such as 2560x1600, upscaling will be used.
For resolutions smaller, like 320x240 downscaling will be used.

Higher resolution graphics for 2x maginification might be provided.
Lower res graphics for 0.5x maginification might be provided as well.

Resolution and magnification can be freely configured by the user within the given limits.

In tiles this means we have 40x25 (=1280x800px) tiles per screen.

== Music Recode ==

Currently the music makes up a large chunk of the total tarball
size. Compression could fix this:

   ,-- Size of data/music/*.ogg
   V
 40MB - Current quality in SVN
 24MB - Default oggenc quality (3)
 14MB - oggenc at 0 quality
 10MB - oggenc at -1 quality

No audible difference on my sound setup. -- grumbel