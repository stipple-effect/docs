# Color scripts

[`< Scripting`](./scripting.md)

**Color scripts** are used to define the behaviour of the [script brush](./script-brush.md) ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/script_brush.png) tool and the ["run a color script"](./color-actions.md#run-a-color-script) ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/color_script.png) color action. They describe a **color to color transformation**.

**Note:**

They may be written to produce [side effects](https://en.wikipedia.org/wiki/Side_effect_(computer_science)), though this will adversely impact performance.

## Contract

*How color scripts must be structured to be accepted by the program*

In addition to being valid *DeltaScript* scripts, color scripts must take a single `color` parameter<sup>1, 2</sup> and return a `color`. Thus, the head function of a color script should be of the following form<sup>3</sup>:

```js
(color c -> color) {
    // contents here...
}
```

**Note:**

<sup>1</sup> - The parameter name `c` is merely used as an example.

<sup>2</sup> - The parameter represented by `c` can optionally be declared as immutable by prepending `final` or `~` to the declaration. For example:

```js
(~ color c -> color) { /* contents here... */ }
```

<sup>3</sup> - Color scripts do not need to have complex function bodies `{ ... }`. For example, the following color script is valid:

```js
(color c -> color) -> rgb(c.r, 0, c.b / 2)
```

## Example

```js
(~ color c -> color) {
    ~ int total = c.r + c.g + c.b;
    ~ int avg = total / 3;

    return rgba(avg, avg, avg, c.a);
}
```

### Description

This script takes the input color `c` and returns a shade of grey with the same lightness as `c` (black or white in extreme cases). This is done by averaging out `c`'s red, green and blue color channels.

### Functions

This script does not utilize any functions from the scripting API.

However, it makes use of the `rgba(int r, int g, int b, int alpha) -> color` function from the *DeltaScript* base language [standard library](https://github.com/jbunke/deltascript). <!-- TODO - GitHub link to SL and to specific function -->

---

**SEE ALSO**

* [Color script examples](https://github.com/jbunke/se-script-examples/tree/main/scripts/color)
