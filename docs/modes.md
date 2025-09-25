# Modes In Text Forge

Text Forge is lightweight and language agnostic, So there is no default dependence on any language. But how you can work
with any file type and have special features like syntax highlighters and linters?
This is where the modes come in, a mode is a special module designed to adapt to certain types of files and languages,
you can install the modes and leave the rest to the editor, everything is automatically managed to you can work with files.

## Mode Features

There is a list of all standard available features for modes, some mode can have more features with custom solutions and
some modes can haven't one or more feature is this list. In short, you can find optional features with *optional* tag, 
features of a mode depends on its developers:

- **Save & Load**

    Modes can encode and decode files, with this customizable encoding system you can work with a lot of files, even
    with files they aren't text files!

- **Syntax Highlighter** _optional_

    We provide both simple and advanced syntax highlighting ability to mode developers, including simple highlighters to
    fully customized highlighters. Highlighters currently can just one theme and highlighter colors are completely mode-driven.

- **Advanced Commenting Handling** _optional_

    We have easy API for defining comment delimiters and logics. Editor provides line folding and more based on these
    information.

- **Mode Panels** _optional_

    Modes can have their panels, so you can configure a mode visually based on mode features.

- **Auto Format** & **Auto Indent** _optional_

    We provide auto format and auto indent options separately, you can run these options to clean your files with modes'
    power. You can use these features from command palette, menus, or with shortcuts; These features are available in 
    `Edit > Indention > Auto Indent` and `Format > Auto Format`, to see shortcuts, type `Auto Indent` or `Auto Format`
    in command palette.

- **Initialization Lifecycle**

    We have high standards about your files safety, so a mode will load completely before working with your file, or if 
    initialization fails, we will cancel task.

- **Code Completion** _optional_

    We provide a mode-based code completion to you with complete API for mode developers, so features and smartness of
    this feature is based on your current mode.

- **Preview Rendering** _optional_

    Modes can generate live preview based on your file, and you can see this preview in **Preview Panel** in right side of editor.

- **File Outline** _optional_

    You can navigate between sections in your file or review them in **Outline Panel** in left side of editor, this is a
    mode-driven feature too, so this section features are based on your mode.

- **Linting** _optional_

    We currently haven't supported LSP & DAP client ([feature tracking issue↗️](https://github.com/text-forge/text-forge/issues/88))
    for complete language based features, but we have a simple mode-driven linting feature, and you can see your file
    problems in **Problems Panel** in bottom of editor, in this panel all error and warnings provided by mode will show
    , and you can navigate between them by clicking on an item.

!!! Note

    A lot of above features were added in TFM API v2.0, you can read more about this API [here](mode_development.md#text-forge-mode-api).
    We provide a lot of these features as optional features, because a mode can work with simple text or non-code files,
    so there is a lot of optional but basic features.

!!! Note

    After TFM API v2.0, we use buffer based save and load instead of file based behavior, this new system have safer 
    error handling and modes can no longer see the file paths in your system directly when you save / load a file.

!!! Important

    Modes are unlimited moduless! So you should be sure about a mode before installing it, otherwise modes can get access
    to your files content, for completely safe experience download official and community modes in [mode library](https://github.com/text-forge/mode-library).

!!! Note

    Auto Format and Auto Indent are triggerable actions, there is an **Auto Indention** toggleable feature in `Format`
    menu that will change indention automatically when you create new line.

## Mode Kits

In programming word, there is a lot of types of programmers, for example you can be a web developer, in this case you 
need to work with some files as your basic workflow, such as `.html`, `.css`, and `.js`. So we provide mode kits, a
mode kit is a collection from related modes create for a special type of users.

## Installing

You can install modes in different ways. In this section, we will explain standard ways.

### From Marketplace

Marketplace is useful feature to install modes is simplest way. This way also protect you from incompatible modes and
limits them.

To install a mode / mode kit from marketplace, go to **Settings > Marketplace** and select **Modes** category, then
click on a mode to see its details. You can use **Install** button to download and install mode. If this button is
disabled your editor isn't compatible with this mode, you can find another mode or try other ways.

After clicking on Install button, you should wait until see **Package Installed!** notification, then you can use your
new mode without restarting the editor.

!!! Note

    You can install these modes in this way:
    - Modes in [Marketplace](https://github.com/text-forge/marketplace)

### From Mode Manager

You can download mode installation files, this file is a `.zip` or `.tfmode` file that you can download it from mode
providers, use **Mode Manager** (`Settings > Mode Manager` in menus) and select this file with `Import Mode / Mode Kit`.
After loading, you will receive an **info** notification that says `"Load mode / mode kit completed"` and you can use 
your new modes now without restarting the editor.

!!! Caution

    This installation doesn't check for mode compability!

!!! Note

    You can install these modes in this way:
    - Modes in [Mode Library](https://github.com/text-forge/mode-library)
    - Modes in [GitHub's `text-forge` topic](https://github.com/topics/text-forge)
    - Any mode that provides `.zip` or `.tfmode` as installation file.

### From Mode Source

Modes works in isolated eviroment, so you can transfer their files to another editor data folder and use them there.
For this installation way you should have a mode source that you can get it from GitHub or somewhere else. To install
one or more mode from source use **Settings > Open Data Folder** and paste mode folder in `modes/` directory. When you
restart your editor you can use new mode.

!!! Note

    You can install these modes in this way:
    - Modes in [Mode Library](https://github.com/text-forge/mode-library)
    - Modes in [GitHub's `text-forge` topic](https://github.com/topics/text-forge)
    - Modes installed in another device or user data.
    - Any mode that provides source code.
