# Automation scripts

[`< Scripting`](scripting.md)

<!-- TODO -->

### Overview
Automation scripts are designed to reduce the tedium of work that could be simplified by automation.

For example, let us consider a scenario where a series of art assets for a game were all made with the same mistake: the artist failed to consider for a particular pixel offset that would be applied to the assets when they were imported into the game engine and animated. Now, instead of having to painstakingly pad the canvas of each of these images individually, let us consider the following automation script:
```js
() {
    project[] projects = $SE.get_projects();

    for (project p in projects) {
        p.pad(0, 0, 32, 0);
        p.save();
    }
}
```
This script stores all of the projects currently open in _Stipple Effect_ into an array `projects`. It then iterates through each project `p` in the array, pads the project canvas by 32 pixels upwards, and saves the modified project again.

This is one of countless examples of how automation scripts can accelerate work in _Stipple Effect_.

### Contract

Automation scripts must have no parameters and return nothing. Thus, the head function of an automation script should be of the following form:
```js
() {
    // contents here...
}
```

### More
* [Automation script examples](https://github.com/jbunke/se-script-examples/tree/main/scripts/automation)
