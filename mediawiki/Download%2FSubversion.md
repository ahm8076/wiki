'''The Subversion (SVN) repository is no longer in use.  For the most recent code under development see the [[Download/Git | Git repository]] instead.'''


----

== Repository ==
SuperTux development is coordinated with the help of the Subversion version control system. In a nutshell, it's a file-storing facility that can be used by multiple users simultaneously, keeping track of changes and archiving old versions of files. You can find out more about Subversion in general on their [http://subversion.apache.org/ homepage].

== Getting the data (anonymous read-only access) ==
Anonymous read access to the repository is granted to everybody. Once you have installed Subversion, all you have to do to get your hands on the data is to use the following command:

 <nowiki>svn checkout http://supertux.lethargik.org/svn/supertux/trunk/supertux</nowiki>

This will create a new directory named ''supertux'' which contains the latest versions of the SuperTux source code and data. Once this is complete, you can use

 svn update

inside the ''supertux'' directory to update to the latest version in the repository. This will only download changed files to save bandwidth.

=== Locations inside the Subversion repository ===

Checking out the path above will get you all you need to contribute to SuperTux. However, if you don't want to check out the entire repository, you can just check out the pieces you need. For example, the media directory is notably large and it only necessary if you are working on sounds or graphics.
{|
||'''<tt><nowiki>http://supertux.lethargik.org/svn/supertux/trunk/htdocs</nowiki></tt>'''
|Website source
|-
||'''<tt><nowiki>http://supertux.lethargik.org/svn/supertux/trunk/media</nowiki></tt>'''
|Additional media files, including source files for audio and graphics
|-
||'''<tt><nowiki>http://supertux.lethargik.org/svn/supertux/trunk/supertux</nowiki></tt>'''
|Latest SuperTux source
|-
||'''<tt><nowiki>http://supertux.lethargik.org/svn/supertux/trunk/supertux-milestone1</nowiki></tt>'''
|SuperTux Milestone 1 source
|-
||'''<tt><nowiki>http://supertux.lethargik.org/svn/supertux/trunk/supertux-portable</nowiki></tt>'''
|[[SuperTux Portable]]
|-
||'''<tt><nowiki>http://supertux.lethargik.org/svn/supertux/trunk/supertux-editor</nowiki></tt>'''
|Official SuperTux level editor that runs under both Mono and MS .NET.
|-
||'''<tt><nowiki>http://supertux.lethargik.org/svn/supertux/branches/supertux/0_3_x</nowiki></tt>'''
|SuperTux [[Milestone 1.9]] branch
|}

== Creating Patches ==

There's a whole section about [[Contributing#Programmers/Code|creating patches]].

