The current svn version allows recording of demos. So let's collect some speed runs :)

(Unfortunately the speed runs can only be replayed with the same version of supertux it was recorded with...)

MatzeB (svn version from 2.Mai)
* [http://www.stud.uni-karlsruhe.de/~uxsm/level1_264.demo level 1] (last displayed time 264)
* [http://www.stud.uni-karlsruhe.de/~uxsm/level2_265.demo level 2] (last displayed time 265)
* [http://www.stud.uni-karlsruhe.de/~uxsm/level3_255.demo level 3] (last displayed time 255)
* [http://www.stud.uni-karlsruhe.de/~uxsm/level19.demo level 19] (last displayed time: 238)
* [http://www.stud.uni-karlsruhe.de/~uxsm/level26.demo level 26] (last displayed time: 234)

= How to create Demos =

First note that '''Demos are only available in the development version!''' If you have compiled an svn version yourself, then you can record a demo of level25 like this for example (started from source dir):

  ./supertux --record-demo mydemo.demo data/levels/world1/level25.stl
  supertux.exe --record-demo mydemo.demo data/levels/world1/level25.stl

You can playback a demo like this:

  ./supertux --play-demo mydemo.demo data/levels/world1/level25.stl
  supertux.exe --play-demo mydemo.demo data/levels/world1/level25.stl

[[Category:For Users]]