# Text Forge Menus
## Introduction
In TextForge, we use menus as the main way to edit with the help of Action Scripts and dynamic 
command structure. This guide has tried to explore the tips for menu options. 

All actions support multi-caret editing, if not, action will show a popup and request caret 
selection. You can click on a text without selection (caret) when hold `Alt` to add new caret.

## File
This menu includes regular actions with working with files and the editor window. 

### New
Opens a new file. It doesn't activate any mode, so it's recommended to save it after creating a new 
file and then continue editing. 

### New Window
Opens another window of the editor. Due to the lack of support for multi-file editing (currently), 
this is a good way to work with multiple files. 

### New With Template

!!! Note

	It isn't yet available. 

### Open
Creates a pop-up to select and open an existing file. 

### Recent Files
It lists recently opened files, clicking on any file will open that file. 

### Save
Saves the open file, if the file doesn't have a specific location (e.g. created with the New option) 
it will be the same as Save. 

### Save As
It creates a pop-up to choose a location and name to save the open file. 

### Reload
It reloads the open file, similar to reopening the same file. 

!!! Note

	Some functions may not work properly after saving a file, in which case please report the 
	problem and use Reload as a temporary solution. 

### Close
It closes the open file, without closing the editor. 

### Create Backup
Saves a manual backup of the open file, use Load From Backup to restore. Go to Preferences for 
automatic backups. 

### Load From Backup
It displays a list of available backups by file and time, restored by clicking on the file version. 

!!! Warning

	This is an experimental feature.

### Copy Path
Copies the path of the open file to the clipboard. 

### Show In FileSystem
It displays the open file in the system files. 

### Secure Delete
It deletes the file completely, fills the entire content of the file with zero bits, and then 
deletes. 

### Restart
Similar to New Window but closes the current window. 

### Exit
Closes the editor. 

## Edit
This menu contains commands and actions related to editing the content of the file. 

### Undo
It takes a step back in memory. 

### Redo
It returns the last Undo. 

### Cut
Copies the selected text to the clipboard and deletes it in the file. It does this for the entire 
line if no text is selected. This option is also available in the context menu. 

### Copy
Copies the selected text (or entire line) to the clipboard. This option is also available in the 
context menu. 

### Paste
Paste the latest clipboard content (instead of the selected text). This option is also available in 
the context menu. 

### Delete
Deletes the selected text or the next character. 

### Select All
Selects all file content. 

### Select Next Occurrence 
The next occurrence selects the selected text and keeps the current selections. If no text is 
selected, it selects the current word. 

### Select All Occurrences 
This operation repeats the Select next occurrence until there is an occurrence. 

### Duplicate Selection 
Duplicates the selected text and selects duplicated text.

### Evaluate Selection
Evaluates the selected text. 

### Line (Submenu)
It puts the actions related to the line in a group. 

#### Move Lines Up
Lines with caret or selection move up one line. 

#### Move Lines Down
Lines with caret or selection move down one line. 

#### Indent
The selected lines are taken one block further in. 

#### Unindent
It brings out the selected lines one block further. 

#### Delete Lines
Removes the entire content of selected lines.

#### Toggle Comment
It converts the line into a comment or vice versa. 

!!! Warning

	This is an experimental feature.

#### Duplicate Lines
It duplicates the selected lines and selects the duplicated lines. 

#### Select Whole Line
Extends the selection to the entire line(s). 

#### Select Paragraph 
It expands the selection to the point where there is a blank line. 

#### Join Lines
It joins the selected lines, leaving a space between each line. 

#### Move To New File
Opens a new file and moves the selected lines to that file. 

### Completion Query
Sends a completion query (request), editor will send request when you stop typing as default, but 
you can do this manually with this option.

### Indention (Submenu)
It puts the actions related to indention in a group.

#### Auto Indent
Will automaticly indent whole file content.

!!! Note

	Some modes haven't support for auto indent, this option will be enabled just for supported modes.

#### Convert Indent To Spaces
Converts indention of currently selected line(s) to spaces and sets indention mode to spaces.

#### Convert Indent To Tabs
Converts indention of currently selected line(s) to tabs and sets indention mode to tabs.

### Convert Case (Submenu)
Provides options to convert selected text case, these options are simple, so we will not explain 
them here.

## Search
This menu includes commands and actions related to sreaching in file content and replace actions.

### Find and Replace
Opens **Find** panel. You can find this panel in right side of editor and open it manually.

### Find Next
Selects next match, or first match when current match is last one.

### Find Previous
Selects previous match, or last match when current match is first one.

