# Forms Overview
- Allow you to gather information from users
- Vast range of data types requires you to have a large number of form controls at your disposal
- Forms are point where front-end and back-end concerns come together
- A form displays info to user, solicits updates, performs some rudimentary validation, and sends data to server

## The `form` tag
- The `form` tag is the parent for all form-related tags- tells the browser where and how to send the data
- Most important attributes are `action` and `method`
- Form should contain at least one `input`, `textarea`, or `select` tag- without one the form is useless
  - We use the terms control, widget, and input to refer to any of these elements as a group

## The `method` Attribute
- Tells browser whether it should use HTTP GET or HTTP POST method when sending data to the server
- You should use `method="get"` when requesting information form server and use `method="post"` when updating data on server
- HTTP suports several other methods but HTML limits you to GET and POST.   You must use JS or a backend application to use other methods

## `action` and `formaction` Attributes
- `action` provides the URL to which the browser sends requests
- Individual action items (`button` and `input type="submit"` elements) in a form can override the form's `action` value by using the `formaction` attribute

## `fieldset` tag
- `fieldset` is an optional tag that groups together form content as a set of related data; most browsers draw a border around the content
- While its common to remove that border with CSS, `fieldset` still provides useful semantic data to the browser and developers can reference it in their CSS for layout and styling purposes
- Forms can have multiple fieldset tags

## The `input` tag
- Describes a control or widget, that is, a mechanism that lets the user supply information or a request to the application on the server
- Each `input` requires a `type` attribute, which has a large number of valid values- each indicates teh type of widget required

## The `label` tag
- Provides a way to associate some identifying text with an input field
- Browser uses the `for` attribute in the `label` tag and the `id` attribute in the `input` tag to associate the two items
- One advantage of this association is that the user can click on the label to make the cursor jump to the desired field
