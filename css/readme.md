# CSS

Once you have layed out the foundation for your website, you then have to style it. That's where CSS comes in! CSS stands for "Cascading Style Sheets" and are used to set the look and layout of a webpage. CSS tells HTML elements where to go and what to look like.

> **Q. Why "cascading"?**

> A. CSS is considered cascading because the computer reads it from top to bottom. That just means that order matters when styling your webpages.

## Syntax

Let's say that I want to style all of the paragraph tags, `<p>`, on my webpage. To do that in CSS, I simply refer to the HTML tag name like so:
```css
p {
  /* Insert styles here! */
}
```
All of my styles will go in between the braces, `{}`. You can also an example of a CSS comment, which is any text between the forward slash and asterisk, `/* */`;

Every CSS style consists of a key and value pair. These are separate from each other by a colon, `:`, and from additional styles by a semicolon, `;`. If I want my paragraphs to be pink and 24px, I can use the following CSS:
```css
p {
  color: pink;
  font-size: 24px;
}
```
You'll notice above that CSS style keys can be one word or more. If they consist of more than one word, they words are linked together by hyphens, `-`.

Our paragraphs above have two styles, but you can add an unlimited number of styles to an element; go wild!

## Using CSS

There are three main methods for adding styles to your HTML: 1) inline styles, 2) style tag, and 3) external styles. The most common method is external, but let's take a brief look at the first two.

### Inline styles

HTML elements can be passed a style property to add CSS. Consider the paragraph example from above. You can add your CSS styles directly to the paragraph element like so:
```html
<p style="color: pink; font-size: 24px">A paragraph of text that goes on for a while...</p>
```
Notice that we have replaced the braces around our styles with double quotation marks, `" "`. This will add the same styles as the example above.

#### Potential issues
Inline styles are useful in specific instances but are not an efficient way to style an entire webpage. Think of the example above; if we want all of our paragraphs to have the same styles, then we're going to need to copy and paste the style information every time we want to create a new paragraph. Not only does that take a lot of time, but it makes maintaining your code more difficult.

### Style tag

There is an HTML style tag, `<style> ... </style>`, that can be used to store your styles. This is usually located within the head tag of your document, but it can be in the body as well. Look at this example:

```html
<!DOCTYPE html>
<html>
  <head>
    <style type="text/css">
      p {
        color: pink;
        font-size: 24px;
      }
    </style>
  </head>
  <body>
    <p>A paragraph of text that goes on for a while...</p>
  </body>
</html>
```
By including our style information in the `<head>` of our webpage, we can ensure that the styles apply to everything in the `<body>`.

#### Potential issues
In many projects, there are more lines of CSS than any other language. Adding all these styles at in the head of a webpage will make it difficult to maintain your code.
