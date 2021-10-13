# Text-formatting Elements

| Purpose         | Element                | Description                              | Self-Closing |
| --------------- | ---------------------- | ---------------------------------------- | ------------ |
| Headings        | h1, h2, h3, h4, h5, h6 | Six levels of section headings           | False        |
| Paragraphs      | p                      | Section of text, like in print           | False        |
| Line Break      | br                     | Separates content with a carriage-return | True         |
| Horizontal Rule | hr                     | A line to separate content               | True         |
| Lists           | ul, ol, li             | Ordered and unordered lists              | False        |
| Text emphasis   | em                     | Emphasizes text                          | False        |
| Text importance | strong                 | Singles out important text               | False        |
| Bold            | b                      | Changes text to bold                     | False        |
| Italic          | i                      | Changes text to italic                   | False        |
| Blockquote      | blockquote             | A quote, with optional citation          | False        |

## Headings - \<h1>, \<h2>, \<h3>, \<h4>, \<h5>, \<h6>

The use of headings and sub-headings to organize the content of the document is likely familiar to you from their use in Word and Google documents. These HTML heading elements serve the same purpose on a web page.

There are six different elements, ranging from `<h1>` representing the most important, down to `<h6>`, representing the least important. In practice, the headings `<h1>`, `<h2`>, and `<h3>` are heavily used, but it is often difficult to consistently follow a hierarchical pattern of importance throughout a site for these smaller heading.

{% hint style="info" %}
There should only be a single `h1` element on a page.
{% endhint %}

### Defaults for h1 - h6

```markup
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
    <h3>Heading 3</h3>
    <h4>Heading 4</h4>
    <h5>Heading 5</h5>
    <h6>Heading 6</h6>
```

![](<../../../.gitbook/assets/image (149).png>)

### A Typical Use of h1 - h3

![](<../../../.gitbook/assets/image (40).png>)

## Paragraphs - \<p>

The paragraph element is meant to display some descriptive text or a paragraph. Consecutive paragraphs will have space between them, just like in a book.

## Lists - \<ul>, \<ol>, \<li>

Lists will be familiar to you, as you've probably created them in Word or Google Docs. There are two options: ordered and unordered. Each type of list requires the use of the container element to specific what type of list, and the inner elements for each list item.

The `ul` element is for an unordered list. The `ol` element is used for an ordered list.

```markup
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>
```

## Emphasizing Text - \<strong>, \<em>, \<b>, \<i>

The use of these elements is often confusing, as it appears that their usage overlaps. This is a topic that is worth reviewing at a later point on the [MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong#usage_notes).

| **Element** | **Usage**                                                                                                                                                        |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| strong      | indicates that its contents have strong importance, seriousness, or urgency. Browsers typically render the contents in bold type                                 |
| em          | marks text that has stress emphasis                                                                                                                              |
| b           | is used to draw the reader's attention to the element's contents, which are not otherwise granted special importance                                             |
| i           | represents a range of text that is set off from the normal text for some reason, such as idiomatic text, technical terms, taxonomical designations, among others |

{% hint style="info" %}
The `<strong>` element is for content that is of greater importance, while the `<b>` element is used to draw attention to text without indicating that it's more important.

While `<em>` is used to change the meaning of a sentence as spoken emphasis does ("I _love_ carrots" vs. "I love _carrots_"), `<strong>` is used to give portions of a sentence added importance (e.g., "**Warning!** This is **very dangerous.**")
{% endhint %}
