# Background Image

If you’d like to set an image as the background of a web page or an HTML element, rather than simply inserting the image onto the page, then you’ll need to use the CSS **background-image** property.

{% hint style="info" %}
If you want to set an image as the background of the entire web page, then you’d have to apply CSS to the body element.
{% endhint %}

If the image is large enough, it will fill the entire page without the need for additional properties.

![](<../../.gitbook/assets/image (15).png>)

```css
background-image: url("https://images.pexels.com/photos/235767/pexels-photo-235767.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940");
```

If the image is not large enough to cover the entire page, it will repeat.

![](<../../.gitbook/assets/image (78).png>)

**background-repeat: no-repeat** - prevents the image from repeating, but leaves part of the background unfilled.

![](<../../.gitbook/assets/image (106).png>)

To ensure the image takes up the entire screen, set the **background-size** property to “cover.” To avoid the image stretching out, set the **background-attachment** property to “fixed.” That way, the image will maintain its original proportions.

![](<../../.gitbook/assets/image (126).png>)

```css
body {
  background-image: url('mouse.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
```

### Resources

{% embed url="https://www.youtube.com/watch?v=33IinMVJf-M" %}

### Object-fit

{% embed url="https://dev.to/ekaterina_vu/how-can-object-fit-property-save-you-from-misusing-the-background-images-hk0" %}

