<!-- FULL SNOWFALL ANIMATION FOR GITHUB PROFILE -->
<div id="snow-container" style="position: fixed; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 9999;">
  <canvas id="snow-canvas" style="display: block; width: 100%; height: 100%;"></canvas>
</div>

<script>
  // Snowfall Animation - Full Screen Effect
  (function() {
    const canvas = document.createElement('canvas');
    canvas.id = 'snowfall-canvas';
    canvas.style.position = 'fixed';
    canvas.style.top = '0';
    canvas.style.left = '0';
    canvas.style.width = '100%';
    canvas.style.height = '100%';
    canvas.style.pointerEvents = 'none';
    canvas.style.zIndex = '9999';
    document.body.appendChild(canvas);
    
    const ctx = canvas.getContext('2d');
    let width, height;
    let snowflakes = [];
    
    function init() {
      width = window.innerWidth;
      height = window.innerHeight;
      canvas.width = width;
      canvas.height = height;
      
      // Create snowflakes
      const flakeCount = 150;
      for (let i = 0; i < flakeCount; i++) {
        snowflakes.push({
          x: Math.random() * width,
          y: Math.random() * height,
          radius: Math.random() * 4 + 1,
          speed: Math.random() * 3 + 1,
          opacity: Math.random() * 0.7 + 0.3,
          sway: Math.random() * 2 - 1
        });
      }
    }
    
    function draw() {
      ctx.clearRect(0, 0, width, height);
      
      snowflakes.forEach(flake => {
        ctx.beginPath();
        ctx.arc(flake.x, flake.y, flake.radius, 0, Math.PI * 2);
        ctx.fillStyle = `rgba(255, 255, 255, ${flake.opacity})`;
        ctx.fill();
        
        // Move snowflake
        flake.y += flake.speed;
        flake.x += Math.sin(flake.y * 0.01) * 0.5 + flake.sway * 0.2;
        
        // Reset if out of bounds
        if (flake.y > height) {
          flake.y = -10;
          flake.x = Math.random() * width;
        }
        
        // Wrap around sides
        if (flake.x > width) flake.x = 0;
        if (flake.x < 0) flake.x = width;
      });
      
      requestAnimationFrame(draw);
    }
    
    window.addEventListener('resize', () => {
      width = window.innerWidth;
      height = window.innerHeight;
      canvas.width = width;
      canvas.height = height;
    });
    
    init();
    draw();
  })();
</script>

<!-- Add some style to make snow visible on light/dark modes -->
<style>
  #snowfall-canvas {
    filter: drop-shadow(0 0 10px rgba(255, 255, 255, 0.8));
  }
  
  /* For dark theme users */
  @media (prefers-color-scheme: dark) {
    #snowfall-canvas {
      filter: drop-shadow(0 0 10px rgba(200, 220, 255, 0.9));
    }
  }
</style>

<!-- Main typing animation - Hi I am a Flutter Developer -->

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=32&duration=2500&pause=449&color=6C63FF&center=true&vCenter=true&width=800&lines=Hi+%F0%9F%91%8B;I'm+Fawzia;%F0%9F%9A%80+Flutter+Developer;%F0%9F%A4%96+Multiple+App+Builder;%F0%9F%93%B1+AI+Tools+Builder;%E2%9A%A1+All+in+One+Ecosystem" alt="Typing Animation" />
</p>

<!-- Professional animated badge instead of GIF -->
<p align="center">
  <img src="https://komarev.com/ghpvc/?username=fawzia12&label=PROFILE+VIEWS&color=00FF9D&style=flat-square" alt="Profile views" />
  <img src="https://img.shields.io/github/followers/fawzia12?label=FOLLOWERS&color=00FF9D&style=flat-square&logo=github" alt="Followers" />
</p>

<!-- Clean developer animation -->
<p align="center">
  <img src="https://user-images.githubusercontent.com/74038190/218265814-3084a4ba-809c-4135-afc0-8685d0aa634b.gif" width="280" />
</p>


