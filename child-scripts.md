# Child scripts

[`< Scripting`](scripting.md)

<!-- TODO -->

[Child scripts](./child-scripts.md) are merely scripts that are run from within another script. Child scripts can have any type signature, but will trigger a runtime error if they are passed arguments that do not match the types of the parameters of their [header function](#syntax).

You may run scripts from within any script, but it is recommended *NOT to run child scripts from within preview or color scripts* for the sake of performance. Also in the interest of performance, it is optimal to declare any child scripts used in a script as `final` (also `~`) `script` variables outside any loops. This way, the child script will only be loaded once per its parent script's execution.
