# Anatomy of a Web Page

## First HTML Documents

In 1980, physicist Tim Berners-Lee, proposed a system for researchers to share documents. Ten years later, he specified the **HTML** language and wrote the browser and server software for the first operational system.

It consisted of a communication system between web browsers and servers where a user could request a document with a unique resource ID (URL) from a web server, and the web server would respond to the request and return the document to the browser to display.

Embedded within the text of the document were **hyper-links** to other documents so that it was possible to refer to other documents and simply click on the link to switch to viewing the new document.

![](<../../.gitbook/assets/image (201).png>)

## **Modern Web Pages**

Modern web pages have progress a long way since those early days and now depend on two additional technologies: **CSS** and **JavaScript**. These four components provide the underpinning of every web page.

| Technology     | Description                                                                                        |
| -------------- | -------------------------------------------------------------------------------------------------- |
| **TEXT**       | The content/information the document wants to display.                                             |
| **HTML**       | **Hypertext Markup Language**. A _mark-up language_ to describe the content of web pages           |
| **CSS**        | **Cascading Style Sheet** - A _stylesheet language_ used to express the presentation of web pages. |
| **JavaScript** | A **programming language** used for both front-end and back-end development to add interactivity.  |

![](<../../.gitbook/assets/image (59).png>)

**TEXT:** a web page document starts out as just text content.

![](<../../.gitbook/assets/image (113).png>)

**HTML:** markup is used to give structure to the content. Markup elements are used to annotate the text to specify formatting such as headings, lists and hyper-links.

![](<../../.gitbook/assets/image (264).png>)

**CSS:** specifies rules to change style properties on selected HTML elements. CSS code is typically stored in a separate file and pulled into the HTML document. CSS is embedded in the HTML document here to make viewing it on one screen easier.

![](<../../.gitbook/assets/image (217).png>)

**JAVASCRIPT**: adds interactivity to the page. For example, you could bring up a video in a popup window when the user clicked on one of the jelly fish images (the code is a little too involved to display here, but you get the idea). JavaScript code, like CSS, is typically stored in an external document and pulled into the HTML document when it is being loaded.

## Examples of CSS and JavaScript

## CSS - CSSZenGarden.com

The site [csszengarden.com](http://csszengarden.com) is a site that educates on the role CSS plays in design and has a link to provide both the HTML and CSS files separately and to view the impact CSS can make.

Go to the site, and click on the HTML FILE link to download the HTML file. Then display that file in your browser by dragging in from your file explorer to a web browser window.

![](<../../.gitbook/assets/image (131).png>)

Below is the HTML with no CSS applied. Very basic, just text, links, and some standard headings.

![](<../../.gitbook/assets/image (13).png>)

### What a Difference CSS can Make!

Next, click on the VIEW ALL DESIGNS link and browse through each of the different design links on the right. Each of these designs has the exact same underlying HTML content, just a different stylesheet!

**Note**: These examples on the site are periodically updated, so these may not represent what is currently on the site.

![](<../../.gitbook/assets/image (52).png>)

![](<../../.gitbook/assets/image (119).png>)

![](<../../.gitbook/assets/image (132).png>)

## JavaScript - Programming/Interactivity

JavaScript is a programming language that enables web pages to provide animation, interactivity, and the relatively recent advances that makes websites behave more like desktop applications.

### JavaScript - Animation

JavaScript can be used to add what I'd call eye-candy to the site. The content is all there, but it's dull without some action. JavaScript can be used to display the content in visually appealing ways and add movement with advanced animations.

{% embed url="https://britishmuseum.withgoogle.com/" %}

{% embed url="https://artsandculture.google.com/exhibit/vincent-van-gogh-s-love-life/0QKiJEq7eauIKg?hl=en" %}

{% embed url="https://www.legworkstudio.com" %}

{% embed url="https://www.sbs.com.au/theboat/" %}

{% embed url="https://mrdoob.com/projects/chromeexperiments/ball-pool/" %}

## JavaScript - Single Page Applications

In the last ten years there's been a huge change in how web sites update their content. It used to be that a web site consisted of a collection of individual pages with hyper-links between them. Clicking on a hyper-link would initiate a request to the web server for the new page and that page would be retrieved and replace the current page in the browser. It's what the technology at the time allowed, but web sites felt clunky and disjointed.

With advances in how web applications communicate between the client and server, it is now possible for most web applications to mimic a desktop experience in that there isn't the constant refreshing of the web site as new pages are requested from the server. For example, Gmail, Google Maps, Google Drive, Twitter and Facebook all feel like real applications, but on the web.

A single page application creates the illusion of a page change, but you are actually on the same page the entire time you are on the site. The URL is changing as you navigate around the site, even though no new page is being loaded from the server. Behind the scenes, data is being passed between the client and server to make this happen.

**Google Search Input** - A really good example of this is the Google Search screen. As the user types into the search input box, JavaScript is being used to communicate with the server and seamlessly retrieve and present relevant search strings based on what the user is typing.

{% hint style="info" %}
Take a look at the Console Developer Tools Network Tab to see the network traffic.
{% endhint %}

![](<../../.gitbook/assets/image (17).png>)

**NY Times** - **Article Comments**

Another example is how the comments section immediately appears when the user clicks on the button to read the comments.

JavaScript responds to the button click, sends as request to the server for all of the comments for the article, and then, without updating the entire page, inserts the new section for the user to interact with the comments.

{% embed url="https://www.nytimes.com/2021/04/06/dining/croissant-recipes.html" %}
