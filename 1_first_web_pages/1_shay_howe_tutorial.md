# HTML and CSS
- Hyper Text Markup Language + Cascading Style Sheets
- Never cross streams

# Common HTML Terms

## Elements
- Designators taht define the structure and content of objects within a page
- Use opening/closing tags

## Attributes
- Properties used to provide additional information about an element
- `id`, `class`, `src`, and `href` are most common
- Defined within the opening tag, after an element's name
- Generally attributes include a name and a value

# Setting up the HTML Document Structure
- All HTML documents have a required structure that includes following declaration and elements:
  - `<!DOCTYPE html>` : informs web browsers which version ofHTML is being used and is placed at beginning of document
  - `<html>` : signifies the beginning of the document
  - `<head>` : identifies top of the document, including any metadata (accompanying info about the page)
  - `<body>` : all visible content within a web page will fall within the `<body>` element

## HTML Comments
``<!--`  and `-->``

# Common CSS Terms

## Selectors
- Selectors indicate which HTML elements are being styled
- Selectors designate exactly which element or elements within our HTML to target and apply styles to
  - May include a combination of different qualifiers to select unique elements
- Selectors generally target an attribute value, such as `id` or `class` value, or target the type of element, such as ``<h1>``, or ``<p>``
- Within CSS, selectors are followed with curly braces, which encompass the styles to be applied to the selected element

## Properties
- Once an element is selected, a property determines the styles that will be applied to that element
- Property names fall after a selector, within curly braces, and immediately preceding a colon `:`
- Examples: `background`, `color`, `font-size`, `height`, and `width`.

## Values
- Used to determine the behavior of the property with a value
- Values come after the colon and before semicolon

## CSS Comments
`/*` and `*/`

# Working With Selectors

## Type Selectors
- Type selectors target elements by their element type, such as ``<div>``, or ``<p>``

## Class Selectors
- Allow us to select an element based on the element's class attribute
- They are a little more specific than type selectors, as they select a particular group of elements rather than all elements of one type
- Allow us to apply same stylkes to different elements at once by using same `class` attribute across multiple elements
- Classes denoted by a leading period followed by the `class` attribute value- `.exampleclass`,

## ID Selectors
- Target only one unique element at a time
- Regardless of which type of element they appear on, `id` attribute values can only be used once per page
- ID selectors are denoted by a leading hash symbol followed by the `id` attribute value- `#shayhowe`

## Additional Selectors
- More selectors exist: https://learn.shayhowe.com/advanced-html-css/complex-selectors/

# Referencing CSS
- In order to get our CSS talking to our HTML, we need to reference the CSS file within our HTML
- Best practice is to include all styles in a single external stylesheet, which is referenced from within the ``<head>`` element of our HTML document
- Using a single external stylesheet allows us to use the same styles across an entire website and quickly make changes sitewide.

# Using CSS Resets
- CSS resets take every common HTML element with a predefined style and provide one unified style for all browsers
- Generally involve removing any sizing, margins, padding, or additional styles and toning these values down
- Because CSS cascades from top to bottom, our reset needs to be at top of style sheet

---------------------------------------------------------------------------------------------------------------------

# Getting to Know HTML

## Semantics Overview
- Semantics within HTML is the practice of giving content on the page meaning and structure using the proper element
- Semantic code describes the *value* of content ona page, regardless of the style or appearance of that content, regardless of the style or appearance of that content
- Several benefits to using semantic elements:  
  - Enabling computers (screen readers, search engines, other devices) to adequately read and understand the content of a webpage
  - Easier to manage and work with as it clearly shows what each piece of content is about
- A ``<p>`` is considered semantic because the content wrapped in a ``<p>`` element is known and understood as a paragraph.

## Block vs Inline Elements
- Block-level elements begin on a new line, stacking on top of the other and occupy any available width
  - May be nested inside one another and may wrap inline-level elements
- Inline-level elements do not begin on a new line- they fall into the normal flow of a document, lining up one after the other and only maintain the width of their content.
  - Inline-level elements may be nested inside one another, however, they cannot wrap block-level elements.

