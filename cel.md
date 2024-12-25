---
title: Cel | Stipple Effect documentation
---

# Cel

[`< Projects`](./project.md)

A **cel** is an intersection of a [layer](./layer.md) and a [frame](./frame.md). A cel comprises the contents of a layer at a particular frame index.

A [project](./project.md) with 6 layers and 12 frames consists of 72 (6 x 12) cels. Thus, a project can be thought of as a matrix of cels.

The user can select a 2-dimensional range of cels by <kbd>Shift</kbd>-clicking on a **destination cel**. The range will be formed from the current cel (current editing layer at active frame index) to the destination cel. While a range of cels is selected, the **cut** (<kbd>Ctrl</kbd> + <kbd>X</kbd>) and **copy** (<kbd>Ctrl</kbd> + <kbd>C</kbd>) commands will target the range of cels rather than any pixel selection present in the project.

**Note:**

Cel ranges copied to the clipboard can only be pasted in projects with the same pixel dimensions (width and height) as the cel range.

---

**SEE ALSO**

* [Layer](./layer.md)
* [Frame](./frame.md)
* [The interface](./interface.md)
