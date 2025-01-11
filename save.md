[`< Overview`](./README.md)

# Saving & Exporting

In addition to saving [projects](./project.md) to *Stipple Effect*'s native file type, users have several export options depending on whether a project is [static or an animation](./frame.md), and for which purposes they intend to use or distribute an asset.

## Native file type

The native file type for *Stipple Effect* projects has the file extension `.stip`. When a project is saved to a STIP file, all of the current project [state](./project.md#state)'s data is saved. This includes pixel [color](./color.md) data, [layer](./layer.md), [frame](./frame.md) and [cel](./cel.md) data, as well as metadata like frame durations, onion skin configurations, etc.

Assets that are works in progress should **always be saved as STIP files**. It is wise to save finished assets as STIP files as well, so that they can be referenced or edited in the future.

## Exporting

Saving a project to any other file type than STIP is considered an **export**. Supported export file types in *Stipple Effect* are widely supported image or video file formats.

### Export formats

**Single PNG:**

For exporting a static project as a [PNG image![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/PNG). PNG images preserve transparency.

**Sprite sheet:**

Exports an animation as a PNG sprite sheet.

**Separate PNGs per frame:**

Exports an animation as a series of separate image files. Files have a shared name segment and are distinguished by a numbered suffix. The user can configure from which index the suffixes should start.

**Animated GIF:**

Exports an animation as an [animated GIF image![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/GIF#Animated_GIF).

**MP4 Video:**

Exports an animation as an [MP4 video![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/MP4_file_format). This is a [lossy compression![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/Lossy_compression) export.

### Export options

**All formats:**
* **Scale factor:** Scale the canvas up by an integer ranging from 1x to 20x. This is useful for assets intended for online distribution on sites not specifically designed for pixel art, such as Twitter. **As a general rule, game assets should NEVER be scaled up.**

**Animation:**
* **Limited range of frames:** When turned on, the user can define a lower and upper bound and only export frames in that range. Turning it off will export all frames.
* **Sprite sheet:**
  * **Sequence order:** Whether to sequence frames onto the sprite sheet vertically (top-to-bottom, left-to-right) or horizontally (left-to-right, top-to-bottom).
  * **Frames per row/column:** How many frames to sequence in the sprite sheet's primary sequencing axis. Whether this applies to rows or columns is determined by the **sequence order** option. The amount of frames to sequence along the complementary axis is inferred.
* **GIF / MP4:**
  * **Frame rate:** The speed of the animation in standard frames per second. Note that a frame with a [relative duration](./frame.md#relative-duration) other than 1x will have its duration scaled accordingly in the export.

## Save associations

Saving a project in *Stipple Effect* for the first time, as well as opening/importing a project, will create a **save association**. Projects with save associations can be **quick-saved** ![](https://raw.githubusercontent.com/stipple-effect/stipple-effect/master/res/icons/save.png) (<kbd>Ctrl</kbd> + <kbd>S</kbd>) without requiring additional save configuration. Opening the **Save As...** ![](https://raw.githubusercontent.com/stipple-effect/stipple-effect/master/res/icons/save_as.png) dialog menu (<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd>) and making changes will overwrite a project's save association.

Projects will be saved or exported according to what their save association dictates. For example, if a PNG is imported into *Stipple Effect*, quick-saving it will re-export it to the same filepath as a PNG and overwrite the file that was imported.

---

**SEE ALSO**

* [Project shortcuts](./shortcuts.md#projects)
