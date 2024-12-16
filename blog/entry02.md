# Entry 2
##### 12/14-16/24

# THE PROGRESS

After finally getting Kaboom in my IDE thanks to [(this video)](https://youtu.be/iHTv4drOw_0), my next step was a simple one. add A moveable player character. Which was a lot harder then I orignally thought. This is because I had to load the sprite before I started coding it.

```
loadSprite ("azHolder", "azzyPlaceholder.png")

const player = add([
   sprite("azHolder"),
   pos(636,height()- 295),
   scale(.1),
   area(),
])
```
Above me is the code to add our little Azzy into existence. This just kind of puts her on the map. Example,
![image](https://github.com/user-attachments/assets/5eb0e396-09f4-4415-9e30-ef220429b9b5)
``const SPEED`` is what we need to actually get her to move. Once we set a speed, we can then bind movement options to the arrow keys, like so:

```
onKeyDown("left", () => {
	player.move(-SPEED, 0)
})

onKeyDown("right", () => {
	player.move(SPEED, 0)
})
```
This is basically telling Kaboom "Hey! When **x** is pressed, make the sprite on screen move!". and just like that, we have our moving sprite! I've said this in the last entry, but now I can go more in depth, the ``const SPEED`` is what makes the sprite move, you can see in the code, SPEED sometimes has a little negitive sign. Well, this determines direction. That's how Kaboom knows to " Make the sprite on screen move **x** direction!" when a key is pressed.

## The works in progress

The goal of this game is to find a friend of Azzy. I tried to code them into the game too,
![image](https://github.com/user-attachments/assets/310a7db6-6578-4c0d-a74f-36af2ad81453)

However as of right now they do not show up because I coded them wrong. They need to be recgonized as an item, if I understand correctly. Since running into them would trigger a "You won!" screen. But, the fact both of them can pop up on the Screen means i've done what I've wanted too.

## The goal for next Blog

By next entry, I want to try and make a level. Not the mechanic where Azzy teleports, but for now just a starting level. I want to add dialouge too. This is to practice making the levels and decorating them, and will help in the long run. [(I found this youtube video I can watch on making Kaboom RPGs, this might help me with my goal!)](https://youtu.be/jcoiEpzD3yc?si=Qwba3LWOlF6S9toI).

## How FP is helping me

A LOT more functions then I expected are required. So when I code this game, I am practicing how to write Functions, and I feel like I am getting better and understanding them as I go on!

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
