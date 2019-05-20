# Tables
- Using tables for layout is an old trick, but today, should stick to using them for tabular data

## Table Tags
- `<table>` tag defines a table
- `<tr>` defines a single row in a table
- `<td>` defines a single cell of content in a table
- `<th>` defines a single heading
  - The first cell in a row or column is typically a heading, but not required
- `<thead>`, `<tbody>`, and `<tfoot>` each define a set of one or more rows that comprise the header, body, and footer rows of a table

## Semantic Table HTML and Heading Scope
- You can use `thead`, `tfoot`, and `tbody` elements to provide semantic identification for header, footer, and body rows
- You can also add the `scope` attribute to identify `th` elements as row (`scope="row")` or column (`scope="col"`) headings

## Tables and CSS
### Background color bleed/eliminate spaces between cells
```css
table {
  border-collapse: collapse;
}
```

## Styling rows differently
```css
tbody tr:nth-child(2n+1) {
  background-color: orange;
}
tbody tr:nth-child(2n+2) {
  background-color: yellow;
}
```
## Styling column headers and row headers differently
```html
<table id="people-table">
  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Major</th>
      <th scope="col">GPA</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Chris Lee</th>
      <td>Supply Chain Mgmt</td>
      <td>3.7</td>
    </tr>
    <tr>
      <th scope="row">Shane Riley</th>
      <td>Photojournalism</td>
      <td>3.8</td>
    </tr>
    <tr>
      <th scope="row">Kevin Wang</th>
      <td>Computer Science</td>
      <td>4.0</td>
    </tr>
  </tbody>
</table>
```
```css
[scope="col"] {
    background-color: green;
}
[scope="row"] {
  background-color: cyan;
}
```

## Make heading span multiple columns
- Use rowspan
```html
<table id="Wine">
  <thead>
    <tr>
      <th scope="col">Type</th>
      <th scope="col">Name</th>
      <th scope="col">Price</th>
    </tr>
    <tr>
      <th scope="row" rowspan="3">Red</th>
      <td>Meiomi Pinot Noir</td>
      <td>$17.99</td>
    </tr>
    <tr>
      <td>Radios Cabernet</td>
      <td>$9.99</td>
    </tr>
    <tr>
      <td>Apothic Red</td>
      <td>$9.97</td>
    </tr>
    <tr>
      <th scope="row" rowspan="3">White</th>
      <td>Kendall Jackson Chardonnay</td>
      <td>$9.97</td>
    </tr>
    <tr>
      <td>Kim Crawford Sauvignon Blanc</td>
      <td>$9.97</td>
    </tr>
    <tr>
      <td>Cloud Break Chardonnay</td>
      <td>$8.99</td>
    </tr>
    <tr>
      <th scope="row" rowspan="3">Sake</th>
      <td>Gekkeikan Sake</td>
      <td>$9.99</td>
    </tr>
    <tr>
      <td>Mura Mura Mountain Sake</td>
      <td>$15.99</td>
    </tr>
    <tr>
      <td>TY KU Sake Junmai Ginjo Black</td>
      <td>$21.99</td>
    </tr>
  </thead>
</table>
```