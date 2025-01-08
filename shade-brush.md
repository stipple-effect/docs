# Shade Brush

[`< Tools`](./tools.md)

**Icon:** ![](https://raw.githubusercontent.com/stipple-effect/stipple-effect/master/res/icons/shade_brush.png)

**Hotkey:** <kbd>D</kbd>

## Behaviour

The **shade brush** works similarly to the regular [brush](./brush.md), but only replaces the color of the pixels it paints over under certain circumstances:

If a pixel's color prior to a paint operation is **included** in the active [color palette](./palette.md), the shade brush attempts to replace it with the *previous* included color (if ![](./assets/ui/left-click.png "Left-Click")) or the *next* included color (if ![](./assets/ui/right-click.png "Right-Click")) in the palette.

If the pixel's color prior to a paint operation is not included, or if there is no previous or next color in the palette, the pixel retains its color.

A pixel can only have its color shifted once per operation. Painting over the same pixel multiple times without unclicking will have no effect once the initial color update has been performed.

## Actions

* **Replace with left-adjacent color in palette:** ![Left-Click & Drag](./assets/ui/left-click-drag.gif "Left-Click & Drag")
* **Replace with right-adjacent color in palette:** ![Right-Click & Drag](./assets/ui/right-click-drag.gif "Right-Click & Drag")
* **Increment/decrement brush width:** *Arrow Keys* or <kbd>Shift</kbd> + *Scroll Wheel*

## Tool Options

* **Brush breadth:** 1px - 100px
* **Brush shape:**
  * Circle
  * Square
  * Line
    * **Angle:** slope of the brush

---

**SEE ALSO**

* [Color palettes](./palette.md)