<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin: 30px 0;">
  
  <!-- FLUTTER CARD - Main Framework -->
  <div style="background: linear-gradient(135deg, rgba(2, 101, 148, 0.2), rgba(2, 101, 148, 0.05)); backdrop-filter: blur(10px); border: 2px solid #026594; border-radius: 20px; padding: 25px; width: 320px; box-shadow: 0 0 30px #02659466; transform: scale(1); transition: 0.3s;">
    <div style="display: flex; align-items: center; gap: 10px; margin-bottom: 15px;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg" width="40" height="40" />
      <h3 style="color: #026594; margin: 0; font-size: 24px; text-shadow: 0 0 10px #026594;">FLUTTER</h3>
    </div>
    <div style="display: flex; flex-wrap: wrap; gap: 10px;">
      <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" />
      <img src="https://img.shields.io/badge/Widgets-6C63FF?style=for-the-badge&logo=flutter&logoColor=white" />
      <img src="https://img.shields.io/badge/Cupertino-000000?style=for-the-badge&logo=apple&logoColor=white" />
      <img src="https://img.shields.io/badge/Material%20Design-757575?style=for-the-badge&logo=material-design&logoColor=white" />
    </div>
    <p style="color: white; margin-top: 15px; font-size: 14px;">Cross-platform • Beautiful UI • Native Performance</p>
  </div>

  <!-- FIREBASE CARD - BaaS -->
  <div style="background: linear-gradient(135deg, rgba(255, 202, 40, 0.2), rgba(255, 202, 40, 0.05)); backdrop-filter: blur(10px); border: 2px solid #FFCA28; border-radius: 20px; padding: 25px; width: 320px; box-shadow: 0 0 30px #FFCA2866; transform: scale(1); transition: 0.3s;">
    <div style="display: flex; align-items: center; gap: 10px; margin-bottom: 15px;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg" width="40" height="40" />
      <h3 style="color: #FFCA28; margin: 0; font-size: 24px; text-shadow: 0 0 10px #FFCA28;">FIREBASE</h3>
    </div>
    <div style="display: flex; flex-wrap: wrap; gap: 10px;">
      <img src="https://img.shields.io/badge/Auth-FF6B6B?style=for-the-badge&logo=firebase&logoColor=white" />
      <img src="https://img.shields.io/badge/Firestore-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" />
      <img src="https://img.shields.io/badge/Storage-00C851?style=for-the-badge&logo=firebase&logoColor=white" />
      <img src="https://img.shields.io/badge/Cloud%20Functions-F24E1E?style=for-the-badge&logo=firebase&logoColor=white" />
    </div>
    <p style="color: white; margin-top: 15px; font-size: 14px;">Real-time DB • Authentication • Serverless</p>
  </div>

  <!-- SUPABASE CARD - Open Source Alternative -->
  <div style="background: linear-gradient(135deg, rgba(62, 207, 142, 0.2), rgba(62, 207, 142, 0.05)); backdrop-filter: blur(10px); border: 2px solid #3ECF8E; border-radius: 20px; padding: 25px; width: 320px; box-shadow: 0 0 30px #3ECF8E66; transform: scale(1); transition: 0.3s;">
    <div style="display: flex; align-items: center; gap: 10px; margin-bottom: 15px;">
      <img src="https://www.vectorlogo.zone/logos/supabase/supabase-icon.svg" width="40" height="40" />
      <h3 style="color: #3ECF8E; margin: 0; font-size: 24px; text-shadow: 0 0 10px #3ECF8E;">SUPABASE</h3>
    </div>
    <div style="display: flex; flex-wrap: wrap; gap: 10px;">
      <img src="https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/Realtime-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" />
      <img src="https://img.shields.io/badge/Auth-6C63FF?style=for-the-badge&logo=supabase&logoColor=white" />
      <img src="https://img.shields.io/badge/Storage-FF6B6B?style=for-the-badge&logo=supabase&logoColor=white" />
    </div>
    <p style="color: white; margin-top: 15px; font-size: 14px;">PostgreSQL • Real-time • Open Source</p>
  </div>

  <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px; margin: 30px 0;">
    <div style="background: rgba(108, 99, 255, 0.1); backdrop-filter: blur(10px); border: 2px solid #6C63FF; border-radius: 15px; padding: 25px; width: 300px;">
      <h3 style="color: #47CCCC;">🚀 LANGUAGES</h3>
      <p>
        <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" />
        <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
        <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
        <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
      </p>
    </div>

## 🤝 LET'S CONNECT

  <!-- Cool Developer Card -->
  <div style="border: 2px solid #6C63FF; border-radius: 20px; padding: 20px; margin: 20px; background: linear-gradient(145deg, #0D0D0D, #1A1A1A); box-shadow: 0 0 30px #6C63FF66;">
    <table>
      <tr>
        <td width="200">
          <img src="https://i.imgur.com/6T1Qw8j.png" width="180" style="border-radius: 50%; border: 4px solid #6C63FF; box-shadow: 0 0 30px #6C63FF;">
        </td>
        <td>
          <h2 style="color: #6C63FF; margin: 0;">Fawzia Rahman</h2>
          <h3 style="color: #47CCCC; margin: 5px 0;">⚡ Mobile Application Developer</h3>
          <p style="color: white;">
            🚀 Building: <b style="color: #FF6B6B;">E-commerce App</b><br>
            📚 Learning: <b style="color: #FF6B6B;">Advanced Flutter</b><br>
            🤝 Looking: <b style="color: #FF6B6B;">Hackathon Team</b><br>
            📧 Contact: <b style="color: #FF6B6B;">fawziarahman280@gmail.com</b>
          </p>
        </td>
      </tr>
    </table>
  </div>


## 📊 GITHUB STATS

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=fawzia12&show_icons=true&theme=radical&hide_border=true&bg_color=0D1117&title_color=6C63FF&icon_color=6C63FF" width="100%">
  
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=fawzia12&theme=radical&hide_border=true&background=0D1117&stroke=6C63FF&ring=6C63FF&fire=6C63FF" width="100%">
  
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=fawzia12&layout=compact&theme=radical&hide_border=true&bg_color=0D1117&title_color=6C63FF" width="100%">
</div>

---

<div align="center">
  <i>Simple • Clean • Professional</i>
  <br>
  <b>Let's build something amazing together ✨</b>
</div>
