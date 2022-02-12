# CSS Flexbox and Grid 
In CSS Flexbox Layout was designed for one dimensional layout either a row or a column while CSS Grid Layout was designed for two dimensional layout - rows and column at the same time. The two share some common features.

## Flexbox Layout
Flexbox was introduced in 2009 as a new layout system. Before the development of flexbox designers had to put too much effort with CSS to create grid layout with no guarantees that it will work in all screen sizes. Flexbox was developed to make align-content using one-dimensional layouts, either vertically or horizontally. Elements in a flexbox layout can have their height or width set to accommodate different screen sizes.

## CSS Grid Layout
CSS allows you to control over grid-template columns and rows .CSS grid allows 
content on both the rows and columns.In CSS Grid unlike the Flexbox wrapping of elements is not there.CSS grid act as an anchor to a multiple elements in a page.The main approach of CSS Grid is the layout first. Grid layout is designed for larger-scale layouts that are not linear in design.

## Flexbox Layout Example
In this example we are going to use flexbox to layout the set of boxes, We have four child items in my container and i have given the flex properties values so that they can grow and shrink from a flex-basis of 140 pixels


```
<div class="wrapper">
  <div>One</div>
  <div>Two</div>
  <div>Three</div>
  <div>Four</div>
  <div>Five</div>
</div>

.wrapper {
  width: 450px;
  display: flex;
  flex-wrap: wrap;
}
.wrapper > div {
  flex: 1 1 140px;
}

```
## CSS Grid Layout
In this example we will make the same layout using Grid. This time we have three 1fr column tracks.We do not need to set anything on the items themselves they will lay themselves out on each cell of the grid.
```
<div class="wrapper">
  <div>One</div>
  <div>Two</div>
  <div>Three</div>
  <div>Four</div>
  <div>Five</div>
</div>
.wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}





```

## Which one to choose
Flexbox works from the content out. We us Flexbox when we have a small design to implement and when you have a set of items and want to space them out evenly in a container then you let the size of the content decide how much individual space each item takes. If the items wrap onto a new line, they will work out their spacing based on their size and the available space on that line.On the other hand Grid works from the layout in. When you use CSS Grid Layout you create a layout and then you place items into it. We can define the gap between our rows or columns very easily, without having to use the margin property, which can cause some side effects especially if we’re working with many breakpoints. If you are using flexbox and you are finding yourself with limited flexibility then you may want to consider CSS Grid Layout.Also CSS grid and flexbox can work together in a layout.For example you could use flexbox to center an element like a button both vertically and horizontally within a particular grid cell.These two provides great flexibility if we use Flexbox with grid.

## **References**
- MDN Web Docs : https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Relationship_of_Grid_Layout
- Webflow Blog : https://webflow.com/blog/flexbox-and-css-grid
