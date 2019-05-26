# Input Types
- The most versatile and widely used form widget is the `input` element

## Type
- Start with the `type` attribute when creating an `input` element

### Most common input types:
- `text`: creates a simple text entry field
  - User can enter any text desired in this control, though developer should almost always validate the data
  - Use the `maxlength` attribute to specify the input's maximum length
- `password`: creates a single-line text field with an obscurred value
- `email`: type allows entry of an email address in the form
  - Browsers try to prevent incorrectly formatted addresses but the developer should always validate too
- `tel`: allows entry of a telephone number- not validated by browsers since numbers vary so much worldwide
- `checkbox`: lets user choose one or more items from a series of yes/no type options
- `radio`: lets the user choose zero or one item from a list of options
  - use the `checked` attribute to mark the default radio button
  - all buttons have same `name` attribute but different `value` attribute
  - boolean `checked` attribute works same as it does with checkboxes by pre-selecting an item
  - typically work best with short lists (more than 5-8 becomes ridiculous)- use `select` when you have more than that
- `submit` creates a button that the user can click to submit the contents of a form to the server
  - The `action` attribute on the `form` tag will typically provide the URL of the server, but you can override using `formaction` attribute
- `reset` creates a button a user can click to reset contents of a form to its default values
  - Does not send a request to the server