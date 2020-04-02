---
date: 2020-04-02 13:53:21 +0200
author: Jimmyrooster
title: How to create gravity in Scratch
image: images/luis-cortes-martinez-G5WQNBpMrmI-unsplash.jpg

---
_Big thanks to_ [_Jimmyrooster_]() _for writing this article._

## Explanation

To create gravity in scratch we first need to understand how gravity acts in the real world. If you have an apple and you drop from high up what happens? Well the speed (or velocity) of the apple increases towards objects exerting gravity - in proportion to mass - until it reaches terminal velocity or hits something.

Let’s start by simplifying this a bit. Most gravity will come from the earth - so we will ignore other objects. The earth will always be at the bottom of the screen. There will also be no terminal velocity.

## Basic Physics in Scratch

Create a sprite for the object you want to fall (or use one you already have).

First, we will need to create a variable for the current velocity of the sprite.
<pre class="ScratchBlocks">
(Y Velocity)
</pre>

We want the y position of the sprite to change by its y velocity every frame. We can do that with this simple loop. You probably want to attach a when green flag clicked block on top of this.
<pre class="ScratchBlocks">
forever
  change y by (Y Velocity)
end
</pre>

That’s great but it doesn’t do anything. This is because Y Velocity stays at zero. To make gravity we need to add a change Y Velocity by block and put a negative number in (so the sprite goes down the screen). Put this in the forever loop.
<pre class="ScratchBlocks">
change [Y Velocity v] by (-3)
</pre>

Things also slow down due to air resistance. For this I just set Y Velocity to 80% (multiplied by 0.8) of what it was. You can change that if you want. We will add this code into the forever loop.
<pre class="ScratchBlocks">
set [Y Velocity v] to ((Y Velocity) * (-8))
</pre>

And finally, there is collision. Create another sprite or colour for the object to collide with.
Let’s say when the thing collides it stops. You want an if else block with a condition for hitting something in the slot at the top; a set Y Velocity to 0 block in the first gap and the gravity code in the else. It falls if it is not colliding otherwise it stops. To make it bounce, you would set the y velocity to Y velocity multiplied by a negative number e.g. -0.9.
Attach this into the forever loop; deleting the previous gravity code.
<pre class="ScratchBlocks">
if <touching color [#b7ff03] ?> then
  set (Y Velocity) to (0)
else
  change (Y Velocity) by (-3)
</pre>

## The final code
You can see the final code <a href="https://scratch.mit.edu/projects/382036051/">here</a>. Feel free to remix it or backpack it for use (but give credit).