# Notes from Walkthrough

# Escaping HTML
- Escape characters with ascii table http://www.asciitable.com/

## Ampersands
- Ampersands can cause trouble with some HTML- best to just always use `&amp;` to be safe.

## Double Quotes
- Use `&quot;` to embed a double quote inside a double-quoted attribute value
- Common practice to replace " with `&quot;` when using an external source of strings inside HTML since you can't know in advance which strings will need `&quot;` and wint won't.

---------------------------------------------------------------------------------------------------------------

# CSS

## Applying CSS
- Three main ways to use CSS in a webpage: inline, internal, and external
- **Inline** CSS uses the `style` attribute on individual HTML tags
- **Internal** CSS uses the `style` element to store all of the CSS in one place in the file
- **External** CSS stores the CSS in a file that is separate from the HTML file

### Inline CSS
- Adding a `style` attribute applies some CSS styling to the single element identified by the tag
- However, defining styles one at a time is tedious and error-prone, and it mixes the presentation ifo with the content
- You will see inline styles in prod code but principally in conjunction with dynamically generated web-pages

## Internal CSS
- Instead of scattering style info all over page with `style` attributes, you can list it all in the `style` element, which belongs inside the `head` element
- The `style` element is easy to use and it puts everything together in one file, which makes it most convenient when you need the CSS for a single page

## External CSS
- Placing CSS in a separate file and identifying that file as a `stylesheet` with a `<link>` tag tells the browser that it should load CSS style info from an external file located on the server
- The `link` tag belongs inside the `<head>` element
- Ex: `<link rel="stylesheet" href="path_to_stylesheet.css" />`
- This is the preferred way to include CSS in most web pages since it lets you share CSS between multiple pages and makes maintenance of CSS code separate from that of HTML
- Browsers can also cache external CSS files which can reduce page load times