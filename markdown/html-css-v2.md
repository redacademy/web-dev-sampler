name: inverse
layout: true
class: center, middle, inverse

---

# Dive Into HTML & CSS

.title-logo[![Red logo](img/red-logo-white.svg)]

---
layout: false

# Housekeeping

- Slides: http://redacademy.github.io/web-dev-sampler/
- Wifi: **WeWork** / Password: **P@ssw0rd**

---

# Agenda (First half)

- What is HTML?
- Elements & Attributes
- Creating a Webpage
- Differences in Doctypes
- Structural Elements

---

# Agenda (Second half)

- What is CSS?
- Adding CSS to your website
- Writing CSS rules

---
template: inverse

# What is the Web?

---

# The Web, Defined

- The web is a collection of web pages and their related resources (images, etc.) that we can access using HTTP
- **Web servers** wait and listen for HTTP requests, then send us a response back saying whether it can serve that request we made
- You can actually see these requests in the developer tools in your browser

---
class: center, middle

![HTTP request diagram](img/slide-assets/http-request-diagram.svg)

--

Let's take a look...

---
template: inverse

# What is HTML?

---
class: center, middle

### What does "HTML" mean?

HTML stands for **HyperText Markup Language**.

It helps us describe the structure of webpage, and its connections with other webpages.

---

# HTML Defined

**HyperText** is a system of clickable text links that let you view information in a non‐linear way.

Hypertext also relates to **hyperlinks**, which also applies to media and non‐text links, such as images or buttons.

---
class: center, middle

.inline-images[
   ![Traditional documents](img/slide-assets/html-traditional-doc.svg)
]

---
class: center, middle

.inline-images[
   ![HyperText documents](img/slide-assets/html-hypertext-doc.svg)
]

---

# HTML Defined

A **markup language** provides a set of rules for how we use characters and symbols (knowns as **elements** in HTML) to annotate text to provide information about its structure or presentation.

HTML simply tells our browser how to structure the text and media on a webpage.

---

# But Why Do We Need It?

- We need to mark-up our document for it to be properly formatted
- When you add formatting in Word, etc. you're marking that document up too
- If you view the source code of a non-marked up document, the browser will replace all of the whitespace with just a single space

---
template: inverse

# Elements & Attributes

---

# Using HTML Elements

HTML elements are surrounded with angle brackets so the browser know how to distinguish them from the text that we actually see on a webpage.

Based on what the browser sees in the angle brackets, it knows how to render the structural format of the page.

*Let's dive in and see how it works...*

---

# A Basic Element

If we wanted to markup a paragraph in HTML, our code would look like this:

```html
<p>The quick brown fox jumps over the lazy dog.</p>
```

Notice that the text is wrapped in `<p>` tags, and the closing tag contains a `/` (e.g. `</p>`) after the opening angle bracket.

*Element tags almost always come in pairs.*

For a full list of elements, check out the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

---

# A Basic Element

And if we want to add a second paragraph, we'll enclose its text inside of its own set of `p` tags:

```html
<p>The quick brown fox jumps over the lazy dog.</p>
<p>Grumpy wizards make toxic brew for the evil Queen and Jack.</p>
```

---

# Adding Attributes

An attribute is a bit of information we add inside the element's opening tag.

The are made up of two parts, a **name** and a **value** that are separated by an equal sign:

```html
<p lang="fr">Bonjour mes amis!</p>
```

Some attributes can be used globally on any HTML element, but many are element-specific.

---

# Nesting Elements

We can also **nest** our tags in HTML. For example, to add emphasis to our paragraph text we can use the `<em>` tags.

```html
<p>
   <em>The quick brown fox jumps over the lazy dog.</em>
</p>
```

Think of nested tags like Russian *Matryoshka* dolls.

---
template: inverse

# Creating a Webpage

---
class: center, middle

### What makes a webpage?

To create a basic webpage, we need three things: a **code editor**, a **file** with a `.html` extension, a handful of **HTML elements** inside it that are common to all webpages.

---

# Code Editors

