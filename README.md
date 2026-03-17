<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rishabh Tripathi | Data Scientist & AI Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --neon-green: #00ff88;
            --neon-cyan: #00cfff;
            --neon-purple: #a855f7;
            --neon-orange: #ff6b35;
            --bg-dark: #0d1117;
            --bg-card: #161b22;
            --text-primary: #ffffff;
            --text-secondary: #8b949e;
        }

        body {
            font-family: 'JetBrains Mono', 'Courier New', monospace;
            background: var(--bg-dark);
            color: var(--text-primary);
            overflow-x: hidden;
        }

        /* Animated Background */
        .animated-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, #0d1117 0%, #1a1f2e 50%, #0d1117 100%);
            z-index: -1;
        }

        .animated-bg::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: 
                radial-gradient(circle at 20% 50%, rgba(0, 255, 136, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 50%, rgba(0, 207, 255, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 50% 50%, rgba(168, 85, 247, 0.05) 0%, transparent 50%);
            animation: bgFloat 20s ease-in-out infinite;
        }

        @keyframes bgFloat {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            33% { transform: translate(30px, -30px) rotate(5deg); }
            66% { transform: translate(-30px, 30px) rotate(-5deg); }
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Typing Animation Section */
        #typing-section {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            gap: 20px;
        }

        .typing-container {
            font-size: 1.5rem;
            color: var(--neon-green);
            text-shadow: 0 0 20px var(--neon-green);
            font-weight: bold;
            min-height: 60px;
            display: flex;
            align-items: center;
        }

        #typed-text {
            border-right: 3px solid var(--neon-green);
            padding-right: 5px;
            animation: blink 0.7s infinite;
        }

        @keyframes blink {
            0%, 50% { border-color: var(--neon-green); }
            51%, 100% { border-color: transparent; }
        }

        .loading-bar {
            width: 300px;
            height: 4px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 2px;
            overflow: hidden;
            display: none;
        }

        .loading-bar.active {
            display: block;
        }

        .loading-progress {
            height: 100%;
            background: linear-gradient(90deg, var(--neon-green), var(--neon-cyan));
            width: 0%;
            animation: loadProgress 1s ease-out forwards;
        }

        @keyframes loadProgress {
            to { width: 100%; }
        }

        /* Content Sections */
        .content-section {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .content-section.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 100px 20px;
            margin-top: -80px;
        }

        .hero h1 {
            font-size: 4rem;
            background: linear-gradient(90deg, var(--neon-green), var(--neon-cyan), var(--neon-purple));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 20px rgba(0, 255, 136, 0.5)); }
            to { filter: drop-shadow(0 0 40px rgba(0, 255, 136, 0.8)); }
        }

        .hero p {
            font-size: 1.5rem;
            color: var(--text-secondary);
            margin-bottom: 30px;
        }

        /* IBM Badge Section */
        .badge-showcase {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 40px;
            padding: 60px 20px;
            flex-wrap: wrap;
        }

        .badge-card {
            background: var(--bg-card);
            border: 2px solid rgba(0, 255, 136, 0.2);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
            max-width: 300px;
        }

        .badge-card:hover {
            border-color: var(--neon-green);
            box-shadow: 0 0 30px rgba(0, 255, 136, 0.3);
            transform: translateY(-10px);
        }

        .badge-image {
            width: 200px;
            height: 200px;
            margin-bottom: 20px;
            filter: drop-shadow(0 0 20px rgba(0, 255, 136, 0.3));
            transition: transform 0.3s ease;
        }

        .badge-card:hover .badge-image {
            transform: scale(1.1) rotate(5deg);
        }

        .badge-title {
            font-size: 1.2rem;
            color: var(--neon-green);
            margin-bottom: 10px;
            font-weight: bold;
        }

        .badge-subtitle {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* Stats Badges */
        .stats-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            padding: 40px 20px;
        }

        .stat-badge {
            background: var(--bg-card);
            border: 2px solid rgba(0, 207, 255, 0.3);
            border-radius: 12px;
            padding: 15px 30px;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .stat-badge:hover {
            border-color: var(--neon-cyan);
            box-shadow: 0 0 20px rgba(0, 207, 255, 0.3);
            transform: scale(1.05);
        }

        /* About Section */
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            padding: 60px 20px;
        }

        .about-card {
            background: var(--bg-card);
            border: 2px solid rgba(168, 85, 247, 0.2);
            border-radius: 16px;
            padding: 30px;
            transition: all 0.3s ease;
        }

        .about-card:hover {
            border-color: var(--neon-purple);
            box-shadow: 0 0 30px rgba(168, 85, 247, 0.2);
            transform: translateY(-5px);
        }

        .about-card h3 {
            color: var(--neon-cyan);
            margin-bottom: 15px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .about-card ul {
            list-style: none;
            color: var(--text-secondary);
        }

        .about-card li {
            padding: 8px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .about-card li:before {
            content: '▹ ';
            color: var(--neon-green);
            font-weight: bold;
            margin-right: 8px;
        }

        /* Tech Stack */
        .tech-stack {
            padding: 60px 20px;
        }

        .tech-stack h2 {
            text-align: center;
            font-size: 2.5rem;
            color: var(--neon-green);
            margin-bottom: 40px;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
        }

        .tech-item {
            background: var(--bg-card);
            border: 2px solid rgba(0, 255, 136, 0.2);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tech-item:hover {
            border-color: var(--neon-green);
            box-shadow: 0 0 25px rgba(0, 255, 136, 0.3);
            transform: translateY(-5px);
        }

        .tech-emoji {
            font-size: 3rem;
            margin-bottom: 10px;
        }

        .tech-name {
            color: var(--text-primary);
            font-size: 1rem;
            font-weight: bold;
        }

        /* Skills Progress */
        .skills-section {
            padding: 60px 20px;
        }

        .skills-section h2 {
            text-align: center;
            font-size: 2.5rem;
            color: var(--neon-cyan);
            margin-bottom: 40px;
        }

        .skill-bar {
            margin-bottom: 30px;
        }

        .skill-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            color: var(--text-primary);
        }

        .progress-bar {
            width: 100%;
            height: 12px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 6px;
            overflow: hidden;
            position: relative;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--neon-green), var(--neon-cyan));
            border-radius: 6px;
            transition: width 1s ease;
            position: relative;
            overflow: hidden;
        }

        .progress-fill::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            animation: shimmer 2s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        /* Contact Section */
        .contact-section {
            padding: 60px 20px;
            text-align: center;
        }

        .contact-section h2 {
            font-size: 2.5rem;
            color: var(--neon-purple);
            margin-bottom: 40px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: var(--bg-card);
            border: 2px solid rgba(0, 255, 136, 0.3);
            border-radius: 12px;
            padding: 15px 25px;
            text-decoration: none;
            color: var(--text-primary);
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            border-color: var(--neon-green);
            box-shadow: 0 0 25px rgba(0, 255, 136, 0.4);
            transform: scale(1.05);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 40px 20px;
            color: var(--text-secondary);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .footer-quote {
            font-size: 1.2rem;
            color: var(--neon-green);
            margin-bottom: 20px;
            font-style: italic;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .hero p { font-size: 1.2rem; }
            .typing-container { font-size: 1.2rem; }
            .tech-grid { grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); }
        }
    </style>
