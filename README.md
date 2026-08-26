<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jane | Developer Portfolio</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
    
    <style>
        /* --- ROOT VARIABLES & SOFT LILAC THEME --- */
        :root {
            --bg-dark: #0D0B12;
            --bg-card: #15121E;
            --bg-card-hover: #1D182B;
            --border-color: #2D263F;
            --border-highlight: #4A3E68;
            
            --lilac-primary: #C8A2C8;
            --lilac-soft: #E6E6FA;
            --lilac-muted: #9B82B3;
            --lilac-glow: rgba(200, 162, 200, 0.15);
            
            --text-main: #F3F0F7;
            --text-muted: #A39BB0;
            
            --font-sans: 'Plus Jakarta Sans', sans-serif;
            --font-mono: 'JetBrains Mono', monospace;
        }

        /* --- GLOBAL RESET & BASE STYLES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            font-family: var(--font-sans);
            line-height: 1.6;
            overflow-x: hidden;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        ul {
            list-style: none;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* --- TYPOGRAPHY & BADGES --- */
        .section-tag {
            font-family: var(--font-mono);
            font-size: 0.85rem;
            color: var(--lilac-primary);
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 12px;
            display: inline-block;
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 40px;
            letter-spacing: -0.5px;
        }

        .pill-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(200, 162, 200, 0.1);
            border: 1px solid var(--border-highlight);
            color: var(--lilac-soft);
            padding: 6px 16px;
            border-radius: 100px;
            font-size: 0.85rem;
            font-weight: 500;
            margin-bottom: 20px;
        }

        .pill-badge .dot {
            width: 8px;
            height: 8px;
            background-color: #50fa7b;
            border-radius: 50%;
            box-shadow: 0 0 8px #50fa7b;
        }

        .tech-badge {
            font-family: var(--font-mono);
            font-size: 0.75rem;
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid var(--border-color);
            color: var(--lilac-soft);
            padding: 4px 10px;
            border-radius: 6px;
        }

        /* --- BUTTONS --- */
        .btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 24px;
            border-radius: 8px;
            font-weight: 600;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .btn-primary {
            background-color: var(--lilac-primary);
            color: var(--bg-dark);
            border: 1px solid var(--lilac-primary);
        }

        .btn-primary:hover {
            background-color: var(--lilac-soft);
            box-shadow: 0 0 20px var(--lilac-glow);
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: transparent;
            color: var(--text-main);
            border: 1px solid var(--border-highlight);
        }

        .btn-secondary:hover {
            border-color: var(--lilac-primary);
            color: var(--lilac-soft);
            background: rgba(200, 162, 200, 0.05);
            transform: translateY(-2px);
        }

        /* --- NAVBAR --- */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 100;
            background: rgba(13, 11, 18, 0.8);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-color);
            padding: 20px 0;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-weight: 800;
            font-size: 1.2rem;
            letter-spacing: -0.5px;
            color: var(--text-main);
        }

        .logo span {
            color: var(--lilac-primary);
        }

        .nav-links {
            display: flex;
            gap: 32px;
        }

        .nav-links a {
            font-size: 0.9rem;
            color: var(--text-muted);
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--lilac-soft);
        }

        /* --- HERO SECTION --- */
        .hero {
            padding: 160px 0 100px;
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 60px;
            align-items: center;
        }

        .hero-heading {
            font-size: 3.5rem;
            font-weight: 800;
            line-height: 1.1;
            margin-bottom: 16px;
            background: linear-gradient(135deg, #FFF 0%, var(--lilac-soft) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-submotto {
            font-size: 1.5rem;
            color: var(--lilac-primary);
            font-weight: 600;
            margin-bottom: 16px;
        }

        .hero-bio {
            color: var(--text-muted);
            font-size: 1.05rem;
            margin-bottom: 32px;
            max-width: 540px;
        }

        .hero-cta {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
        }

        /* --- HERO PROFILE CARD --- */
        .profile-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 32px;
            position: relative;
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
            transition: border-color 0.3s ease;
        }

        .profile-card:hover {
            border-color: var(--border-highlight);
        }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 16px;
            margin-bottom: 24px;
        }

        .card-badge {
            font-family: var(--font-mono);
            font-size: 0.8rem;
            color: var(--lilac-primary);
        }

        .card-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-bottom: 24px;
        }

        .stat-box {
            background: rgba(255, 255, 255, 0.02);
            padding: 16px;
            border-radius: 8px;
            border: 1px solid var(--border-color);
        }

        .stat-number {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--lilac-soft);
            display: block;
        }

        .stat-label {
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        .status-box {
            display: flex;
            align-items: center;
            gap: 12px;
            background: rgba(200, 162, 200, 0.05);
            padding: 12px 16px;
            border-radius: 8px;
            border: 1px dashed var(--border-highlight);
            font-size: 0.85rem;
            color: var(--lilac-soft);
        }

        /* --- INFINITE TICKER MARQUEE --- */
        .marquee-section {
            padding: 30px 0;
            background: var(--bg-card);
            border-y: 1px solid var(--border-color);
            overflow: hidden;
            white-space: nowrap;
        }

        .marquee-content {
            display: inline-flex;
            gap: 40px;
            animation: scroll 20s linear infinite;
        }

        .marquee-item {
            font-family: var(--font-mono);
            font-size: 1rem;
            color: var(--text-muted);
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .marquee-item span {
            color: var(--lilac-primary);
        }

        @keyframes scroll {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- SECTIONS COMMON --- */
        .section {
            padding: 100px 0;
            border-bottom: 1px solid var(--border-color);
        }

        /* --- PROJECTS --- */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 32px;
        }

        .project-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: translateY(-6px);
            border-color: var(--border-highlight);
            box-shadow: 0 12px 30px rgba(0,0,0,0.5);
        }

        .project-img-placeholder {
            height: 200px;
            width: 100%;
            background: #110E18;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .project-img-placeholder svg {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .project-content {
            padding: 24px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .project-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
        }

        .project-desc {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 20px;
            flex-grow: 1;
        }

        .project-tags {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
            margin-bottom: 20px;
        }

        /* --- TOOLKIT GRID --- */
        .toolkit-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 24px;
        }

        .toolkit-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 24px;
        }

        .toolkit-card h3 {
            font-size: 1.1rem;
            color: var(--lilac-soft);
            margin-bottom: 16px;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 8px;
        }

        .toolkit-list li {
            font-size: 0.9rem;
            color: var(--text-muted);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .toolkit-list li::before {
            content: "▹";
            color: var(--lilac-primary);
        }

        /* --- PROCESS --- */
        .process-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 24px;
        }

        .process-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 28px;
            position: relative;
        }

        .process-number {
            font-family: var(--font-mono);
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--lilac-primary);
            margin-bottom: 12px;
            display: block;
        }

        .process-card h3 {
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        .process-card p {
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        /* --- CONTACT & FOOTER --- */
        .contact-section {
            text-align: center;
            padding: 120px 0;
        }

        .contact-heading {
            font-size: 3rem;
            font-weight: 800;
            margin-bottom: 20px;
            letter-spacing: -1px;
        }

        .contact-email {
            font-size: 1.5rem;
            font-family: var(--font-mono);
            color: var(--lilac-primary);
            display: inline-block;
            margin-bottom: 30px;
            border-bottom: 2px solid transparent;
            transition: all 0.3s ease;
        }

        .contact-email:hover {
            color: var(--lilac-soft);
            border-bottom-color: var(--lilac-soft);
        }

        footer {
            padding: 40px 0;
            text-align: center;
            font-size: 0.85rem;
            color: var(--text-muted);
            border-top: 1px solid var(--border-color);
        }

        @media (max-width: 992px) {
            .hero {
                grid-template-columns: 1fr;
                gap: 40px;
                padding-top: 120px;
            }
            .toolkit-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 600px) {
            .hero-heading {
                font-size: 2.5rem;
            }
            .nav-links {
                display: none;
            }
            .toolkit-grid {
                grid-template-columns: 1fr;
            }
            .contact-heading {
                font-size: 2rem;
            }
            .contact-email {
                font-size: 1.1rem;
            }
        }
    </style>
</head>
<body>

    <!-- NAVBAR -->
    <nav class="navbar">
        <div class="container nav-container">
            <a href="#" class="logo">JANE<span>.DEV</span></a>
            <ul class="nav-links">
                <li><a href="#home">01 Home</a></li>
                <li><a href="#skills">02 Skills</a></li>
                <li><a href="#projects">03 Work</a></li>
                <li><a href="#process">04 Process</a></li>
            </ul>
            <a href="#contact" class="btn btn-secondary">Let's talk ↗</a>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <header id="home" class="container hero">
        <div>
            <div class="pill-badge">
                <span class="dot"></span>
                • Student / Builder
            </div>
            <h1 class="hero-heading">Hello, Jane</h1>
            <div class="hero-submotto">Code that turns ideas into things.</div>
            <p class="hero-bio">
                I'm a developer passionate about crafting sleek digital experiences, building functional software, and exploring modern web technology stacks.
            </p>
            <div class="hero-cta">
                <a href="#projects" class="btn btn-primary">See selected work ↘</a>
                <a href="https://github.com/honeylemorano" target="_blank" class="btn btn-secondary">GitHub ↗</a>
            </div>
        </div>

        <!-- SIDE PROFILE CARD -->
        <div class="profile-card">
            <div class="card-header">
                <span class="card-badge">DEV / PROFILE_001</span>
                <span class="tech-badge">STATUS: ONLINE</span>
            </div>
            <div class="card-stats">
                <div class="stat-box">
                    <span class="stat-number">2</span>
                    <span class="stat-label">Active Repositories</span>
                </div>
                <div class="stat-box">
                    <span class="stat-number">100%</span>
                    <span class="stat-label">Passion to Build</span>
                </div>
            </div>
            <div class="status-box">
                <span>⚡</span>
                <span>Currently learning & building web apps</span>
            </div>
        </div>
    </header>

    <!-- INFINITE TECH TICKER -->
    <section class="marquee-section">
        <div class="marquee-content">
            <div class="marquee-item"><span>/</span> HTML5</div>
            <div class="marquee-item"><span>/</span> CSS3</div>
            <div class="marquee-item"><span>/</span> JAVASCRIPT</div>
            <div class="marquee-item"><span>/</span> PHP</div>
            <div class="marquee-item"><span>/</span> MYSQL</div>
            <div class="marquee-item"><span>/</span> C#</div>
            <div class="marquee-item"><span>/</span> GIT</div>
            <div class="marquee-item"><span>/</span> UI/UX DESIGN</div>
            <div class="marquee-item"><span>/</span> HTML5</div>
            <div class="marquee-item"><span>/</span> CSS3</div>
            <div class="marquee-item"><span>/</span> JAVASCRIPT</div>
            <div class="marquee-item"><span>/</span> PHP</div>
            <div class="marquee-item"><span>/</span> MYSQL</div>
            <div class="marquee-item"><span>/</span> C#</div>
            <div class="marquee-item"><span>/</span> GIT</div>
            <div class="marquee-item"><span>/</span> UI/UX DESIGN</div>
        </div>
    </section>

    <!-- WORK / PROJECTS SECTION -->
    <section id="projects" class="section">
        <div class="container">
            <span class="section-tag">03 / Selected Work</span>
            <h2 class="section-title">Featured Projects</h2>

            <div class="projects-grid">
                <!-- Project 1: Luxcary Online Shopping System -->
                <div class="project-card">
                    <div class="project-img-placeholder">
                        <!-- Homepage Preview Mockup: E-Commerce Storefront -->
                        <svg viewBox="0 0 400 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <rect width="400" height="200" fill="#15121E"/>
                            <!-- Mini Browser Header -->
                            <rect width="400" height="24" fill="#1D182B"/>
                            <circle cx="12" cy="12" r="3" fill="#FF5F56"/>
                            <circle cx="22" cy="12" r="3" fill="#FFBD2E"/>
                            <circle cx="32" cy="12" r="3" fill="#27C93F"/>
                            <rect x="70" y="6" width="260" height="12" rx="3" fill="#2D263F"/>
                            <!-- Storefront Content Mock -->
                            <rect x="20" y="36" width="360" height="24" rx="4" fill="#201A2E"/>
                            <rect x="30" y="44" width="60" height="8" rx="2" fill="#C8A2C8"/>
                            <rect x="300" y="44" width="40" height="8" rx="2" fill="#9B82B3"/>
                            <rect x="350" y="44" width="20" height="8" rx="2" fill="#9B82B3"/>
                            <!-- Hero Banner inside Shop -->
                            <rect x="20" y="68" width="360" height="50" rx="4" fill="#2A223B"/>
                            <rect x="35" y="80" width="120" height="10" rx="3" fill="#E6E6FA"/>
                            <rect x="35" y="96" width="80" height="8" rx="2" fill="#C8A2C8"/>
                            <!-- Product Cards Grid inside Shop -->
                            <rect x="20" y="126" width="112" height="60" rx="4" fill="#1D182B"/>
                            <rect x="144" y="126" width="112" height="60" rx="4" fill="#1D182B"/>
                            <rect x="268" y="126" width="112" height="60" rx="4" fill="#1D182B"/>
                        </svg>
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Luxcary Online Shopping System</h3>
                        <p class="project-desc">An e-commerce platform designed for smooth product catalog browsing, dynamic cart management, and seamless checkout functionality.</p>
                        <div class="project-tags">
                            <span class="tech-badge">PHP</span>
                            <span class="tech-badge">MySQL</span>
                            <span class="tech-badge">HTML/CSS</span>
                            <span class="tech-badge">JS</span>
                        </div>
                        <a href="https://github.com/honeylemorano/Luxcary-online-shopping-system" target="_blank" class="btn btn-secondary" style="font-size:0.85rem; padding: 8px 16px;">View source code ↗</a>
                    </div>
                </div>

                <!-- Project 2: Restaurant Reservation System -->
                <div class="project-card">
                    <div class="project-img-placeholder">
                        <!-- Homepage Preview Mockup: Restaurant Booking Interface -->
                        <svg viewBox="0 0 400 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <rect width="400" height="200" fill="#15121E"/>
                            <!-- Mini Browser Header -->
                            <rect width="400" height="24" fill="#1D182B"/>
                            <circle cx="12" cy="12" r="3" fill="#FF5F56"/>
                            <circle cx="22" cy="12" r="3" fill="#FFBD2E"/>
                            <circle cx="32" cy="12" r="3" fill="#27C93F"/>
                            <rect x="70" y="6" width="260" height="12" rx="3" fill="#2D263F"/>
                            <!-- Restaurant App Header -->
                            <rect x="20" y="36" width="360" height="30" rx="4" fill="#201A2E"/>
                            <rect x="35" y="47" width="90" height="8" rx="2" fill="#C8A2C8"/>
                            <rect x="280" y="43" width="85" height="16" rx="4" fill="#C8A2C8"/>
                            <!-- Booking Hero / Table Grid Mock -->
                            <rect x="20" y="74" width="220" height="110" rx="6" fill="#1D182B"/>
                            <rect x="35" y="88" width="80" height="10" rx="2" fill="#E6E6FA"/>
                            <rect x="35" y="106" width="180" height="24" rx="4" fill="#2A223B"/>
                            <rect x="35" y="136" width="100" height="24" rx="4" fill="#C8A2C8"/>
                            <!-- Side Table Status Panel -->
                            <rect x="252" y="74" width="128" height="110" rx="6" fill="#1D182B"/>
                            <circle cx="280" cy="105" r="10" fill="#27C93F" opacity="0.8"/>
                            <circle cx="320" cy="105" r="10" fill="#FF5F56" opacity="0.8"/>
                            <circle cx="280" cy="145" r="10" fill="#27C93F" opacity="0.8"/>
                            <circle cx="320" cy="145" r="10" fill="#27C93F" opacity="0.8"/>
                        </svg>
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Restaurant Reservation System</h3>
                        <p class="project-desc">A database-integrated web application built to manage customer table bookings, schedule tracking, and real-time availability.</p>
                        <div class="project-tags">
                            <span class="tech-badge">PHP</span>
                            <span class="tech-badge">MySQL</span>
                            <span class="tech-badge">JavaScript</span>
                        </div>
                        <a href="https://github.com/honeylemorano" target="_blank" class="btn btn-secondary" style="font-size:0.85rem; padding: 8px 16px;">View source code ↗</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- TOOLKIT / SKILLS SECTION -->
    <section id="skills" class="section">
        <div class="container">
            <span class="section-tag">02 / Capabilities</span>
            <h2 class="section-title">Tech Toolkit</h2>

            <div class="toolkit-grid">
                <div class="toolkit-card">
                    <h3>Frontend</h3>
                    <ul class="toolkit-list">
                        <li>HTML5 & CSS3</li>
                        <li>JavaScript (ES6+)</li>
                        <li>Responsive Layouts</li>
                        <li>Modern UI Frameworks</li>
                    </ul>
                </div>
                <div class="toolkit-card">
                    <h3>Backend</h3>
                    <ul class="toolkit-list">
                        <li>PHP Development</li>
                        <li>MySQL Databases</li>
                        <li>RESTful Logic</li>
                        <li>CRUD Architecture</li>
                    </ul>
                </div>
                <div class="toolkit-card">
                    <h3>Desktop</h3>
                    <ul class="toolkit-list">
                        <li>C# Programming</li>
                        <li>Desktop GUI Apps</li>
                        <li>Object-Oriented Dev</li>
                    </ul>
                </div>
                <div class="toolkit-card">
                    <h3>Workflow</h3>
                    <ul class="toolkit-list">
                        <li>Git & GitHub</li>
                        <li>UI/UX Prototyping</li>
                        <li>VS Code Workflow</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- PROCESS SECTION -->
    <section id="process" class="section">
        <div class="container">
            <span class="section-tag">04 / Workflow</span>
            <h2 class="section-title">How I Build</h2>

            <div class="process-grid">
                <div class="process-card">
                    <span class="process-number">01</span>
                    <h3>Understand</h3>
                    <p>Defining problem statements, user requirements, and technical constraints before coding.</p>
                </div>
                <div class="process-card">
                    <span class="process-number">02</span>
                    <h3>Structure</h3>
                    <p>Architecting databases, wireframing user interfaces, and structuring clean project hierarchies.</p>
                </div>
                <div class="process-card">
                    <span class="process-number">03</span>
                    <h3>Build</h3>
                    <p>Writing clean, maintainable code using modern standards, frameworks, and responsive design.</p>
                </div>
                <div class="process-card">
                    <span class="process-number">04</span>
                    <h3>Refine</h3>
                    <p>Testing functionality, polishing UI aesthetics, and optimizing performance for live deployment.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTACT & FOOTER -->
    <section id="contact" class="contact-section container">
        <span class="section-tag">05 / Get In Touch</span>
        <h2 class="contact-heading">Have an idea? Let's make it work.</h2>
        <a href="mailto:jane@example.com" class="contact-email">jane.dev@example.com ↗</a>
        <div>
            <a href="https://github.com/honeylemorano" target="_blank" class="btn btn-primary">Visit My GitHub Profile ↗</a>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>© 2026 Jane — Built from scratch</p>
        </div>
    </footer>

</body>
</html>
