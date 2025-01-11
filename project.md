---
title: Project | Stipple Effect documentation
---

[`< Overview`](./README.md)

# Project

A *Stipple Effect* session consists of one or multiple **projects**. Projects are sometimes referred to – especially in the [source code![](./assets/ui/external.png)](https://github.com/stipple-effect/stipple-effect) – as **contexts**.

The projects that are currently loaded in the program are arranged in the [projects panel](./interface.md#projects).

Projects have a [save association](./save.md) that determines their destination folder, name, file type, and more.

Projects consist of a sequence of [states](#state).

## State

A **project state** is a snapshot of a project at a particular point in its [history](./state-control.md#history). Every time a project is edited, its state changes. 

A state is comprised of [layer](./layer.md), [frame](./frame.md), and [selection](./selection.md) data, along with metadata that tells the program about the operation that resulted in the most recent state change. When a project is saved or exported, only its active state is saved.

---

**SEE ALSO**

* [State control](./state-control.md)
* [Saving & exporting](./save.md)
* [Scope](./scope.md)
