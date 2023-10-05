# CSS NOTES

## Conflicts
- Order of preceedence
    - Declarations marked !important
    - Inline styles
    - id (if multiple, latest in code applies)
    - class or pseudo-class (:)
    - element selector
    - universal selector (*)

## Iheritance
- Some styles get their styling from their parent elements (e.g., <body><p>).
- The most specific style is the one applied (i.e., inherited properties get overwritten).
- All styles do not get inherited (e.g., border-top, margin-top etc.). Mostly Text related props are inherited.

## Box Model (default)
- Defines how elements are displayed (content border and space within)
- Padding: Inside the element
- Margin: Outside the element
- Border: Border of the element (still part of the element)
- Content: Content of the element
- Fill area: Content + Padding (bg image, bg color)
- Final element width (default): Content + Padding + Border + Margin
- Final element height (default): Content + Padding + Border + Margin

### Box Model (box-sizing: border-box)
- Final element width: Content + Padding + Border
- Final element height: Content + Padding + Border
- Padding and border are included in the width and height of the element

### Padding
- Order of padding: top, right, bottom, left (clockwise)
- Order when specifying just two values: top/bottom, right/left (clockwise)
- When needed space within and element

### Margin
- Order of margin: top, right, bottom, left (clockwise)
- Overlapping margins do not add up -> Collapsing margins (largest margin wins)
- When needed space outside an element

### Adding dimension to an element
- width: 100px;
- height: 100px;

### Types of boxes
- Block: Takes up the whole width of the page (e.g., div, p, h1, h2, h3, h4, h5, h6, ul, ol, li, form, table)
- Inline: Takes up only the space it needs (e.g., span, a, img, input, textarea, button)
- Inline-block: Takes up only the space it needs but can have width and height (e.g., input, textarea, button)
    - takes up the space it needs
    - can have width and height
- None: Element is not displayed (e.g., display: none;)
- Flex: Element is displayed as a flex container (e.g., display: flex;)
- Grid: Element is displayed as a grid container (e.g., display: grid;)
- Inline-flex: Element is displayed as an inline flex container (e.g., display: inline-flex;)
- in css you can change behaviour by setting display: block/inline/inline-block

## FLOW
- Normal vs Abslutely positioned elements

### Normal flow
- Elements are positioned in the order they appear in the HTML code

### Absolute positioning
- Elements are positioned relative to their parent element
- "Out of flow" -> Does not affect the position of other elements
- By default positioned relative to the body element
- Can be positioned relative to the nearest positioned ancestor that has a position other than static (e.g., relative, absolute, fixed, or sticky)
- Used for single small elements 

## Pseudo elements
- Meant to style a specific part of an element
- + is the adhacent sibling selector

## Layout
- How all elements are displayed on a page
- Gives the page a structure

### Floats
- Floats are used to wrap text around an image
- Floats are used to create entire web layouts
- Floats are used to create text columns
- Floats are used to "fix" elements at a specific position
- When setting a float value to an eleement, it is as if it is removed from the normal flow of the page and not considered by marginals paddings etc. of other elements
- using the poperty clear: both; on an element will make it go below the floated element
- clearfix hack: https://www.w3schools.com/css/css_float.asp

## FLEXBOX
- Flexbox is a layout mode that arranges elements in a predictable way for different screen sizes and browsers
- Flexbox is direction-agnostic
- Flexbox is a whole module and not a single property
- Flexbox is based on "flex-flow directions"
- Flexbox allows you to align elements vertically and horizontally by setting the propery justify-content and align-items
    - align-items: center, flex-start, flex-end, stretch, baseline
    - justify-content: center, flex-start, flex-end, space-between, space-around, space-evenly
- set of related CSS properties for building 1-dimensional layouts
- Main idea is to divide the available space into flex items within their container
- Makes it easy to autimatically align items to on another inside a parent container
- The element on where we want to use the flexbox is called the *flex container*
- The elements inside the flex container are called *flex items*
- The direction for the flex items is called the *main axis*
- The direction perpendicular to the main axis is called the *cross axis*

### Flex container
- Properties: gap, justify-content, align-items, flex-direction, flex-wrap, flex-flow, align-content

### Flex items
- Properties: order, flex-grow, flex-shrink, flex-basis, flex, align-self
- Addign manually space between flex items: margin-left: 10px; margin-right: 10px; OR gap: 20px;

### Default Flexbox properties
- flex-grow (default 0) -> if the elements can grow if needed
- flex-shrink (default 1) -> if the elements can shrink if needed
- flex-basis (default auto) -> width of the element (not rigid, the browser optimizes the space for the content)
- flex 1 -> flex-grow: 1; flex-shrink: 1; flex-basis: 0%;

## Grid
- Grid is a layout mode that arranges elements in a predictable way for different screen sizes and browsers
- enabled by display: grid;
- The amount of columns is specified through the property grid-template-columns (e.g., grid-template-columns: 100px 100px 100px;)
- the row height and count can be set by grid-template-rows (e.g., grid-template-rows: 100px 100px 100px;)
- A grid is made up of columns and rows, like a coordinate system
- You can specify an item in the grid by using the grid-column-start and grid-column-end properties (e.g., grid-column-start: 1; grid-column-end: 3;)
- gap 2px 2px = row-gap 2px column-gap 2px
- grid-row grid-column