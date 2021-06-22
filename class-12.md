# Canvas Element:

- Creates a space within the HTML to draw shapes.
- Should include fallback content, which allows older browsers to display content.
- requires a closing tag, unlike an image src element.

## The Grid (or coordinate space):

- Has an x (width) axis and a y (height) axis.

### Drawing Rectangles

- fillRect(x, y, width, height)
  Draws a filled rectangle.
- strokeRect(x, y, width, height)
  Draws a rectangular outline.
- clearRect(x, y, width, height)
  Clears the specified rectangular area, making it fully transparent.
  
### Drawing Paths

- beginPath()
  Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
- Path methods
  Methods to set different paths for objects.
- closePath()
  Adds a straight line to the path, going to the start of the current sub-path.
- stroke()
  Draws the shape by stroking its outline.
- fill()
  Draws a solid shape by filling the path's content area.
