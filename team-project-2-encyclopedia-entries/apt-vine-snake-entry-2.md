# The `sup` Tag

**Inline Element**

*Tag used to format text as superscript*

In HTML, the `sup` tag is used to define superscript text. The word "sup" is short for superscript.

Characters formatted as superscript are smaller than standard characters and appear slightly above the normal line of type. Superscript is commonly used to render footnotes, language features, and mathematical exponents.

Here's an example of superscript alongside normally formatted text:
<pre>These are standard characters <sup>And here is some superscript</pre>

## Syntax

To format text as superscript, wrap it in `sup` tags:

```
<sup>This text will be rendered as superscript.</sup>

This text, however, will be rendered as normal, unformatted text.
```

Note `sup` elements require both an opening and closing tag.

### Attributes
the `sup` tag has no element-specific attributes and, like all elements, accommodates the set of global attributes. [Click here](#) to learn more about HTML global attributes.

## Default Styling
As noted above, superscript text is generally a fraction of the height of unformatted text and floats vertically above the normal line of characters. This is achieved via a set of default CSS declarations associated with the `sup` tag; these declarations are defined by the User Agent styles specific to each browser. Here is a selection of the CSS styling for superscript text on the Chrome browser:

```
sup {
    position: relative;
    top: -0.5em;
    font-size: 75%;
    vertical-align: baseline;
}
```

This styling effectively shrinks the `sup` element to 75% of the normal text size and then positions it at the top of the text line. Like any other element, the User Agent styles can be overwritten and new CSS can be specified by the developer to suit individual needs and preferences.

## Using Superscript

As noted, superscript is commonly used to format text used in footnotes, exponents, and language-specific grammatical features. Here are some examples of superscript in action:

Footnotes:
<pre>According to the sociologists, the cultural traditions of the tribe
were aberrant compared to those practiced throughout neighboring tribes
and the surrounding regions<sup>2</sup>.</pre>

Mathematics:
<pre>4x<sup>2</sup> + 2x - 4 = 0</pre>

Language:
<pre>Welcome, my friends, to the 21<sup>st</sup> Century!</pre>

## Compatibility

### Desktop

| Chrome  | Firefox | Internet Explorer | Opera | Safari |
|:-------:|:-------:|:-----------------:|:-----:|:------:|
|   Yes  |   Yes   |       Yes         |  Yes  |  Yes   |

### Mobile

| Android  | Firefox Mobile | IE Phone | Opera Mobile | Safari Mobile |
|:--------:|:--------------:|:--------:|:------------:|:-------------:|
|    Yes   |        Yes     |   Yes    |      Yes     |      Yes      |


## Special Notes

Similar to superscript, subscript is a text format whereby text is minimized and printed slightly below the normal line of type. To render text in subscript, rather than superscript, you can use the `sub` tag. [Click here](#) to learn more about the `sub` tag and how subscript differs from superscript.
