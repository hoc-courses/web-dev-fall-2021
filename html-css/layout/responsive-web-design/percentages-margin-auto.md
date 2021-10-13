# Percentages/Margin Auto

Using percentages and automatically calculated margins allows the content to respond correctly for a range of devices.

For example, if you set the width of the parent container to 80%, and the left and right margins to auto, then the content will adjust has the width changes so that it always takes up 80% of the screen and the specific width of the margins will be adjusted proportionately.

#### Percentages are always relative to the parent.

```css
.parent {
  width: 80%;
  margin: 0 auto;
}

.child { 
  width:50%;
  height:250px;
}
```

![](<../../../.gitbook/assets/image (60).png>)
