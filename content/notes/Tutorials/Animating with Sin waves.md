---
title: "Animating with Sin waves"
---

⭐️ In this tutorial we will learn how to use `sin` to create movement!

### Hello Sin Circle

The function `sin` is very useful because if you feed it time `t()`  it will grow and then shrink and then grow and then shrink forever.

So if we use for the size of a circle, the circle will grow and shrink. The value fluctuates from -1 to 1 to -1 to 1. If we want a bigger value we can multiply it to get a bigger range: `10*sin(t())` will go from -10 to 10 to -10 to 10.

Note that half the time we won't see the cirlce when the size is negative.

```lua
function _draw()
  -- clear screen
  cls()

  -- get time value
  time = t()



  -- size from sin
  size = 10*sin(time)

  -- circfill( x, y, radius, color )
  circfill(64, 64, size, 12)
end
```

![[notes/images/sin_2.gif]]

### Fast forward and Slow motion

The circle is moving too fast!!

We can slow and speed up time by dividing or multiplying it.

So let's change code to be `time = t() / 2`

```lua
function _draw()
  -- clear screen
  cls()

  -- get time value
  -- divide time by 2 to slow it down
  time = t() / 2

  -- size from sin
  size = 10*sin(time)

  -- circfill( x, y, radius, color )
  circfill(64, 64, size, 12)
end
```

![[notes/images/sin_1.gif]]

### Shifting the range

What if we want our circle to start from a positive size, let's say go from 10 to 30?

If we add 1 to sin, instead of -1 to 1 we will get 0 to 2 because `-1 + 1 = 0` and `1 + 1 = 2` 

So let's change our code to be:

 `s = sin(time)+1`

If we divide this by 2 we will get a nice 0 to 1 range:

`s = (sin(time)+1)/2`

Now that we have 0 to 1 we can easily get the range 10 to 30.

Let's make the size go from 0 to 20 by multiplying `s` by 20:

 `size = s*20`.

And then add 10 to make it from from 10 to 30:

`size = 10 + s*20`

```lua
function _draw()
  -- clear screen
  cls()

  -- get time value
  -- divide time by 2 to slow it down
  time = t() / 2

  -- change sin range to 0-1
  s = (sin(time)+1)/2

  -- size from sin shifted to 10-30
  size = 10 + 20*s

  -- circfill( x, y, radius, color )
  circfill(64, 64, size, 12)
end
```

![[notes/images/sin_0.gif]]

### Exercise

Can you mofiy the code to make the circle change color over time. From red to pink?

![[notes/images/sin_5.gif]]

### Spinning with sin and cos!

Something cool about sin and it's sibling cos is that it can create circular motion!

If you set the x position of a circle to `cos` and the y pos to `sin` you will see it spin in a circle
  
  `x = center + radius * cos(time)`
  `y = center + radius * sin(time)`

```lua
function _draw()
  -- clear screen
  cls()

  -- get time value
  -- divide time by 2 to slow it down
  time = t() / 4

  -- change sin range to 0-1
  s = (sin(time)+1)/2

  -- size and color sin
  size = 8
  c = 12
  
  -- rotate
  center = 64
  r = 40
  
  x = center + r*cos(time)
  y = center + r*sin(time)

  -- draw path
  circ(center,center,r,1)

  -- draw circle
  circfill(x, y, size, c)
  
end
```

![[notes/images/sin_6.gif]]


### Exercise

Can you make a solar system or another cool animation using sin and cos?

![[notes/images/sin_8.gif]]

### Next

⭐️ [[notes/Tutorials/Dithering Effect]]