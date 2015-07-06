name: inverse
layout: true
class: center, middle, inverse

---

# Dive Into HTML & CSS

.title-logo[![Red logo](/img/red-logo-white.svg)]

---
layout: false

# Housekeeping

- Slides: http://redacademy.github.io/web-dev-sampler/
- Wifi: **RA_Student** / Password: **RA_Learning**

---

# Agenda (6&ndash;7:30 p.m.)

- What is HTML?
- Elements & Attributes
- Creating a Webpage
- Differences in Doctypes
- Structural & Semantic Tags

---

# Agenda (7:30&ndash;9 p.m.)

- What is CSS?
- Adding CSS to your website
- Using CSS
- How CSS cascades
- Classes and IDs

---
template: inverse

# What is the Web?

---
class: center, middle

![HTTP request diagram](/img/slide-assets/http-request-diagram.svg)

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
   ![Traditional documents](/img/slide-assets/html-traditional-doc.svg)
]

---
class: center, middle

.inline-images[
   ![HyperText documents](/img/slide-assets/html-hypertext-doc.svg)
]

---

# HTML Defined

A **markup language** provides a set of rules for how we use characters and symbols (knowns as **tags** or **elements** in HTML) to annotate text to provide information about its structure or presentation.

HTML simply tells our browser how to structure the text and media on a webpage.

---
template: inverse

# Elements & Attributes

---

class: center, middle

.inline-images[
   ![HTML element structure](/img/slide-assets/html-tag-structure.svg)
]

---

# Using HTML Elements

HTML elements are surrounded with angle brackets so the browser know how to distinguish them from the text that we actually see on a webpage.

Based on what the browser sees in the angle brackets, it knows how to render the structural format of the page.

HTML elements are often interchangeably called **tags**.

*Let's dive in and see how it works...*

---

# A Basic Element

If we wanted to markup a paragraph in HTML, our code would look like this:

```html
<p>The quick brown fox jumps over the lazy dog.</p>
```

Notice that the text is wrapped in `<p>` tags, and the closing tag contains a `/` after the opening angle bracket.

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
<p><em>The quick brown fox jumps over the lazy dog.</em></p>
```

Think of nested tags like Russian *Matryoshka* dolls.

---

background-image: url(/img/slide-assets/russian-nesting-dolls.jpg)

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

Any program that edits plain text files can be used as a code editor (e.g. Notepad on Windows or TextEdit on a Mac).

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

*Let's see what happens when we create an HTML file and add this code to it...*

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
   ![Root folders](/img/slide-assets/html-folder-structure.png)
]

---

#  New Site = New Folder

You'll also want to create a new `root folder` for each *different* website that you build:

.inline-images[
   ![Root folders](/img/slide-assets/html-multiple-sites.svg)
]

---

# File/Folder Naming Tips

Use these sanity-saving tips to name your folders and files:

- Stick to lowercase consistently
- Don't use space in your file names, instead use hyphens or underscores to separate words
- Don't use special characters in your file names
- Choose logical and descriptive names for files and folders

---

# Exercise 1

Your turn! Time to create your first webpage.

First things first...you need to **pick a code editor** to download and install it (if you haven't done so already).

Next **create a root folder** somewhere on our computer and save a new file called `index.html`.

Then open that file and create a simple webpage containing `<html>`, `<head>`, `<title>`, and `<body>` tags, then add a few paragraphs of text.

Lastly, save your new website and **check it out in a browser**.

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

#Where Does It Go?

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

# Structural Tags

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
<h6>Heading 5</h6>
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

# Horizontal Rules

A horizontal rule will create a separator on your page:

```html
<p>This paragraph talks about a specific topic.</p>
<hr />
<p>This paragraph shifts to a different topic.</p>
```

Notice something special about this elements? It doesn't contain any text, an is represented by a single, self-closing tag. This is called an **empty element**.

---
template: inverse

# Semantic Tags

---
class: center, middle

### Structural vs. Semantic?

Semantic elements don't affect the structure of a webpage, but they do add extra information about its content.

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
template: inverse

# Last but not least...

---

# Link Elements

Links are the lifeblood of the web, so let's take a look at how we make one:

```html
<p>The <a href="https://developer.mozilla.org/en-US/" target="_blank">
Mozilla Developer Network</a> is a great resource!</p>
```

**Note** that any text contained within the `<a>` tags will be linked to the page inside the quotes of the `href` attribute.

The `target` attribute is typically used to call a new window or tab to open for external links. Internal links don't need the `target` attribute.

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

**[Download this text file](../resources/sample-text.txt)** and paste its content into your `index.html` file inside your code editor.

Let's mark this content up with **paragraph tags** and a **heading tag** for the title.

Next, link the entire "Excerpt from..." line (directly under the title) to its original source by adding a **link tag**:

`http://cristal.inria.fr/~weis/info/commandline.html`

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
      <link rel="stylesheet" type="text/css" href="style.css">
   <head>
   <body>
      <p>Hello, world!</p>
   </body>
