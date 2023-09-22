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

<script>
    window.addEventListener('load', function () {
        const canvas = document.getElementById('spriteContainer');  // sets the canvas as a variable by calling the canvas element from the HTML code, using the id we set
        const ctx = canvas.getContext('2d'); // the getContext function is a given function within the canvas object. It allows us more functionality with the sprite image.

        // constant variables used for sprite and canvas
        const SPRITE_WIDTH = 160;
        const SPRITE_HEIGHT = 144;
        const SCALE_FACTOR = 2;
        const FRAME_LIMIT = 48;
        const FRAME_RATE = 15;

        // sets canvas properties
        canvas.width = SPRITE_WIDTH * SCALE_FACTOR;
        canvas.height = SPRITE_HEIGHT * SCALE_FACTOR;

        //more code will be placed here later
    });

</script>
