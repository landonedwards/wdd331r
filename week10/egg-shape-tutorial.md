# Egg Shape Tutorial

First, you want to start by creating a div and giving it a class or ID so you can select it. Once you’ve selected your empty div, you should set its display to block so it gets its own line and is not crowded by other elements. 

We should add a background color to it, so we can see what is happening to the shape as we make changes. Then, we’ll want to set the width and height. Generally, for a vertical egg, the height should be 30 - 45% greater than the width. On the lower end, 30% gives us a rounder egg, while closer to 45% makes it taller and more slender. We’ll set our width at 120px and our height at 170px, which is about 42% greater than the width. 

Now, we should define a border-radius. A border radius accepts several different value formats, but the one we’ll be using includes a slash, which separates the horizontal rounding from the vertical rounding. The first section is horizontal and accepts 4 values in this order: top-left, top-right, bottom-right, bottom-left. The second section is vertical and accepts the same values. We want the horizontal ends to be symmetrical and curve to the center, so we’ll use 50% for all of them. Then, because we want the top half of the egg to be narrower than the lower half, we’ll use 60% for the top-left and top-right parameters. We can use 40% for the bottom-right and bottom-left parameters. 

## Completed Egg
https://codepen.io/landonedwards/pen/raMjayO