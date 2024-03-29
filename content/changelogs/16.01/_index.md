---
title: "Version 16.01"
date: 2016-01-28T06:20:22+02:00
draft: false
aliases:
  - /downloads/45
---
For the release 16.01, we provide a top-level changelog hereby about what has changed since 13.12 (to download this or a full change log, links are provided at the bottom of this page):

## Compiler

* Improve compiler detection (e.g. for Intel compiler suite)
* Propgrid based compiler flags dialog
* Support new compilers (BFIN-ELF, LM8-GCC, LM32-GCC, ZPU-GCC...)
* Support resource compiler options
* Support new compiler switches (GCC, MSVC...)
* Correct some regular expressions for compiler settings (i.e. for GCC 5)
* Add support for multi-line error messages, used by e.g. for gfortran
* Make building/cleaning custom makefile projects more verbose
* Detect and show general error (e.g. command line error with clang)
* Fixed several bugs
* Misc. other improvments

## Code Completion

* Tell parser internal threads to abort when project is closed.
* Fixed handling of assignment within for loop
* Fix for function pointer parsing with assignment
* Fixed bug that the * or & sign is removed in the inserted text
* Fixed variable parsing with "=" or "[]"
* Fixed several other bugs
* Fixed document parsing error with doxygen block comment
* Fixed code completion fails with the "using Alias = Type" syntax in C++11
* Fixed code completion fails with function-try blocks
* Fixed code completion ignores parameters of catch-clauses
* Fixed code completion problem with some wx classes
* Fixed a bug that code completion setting don't get saved when C::B closed
* Fixed a bug when handling "##" operator in macro expansion
* Fixed a bug in splitting macro arguments
* Fixed several dead lock and potential crash-candidate issues
* Fixed a bug that we don't get code suggestion list for a function's parameter
* Fix broken colouring for mixed platform projects
* Fix MSVC processor architecture detection for more recent MSVC compilers
* Fix calling package scripts on platforms where these are not supported and may cause a freeze
* Fix handling of struct pointer typedef
* Fix infinite loop when recursive macro expansion reaches max account
* Fix infinite loop when traversing headers and there are loops caused by symlinks
* Avoid scanning for include folders of compilers/project/targets not supported by current platform
* Support access functions belonging to STL containers
* Resolve typedef declarations in class templates
* Handle skip assignment and ternary operator
* Handle template alias, __declspec(xxx) and several other special cases
* Handle stringize operator ('#') when expanding macros
* Added support for "noexcept" while parsing and for doxygen
* Improved parsing support for func ptr
* Improved calltips support for macro and typedef
* Show constructor args in documentation popup and improve constructor call-tips
* Include *.hh, *.hxx and *.h++ for parsing by default
* Use the macro expansion stack, this avoid expanding the used macros
* Support macros in local scope
* Support function pointer arrays
* Code re-factoring for code completion plugin and CCTest
* Remove the macro replacement UI part in the CC's setting dialog (no longer needed)
* Misc. other improvments

## CCManager (new)

* Introduce CCManager (SDK) that allows to work with several code completion plugins easier and to overall simplify code completion plugins
* Enable colour configuration of tooltips
* Allow overloaded call-tip navigation by arrow keys
* Allow tooltips to be shown via only keybindings
* Configuration options for main CC behaviours in one place
* Support asynchronous display of CC documentation popups
* Better support memory of user's selection of dynamic changing overloaded call-tips
* Support multiline calltips
* Show calltips on seperate pages
* **Documentation popup**: Dynamically size width while visible if more space becomes available
* Fix layout of documentation popup on Windows
* Prevent documentation popup from displaying off the edge of the current monitor
* Do not cancel calltip during refresh (reduce flicker)
* Utilize buffered CCTokens for autocomp
* Hide tooltip on scroll
* Handle editor tooltips

## Debugger

* Fix issue with watches window column auto-sizing
* Better auto-sizing in the CPU registers dialog
* Fix infinite loop when parsing watches generated by Python pretty printers
* Fix parsing gdb locals/arguments when the values contain escaped double and single quotes
* Add support for executing additional shell commands when using GDB
* Add flag to enable/disable loading of .gdbinit
* Expand macros in the additional GDB commands
* Improve logging, while trying to interrupt the debuggee
* Try to detect when the terminal couldn't be started and print an error instead of entering annoying loop
* Determine console pid from ps-command, returns either the same as we have now (e.g. xterm) or the pid of the sleep-command and works therefore also with newer gnome-terminals

## New plugin: Project Options Manipulator