</html>
```

---
class: center, middle

.inline-images[
   ![Linking to an external stylesheet](/img/slide-assets/css-folder-structure.png)
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
   ![CSS declaration](/img/slide-assets/css-declaration-diagram.svg)
]

---

# A CSS Declaration

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

We can also use CSS to **font size**, **background colours**, the **position** of elements in the browser window, and much more.

---

# A CSS Declaration

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
   ![CSS Box Concept](/img/slide-assets/css-box-concept.svg)
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
   ![CSS Box Model](/img/slide-assets/css-box-model.svg)
]

---

# Box Model Properties

Using the box model to style our HTML elements, we can use CSS properties such as:

```css
p {
   margin: 15px;
   border-top: 1px solid black;
   border-bottom: 3px dotted blue;
   padding-left: 30px;
   width: 300px;
}
```

You can target specific sides of a box by adding `-bottom`, `-top`, `-left`, or `-right` to the properties. Otherwise, the style will apply to all sides.

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

If you include **four properties**, they will be applied in the order **top**, **right**, **bottom**, and **left** (like going around a clock).

---

# Exercise 4

Let's style up some of the paragraphs using some of the CSS properties we just learned.

First, let's organize our `h1` and `p` tags by wrapping them in an `article` tag. Set the width of the `article` to **800px**, and **center it** on the page using the margin trick.

On the `body` element, set the font to `Arial, sans-serif`.

For all paragraphs, use CSS to add **20px of margin below** them. Adjust their `line-height` to be **1.25**.

Lastly, set the `color` of the `h1` to any colour but black.

---
template: inverse

# How CSS Cascades

---
class: center, middle

### The "C" in "CSS"

The idea of **cascading order** is the key to how CSS works on our HTML elements.

---

# Specificity

There are two main thing to know about specificity in CSS:

1. Where specificity is equal, **the rule that comes last applies**
2. Where specificity isn't equal, **the more specific rule applies**

---

# Inheritance

Inheritance is another important concept in CSS.

This means exactly what it suggests&mdash;**child elements in your HTML will inherit styles from an parent elements** in which they are nested.

This saves from having to specify the same styles for every element used.

---

# Specificity & Inheritance

So for example, this CSS:

```css
header {
   font-family: Helvetica, sans-serif;
}
```

Will style all of the text inside the `<header>` in Helvetica:

```html
<header>
   <h1>My Site Title</h1>
   <p>My excellent tagline</p>
</header>
```

---

# Specificity & Inheritance

But if we wrote a more specific rule for the `<h1>`:

```css
header {
   font-family: Helvetica, sans-serif;
}

header h1 {
   font-family: Georgia, serif;
}
```

The `<h1>` inside the header will be rendered in Georgia, and the style that **descends** from the parent `<header>` will be overwritten.

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

# Multiple Classes/IDs

You can specify multiple classes or IDs for an element by separating them with a space:

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

Let's add classes and IDs to our webpage to target our CSS with more specificity.

Add a class of `title` to the `h1` and update your CSS to target your custom heading colour at the new class instead of all `h1` elements.

Add a class of `description` to the first paragraph tag that contains the excerpt link. Now make that text italic using CSS.

Lastly, add an ID of `source` to the excerpt's link tag and set a custom text colour for that ID.

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
   RED Academy's<br />Web Developer Foundation class starts on July 13!
]
