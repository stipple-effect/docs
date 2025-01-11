[`< Scripting`](./scripting.md)

# Child scripts

**Child script** is a catch-all categorization for a script that is executed from within another script. A script that calls a child script is known as the **parent script**. Like "child script", this is also a relative, contextually-dependent categorization.

Child scripts are useful for housing atomic chunks of work that would otherwise have to be written over and over as part of longer automation, preview, and color scripts.

**Note:**

You may run child scripts from within any script, but **it is recommended NOT to run child scripts from within [preview scripts](./preview-scripts.md) or [color scripts](./color-scripts.md)** for the sake of performance.

## Contract

*How child scripts must be structured to be accepted by the program*

Child scripts can have any type signature. However, they will trigger a runtime error if they are passed arguments that do not match the types of their [header function](./scripting.md#script-structure)'s parameters.

## Reading and executing scripts from within a script

There are two API functions that are fundamental to understanding child scripts:

### [`$SE.read_script(string filepath -> script)`](../api/global.md#read_script)

Child scripts will always exist as text files in somewhere in the file directory. They can be loaded into a running parent script with the `$SE.read_script(string filepath)` function, where the parameter `filepath` is the file path of the child script in the file directory.

**Note:**

In the interest of performance, it is best to declare any child scripts used in a script as `final` (alternatively `~`; synonymous) `script` variables outside any loops. This way, the child script will only be loaded once per its parent script's execution.

### [`script::run(A)`](../api/script.md#run) and `script::run(A) -> R`

`script` objects represent child scripts. They are executed with the `run()` function. Depending on whether the child script returns a value or not, `run()` should either be called as an [expression![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/Expression_(computer_science)) or as a [statement![](./assets/ui/external.png)](https://en.wikipedia.org/wiki/Statement_(computer_science)).

---

**SEE ALSO**

* [`script` type – API specification](../api/script.md)
