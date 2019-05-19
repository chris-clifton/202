# Everything is a Box
- As the browser renders a document, it processes one element at a time.  It must determine how much horizontal and vertical space (a rectangle, or box) it needs to draw them.
- It uses the browser defaults and your CSS to calculate the required dimensions.  If there's enough horizontal space remaining on current line, the browser places the next element there, otherwise, it starts a new line.
- Each line uses enough vertical space to contain all its rectangles
- This process repeats for every box on the page

## Important Takeaways
- Every element requires a box-shaped segment of the page.
- Every character of text content also needs a boxed portion of the page
- The browser calculates the dimensions of that box by using the browser defaults and CSS

## Box Properties
- Every element has the following properties (browser may ignore some)
### Width and Height
- Define how much horizontal and vertical space it needs for the *content area* of the box, which may or may not include the padding and borders
### Padding
- Is an area that surrounds the content area of the box and separates the content from its border.  Typically opaque and hides anything that it overlays.
### Border
- The boundary that surrounds the padding
### Margin
- The transparent area that lies outside the border and supplies separation between elements
### Display
- Determines how the browser lays out an element relative to its neighbors

![Chrome's Box Model](http://d3jtzah944tvom.cloudfront.net/202/images/lesson_2/chrome_box_model.png "Figure 1")

- This diagram shows an element that has a content area that:
  -  is 928 pixels wide and 168 high
  - has 10 pixels each of top and bottom padding, plus 20 each of left and right padding
  - border is 1 pixel thick
  - 28-pixel bottom margien (left, right, and top are 0)