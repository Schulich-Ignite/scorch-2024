# Day 4; Advanced JS, Vendoring (Using other people’s code)

Writing javascript is great and all, but it's exhausting to do everything ourselves. This session will cover vendoring, and how to use existing javascript libraries to add functionality to our webpages!

## Resources

Here are a list of the additional resources from the [slides](https://docs.google.com/presentation/d/11wsO5GInwXgOYPZpMVZZcEoyw6hejeBGTJDzuDC6uys/edit?usp=share_link)

### Table of contents
- [NPM](#npm)
- [The dangers of CDN’s](#the-dangers-of-cdns)
- [Editor types](#editor-types)
    - [Single Pane/Classic WYSIWYG](#single-paneclassic-wysiwyg)
    - [Forms](#forms)
    - [Document based](#document-based)
- [Problems with HTML generation continued](#problems-with-html-generation-continued)
- [Visualization](#visualization)
- [Games](#games)


### NPM

NPM is the Node Package Manager, this is a system that lets you run NodeJS packages. We don’t have time to cover NodeJS in this course, but it’s worth learning if you want to go forward in web development. Basically nodeJS makes writing large javascript projects easier, so a lot of people use it!

It allows you not only to write normal javascript, but actually extend javascript by running your own NodeJS server that gives you extra functionality javascript doesn’t have!

We have a series talking about npm on the ignite blog [here](https://schulichignite.com/blog/intro-to-node/npm-intro/)

If you want to learn about NodeJS and NPM we have left you some resources here:

-   [Full NodeJS tutorial](https://www.youtube.com/watch?v=fBNz5xF-Kx4)
-   [NPM explained](https://www.youtube.com/watch?v=P3aKRdUyr0s)

### The dangers of CDN’s

There are a few security considerations with CDN’s. [Here is a post we made talking about them, and how to avoid some of the problems!](https://schulichignite.com/blog/dangers-of-cdns/)

### Editor types

Single pane: [quill](https://quilljs.com/), [tiny MCE](https://www.tiny.cloud/) etc. Good for “small burst” content (twitter, reddit, comment section)

Block Based: [Guttenberg](https://wordpress.org/gutenberg/), [editor J](https://editorjs.io/)S etc., Good for “long content” (medium articles, blog posts)

Form Based: [Formspree](https://formspree.io/), [Wix getting started](https://www.wix.com/) etc. Good for “highly structured content” (Contact forms, sign-in/check-in, profile pages etc.)

Document based: [Microsoft office suite](https://www.office.com/), [google suite](https://drive.google.com/). Good for documents, include WYSIWYG’s with page metadata/state

#### Single Pane/Classic WYSIWYG

Everything is typed in one box, with controls either at the top, or inline ([reddit](https://reddit.com/), [slack](https://slack.com/), [medium](https://medium.com/), etc.)

#### Forms

Not necessarily a WYSIWYG, but forms will often be used for content that has rules, or multiple inputs (i.e valid phone number, certain length etc.). These are often combined with WYSIWYG’s

#### Document based

Will often have a classic WYSIWYG, but then will also have a form/forms to configure settings about the document

### Problems with HTML generation continued

Regardless of what you’re doing always sanitize any input you’re getting, and make sure you can avoid some common security mistakes.

Here are some good resources on how to avoid problems:

-   [How To Prevent The Most Common Cross Site Scripting Attack - YouTube](https://www.youtube.com/watch?v=ns1LX6mEvyM)
-   [Input Sanitization - Peter Faiman - YouTube](https://www.youtube.com/watch?v=fMZNRKSRb8g)
    
And here’s a video on what can happen if you don’t:

-   [Someone finds bug in guy’s twitch chat app](https://www.youtube.com/watch?v=2GtbY1XWGlQ)
    
Much more complicated version of this:

-   [XSS on Google Search - Sanitizing HTML in The Client? - YouTube](https://www.youtube.com/watch?v=lG7U3fuNw3A)

### Visualization

Sometimes you just wanna make something that looks cool, these libraries let you make things that are visually complicated (3d objects, graphs, charts etc.)

-   [P5js](https://p5js.org/); javascript version of processing
    
-   [Chartjs](https://www.chartjs.org/); Super simple to use chart generator
    
-   [D3js](https://d3js.org/); Has a huge variety of charts, bit more complicated
    
-   [Threejs](https://threejs.org/); Incredibly powerful 3D library
    
-   [WebGL](https://get.webgl.org/); The web version of [openGL](https://www.opengl.org/) (3D library)
    
-   [Plotly](https://plotly.com/); Multi-language graph library
    
-   [Mermaid](https://mermaid-js.github.io/mermaid); A tool that has its own language, [editor](https://mermaid.live/edit) and format for creating charts that some people really like

### Games


Games are fun, and you can make them run entirely in the browser. There are a few familiar faces from the last slides, but regular 3d libraries are a bit more complicated than dedicated game engines

-   [Unity](https://docs.unity3d.com/Manual/webgl-building.html); Like unity, but in the web!
    
-   [P5js](https://p5js.org/); javascript version of processing
    
-   [Threejs](https://threejs.org/); Incredibly powerful 3D library
    
-   [WebGL](https://get.webgl.org/); The web version of [openGL](https://www.opengl.org/) (3D library)
    
-   [Babylon](https://www.babylonjs.com/); 3d game engine with [node materials](https://nme.babylonjs.com/) & [editor](https://playground.babylonjs.com/) ([demo](https://spacepirates.babylonjs.com/))
    
-   [PixiJS](https://github.com/pixijs/pixijs); 2D Game engine that is very fast
    
-   [Melon JS](https://github.com/melonjs/melonJS); 2D game engine with [map editor](https://www.mapeditor.org/) compatibility
