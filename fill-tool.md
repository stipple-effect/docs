# Fill

[`< Tools`](./tools.md)

**Icon:** ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/fill.png)

**Hotkey:** <kbd>F</kbd>

## Behaviour

* performs a search operation that captures pixels based on how similar their color is to the pixel that initiated the operation
* replaces the color of all captured pixels with either the primary or secondary [system color](./color.md#system-colors)

## Actions

* **Fill with primary color:** ![](./assets/ui/left-click.png "Left-Click")
* **Fill with secondary color:** ![](./assets/ui/right-click.png "Right-Click")
* **Adjust tolerance:** *Arrow Keys* or <kbd>Shift</kbd> + *Scroll Wheel*

## Modifiers

* <kbd>Shift</kbd> - hold to enable **global mode**

## Tool Options

* **Tolerance:** determines how similar adjancent colors must be for the fill to spread
* **Search diagonally:** when turned on, diagonal pixels are checked for adjacency in addition to cardinally adjacent pixels.

![Adjacency diagram](./assets/theory/adjacency.png)

---

**SEE ALSO**

* [Wand](./sel-area-tools.md#wand)
