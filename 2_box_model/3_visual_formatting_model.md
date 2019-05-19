# The Visual Formatting Model
- `display` has more than two dozen values, but most CSS uses the values `block`, `inline` and `inline-block`
- We call this property the visual formatting model

## Block elements
- Block-level elements occupies the entire space of its parent element (container)
  - A block-level element always starts ona new line and takes up the full width available (stretches out to the lft and rigth as far as it can)
- Browsers typically display the block-level element with a newline both before and after the element.
  - You can visualize them as a stack of boxes
- Most `block` elements group one or more elements - some of which may themselves be `block` elements into areas of the page
  - Example, the `<header>` element groups together elements into a page header
  - We often call such `block` elements **containers**
  - Master container is the `<body>` element- every other element belongs to a container and must appear only within a `<body>` element
- Height and width values never include the margins
- Technically, margins provide spacing between elements but are not a part of them.  You do need to account for margins when determining whether an item will fit in a given space.
### Common Block Elements
- Most elements are `block` elements by default.  Most common:
  - `section`, `article`, `aside`, `header`, `footer`
  - `p`
  - `h1` through `h6`
  - `ul`, `ol`, `dl`
  - `figure` and `figcaption`
    - Used to designate an area of self-contained content that does not affect the main flow of the article
    - Useful with items like diagrams, illustrations, images, and sections of computer code.  Figcaption provides the caption.
  - `form` and `fieldset`
- You can convert any element to a `block` element with `display: block;` CSS property.
- It's common to render links `<a>` and images as `block` elements

## Inline Elements
- Inline elements provide a small bit of semantic meaning to content
- Browsers use this to alter the way they display small sections of text, which, in turn, helps the reader spot specific items with ease
  - Example, if you want to use bolded text for definitions, you can use the `<b>` element to render definitions in boldface.  
- Common Inline Elements
  - `span`
  - `b`, `i`, `u`, `strong`, `em`
  - `a`
  - `sub` and `sup` (subscript and superscript)
  - `img`
- Inline elements handle the dimension properties different than `block` elements.
- Browsers handle *left* and *right* margins and padding for `inline` the same as `block` elements, but the process other properties differently
- Convert any element in `inline` by using `display: inline;` CSS property.
- Most common reason to do so is to override a prior declaration
### Inline Properties:
- `width` and `height` are ignored, except the `img` element but instead use values computed from element content
- top and bottom margins are ignored
- borders are not ignored, and results may look odd
- top and bottom padding are not ignored, but you won't notice this unless you have a border or background

## Inline-Block Elements
- `inline-block` elements are a mixture of both `inline` and `block`
- They act like `block` elements except for one significant detail- they do not take up an entire row when the `width` property is less than the available width.
- Instead, they flow in the same way that text and `inline` elements flow from one line to the next, which lets you place `inline-block` elements side-by-side with other `inline` or `inline-block` elements
- Also differ in that `inline-block` elements observe the width and height properties
- Padding, borders, margin all work like they do with `block` elements
- Browsers perform vertical alignment for adjacent `inline-block` elements as well as ordinary `inline` elements and make use of the `vertical-align` property
- It's a common misbelief that images are `inline-block` but they are in fact `inline` elements
- Convert any element to `inline-block` with the CSS property `display: inline-block;`
- Useful application for this is to arrange the contents of a list horizontally instead of vertically- like navigation bars.

## Nesting Elements and the Visual Display Model
- HTML lets you nest elements inside other elements but such nesting is not uncontrolled
- Example, you can't nest `block` and `inline-block` elements within `inline` elements
  - You can put an `em` (inline) inside a `blockquote` (block), but you can't but a `blockquote` in an `em`.
- One exception:
  - You can nest `block` and `inline-block` elements inside an `<a>` tag, provided the block does not include interactive elements like `input`, `button`, `select`, `textarea` or another `a` tag.
- Your browser may render improperly nested elements the way you want them to appear, but you should not rely on that behavior; other browsers or browser versions may not.
  - If W3C complains about nesting, you should correct it in most cases

## Other Visual Display Models
- List items default to `list-item` display model
- Table cells default to `table-cell` display model
- Won't use much in practice so don't memorize
- Two new `display` properties are poised for widespread growth: `flex` and `grid`
  - These properties solve a lot of design problems that plague front-end developers
