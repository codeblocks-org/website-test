---
title: "Version 25.03"
date: 2025-03-31T00:00:00+00:00
draft: false
aliases:
  - /downloads/binaries/changelog
---
For the release 25.03, we provide a changelog hereby about what has changed since 20.03 (to download the change log, a link is provided at the bottom of this page):

## General

 * Added active plugin information to the About dialog.
 * Added support for riscv64 build on Linux.
 * Added UI for automatic source folders aka project globs.
 * Allow managing Globs also via pop-up menu in project explorer.
 * Allow importing/exporting global variable sets.
 * Allow removal from project of multiple selected files.
 * Allow splash screen translation.
 * Make many strings translatable.
 * Fix detection of opened wxs and double saving query.
 * Add new wxArtProvider ID to wxSmith's image picker dialog.
 * Don't use deprecated gamin library.
 * Use wxColourPickerCtrl for colour selection in all settings.
 * Fixed C::B icon flash in taskbar.
 * Enhanced HI-DPI support.
 * Colour editor: Add "Reset all" button.
 * Make opening a file from the command line (--file) in an already running instance to work correctly.
 * Correct definition of DEFAULT_CONSOLE_SHELL for Mac.
 * Rework Drag and Drop: Complete rework of dnd in project tree and editor.
 * Support DnD of files to virtual folders.
 * Do not check compiler in skipped targets.
 * Do not select all files in "Remove files..." by default.
 * Editor: Allow customising changebar colours.
 * Editor: Fix popup font size when using Direct2D.
 * Enable app and debug log in batch build mode.
 * Find dialog: disable Find button if some input value is incorrect.
 * Fix change of encoding in already opened files when changing encoding settings.
 * Fix hangs when returning focus to C::B.
 * Fix missing target selection choice in compiler's toolbar.
 * Fix renaming virtual folders.
 * Fix sorting of libraries and search paths in Build Options.
 * Ignore case when sorting plugins in the configuration dialog.
 * Lexer: add make_unique, make_unique_for_overwrite, make_pair, thread and mutex.
 * Lexer: Add enums to the list of keywords in the Squirrel lexer.
 * Lexer: Highlighting of fortran-77 columns in Editor.
 * Logger: Scroll to the end of log control if a new message is added.
 * Make DirectWrite the default value for editor technology in MSW.
 * Modernise/update crash handler dll (exchndl) from v0.9.9 to v0.9.11 (Windows only change).
 * Move crash report file if C::B folder is not writable.
 * Printing: Fix endless loop when printing without specifying page size.
 * Printing: Add support for printing multiple documents as a block.
 * Printing: Detect incorrect page range (start > end).
 * Project Menu: Do not show "Notes" and "Set programs' arguments" if no project is opened.
 * Total rework of global user variables. Added Exoirt/Import capability. 
 * Make sure global variables can be used directly after they are defined.
 * Fix showing the default colour in Settings -> Environment -> Colours.
 * Syntax highlighting: fix default colour detection and restoration.
 * Add display info to the Help -> About -> Information dialog
 * Add option to display projects in alphabetical order in management panel.
 * Fixed opening more than one instance of CB (Windows).
 * Fix renaming of opened files.
 * Restore project manager tree position after deleting or renaming files.
 
## Plugins
 
 * Added Jens Lody's DisplayEvent core plugin.
 
### AStyle
 
 * Updated to v3.2 which seems to be the latest as the project seems stalled.
 
### BrowseTracker
 
 * Enable settings translation.
 
### Code completion
 
 * Restored the Symbol Browser.
 * Fix adding parentheses and doc window not popping up on MSW.
 * Fix freeze when adding project files
 * Fix clobbered CB global settings changes when closing loaded projects. 
 * Fix infinite loop when parsing files with illegal UTF8 chars.
 * Fixed and stress tested crashes caused by invalid pointers in CodeBrowser.
 
### Compiler
 
 * Added MinGW64, MSYS2, MSVC17 and TDM compilers.
 * Added support for the c++ standards 23 and 26 (and their gnu extensions).
 * Added options -std=c23 and -std=gnu23 on GCC13 and newer.
 * Added response files for to long command lines on compiling and linking.
 * Use correct option for C++20 depending on version.
 * Disable the Run button if there is no project and there is no valid editor.
 * Disable the Run button if the executable does not exist.
 * Fix Cygwin detection.
 * Fix Intel compiler creation of static libraries.
 * Support SDCC 4.2.0 new options and other enhacements.
 * Sort compilers alphabetically, hide invalid compilers in project options.
 * Update AVR gcc compiler flags. Add missing uC and add some comments for better readability.
 * Update SDCC compiler toolchain executables.
 * Use the same shell for cleaning and compiling makefiles.
 * Enhanced MinGW compiler detection.
 * Sort compiler list in compiler detection dialog.
 
