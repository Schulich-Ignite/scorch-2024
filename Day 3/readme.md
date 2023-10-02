# Day 3; Bootstrap and javascript

Now that we've learned more about CSS and design we can move on to a very common CSS framework, bootstrap. We will cover the fundamentals of bootstrap including when to use different components, and how they work. We will then look at the basics of javascript including Syntax, and the Window, Document and Element objects

## Resources

Here are a list of the additional resources from the [slides](https://docs.google.com/presentation/d/1yJsuSJqDy4bKW2JAeeewxk3_-V74yy6GbY9unA9NDgQ/edit?usp=sharing)

### Table of contents
- [We made a post talking about other options](#we-made-a-post-talking-about-other-options)
- [Other reasons to use CSS frameworks](#other-reasons-to-use-css-frameworks)
    - [Not everyone uses the web the same](#not-everyone-uses-the-web-the-same)
- [Other navigations](#other-navigations)
- [Resource about CSS grid](#resource-about-css-grid)
- [Alternatives to bootstrap icons](#alternatives-to-bootstrap-icons)
- [What if we have A LOT of data?](#what-if-we-have-a-lot-of-data)
- [How can we let users know where to find us?](#how-can-we-let-users-know-where-to-find-us)
- [Where bootstrap responsiveness comes from](#where-bootstrap-responsiveness-comes-from)
- [Where to look for details about flexbox](#where-to-look-for-details-about-flexbox)
- [Warning - Javascript types are a myth, anything is anything](#warning---javascript-types-are-a-myth-anything-is-anything)
- [Window object usage - database](#window-object-usage---database)
- [Creating Element Object(s)](#creating-element-objects)
- [Fullscreen](#fullscreen)


### We made a post talking about other options

Variety is the spice of life, [so we made a post talking about other options](https://schulichignite.com/blog/how-to-cheat-at-css/) as well as various other ways to approach not having to write all your CSS by hand

### Other reasons to use CSS frameworks

-   Lots of pre-built code by community
-   Easier to get people to answer questions since CSS is standardized
-   Solves problems you’ve never heard of/thought about
    - Accessibility
    - RTL
    - mobile responsive

#### Not everyone uses the web the same

-   [RTL](https://en.wikipedia.org/wiki/Right-to-left_script)
-   [Screen readers](https://en.wikipedia.org/wiki/Screen_reader)

### Other navigations

There are also other forms of navigations like [tabs](https://getbootstrap.com/docs/5.2/components/navs-tabs/#tabs)

### Resource about CSS grid

There is a feature built into CSS that is similar also called grid

Learn more about the CSS Grid [here](https://www.w3schools.com/css/css_grid.asp)

[CSS Grid Garden](https://cssgridgarden.com/) is an interactive game that will teach you how to use the CSS Grid and help you to practice using it

### Alternatives to bootstrap icons

There are many great icon libraries to use in your site designs, a few are:

-   [The Noun Project](https://thenounproject.com/) (requires attribution if not a premium subscriber to their library) - ~5 million icons
-   [Pixel Art Icons](https://pixelarticons.com/) - ~480 free pixel icons
-   [Icon Monstr](https://iconmonstr.com/) -~4,500+ free icons (updated frequently)

Also note, that when using some icons outside of the bootstrap library, you’ll need to download the file and add it to the page using an img element

### What if we have A LOT of data?

[Accordion](https://getbootstrap.com/docs/5.2/components/accordion/) (sometimes called collapse) let you put a ton of data into one spot. A good example is FAQs (if you look they work similar to the navbar toggler)

### How can we let users know where to find us?

A lot of the time you will have other places you want your users to find you. It’s a good idea to chuck a footer at the bottom of the page 

### Where bootstrap responsiveness comes from

Remember media queries, columns are a combination of using media queries and a technology called [flexbox](https://www.w3schools.com/css/css3_flexbox.asp) (similar to inline-block)

[Example from here](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)


### Where to look for details about flexbox

If you are interested you can checkout flexbox. It can do a lot of what we looked at earlier (and more!).

It’s hard to wrap your head around when you start, but [this video](https://www.youtube.com/watch?v=u044iM9xsWU) is very helpful!

### Warning - Javascript types are a myth, anything is anything

**Javascript will let you change the type of any object without asking for it**

This means unlike python that throws errors when you try to do something unsupported, javascript will just avoid errors at all costs!

```js
('b'+'a'++'a'+'a').toLowerCase() // "banana"
```

### Window object usage - database

We will not be covering this in detail, but if you ever need to store some data in the browser there are 2 good options that use the [storage api](https://www.w3schools.com/html/html5_webstorage.asp)

-   [window.localStorage](https://www.w3schools.com/html/html5_webstorage.asp#:~:text=The%20localStorage%20Object,%22lastname%22)%3B); Stores data persistently
-   [window.sessionStorage](https://www.w3schools.com/html/html5_webstorage.asp#:~:text=The%20sessionStorage%20Object,the%20current%20session%3A); Stores data for one browser session (until closed)
    

You can see the data stored in your browser by going to the “application” tab in the developer tools (see image)

There is also [indexDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) which is more complicated but handles LOTS of data better

### Creating Element Object(s)


This is more complicated. Best practice is to follow [this guide](https://www.w3schools.com/js/js_htmldom_nodes.asp), however there is a simpler way to do this for common use cases:

```html
<div id="content"></div>
<script>
    content = document.getElementById("content"); // Get element with ID content
    text = document.createE1ement("h1");          // Create H1 element
    text.innerHTML="Hello world";                 // Add Hello World making it <h1>Hello World</h1>
    content.appendChild(text);                    // Add the new element to the div
</script>
```

Note that you can set the styles, attributes etc of the element the same way we have in previous slides

### Fullscreen

The last thing that may come up depending on your projects is how to make something fullscreen. Since this is more niche we are not going to demo this, instead [here is the reference info](https://www.w3schools.com/jsref/api_fullscreen.asp), and [here is an example we included](https://github.com/Schulich-Ignite/scorch-winter-2023/blob/main/Day%202/examples/fullscreen.html) of how to do this.