## `<div>` and `<span>` // Divisions & Spans
- ``<div>`` and ``<span>`` are HTML elements that act as containers solely for styling purposes- they do not hold any semantic value.
- ``<div>`` and ``<span>`` are both extremely valuable when building a website in that they give us the abiliity to apply targeted styles to a contained set of content.
- A ``<div>`` is a block-level element that is commonly used to identify large groupings of content and which helps to build a web page's layout and design.
- A ``<span>`` is an inline-level element commonly used to identify smaller groupings of text within a block-level element.
- Common to see div's and span's with a `class` or `id` for styling
  - Must be careful choosing these attribute names- they should describe the content of an element, not the appearance

# Using Text-Based Elements

## `<h1>` through `<h6>` // Headings
- Headings are block-level elements and come in six different rankings: `<h1>` through `<h6>`
  - Headings help quickly break up content and establish hierarchy
  - Are key identifiers for users reading a page
  - Help search engines to index and determine content on a page
- Headers should be used in an order that is relevant to the content of a page
  - Primary heading should be marked `<h1>`
- Each heading level should be used wher it is semantically valued and not be used to make text bold or big

## `<p>` // Paragraphs
- Headings often followed by supporting paragraphs and defined using `<p>`
- Paragraphs can appear one after the other, adding info to a page as desired.

## `<strong>` and `<b>` // Bold
- To make text bold and place a strong importance on it, use the `<strong>` inline-level element
- `<strong>` is semantically used to give strong importance to text and is most popular for boldig text
- `<b>` means to stylistically offest text, which isn't always best choice for text deserving prominent attention

## `<em>` and `<i>` // Italics
- To italicize text, thereby placing emphasis on it, use `<em>` inline-element
- `<i>` element is used to semantically convey an alternative voice or tone, almost as if it were placed in quotation marks

## `<blockquote>` // Block Quote
- Extended quotations should use the `<blockquote>` tag.  

# Building Structure
- Stucture used to be built using divs- problem with that was that divs provide no semantic value and it was difficult to determine the intention of the divs
- HTML5 introduced structurally based elements including: ``<header>``, ``<nav>``, ``<article>``, ``<section>``, ``<aside>``, and ``<footer>`` elements
  - All these elements are intended to give meaning to the organization of our pages and improve our structural semantics
  - Are all block-level elements and do not have any implied position or style
  - Elements may be used multiple times per page, so long as each use reflects the proper semantic meaning

## `<header>` // Header
- ``<header>``
- Used to identify the top of a page, article, section, or other segment of a page
- In general, header element may include a heading, introductory text, and even navigation

### `<header>` vs `<head>` vs `<h1>` through `<h6>`
- `<header>` is the structural element that outlines the heading of a segment of a page and falls within the `<body>` element
- `<head>` element is not displayed on a page at all and is used to outline metadata, like document title and links to external files and falls within the `<html>` element
- Heading elements `<h1>` through `<h6>` are used to designate multiple levels of text headings througout a page

## `<nav>` // Navigation
- `<nav>` element identifies a section of major navigational links on a page
- Should be reserved for primary navigation sections only, such as global navigation, a table of contents, previous/next links, or other noteworthy groups of nav links
- Most commonly, links included in `<nav>` element will link to other pages within the same website or parts of same web page
  - Miscellaneous one-off links should not be wrapped in `<nav>` and should use the `<a>` anchor element instead

## `<article>` // Article
- The `<article>` element is used to identify a section of independent, self-contained content that my be independently distributed or reused
- Often use `<article>` element to mark up blog posts, newspaper articles, user-submitted content, etc.
- `<article>`'s have `<sections>`
- When deciding to use `<article>`, we must determine if the content within the element could be replicated elsewhere without
  - If the content within `<article>` were removed from the context of the page and placed somewhere else (printed, in an email) that content should still make sense

## `<section>` // Section
- Used to identify a thematic grouping of content, which generally, but not always, includes a heading
- The grouping of content within the `<section>` element may be generic in nature but its useful to identify all the content as related
- Commonly used to break up and provide hierarchy to a page

### `<article>` vs `<section>` vs `<div>`
- Look at the content
- Both `<article>` and `<section>` elements contribute to a document's structure and help outline a document
- If content is being grouped solely for styling purposes and doesn't provide value to outline of document, use `<div>`
- If content adds to document outline and can be independently redistributed or syndicated, use `<article>`
- If content adds up to the document outline and represents a thematic group of content, use `<section>`

