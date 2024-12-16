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
Thus is basically telling Kaboom "Hey! When **x** is pressed, make the sprite on screen move **x** direction!". and just like that, we have our moving sprite!


[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