### Debugger
 
 * CDB driver: Implement user arguments.
 * Add an option to disable the switching of the perspective when starting the debugger.
 * Add support for Examine memory dialog when using the CDB debugger.
 * Add support for newer versions of CDB.
 * Add support for Threads list and local variables for CDB debugger.
 * Fix for 64-bit addresses in CDB.
 * Fix support for debugging using Cygwin.
 
### File manager
 
 * Prevent deletion of the system root folder.
 
### Help
 
 * Fix access violation on MSW.
 * Remove memory leak.
 
### LibFinder
 
 * Fix stack corruption when clicking on "Try to detect missing ones".
 
### ProjectsImporter
 
 * Fix import of MSVC++ 6 workspaces.
 
### Regex Testbed
 
 * Add testing of std::regex.
 * Allow pasting C-escaped code.
 * General improvements.
 
### ReopenEditor
 
 * Fix crash when changing window mode.
 
### ScriptedWizard:
 
 * Remove stray bracket in SDL2 wizard script.
 * Allow resizing.
 * Fix DirectX, GTK, OpenCV and STLPort script syntax.
 * Fix SFML project script.
 * Fix support of Clang in wxWidgets' wizard.
 * Make new wxWidgets projects DPI-aware on MSW.
 * wizard: Update wxWidgets project wizard (thanks PB)
 * Add wx3.3 to wxWidgets wizard.
 * Allow translation.
 
### SourceExporter
 
 * Updated wxPDFDoc library.
 
### Spellchecker
 
 * Fix big memory leak.
 * Show flag for some generic dictionaries.
 
### ThreadSearch
 
 * Add edit button in the directory select dialog
 * Add a "MatchInComments" option.
 * Better auto scroll.
 * Repeat the last search if the search text field is empty, and there was a last search found.
 
### TODO
 
 * Fix panel not filling correctly.
 * Avoid invalid date assertion when sorting date column.
 
### wxSmith
 
 * Added EVT_ICONIZE, EVT_ACTIVATE, EVT_MENU_OPEN, EVT_MENU_CLOSE and EVT_MENU_HIGHLIGHT_ALL to wxsFrame.
 * Fixed generated code for embedded panels that does not resize correctly.
 * Make disabling I18n in wxSmith really work.
 * Add flag wxAUI_MGR_LIVE_RESIZE to wxAuiManager.
 * Add missing wxART_CLOSE to the bitmap editor.
 * Add missing wxYES for confirm dialogs, to overwrite existing files.
 * Add setting for using Bind() instead of Connect(), disabled by default.
 * Add support for stretchable separator.
 * Add wxDataViewCtrl, wxDataViewListCtrl and wxDataViewTreeCtrl widgets.
 * Add wxEditableListBox to the standard tab.
 * Allow change of I18N setting in existing resources.
 * allow specific and generic object event functions.
 * Allow use of the Validator property when creating Custom Widget code.
 * Added two properties to wxsGLCanvas. Update generated code.
 * Better UI for the Toolbar editor.
 * Fix code generation for wxsCustomControl when Style is empty.
 * Fix crash when deleting the last tool.
 * Fix EOL in generated code.
 * Fix widget order of Standard, Advanced and Contrib palettes.
 * Fix tab usage, currently the setting is inverted.
 * Generate code to destroy the common dialogs.
 * Make the OK button the default one in wxStdDlalogButtonSizer.
 * Make wxsCustomWidget create code for the common properties.
 * Remove duplicated style wxTAB_TRAVERSAL in dialogs and wxsFrame.
 * Remove duplicated wxSTAY_ON_TOP in wxsFrame.
 * Fix project corruption when renaming wxSmith-related files.
 * Replace long with wxWindowID in the generated code.
 * Support wxWindgets 3.2 font weights.
 * Do not call _() in the generated code for texts like "*" or "12".

# Summary, for download

Download the full changelog here: https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/changelog

## Older Changelogs

See [Changelog for 20.03](/changelogs/20.03)

See [Changelog for 17.12](/changelogs/17.12)

See [Changelog for 16.01](/changelogs/16.01)

See [Changelog for 13.12](/changelogs/13.12)

See [Changelog for 12.11](/changelogs/12.11)

## Special thanks

Special thanks for their (continuous) support go to:

 * Alatar
 * Artem VL
 * blauzahn
 * Christophe Marc BERTONCINI
 * Commaster
 * danselmi
 * darmar
 * drzacek
 * Eran Ifrah
 * Fabián Inostroza
 * Gérard Durand (gd_on)
 * Gokul Krishnan
 * Hayleyfire
 * homertp
 * Jacques Laffont
 * Juan Manuel Fernández Muñoz
 * LETARTARE
 * Lionel
 * Martin Strunz
 * Miguel Gimenez
 * ouch
 * sodev
 * Specialmart
 * stahta01
 * Xaviou
 * Zheng Fan
