***
Just the other day, I had someone come up to me and say, "Oh you can solve Rubik's Cubes? Well, I heard you just use one algorithm every time, so it really isn't impressive."

So what did I do? I proved them right!
***
# 2x2-Devils-Algorithm

This repo contains a Devil's Algorithm for the 2x2 Rubik's Cube. What does it do? Well, let's say you have a 2x2 cube that you haven't solved in over 10 years. Frustrating right? Well, simply put the Yellow-Orange-Green corner in the back-bottom-left slot (with yellow on the bottom), and apply these moves! **BAM!** That's one more solved cube.

You heard that right. This algorithm will eventually solve *ANY* 2x2 cube, as long as the YOG corner is in the BBL slot with yellow on the bottom. No catches, no fine print. 

How does this algorithm work? Well, first I needed to find a way to visit every possible position on the 2x2 cube (there are 3674160). Well, here's my logic. What if I generated every possible 2x2 position, and just solved them all? 

And that's exactly what I did. Here's a simple overview of how this algorithm works

- Apply one of the 3674160 possible solutions to a 2x2 cube
- If this solved your cube, then great!
- If not, the next line will undo the attempted solution, putting the cube back to it's starting point
- Repeat until your cube is solved

The process is quite simple in theory, but obviously the hardest part is actually generating every 2x2 position and solving them all. Luckily, u/ben1996123 on Reddit was kind enough to generate all the scrambles for me, so all I had to do was write a program to solve any possible position of a Rubik's Cube (see `CubeBot2.0`), run the program on Ben's scrambles, and write the scrambles and solutions to a `.txt` file! Simple, isn't it?