### Replace All
Replaces all matches, it's same as Replace All button in Find panel.

## Go To
This menu includes commands and actions related to fast navigation in file content and sections.

### Go To Line
Shows a popup to go to selected line, **line numbers start from 1.**

### Code Regions

!!! Note

	It isn't yet available. 

### Insert Navigation Mark

!!! Note

	It isn't yet available. 

### Navigation Marks

!!! Note

	It isn't yet available. 

### Table Of Contents

!!! Note

	It isn't yet available. 

### Bookmarks

!!! Note

	It isn't yet available. 

### Toggle Bookmark

!!! Note

	It isn't yet available. 

### Remove All Bookmarks

!!! Note

	It isn't yet available. 

## Command
This menu includes commands and actions related to commands that you can run.

### Command Palette
Shows command palette. You can run all commands here by clicking on them and there is a search box.
When you type, command items order updates based on similarity of they name with your search, and
matching segments will be highlighted. If exists, you can see command shortcut in right side of 
command name.

## Format
This menu includes commands and actions related to formatting file content.

### Auto Format
Will automaticly format whole file content.

!!! Note

	Some modes haven't support for auto format, this option will be enabled just for supported modes.

### Auto Indention
When enabled, editor will try to calculate indention level when you add new line; Otherwise, will 
apply last line indention level for new line.

!!! Note

	This is an experimental feature and can have wrong behavior.

### Remove All Indents
Removes all indention and white spaces in both side of all lines.

### Save As Template

!!! Note

	It isn't yet available. 

### Templates

!!! Note

	It isn't yet available. 

## View 
This menu includes options and actions related to editor layout and visible items.

### Increase Font Size
Increases content font size by 2px.

### Reduce Font Size
Reduces content font size by 2px.

### Reset Font Size
Resets content font size to default (16px).

### Focus On Editor
Will move focus from everywhere to main editor. For example you can open notification panel to see
notifications and then use `Esc` (This action shortcut) to back to editor very fast and easy.

### Line Length Guides
Opens a popup to configure line length guide lines. You can have zero or more line length guides and
add them as a comma-separated list, first item will be main and hard guide line and will draw with 
more contrast.

### Show Bookmarks
When enabled, shows bookmarks in gutter.

!!! Note

	Bookmarks feature isn't yet available.

### Show Line Numbers
When enabled, shows line numbers in gutter (from 1).

### Show Fold Gutter
When enabled, shows fold / unfold buttons in foldable lines gutter.

### Show Minimap
When enabled, shows minimap in right side of editor.

### Block Type Caret
When enabled, shows caret as block.

!!! Important

	This ins't replace edit mode (replace next character instead of insert new character before it),
	to switch between insert and replace editing modes, press `insert` button.

### Highlight All Occurrences
When enabled, highlightes other occurrences of currently selected text.

### Highlight Current Line
When enabled, highlightes lines with caret.

### Show Control Characters
When enabled, shows control characters.

!!! Tip

	You can insert control characters from context menu.

### Show Tabs
When enabled, shows each tab with a transparent.

### Show Spaces
When enabled, shows each space with a transparent center-dot.

### Full Screen
When enabled, makes editor window fullscreen.

## Tools
This menu includes tools, them settings, and extensions options.

### Color Picker
Shows a color picker window to help you work with colors.

### Security

!!! Note

	It isn't yet available. 

### Counter

!!! Note

	It isn't yet available. 

### Translation

!!! Note

	It isn't yet available. 

### Clipboard History

!!! Note

	It isn't yet available. 

### Function Creator.

!!! Note

	It isn't yet available. 

### Documentation

!!! Note

	It isn't yet available. 

### Auto Completion

!!! Note

	It isn't yet available. 

### Time Management.

!!! Note

	It isn't yet available. 

### Calendar

!!! Note

	It isn't yet available. 

### By Extensions
Keeps options provided by extensions.

## Settings
This menu includes options and actions related to editor data and configuration.

### Preferences
Shows Preferences window.

### Mode Manager
Shows Mode Manager window.

### Extensions
Shows Extensions window.

### Open Data Folder
Opens editor data folder.

## Help
This menu includes options related to manuals and online resources.

### GitHub Repository
Opens editor source GitHub repository in browser.

### Mode Library
Opens official Mode Library repository in browser.

### Forum
Opens official forum in browser.

### Share Feedback
Opens create topic window in forum in browser.

### Submit Issue
Opens issue template selection window in GitHub repository in browser.

### Online Docs
Opens home page of online documentation in browser.

### About
Opens about dialog.
