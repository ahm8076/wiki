== SVN Version ==

* After Starting supertux CPU usage is 100% and mouse and keyboard aren't working in SuperTux. OpenAL reports that it couldn't open /dev/snd. If you are using dmix with ALSA add this to ~/.openalrc
 (define devices '(alsa))
 (define alsa-out-device "output")
 (define sampling-rate 44100)
 (define speaker-num 2)

After this SuperTux should work as normal. And you can now play all other games that uses OpenAL while you are listening to the music.
credits for this solution goes to Matze Braun.

== OpenAL ==

By default OpenAL uses OSS output. On modern systems OSS is emulated by ALSA anyway, so usually using
ALSA directly sounds better. Create ~/.openalrc:

 (define devices '(alsa))
 (define speaker-num 2)
 (define alsa-out-device default)

=== strange ./configure error ===

If ./configure bails out with
"configure: error: /bin/sh mk/autoconf/config.sub i686-pc-linux-oldld failed"
this will most probably mean you forgot to install g++ (hence -oldld instead of -gnu). Install (a recent version of) g++ and you're good to go.

[[Category:Developer documentation]]