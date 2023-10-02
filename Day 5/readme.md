# Day 5 Markup languages, templating & SSG's

Up until now we've learned how to create basic websites, style them nicely, and add some functionality with javascript. Now we're going to look into some other ways of developing websites to create more complex systems and to help us create sites faster!

## Resources

Here are a list of the additional resources from the [slides](https://docs.google.com/presentation/d/1E0M7G5Ukue1cqFQ3SvwbuNGYzey7WnlY_dEnDqFQRCM/edit?usp=sharing)

### Table of contents#
- [A few extra resources](#a-few-extra-resources)
- [Other code generation examples](#other-code-generation-examples)
- [Jinja in other languages](#jinja-in-other-languages)
- [Other templating languages \& uses](#other-templating-languages--uses)
- [ezcv resources](#ezcv-resources)
    - [Required config](#required-config)
    - [Using filters in themes](#using-filters-in-themes)
    - [Galleries](#galleries)
- [Hugo](#hugo)
    - [Why use it](#why-use-it)
    - [Why we didn't use it](#why-we-didnt-use-it)
    - [Examples](#examples)
- [Astro](#astro)


### A few extra resources

I wanted to leave you with a few other resources where you can start diving into learning more about frontend or backend. Some are youtubers some are websites

Frontend/Backend:

-   [Mark Hinton](https://www.youtube.com/c/codesignDev/videos)
-   [Web Dev Simplified](https://www.youtube.com/c/WebDevSimplified)
-   [Theo](https://www.youtube.com/c/TheoBrowne1017)
-   [Fireship](https://www.youtube.com/c/Fireship)

Frontend specialized:

-   [Kevin Powell](https://www.youtube.com/kepowob/videos)
-   [Chrome web dev GUI Snippets series](https://www.youtube.com/watch?v=no1YV6xgIv8&list=PLNYkxOF6rcIAkCqEvHXCAkbRVhjEMbf_i)
-   [Codepen](https://codepen.io/)

Backend specialized:

-   [Hussein Nasser](https://www.youtube.com/c/HusseinNasser-software-engineering/videos)
-   [Network Chuck](https://www.youtube.com/c/NetworkChuck/videos)

### Other code generation examples


-   Emmet, the snippet system we’ve been using
-   Formatting tools such as [flake-8](https://flake8.pycqa.org/en/latest/), or [prettier](https://prettier.io/)
-   Online website builders such as [squarespace](https://www.squarespace.com/)
-   No-code platforms like [scratch](https://scratch.mit.edu/projects/editor/?tutorial=getStarted) (generates [squeak](https://squeak.org/) code)

### Jinja in other languages

JS:
-   [Jinja-js](https://github.com/sstur/jinja-js) (this one is deprecated, see next slide instead)
    
rust:
-   [tera](https://crates.io/crates/tera)

dart:
-   [Jinja](https://pub.dev/packages/jinja)

Java:
-   [Jinjava](https://github.com/HubSpot/jinjava)

### Other templating languages & uses


php:
-   [twig](https://twig.symfony.com/)

Go:
-   [Template](https://pkg.go.dev/text/template)
    
JS:

-   [Liquid](https://npm.io/package/liquidjs) 
-   [Mustache](https://github.com/janl/mustache.js) ([main site](https://mustache.github.io/))
-   [Nunjucks](https://mozilla.github.io/nunjucks/) ([based on jinja](https://mozilla.github.io/nunjucks/templating.html#:~:text=Nunjucks%20is%20essentially%20a%20port%20of%20jinja2%2C%20so%20you%20can%20read%20their%20docs%20if%20you%20find%20anything%20lacking%20here.%20Read%20about%20the%20differences%20here.))
    
Python:

-   [Chevron](https://github.com/noahmorrison/chevron)

**Other Templating language uses**:

-   [Templating config files](https://www.digitalocean.com/community/tutorials/how-to-create-and-use-templates-in-ansible-playbooks)
-   “No-code” languages ([scratch](https://scratch.mit.edu/), [darklang](https://darklang.com/))
-   Project templates/IDE’s ([cookiecutter](https://cookiecutter.readthedocs.io/en/stable/), [create-react-app](https://www.npmjs.com/package/create-react-app))
-   Transpiler’s ([universal transpiler](http://jarble.github.io/transpiler/))
-   Email systems ([hubspot](https://www.hubspot.com/products/sales/email-tracking?hubs_content=www.hubspot.com%2Fproducts%2Fcrm&hubs_content-cta=Email%20tracking))

### ezcv resources

#### Required config

Many configuration variables are required this is set in the metadata.yml file inside a theme. You will get a message if you are missing one

#### Using filters in themes

On top of existing jinja filters there are a few [ezcv specific filters](https://ezcv.readthedocs.io/en/latest/theme-development/#available-custom-filters), you can also [add your own filters](https://ezcv.readthedocs.io/en/latest/contributor-docs/#filters) if you need to inject python code while processing templates.

#### Galleries

[Galleries](https://ezcv.readthedocs.io/en/latest/usage/#image-gallery) are a special type of section. It consists of only images.


### Hugo

[Hugo](https://gohugo.io/) is another static site generator that gets used often. It is faster than ezcv and has more features, but it uses a custom template language that is really only used in hugo, and you have to setup everything yourself!

#### Why use it

-   It’s ubiquitous (used a lot in industry)
    
	-   Large community
	    
	-   Lots of third party themes
	    
	-   Lots of guides, tutorials and videos
    

-   It’s fast
    
-   It’s been tested with many more users and use cases
    
-   It gives you lower level access to things like files


#### Why we didn't use it

-   It’s more complicated
    
-   The templating language is pretty much only used in hugo
    
-   Setting up go can be more complicated on some OS’s
    
-   It’s designed to assume you’re building from scratch, so the theme implementation is not as baked in
    
-   There are lots of ways to do the same thing
    
-   It’s designed more for blogs/businesses than individuals

#### Examples

**[Schulich ignite](https://github.com/Schulich-Ignite/website)**

### Astro

If you want a system that fully uses Javascript [Astro](https://astro.build/) can also do what hugo does
