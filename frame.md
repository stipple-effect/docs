---
title: Frame | Stipple Effect documentation
---

# Frame

[`< Projects`](./project.md)

A **frame** is a snapshot of an animation. Multi-frame [projects](./project.md) are considered **animations**, while a project with a single frame is **static**.

Frames are *Stipple Effect* projects' horizontal organizational axis. Conversely, [layers](./layer.md) make up the vertical axis. The intersection of a particular frame and a particular layer is called a [cel](./cel.md).

## Relative duration

Frames have a default relative duration of **1.0x**. This number is a multiple of how long a frame is displayed during playback relative to a standard frame.

For example, if the playback speed in *Stipple Effect* is set to 10 frames per second, a frame with a relative duration of 1.6x will be displayed for 160 milliseconds during playback. This is because a standard frame at 10 FPS would be displayed for 100 milliseconds, and 160 is 1.6x that duration.

## Playback modes

*Stipple Effect* supports the following playback modes:
* ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/forwards.png) Forwards
* ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/backwards.png) Backwards
* ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/loop.png) Loop
* ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/pong.png) Ping-pong - playback direction changes when the first and last frames are reached

**Note:**

These playback modes are merely internal. When projects are [exported](./save.md) as GIFs or videos, their frames are sequenced in ascending numerical order.

## Frame actions

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/new_frame.png) Add new frame

[*API function*](../se-api/project.md#add_frame)

**Shortcut:** <kbd>Ctrl</kbd> + <kbd>F</kbd>

Adds a new frame to the project directly after the current active frame. The new frame becomes the new active frame.

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/duplicate_frame.png) Duplicate frame

[*API function*](../se-api/project.md#duplicate_frame)

**Shortcut:** <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>F</kbd>

Duplicates the current active frame of project and inserts the duplicate directly after the initial frame. The duplicate frame becomes the new active frame.

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/remove_frame.png) Remove frame

[*API function*](../se-api/project.md#remove_frame)

**Shortcut:** <kbd>Ctrl</kbd> + <kbd>Backspace</kbd>

Removes the current active frame of the project. If the frame to be removed is the first frame, the active frame becomes the new first frame after the removal. Otherwise, the new active frame is the frame that preceded the frame that was removed.

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/move_frame_back.png) Move frame back

[*API function*](../se-api/project.md#move_frame_back)

**Shortcut:** <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + *Left Arrow Key*

Swaps the active frame of the project with the preceding frame.

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/move_frame_forward.png) Move frame forward

[*API function*](../se-api/project.md#move_frame_forward)

**Shortcut:** <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + *Right Arrow Key*

Swaps the active frame of the project with the following frame.

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/frame_properties.png) Frame properties menu

**Shortcut:** <kbd>Shift</kbd> + <kbd>F</kbd>

Opens the frame properties menu. This menu allows users to configure a frame's relative duration.

## Playback actions

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/to_first_frame.png) To first frame - <kbd>Ctrl</kbd> + *Left Arrow Key*

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/previous.png) Previous frame - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Space</kbd>

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/play.png) Play / ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/stop.png) Stop - <kbd>Space</kbd>

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/next.png) Next frame - <kbd>Ctrl</kbd> + <kbd>Space</kbd>

### ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/to_last_frame.png) To last frame - <kbd>Ctrl</kbd> + *Right Arrow Key*

### Cycle playback mode - <kbd>Ctrl</kbd> + <kbd>Enter</kbd>

---

**SEE ALSO**

* [Frame shortcuts](./shortcuts.md#frames)
* [Cel](./cel.md)
* [Layer](./layer.md)
* [The interface](./interface.md)
