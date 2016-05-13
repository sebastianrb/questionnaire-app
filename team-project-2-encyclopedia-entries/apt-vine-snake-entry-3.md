# The `min-height` Property

The `min-height` CSS property sets the minimum height measurement an element can exhibit.

When a minimum height is set, the styled element will render at no less than the height set by the property's value; however, the element might render at greater heights, depending on the size and layout of its content and child elements.

## Syntax and Application

Here's an example of the `min-height` property styling `div` elements with the class of `tall`:

```
div.tall {
    min-height: <value>;
}
```

###Applicability
The `min-height` property can be applied to all elements except for inline elements and table elements.

### Values

The `min-height` property has a default, or initial, value of 0 and thus does not apply until set specifically by the user. In addition, this property is not inherited by any child elements.

Accepted property values:

* Pixels
* Percentages
* Inherit

#### Pixels

If the value is set in pixels, the target element will not exhibit a height of less than the specified pixel amount.

```
fieldset#form {
    min-height: 400px;
}
```

In the example above, the fieldset with ID `form` will always have a height of at least 400 pixels. The fieldset could become taller, however.

#### Percentages

If the value is set in a percentage, the target element will not exhibit a height of less than that percentage of the parent element's height.

```
fieldset#form div{
    min-height: 20%;
}
```

In the example above, any `div` element inside the `fieldset` will always have a height of at least 20% of the height of the `fieldset`. If the `fieldset` has a height of 1000 pixels, for instance, the child `div`s will exhibit a minimum height of 200 pixels (or 20% of 1000).

#### Inherit

If the value of the property is set to `inherit`, the target element will inherit the `min-height` value of the closest parent whose `min-height` value is set. If no parent is styled by the property, the target element won't inherit a minimum height.

## Example: A Parent with Minimum Height

In this example, we'll look at a parent div shaped as a pink block with the class of `parent`, and a child block-shaped div with the class of `child` inside of it.

Keep in mind that, by default, elements will automatically adjust height to fit contents and child elements.

```
        background: green;
```

## Example: A Parent with Minimum Height

Write a introduction to the example, sufficient to explain what the example is showing.

```
        background: url('path_to_image.png');
```


## Compatibility

### Desktop

| Chrome  | Firefox | Internet Explorer | Opera | Safari |
|:-------:|:-------:|:-----------------:|:-----:|:------:|
|   Yes  |   Yes   |       Yes         |  Yes  |  Yes   |

### Mobile

| Android  | Firefox Mobile | IE Phone | Opera Mobile | Safari Mobile |
|:--------:|:--------------:|:--------:|:------------:|:-------------:|
|    Yes   |        Yes     |   Yes    |      Yes     |      Yes      |
