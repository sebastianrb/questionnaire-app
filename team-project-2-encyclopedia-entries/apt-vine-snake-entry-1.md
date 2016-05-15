#`<div>`

*Container to group elements for styling purposes*

The `<div>` element is a block element used to define sections of a web page by grouping elements together. This grouping of elements makes it easy to position elements in a layout. The `<div>` element should be thus viewed as a container for other elements.

`<div>`s are usually given a `class` or `id` attribute, which are used to target them with CSS.

## Syntax

	<div attributes>
		/* Child elements go here */
	</div>

### Attributes 

The `<div>` tag can have all [global attributes](https://developer.mozilla.org/en/docs/Web/HTML/Element/div).

#### Class and Id

The `class` and `id` attributes are commonly used with the `<div>` tag. Their usage is illustrated in the examples below.

## Example 1

In the example below three paragraphs are wrapped in a div with the class name `container`. Giving `<div>`s a class name is a common practice. Giving them an `id` happens less frequent. `id`s are used to target specific elements, that need a different styling for example. In the example HTML code below, the last paragraph can be targeted in CSS style sheets by referring to its id `last-paragraph`.

	<div class="container">
		<div>
			<p></p>
		</div>
		<div>
			<p></p>
		</div>
		<div id="last-paragraph">
			<p></p>
		</div>
	</div>

## Example 2 - Complex

In the following example, `<div>` elements are used to divide a web page first in colums and later divide those colums into rows. Of course, merely giving `<div>` elements such a class name won't necessarily arrange the web page for you. They need to be aligned using the `display` property of CSS for example. 

	<div class="container">
		<div class="col">
			<div class="row"></div>
			<div class="row"></div>
			<div class="row"></div>
		</div>
		<div class="col">
			<div class="row"></div>
			<div class="row"></div>
			<div class="row"></div>
		</div>
		<div class="col">
			<div class="row"></div>
			<div class="row"></div>
			<div class="row"></div>
		</div>
	</div>

## Browser Support

### Desktop

| Chrome  | Firefox | Internet Explorer | Opera | Safari |
|:-------:|:-------:|:-----------------:|:-----:|:------:|
|   1.0  |   Yes   |       Yes         |  Yes  |  Yes   |

### Mobile

| Android  | Firefox Mobile | IE Phone | Opera Mobile | Safari Mobile |
|:--------:|:--------------:|:--------:|:------------:|:-------------:|
|    Yes   |        Yes     |   Yes    |      Yes     |      Yes      |


## Special Notes

`<div>`s should only be used when no semantic tag is available for the task at hand. For example, to define a navigation bar the `<nav>` element is preferred.

Because `<div>`s are block elements, they will be positioned under the previous element. This attribute can be changed by changed its display property to `inline` or `inline-block`.