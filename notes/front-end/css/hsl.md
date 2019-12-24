[UP](./index.md)

# hsl()

Colors have several characteristics including hue, saturation, and lightness.

## hue
- what people generally think of as 'color'. 

If you picture a spectrum of colors starting with red on the left, moving through green in the middle, and blue on right, the hue is where a color fits along this line. In hsl(), hue uses a color wheel concept instead of the spectrum, where the angle of the color on the circle is given as a value between 0 and 360.

## saturation
- the amount of gray in a color.  

A fully saturated color has no gray in it, and a minimally saturated color is almost completely gray. This is given as a percentage with 100% being fully saturated.

## lightness 
the amount of white or black in a color.  

A percentage is given ranging from 0% (black) to 100% (white), where 50% is the normal color.

## tone
The hsl() option in CSS also makes it easy to adjust the tone of a color.  

### tinting
Mixing **white with a pure hue creates a tint** of that color

### shading
**adding black will make a shade**.  

### tone = tinting & shading
Alternatively, a tone is produced by adding gray or by both tinting and shading.  

Recall that the 's' and 'l' of hsl() stand for saturation and lightness, respectively.  
The saturation percent changes the amount of gray and the lightness percent determines how much white or black is in the color.  
This is useful when you have a base hue you like, but need different variations of it.