# Intro
- Types of display objects, dimensions and spacing, and the Box Model

## Testing and Validation
- Testing and validation should be a habit
- Update code, test results in browser, validate HTML, validate CSS, check page on other browsers

## Pesticide
- Chrome plugin that allows you to put boxes around the elements of a page
- Hold control and it gives you a box that tells you which element youre hovering over
- Shows how margins, borders, padding, and box model all interact on the page

## What to Focus On
- Focus on CSS Box Model, which describes the mechanism that browsers use to construct a web page from the seemingly unrelated HTML and CSS code.
- Probably the most crucial concept a web developer needs to understand
- Learn what to expect from the browser when it processes your HTML and CSS and how that changes depending on the visual display model, box-sizing model, and box properties
- Don't skim this lesson: read it several times until you're sure you understand the concepts

## Vocabulary
- Box Model
  - Box Properties
    - Width and height
    - Padding and margins
    - Borders
  - Visual Display models
    - `block`
    - `inline`
    - `inline-block`
  - Box Sizing Model
    - `bontent-box`
    - `border-box`
  - Dimensions
    - Absolute units
    - Relative units
- Container
- Physical pixels
- CSS reference pixels

### Box Properties
- Every box has a width, heigh, padding, border and margins; know the difference
- Padding, borders, and margins have separate properties to set the left, right, top, and bottom of each element.  YOu can use shortcut properties to specify all four sides at once
- How does the visual display model interact with margins, borders, and padding?

### Visual Display Models
- Understand the difference between `inline`, `block`, and `inline-block`
- Containers are almost always `block` elements, while non-containers are almost always `inline`.  When in doubt, check MDN.
- Don't try to memorize which HTML elements are `block` or `inline`
- How and when can you change an element's visual display model?

### Box Sizing Models
- Understand the `content-box` and `border-box` sizing models
- How and when can you change the box-sizing model for an element?

### Dimensions
- Know the differences between `px`, `em`, `rem`, `%`, and `auto`
- Understand why we need to talk about CSS reference pixels and physical pixels.  Don't try to memorize the details but understand the topic well enough you won't be surprised when you encounter the differences in the wild
- Use `auto` margins to center block elements horizontally

## HTML
- Don't try to memorize new HTML elements you meet in this lesson

## CSS
- Become comfortable with `display`, `box-sizing`, `width`, `height`, `padding`, `border`, and `margin` properties.  Memorize this list of properties so you can look up the details when needed.
-