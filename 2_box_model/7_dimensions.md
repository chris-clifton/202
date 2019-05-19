# Dimensions
- Some CSS properties require lengths as property values to provide the size of some detail on the page
  - Example, font-size, margin, padding, width etc. use 12px or 3em or 50%
  - These values are **measurements** or **dimensions**
  - `px`, `rem`, `%` etc. are called **measurement units** or **units**

## `<length>`
- Length data type represents a distance value
- Percentage values are CSS dimensions and though they are usable in some of the same properties that accept length values, they themselves are not length values
### Syntax
- Consist of a number followed by a unit
#### Relative Length Units
- Relative lengths represent a measurement in terms of some other distance.  Depending on the unit, this can be the size of a specific character, line heigh, or size of viewport
- Font-relative lengths define the length value in terms of the size of a particular character or font attrbute in the font currently in effect in an element or its parent
- Relative units, especially `em` and `rem` are often used to create scalable layouts, which maintain the vertical rhythym of the page even when the user changes the font size
- `em`: represents the calculated font-size of the element.  If used on the `font-size` property itself, it represents the inherited font-size of the element
- `rem`: represents the font-size of the root element (typically `<html>`).  When used within the root element font-size, it represents its initial value (a common browser default is 16px, but user-defined preferences may modify this)
#### Absolute Length Units
- Represent a physical measurement when the physical properties of the output medium are known, such as for print layout
- This is done by anchoring one of the units to a physical unit, and then defining the others relative to it
- The anchoring is done differently for low-resolution devices like screens than high-resolution devices like printers
  - Low-dpi devices: the unit px represents the physical reference pixel; other units are defined relative to it
    - 1in is defined as 96px, which equals 72pt- consequence is dimensions described in inches, centimeters, and millimeters don't necessarily match the size of the physical unit with the same name
  - High-dpi devices: inches, centimeters, millimeters are samea s their physical counterparts
- Many users increase client's default font size to make text more legible so absolute lengths can cause accessibility problems since they are fixed and do not scale according to user settings.  For this reason, prefer relative lengths when setting font-size.
- `px`: one pixel.  For screen displays, traditionally represents one device pixel (dot), however for printers and high-dpi devices, one css pixel implies multiple device pixels. 1px = 1/96th of 1in
- `cm`: centimeter 1cm = 96px/2.54in
- `mm`: millimeter 1mm = 1/10th of 1cm
- `in`: inch 1in = 2.54cm = 96px
- `pt`: one point 1pt = 1/72nd of 1in

### Interpolation
- When animated, values of the length data type are interpolated as real floating-point numbers.  Inteprolation happens on the calculated value.  Sped is determined by the timing function associated with the animation.

## `<percentage>`
- Percentage data type represents a percentage value.  It is often used to define a size as relative to an element's parent object
- Numerous properties can use percentages, such sa width, height, margin, padding, font-size
### Syntax
- The percentage data type consists of a number and percent sign
- Optionally, may include a `+` or `-` sign, though negative values are not valid for all properties
### Interpolation
- When animated, values of the percent data type are interpolated as real floating-point numbers.  Speed determined by the timing function of the animation.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Absolute vs Relative Units
- We measure everything using either absolute or relative units
## Absolute Units
- CSS has one absolute unit of significance: the pixel
- Pixels are similar to the single dot on a monitor but the actual term implies a lot more meaning
- Physical vs Reference Pixel
  - Problem with using pixels as absolute unit: a pixel on desktop computer and a pixel on a cell phone aren the same size
  - Worst yet, the pixel density of displays causes variations in size as well.  A pixel on a high def screen is much smaller than a pixel on a standard or low resolution dispaly
  - CSS distinguishes between a physical pixel (device pixel) and reference pixel (CSS pixel). 
  - The size of a referenc epixel is the size of a pixel on a display that has 96 pixels per inch
    - If you're on a high res display, you might have 192 pixels per inch
## Relative Units
- em, rem, percentages
#### Ems and Rems
- Ems and rems are proportional to the calculated and root font sizes, respectively.  
  - The calculated font size is the height of the current font in pixels.  
  - The root font size is the height of the base font for the document: the font size desginated for the `html` element
  - If the calculated font size is 20 pixels and root font size is 16 pixels, then 1.5em is 30 px while 1.5rem is 24px.
- In most cases, you should use pixels to specify the root font size.  Some devs use ems or rems to give the user some control over the font, but this can result in odd behavior as your precisely positioned items start to overflow, overlap or rearrange themselves on the page
  - Good idea to set root font size in both the html and body elements and always use pixels when you do so
  - Easier to work with rems instead of ems since rems are consistent.  Once youve set root font size for document, 1.5rem means the same thing everywhere else in doc
    - Some older browsers dont support rems so use a fallback  (font-size: 20px; font-size: 1.25rem;)
#### Percentages
- Use percentages to define dimensions as a fraction of the container's width or height
- If you place a `block` or `inline-block` element in a container and set it to `width: 50%;`, the element's width is 50% of the width of the container
  - Remember width and height have no effect on `inline` elements
#### Auto
- The `auto` specifier can be used when you want to let browser determine a width or height for you
- Common uses:
  - As a width or height, it tells the browser to try to fit the etnire element in its container
  - As a left or right margin value on a block element, it tells the browser to push the element all the way to the right or left inside its container (it pushes it the opposite direction!).  You can center a block element by setting both left and right margins to auto
  - As a top of bottom margin value, auto is equivalent to 0
  - Padding does not accept auto values
#### Zero Lengths
- Standard CSS style omits the units when providing a length of 0 units.  You can just write '0' because 0 is the same in any unit.
#### Mixing Units
- You can freely mix units anywhere you want on a page, you can use pixels for some elements, rems for others, % and auto even within a single element's styling
- But be careful- mixing and matching can lead to problems when you want to determine the "right" length to make something come out correct

### When to Use the Different Units
- Use absolute units sparingly and stick with pixels.  Pixels work well for:
  - root font size
  - image widths and heights
  - top and bottom margins and padding, sometimes useful with left and right margins and padding
  - width or height of fixed-width/fixed-heigh containers such as navigation side bars
  - border widths
- Use relative units liberally:
  - Use rems for fonts, possibly with a fallback to ems or pixels.  The root font should use pixels
  - If you must use ems instead of rems, try to avoid compounding font sizes
  - Use rems, ems, or pixels for left and right margins and padding
  - Use % for measurements that are proportional to the container element's width/height
    - Percentages work best for container dimensions and come in handy when you want certain areas of the page to grow and shrink as the width of the browser window changes
  - Use auto with width and height to let the browser calculate an appropriate value
  - Use auto with left and right margins to left, center, or right justify a block element within its container
- You can ignore or break these rules when appropriate