## `<aside>` // Aside
- `<aside>` holds content, such as sidebars, inserts, or brief explanations that is tangentially related to content surrounding it.
- When used within an `<article>` element, `<aside>` may identify content related to the author of the article
- We may instinctively think of an `<aside>` as an element that appears off to the left or right side of a page
  - Must remember, though, that all structural elements, including `<aside>` are block-level elements and as such will appear on a new line and occupy the full available width of the page or of the element they are nested within (parent element)

## `<footer>` // Footer
- `<footer>` identifies closing or end of a page, article, section, or other segment of a page
- Generally found at the bottom of its parent
- Content within `<footer>` element should be relative information and sould not diverge from the document or section its included with

## `<a>` // Anchor
- By nature the anchor element is an inline element and, according to web standards, inline elements may not wrap block-level elements
- With the intro of HTML5, anchor elements specifically ahve permission to wrap either block, inline, or any other level elements
- This allows entire blocks of content on a page to become links

## Relative and Absolute Paths
- Two most common types of links are to *other pages* of same website and links to *other websites*.
- Links pointing to other pages of same webpage will have a relative path
- Links pointing to other webpages will have absolute paths and require the full domain

## Linking to an Email Address // Encoding Parameters
- To create an email link, the `href` value needs to start with `mailto:` followed by the email address to which the email should be sent
- Additionally, subject line and other info may be populated
- To add subject line, include `subject=` parameter after email address and question mark
- Multiple words must be encoded using `%20`
- Ex: altogether, a link to `shay@awesome.com` with subject of "Reaching OUt" and a body text of "How are you" would require following `href`:
  - ``<a href="mailto:shay@awsesome.com?subject=Reaching%20Out&body=How%20are%20you">`Email Me`</a>``

## Opening Links in New Window
- One feature available with hyperlinks is the ability to determine where a link opens when clicked.  Typically, links open in the same window from which they are clicked, but some may be opened in new windows
- To trigger action of opening in new window, use `target` attribute with a value of `_blank`
- `target` attribute specifies where the link will be opened and `_blank` specifies a new blank window

## Linking to Parts of the Same Page
- Create on-page link by first setting an `id` attribute on the element we wish to link to
- Then, use the value of that `id` within an anchor element's `href` attribute with a poundsign
  - Ex: ``<body id="top">``....``<a href=#top>`Back to Top`</a>``

---------------------------------------------------------------------------------------------------------------------

# Getting to Know CSS

## The Cascade
- Within CSS, all styles cascade from the top of a style sheet to the bottom, allowing different styles to be added or overwritten as the style sheet progresses

## Cascading Properties
- Cascade also works with properties inside individual selectors
- If you set a background property to orange, and then directly below set it to green, you will get a green background

## Calculating Specificity
- Every selector in CSS has a specificity weight
- A specificity weight, along with its placement in the cacade, identifies how its styles will be rendered
  - `type`, `class`, and `id` selectors each has a different specificity weight
- `type` has the lowest specificity and holds a point value of `0-0-1`
- `class` has a medium specificity and holds a point value of `0-1-0`
- `id` selector has a high specificity and holds a point value of `1-0-0`

## Specificity Points
- Three columns: first column counts ID selectors, second column counts class selectors, third column counts type selectors
- Intentionally hyphenated, as their values are not computed from a base of 10
- The higher the specificity weight of a selector, the more superiority the selector is given when a styling conflict occurs

## Combining Selectors
- By combining selectors we can be more specific about which element or group of elements we'd like to select
- When selectors are combined, they should be read *right to left* with the rightmost selector being the *key selector*
- The key selector identifies exactly which element the styles will be applied to.  Any selector to the left is a prequalifier.

## Spaces within Selectors
- Use and omission of spaces makes a huge difference in selectors
- Take `.hotdog p.mustard` for example
- Since there isn't a space between paragraph's type selector and the `mustard` class selector that means the selector will only select paragraph elements with the class of `mustard`.  If the paragraph type selector was removed, and the mustard class selector had spaces in it, it would select any element with the class of mustard
- The best practice is not to prefix a class selector with a type selector
- Generally, we want to select any element with a given class, not just one type of element and, following this, we should redo this as `.hotdog .mustard`

## Specificity Within Combined Selectors
- When selectors are combined, so are the specificity weights of the individual selectors
- These can be calculated by counting each different type of selector within a combined selector
- The higher our specificity weights rise, the more likely our cascade is to break

