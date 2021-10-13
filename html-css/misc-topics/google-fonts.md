# Google Fonts

Google has a collection of free fonts you can use in your web pages. This topic covers the steps to access them and include them in your pages.

## Loading a Google Font

First, search for the specific typeface you want to use. In this example, we'll search for the Poppins font. Click on the link to go to the page for the font.

![](https://raw.githubusercontent.com/hoc-labs/images/main/search-google-poppins-font.PNG)

Next, select the specific font you want to import. For example, I've selected "Extra-light 200".

![](https://raw.githubusercontent.com/hoc-labs/images/main/selected-font.png)

Next, click on the **Select this style** button to bring up the font detail box on the right.

![](https://github.com/hoc-labs/images/blob/main/selected-font-2.png?raw=true)

To include an external font, there are two methods.

* As a `<link>` element in the `<head>` section of the HTML document.
* As an @import in your stylesheet.

## Add the Import Code to Your Site

Choose the method you want to use to import the font and then copy the import code and paste it into your HTML `<head>` element if you are using the `<link>` option or at the top of your stylesheet if you are using the @import method.

{% hint style="info" %}
In the Resources section, there is a link to a discussion on stackoverflow.com that suggests that the `<link>` method is preferred.
{% endhint %}

### Resources

{% content-ref url="typography.md" %}
[typography.md](typography.md)
{% endcontent-ref %}

{% embed url="https://stackoverflow.com/questions/12316501/including-google-web-fonts-link-or-import" %}