* (Mass-)Manipulate options across targets in a project or projects in a workspace more easily
* Support replacements of (existing) custom vars
* Allow to limit scope of operations to specific target types
* Added support to replace in options
* Support resource compiler options
* Support to remove project files that are not assigned to a target
* Implemented search/add/remove of (resource) include dirs, custom vars, linker libs / folders...

## wxSmith

* Remove deprecated and never used Shadow and Bezel related code from wxsGauge.
* Incorpated wxSmithPlot (wxMathPlot) plugin
* Do not return wxALIGN_NOT for empty-flags, because xrc-handlers does not recognize it, use wxALIGN_LEFT instead, because it's internally the same
* Allow wxALIGN_CENTER (2d-centered) in sizeres again, as it is handled differently in wxWidgets
* Enable setting min and max size for sizers.
* Fixed wxSizerFlagsProperty, vertical align is not allowed inside vertical sizers, horizontal align is not allowed inside horizontal sizers, wxEXPAND is not allowed together with alignment and breaks layout in most recent wxWidgets.
* Fixed warnings about deprecated font-enums; add setter- and getter-functions for wxFontStyle, wxFontWeight and wxFontFamily to wxsPropertystream
* Several other bug fixes and improvements

## AStyle

* **Major improvement to astyle plugin**: Make it fully (options-) compatible with v2.05.1+
* Added new astyle options and formatters
* Removed obsolete astyle options
* When formatting text, only mark as modified lines that actually changed
* Fixed saving some options did not work
* Fixed resource

## FileManager

* Disable drag and drop in the tree if browsing a commit state of a version controlled folder
* Correctly resolve path to item when displaying version controlled path in changes only mode
* Improve support for displaying status icons representing the changes in the working copy or a particular commit when browsing version controlled directories. Also improves robustness when viewing the mercurial log
* Retrieve only relative paths when showing changes to a directory under version control
* Add checkbox to view only changed files from the last commit in a version controlled directory
* Fixed a couple of bugs with mercurial repo browsing
* Support for showing only commits with changes to a particular file
* Fixed crash if setting a folder to root which is under version control and where the VCS executables could not be run
* 'show changed files only' - flattens the tree of a directory under version control and shows only the files that have changed
* Support viewing diffs and browsing the history of a version controlled folder (currently supports GIT, SVN, BZR and HG).
* Support providing git status decorators (a bit clunky though)
* Correct labels for status decorator settings in default.conf for HG and BZR (they were reversed)
* Fixed crash bugs

## HeaderFixupPlugin

* Partial STL completion
* Use istream/ostream directly

## Help

* Always search in all man help root directories, not just the active one for the currently selected help file
* Update man search dirs, when the user changes the settings of the plugin
* Sort the result for the man page viewer
* Append the language of the manual page at the end of the link
* Fix looking up symbolic linked man pages in gz or bz2 files

## KeyBinder

* Handle Ctrl-- and Ctrl-+
* Make the plugin use the new events

## SpellChecker

* Check C++ raw strings like the other strings
* Improved checking accuracy in utf8 comments
* Activate OnlineSpellChecking for VHDL block comments and strings and for verilog strings
* Update language rules for checkable styles
* Do not check spelling of doxygen keywords

## Wizards

* Fix the ARM wizard to show a proper list of compilers
* Make it possible to create target wizard, without the need to add BuildTarget panel
* Make it possible to get or set the value from a wxComboBox
* Modify the ComboBox APIs to work with wxChoice or similar controls
* Add API for filling a wxChoice control with filtered compilers list (removed some code duplication, too)
* OpenCV project wizard improvement for MinGW target, it first try to detect whether a release version of OpenCV library exists, if not, try detecting whether a debug version exists

## ClassWizard

* Fix & issue with member vars in new class wizard
* Support for "scope" in class wizard
* Only add include dir, if it is not empty

## ToolsPlus

* Fixed memory leak
* Move cursor after typing text in the tools output window
* Add context menu on output pages and add entry to "close inactive tool pages"
* Use the same font as for editors in the toolsplus output window
* Improve input handling in the output window by only passing through regular key strokes

## DoxyBlocks

* Improve handling of config-folder
* Strip default menu keybindings that conflict core C::B shortcuts

## Browse Tracker

* Fix incorrect scintilla margin marker usage
* Better resolution of Jump line recording
* Add modifed user contrib tool bar

## SmartIndent

* **HDL**: do correctly unindent architecture", "entity" and "configuration".
* **HDL**: tidy up formating when CC finished
* **HDL**: do correctly unindent "end function" and "end procedure".
* Unindent "end block" correctly in VHDL mode
* Base next line indentation on the last non-empty line
* Handle (some) smart indentation for embedded languages (PHP, JavaScript, etc) within HTML

