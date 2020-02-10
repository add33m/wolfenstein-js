# wolfenstein-js

A fun little ray casting game in the style of Wolfenstein 3D by Id Software. Made using [Koda.nu](https://koda.nu/)'s simple.js-library.

Feel free to steal the code, modify it or just play around and learn about how it works!
Please note that this is an older project of mine, and it probably has some lazy, badly written code hidden amongst it.

## How to play

1. Open `main.html` in your browser of choice.
2. Use WASD to move around, left and right arrows to look to the sides and the up/down arrows to change the FOV.
3. Have fun!

## How it works

The basis of this little game is something called "ray casting". Ray casting works by essentially sending out a virtual laser beam and using math to try and figure out where it lands.
When you know where the laser ends up, you can use that information to calculate the height of the closest wall for that column of the screen.
What this means is that for every horizontal "pixel" you draw a thin strip, where the height is equal to a constant divided by the distance to the point where the laser hits perpendicular to the player's view. While this may sound horribly complicated, it just comes down to calculating how far away the walls are in a certain bit of the screen, and then drawing the wall taller as the wall gets closer. Pretty fun and simple!

You can open up `raycaster.html` to get a closer look at how the raycasting part of the game works. It will let you control a single ray and see where it intersects the grid, as well as where it hits the wall. This is what I used to initially get the rays tracing properly.

## Credit

[This great video](https://www.youtube.com/watch?v=eOCQfxRQ2pY) by [Matt Godbolt](https://www.youtube.com/channel/UCC3kVzi4cWpLl16KmzsEtiQ) on YouTube is what inspired me to make this project. You should totally check it out and learn a thing or two about maths and trigonometry!

Textures for this game were taken from [areyep.com](http://www.areyep.com/RIPandMCS-TextureLibrary.html). They talk about the process of creating them and make some really cool stuff. Check them out!