# Day 2; Advanced CSS & design fundamentals

This session will cover:

- Advanced CSS
    - Pseudo Selectors
    - Media Queries
    - Display type
    - CSS Frameworks
- Design Systems
    - Component Model
- Making CSS Easier
    - CSS Frameworks


## Resources

Here are a list of the additional resources from the [slides](https://docs.google.com/presentation/d/1Oieq85RO95CwR1lQUK_f1akb_AifEJgLI7VatIOztf4/edit?usp=sharing)

### Table of contents

- [Positions](#positions)
- [Z-index](#z-index)
- [Grid](#grid)


### Positions

The browser’s default positioning lays out all inline elements(e.g a, img, span) from left to right, and all block elements(e.g headers, div, p) from top to bottom.

Position allows us to specify the way the browser positions an element. By default, all element positions are set to static.

[Good video about this](https://www.youtube.com/watch?v=86nTToBm2uQ)

### Z-index

The web is all boxes, and unfortunately they’re 3D. If something is overlapping use z-index to fix it


Also it’s recommended to add this to your CSS ([box-sizing reference](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)):
	
```css
*{
    box-sizing: border-box;
    margin:0;
}
```

This will solve a number of styling problems you run into


### Grid

Does what it says on the tin, let’s you create grids!

You can checkout a breakdown of CSS grids [here](https://css-tricks.com/snippets/css/complete-guide-grid/)







