(preferences)=

# Preferences

Starting with version 0.4.6, napari provides persistent settings.

Settings are managed by the global `SETTINGS` object and can be imported as:

```python
from napari.utils.settings import SETTINGS
```

## Sections

The settings are grouped by sections and napari core provides the following:

### APPEARANCE

User interface appearance settings.


#### Highlight thickness

*Select the highlight thickness when hovering over shapes/points.*

* <small>Access programmatically with `SETTINGS.appearance.highlight_thickness`.</small>

* <small>Type: `napari.utils.events.evented_model.ConstrainedIntValue`.</small>

* <small>Default: `1`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### Show layer tooltips

*Toggle to display a tooltip on mouse hover.*

* <small>Access programmatically with `SETTINGS.appearance.layer_tooltip_visibility`.</small>

* <small>Type: `builtins.bool`.</small>

* <small>Default: `False`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### Theme

*Select the user interface theme.*

* <small>Access programmatically with `SETTINGS.appearance.theme`.</small>

* <small>Type: `napari.utils.settings._defaults.Theme`.</small>

* <small>Default: `'dark'`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>

### APPLICATION

Main application settings.


#### Console notification level

*Select the notification level for the console.*

* <small>Access programmatically with `SETTINGS.application.console_notification_level`.</small>

* <small>Type: `napari.utils.notifications.NotificationSeverity`.</small>

* <small>Default: `<NotificationSeverity.NONE: 'none'>`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### First time

*Indicate if napari is running for the first time. This setting is managed by the application.*

* <small>Access programmatically with `SETTINGS.application.first_time`.</small>

* <small>Type: `builtins.bool`.</small>

* <small>Default: `True`.</small>

#### GUI notification level

*Select the notification level for the user interface.*

* <small>Access programmatically with `SETTINGS.application.gui_notification_level`.</small>

* <small>Type: `napari.utils.notifications.NotificationSeverity`.</small>

* <small>Default: `<NotificationSeverity.INFO: 'info'>`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### IPython interactive

*Toggle the use of interactive `%gui qt` event loop when creating napari Viewers in IPython.*

* <small>Access programmatically with `SETTINGS.application.ipy_interactive`.</small>

* <small>Type: `builtins.bool`.</small>

* <small>Default: `True`.</small>

#### Language

*Select the display language for the user interface.*

* <small>Access programmatically with `SETTINGS.application.language`.</small>

* <small>Type: `napari.utils.settings._defaults.Language`.</small>

* <small>Default: `'en'`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### Opened folders history

*Last saved list of opened folders. This setting is managed by the application.*

* <small>Access programmatically with `SETTINGS.application.open_history`.</small>

* <small>Type: `builtins.str`.</small>

* <small>Default: `[]`.</small>

#### Playback frames per second

*Playback speed in frames per second.*

* <small>Access programmatically with `SETTINGS.application.playback_fps`.</small>

* <small>Type: `builtins.int`.</small>

* <small>Default: `10`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### Playback loop mode

*Loop mode for playback.*

* <small>Access programmatically with `SETTINGS.application.playback_mode`.</small>

* <small>Type: `napari.utils.settings._constants.LoopMode`.</small>

* <small>Default: `<LoopMode.LOOP: 'loop'>`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### Preferences size

*Last saved width and height for the preferences dialog. This setting is managed by the application.*

* <small>Access programmatically with `SETTINGS.application.preferences_size`.</small>

* <small>Type: `typing.Tuple[int, int]`.</small>

* <small>Default: `None`.</small>

#### Saved folders history

*Last saved list of saved folders. This setting is managed by the application.*

* <small>Access programmatically with `SETTINGS.application.save_history`.</small>

* <small>Type: `builtins.str`.</small>

* <small>Default: `[]`.</small>

#### Save window geometry

*Toggle saving the main window size and position.*

* <small>Access programmatically with `SETTINGS.application.save_window_geometry`.</small>

* <small>Type: `builtins.bool`.</small>

* <small>Default: `True`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### Save window state

*Toggle saving the main window state of widgets.*

* <small>Access programmatically with `SETTINGS.application.save_window_state`.</small>

* <small>Type: `builtins.bool`.</small>

* <small>Default: `True`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### Window fullscreen

*Last saved fullscreen state for the main window. This setting is managed by the application.*

* <small>Access programmatically with `SETTINGS.application.window_fullscreen`.</small>

* <small>Type: `builtins.bool`.</small>

* <small>Default: `None`.</small>

#### Window maximized state

*Last saved maximized state for the main window. This setting is managed by the application.*

* <small>Access programmatically with `SETTINGS.application.window_maximized`.</small>

* <small>Type: `builtins.bool`.</small>

* <small>Default: `None`.</small>

#### Window position

*Last saved x and y coordinates for the main window. This setting is managed by the application.*

* <small>Access programmatically with `SETTINGS.application.window_position`.</small>

* <small>Type: `typing.Tuple[int, int]`.</small>

* <small>Default: `None`.</small>

#### Window size

*Last saved width and height for the main window. This setting is managed by the application.*

* <small>Access programmatically with `SETTINGS.application.window_size`.</small>

* <small>Type: `typing.Tuple[int, int]`.</small>

* <small>Default: `None`.</small>

#### Window state

*Last saved state of dockwidgets and toolbars for the main window. This setting is managed by the application.*

* <small>Access programmatically with `SETTINGS.application.window_state`.</small>

* <small>Type: `builtins.str`.</small>

* <small>Default: `None`.</small>