## Layering Styles with Multiple Classes
- One way to keep the specificity weights of our selectors low is to be as modular as possible, sharing similar styles from element to element
- One way to be as modular as possible is to layer on different styles by using multiple classes
- Elements in HTML can have more than one class attribute value so long as each value is space separated
- With that, we can place certain styles on all elements of one sort while placing other styles only on specific elements of that sort

## Common CSS Property Values

### Colors
- All color values within CSS are defined on an sRGB (standard red, green, blue) color space
- Colors within this space are formed by mixing rgb color channels together, mirroring the way tv's and monitors generate all the different colors they display
- There are four primary ways to represent sRGB colors in CSS
#### Keywords: `red;`
- Color values names such as `red`, `green`, and `blue`
- Are simple in nature, but provide limited options and are not the most popular color value choice
#### Hexadecimal: `#ff6600;`
- Consist of a pound folowed by a three or six character hexadecimal figure /[0-9a-f]/i with 16.7 million possible colors
- Six figure notation:
  - Characters 1 and 2 - red
  - Characters 3 and 4 - green
  - Characters 5 and 6 - blue
  - If these three pairs are all matching (`#ff6600`) then it can be shortened to `#f60`
- 0 equals black, f equals white
#### RGB and RGBa: `rgb(128, 0, 0);` and `rgba(128, 0, 0, .5);`
- Stated using the `rgb()` function and uses three comma-separated values each an integer between 0 and 255
- 0 equals black, 255 equals white
  - First value - red
  - Second value - green
  - Third value - blue
- Allow an alpha/transparency channel by using the `rgba()` function, which requires a fourth value which must be a number between 0 and 1
  - This decimal determines the opaqueness of the color
  - 0 fully transparent, 1 fully opaque
#### HSL and HSLa: `hsl()` and `hsla()`
- Stands for Hue, Saturation, and Lightness
- Within parenthesis, function accepts three comma-separated values, like `rgb()`
  - First value - Hue
    - Number 0 to 360
    - Representing degree value on color wheel
  - Second Value - Saturation
    - Percentage 0% to 100%
    - Represents how saturdated with color the hue is with 0% being grayscale and 100& being fully saturated
  - Third Value - Lightness
    - Percentage 0% to 100%
    - How light or dark the color is with 0% being black and 100% being white
- Also may include an alpha or transparency channel, same as RGBa

### Lengths
- Length values in CSS are similar to colors in that there are a handful of different types of values for length- all serve distinct purposes
- Length values come in two forms: absolute and relative
#### Absolute Lengths
- Simplest length value- they are fixed to a physical measurement such as inches, centimeters, or millimeters
- Most popular unit is the pixel and represented as `px`
##### Pixels
- Pixel is equal to 1/96th of an inch, thus there are 96 pixels in an inch
- Exact measurement of a pixel may vary slightly between high-density and low density viewing devices
- Pixels have lost some popularity due to changing landscape of viewing devices and varying screen sizes/resolutions
- They are trustworthy for getting started, though
#### Relative Lengths
- Relative lengths rely on the length of another measurement
##### Percentages
- One of the most popular relative values
- Defined in relation to the length of another object
- For example, to set the `width` to 50%, we have to know the width of the parent element
##### Em
- The `em` unit is also popular relative value
- Calculated based on an elements font size
- A single em unit is equivalent to an element's font size
- Ex: If an element has a font size of `14px;` and a width set to `5em;` the width would be `70px` (14 * 5)
- When a font size is not explicitly stated for an element, the em unit will be relative to the font size of the closest parent element with a stated font size

---------------------------------------------------------------------------------------------------------------------

# The Box Model

## How are Elements Displayed?
- Block-level elements: occupy any available width, regardless of their content, and begin on a new line
- Inline-level elements: occupy only the width their content requires and line up on the same line, one after the other

### Display
- Exactly how elements are displayed is determined by the `display` property
- Every element has a default `display` property value, however, the value may be overwritten
- Most common values for `display` property are `block`, `inline`, `inline-block` and `none`
- Space Between Inline-Block elements
  - One important distinction with inline-block elements is that they are not always touching, or displayed directly against one another
  - Usually a small space will exist between two inline-block elements







---------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------