</head>
<body>
    <div class="animated-bg"></div>

    <!-- Typing Animation Section -->
    <div id="typing-section">
        <div class="typing-container">
            <span id="typed-text"></span>
        </div>
        <div class="loading-bar" id="loading-bar">
            <div class="loading-progress"></div>
        </div>
    </div>

    <!-- Main Content -->
    <div id="main-content" style="display: none;">
        <div class="container">
            <!-- Hero Section -->
            <section class="hero content-section" data-delay="200">
                <h1>RISHABH TRIPATHI</h1>
                <p>Data Scientist | Fullstack Developer | AI Engineer</p>
                <p style="color: var(--neon-green); font-size: 1.2rem;">🚀 Trailblazer. Always Building.</p>
            </section>

            <!-- IBM Badge Showcase -->
            <section class="content-section" data-delay="600">
                <div class="badge-showcase">
                    <div class="badge-card">
                        <img src="ibm-badge.png" alt="IBM Python for Data Science" class="badge-image">
                        <div class="badge-title">IBM Certified</div>
                        <div class="badge-subtitle">Python for Data Science - Cognitive Class</div>
                    </div>
                    <div class="badge-card">
                        <div style="font-size: 5rem; margin-bottom: 20px;">🎯</div>
                        <div class="badge-title">Trailblazer Status</div>
                        <div class="badge-subtitle">Actively Building the Future</div>
                    </div>
                </div>
            </section>

            <!-- Stats Badges -->
            <section class="content-section" data-delay="1000">
                <div class="stats-container">
                    <div class="stat-badge" style="border-color: rgba(0, 255, 136, 0.5);">
                        <span style="color: var(--neon-green);">📍</span> INDIA 🇮🇳
                    </div>
                    <div class="stat-badge" style="border-color: rgba(255, 107, 53, 0.5);">
                        <span style="color: var(--neon-orange);">⚡</span> ACTIVELY BUILDING
                    </div>
                    <div class="stat-badge" style="border-color: rgba(168, 85, 247, 0.5);">
                        <span style="color: var(--neon-purple);">🎓</span> AI/ML SPECIALIST
                    </div>
                </div>
            </section>

            <!-- About Cards -->
            <section class="content-section" data-delay="1400">
                <div class="about-grid">
                    <div class="about-card">
                        <h3>📚 Currently Learning</h3>
                        <ul>
                            <li>React Native 📱</li>
                            <li>GoLang ⚡</li>
                            <li>Web3 Integration 🌐</li>
                        </ul>
                    </div>
                    <div class="about-card">
                        <h3>🤝 Collaborating On</h3>
                        <ul>
                            <li>Speech & Language Therapy Automation 🧠</li>
                            <li>Smart Traffic Management × Web3 🚦</li>
                            <li>GenAI Applications 🤖</li>
                        </ul>
                    </div>
                    <div class="about-card">
                        <h3>✍️ Writing About</h3>
                        <ul>
                            <li>Latest Tech Trends</li>
                            <li>Real-time Project Implementation</li>
                            <li>AI/ML Best Practices</li>
                        </ul>
                    </div>
                </div>
            </section>

            <!-- Tech Stack -->
            <section class="tech-stack content-section" data-delay="1800">
                <h2>&gt; TECH_ARSENAL</h2>
                <div class="tech-grid">
                    <div class="tech-item">
                        <div class="tech-emoji">🐍</div>
                        <div class="tech-name">Python</div>
                    </div>
                    <div class="tech-item">
                        <div class="tech-emoji">⚛️</div>
                        <div class="tech-name">React</div>
                    </div>
                    <div class="tech-item">
                        <div class="tech-emoji">🔥</div>
                        <div class="tech-name">PyTorch</div>
                    </div>
                    <div class="tech-item">
                        <div class="tech-emoji">🧠</div>
                        <div class="tech-name">TensorFlow</div>
                    </div>
                    <div class="tech-item">
                        <div class="tech-emoji">📊</div>
                        <div class="tech-name">Data Science</div>
                    </div>
                    <div class="tech-item">
                        <div class="tech-emoji">🟢</div>
                        <div class="tech-name">Node.js</div>
                    </div>
                    <div class="tech-item">
                        <div class="tech-emoji">🔷</div>
                        <div class="tech-name">Go</div>
                    </div>
                    <div class="tech-item">
                        <div class="tech-emoji">☁️</div>
                        <div class="tech-name">AWS</div>
                    </div>
                </div>
            </section>

            <!-- Skills Progress -->
            <section class="skills-section content-section" data-delay="2200">
                <h2>&gt; SKILL_LEVELS</h2>
                <div class="skill-bar">
                    <div class="skill-label">
                        <span>AI / ML 🧬</span>
                        <span>95%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 0%" data-width="95%"></div>
                    </div>
                </div>
                <div class="skill-bar">
                    <div class="skill-label">
                        <span>React ⚛️</span>
                        <span>90%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 0%" data-width="90%"></div>
                    </div>
                </div>
                <div class="skill-bar">
                    <div class="skill-label">
                        <span>Python 🐍</span>
                        <span>90%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 0%" data-width="90%"></div>
                    </div>
                </div>
                <div class="skill-bar">
                    <div class="skill-label">
                        <span>Node.js 🟢</span>
                        <span>80%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 0%" data-width="80%"></div>
                    </div>
                </div>
                <div class="skill-bar">
                    <div class="skill-label">
                        <span>GoLang 🔷</span>
                        <span>50%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 0%" data-width="50%"></div>
                    </div>
                </div>
            </section>

            <!-- Contact Section -->
            <section class="contact-section content-section" data-delay="2600">
                <h2>&gt; CONNECT</h2>
                <div class="social-links">
                    <a href="https://linkedin.com/in/rishabh-tripathi-403420210" class="social-link" target="_blank">
                        <span>💼</span> LinkedIn
                    </a>
                    <a href="https://github.com/rish-23072005" class="social-link" target="_blank">
                        <span>💻</span> GitHub
                    </a>
                    <a href="https://medium.com/@Rishabhtripathi" class="social-link" target="_blank">
                        <span>📝</span> Medium
                    </a>
                    <a href="https://youtube.com/@rishabhtripathi5124" class="social-link" target="_blank">
                        <span>📺</span> YouTube
                    </a>
                </div>
            </section>

            <!-- Footer -->
            <footer class="footer content-section" data-delay="3000">
                <div class="footer-quote">
                    "Don't just consume technology. Create with it."
                </div>
                <p>— Rishabh Tripathi</p>
                <p style="margin-top: 20px;">Transmission ends. Stay curious. Keep building. 🚀</p>
            </footer>
        </div>
    </div>

    <script>
        // Typing Animation
        const textToType = "> Initializing agent profile...\n> Loading tech stack... ✅\n> Building things that matter 🚀\n> AI | ML | MERN | Web3 | GenAI\n> Trailblazer. Always 🚀";
        const typedTextElement = document.getElementById('typed-text');
        let charIndex = 0;
        const typingSpeed = 50; // milliseconds per character

        function typeText() {
            if (charIndex < textToType.length) {
                const char = textToType.charAt(charIndex);
                if (char === '\n') {
                    typedTextElement.innerHTML += '<br>';
                } else {
                    typedTextElement.textContent += char;
                }
                charIndex++;
                setTimeout(typeText, typingSpeed);
            } else {
                // Typing complete, show loading bar
                setTimeout(() => {
                    document.getElementById('loading-bar').classList.add('active');
                    
                    // After loading completes, show main content
                    setTimeout(() => {
                        document.getElementById('typing-section').style.display = 'none';
                        document.getElementById('main-content').style.display = 'block';
                        
                        // Trigger content animations
                        revealContent();
                    }, 1200); // 1200ms for loading bar animation
                }, 500); // 500ms delay before showing loading bar
            }
        }

        // Content Reveal with precise timing
        function revealContent() {
            const sections = document.querySelectorAll('.content-section');
            
            sections.forEach((section) => {
                const delay = parseInt(section.dataset.delay);
                
                setTimeout(() => {
                    section.classList.add('visible');
                    
                    // Animate skill bars when visible
                    if (section.classList.contains('skills-section')) {
                        const progressBars = section.querySelectorAll('.progress-fill');
                        progressBars.forEach((bar) => {
                            setTimeout(() => {
                                bar.style.width = bar.dataset.width;
                            }, 100);
                        });
                    }
                }, delay);
            });
        }

        // Start typing animation on page load
        window.addEventListener('load', () => {
            setTimeout(() => {
                typeText();
            }, 500);
        });

        // Console easter egg
        console.log('%c> AGENT PROFILE LOADED', 'color: #00ff88; font-size: 20px; font-weight: bold;');
        console.log('%c> System Status: OPERATIONAL ✅', 'color: #00cfff; font-size: 14px;');
        console.log('%c> Trailblazer Mode: ACTIVE 🚀', 'color: #a855f7; font-size: 14px;');
    </script>
</body>
</html>