#### Show status bar

*Toggle diplaying the status bar for the main window.*

* <small>Access programmatically with `SETTINGS.application.window_statusbar`.</small>

* <small>Type: `builtins.bool`.</small>

* <small>Default: `True`.</small>


### PLUGINS

Plugins settings.


#### Plugin sort order

*Sort plugins for each action in the order to be called.*

* <small>Access programmatically with `SETTINGS.plugins.call_order`.</small>

* <small>Type: `typing.List[napari.utils.settings._defaults.PluginHookOption]`.</small>

* <small>Default: `None`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### Disabled plugins

*Plugins to disable on application start.*

* <small>Access programmatically with `SETTINGS.plugins.disabled_plugins`.</small>

* <small>Type: `builtins.str`.</small>

* <small>Default: `set()`.</small>

#### Reader plugin extension association.

*Assign file extensions to specific reader plugins*

* <small>Access programmatically with `SETTINGS.plugins.extension2reader`.</small>

* <small>Type: `builtins.str`.</small>

* <small>Default: `{}`.</small>

#### Writer plugin extension association.

*Assign file extensions to specific writer plugins*

* <small>Access programmatically with `SETTINGS.plugins.extension2writer`.</small>

* <small>Type: `builtins.str`.</small>

* <small>Default: `{}`.</small>


### SHORTCUTS

Shortcut settings.


#### shortcuts

*Set keyboard shortcuts for actions.*

* <small>Access programmatically with `SETTINGS.shortcuts.shortcuts`.</small>

* <small>Type: `typing.List[str]`.</small>

* <small>Default: `{'napari:toggle_console_visibility': ['Control-Shift-C'], 'napari:reset_scroll_progress': ['Control'], 'napari:toggle_ndisplay': ['Control-Y'], 'napari:toggle_theme': ['Control-Shift-T'], 'napari:reset_view': ['Control-R'], 'napari:increment_dims_left': ['Left'], 'napari:increment_dims_right': ['Right'], 'napari:focus_axes_up': ['Alt-Up'], 'napari:focus_axes_down': ['Alt-Down'], 'napari:roll_axes': ['Control-E'], 'napari:transpose_axes': ['Control-T'], 'napari:toggle_grid': ['Control-G'], 'napari:toggle_selected_visibility': ['V'], 'napari:activate_label_erase_mode': ['E'], 'napari:activate_fill_mode': ['F'], 'napari:activate_paint_mode': ['P'], 'napari:activate_label_pan_zoom_mode': ['Z'], 'napari:activate_label_picker_mode': ['L'], 'napari:new_label': ['M'], 'napari:decrease_label_id': ['D'], 'napari:increase_label_id': ['I'], 'napari:activate_points_add_mode': ['P'], 'napari:activate_points_select_mode': ['S'], 'napari:activate_points_pan_zoom_mode': ['Z'], 'napari:select_all': ['A'], 'napari:delete_selected_points': ['Backspace', 'Delete'], 'napari:activate_add_rectangle_mode': ['R'], 'napari:activate_add_ellipse_mode': ['E'], 'napari:activate_add_line_mode': ['L'], 'napari:activate_add_path_mode': ['T'], 'napari:activate_add_polygon_mode': ['P'], 'napari:activate_direct_mode': ['D'], 'napari:activate_select_mode': ['S'], 'napari:activate_shape_pan_zoom_mode': ['Z'], 'napari:activate_vertex_insert_mode': ['I'], 'napari:activate_vertex_remove_mode': ['X'], 'napari:copy_selected_shapes': ['Control-C'], 'napari:paste_shape': ['Control-V'], 'napari:select_all_shapes': ['A'], 'napari:delete_selected_shapes': ['Backspace', 'Delete'], 'napari:finish_drawing_shape': ['Escape']}`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>

### EXPERIMENTAL

Experimental settings.


#### Render Images Asynchronously

*Asynchronous loading of image data. 
This setting partially loads data while viewing. 
You must restart napari for changes of this setting to apply.*

* <small>Access programmatically with `SETTINGS.experimental.async_`.</small>

* <small>Type: `builtins.bool`.</small>

* <small>Default: `False`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>
#### Enable Asynchronous Tiling of Images

*Renders images asynchronously using tiles. 
You must restart napari for changes of this setting to apply.*

* <small>Access programmatically with `SETTINGS.experimental.octree`.</small>

* <small>Type: `typing.Union[bool, str]`.</small>

* <small>Default: `False`.</small>
* <small>UI: This setting can be configured via the preferences dialog.</small>

**Support for plugin specific settings will be provided in an upcoming release.**

## Changing settings programmatically

```python
from napari.utils.settings import SETTINGS

SETTINGS.appearance.theme = "light"
```

## Reset to defaults via CLI

To reset all napari settings to the default values:

```bash
napari --reset
```

## The preferences dialog

Starting with version 0.4.6, napari provides a preferences dialog to manage
some of the provided options.

### Appearance

![appearance](../images/_autogenerated/preferences-appearance.png)



### Application

![application](../images/_autogenerated/preferences-application.png)



### Plugins

![plugins](../images/_autogenerated/preferences-plugins.png)



### Shortcuts

![shortcuts](../images/_autogenerated/preferences-shortcuts.png)



### Experimental

![experimental](../images/_autogenerated/preferences-experimental.png)



### Reset to defaults via UI

To reset the preferences click on the `Restore defaults` button and continue
by clicking on `Restore`.

![](../images/_autogenerated/preferences-reset.png)
