# Introduction to Graphics

An overview of graphics using the [C++ Utils](https://github.com/ILXL/cpputils) ``graphics`` classes.

*You can follow this README directly from a terminal, or try it as a lab on [CS50](https://lab.cs50.io/ILXL-guides/intro-to-graphics/). If you do it directly, you can ignore text in brackets like {% this %}.*

## Setup

First, get the graphics::Image library:

```
git clone https://github.com/ILXL/cpputils.git
```

We can now ``#include "cpputils/graphics/image.h"`` to use the classes graphics::Image and graphics::Color.

{% next %}

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


Try making more colors with [Google's HTML color picker](https://www.google.com/search?q=color+picker).

*Aside: Unlike mixing paint, where combining red, green and blue would make dark brown, mixing red, green and blue light creates White light. Why? Consider: white light from the sun goes through a prism to create all the colors of the rainbow. Re-combining those colored lights can produce white again! However, because computers only have three pixel colors it is physically impossible for monitors to reproduce every color your eye can see!*

### Image coordinates

Images are made from a grid of pixels. We can reference individual pixels by their coordinates within the grid: their X location and their Y location.

Unlike the Cartesian coordinate system used in math classes, an image coordinate system begins in the top left corner at (0, 0), and then X increases to the right, while Y increases going down.

![8th grade vs pixel coordinate system](https://processing.org/tutorials/drawing/imgs/drawing-03.svg)
*https://processing.org/tutorials/drawing/imgs/drawing-03.svg*

In the image above, the top left pixel is (0, 0) while the bottom right pixel is (6, 6).

## graphics::Image class

You can get the ``graphics::Image`` class for drawing and displaying images when you ``#include "cpputils/graphics/image.h"``.

To create a new image which is 100x100 pixels::

```cpp
const int size = 100;
graphics::Image image;
image.Initialize(size, size);
```

This creates a new, all-white image size 100 by 100 pixels.

Your turn: Open ``main.cc`` and create an image that's 200x200 pixels. Make sure you've initialized cpputils using the ``git subtree`` command from the [Setup](#setup) step (check: when you type ``ls`` you should see that cpputils exists).

{% next %}

### Drawing shapes

You can draw circles, rectangles and lines on a graphics::Image. Here is the function prototype to draw a circle:

```cpp
/**
 * Draws a circle centered at (x, y) with radius |radius|, and color
 * specified by |red|, |green| and |blue| channels. Returns false if
 * params are out of bounds.
 */
bool DrawCircle(int x, int y, int radius, int red, int green, int blue);
```

```cpp
/**
 * Draws a line from (x0, y0) to (x1, y1) with color specified  by |red|, |green| and
 * |blue| channels, and optional width |thickness|. Returns false if params are out of bounds.
 */
bool DrawLine(int x0, int y0, int x1, int y1, int red, int green, int blue, int thickness = 1);
```

### Interacting with pixels

## graphics::Color class

### Using graphics::Color with Images

## Listening to mouse events
