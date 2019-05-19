# Adding Images to Web Pages

## The `<img>` element
- `<img>` is a self-closing tag that tells the browser to laod an image from a separate resource, such as a file on the server, and display it
- It has two attributes you should use every time you use it and one that you should use when you don't supply a caption
- `src`: the required attribute source tells the browser where to find the image
- `alt`: the alt attribute describes the content of the image as an aid for users who cannot view the images.
  - Also, most browsers will display the alt text when they can't display an image
  - Search engines use `alt` to index images, which makes it relevant for SEO
- `title`: title attribute supplies some text that the browser can display using alternative means, such as a tooltip.  
  - Title is a good choice when you don't include an explicit caption with the image
  - Avoid using the same value for `alt` and `title`- screen readers read both attributes to the user, which is annoying.
```html
  <img src="lucrezia.jpg" alt="Da Vinci's Smarter Sister, Lucrezia" title="Lucrezia's Portrait" />
```

## Figure and Figcaption
- If we want a caption for an image, we can add a paragraph element below it, but there's no way to show the relationship between the `img` and `p` elements.
  - You could group them in a div, but a div has no semantic meaning and fails to establish a connection
- The `figure` element fills this gap- it designates an item as a representation of information discussed in the content
```html
  <figure>
    <img src="masthead.jpg" alt="Sunset over the forest" />
    <figcaption>The sun sets over the dense forest</figcaption>
  </figure>
```
- If you don't reference the media in the text, and you don't need a caption, then you don't need the figure tag

## Images as Links
- To make an image clickable, put the `img` tag inside the `a` tag
```html
  <a href="url-of-link">
    <img src="url-of-image" alt="alt-text" title="title-text"/>
  </a>
```
## Background Images
- You can add background images to a page or element by applying the CSS `background` or `background-image` property
- Background images appear behind the content for the element that requested the background and its descendents
- Most background images apply to an entire page, so we use the body selector to specify them
- There are several other background properties you can provide with a background image, including the size of the image, positioning, and repeat counts

## Working with Images
- When you provide a width, but no height, the height is adjusted automatically to maintain the aspect ratio