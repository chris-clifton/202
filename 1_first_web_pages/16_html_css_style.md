# HTML and CSS Style Guide
- Shay Howe: Writing Your Best Code: http://learn.shayhowe.com/html-css/writing-your-best-code/

## HTML Style
- Avoid two elements on same line
- Indent nested tabs two spaces
- Don't indent `<html>` tag
- Use `/>` with self closing tags

## CSS Style
- Don't put more than one property on same line
- Exception is for using fallbacks for older browsers
- Indent property names and values by two spaces
- Put opening { on same line as selector and } on line of its own at end of property
- Include a space after the `:` but not before between properties and values
- No spaces before the `;`
- Order of properties in a rule are typically insignificant but beware of properties that override each other
- Order of rules is significant but depends on the cascade, specificity, and inheritance rules
  - List selectors in functional groups
    - Put all header-specific selectors together, all article-specific selectors together, etc.
    - Keep things grouped by functioin
    - If something doesn't work, look at cascade, specificity, and inheritance rules
    