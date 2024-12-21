# Selection movement tools

[`< Tools`](./tools.md)

## Universal

The **move selection** and **pick up selection** behave almost identically. The only difference is that the move selection tool modifies the *selection area*, while the pick up selection tool modifies the *contents of the selection*.

### Actions

* ![Click & Drag](./assets/ui/click-drag.gif "Click & Drag") - depending on the cursor position...
  * *within or outside selection* - **move selection**
  * *hovering over a transform node* - **stretch selection**
  * *around a transform node* - **rotate selection**
* *Arrow Keys* - **move selection**

### Modifiers

* <kbd>Shift</kbd> - hold to snap the [translation](https://en.wikipedia.org/wiki/Translation_(geometry)) to the nearest multiple of the selection dimensions
* <kbd>Ctrl</kbd> + <kbd>Shift</kbd> - hold to snap the translation to the top left of the occupying pixel grid cell<sup>1</sup>

<sup>1</sup> - only works when the [pixel grid]() is turned on and the selection is being moved by ![Click & Drag](./assets/ui/click-drag.gif "Click & Drag")

## Move selection

**Icon:** ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/move_selection.png)

**Hotkey:** <kbd>M</kbd>

## Pick up selection

**Icon:** ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/pick_up_selection.png)

**Hotkey:** <kbd>U</kbd>
