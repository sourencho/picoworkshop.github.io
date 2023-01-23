---
title: "Text, Lines, Shapes & Color"
---

##  Let's draw with code!

## Circle

Pico-8 has a special function `_draw` that executes over and over

Let's try to draw a circle using this function

```lua
function _draw()
  -- clear screen
  cls()

  -- circfill( x, y, radius, color )
  circfill(64, 64, 6, 12)
end
```

The screen is 128x128 pixels and the X and Y values flow right and down. To pick a color use a number.

![[notes/images/circfill.gif]]


### Let's move things around!

There is another special function `_init` that is executes once at the start.

Let's define a variable `x` there and then make `x` bigger every time in draw to move the circle.

```lua
function _init()
	x = 10
end

function _draw()
  -- clear screen
  cls()

  -- make x bigger
  x = x + 2

  -- circfill( x, y, radius, color )
  circfill(x, 64, 10, 8)
end
```

We can use an `if` statment to teleport the circle back to start of the screen

```lua
function _init()
	x = 10
end

function _draw()
  -- clear screen
  cls()

  -- make x bigger
  x = x + 2

  -- circfill( x, y, radius, color )
  circfill(x, 64, 10, 8)

  if x > 147 then
    x = -20
  end
end
```

### Exercise: Make the ball go diagonally

Make sure it loops!

![[notes/images/diagonal.gif]]

### Exercise: Draw a scene

Draw a moving picture using circles, rectangles, lines and/or text.

You can refer to the [[notes/Misc/Cheatsheet]] to find code for shapes.

For example a flower, face, house, abstract art~

### Appendix

*Some material in this tutorial is taken from [# Intro to Pico-8 Programming](https://demoman.net/?a=intro-to-lua)*