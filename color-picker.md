# Color Picker

[`< Tools`](./tools.md)

**Icon:** ![](https://raw.githubusercontent.com/stipple-effect/stipple-effect/master/res/icons/color_picker.png)

**Hotkey:** <kbd>C</kbd>

## Behaviour

Set the primary or secondary color to the color of the clicked pixel of the currently selected [cel](./cel.md).

## Actions

* **Assign color to primary slot:** ![](./assets/ui/left-click.png "Left-Click")
* **Assign color to secondary slot:** ![](./assets/ui/right-click.png "Right-Click")

## Modifiers

* <kbd>Shift</kbd> - search layer by layer for the **highest non-transparent color** (alpha/opacity value greater than 0) at the specified pixel; does nothing if no such pixel is found
* <kbd>Ctrl</kbd> - sample the pixel from a **flattened** equivalent of the project; useful when dealing with layers of partial transparency