## CppCheck

* Add support for macros in the path of the cppcheck executable, clean up the code a bit
* Fix the text control in the config panel
* Add support for #defines

## NassiShneiderman

* Enhancement of the Cparser
* Add a menu entry to allow creating diagrams from selected text
* Match diagram colors to editor colors

## EditorTweaks

* Add menu item for controlling if the whitespace characters should be visible
* New option to enable laptop friendly keyboard shortcuts
* **Aligner**: Add shortcut to repeat the last align operation

## Other Plugins

* **EnvVar**: Misc. improvements
* **ToDo plugin**: Fixed ToDo List plugin does not ignore */ if it is on the same line
* **ToDo plugin**: disable refresh the list on double click
* **cb_koders**: Fix for non working ohloh search (ohloh was koders is now openhub/BlackDuck)
* **Thread Search**: Fixed thread safety issue in ThreadSearchEvent class
* **IncrementalSearch**: hide border of internal text-control and place it more left in the combo-control; layout was ugly on windows
* **OccurrencesHighlighting**: Fixed issue for #ifndef-ed code
* **CodeSnippets**: Remove edit & search CB duplicate code that caused issues

## Updated 3rd party libs

* Updated hunspell to v1.3.3 for security fixes and to fix crash with Korean keyboard
* Updated zlib lib to v1.2.8 to address security issues
* Updated bzib2 lib to v1.0.6 to address security issues
* Updated (wx)Scinitlla to v3.53, finally bringing the "HEX" lexers to the core
* Updated astyle update to v2.0.6pre (required due to license change)
* Updated Mozilla character encoding detection to recent releases

## Targeting wxWidgets 3.0 and 64 bit builds

* Fix "Fit toolbars" and "Optimize toolbars".
* **Scintilla**: Fix Don't allocate new ids every time a timer is created or for every editor
* Updated many wxWidgets API calls
* Fixed many UI glitches
* Fixed many assertions
* Fixed many crashes
* Fixed aligmnents
* Incorporate wx3.0 negative menu id's
* Temporary (?) remove wxTreeList from wxContribItems and wxSmithContribItems for wx30-builds to avoid a a name conflict, because a treelistctrl is part of wx >= 2.9.3
* Fixed warnings about deprecated font-enums with wx3.1

## Misc

* **Support for new lexers**: BibTeX, Coffee, IHex, JavaScript, Proty, Windows-Registry files, SREC, TeHEX
* **Editor**: Add menu commands for searching the selected text without opening the find-replace dialog
* **Editor**: Mark editor tabs of read-only files with an icon
* **New tool**: CbLauncher to launch C::B under Windows using modified application path's variables (for experts)
* **New version of crash handler (exchndl)**: More resiliency against truncated PE files and log message when loading symbols
* New command line option --user-data-dir=<path> to specify an alternative directory for user settings and user installed plugins
* 'Add file(s)' doesn't account for all generated files for all target's compilers
* Assign CRTL+P to the "Print" command by default
* Save notebook layout in project- and workspace-layout files (and load it from there)
* Save tab-layout of the files belonging to  the project in a project-layout file; save all tabs in a workspace-layout file
* Better multi monitor support for non windows system
* Introduce new API's to SDK for convenience
* **Scripting**: Expose several new API's
* Add versioning to project and workspace layout files
* Re-organised editor settings to make the grouping more logical
* Removed obsolete google code search, added StackOverflow and CodeProject search
* **File properties**: Count statistics language independantly
* **SmartIndent**: Handle (some) smart indentation for embedded languages (PHP, JavaScript, etc) within HTML
* Fixed plugin installation errors under Windows
* Make the check for externally modified files configurable, useful for slow network shares
* Ignore VCS (SVN, GIT, Mercurial...) folders when recursively adding files
* Avoid conflicts in portable mode
* Allow to clean a single object file within a project tree from project manager
* Updated C++ lexer keywords for more correctness
* **Linux**: Use standard-conform paths for config- and data-folders
* Support for Windows 10
* Many UI improvements
* Many other bug-fixes and improvements

# Summary, for download

Download the short (this) changelog here: https://sourceforge.net/projects/codeblocks/files/Binaries/16.01/changelog

Download the full changelog here: https://sourceforge.net/projects/codeblocks/files/Binaries/16.01/changelog_full

## Older Changelogs

See [Changelog for 13.12](/changelogs/13.12)

See [Changelog for 12.11](/changelogs/12.11)
