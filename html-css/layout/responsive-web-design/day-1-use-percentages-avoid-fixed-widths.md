# Avoid Fixed Widths/Heights

### A website is responsive by default. 

The default width and height on a block element is 100% of the parent element. 

Setting widths or heights on an element prevents it from being responsive and you will either need to use lots of media queries to adjust the width/heights or have scroll bars appear.

#### Fixed-width on a parent

![](<../../../.gitbook/assets/image (54).png>)

#### Setting fixed-width on a child element

![](<../../../.gitbook/assets/image (53).png>)

This is expected behavior with CSS because it is trying to do its best to not lose information. For example, if there is text in the child element, it's not desirable to have it scroll, but at least the user can scroll to see the text.

![](<../../../.gitbook/assets/image (55).png>)

```css
.child {
    overflow:hidden;
}
```

You could add the property `overflow:hidden` to the child element, but then you lose the ability to read the text, which is worse.

![](<../../../.gitbook/assets/image (57).png>)
