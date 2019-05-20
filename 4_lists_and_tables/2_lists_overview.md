# Lists
- Three types of lists: unordered, ordered, description

## Unordered Lists
- Unordered lists contain a series of unordered items
  - Unordered means there is no visual numbering or naming system for items in the list
  - Content itself my have an implicit ordering, but browser displays a bullet instead of a number/letter for each item
  - Rendered vertically

## Ordered Lists
- Lists with ordered content- they have a sequence that is a visual component of the list
- Most browsers render vertical list of numbered items but you can change this to roman numerals and alphabetic

## Description Lists
- Called "Definition Lists" before HTML5 contain a list of terms and definitions
- Each item in the list includes one or more terms and one or more definitions
- Uses `<dl>`, `<dt>`, and `<dd>` tags to construct description lists

## Nested Lists
- You can nest any list within another list, regardless of types.  You can mix and match, put an unordered inside a description, etc. etc.

## Horizontal Lists
- Set the width of the menu (ul).
- Set the font for the list (ul) to 0, then restore it for the list items (li).
- Set the list items to inline-block.
- Set the width of the list items to a value that will distribute the values the way you want them distributed (typically, you want a percentage width).
- Center the list items horizontally.