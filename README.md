<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أنس إيرامي - مطور برمجيات إبداعي</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Inter Font from Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        /* CSS مخصص لتأثير الماتريكس والتوهج النيون الأقوى */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #000; /* ضمان خلفية سوداء لتأثير الماتريكس */
            overflow-x: hidden; /* منع التمرير الأفقي */
        }

        /* تصميم لوحة الماتريكس */
        #matrixCanvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            z-index: -1; /* وضعها خلف المحتوى */
            background-color: #000; /* احتياطي */
        }

        /* تأثير توهج النص النيون */
        .neon-text {
            text-shadow:
                0 0 7px #00ffe0, /* توهج أخف */
                0 0 10px #00ffe0,
                0 0 21px #00ffe0,
                0 0 42px #00ffe0, /* توهج أقوى */
                0 0 82px #00ffe0,
                0 0 92px #00ffe0,
                0 0 102px #00ffe0,
                0 0 151px #00ffe0;
            color: #fff; /* اللون الأساسي للنص */
        }

        /* تأثير تحويم الروابط النيون */
        .neon-link:hover {
            color: #ff00ff; /* أرجواني عند التحويم */
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

        /* حاوية المحتوى لإعطائها عمقًا فوق الماتريكس */
        .content-container {
            position: relative;
            z-index: 1; /* ضمان أن المحتوى فوق اللوحة */
            background-color: rgba(0, 0, 0, 0.6); /* خلفية داكنة شفافة قليلاً لسهولة القراءة */
            backdrop-filter: blur(3px); /* تأثير ضبابي خفيف للعمق */
            border-radius: 1.5rem; /* حواف مستديرة للحاوية الرئيسية */
            border: 2px solid rgba(0, 255, 224, 0.3); /* حدود نيون خفيفة */
            box-shadow: 0 0 30px rgba(0, 255, 224, 0.4), 0 0 60px rgba(255, 0, 255, 0.3); /* توهج بلونين */
        }

        /* تصميم خاص لصورة الرأس لإعطائها توهجًا */
        .header-image-glow {
            box-shadow:
                0 0 10px #00ffe0,
                0 0 20px #00ffe0,
                0 0 30px #00ffe0,
                0 0 40px #00ffe0;
            border-radius: 1.5rem; /* مطابقة للحاوية */
        }

        /* تصميم أيقونات المهارات لإعطائها توهجًا خفيفًا */
        .skill-icon-glow img {
            transition: transform 0.3s ease-in-out, filter 0.3s ease-in-out;
        }
        .skill-icon-glow img:hover {
            transform: scale(1.1);
            filter: drop-shadow(0 0 8px #00ffe0) drop-shadow(0 0 15px #ff00ff);
        }

        /* تعديلات استجابة للشاشات الأصغر */
        @media (max-width: 768px) {
            .content-container {
                padding: 1rem;
                margin: 1rem;
            }
            .neon-text {
                font-size: 1.5rem; /* ضبط حجم الخط للشاشات الأصغر */
            }
        }
    </style>
</head>
<body class="text-white">
    <!-- لوحة الماتريكس -->
    <canvas id="matrixCanvas"></canvas>

    <!-- حاوية المحتوى الرئيسية -->
    <div class="content-container max-w-4xl mx-auto my-8 p-6 md:p-10">

        <!-- شعار الرأس المتحرك -->
        <div class="flex justify-center mb-8">
            <img src="https://raw.githubusercontent.com/Anas-2003/Anas-2003/main/assets/logo-animated.gif" width="150" alt="شعار أنس إيرامي" class="rounded-full header-image-glow">
        </div>

        <!-- الرأس بتأثير التموج -->
        <div class="text-center mb-8">
            <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00ffe0,100:ff00ff&height=300&section=header&text=Anas%20Erami%20🚀&fontSize=60&animation=fadeIn&fontColor=ffffff" alt="صورة الرأس" class="w-full rounded-xl header-image-glow">
        </div>

        <!-- نص متحرك -->
        <div class="text-center mb-12">
            <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=30&duration=4000&pause=1000&color=00FFE0&center=true&vCenter=true&width=600&lines=Hi+I’m+Anas+Erami.;Creative+Software+Developer.;Coding+is+my+art.;Let’s+build+something+amazing!" alt="نص متحرك" class="w-full max-w-xl mx-auto">
        </div>

        <hr class="border-t-2 border-purple-500 my-8">

        <!-- قسم عني -->
        <h2 class="text-3xl font-bold mb-4 text-center neon-text">👨‍💻 عني</h2>
        <p class="text-lg leading-relaxed mb-4 text-center neon-text">
            ✨ مطور برمجيات شغوف بحب <strong class="text-purple-400">الكود النظيف، الحلول الإبداعية، والتقنيات الحديثة</strong>.
        </p>
        <p class="text-lg leading-relaxed mb-4 text-center neon-text">
            ⚡ أعتقد أن <strong class="text-green-400">البرمجيات الرائعة ليست مجرد وظيفية—إنها ملهمة.</strong>
        </p>
        <p class="text-lg leading-relaxed mb-8 text-center neon-text">
            💡 أستكشف دائمًا أدوات وأطر عمل واتجاهات جديدة لأبقى في المقدمة.
        </p>

        <hr class="border-t-2 border-green-500 my-8">

        <!-- قسم التقنيات -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">🚀 التقنيات</h2>
        <div class="flex justify-center mb-8 skill-icon-glow">
            <img src="https://skillicons.dev/icons?i=html,css,js,react,tailwind,nodejs,python,django,flask,flutter,dart,mongodb,mysql,postgresql,git,linux,docker" alt="أيقونات التقنيات" class="w-full max-w-3xl">
        </div>

        <hr class="border-t-2 border-blue-500 my-8">

        <!-- قسم ما يميزني -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">🌟 ما يميزني</h2>
        <ul class="list-disc list-inside text-lg leading-relaxed mb-8 space-y-2 text-center">
            <li class="neon-text">🎨 <strong class="text-pink-400">حل المشكلات بشكل إبداعي</strong> بشغف لبناء حلول أنيقة</li>
            <li class="neon-text">⚡ <strong class="text-yellow-400">متعلم سريع</strong> ودائمًا فضولي حول التقنيات الناشئة</li>
            <li class="neon-text">🤝 مدافع عن <strong class="text-cyan-400">التعاون مفتوح المصدر</strong> ومشاركة المعرفة</li>
        </ul>

        <hr class="border-t-2 border-orange-500 my-8">

        <!-- قسم إحصائيات GitHub -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">📊 إحصائيات GitHub</h2>
        <div class="flex flex-col items-center space-y-6 mb-8">
            <img src="https://github-readme-stats.vercel.app/api?username=anas-2003&show_icons=true&theme=radical&hide_border=true&count_private=true" alt="إحصائيات GitHub" class="w-full max-w-md rounded-lg header-image-glow">
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=anas-2003&theme=radical&hide_border=true" alt="سلسلة GitHub" class="w-full max-w-md rounded-lg header-image-glow">
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=anas-2003&layout=compact&theme=radical&hide_border=true" alt="أكثر اللغات استخدامًا" class="w-full max-w-md rounded-lg header-image-glow">
        </div>

        <hr class="border-t-2 border-red-500 my-8">

        <!-- قسم رسم بياني للمساهمات المتحركة -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">🐍 رسم بياني للمساهمات المتحركة</h2>
        <div class="flex justify-center mb-8">
            <img src="https://raw.githubusercontent.com/Anas-2003/Anas-2003/output/github-contribution-grid-snake.svg" alt="رسوم متحركة للأفعى" class="w-full max-w-2xl rounded-lg header-image-glow">
        </div>

        <hr class="border-t-2 border-indigo-500 my-8">

        <!-- قسم تواصل معي -->
        <h2 class="text-3xl font-bold mb-6 text-center neon-text">🌐 تواصل معي</h2>
        <div class="flex justify-center space-x-4 mb-12">
            <a href="mailto:anaserami17@gmail.com" class="neon-link">
                <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="شارة البريد الإلكتروني"/>
            </a>
            <a href="https://github.com/anas-2003" class="neon-link">
                <img src="https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white" alt="شارة GitHub"/>
            </a>
        </div>

        <hr class="border-t-2 border-teal-500 my-8">

        <!-- شعار التذييل -->
        <h3 class="text-2xl font-bold text-center neon-text" style="color:#00ffe0;">
            ❤️ الإبداع • 💥 الشغف • 🚀 التعلم المستمر ❤️
        </h3>

        <!-- تأثير تموج التذييل -->
        <div class="text-center mt-8">
            <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00ffe0,100:ff00ff&height=200&section=footer" alt="صورة التذييل" class="w-full rounded-xl header-image-glow">
        </div>
    </div>

    <!-- JavaScript لتأثير الماتريكس -->
    <script>
        window.onload = function() {
            const canvas = document.getElementById('matrixCanvas');
            // تحقق من وجود اللوحة قبل محاولة الحصول على السياق
            if (!canvas) {
                console.error("Matrix canvas not found!");
                return;
            }

            const ctx = canvas.getContext('2d');
            // تحقق من وجود السياق قبل المتابعة
            if (!ctx) {
                console.error("2D context not supported for canvas!");
                return;
            }

            // تعيين أبعاد اللوحة
            let W = canvas.width = window.innerWidth;
            let H = canvas.height = window.innerHeight;

            // التعامل مع تغيير حجم النافذة
            window.addEventListener('resize', () => {
                W = canvas.width = window.innerWidth;
                H = canvas.height = window.innerHeight;
                columns = Array(Math.floor(W / fontSize)).fill(0); // إعادة حساب الأعمدة
            });

            // أحرف الماتريكس (كاتاكانا اليابانية، أرقام، رموز)
            const matrixChars = "日ﾊﾐﾋｰｳｼﾅﾓﾆｻﾜﾂｵﾘｱﾎﾃﾏｹﾒｴｶｷﾑﾕﾗｾﾈｽﾀﾇﾍｦｲｸｺｿﾁﾄﾉﾌﾔﾖﾙﾚﾛﾝ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ";
            const fontSize = 20; // حجم كل حرف
            let columns = Array(Math.floor(W / fontSize)).fill(0); // مصفوفة لتخزين موضع Y لكل عمود

            // رسم الأحرف
            function drawMatrix() {
                // ارسم مستطيلاً أسود شبه شفاف على كامل اللوحة
                // هذا يخلق تأثير التلاشي
                ctx.fillStyle = 'rgba(0, 0, 0, 0.05)';
                ctx.fillRect(0, 0, W, H);

                // تعيين لون الأحرف (أخضر نيون)
                ctx.fillStyle = '#00ffe0';
                ctx.font = `${fontSize}px monospace`; // خط أحادي المسافة لعرض حرف ثابت

                // حلقة على كل عمود
                for (let i = 0; i < columns.length; i++) {
                    // احصل على حرف عشوائي من سلسلة matrixChars
                    const text = matrixChars.charAt(Math.floor(Math.random() * matrixChars.length));
                    const x = i * fontSize; // موضع X للعمود
                    let y = columns[i] * fontSize; // موضع Y للحرف في هذا العمود

                    // أضف توهجًا خفيفًا للأحرف
                    ctx.shadowBlur = 10;
                    ctx.shadowColor = '#00ffe0';

                    // ارسم الحرف
                    ctx.fillText(text, x, y);

                    // أعد ضبط الظل للرسم التالي لتجنب التأثير التراكمي على الخلفية
                    ctx.shadowBlur = 0;

                    // إذا وصل الحرف إلى أسفل الشاشة
                    // أو تم استيفاء شرط عشوائي (لإنشاء فجوات/تدفقات جديدة)
                    if (y > H && Math.random() > 0.975) {
                        columns[i] = 0; // إعادة تعيين إلى الأعلى
                    } else {
                        columns[i]++; // تحريك الحرف للأسفل
                    }
                }
                requestAnimationFrame(drawMatrix); // تكرار الرسوم المتحركة
            }

            // ابدأ الرسوم المتحركة عند تحميل النافذة.
            drawMatrix();
        };
    </script>
</body>
</html>

