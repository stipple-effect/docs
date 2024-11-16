# Stipple Effect documentation

This is the documentation for *Stipple Effect*. It aims to describe in plain language how the program and all of its components work.

For the documentation of the particular behaviours of scripting functions, please read the [API](../api/).

## What is *Stipple Effect*?

*Stipple Effect* is a pixel art editor that supports animation and [scripting](./scripting.md). It is designed to support a variety of workflows and to encourage rapid, iterative creation of video game art assets and other types of artwork.

Please read the [frequently asked questions](../faq) for more information about the program.

## Getting Started

You may wish to start by familiarizing yourself with the fundamental concepts:

* [The interface](./interface.md)
* [Tools](./tools.md)
* [Projects](./project.md)
  * [State](./project.md/#state)
  * [Layer](./layer.md)
  * [Frame](./frame.md)
  * [Cel](./cel.md)
* [Selection](./selection.md)
* [Color palettes](./palette.md)

## Program Actions & Features

* [Sizing & frame control](./sizing.md)
  * [Resize](./sizing.md/#resize)
  * [Pad canvas](./sizing.md/#pad-canvas)
  * [Split sprite sheet into frames](./sizing.md/#split-a-sprite-sheet-into-frames)
  * [Stitch animation into sprite sheet](./sizing.md/#stitch-an-animation-into-a-sprite-sheet)
* [State control](./state-control.md)
  * [Undo/redo](./undo.md)
  * [History](./state-control.md/#history)
  * [Time lapse](./state-control.md/#generate-a-time-lapse)
* [Color actions](./color-actions.md)
  * [Palettization](./color-actions.md/#palettization)
  * [Extract canvas colors to a palette](./color-actions.md/#extract-canvas-colors-to-palette)
  * [HSV adjustment](./color-actions.md/#hsv-adjustment)
  * [Run a color script](./color-actions.md/#run-a-color-script)
* [Outlining](./outline.md)

## Technical

* [Scripting](./scripting.md)
  * [Automation scripts](./automation-scripts.md)
  * [Preview scripts](./preview-scripts.md)
  * [Color transformation scripts](./color-scripts.md)
  * [Child scripts](./child-scripts.md)
* [Saving & exporting](./save.md)
* [Shortcuts](./shortcuts.md)

### Theory

* [Scope](./scope.md)
* [Color](./color.md)
