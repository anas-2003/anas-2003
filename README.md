<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>أنس إيرامي - مطور برمجيات إبداعي</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Inter Font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Inter', sans-serif;
      background-color: #000;
      margin: 0;
      overflow-x: hidden;
    }
    #matrixCanvas {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
    }
    .neon-text {
      text-shadow:
        0 0 10px #00ffe0,
        0 0 20px #00ffe0,
        0 0 30px #00ffe0,
        0 0 50px #00ffe0;
      color: #fff;
    }
    .neon-link:hover {
      color: #ff00ff;
      text-shadow:
        0 0 10px #ff00ff,
        0 0 20px #ff00ff,
        0 0 30px #ff00ff,
        0 0 50px #ff00ff;
    }
    .content-container {
      position: relative;
      z-index: 1;
      /* --- FIX 1: Increased contrast and blur for better visibility --- */
      background-color: rgba(10, 20, 30, 0.75); /* Was almost pure black */
      backdrop-filter: blur(8px); /* Was 4px */
      border-radius: 1.5rem;
      border: 2px solid rgba(0, 255, 224, 0.4);
      box-shadow: 0 0 30px rgba(0, 255, 224, 0.4),
                  0 0 60px rgba(255, 0, 255, 0.3);
      padding: 2rem;
      margin: 2rem auto;
      max-width: 900px;
    }
    .header-image-glow {
      box-shadow:
        0 0 15px #00ffe0,
        0 0 30px #00ffe0;
      border-radius: 1.5rem;
    }
    .skill-icon-glow img:hover {
      transform: scale(1.1);
      filter: drop-shadow(0 0 15px #00ffe0)
              drop-shadow(0 0 25px #ff00ff);
      transition: all 0.3s ease;
    }
  </style>
</head>
<body class="text-white">
  <!-- Matrix Canvas -->
  <canvas id="matrixCanvas"></canvas>

  <!-- Main Content -->
  <div class="content-container">
    <!-- Animated Logo -->
    <div class="flex justify-center mb-8">
      <img src="https://raw.githubusercontent.com/Anas-2003/Anas-2003/main/assets/logo-animated.gif" width="150" alt="Logo" class="rounded-full header-image-glow">
    </div>

    <!-- Waving Header -->
    <div class="text-center mb-8">
      <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00ffe0,100:ff00ff&height=250§ion=header&text=Anas%20Erami%20🚀&fontSize=50&animation=fadeIn&fontColor=ffffff" alt="Header" class="w-full rounded-xl header-image-glow">
    </div>

    <!-- Typing Text -->
    <div class="text-center mb-8">
      <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=28&duration=4000&pause=1000&color=00FFE0¢er=true&vCenter=true&width=600&lines=Hi+I'm+Anas+Erami.;Creative+Software+Developer;Coding+is+my+art.;Let's+build+something+amazing!" alt="Typing Animation" class="w-full max-w-xl mx-auto">
    </div>

    <hr class="border-t-2 border-purple-500 my-8">

    <!-- About Me -->
    <h2 class="text-3xl font-bold mb-4 text-center neon-text">👨‍💻 About Me</h2>
    <p class="text-lg text-center neon-text mb-4">
      ✨ Passionate software developer with a love for <strong class="text-purple-400">clean code, creative solutions, and modern technologies</strong>.
    </p>
    <p class="text-lg text-center neon-text mb-8">
      ⚡ I believe <strong class="text-green-400">great software isn’t just functional—it’s inspiring.</strong>
    </p>

    <hr class="border-t-2 border-green-500 my-8">

    <!-- Tech Stack -->
    <h2 class="text-3xl font-bold mb-6 text-center neon-text">🚀 Tech Stack</h2>
    <div class="flex justify-center mb-8 skill-icon-glow">
      <img src="https://skillicons.dev/icons?i=html,css,js,react,tailwind,nodejs,python,django,flask,flutter,dart,mongodb,mysql,postgresql,git,linux,docker" alt="Tech Icons" class="w-full max-w-3xl">
    </div>

    <hr class="border-t-2 border-blue-500 my-8">

    <!-- GitHub Stats -->
    <h2 class="text-3xl font-bold mb-6 text-center neon-text">📊 GitHub Stats</h2>
    <div class="flex flex-col items-center space-y-6 mb-8">
      <img src="https://github-readme-stats.vercel.app/api?username=anas-2003&show_icons=true&theme=radical&hide_border=true&count_private=true" alt="GitHub Stats" class="w-full max-w-md rounded-lg header-image-glow">
      <img src="https://streak-stats.demolab.com/?user=anas-2003&theme=radical&hide_border=true" alt="GitHub Streak" class="w-full max-w-md rounded-lg header-image-glow">
    </div>

    <hr class="border-t-2 border-red-500 my-8">

    <!-- Contribution Snake -->
    <h2 class="text-3xl font-bold mb-6 text-center neon-text">🐍 Contribution Snake</h2>
    <div class="flex justify-center mb-8">
      <img src="https://raw.githubusercontent.com/Anas-2003/Anas-2003/output/github-contribution-grid-snake.svg" alt="Contribution Snake" class="w-full max-w-2xl rounded-lg header-image-glow">
    </div>

    <hr class="border-t-2 border-indigo-500 my-8">

    <!-- Contact -->
    <h2 class="text-3xl font-bold mb-6 text-center neon-text">🌐 Contact Me</h2>
    <div class="flex justify-center space-x-4 mb-8">
      <a href="mailto:anaserami17@gmail.com" class="neon-link">
        <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Badge"/>
      </a>
      <a href="https://github.com/anas-2003" class="neon-link">
        <img src="https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge"/>
      </a>
    </div>

    <h3 class="text-2xl font-bold text-center neon-text">
      ❤️ Creativity • 💥 Passion • 🚀 Continuous Learning ❤️
    </h3>
  </div>

  <!-- Matrix Animation -->
  <script>
    const canvas = document.getElementById('matrixCanvas');
    const ctx = canvas.getContext('2d');

    // --- FIX 2: Encapsulated setup logic into a function for reuse ---
    let W, H, columns, drops;
    const fontSize = 16;
    const matrix = "日ﾊﾐﾋｰｳｼﾅﾓﾆｻﾜﾂｵﾘｱﾎﾃﾏｹﾒｴ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ";

    // Function to set up or reset the canvas and columns
    function setup() {
      W = window.innerWidth;
      H = window.innerHeight;
      canvas.width = W;
      canvas.height = H;
      columns = Math.floor(W / fontSize);
      drops = [];
      for(let i = 0; i < columns; i++) {
        drops[i] = 1;
      }
    }

    function draw() {
      ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
      ctx.fillRect(0, 0, W, H);
      ctx.fillStyle = "#00ffe0";
      ctx.font = `${fontSize}px monospace`;

      for(let i = 0; i < drops.length; i++) {
        const text = matrix[Math.floor(Math.random() * matrix.length)];
        ctx.fillText(text, i * fontSize, drops[i] * fontSize);
        if(drops[i] * fontSize > H && Math.random() > 0.975) {
          drops[i] = 0;
        }
        drops[i]++;
      }
    }

    // Initial setup
    setup();
    
    // Start the animation
    setInterval(draw, 33);

    // Reset canvas on window resize
    window.addEventListener('resize', setup);
  </script>
</body>
</html>