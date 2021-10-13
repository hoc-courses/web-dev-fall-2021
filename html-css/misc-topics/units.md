# Units

There are two types of units: absolute and relative units.

* **Absolute units** are always the same size, even when the user zooms in on the browser.
* **Relative units** are based on the size of something else, such as the font size or viewport size. When the user zooms in the browser, elements using relative units will increase in size too.

The following table contains some of the most commonly used CSS units.

| Unit   | Relative or absolute | Description                                                                                                           |
| ------ | -------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `rem`  | Relative             | 1rem is equal to the font size of the root element. If the root font size is 16px, then 1rem = 16px and 0.5rem = 8px  |
| `em`   | Relative             | 1em is equal to the font size of the parent element. If the parent font size is 16px, then 1em = 16px and 0.5em = 8px |
| `%`    | Relative             | 100% is equal to the full width or height of the parent element. Mainly used for widths.                              |
| `px`   | Absolute             | 1px is 1/96th of 1 inch                                                                                               |
| vh, vw | Relative             | 100% is equal to the full width or height of the viewport.                                                            |

There are many CSS properties whose value represents a length. For example, width, margin, padding, font-size all expect a length value. But lengths can be expressed in different units and it is important to know the differences between them.

If you want to view all CSS units, visit the [MDN CSS values and units page](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Values_and_Units#numeric_data_types).

{% hint style="info" %}
Some users who find it difficult to read small text will use the browser zoom to increase the content size. Since absolute units do not increase in size with browser zoom, we should use relative units whenever possible. Therefore, we should **prefer** using `rem` and `%`, and **avoid** using `px`.
{% endhint %}

## Absolute Units (px)

Absolute units are not relative to anything else and generally stay the same size. They are not affected by any screen size or fonts.

**Pixels - px (**1px = 1/96th of 1 inch) are the absolute unit that is used in web design. Pixels are very easy to use, because they specify the exact length. But they are **not a good choice for accessibility**. For example, if you increase your font to large in your browser settings, your hard-coded absolute font-sizes will not change.

## Font-relative Units (em and rem)

**em -** Em inherits size from its immediate parent’s font size. Say, if a parent element has font-size:18px, then 1em will be measured as 18px for all its child’s.

The advantage of using em is, if you decide to change the font-size, padding, and margin of each element proportionately, then you just have to change the parent element font size and all other elements will adjust accordingly.

That won’t be the case with absolute units like px, where you have to adjust each element individually.

**rem** - rem units always refer to the root element font size, not the parent element.

## Resources

{% embed url="https://youtu.be/_-aDOAMmDHI" %}



{% embed url="https://getflywheel.com/layout/choose-css-unit-create-better-site-layouts-how-to/" %}

