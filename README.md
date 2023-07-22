
<h1 align="center">Hello World</h1>


- 👋 Hi, I’m @roberth89
- 👀 I’m interested in programming...


<h2 align="center">Courses</h2>

<h3>Games Unity 2D</h3>

![image](https://media.giphy.com/media/SsqSVndYYzXI8xpa25/giphy.gif?cid=790b761111b05b196ae2e80c0cabb23bd7e3b36fbd1cb982&rid=giphy.gif&ct=g)


<!--

<p align="center">
  <img src="https://media.giphy.com/media/13HgwGsXF0aiGY/giphy.gif">
</p>
-->

<h3>TypeScript</h3>

https://user-images.githubusercontent.com/90001688/139599912-67562b40-f348-4ce5-9237-c6f4ed10ba34.mp4

<h3>Dart + Flutter</h3>

https://user-images.githubusercontent.com/90001688/142136787-ab7209a5-3210-47ea-bb48-fc79708ab539.mp4

<h3>Python</h3>

https://user-images.githubusercontent.com/90001688/224211346-58c0fbe9-9602-4f35-931b-7885cb0d6a9c.mp4

<canvas>
            
</canvas>


* {margin: 0; padding: 0}
body {background: #000;}
canvas {display: block;}

// Initialising the canvas
var canvas = document.querySelector('canvas'),
    ctx = canvas.getContext('2d');

// Setting the width and height of the canvas
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

// Setting up the letters
var letters = 'ABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZ';
letters = letters.split('');

// Setting up the columns
var fontSize = 10,
    columns = canvas.width / fontSize;

// Setting up the drops
var drops = [];
for (var i = 0; i < columns; i++) {
  drops[i] = 1;
}

// Setting up the draw function
function draw() {
  ctx.fillStyle = 'rgba(0, 0, 0, .1)';
  ctx.fillRect(0, 0, canvas.width, canvas.height);
  for (var i = 0; i < drops.length; i++) {
    var text = letters[Math.floor(Math.random() * letters.length)];
    ctx.fillStyle = '#0f0';
    ctx.fillText(text, i * fontSize, drops[i] * fontSize);
    drops[i]++;
    if (drops[i] * fontSize > canvas.height && Math.random() > .95) {
      drops[i] = 0;
    }
  }
}

// Loop the animation
setInterval(draw, 33);


