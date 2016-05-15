# Margin

*Shorthand CSS property to set space around elements*

The `margin` property is the outermost element of the box model. It creates space around an element's border.

The `margin` property is used to set the top, right, bottom and left margin of an HTML element in one line as opposed to declaring `margin-top`, `margin-right`, `margin-bottom` and `margin-left` seperately.

Setting values for `margin` works clockwise: the first value that is specified is the top margin, the second value is the right margin, the third value is the bottom margin and the fourth value is the left margin.

Even though `margin` is already a shortcut property, its syntax can be minimalized even further. If the left and right margins have the same values, you could declare `margin` with only three values for example (top, horizontal and bottom). There are four possible forms of using `margin`:

* `margin: top right bottom left`   
* `margin: top horizontal-margins bottom` 
* `margin: vertical-margins horizontal-margins`
* `margin: all-margins`
	
The usage of all forms is illustrated in the examples below.

## Syntax

	margin: <length | percentage | auto | initial | inherit> ;

### Values

#### length

To set a fixed width on an element, the `length` value is used. Both absolute and relative units can be used to express a `length`. The most commonly used units are `em`/`rem` (relative) and `px` (absolute). The `em` and `rem` values are relative to the parent element's font size and the root element's (e.g. `<html>`) respectively. 

Negative values are allowed here and do what is expected: move an element to the the side of the specific margin. So `margin: 0 0 -5px 0` would 'absorb' the element into the bottom.

#### percentage

A percentage value will set the margin of an element to a percentage of its parent element. For example, a paragraph with a margin of 10% inside a div with a width of 100px wil have margins of 10px.

#### auto

The `auto` value tells a margin to use all available space left. It doesn't work on inline elements, floated elements and absolute elements. `auto` will also not work on a block element withouth a specified `width`. Lastly, it will only work on horizontal margins (left and right). When auto is used for vertical margins, it will set those margins to 0px (except on absolute elements).

The `auto` value can thus be used to set the left and right margin of block elements evenly, which will result in the element being centered. It will let the left and right margins increase, until the element is centered horizontally (in alignment with the y-axis of the viewport). To center a `<div>` element for example, the `auto` value could be used in the following way: `margin: 0 auto;`. Note that the `0` actually doesn't even need to be specified, since the browser will set it to 0 automatically when `auto` is applied to a vertical margin.

#### initial

`initial` will set the `margin` property to its default value. 

You may wonder why you would want to set this value. If you want the default value, you wouldn't change the `margin` property in the first place. A good example when you would want to use this value is when a class overwrote the margin of an element, but you didn't want a particular element's margin to change. In that case, you could target the element and set its `margin` value to `initial`, which changes it back to the default value.

#### inherit

The `inherit` value takes the `margin` of the parent element and applies it to the element.

## Example 1

This will set the top margin to 5px, the right margin to 10px, the bottom margin to 15px and the left margin to 8px (notice the clockwise pattern).

	margin: 5px 10px 15px 8px;

## Example 2

This example will set the top margin to 5px, the right and left margin to 10px and the bottom margin to 15px;

	margin: 5px 10px 15px;
	
## Example 3

When two values are specified, the first value, 5px in this case, sets the margin for the top and bottom. The second value sets the right and left margin.

	margin: 5px 10px;

## Example 4

When only one value is specified, this value will be the margin for all four sides (top, right, bottom, left). In this case, all margins will be 5px.

	margin: 5px;
	
## Example 5 - Complex

This example will set the top margin to 30px and the bottom margin to 0px (note that no unit needs to be specified when the margin is 0). The left margin will be three times as big as that of its parent element (3em). The right margin will be as big as it needs to be to fill up the remaining space, which is what `auto` does. In case you are wondering: yes, this will very likely look like the element is 'floated' to the left (unless it has an unusually large left margin).

	margin: 30px auto O 3em;

## Browser Support


### Desktop

| Chrome  | Firefox | Internet Explorer | Opera |    Safari   |
|:-------:|:-------:|:-----------------:|:-----:|:-----------:|
|   1.0   |   1.0   |       3.0         |  3.5  |  1.0 (85)   |

**Note**: The `auto` value works from Internet Explorer 6.0 (strict mode).

### Mobile

| Android  | Firefox Mobile | IE Phone | Opera Mobile | Safari Mobile |
|:--------:|:--------------:|:--------:|:------------:|:-------------:|
|    1.0   |        1.0     |   6.0    |      6.0     |      1.0      |

## Special Notes

Vertical margins of block elements may collapse into a single margin (the margin of whichever element has the largest margin). This happens in the following cases:
	
* Two adjacent siblings (elements directly following each other) have their margins collapsed.

* Empty block elements (no border, padding, inline content, `height` or `min-height` to separate the top margin of an element from its bottom margin) have their margins collapsed as well.

* A parent element and its first child have their top margins collapsed when no border, padding, inline content or clearance separates the top margin of the parent element and that of the child element. The margin becomes the largest of the two elements and ends up outside of the parent element.

* A parent element and its last child have their bottom margins collapsed when no border, padding, inline content, (`min-/max-`)`height` separates the bottom margins of the two.

The parent/child cases can be solved in a variety of ways.

* Floating either the parent or child element.
* Making either the parent of child an inline element.
* Setting the `overflow` property of the parent element to `auto`.


