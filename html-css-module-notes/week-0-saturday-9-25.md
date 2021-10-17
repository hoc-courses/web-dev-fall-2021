# Week 0: Saturday 9/25

### Design Patterns

#### Use a container class to control content width, left/right margins, max-width

Don't use hard-coded widths, except for max-width. Use a percentage and auto left/right margins.

```css
.container {
  width:80%;
  margin: 0 auto;
  padding:40px 0;
  max-width:800px;
}
```

![](<../.gitbook/assets/image (71).png>)

#### Use Padding to get uniform space within a parent of multiple children (except when using flexbox.

Flexbox ignores padding/margins of children, so you can use the flex justify-content and align-items to get the correct layout.

![](<../.gitbook/assets/image (75).png>)

![](<../.gitbook/assets/image (76).png>)

![](<../.gitbook/assets/image (77).png>)

### Review Past Assignments from [Thursday](week-1-thursday-9-23.md)
