---
layout: media_memory
title: HTML5 Canvas Memory Game
categories: portfolio
image:
  teaser: memory/memory-teaser-400x400.png
---

This is a little memory tiles game that is programmed in CoffeeScript and uses the HTML5 canvas API for simple 2D rendering and animations. It was originally made in a hackathon designed to interact with an Arduino robot - if you won the game, the robot would do a little dance. Unfortunately I do not have a video of the dancing robot. The code is up on my [GitHub](https://github.com/j-v/edubots-memory).

The object of the game is to flip over matching pairs of tiles until all the tiles are flipped over. 

<div id="canvasDiv" class="float-left">
    <canvas id="myCanvas" width="870" height="700"></canvas>
</div>