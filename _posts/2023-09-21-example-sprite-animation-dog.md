---
toc: true
layout: post
title: Example Sprite Animation (Doggy)
description: An intro to sprite sheets for 2D game animation :0
type: hacks
courses: { csse: {week: 5} } 
---

<body>
    <div>
        <canvas id="spriteContainer"> <!-- Within the base div is a canvas. An HTML canvas is used only for graphics. It allows the user to access some basic functions related to the image created on the canvas (including animation) -->
            <img id="dogSprite" src="/bvk-csse-1/images/dogSprites.png">
        </canvas>
        <div id="controls"> <!--basic radio buttons which can be used to check whether each individual animaiton works -->
            <input type="radio" name="animation" id="idle" checked>
            <label for="idle">Idle</label><br>
            <input type="radio" name="animation" id="barking">
            <label for="barking">Barking</label><br>
            <input type="radio" name="animation" id="walking">
            <label for="walking">Walking</label><br>
        </div>
    </div>
</body>