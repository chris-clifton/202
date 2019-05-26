# Input Attributes
- The input tag supports a variety of attributes

## `value` Attribute
- Most input controls can use `value`, but meaning varies with the type
- For text-based types such as `text`, `email`, and `number`, the value assigns a default value for the control (works like a placeholder)
- Checkbox and radio types use the `value` attribute to set the value that the form submits for the indicated checkbox or radio group element
- Button types use `value` attribute as the label that appears on the button

## `size` and `maxlength` Attributes
- These attributes apply to most text-based input types
- `size` lets you control the size of an `input` element in characters
- `maxlength` limits the number of input values

## `placeholder` Attribute
- Lets you display some text when a field is empty to help describe expected input
- Most browsers display `placeholder` in a grayed-out font and erase the placeholder text as soon as you start typing
- Some sites use placeholders as a substitute for labels but dont do this as it breaks screen readers

## `disabled` Attribute
- lets you disable `input` elements- the browser will render the element but won't let the user interact with it
- turns on the `:disabled` CSS psuedo-class

## `required` Attribute
- Marks an input as required- browser won't let you submit the form until the user completes all required fields
- Turns on the `:required` CSS psuedo-class

## `autocomplete` Attribute
- You can use on most text-box elements 
- Common on smartphones and tablets but can be a nuisance