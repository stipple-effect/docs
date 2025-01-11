[`< Overview`](./README.md)

# Fonts

*Stipple Effect* uses the underlying [*Delta Time*![](./assets/ui/external.png)](https://github.com/jbunke/delta-time) library to load and display fonts. Thus, the program's native system fonts, as well as user-defined fonts uploaded for use by the [text tool](./text-tool.md) at runtime, must comply with Delta Time's **font standard**.

## Font files

### Format

*Stipple Effect* font files must have the following dimensions:

* **Width:** multiple of 319px
* **Height:** multiple of 303px

### Parsed pixel colors

* **Red** (`#ff0000`) - parsed as part of the [glyph![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/Glyph) associated with its bounding box
* **Green** (`#00ff00`) - parsed as left- or right pixel boundary of the glyph associated with its bounding box *at that particular pixel height*

**Read more:**
* [Color hex codes![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/Web_colors#Hex_triplet)

### Boundary enforcement

Explicitly defining boundaries using the color green can a few applications, including:

* defining [monospaced![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/Monospaced_font) fonts

![Monospaced and proportional font comparison](./assets/theory/monospacing.png "Monospaced and proportional font comparison")

* enforcing spacing for sequences of characters that would otherwise overlap or interlock

![How characters may interlock or overlap if boundaries are not explicitly defined](./assets/theory/spacing.png "How characters may interlock or overlap if boundaries are not explicitly defined")

## Character sets

Fonts support following **character sets**:

* [ASCII![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/ASCII#Printable_character_table)

![Default ASCII set provided by Stipple Effect as a template](./assets/theory/ascii.png)

* Latin Extended

![Default Latin Extended set provided by Stipple Effect as a template](./assets/theory/latin-extended.png)

Future updates will aim to extend the characters supported by fonts, which will eventually mean additional character sets.

The ASCII character set is must be provided by user-defined fonts. Additional character sets are optional.

## Uploading fonts

Fonts can be uploaded while using the [text tool](./text-tool.md) with <kbd>Shift</kbd> + <kbd>T</kbd>, or by clicking on ![](https://raw.githubusercontent.com/stipple-effect/stipple-effect/master/res/icons/new_font.png) in the [tool options bar](./interface.md#tool-options).
