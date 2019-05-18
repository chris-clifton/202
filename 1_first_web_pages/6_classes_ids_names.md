# Classes, ID's and Names
- HTML provides three ways to identify certain elements: classes, ID's, and names
- Any element can use a `class` or `ID`, some can use `name` and some can use all three at once.

## Classes
- The `class` attribute idenfities a set of page elements that you wish to style consistently
- Use the `class` attribute to assign a class or classes to an element
- Any number of elements may belong to the same class
- ANy element can belong to one or more classes- list al names separated by spaces in the `class` attribute
- Prefer semantic class names, they should provide meaning.
- Use CSS class selectors (`.classname`) to select elements by class
- Class selectors have lower CSS specificity than ID selectors, but higher than tag name selectors

## IDs
- The `id` attribute applies a unique identification string to a single element, such as a headline
- No other `id` attributes on the page should have the same ID
- Use the `id` attribute to assign an ID to an element
- Each ID on a page must be unique
- Each element can have one ID or none
- Use semantic ID names- they should provide meaning
- Use CSS ID selectors (`#idname`) to select elements by ID
- ID selectors have a higher specificity than class selectors and type selectors
- Browsers wont tell you when you use the same ID on more than one element.  Won't totally break HTML/CSS but will cause problems with JS
- Use the W3C HTML validator to catch accidental ID duplication

## Names
- We won't use the `name` attribute a whole lot but its worth knowing that it ties form elements to data on the server (typically doesn't play a role in styling)
- Since the `for` attribute references an ID, its accepted practice to use both a `name` and an `id` on form elements and use the same value for both
- Use the `name` attribute to assign a name to a form data element that the server can use to obtain the value
- Not all tags accept the `name` attribute, it applies to input controls in forms.  Some other elements ahave a name attribute too but with a different meaning.
- Always use a `name` attribute on form elemetns that accept it
- Each name in a form should be unique to that form except for radio buttons and checkboxes that belong to a single group
- Use descriptive `name` values, not semantic.  For instance, use `name="last-name"` instead of `name="input-field"`
- Avoid trying to select elements in CSS by using the `name` attribute

