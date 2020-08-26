# Introduction to Graphics

An overview of graphics using the [C++ Utils](https://github.com/ILXL/cpputils) ``graphics`` classes.

## What is a pixel?

A pixel is a set of three tiny lights on a display: Red, Green and Blue.

![Macro photograph of text "RGB" in LCD display](https://upload.wikimedia.org/wikipedia/commons/7/70/LCD_RGB.jpg)
*https://commons.wikimedia.org/wiki/File:LCD_RGB.jpg*

Images are made from two-dimensional grids of pixels.

### Color

Pixels are so small that our eyes cannot make out the individual red, green and blue components. Instead, we merge the three colors together, creating an illusion of multi-colored light.

To specify a color, you can specify the brightness of the red, green and blue components of each pixel. Brightnesses may range between 0 and 255. (255 is 2^8 - 1).

By convention, we list red, then green, then blue.

Here are some examples:

<div style="padding: 6px; background-color: black; color: white">Red: 0, Green: 0, Blue: 0</div>
<div style="padding: 6px; background-color: white; color: black">Red: 255, Green: 255, Blue: 255</div>
<div style="padding: 6px; background-color:rgb(255,0,0); color: white">Red: 255, Green: 0, Blue: 0</div>
<div style="padding: 6px; background-color:rgb(0,255,0); color: black">Red: 0, Green: 255, Blue: 0</div>
<div style="padding: 6px; background-color:rgb(0,0,255); color: white">Red: 0, Green: 0, Blue: 255</div>
<div style="padding: 6px; background-color:rgb(255,191,0); color: black">Red: 255, Green: 191, Blue: 0</div>
<div style="padding: 6px; background-color:rgb(138,34,179); color: white">Red: 138, Green: 84, Blue: 179</div>

Try making more colors with [Google's HTML color picker](https://www.google.com/search?q=color+picker).

*Aside: Unlike mixing paint, where combining red, green and blue would make dark brown, mixing red, green and blue light creates White light. Why? Consider: white light from the sun goes through a prism to create all the colors of the rainbow. Re-combining those colored lights can produce white again! However, because computers only have three pixel colors it is physically impossible for monitors to reproduce every color your eye can see!*

### Pixel coordinates

## graphics::Image class

### Interacting with pixels

### Drawing shapes and text

## graphics::Color class

### Using graphics::Color with Images

## Listening to mouse events
