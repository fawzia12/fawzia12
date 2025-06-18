<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Fawzia's Portfolio</title>
  <style>
    /* Full screen snow background */
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      overflow: hidden;
      background: #000; /* dark background */
      color: white;
      font-family: Arial, sans-serif;
    }

    #snow {
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      pointer-events: none;
      z-index: 9999;
    }

    /* Centered container for your text */
    .content {
      position: relative;
      z-index: 10;
      text-align: center;
      padding: 100px 20px;
    }

    h1, h3 {
      margin: 0.2em 0;
    }
  </style>
</head>
<body>

  <canvas id="snow"></canvas>

  <div class="content">
    <h1>Hi 👋, I'm Fawzia</h1>
    <h3>A passionate frontend developer</h3>

    <p>🔭 I’m currently working on <strong>ecommerce App</strong></p>
    <p>🌱 I’m currently learning <strong>Flutter</strong></p>
    <p>👯 I’m looking to collaborate on <strong>Hackathon</strong></p>
    <p>📫 How to reach me: <strong>fawziarahman280@gmail.com</strong></p>
  </div>

  <script>
    // Simple snow animation on canvas
    const canvas = document.getElementById('snow');
    const ctx = canvas.getContext('2d');
    let width, height;
    let snowflakes = [];

    function init() {
      resize();
      createSnowflakes();
      animate();
    }

    function resize() {
      width = window.innerWidth;
      height = window.innerHeight;
      canvas.width = width;
      canvas.height = height;
    }

    window.addEventListener('resize', resize);

    function createSnowflakes() {
      const flakeCount = 150;
      snowflakes = [];
      for(let i=0; i<flakeCount; i++) {
        snowflakes.push({
          x: Math.random() * width,
          y: Math.random() * height,
          radius: Math.random() * 4 + 1,
          speed: Math.random() * 1 + 0.5,
          opacity: Math.random()
        });
      }
    }

    function animate() {
      ctx.clearRect(0, 0, width, height);
      ctx.fillStyle = 'white';
      ctx.beginPath();
      snowflakes.forEach(flake => {
        ctx.moveTo(flake.x, flake.y);
        ctx.arc(flake.x, flake.y, flake.radius, 0, Math.PI * 2);
      });
      ctx.fill();

      update();
      requestAnimationFrame(animate);
    }

    function update() {
      snowflakes.forEach(flake => {
        flake.y += flake.speed;
        if(flake.y > height) {
          flake.y = 0;
          flake.x = Math.random() * width;
        }
      });
    }

    init();
  </script>
</body>
</html>

