# Center image
- Easiest way is to use an `auto` width but you must also change the visual display model to `block`

# Center block element
- `margin: xxx auto;` where xxx is size of top and bottom margins

# Scalable width
- Makes it so the element will occupy 100% of the container (shrink with it) and scale up to 800px in size, and automatic margin makes up the difference
  ```css  
    width: 100%;
    max-width: 800px;
  ```
- Make sure no other measurements for the element are fixed or else things will get weird

# Fighting the Space Between Inline Block Elements
- Use comments
    ```html
    <ul>
      <li>one</li><!--
      --><li>two</li><!--
      --><li>three</li>
    </ul>
    ```
- Remove the whitespace all together
    ```html
    <ul>
      <li>one</li
      ><li>two</li
      ><li>three</li>
    </ul>
    ```
    ```html
    <ul>
      <li>
      one</li><li>
      two</li><li>
      three</li>
    </ul>
    ```
- Negative margins: -4px does the trick
  ```css
      nav a {
      display: inline-block;
      margin-right: -4px;
    }
  ```
- Skip the closing tag
  ```html
    <ul>
      <li>one
      <li>two
      <li>three
    </ul>
  ```
