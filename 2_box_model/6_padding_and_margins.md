# Padding and Margins

## Difference between Padding and Margins?
- Both padding and margins surround elements with whitespace
- Padding lies inside the border, and margins are outside it
- You always have them, they can just be set to zero-width so its invisible, but browser knows its there and uses it in the box model
- Margins are typically transparent and padding is typically opaque
- Padding is part of the visible and clickable bounds of an element, while a margin is the spacing between adjacent elements

## Margins, Padding, and Backgrounds
- An element's background appears in the padding area
- The container's background appears in the margin 

## Top and Bottom Margins and Padding on Inline Elements
- Browser doesn't use top and bottom margins or padding for `inline` elements for spacing
- New developers often forget this- no matter how big the top and bottom margins are on an `inline` element, they do not affect the placement of the element's content nor the content surrounding it

## Margin Collapse
- An even bigger difference between margins and padding is that top and bottom margins "collapse" between `block` elements
- If you position two adjacent `block` elements above each other, the margin between them is not the sum of the bottom margin of the first and top margin of the second- instead the margin collapses to the larger of the two margins in question
- Only occurs with top and bottom margins- not left and right.  Padding does not collapse.

## Should I use Padding or Margins?
- No firm answer 
- Strategy is to use margins for spacing between elements, and padding to affect the visible or clickable area of one
- Within a container, use padding for horizontal separation between edges and content, and margins for vertical distance.
- Another approach is to use margins everywhere except when you need padding.  Probably need padding when:
  - Want to change height of width of a border
  - Want to adjust how much background is visible around an element
  - You want to alter the amount of clickable arean
  - You want to avoid margin collapse
  - You want some horizontal spacing to the left or right of an `inline` element
  - Use padding for separation between left and rigth sides of a container and its content, use margins for vertical gap.