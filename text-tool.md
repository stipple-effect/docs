# Text Tool

[`< Tools`](./tools.md)

**Icon:** ![](https://raw.githubusercontent.com/jbunke/stipple-effect/master/res/icons/text_tool.png)

**Hotkey:** <kbd>T</kbd>

## Behaviour

<!-- TODO -->

## Actions

## Modifiers

## Tool Options

## Special character sequences

*Stipple Effect* has a host of **special character sequences** that are replaced by special characters when typed. Sequences are prepended by `[+` and following by `]`, with no spaces in between. For example, the full sequence needed to produce the character *Á* (uppercase A with acute accent) is `[+A/]`.

This is the full list of currently supported sequences and special characters:

| Sequence          | Special character | Description                       |
| :---------------: | :---------------: | :-------------------------------: |
| `A/` | Á | uppercase A with acute accent |
| `a/` | á | lowercase A with acute accent |
| `E/` | É | uppercase E with acute accent |
| `e/` | é | lowercase E with acute accent |
| `I/` | Í | uppercase I with acute accent |
| `i/` | í | lowercase I with acute accent |
| `O/` | Ó | uppercase O with acute accent |
| `o/` | ó | lowercase O with acute accent |
| `U/` | Ú | uppercase U with acute accent |
| `u/` | ú | lowercase U with acute accent |
| `N/` | Ń | uppercase N with acute accent |
| `n/` | ń | lowercase N with acute accent |
| `A\` | À | uppercase A with grave accent |
| `a\` | à | lowercase A with grave accent |
| `E\` | È | uppercase E with grave accent |
| `e\` | è | lowercase E with grave accent |
| `I\` | Ì | uppercase I with grave accent |
| `i\` | ì | lowercase I with grave accent |
| `O\` | Ò | uppercase O with grave accent |
| `o\` | ò | lowercase O with grave accent |
| `U\` | Ù | uppercase U with grave accent |
| `u\` | ù | lowercase U with grave accent |
| `N\` | Ǹ | uppercase N with grave accent |
| `n\` | ǹ | lowercase N with grave accent |
| `A~` | Ã | uppercase A with tilde |
| `a~` | ã | lowercase A with tilde |
| `O~` | Õ | uppercase O with tilde |
| `o~` | õ | lowercase O with tilde |
| `N~` | Ñ | uppercase N with tilde |
| `n~` | ñ | lowercase N with tilde |
| `A^` | Â | uppercase A with circumflex |
| `a^` | â | lowercase A with circumflex |
| `E^` | Ê | uppercase E with circumflex |
| `e^` | ê | lowercase E with circumflex |
| `I^` | Î | uppercase I with circumflex |
| `i^` | î | lowercase I with circumflex |
| `O^` | Ô | uppercase O with circumflex |
| `o^` | ô | lowercase O with circumflex |
| `U^` | Û | uppercase U with circumflex |
| `u^` | û | lowercase U with circumflex |
| `A:` | ? | ??? |
| `` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |
| `?` | ? | ??? |

With the use of special character sequences, *Stipple Effect* supports the standard orthographies of the following languages:
* Afrikaans
* Albanian
* Catalan
* Danish
* Dutch
* English
* Finnish
* French
* Italian
* German
* Norwegian (Bokmål & Nynorsk)
* Portuguese
* Spanish (Castilian)
* Swedish
* Turkish
* Xhosa
* Yorùbá
* Zulu
* \+ more

Future updates will extend the special character set to support:
* Czech
* Estonian
* Hausa
* Igbo
* Polish
* Serbo-Croatian (Latin alphabet)
* Slovak
* Slovene
* \+ more


```java
// composed subdot + tone accent (Yoruba)
compositionSequenceMap.put(LSC_YO_UPPERCASE_OPEN_E_HIGH_TONE,
        makeCompositionSequence(".E/"));
compositionSequenceMap.put(LSC_YO_LOWERCASE_OPEN_E_HIGH_TONE,
        makeCompositionSequence(".e/"));
compositionSequenceMap.put(LSC_YO_UPPERCASE_OPEN_E_LOW_TONE,
        makeCompositionSequence(".E\\"));
compositionSequenceMap.put(LSC_YO_LOWERCASE_OPEN_E_LOW_TONE,
        makeCompositionSequence(".e\\"));
compositionSequenceMap.put(LSC_YO_UPPERCASE_OPEN_O_HIGH_TONE,
        makeCompositionSequence(".O/"));
compositionSequenceMap.put(LSC_YO_LOWERCASE_OPEN_O_HIGH_TONE,
        makeCompositionSequence(".o/"));
compositionSequenceMap.put(LSC_YO_UPPERCASE_OPEN_O_LOW_TONE,
        makeCompositionSequence(".O\\"));
compositionSequenceMap.put(LSC_YO_LOWERCASE_OPEN_O_LOW_TONE,
        makeCompositionSequence(".o\\"));

// subdot
compositionSequenceMap.put('Ẹ', makeCompositionSequence(".E"));
compositionSequenceMap.put('ẹ', makeCompositionSequence(".e"));
compositionSequenceMap.put('Ọ', makeCompositionSequence(".O"));
compositionSequenceMap.put('ọ', makeCompositionSequence(".o"));
compositionSequenceMap.put('Ṣ', makeCompositionSequence(".S"));
compositionSequenceMap.put('ṣ', makeCompositionSequence(".s"));

// umlaut
compositionSequenceMap.put('Ä', makeCompositionSequence("A:"));
compositionSequenceMap.put('ä', makeCompositionSequence("a:"));
compositionSequenceMap.put('Ë', makeCompositionSequence("E:"));
compositionSequenceMap.put('ë', makeCompositionSequence("e:"));
compositionSequenceMap.put('Ï', makeCompositionSequence("I:"));
compositionSequenceMap.put('ï', makeCompositionSequence("i:"));
compositionSequenceMap.put('Ö', makeCompositionSequence("O:"));
compositionSequenceMap.put('ö', makeCompositionSequence("o:"));
compositionSequenceMap.put('Ü', makeCompositionSequence("U:"));
compositionSequenceMap.put('ü', makeCompositionSequence("u:"));

// cedille / cedilha
compositionSequenceMap.put('Ç', makeCompositionSequence(",C"));
compositionSequenceMap.put('ç', makeCompositionSequence(",c"));
compositionSequenceMap.put('Ş', makeCompositionSequence(",S"));
compositionSequenceMap.put('ş', makeCompositionSequence(",s"));

// SPECIAL
// eszett - (UPPERCASE ESZETT IS NOT A LETTER!)
compositionSequenceMap.put('ß', makeCompositionSequence("ss"));
// Turkish silent Gs
compositionSequenceMap.put('Ğ', makeCompositionSequence("G("));
compositionSequenceMap.put('ğ', makeCompositionSequence("g("));
// Turkish special Is
compositionSequenceMap.put('İ', makeCompositionSequence("I."));
compositionSequenceMap.put('ı', makeCompositionSequence("i."));
// ash
compositionSequenceMap.put('Æ', makeCompositionSequence("AE"));
compositionSequenceMap.put('æ', makeCompositionSequence("ae"));
// ringed a
compositionSequenceMap.put('Å', makeCompositionSequence("A0"));
compositionSequenceMap.put('å', makeCompositionSequence("a0"));
// o with slash
compositionSequenceMap.put('Ø', makeCompositionSequence("O|"));
compositionSequenceMap.put('ø', makeCompositionSequence("o|"));
```