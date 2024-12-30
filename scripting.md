# Scripting

[`< Overview`](./README.md)

*Stipple Effect* lets users write scripts for a range of applications. A **script** is a short series of instructions for the program to execute.

## DeltaScript

*Stipple Effect* scripts are written in a scripting language called [*DeltaScript*](https://github.com/jbunke/deltascript), which was designed by the developer of the program. *DeltaScript* is described as a **lightweight scripting language skeleton**. This means that the *DeltaScript* base language is easy to learn, with only essential functions in its standard library. <!-- TODO - standard library link -->

The language was also designed to be **powerful**, **expressive**, and **concise**. The syntax is concise and devoid of [boilerplate](https://en.wikipedia.org/wiki/Boilerplate_code), and has many shorthands to make scripts shorter without sacrificing readability. It should also be familiar to users with prior programming experience, as the **syntax is similar to other [C-family languages](https://en.wikipedia.org/wiki/List_of_C-family_programming_languages) like C++, Java, JavaScript, and Go**.

**Do not be discouraged if you have little to no programming experience, or if you are hesitant about learning a new language.** There are plenty of resources to familiarize yourself with scripting in _Stipple Effect_, including:

* [Script examples with explanations](https://github.com/jbunke/se-script-examples)
* [DeltaScript language specification](https://github.com/jbunke/deltascript/blob/master/docs/lang-spec.md)
* [*Stipple Effect* YouTube playlist (w/ tutorials)](https://www.youtube.com/playlist?list=PLy71S74rTLnPEwYYtAXvh2er8QBvWIwRL)

## API

*DeltaScript* is designed to be extended for the needs of the individual applications that utilize it. As the base language is quite bare, most of the powerful scripting functionality for *Stipple Effect* is defined in the **scripting API** - *Stipple Effect*'s extension of *DeltaScript*. You can read the API specification [here](../api/).

## Types of scripts

Scripts in *Stipple Effect* scripts fall into the following categories:

* [Automation scripts](./automation-scripts.md) - automate tasks and execute actions programmatically
* [Preview scripts](./preview-scripts.md) - transform the contents of the [project](./project.md) that are displayed in the [preview window](./preview-window.md)
* [Color scripts](./color-scripts.md) - color to color transformations for the [script brush](./script-brush.md) ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/script_brush.png) tool and the ["run a color script"](./color-actions.md#run-a-color-script) ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/color_script.png) color action
* [Child scripts](./child-scripts.md) - catch-all term for scripts executed from within other scripts

## Getting Started

### Script files and text editor

Script files use the file extension `.ses`. They can be written in the text editor of your choosing. However, **[Visual Studio Code](https://code.visualstudio.com/) (VS Code) is recommended** because of the [*DeltaScript for Stipple Effect* syntax highlighting extension](https://marketplace.visualstudio.com/items?itemName=jordanbunke.deltascript-for-stipple-effect) that is distributed on the VS Code Marketplace.

### Script structure

Scripts consist of a nameless header function, optionally followed by **named helper functions**. The type signature of the script is the type signature of its header function. Functions can optionally accept parameters and return a value of a specified return type, **though neither are required**.

```js
// header function - this is the entry point of the script's execution
// * has a single parameter "letters"
// * returns a string
(int letters -> string) {
    string word = "";

    for (int i = 0; i < letters; i++)
        word += random_letter();

    return word;
}

// helper function "random_letter"
// * has no parameters
// * returns a char
random_letter(-> char) {
    ~ int MIN = (int) 'a';
    ~ int MAX_EX = ((int) 'z') + 1;

    // "rand" is a function defined by the DeltaScript standard library
    return (char) rand(MIN, MAX_EX);
}
```

A full breakdown of the syntax and semantics of *DeltaScript* can be found in the [language specification](https://github.com/jbunke/deltascript/blob/master/docs/lang-spec.md).

---

**SEE ALSO**

* [Script examples](https://github.com/jbunke/se-script-examples)
* [*DeltaScript for Stipple Effect* - VS Code syntax highlighting extension](https://marketplace.visualstudio.com/items?itemName=jordanbunke.deltascript-for-stipple-effect)
* [Stipple Effect video playlist (w/ tutorials)](https://www.youtube.com/playlist?list=PLy71S74rTLnPEwYYtAXvh2er8QBvWIwRL)
