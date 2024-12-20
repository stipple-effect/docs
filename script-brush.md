# Script Brush

[`< Tools`](./tools.md)

**Icon:** ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/script_brush.png)

**Hotkey:** <kbd>Q</kbd>

## Behaviour

The **script brush** is used to apply custom color transformations. It requires a [color script](./color-scripts.md) to define its behaviour.

## Actions

* **Replace existing color:** ![Click & Drag](./assets/ui/click-drag.gif "Click & Drag")
* Use system colors as input
  * **Use primary color as input:** <kbd>Shift</kbd> + ![Left-Click & Drag](./assets/ui/left-click-drag.gif "Left-Click & Drag")
  * **Use secondary color as input:** <kbd>Shift</kbd> + ![Right-Click & Drag](./assets/ui/right-click-drag.gif "Right-Click & Drag")
* **Increment/decrement brush width:** *Arrow Keys* or <kbd>Shift</kbd> + *Scroll Wheel*

## Tool Options

* **Brush breadth:** 1px - 100px
* **Brush shape:**
  * Circle
  * Square
  * Line
    * **Angle:** slope of the brush
* **Color script:** upload a DeltaScript `color -> color` script to define the brush's behaviour

---

**SEE ALSO**

* [Color scripts](./color-scripts.md)
* [Scripting](./scripting.md)