Any program that edit plain text files can be used as a code editor (e.g. Notepad on Windows).

But programs that are specially designed for editing code offer extra features like **syntax highlighting**.

Some good (free) code editor options include:

- **[Sublime Text](http://www.sublimetext.com/)** or **[Atom](https://atom.io/)** (Mac or Windows)
- **[Text Wrangler](http://www.barebones.com/products/textwrangler/)** (Mac)
- **[Notepad++](https://notepad-plus-plus.org/)** (Windows)

---

# Building Blocks

Virtually all websites share the same basic structure. They contain a `<head>` and a `<body>`, and those two elements are wrapped in `<html>` tags:

```html
<html>
   <head>
      <title>This is the Page Title</title>
   </head>
   <body>
      <p>This is a paragraph.</p>
   </body>
</html>
```

---

# Exercise 1

Let's see what happens when we create our first piece of HTML code.

Traditionally, you'd use a text editor, but we'll be using codepen.

https://codepen.io/pen

Try making a `<p>` element now.

---

# Codepen

- A sandbox/playground for coding HTML
- Takes care of some boilerplate for us
- Takes care of creating & linking files

---
template: inverse

# Structural Elements

---

# Headings

We've already seen the `<p>` element in action, now let's take a look at headings.

In HTML, you can denote 6 different levels of headings with markup like so:

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

---

# Lists

In HTML we can create both **ordered** and **unordered** lists:

```html
<ol>
   <li>Mix ingredients</li>
   <li>Put cake in oven</li>
</ol>
```

```html
<ul>
   <li>Apples</li>
   <li>Oranges</li>
</ul>
```

---
template: inverse

# A Few More Elements...

---

# Strong & Emphasis

The `<strong>` tag indicates that the text contained within is of strong importance:

```html
<p><strong>Warning!</strong> This is extremely dangerous.</p>
```

A browser will display this text as bold by default.

The `<em>` tag indicates a subtle shift in meaning of the text:

```html
<p>The most important thing is <em>that you do not quit!</em></p>
```

A browser will display this text as italicized by default.

---

# Link Elements

Links are the lifeblood of the web. This is how we make them:

**Example 1:**

```html
<a href="http://www.redacademy.com">Visit the RED Academy website!</a>
```

**Example 2:**

```html
<p>The <a href="https://developer.mozilla.org/en-US/">Mozilla Developer Network</a> is a great resource!</p>
```

**Note** that any text contained within the `<a>` tags will be linked to the page inside the quotes of the `href` attribute.

---

# Link Elements

Links can also be **relative** to the root folder of your website:

```html
<a href="about.html">About Us</a>
```

And if a page is in a sub-folder:

```html
<a href="sub_pages/about.html">About Us</a>
```

---

# Exercise 2


https://codepen.io/redcjrc/pen/XPjGNJ

Let's mark this content up with **paragraph tags**, and **heading tags** for the book title and chapter title.

Next, link the "Project Gutenberg" text (at the bottom) to its source by adding an **anchor tag**:

`https://www.gutenberg.org/files/11/11-h/11-h.htm`

*Also experiment by adding bold or italic text wherever you like!*

---
template: inverse

# BREAK TIME

---
template: inverse

# What Is CSS?

---
class: center, middle

### What does "CSS" mean?

CSS stands for **Cascading Style Sheets**.

CSS describes how an HTML element will be rendered on a screen. In other words, it allows us to add **styles** to our HTML.

---
class: center, middle

.large[
   **HTML** &rarr; the content layer

   **CSS** &rarr; the presentation layer
]

---

# CSS to the Rescue

CSS allows us to abstract presentation details away from the content and structure of our HTML.

That makes it much easier to globally add and change styles for our websites.

*So let's take a look at how it works...*

---

template: inverse

# Adding CSS to Your Website

---
class: center, middle

### Including CSS

There are a few different ways we can add CSS to a website. Today we will focus on **external stylesheets**.

---

# External CSS

With external CSS, you put all of your CSS in a separate `.css` file, and link to it inside the `<head>` of your document:

```html
<!DOCTYPE html>
<html>
   <head>
      <title>My Page</title>
      <link rel="stylesheet" href="style.css">
   <head>
   <body>
      <p>Hello, world!</p>
   </body>
</html>
```

---
class: center, middle

.inline-images[
   ![Linking to an external stylesheet](img/slide-assets/css-folder-structure.png)
]

---

# External Advantages

- It's easy to link the same stylesheet to multiple pages across your website
- It's much easier to make global changes to your CSS that are immediately picked up throughout the website
- Your website's content is clearly separated from your website's style

---
template: inverse

# Using CSS

---
class: center, middle

.large[
   What does CSS look like?
]

---
class: center, middle

.inline-images[
   ![CSS rule](img/slide-assets/css-declaration-diagram.svg)
]

---

# Writing CSS Rules

But you can do a lot more than just change the background color behind some paragraph text:

```css
p {
   color: red;
   font-family: Helvetica, Arial, sans-serif;
   font-style: italic;
   line-height: 1.25;
   margin-bottom: 15px;
}
```

We can also use CSS to **font size**, **background color**, the **position** of elements in the browser window, and much more.

---

# Writing CSS Rules

We can also be more specific about targeting those styles to only affect `<p>` tags that are inside a particular element:

```css
article p {
   color: red;
   font-family: Helvetica, Arial, sans-serif;
   font-style: italic;
   line-height: 1.25;
   margin-bottom: 15px;
}
```

This rules is said to be more **specific** than the last rule.

---

# Boxes Everywhere

When writing CSS, it's helpful to think of every HTML element in your document being wrapped in an invisible box.

.inline-images[
   ![CSS Box Concept](img/slide-assets/css-box-concept.svg)
]

---
class: center, middle

.large[
   This is called the **box model**.<br />It's an important CSS concept.
]

---

# The Box Model

The box model gives additional properties that we can adjust for each HTML too. These properties include:

- `margin`
- `border`
- `padding`
- `width`
- `height`

---
class: center, middle

.inline-images[
   ![CSS Box Model](img/slide-assets/css-box-model.svg)
]

---

# Box Model Properties

Using the box model to style our HTML elements, we can use CSS properties such as:

```css
p {
   border-top: 1px solid black;
   border-bottom: 3px dotted blue;
   padding-left: 30px;
   margin: 15px;
   width: 300px;
}
```

You can target specific sides of a box by adding **`-bottom`, `-top`, `-left`,** or **`-right`** to the properties. Otherwise, the style will apply to all sides.

---

# Box Model Shorthand

Or instead of writing out all the properties for each side, we can use shorthand:

```css
header {
   margin: 0 auto; /* this is horizontal centering trick in CSS */
   padding: 5px 0 5px 10px;
}
```

If you include **two properties**, they are applied to the **top/bottom** and then **left/right**.

If you include **four properties**, they will be applied in the order **top**, **right**, **bottom**, and **left** (clock-wise).

---

# Box Model Shorthand

Look for patterns in your CSS property values, for example:

```css
header {
   margin: 10px 0 10px 0;
}
```

Can be re-written as:

```css
header {
   margin: 10px 0;
}
```

*Your goal as a web dev is to do as little typing as possible!*

---

# Exercise 4

First, in our **html**: let's organize our webpage content in an `<article>` element.

In our **css** file, set the `width` of the `article` to **800px**. Now *center* this same `article` element using the margin trick: `margin: 0 auto;`

On the `body` element, set the font to `Arial, sans-serif`.

For all paragraph elements, add a bottom margin: `margin-bottom` with a **24px** value. Also adjust the `line-height` property and set its value to **1.25** for your paragraphs.

---

# What We've Learned

- How to create a webpage
- What HTML is and it's basic elements
- How to include CSS in our webpage
- What the box model is

---
template: inverse

# Questions?

---
class: center, middle

   <h3>RED's courses will start:</h3>
   Full-time: October 1st<br />
   Part-time: October 8th<br />
   For scholarship information email `felicity@redacademy.com`
