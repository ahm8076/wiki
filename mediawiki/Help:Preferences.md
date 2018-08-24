{{PD Help Page}}

Clicking on the [[Special:preferences|my preferences]] link in the upper right while logged in allows you to change your preferences. You will be presented with the User profile section, as well as a bar of tabs across the top for changing other types of settings.

==User profile==
===User profile===
* ''Username'': Your user name. Only bureaucrats can change your username, and the wiki must also have the {{mediawiki|Extension:Renameuser|Renameuser extension}} installed.
* ''User ID'': A number assigned to your account when you created it (for example, if your number is 42 you are the 42nd user to sign up at this particular wiki). This number is used for internal purposes.
* ''Number of edits'': How many edits you have made. Not all wikis will have this.
* ''Real name'': If provided, this will be used for attribution (rather than using your username). Providing your real name is entirely optional. Some wikis do not have this option.
* ''E-mail'': Your email address, if you have supplied one. You can also change or remove your address here.
* ''Nickname'': When you sign your name (using <code><nowiki>~~~~</nowiki></code>), what you enter here will be used at the start instead of a simple link to your user page. By default, anything you enter here will be wrapped with <code><nowiki>[[ ]]</nowiki></code>; if you want to use special linking, enable ''Raw signatures (without automatic link)''.
* ''Language'': This controls what language the interface is displayed in.  MediaWiki's default interface includes localisations for all supported languages, but this is not necessarily the case with extensions or custom skins. Page text will '''not''' be translated, nor will templates (unless the templates integrate text localisation).

===Change password===
To change your password, enter your old password in the first box and your new password in the last two. If you want this site to remember your login, check ''Remember my login on this computer''. Note that this function requires you to have cookies enabled in your browser, and if your cookie is cleared or expires you will no longer be remembered.

===E-mail===
If you have supplied an email address, you will need to click the ''verify address'' button in order to use these functions. You will receive an email; simply open it and follow the link to enable the following functions.

* ''E-mail me when a page I'm watching is changed''
* ''E-mail me when my user talk page is changed''
* ''E-mail me also for minor edits of pages''
* ''Enable e-mail from other users''
* ''Send me copies of emails I send to other users''

===Languages===

From your preferences you can select what language you would like the interface to be in. Only the buttons like 'edit' and 'talk', in addition to a few pages in the sidebar, will be affected. The main text of the pages will not be changed by this for the vast majority of pages, although there are a few pages where it will, like some in the Wikimedia Meta Wiki.

==Skin==
Here you can choose the skin you want to use (use ''Preview'' if you want to see a skin before you choose it). By default, MediaWiki includes the following skins:
* Chick
* Classic
* Cologne Blue
* MonoBook (default)
* MySkin
* Nostalgia
* Simple
While you can choose whatever skin you like, bear in mind that some wikis will incorporate templates or layout elements that will not display as intended in some of these skins. Generally speaking, sticking with MonoBook (or whatever the wiki's default skin is) will ensure you see pages as intended.

==Math==
Here you can control how mathematical equations described using the <code><nowiki><math></nowiki></code> tag will be displayed. Mathematical formulae uploaded as images or written outside the math tag will not be affected by this setting.
* ''Always render PNG''
* ''HTML if very simple or else PNG''
* ''HTML if possible or else PNG''
* ''Leave it as TeX (for text browsers)''
* ''Recommended for modern browsers''
* ''MathML if possible (experimental)''

==Files==
Here you can determine how images will be displayed. Images displayed by direct pasting of a URL (if the wiki has it enabled) will not be affected by this setting.

* ''Limit images on image description pages to'': This setting lets you choose how big image previews will be on the Image: pages. If you know what your current screen resolution is you may like to set this to one or two sizes smaller than your own screen. If you have a slow connection (such as dial-up) you may want to limit them to 320×240.
* ''Thumbnail size'': Define how big you want thumbnails to appear. This setting will not affect thumbnails with dimensions determined by an editor, nor can it increase images beyond their original dimensions.

==Date and time==
The following is normally rendered depending on preferences:

<pre>
 [[2001-01-05]] (or [[2001]]-[[01-05]]) (with leading zeros)
 [[2001]] [[January 5]] ([[2001]] [[January 05]])
 [[January 5]], [[2001]] ([[January 05]], [[2001]])
 [[5 January]] [[2001]] ([[05 January]] [[2001]])
 [[January 5]] ([[January 05]])
 [[5 January]] ([[05 January]])
</pre>

==Editing==
Settings to control editing pages, including the size of the edit box displayed and whether to watch pages that you have edited or created automatically.

==Recent changes==
* ''Days to show in recent changes'': Here you can specify how far back the [[Help:Tracking changes|recent changes]] pages will go. Note that the list will stop prematurely if the number of edits is exceeded (see below)
* ''Number of edits to show in recent changes'': Here you can specify how many edits should be displayed.
* ''Hide minor edits in recent changes'': This enables you to hide edits marked as minor (see [[Help:Editing pages]]). Since some users will rapidly make a lot of tiny tweaks to update templates or fix spelling errors you may find enabling this to be useful. You can also turn this on temporarily from the recent changes page (see [[Help:Tracking changes]]).
* ''Enhanced recent changes (JavaScript)'': Enhanced recent changes condenses edits into a per-page list. As indicated, this requires JavaScript to be enabled. See [[Help:Tracking changes]] for more information on this feature.

==Watchlist==
Setting to control the behaviour of the watchlist (See [[Help:Watchlist]]) Most of these options are also available on the watchlist display itself, but by setting them in your preferences you control the default behaviour i.e. Every time you visit the watchlist it will do the same.

==Search==
Default settings for searches including how many results to display and how much context to show for each result.  Check the boxes next to the namespaces which you want to show up, the first time that you search for something.  You can override this when doing an actual search, by checking or unchecking the boxes at the bottom of the search results screen.

''Administrators'': To change the namespace default preferences for new users (or users who haven't changed their preferences yet), see {{mediawiki|Manual:$wgNamespacesToBeSearchedDefault}}

==Misc==
Other settings such as numbering and justification.

== See also ==
* [[Help:Skins]]

{{Languages|Help:Preferences}}

[[Category:Help|Preferences]]
[[Category:Imported help]]