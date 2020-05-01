### Thursday, April 30th  

**Design Web Pages with CSS**

Introducing CSS to your HTML webpage allows for quite a bit more flexibility when it comes to design.

That's because CSS - or *Cascading Style Sheets* - is a style focused rather than content focused language.  Essentially, CSS asks you to place all of your content within boxes (remember all those tags we used while building with html?) and then provides the tools to reference those boxes in such a way that we can control everything from the color and font of the text to where images are shown and how visitors to our page experience interactive elements like buttons.

The layout of css is unique from html in that it primarly works with selectors and declarations.

* The **Selector** declares what portion of the code we will be affecting
* The **Declaration** effects a change to that selector by declaring a property and a value for that property.

So, for example, a line of css code that is meant to change the font of content marked as a paragraph would look like this:

> p {
    font-family: Arial;}

In this example, *p* is the selector and the declaration that follows includes the property *font-family* which is set to the value *Arial*.

In addition to using existing tags as selectors, you can also use class or id as a selector. 

>Class Selector is indicated with a . before the attribute name
>ID Selector is indicated with a # before the attribute name

---

#### So, where does this new information go???

Here's where you have a couple options.  You can in fact use some minor css elements inline within your html.  This might look like using the following code to change the color of the text:

>  `<h3 style="color:blue;">This is a blue heading</h3>` 

When rendered, that code would produce the following: <h3 style="color:blue;">This is a blue heading</h3>

However, too much of this can make your code look cluttered.

For a single page website, you may opt for something called internal css.  This is not inline like the previous example, but is instead code added within the head tags that will instruct the styling of the rest of the page.  This code will be entered within `<style>` tags and should include a type attribute that indicates what you are using css to style.  This would look like:

> `<head>`

>`<style type="text/css"> CSS CODE HERE </style>`

>`</head>`

This allows you to keep all the CSS formatting up in the head of your code - but even that can end up looking rather cluttered.  That's why many prefer to keep a separate style sheet entirely.  Sometimes even more than one!

But if your CSS code is entirely separate - how, you may ask, can the one influence the other?  Well, this is the perfect time to learn how to link files to your code.

Again, like with internal css, you want to work within the head tags of your code.  However, instead of inluding the nitty gritty of the css code there, you'll instead include a link using the following format:

> `<link href="FILENAME.css" type="text/css" rel="stylesheet" />`

That line allows your project to pull formatting from the linked css file so that you can keep your workplace tidy without sacrificing your ability to format your page.

---

#### And Now, a little on COLORS

Color is a great way to make your page pop, and utilitzing thoughtful contrast between you text and background can greatly improve readability for your site visitors.

CSS has several ways of indicating color: color name, rgb value, hex code, and hsl.

>Color Name is exactly what it sounds like - there are over 100 predefined color names that a browser can recognize, such as MediumAquaMarine.

>RGB value actually combines Red, Green and Blue - each in a value between 0 and 255 - to give you a specific shade.  For example, that same MediumAquaMarine can be written as rgb(102,205,170).  A fourth value, a, can be added to indicate opacity.

>Hex values convey information in a similar way to rgb, but subsituting in hex codes.  So returning to MediumAquaMarine we now have #66cdaa

>HSL stands for Hue, Saturation and Lightness.  Hue looks at a color wheel and indicates the hue as an angle between 0 and 360.  Saturation and Lightness are both expressed as a percentage.  Just like rgb, hsl can also take an optional fourth value of a to express opacity.

[Home](https://jchinzi.github.io/learning-journal/)