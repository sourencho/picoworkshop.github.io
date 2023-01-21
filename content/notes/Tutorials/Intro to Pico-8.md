---
title: "Intro to Pico-8"
---

## Intro

We will be making visuals in Pico-8 which is a fantasy console for making, sharing and playing tiny games and other computer programs.

Pico-8 has some limitations like a console would have:
- 128x128 pixel display
- 16 colours
- Lua coding

Pico-8 can be run in your browser for free at [pico-8.edu.com](https://www.pico-8-edu.com/)!

![[notes/images/pico8_edu_release.gif]]

## Examples

People make cool visuals and games!

- Homepage: [www.lexaloffle.com/pico-8.php](https://www.lexaloffle.com/pico-8.php)
- Demos: `INSTALL_DEMOS`
- BBS: [Lines](https://www.lexaloffle.com/bbs/?pid=64653#p)
- Celeste:  `LOAD #15133`


## Demo

I'll show you a quick visual made with math!

1. Draw a sprite
   
   ![[notes/images/editors.png]]
2. Write some code

```lua
function _draw()
	cls()
	for i=0,15 do
		x=64+cos(t()/4+i/16)*40
		y=64+sin(t()/6+i/16)*40
		spr(1,x,y)
	end

	s = "★ picoworkshop.xyz ★"
	print(s, 64-#s*2, 64, 14)

end
```
3. Save & Share
   
   `SAVE @URL`
   
   https://www.pico-8-edu.com/?c=AHB4YQCpAJtnv8L9Z7-C8S8Q7Z59_iOc-g5HXLG0lD-BM9hkom-zgdvuOeago7KNsu_Dh0jPOuuijXBiZaqYOSoMR5qJNjupW3HGSzgnLtecFTpfzTss5fHSSJHKCjxBOjQUDMVLS8VBT5QMTGxt7RUj79A_QxSetjLyFnXeT0yU_cLI4NLCUDw1dttd2d5xRhgty8FyciMQDwA=&g=w-w-QrQrw-wrHQHQLDLQLDLw-wsXg7Ew-wsXg7Ew-wrHQHQbObObw-wxrerw-wy7C
   
   or
   
   `CTR+7` & `SAVE DEMO.P8.PNG`
   
   ![[notes/images/demo.p8.png]]
