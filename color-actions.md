[`< Overview`](./README.md)

# Color actions

**Color actions** are algorithmic operations that operate over every pixel in a given [scope](./scope.md) of the current [project](./project.md).

## ![](https://raw.githubusercontent.com/stipple-effect/stipple-effect/master/res/icons/palettize.png) Palettization

[*API function*](../api/project.md#palettize)

**Shortcut:** <kbd>Shift</kbd> + <kbd>P</kbd>

Maps every non-transparent pixel in scope to the nearest RGBA color included in the currently selected [palette](./palette.md).

![](./assets/graphics/palettization.gif)

## ![](https://raw.githubusercontent.com/stipple-effect/stipple-effect/master/res/icons/contents_to_palette.png) Extract canvas colors to palette

[*API function*](../api/project.md#extract_to_pal)

**Shortcut:** <kbd>Shift</kbd> + <kbd>D</kbd>

Adds every unique non-transparent color found on pixels in scope to the currently selected palette.

## ![](https://raw.githubusercontent.com/stipple-effect/stipple-effect/master/res/icons/hsv_shift.png) HSV adjustment

[*API function*](../api/project.md#hsv_shift)

**Shortcut:** <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>H</kbd>

Adjusts the colors of the pixels in scope by a user-determined hue shift, saturation shift or scale factor, and value shift or scale factor.

**Read more:**

* [HSV color model](./color.md#hsv)

## ![](https://raw.githubusercontent.com/stipple-effect/stipple-effect/master/res/icons/color_script.png) Run a color script

[*API function*](../api/project.md#color_script)

**Shortcut:** <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>W</kbd>

Applies a color transformation defined by a [color script](./color-scripts.md) to all the pixels in scope.

---

**SEE ALSO**

* [Color](./color.md)
* [Color actions shortcuts](./shortcuts.md#color-actions)
* [Color scripts](./color-scripts.md)
* [Color palettes](./palette.md)
* [Scope](./scope.md)
