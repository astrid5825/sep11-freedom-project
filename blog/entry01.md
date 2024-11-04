# Entry 1
##### 11/4/2024

## Context
I am using ***Kaboom.Js***. And I will be writing about it, even though I am not using impact anymore, I wanted to keep this in. Because it might come in handy for people who are using Impact.

# Kaboom, what is it?

*Kaboom* is a program the helps to make games, usually these games are platformers, however! My game will be about the player (her name will be Azzy) trying to find her friend. So I decided to go with a top-down RPG style, which you can do with *Kaboom!*

the first thing I looked at is **the playground**. The playground really helpful, its like a template for code you might need. Like movement code, or code for sprites. as an example, here is the code needed for movement in Kaboom!

```
kaboom()

loadSprite("bean", "/sprites/bean.png")
```
^^^ Loads a sprite

```
const SPEED = 320
```
^^^ this first part tells us how fast a player is moving via "Pixels per second".
```
const player = add([
	sprite("bean"),
```
^^^ this actually makes the sprite we loaded before count as "the player"
```
	pos(center()),
])
```
^^^ tells us where the center is/ where we would start off

```
onKeyDown("left", () => {
	player.move(-SPEED, 0)
})

onKeyDown("right", () => {
	player.move(SPEED, 0)
})

onKeyDown("up", () => {
	player.move(0, -SPEED)
})

onKeyDown("down", () => {
	player.move(0, SPEED)
})
```
^^^ ``.onKeyDown()`` tells us what keys would need to be pressed for something to happen, as well as where the sprite would move. While ``player.move()`` tells us how much the sprite would move if that ket was clicked.

All of this was found in the playground alone, as well as other code snippids. The next blog entry will be about me putting Kaboom into my IDE, since I did it wrong the first time. As well as sprite making in general.

# 10/20/2024, impact notes (this is extra)

## Impact.Js (from what I understood)

Impact.Js is used to mainly make platforming games, however I want to see if I am able to make a game with gameplay mechanics similar to a platformer, but with a slightly different twist. Orignally, a issue I had was getting Impact to run. I wasn't sure what I was even supposed to do. Thanks to Slack and youtube, I now how to open it... oof XP.

## IMPACT
*Impact actually has it's own way of loading other Javascript sourcefiles into an Object, you'd need something called a "define Block". Shown below:
```
ig.module(
 'game.my-file'
)
.requires (
'impact.game'
'impact.image'
'game.other-files'
)
.defines (function(){
//this is where somebody would put their code for a module, will be explained later
```
this would be used to describe a Modules, which help Load things correctly for your game. While the stuff above in "Requires" loads things, where you define is where you would actually start coding the game.
*Impact uses "Classes". Which is already in Javascript, The Classes in Impact is simple Usually, classes have a structure similar to this
```
var placeHolder = ig.placeHolder.extended({
name : '',
init: function (name) {
This.name=name;
}
});
```
What this does is create a new "person" (class), **(note ig = Impact)**. From this base, you can extend and build onto this. You can make as many as you want. **(Note, "name" is a property of the class, you need to use ``.name=name;`` )**

[Next](entry02.md)

[Home](../README.md)
