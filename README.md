# Keybinder

This Firefox add-on allows the user to customize various shortcuts, as well as completely disable the ones he doesn't like.
It is based (and a large part of the code) was originally written by Tim Taubert for the "Customizable Shortcuts" add-on that can be found here: https://addons.mozilla.org/en-US/firefox/addon/customizable-shortcuts/
After much work and, at one point trying to contribute to the original project but being unable to reconcile all the changes I made with the original author, I decided to release my own branch of the extension.

- Version: 1.1.1
- Date: 2014-09-16
- Official site: <https://github.com/Lord-Kamina/keybinder>

## Changes
#### Version 1.1.1
* Multiple bug fixes
	- Fixed bug when opening the shortcut dialog when already open; now, it focuses the window instead of trying to recreate it.
	- Same thing for URL patterns in the extension manager.
	- Clean-up script wasn't getting rid of menu items, fixed that.
	- Prevent the extension from adding redundant menu items.
	- Fixed odd bug whereby pressing dead keys (and some punctuation) would prevent them from working.

#### Version 1.1
* Renamed Extension and changed icon.
* As per the original add-on, changed to MPL 2.0.
* Improved the flexibility and robustness of the content-scripts
	- Added sanity checks and a more robust interface for adding URLS to be scanned for plugins.
	- Improved the code and handling of workers.
	- Make sure they actually get removed once they're not being used anymore.
	- All changes to settings should now be applied immediately to open pages, as soon as they are made.

#### Version 1.0
* Moved config to it's own dialog, under Tools Menus.
* Detects, color codes and warns conflicting shortcuts.
* Added supports for a few of the shortcuts with no ID.
* Fixed the configuration dialog search.
* Prevent the extension from mapping unknown non-US keys to shortcuts (tildes, accents, etc.)
* Added Private-Browsing support (although, to make sure we don't write to disk during Private Browsing, the Tools menu will only display the addon on non-Private windows)
* Added work-around for bug 78414.
* Added work-around for bug 406199.
* The extension should now be localizable.
* Several other minor changes and fixed from the original extension.

# TO DO
* Find alternative to the deprecated "window-utils" API; so far a suitable replacement has not come forth.

## License

Keybinder is licensed under the terms of MPL 2.0
