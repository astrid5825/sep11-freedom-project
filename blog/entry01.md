# Entry 1
##### 10/20/2024

# Intro to Impact.Js

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
