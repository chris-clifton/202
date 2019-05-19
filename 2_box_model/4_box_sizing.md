# Box Sizing

## Article: CSS-Tricks | Box Sizing
- https://css-tricks.com/box-sizing/

### Important Takeaways
- The usable `box-sizing` property values are `content-box` and `border-box`.  The CSS standard deprecates the `padding-box` setting so dont use it.
- The `content-box` setting is the default setting for the `box-siznig` property for all elements in all modern browsers.
  - In this model, the width and height properties specify the size of the content area- you need to add padding and borders to get the size of the visible box
- The `border-box` setting causes the browser to interpret the width and height properties as the total width and height of the box, excluding margins
  - Padding and borders subtract from the content area
- The `border-box` setting is the "best" since it simplifies the math a dev must do
  - Ex: if we have a box with with of 50% and padding of 12px, it insures it's precisely 50% of container width, not 50% plus 24px (12px each side)
- If you want to use `border-box` pretty much everywhere, use following CSS
```CSS
  html {
    box-sizing: border-box;
  }

  *, *::before, *::after {
    box-sizing: inherit;
  }
```

h338
w