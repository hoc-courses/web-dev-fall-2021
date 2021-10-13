# Image

## Images - \<img>

{% hint style="info" %}
The img element is a self-closing element. There is no content allowed between the opening and closing tags, so the correct syntax is \<img/>
{% endhint %}

| Attribute | Description                                                                                |
| --------- | ------------------------------------------------------------------------------------------ |
|           | Embeds an image in the document                                                            |
| src       | The value of the src attribute can be a path to a local image or an url to a remote image. |
| alt       | An alternative to identify the content of the image for screen readers.                    |

### img element attributes

The \<img element is our first element that demonstrates the use of attributes on the element.

\<img src="images/pink-jelly.jpg" alt="jellyfish">

* **src** - the location of the image file
  * can be the relative location of an image file within the project directory
  * can also be an URL to a remote image file.
* **alt** - text used to support accessibility and search engines, or to display fallback text in case the image cannot be loaded.

### Images are inline elements

This means that they only take up as much horizontal space as their width and it can effect how the content following it behaves. For more information on how this effects the display of an images see the topic on[ Block vs Inline Elements](../../css-intro/block-vs-inline.md).

### Image Guidelines

* The best format for images are `jpeg`, `gif`, or `png`.
* Save the image in the correct size for which it will be displayed so that it doesn't waste a lot of time downloading. If you need to crop or shrink an image, sites like [www.pixlr.com](https://github.com/annechinn/html-css-gitbook-v2/tree/a7a3384c0e35ad09c9a0505d39900561a21fec26/basic-html-labs/article-progression/www.pixlr.com) are a good choice.
* Store images in a special folder, named images, within the project to keep things organized.

### Finding Place-holder Images

Just like we used place-holder text for our paragraph content, we often need place-holder images to use for development purposes. The sites [unsplash.com](http://unsplash.com) and [pexels.com ](http://www.pexels.com) are great sites that have a wide assortment of free images to use in your pages.
