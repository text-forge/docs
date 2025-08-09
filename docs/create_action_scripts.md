# Create action scripts

!!! Note
    Reading [Action Scripts Guide](action_scripts.md) is recommended before creating actions scripts.

## Regular action scripts

There is some different types of action scripts based on their base classes, `ActionScript` class designed for regular
action scripts and can handle a lot of tasks.

To add new action script you should make sure there is an item in menus for that action script, you can use `data/main_ui.ini`
to add new options (or menus), to understand about structure of this file you can see [here](https://text-forge.github.io/docs/data_driven_ui/#menus).
After select your option create a script in `action_scripts/` directory with same name (but in snake_case), it this case
we will create **Copy Path** action script that will copy file path of opened file in clipboard, so we will create
`action_scripts/copy_path.gd` and use this script as start point:

```gdscript
extends ActionScript
```

Just that! Run project and see option is enabled. But there is no action for now, so we have 3 steps to complete our 
action script:

### Add initializing

We needn't any special initializing for this action script, all we need is disabling it when there is no opened file, 
there is ready-made feature for this:

```gdscript
extends ActionScript

func _initialize() -> void:
    requires_file = true
    requires_saved_file = true
```

With this function `ActionScript` class will disable option when there isn't saved file, it means when you create a new
file this option will keep disabled until that file saved, because before that there is no file path. Otherwise, (for 
example when user uses Open) option will be enabled.

### Add main action

We have initialized action script, but there is no action, so let's add it. To do this we use `_run_action()` function,
this function will be called when user clicks in option in menus, presses shortcut (we will add shortcut later) or uses
command palette. So we can complete our action script with this function:

```gdscript
extends ActionScript

func _initialize() -> void:
	requires_file = true
	requires_saved_file = true

func _run_action() -> void:
	DisplayServer.clipboard_set(Global.get_file_path())
```

Almost done! We have completed action script, and you can try it now in witch way you want.

### Add shortcut

There is an easy way for adding shortcuts to action scripts, so let's see how we can do it. To have shortcut we need a
`Shortcut` resource stored in `shortcuts/` directory, so go to Godot's FileSystem dock and use RMB on `res://shortcuts/`,
then click on Create New > Resource... and create a `Shortcut` resource and save it as `copy_path.tres`. Shortcut will
be opened in Inspector, click on `Events` and add new element, then create a new `InputEventKey` in that element. Use 
`Configure` button and set your shortcut, then run project and try it. You can open command palette (Ctrl+P) and type `copy path`
to see shortcut.