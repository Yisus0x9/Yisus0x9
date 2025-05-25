<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README Animado - Yisus</title>
    <style>
        body {
            background: #0d1117;
            color: #e6edf3;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
            line-height: 1.5;
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        h2, h3 {
            color: #f0f6fc;
        }

        .profile-section {
            text-align: center;
            margin: 40px 0;
        }

        .animated-profile-container {
            position: relative;
            display: inline-block;
            margin: 20px 0;
        }

        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            position: relative;
            z-index: 2;
        }

        .rotating-border {
            position: absolute;
            top: -15px;
            left: -15px;
            right: -15px;
            bottom: -15px;
            border-radius: 50%;
            background: conic-gradient(
                from 0deg,
                #ff0080,
                #ff8c00,
                #ffd700,
                #00ff80,
                #00bfff,
                #8000ff,
                #ff0080
            );
            animation: rotate 3s linear infinite;
            z-index: 1;
        }

        .inner-border {
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            background: #0d1117;
            border-radius: 50%;
            z-index: 1;
        }

        .glow-effect {
            position: absolute;
            top: -20px;
            left: -20px;
            right: -20px;
            bottom: -20px;
            border-radius: 50%;
            background: radial-gradient(
                circle,
                rgba(255, 0, 128, 0.3) 0%,
                rgba(255, 140, 0, 0.2) 25%,
                rgba(255, 215, 0, 0.2) 50%,
                rgba(0, 255, 128, 0.2) 75%,
                transparent 100%
            );
            animation: pulse 2s ease-in-out infinite alternate;
            z-index: 0;
        }

        .floating-lights {
            position: absolute;
            top: -30px;
            left: -30px;
            right: -30px;
            bottom: -30px;
            border-radius: 50%;
            z-index: 0;
        }

        .light {
            position: absolute;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            animation: orbit 4s linear infinite;
        }

        .light:nth-child(1) {
            background: #ff0080;
            box-shadow: 0 0 10px #ff0080, 0 0 20px #ff0080;
            animation-delay: 0s;
        }

        .light:nth-child(2) {
            background: #00bfff;
            box-shadow: 0 0 10px #00bfff, 0 0 20px #00bfff;
            animation-delay: -1s;
        }

        .light:nth-child(3) {
            background: #ffd700;
            box-shadow: 0 0 10px #ffd700, 0 0 20px #ffd700;
            animation-delay: -2s;
        }

        .light:nth-child(4) {
            background: #00ff80;
            box-shadow: 0 0 10px #00ff80, 0 0 20px #00ff80;
            animation-delay: -3s;
        }

        @keyframes rotate {
            from {
                transform: rotate(0deg);
            }
            to {
                transform: rotate(360deg);
            }
        }

        @keyframes pulse {
            0% {
                transform: scale(1);
                opacity: 0.3;
            }
            100% {
                transform: scale(1.1);
                opacity: 0.6;
            }
        }

        @keyframes orbit {
            from {
                transform: rotate(0deg) translateX(105px) rotate(0deg);
            }
            to {
                transform: rotate(360deg) translateX(105px) rotate(-360deg);
            }
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 30px 0;
        }

        .social-links img {
            transition: transform 0.3s ease, filter 0.3s ease;
        }

        .social-links img:hover {
            transform: scale(1.1) rotate(5deg);
            filter: brightness(1.2);
        }

        .badge {
            display: inline-block;
            margin: 10px 0;
        }

        .stats-section {
            text-align: center;
            margin: 40px 0;
        }

        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin: 20px 0;
        }

        .tech-icons img {
            transition: transform 0.3s ease, filter 0.3s ease;
        }

        .tech-icons img:hover {
            transform: translateY(-5px) scale(1.1);
            filter: drop-shadow(0 5px 15px rgba(255, 255, 255, 0.3));
        }

        .about-text {
            text-align: left;
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.6;
        }

        .highlight {
            color: #58a6ff;
            font-weight: 600;
        }

        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }
            
            .profile-image {
                width: 120px;
                height: 120px;
            }
            
            .rotating-border {
                top: -12px;
                left: -12px;
                right: -12px;
                bottom: -12px;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="profile-section">
            <h2>Hi 👋! I'm Yisus, I'm from Mexico and I'm a student of computer systems engineering at the National Polytechnic Institute</h2>
            
            <div class="animated-profile-container">
                <div class="glow-effect"></div>
                <div class="rotating-border"></div>
                <div class="inner-border"></div>
                <div class="floating-lights">
                    <div class="light"></div>
                    <div class="light"></div>
                    <div class="light"></div>
                    <div class="light"></div>
                </div>
                <img class="profile-image" src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExMWZycWV6bGdhZnQzY2dpYTJrMXBueWJyb3lob2FmOGxkbHFmZXhsZyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/jBOOXxSJfG8kqMxT11/giphy.gif" alt="Profile GIF" />
            </div>

            <div class="badge">
                <img src="https://visitor-badge.laobi.icu/badge?page_id=Yisus0x9.Yisus0x9&" alt="Visitor Badge" />
            </div>

            <div class="social-links">
                <a href="https://www.linkedin.com/in/pe%C3%B1arrieta-villa-jes%C3%BAs-573066352?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank">
                    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="LinkedIn" />
                </a>
                <a href="https://www.instagram.com/yisu0s9/profilecard/?igsh=MTZpYTY5cjc4YjU1Mw==" target="_blank">
                    <img src="https://img.shields.io/static/v1?message=Instagram&logo=instagram&label=&color=E4405F&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="Instagram" />
                </a>
                <a href="https://discord.gg/Yisus0m9n7" target="_blank">
                    <img src="https://img.shields.io/static/v1?message=Discord&logo=discord&label=&color=7289DA&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="Discord" />
                </a>
            </div>
        </div>

        <h3>👩‍💻 About Me</h3>
        <div class="about-text">
            <p>I'm passionate about continuously learning new technologies and skills that contribute to my professional growth. I particularly enjoy working with the <span class="highlight">Java programming language</span>, due to its versatility and the wide range of applications it offers.</p>
            
            <p>On the other hand, I'm tremendously enthusiastic about the <span class="highlight">hardware world</span>, particularly in the IoT and embedded systems domain. I find it fascinating how complex problems can be solved by integrating tangible elements that can be controlled and programmed to achieve specific objectives.</p>
            
            <p>Currently, I'm also exploring the exciting world of <span class="highlight">artificial intelligence</span>, from machine learning to deep learning. It's incredible the potential and possibilities these technologies offer to transform the way we approach real-world challenges.</p>
            
            <ul style="list-style: none; padding-left: 0;">
                <li>🔭 I'm working as <span class="highlight">hardware developer</span></li>
                <li>📚 I'm currently learning <span class="highlight">English, Spring Framework and Fusion 360</span></li>
                <li>⚡ In my free time I enjoy spending time with friends, playing video games, and watching videos about how innovative IoT and embedded systems projects are developed.</li>
            </ul>
        </div>

        <div class="stats-section">
            <h3>🔥 My Stats:</h3>
            <img src="https://streak-stats.demolab.com?user=Yisus0x9&locale=en&mode=daily&theme=dark&hide_border=false&border_radius=5&order=3" height="220" alt="GitHub Stats" />
        </div>

        <h3>🛠 Language and tools</h3>
        <div class="tech-icons">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="30" alt="Java" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="30" alt="C" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/haskell/haskell-original.svg" height="30" alt="Haskell" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/raspberrypi/raspberrypi-original.svg" height="30" alt="Raspberry Pi" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="30" alt="JavaScript" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" height="30" alt="TypeScript" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="30" alt="React" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="30" alt="HTML5" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="30" alt="CSS3" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="30" alt="Python" />
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" height="30" alt="Next.js" />
        </div>
    </div>
</body>
</html>
