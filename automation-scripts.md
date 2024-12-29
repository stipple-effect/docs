---
title: Automation scripts | Stipple Effect documentation
---

# Automation scripts

[`< Scripting`](scripting.md)

As the name suggests, **automation scripts** are designed for the automation of tasks that would be repetitive and tedious to complete manually. However, their scope extends far beyond that, as they can be used to programmatically execute most program actions.

## Contract

*How automation scripts must be structured to be accepted by the program*

In addition to being valid *DeltaScript* scripts, automation scripts must have **no parameters and return nothing**. Thus, the head function of an automation script should be of the following form:

```js
() {
    // contents here...
}
```

## Example

Let us consider a scenario where a series of art assets for a game were all made with the same mistake: the artist failed to consider for a particular pixel offset that would be applied to the assets when they were imported into the game engine and animated. Now, instead of having to painstakingly pad the canvas of each of these images manually, let us consider the following automation script:

```js
() {
    project[] projects = $SE.get_projects();

    for (p in projects) {
        p.pad(0, 0, 32, 0);
        p.save();
    }
}
```

### Description

This script stores all of the projects currently open in _Stipple Effect_ into an array `projects`. It then iterates through each project `p` in the array, [pads](./sizing.md#pad-canvas) `p` canvas by 32 pixels upwards along the top edge, and [saves](./save.md) `p`.

This is one of countless examples of how automation scripts can accelerate work in *Stipple Effect*.

### Functions

This script utilizes the following API functions:

* [`$SE.get_projects()`](../se-api/global.md#get_projects)
* [`project:pad(int l, int r, int t, int b)`](../se-api/project.md#pad)
* [`project:save()`](../se-api/project.md#save)

---

**SEE ALSO**

* [Automation script examples](https://github.com/jbunke/se-script-examples/tree/main/scripts/automation)
