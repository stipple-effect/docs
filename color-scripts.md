# Color scripts

[`< Scripting`](scripting.md)

<!-- TODO -->

### Overview
Color scripts are used to defined custom color action behaviour. Examples of color actions in _Stipple Effect_ are HSV level shifting and palettization. These target a scope of the project, whether it be a layer, the selection, a frame, the layer-frame, or the entire project, and then apply a transformation to the colors of the pixels in the targeted scope. Executing a color script is a more generalized framework of this behaviour, whereby users can programmatically specify the input to output color mapping.

Example:
```js
(~ color c -> color) {
    ~ int total = c.r + c.g + c.b;
    ~ int avg = total / 3;

    return rgb(avg, avg, avg, c.a);
}
```
This script takes the input color `c` and returns a shade of grey (or black or white in extreme cases) with the same lightness as `c`.

### Contract

Color scripts must have take a single `color` parameter<sup>a, b</sup> and return a `color`. Thus, the head function of a color script should be of the following form<sup>c</sup>:
```js
(color c -> color) {
    // contents here...
}
```

<sup>a</sup> - The parameter name `c` is just used as an example.

<sup>b</sup> - The parameter represented by `c` can optionally be declared as immutable by prepending `final` or `~` to the declaration. For example:
```js
(~ color c -> color) { /* contents here... */ }
```

<sup>c</sup> - Color scripts do not have to have complex function bodies `{ ... }`. For example, the following preview script is valid:
```js
(color c -> color) -> rgb(c.r, 0, c.b / 2)
```

### More
* [Color script examples](https://github.com/jbunke/se-script-examples/tree/main/scripts/color)
