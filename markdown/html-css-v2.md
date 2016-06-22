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
- Wifi: **RA_Student** / Password: **RA_Learning**

---

# Agenda (6&ndash;7:00 p.m.)

- What is HTML?
- Elements & Attributes
- Creating a Webpage
- Differences in Doctypes
- Structural Elements

---

# Agenda (7&ndash;8:00 p.m.)

- What is CSS?
- Adding CSS to your website
- Writing CSS rules
- Classes and IDs

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

class: center, middle

.inline-images[
   ![HTML element structure](img/slide-assets/html-tag-structure.svg)
]

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

background-image: url(img/slide-assets/russian-nesting-dolls.jpg)

.footnote.white[
   Image Credit: [Bradley Davis](https://www.flickr.com/photos/backpackphotography/2318055128/)
]

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

Let's see what happens when we create an HTML file and add this code from the previous slide to it.

If you haven't already, you'll need to download a code editor such as Atom to do this.

Save your new webpage as `index.html` and open it in a web browser to see what it looks like.

---
class: center, middle

### Why call it index.html?

When you name a file `index.html` (most) web servers will automatically know that this is the homepage.

---

# One Folder = One Site

Before long, you're going to want to add additional pages to your site, or other files (like images).

To keep all of those HTML files and your other webpage assets organized, you'll want to set up a folder somewhere on your computer.

We call this the **root folder** of your project. You can name it anything you'd like and it can contain any number of sub‐folders to further organize your files.

---
class: center, middle

.inline-images[
   ![Root folders](img/slide-assets/html-folder-structure.png)
]

---

#  New Site = New Folder

You'll also want to create a new `root folder` for each *different* website that you build:

.inline-images[
   ![Root folders](img/slide-assets/html-multiple-sites.svg)
]

---

# File/Folder Naming Tips

Use these sanity-saving tips to name your folders and files:

- Stick to lowercase consistently
- Don't use space in your file names, instead use hyphens or underscores to separate words
- Don't use special characters in your file names
- Choose logical and descriptive names for files and folders

---
template: inverse

# Doctypes

---

# A Little Bit of History

Doctypes have a long and complicated history on the web.

The important thing to know is that the doctype declaration is not an HTML tag, but rather tells the browser which version of HTML the webpage uses.

---

# Then & Now...

**XHTML:**

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
```

**HTML5:**

```html
<!DOCTYPE html>
```

---

# Where Does It Go?

Doctype declarations go at the top of your `.html` files:

```html
<!DOCTYPE html>
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

**[Download this text file](resources/aiw-text.txt)** and paste its content into your `index.html` file inside your code editor.

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

# Before CSS...

In the old days, we used to add styles to our websites like this:

```html
<p>
   <font face="Arial" color="red" size="2">Some text...</font>
</p>
```

Now imagine a large website with dozens of pages...can you see a major flaw in styling a website this way?

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

# Exercise 3

Let's **add a CSS file to your website now**.

To do that, create a `style.css` file in the root folder of your website.

Next, just like in the previous example, add a `<link>` tag to the `<head>` of your HTML file so it knows to apply the styles that we add to this file later on to your page.

**Be mindful of relative paths of the style.css, in relation to your index.html file**

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

First, in our **index.html** file: let's organize our webpage content in an `<article>` element.

In our **style.css** file, set the `width` of the `article` to **800px**. Now *center* this same `article` element using the margin trick: `margin: 0 auto;`

On the `body` element, set the font to `Arial, sans-serif`.

For all paragraph elements, add a bottom margin: `margin-bottom` with a **24px** value. Also adjust the `line-height` property and set its value to **1.25** for your paragraphs.

---
template: inverse

# Class & IDs

---

# What are they?

Every HTML element can have `class` and `id` attributes added to it like this:

```html
<h1 class="site-title" id="masthead">My Awesome Website</h1>
```

Classes and IDs make it much easier to target specific CSS (and JavaScript) to elements in our HTML.

---

# What's the difference?

Think about an actual school...a student can be in multiple classes, but each student will have a unique name.

Similarly, if an HTML element has an ID, that ID must be unique to the element. But a class can be applied to as many elements as you like.

---

# Classes in CSS

To target an element's class in your CSS, you would use a dot plus the class name:

```html
<h1 class="site-title" id="masthead">My Awesome Website</h1>
```

```css
.site-title {
   font-weight: bold;
}
```

---

# IDs in CSS

To target an element's ID in your CSS, you would use a pound sign plus the ID name:

```html
<h1 class="site-title" id="masthead">My Awesome Website</h1>
```

```css
.site-title {
   font-weight: bold;
}

#masthead {
   color: red;
}
```

---

# Multiple Classes

You can specify multiple classes for an element by separating them with a space:

```html
<h1 class="site-title home-title" id="masthead">My Awesome Website</h1>
```

And if you wanted to target an element that had both of those classes, your CSS would look like this:

```css
.site-title.home-title {
   font-size: 32px;
}
```

---
class: center, middle

.large[
   Which do you pick?
]

---

# Classes vs. IDs

In general, you'll want to **stick to classes** wherever possible.

IDs are considered to be **more specific** than classes in your CSS, which makes the ID-based styles you apply to your website harder to override later on.

Classes are also reusable, which can help make your CSS more efficient.

---

# Exercise 5

In our **index.html** file, add a class of `title` to the `<h1>` element and update your CSS to target your custom heading colour at the new class instead of all `h1` elements.

**Hint:** `<h1 class="...">`

Add a class of `author` to the paragraph containing the author name. Now make only that line italic using CSS.

Lastly, add an ID of `source` to the excerpt's link tag

In our **style.css** file, add a CSS rule for this `#source` id we just created and adjust its `color` property to `red`.

---

# What We've Learned

- How to create a webpage
- What HTML is and it's basic elements
- How to include CSS in our webpage
- What the box model is
- How to use classes and IDs to target our styles

---
template: inverse

# Questions?

---
class: center, middle

.large[
   RED Academy's<br />summer cohort starts <br />in July!
]
