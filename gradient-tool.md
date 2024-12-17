# Gradient Tool

[`< Tools`](./tools.md)

**Icon:** ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/gradient_tool.png)

**Hotkey:** <kbd>G</kbd>

## Behaviour

* draws a gradient from the primary to the secondary color, or vice versa
* functions either as a **brush** or as a **geometric gradient** defined by a start- and endpoint

## Actions

* **Draw gradient from primary to secondary color:** ![Left-Click & Drag](./assets/ui/left-click-drag.gif "Left-Click & Drag")
* **Draw gradient from secondary to primary color:** ![Right-Click & Drag](./assets/ui/right-click-drag.gif "Right-Click & Drag")
* **Increment/decrement brush width:** *Arrow Keys* or <kbd>Shift</kbd> + *Scroll Wheel*

## Modifiers

* <kbd>Ctrl</kbd> - hold to enable geometric mode
* **[in geometric mode]** <kbd>Shift</kbd> - snap the slope of gradient to the nearest 15° angle

## Tool Options

### Universal

* **Dithered:** when turned on, the gradient colors are determined via 4x4 ordered dithering rather than linear interpolation

### In brush mode

* **Brush breadth:** 1px - 100px
* **Brush shape:**
  * Circle
  * Square
  * Line
    * **Angle:** slope of the brush

### In geometric mode

* **Gradient shape:**
  * Linear
  * Radial
  * Spiral
* **Bounded:** when turned on, the gradient is not padded with the primary and secondary colors beyond its start- and endpoint
* **Mask:** when turned on, the gradient only replaces pixels within a certain color similarity threshold when compared with its starting point
  * **Contiguous:** when turned on, candidate pixels to be replaced by the gradient must be adjacent to other pixels that have been replaced as part of the same operation
  * **Tolerance:** determines how similar colors must be
