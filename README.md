<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anas Erami - Creative Software Developer</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Inter Font from Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        /* Custom CSS for Matrix effect and stronger neon glow */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #000; /* Ensure black background for matrix effect */
            overflow-x: hidden; /* Prevent horizontal scroll */
        }

        /* Matrix Canvas Styling */
        #matrixCanvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            z-index: -1; /* Place behind content */
            background-color: #000; /* Fallback */
        }

        /* Neon Text Glow Effect */
        .neon-text {
            text-shadow:
                0 0 7px #00ffe0, /* Lighter glow */
                0 0 10px #00ffe0,
                0 0 21px #00ffe0,
                0 0 42px #00ffe0, /* Stronger glow */
                0 0 82px #00ffe0,
                0 0 92px #00ffe0,
                0 0 102px #00ffe0,
                0 0 151px #00ffe0;
            color: #fff; /* Base color for text */
        }

        /* Neon Link Hover Effect */
        .neon-link:hover {
            color: #ff00ff; /* Magenta on hover */
            text-shadow:
                0 0 7px #ff00ff,
                0 0 10px #ff00ff,
                0 0 21px #ff00ff,
                0 0 42px #ff00ff,
                0 0 82px #ff00ff,
                0 0 92px #ff00ff,
                0 0 102px #ff00ff,
                0 0 151px #ff00ff;
        }

        /* Container for content to give it depth above the matrix */
        .content-container {
            position: relative;
            z-index: 1; /* Ensure content is above canvas */
            background-color: rgba(0, 0, 0, 0.6); /* Slightly transparent dark background for readability */
            backdrop-filter: blur(3px); /* Subtle blur for depth */
            border-radius: 1.5rem; /* Rounded corners for the main container */
            border: 2px solid rgba(0, 255, 224, 0.3); /* Subtle neon border */
            box-shadow: 0 0 30px rgba(0, 255, 224, 0.4), 0 0 60px rgba(255, 0, 255, 0.3); /* Dual color glow */
        }

        /* Specific styling for the header image to give it a glow */
        .header-image-glow {
            box-shadow:
                0 0 10px #00ffe0,
                0 0 20px #00ffe0,
                0 0 30px #00ffe0,
                0 0 40px #00ffe0;
            border-radius: 1.5rem; /* Match container */
        }

        /* Style for skill icons to give a subtle glow */
        .skill-icon-glow img {
            transition: transform 0.3s ease-in-out, filter 0.3s ease-in-out;
        }
        .skill-icon-glow img:hover {
            transform: scale(1.1);
            filter: drop-shadow(0 0 8px #00ffe0) drop-shadow(0 0 15px #ff00ff);
        }

        /* Responsive adjustments for smaller screens */
        @media (max-width: 768px) {
            .content-container {
                padding: 1rem;
                margin: 1rem;
            }
            .neon-text {
                font-size: 1.5rem; /* Adjust font size for smaller screens */
            }
        }
    </style>
</head>
<body class="text-white">
    <!-- Matrix Canvas -->
    <canvas id="matrixCanvas"></canvas>

    <!-- Main Content Container -->
    <div class="content-container max-w-4xl mx-auto my-8 p-6 md:p-10">

        <!-- Animated Header Logo -->
        <div class="flex justify-center mb-8">
            <img src="https://raw.githubusercontent.com/Anas-2003/Anas-2003/main/assets/logo-animated.gif" width="150" alt="Anas Erami Logo" class="rounded-full header-image-glow">
        </div>

        <!-- Header with Waving Effect -->
        <div class="text-center mb-8">
            <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00ffe0,100:ff00ff&height=300&section=header&text=Anas%20Erami%20🚀&fontSize=60&animation=fadeIn&fontColor=ffffff" alt="Header" class="w-full rounded-xl header-image-glow">
        </div>

        <!-- Typing SVG -->
        <div class="text-center mb-12">
            <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=30&duration=4000&pause=1000&color=00FFE0&center=true&vCenter=true&width=600&lines=Hi+I’m+Anas+Erami.;Creative+Software+Developer.;Coding+is+my+art.;Let’s+build+something+amazing!" alt="Typing SVG" class="w-full max-w-xl mx-auto">
        </div>

        <hr class="border-t-2 border-purple-500 my-8">

        <!-- About Me Section -->
        <h2 class="text-3xl font-bold mb-4 text-center neon-text">👨‍💻 About Me</h2>
        <p class="text-lg leading-relaxed mb-4 text-center neon-text">
            ✨ Passionate software developer with a love for <strong class="text-purple-400">clean code, creative solutions, and modern technologies</strong>.
        </p>
        <p class="text-lg leading-relaxed mb-4 text-center neon-text">
            ⚡ I believe <strong class="text-green-400">great software isn’t just functional—it’s inspiring.</strong>
        </p>
        <p class="text-lg leading-relaxed mb-8 text-center neon-text">
            💡 Always exploring new tools, frameworks, and trends to stay ahead.
        </p>

        <hr class="border-t-2 border-green-500 my-8">

        <!-- Tech Stack Section -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">🚀 Tech Stack</h2>
        <div class="flex justify-center mb-8 skill-icon-glow">
            <img src="https://skillicons.dev/icons?i=html,css,js,react,tailwind,nodejs,python,django,flask,flutter,dart,mongodb,mysql,postgresql,git,linux,docker" alt="Tech Stack Icons" class="w-full max-w-3xl">
        </div>

        <hr class="border-t-2 border-blue-500 my-8">

        <!-- What Makes Me Unique Section -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">🌟 What Makes Me Unique</h2>
        <ul class="list-disc list-inside text-lg leading-relaxed mb-8 space-y-2 text-center">
            <li class="neon-text">🎨 <strong class="text-pink-400">Creative problem-solver</strong> with a passion for building elegant solutions</li>
            <li class="neon-text">⚡ <strong class="text-yellow-400">Fast learner</strong> and always curious about emerging technologies</li>
            <li class="neon-text">🤝 Advocate for <strong class="text-cyan-400">open-source collaboration</strong> and sharing knowledge</li>
        </ul>

        <hr class="border-t-2 border-orange-500 my-8">

        <!-- GitHub Stats Section -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">📊 GitHub Stats</h2>
        <div class="flex flex-col items-center space-y-6 mb-8">
            <img src="https://github-readme-stats.vercel.app/api?username=anas-2003&show_icons=true&theme=radical&hide_border=true&count_private=true" alt="GitHub Stats" class="w-full max-w-md rounded-lg header-image-glow">
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=anas-2003&theme=radical&hide_border=true" alt="GitHub Streak" class="w-full max-w-md rounded-lg header-image-glow">
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=anas-2003&layout=compact&theme=radical&hide_border=true" alt="Top Languages" class="w-full max-w-md rounded-lg header-image-glow">
        </div>

        <hr class="border-t-2 border-red-500 my-8">

        <!-- Contribution Graph Animation -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">🐍 Contribution Graph Animation</h2>
        <div class="flex justify-center mb-8">
            <img src="https://raw.githubusercontent.com/Anas-2003/Anas-2003/output/github-contribution-grid-snake.svg" alt="Snake animation" class="w-full max-w-2xl rounded-lg header-image-glow">
        </div>

        <hr class="border-t-2 border-indigo-500 my-8">

        <!-- Connect With Me Section -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">🌐 Connect With Me</h2>
        <div class="flex justify-center space-x-4 mb-12">
            <a href="mailto:anaserami17@gmail.com" class="neon-link">
                <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Badge"/>
            </a>
            <a href="https://github.com/anas-2003" class="neon-link">
                <img src="https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge"/>
            </a>
        </div>

        <hr class="border-t-2 border-teal-500 my-8">

        <!-- Footer Motto -->
        <h3 class="text-2xl font-bold text-center neon-text" style="color:#00ffe0;">
            ❤️ Creativity • 💥 Passion • 🚀 Continuous Learning ❤️
        </h3>

        <!-- Footer Waving Effect -->
        <div class="text-center mt-8">
            <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00ffe0,100:ff00ff&height=200&section=footer" alt="Footer" class="w-full rounded-xl header-image-glow">
        </div>
    </div>

    <!-- JavaScript for Matrix Effect -->
    <script>
        window.onload = function() {
            const canvas = document.getElementById('matrixCanvas');
            const ctx = canvas.getContext('2d');

            // Set canvas dimensions
            let W = canvas.width = window.innerWidth;
            let H = canvas.height = window.innerHeight;

            // Handle window resize
            window.addEventListener('resize', () => {
                W = canvas.width = window.innerWidth;
                H = canvas.height = window.innerHeight;
                columns = Array(Math.floor(W / fontSize)).fill(0); // Recalculate columns
            });

            // Matrix characters (Japanese Katakana, numbers, symbols)
            const matrixChars = "日ﾊﾐﾋｰｳｼﾅﾓﾆｻﾜﾂｵﾘｱﾎﾃﾏｹﾒｴｶｷﾑﾕﾗｾﾈｽﾀﾇﾍｦｲｸｺｿﾁﾄﾉﾌﾔﾖﾙﾚﾛﾝ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ";
            const fontSize = 20; // Size of each character
            let columns = Array(Math.floor(W / fontSize)).fill(0); // Array to store Y position for each column

            // Drawing the characters
            function drawMatrix() {
                // Draw a semi-transparent black rectangle over the entire canvas
                // This creates the fading trail effect
                ctx.fillStyle = 'rgba(0, 0, 0, 0.05)';
                ctx.fillRect(0, 0, W, H);

                // Set color for the characters (neon green)
                ctx.fillStyle = '#00ffe0';
                ctx.font = `${fontSize}px monospace`; // Monospace font for consistent character width

                // Loop over each column
                for (let i = 0; i < columns.length; i++) {
                    // Get a random character from the matrixChars string
                    const text = matrixChars.charAt(Math.floor(Math.random() * matrixChars.length));
                    const x = i * fontSize; // X position for the column
                    let y = columns[i] * fontSize; // Y position for the character in this column

                    // Add a subtle glow to the characters
                    ctx.shadowBlur = 10;
                    ctx.shadowColor = '#00ffe0';

                    // Draw the character
                    ctx.fillText(text, x, y);

                    // Reset shadow for next draw to avoid cumulative effect on background
                    ctx.shadowBlur = 0;

                    // If the character has reached the bottom of the screen
                    // or a random condition is met (to create gaps/new streams)
                    if (y > H && Math.random() > 0.975) {
                        columns[i] = 0; // Reset to the top
                    } else {
                        columns[i]++; // Move character down
                    }
                }
                requestAnimationFrame(drawMatrix); // Loop the animation
            }

            // Start the animation on window load.
            drawMatrix();
        };
    </script>
</body>
</html>

