This page describes the new versioning scheme that will be used for SuperTux.

== The scheme ==

=== SuperTux ===

Releases will have the form of <tt>x.y.z</tt>.

* <tt>x</tt> is increased only when there is a ''major'' update or we reach a ''major'' milestone. When <tt>x</tt> is increased, <tt>y</tt> and <tt>z</tt> are reset to <tt>0</tt>
* <tt>y</tt> is increased for each new regular, planned released. When <tt>y</tt> is increased, <tt>z</tt> is reset to <tt>0</tt>. Odd versions of <tt>y</tt> indicate a ''development branch''. Even versions of <tt>y</tt> indicate a ''stable branch''.
* <tt>z</tt> is increased when there is a bugfix release or minor changes are made, such as a couple new features and new content (eg, new worlds or levels). For development branches, bigger changes are more likely to make it into <tt>z</tt>-releases.

The development branches are used to work our way to a stable release. For example, the <tt>0.3.x</tt> will be used to create a stable <tt>0.4.0</tt> ([[Milestone 2]]) release.

While development releases are likely to be stable, they are more likely to receive less testing before a release, so we cannot guarantee their stability.

As a rule, <tt>z</tt>-releases cannot break level editor functionality in stable branches. For development branches you should check the wiki to make sure your version of the SuperTux Editor works with your version of SuperTux. To be sure, if you are using the development branch you should always be using the latest version of both SuperTux and the SuperTux Editor.

=== SuperTux Editor ===

Releases will have the form of <tt>x.y.z</tt>.

* <tt>x</tt> and <tt>y</tt> will match the <tt>x</tt> and <tt>y</tt> of the SuperTux release the editor works for.
* <tt>z</tt> is increased when there is a bugfix release or minor changes made to the editor. This number does not necessarily match up with the <tt>z</tt> of the SuperTux release.

=== Brown-paper-bag releases ===

A fourth decimal point number <tt>n</tt>, of the form <tt>x.y.z.n</tt>, will be used for [http://www.answers.com/topic/brown-paper-bag-bug-computer-jargon brown-paper-bag] releases. Hopefully we never need to use this.

== Release branches ==

=== <tt>0.1.x</tt> releases ===

This is the [[Milestone 1]] branch.

The <tt>0.1.x</tt> releases do not follow the current versioning scheme. <tt>0.1.x</tt> is considered a ''stable branch''.

=== <tt>0.2.x</tt> releases ===

There will not be any <tt>0.2.x</tt> releases.

=== <tt>0.3.x</tt> releases ===

The <tt>0.3.x</tt> branch is being used to develop SuperTux 0.4.0. It is implementing the [[Milestone 1.9]] and [[Milestone 2 Design Document|Milestone 2]] goals.

There will be no <tt>0.3.2</tt> release. There were some unofficial releases of SuperTux incorrectly labelled as version <tt>0.3.2</tt> so in order to avoid confusion there will be no official <tt>0.3.2</tt> release.

=== <tt>0.4.x</tt> releases ===

SuperTux 0.4.0 will be the next stable ([[Milestone 2]]) release.

=== <tt>SVN</tt> "releases" ===

SVN builds will have version numbers of the form <tt>x.y.z-SVN</tt> with an optional version specifier at the end. <tt>x.y.z</tt> will be the latest unstable release, and the version specifier will be the result of running <code>svnversion</code>.

[[Category:Developer documentation]]