== Web Access ==
If you just want to browse through the source a bit, then you can use the [http://supertux.lethargik.org/viewvc/viewvc.cgi/trunk/supertux/ Repository HTTP Interface] which should work well with your web browser.

== Developer SVN access ==

If you have submitted some good patches and want to get actively involved in the SuperTux project, [[SuperTux FAQ#How can I get in touch with you.3F|contact]] us for write access to the repository. You will then have to issue the following command in the ''supertux'' directory:

<pre>svn switch --relocate http://supertux.lethargik.org/svn/supertux/trunk/supertux \
  svn+ssh://&lt;your_lethargik_username&gt;@lethargik.org/home/supertux/svn/supertux/trunk/supertux</pre>

After running an <code>svn update</code> to make sure everything went smoothly, you can start checking in your changes:

 svn commit -m "Totally changed src/main.cpp to implement HTCPCP!"

If you only want to commit changes to some files, add their names to the end of the command.

=== Move from BerliOS ===
Contact [http://supertux.lethargik.org/bugs/view.php?id=8#32 sik0fewl] to get developer access if you used to have it on BerliOS. Also sik0fewl is responsible for adding new developers (but other developers have to agree with it first).

When switching to the new SVN from BerliOS (using <code>switch --relocate</code>) make sure to be on revision 4542 - '''NOT''' any later revision (else you will get a checksum error). You can use <code>svn update -r4542</code> to downgrade.

== Ubuntu Repository ==
An Ubuntu repository for the SVN version of SuperTux exists as a [https://launchpad.net/~stownsend42/+archive/supertux-svn Launchpad PPA] To install SuperTux from this repository, add ppa:stownsend42/supertux-svn to your Software Sources, then install the supertux-svn package. At this time, new packages are only being built for lucid (10.04) and maverick (10.10).

NOTE: THIS REPOSITORY IS NO LONGER MAINTAINED. NO NEW BUILDS WILL BE UPLOADED.

If anyone else would like to take up this project, please feel free to do so. If you need help, contact me at stownsend42@sbcglobal.net

== Debian Repository ==
First add the public key to authenticate the repository by running the following:
 <code><nowiki>wget -q https://supertux.lethargik.org/apt/supertux.key -O- | sudo apt-key add -</nowiki></code>

Then add the following to your repository sources (/etc/apt/sources.list or your favorite editor)
 <code><nowiki>deb http://supertux.lethargik.org/apt VERSION contrib</nowiki></code>
Replace VERSION with your Debian version, e.g. lenny/squeeze/sid or stable/testing/unstable.

Finally, install the "supertux-svn" package.

== Gentoo Linux ==
If you have any problems with supertux on [http://gentoo.org/ Gentoo] or trouble understanding the instructions below, please contact <tt>binki</tt> on [[Contact#IRC|<tt>#supertux</tt>]]. He'll be glad to help if he can and to know that his ebuilds are useful ;-).

=== Get the Overlays ===

To install the latest and greatest development versions of supertux and supertux-editor, please grab [http://ohnopub.net/~ohnobinki/gentoo#overlay my overlay]. It includes a few other things than the live supertux ebuild, but if you're not running ~arch (you'll know if you are) this shouldn't affect your Gentoo installation. If you have any issues with the overlay itself, just contact <tt>binki</tt> or [https://ohnopub.net/bugzilla/enter_bug.cgi?product=ohnobinki_overlay file a bug]. To install my overlay, first set up layman. Make sure that the <code>subversion</code> and <code>mercurial</code> useflags are set in <code>/etc/make.conf</code> before emerging layman:

 <code><nowiki>emerge -va layman</nowiki></code>

After layman is installed, it should print out instructions for modifying your <code>make.conf</code>. This will enable portage to see ebuilds in layman-managed overlays. Recent versions of layman will suggest to add something lik the following to <code>make.conf</code>:

 <code><nowiki>source /var/lib/layman/make.conf</nowiki></code>

Then, install the overlays. SuperTux and its dependencies are spread between my overlay and the somewhat more official [http://overlays.gentoo.org/proj/sunrise Sunrise User Overlay].

 <code><nowiki>layman -f -a ohnobinki -a sunrise</nowiki></code>

=== Unmask and Emerge ===

Then, add the necessary package (dependencies of supertux and supertux itself) to <code>/etc/portage/package.keywords</code>. If <code>package.keywords</code> doesn't exist, you may create it in <code>/etc/portage</code>. Deposit the following lines into this file:

 <code><nowiki>dev-libs/findlocale
dev-libs/tinygettext
games-arcade/supertux
dev-games/supertux-editor</nowiki></code>

Now just emerge supertux and/or supertux-editor :-)

 <code><nowiki>emerge -va supertux supertux-editor</nowiki></code>

If you are brave and want builds straight from SVN, place <code>**</code> after the supertux and supertux-editor packages in <code>package.keywords</code>:

 <code><nowiki>games-arcade/supertux **
dev-games/supertux-editor **</nowiki></code>

===Getting the SVN for mac===

I have provided a link to download packaged SVN builds for mac: [[Download/Supertux SVN Version Mac]] [[User:Monster|Monstertux]] 21:03, 13 April 2011 (UTC)

[[Category:Development]]
[[Category:Meta]]
[[Category:SuperTux]]