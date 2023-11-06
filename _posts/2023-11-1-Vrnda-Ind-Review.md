---
layout: post
toc: True
title: B. Vrnda's Individual Review
description: This is my guide to my individual review. Including my commits, code, experiments, and problems w/ their solutions to show my general progress.
type: tangibles
courses: { csse: {week: 12} } 
---

<!--
How I wanna structure it:

- Each file has:
    - link to commit + issue 
    - purpose of the file
    - what code I used (i.e. JS OOP -> to have two separate objects)
    - fails
    - solutions + what I learned 

- Conclusion:
    - what I developed over the tri
    - general learnings

-->

## Coding Contributions

[(All my commits)](https://github.com/kaylale124/final-game/commits?author=BVrndaKanhye)

### Week 1-2: Making Projectile

#### [Week 1 Issue](https://github.com/kaylale124/final-game/issues/1#issue-1933785897): 
    - Make egg projectile 

#### What I did:
    - Used a [space invaders tutorial](https://www.youtube.com/watch?v=MCVU0w73uKI) to make a mini version of space invaders with a chicken placeholder + circular projectile using OOP
        - I made a class Player and class Projectile to have two game objects appear on the screen

#### Code for reference:
    - *Unavailable because I deleted that file before being aware I should've saved it for reference*
    - Will explain in week 2 code

#### [Week 2 Issue](https://github.com/kaylale124/final-game/issues/1#issue-1933785897): 
    - egg-shaped projectile (try replacing w/ image)
    - egg integrate with chicken

#### What I did:
    - Managed to change the draw function from small circles -> our egg image
        - Altered OOP Programming

#### Code for reference:

````js
// class Player code

        class Projectile {
            constructor(canvas, ctx, x, y, speed, image) {
                this.canvas = canvas;
                this.ctx = ctx;
                this.x = x;
                this.y = y;
                this.speed = speed;
                this.image = image;
            }

            move() {
                this.y -= this.speed;
            }

            draw() {
                this.ctx.drawImage(this.image, this.x, this.y);
            }
        }

        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        let projectiles = [];

        const projectileImage = new Image();
        projectileImage.src = "{{site.baseurl}}/images/egg-projectile.png";

        const player = new Player(canvas, ctx);

    // addEventListenener code + drawing player and canvas

    // interesting ChatGPT way of having projectile continously spawn w/out woNKY
            for (let i = projectiles.length - 1; i >= 0; i--) {
                projectiles[i].move();
                projectiles[i].draw();

                if (projectiles[i].y < 0) {
                    projectiles.splice(i, 1);
                }
            }

            requestAnimationFrame(draw);

        draw();
````

#### Failures -> Reasons/Solutions
- I struggled to implement the background into this code ->  I didn't realize til later that I was using css in "display: block" which wouldn't allow an image to be loaded
- Egg wasn't showing up at first -> I had to define the image source and call it to load with the event listeners for w and space because draw and ctx.fillStyle were to describe drawing w/ color & shape
- Couldn't change the block to a chicken and integrate the two -> had to do something similar like the projectile where I called/used draw function to have image appear (Solved in W3)

### Week 3-4: Chicken and INTEGRATION

#### Week 3 Issue:
    - Change chicken placeholder to chicken image
    - Figure out how to customize chicken in game (?)

#### What I did:
    - Used help from ChatGPT on how to change the block into the chicken image

#### Code for reference:
    - *Unavailable because I deleted that file before being aware I should've saved it for reference*
    - Will explain in week 2 code

#### Failures -> Reasons/Solutions

#### [Week 1 Issue](https://github.com/kaylale124/final-game/issues/1#issue-1933785897): 
    - Make egg projectile 

#### What I did:
    - Used a [space invaders tutorial](https://www.youtube.com/watch?v=MCVU0w73uKI) to make a mini version of space invaders with a chicken placeholder + circular projectile using OOP
        - I made a class Player and class Projectile to have two game objects appear on the screen

#### Code for reference:
    - *Unavailable because I deleted that file before being aware I should've saved it for reference*
    - Will explain in week 2 code

#### Failures -> Reasons/Solutions


<!--
````js
code here
````
-->