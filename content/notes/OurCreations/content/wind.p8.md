
---
title: "wind.p8"
---

![[notes/OurCreations/gifs/sourencho_wind_0.gif]]

Credit
- sourencho
- February 2022

Link

https://www.pico-8-edu.com/?c=AHB4YQENAPkC4EeEyyukxiwGBiYwZnBmcUdRRMGtxwYGRkFHh1FHR2GMbQ4FJkUBrkfGRSZHJkfB7E0OJK0HhsUNhOxNIcGsB04lTSEhryemBSXtxU1FJkUhQa5nLk4O4BGWT9h-ifnCDi9x0NlP8Azl7UeUzzA09BRt_QCv4MXro7g-JYw3jjloIEuawjDp6TcddNVJgWbIVVelfd5aYcsqgZVWhq6fOX9mSGLgIZbyWElkMBsakQ8ZG3uJcqjspyZarZEJlYB4xhuFGsEzTIw8QTd02lCRlDtN1Ew0e3sbG_lEmJkjrqd2FicmHqIdyR5hdK246nEq&g=w-w-w-w1HQHw-w2Xw-w3Xw-w2HQH

Code

```lua
?"\^!5f100▒1⬇️3⬅️;⌂"
n=600
::😐::
cls(0)
p=2.2929
for i=0,n do
	f=p*i
	y=1-(i/n*2)
	r=sqrt(1-y*y)
	x=cos(f)*r
	z=sin(f)*r
	b=(x+z*1.3)+3.3
	b=b^5/700
	x=64+x*30
	y=64+y*30
	srand(i)
	u=4*sin(t()/3)+3
	v=5*abs(cos(rnd()+t()))
	line(x,y,x+u,y+v,1.5*(b+1))
end
flip()
goto 😐
```