<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jayesh Jagan Dhumal | Frontend & Python Full-Stack Developer</title>
    <!-- Google Fonts: Poppins -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --dark-bg: #0f172a;
            --light-bg: #f8fafc;
            --card-bg: #ffffff;
            --text-main: #1e293b;
            --text-muted: #64748b;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--light-bg);
            color: var(--text-main);
            line-height: 1.6;
        }

        /* Navbar */
        nav {
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .nav-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            list-style: none;
        }

        .nav-links a {
            color: #e2e8f0;
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #38bdf8;
        }

        /* Hero / Header Section */
        header {
            background: linear-gradient(135deg, #0f172a 0%, #1e3a8a 100%);
            color: white;
            text-align: center;
            padding: 80px 20px;
        }

        header h1 {
            font-size: 2.8rem;
            font-weight: 700;
            margin-bottom: 10px;
            letter-spacing: 0.5px;
        }

        header .subtitle {
            font-size: 1.2rem;
            color: #38bdf8;
            font-weight: 500;
            margin-bottom: 15px;
        }

        header .location {
            font-size: 0.95rem;
            color: #cbd5e1;
            margin-bottom: 25px;
        }

        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 10px 24px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-primary {
            background-color: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }

        .btn-outline {
            border: 1.5px solid #38bdf8;
            color: #38bdf8;
        }

        .btn-outline:hover {
            background-color: #38bdf8;
            color: #0f172a;
            transform: translateY(-2px);
        }

        /* Main Container */
        .container {
            max-width: 1050px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        /* Section Styling */
        .section-card {
            background: var(--card-bg);
            border-radius: 16px;
            padding: 35px;
            margin-bottom: 30px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
            border: 1px solid #e2e8f0;
            transition: transform 0.3s ease;
        }

        .section-title {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--dark-bg);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 10px;
        }

        .section-title i {
            color: var(--primary);
        }

        /* Skills Badges */
        .skill-group {
            margin-bottom: 18px;
        }

        .skill-group h4 {
            font-size: 1rem;
            color: var(--text-muted);
            margin-bottom: 10px;
        }

        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .badge {
            background: #eff6ff;
            color: var(--primary);
            padding: 6px 16px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 500;
            border: 1px solid #bfdbfe;
            transition: all 0.2s;
        }

        .badge:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-2px);
        }

        .badge.learning {
            background: #fef3c7;
            color: #b45309;
            border-color: #fde68a;
        }

        .badge.learning:hover {
            background: #d97706;
            color: white;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .project-card {
            background: #f8fafc;
            border: 1px solid #e2e8f0;
            border-radius: 12px;
            padding: 25px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(37, 99, 235, 0.1);
            border-color: var(--primary);
        }

        .project-card h3 {
            font-size: 1.15rem;
            color: var(--dark-bg);
            margin-bottom: 8px;
        }

        .tech-stack {
            font-size: 0.8rem;
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 12px;
        }

        .project-card p {
            font-size: 0.92rem;
            color: var(--text-muted);
            margin-bottom: 20px;
        }

        .project-link {
            color: var(--primary);
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        .project-link:hover {
            text-decoration: underline;
        }

        /* Education Timeline */
        .edu-item {
            padding-left: 20px;
            border-left: 3px solid var(--primary);
            margin-bottom: 20px;
        }

        .edu-item:last-child {
            margin-bottom: 0;
        }

        .edu-item h3 {
            font-size: 1.1rem;
            color: var(--dark-bg);
        }

        .edu-item p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Contact Section */
        .contact-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-between;
            align-items: center;
        }

        .contact-info p {
            margin-bottom: 8px;
            font-size: 0.95rem;
        }

        .contact-info i {
            color: var(--primary);
            width: 22px;
        }

        .social-links {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .social-btn {
            background: var(--dark-bg);
            color: white;
            padding: 10px 20px;
            border-radius: 8px;
            text-decoration: none;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: background 0.3s;
        }

        .social-btn:hover {
            background: var(--primary);
        }

        /* Footer */
        footer {
            background: var(--dark-bg);
            color: #94a3b8;
            text-align: center;
            padding: 25px 20px;
            font-size: 0.9rem;
            margin-top: 40px;
        }

        @media (max-width: 600px) {
            header h1 { font-size: 2rem; }
            .nav-links { gap: 15px; font-size: 0.85rem; }
        }
    </style>
</head>
<body>

    <!-- Sticky Navigation -->
    <nav>
        <ul class="nav-links">
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero Header -->
    <header>
        <h1>Jayesh Jagan Dhumal</h1>
        <p class="subtitle">Frontend Web Developer (Fresher) | Pursuing Python Full-Stack</p>
        <p class="location"><i class="fas fa-map-marker-alt"></i> Thane, Maharashtra, India</p>
        <div class="hero-btns">
            <a href="#projects" class="btn btn-primary"><i class="fas fa-code"></i> View Projects</a>
            <a href="#contact" class="btn btn-outline"><i class="fas fa-envelope"></i> Contact Me</a>
        </div>
    </header>

    <div class="container">
        
        <!-- About Section -->
        <section id="about" class="section-card">
            <h2 class="section-title"><i class="fas fa-user"></i> About Me</h2>
            <p>Hello! I am <strong>Jayesh Jagan Dhumal</strong>, a final-year B.Sc. IT student from Thane. I am currently pursuing my <strong>Python Full-Stack Development</strong> training at <strong>NetTech India, Thane</strong>. I have successfully completed my frontend training in <strong>HTML, CSS, JavaScript, jQuery, and React</strong>, and I love building clean, responsive, and user-friendly web applications.</p>
        </section>

        <!-- Technical Skills -->
        <section id="skills" class="section-card">
            <h2 class="section-title"><i class="fas fa-laptop-code"></i> Technical Skills</h2>
            
            <div class="skill-group">
                <h4>Frontend Technologies</h4>
                <div class="badges">
                    <span class="badge">HTML5</span>
                    <span class="badge">CSS3</span>
                    <span class="badge">JavaScript (ES6)</span>
                    <span class="badge">jQuery</span>
                    <span class="badge">React</span>
                </div>
            </div>

            <div class="skill-group">
                <h4>Currently Learning (Backend & Database)</h4>
                <div class="badges">
                    <span class="badge learning">Python</span>
                    <span class="badge learning">SQL</span>
                    <span class="badge learning">Backend Development</span>
                </div>
            </div>

            <div class="skill-group">
                <h4>Tools & Environment</h4>
                <div class="badges">
                    <span class="badge">Visual Studio Code</span>
                    <span class="badge">Git</span>
                    <span class="badge">GitHub</span>
                    <span class="badge">GitHub Pages</span>
                    <span class="badge">XAMPP</span>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects" class="section-card">
            <h2 class="section-title"><i class="fas fa-folder-open"></i> Frontend & Practice Projects</h2>
            
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card">
                    <div>
                        <h3>1. JDtify Web Music Player</h3>
                        <div class="tech-stack">HTML • CSS • JavaScript</div>
                        <p>A responsive web music player with custom audio controls, play/pause functionality, and an interactive playlist interface.</p>
                    </div>
                    <a href="https://github.com/jayeshdhumal355" target="_blank" class="project-link"><i class="fab fa-github"></i> GitHub Link <i class="fas fa-arrow-right"></i></a>
                </div>

                <!-- Project 2 -->
                <div class="project-card">
                    <div>
                        <h3>2. Live Weather App</h3>
                        <div class="tech-stack">HTML • CSS • JavaScript • API</div>
                        <p>A web application that fetches and displays real-time temperature, humidity, and weather updates for any city.</p>
                    </div>
                    <a href="https://jayeshdhumal355.github.io/weather-app/" target="_blank" class="project-link"><i class="fas fa-external-link-alt"></i> Live Preview / GitHub <i class="fas fa-arrow-right"></i></a>
                </div>

                <!-- Project 3 -->
                <div class="project-card">
                    <div>
                        <h3>3. Personal Portfolio Website</h3>
                        <div class="tech-stack">HTML • CSS • JS • React</div>
                        <p>Responsive personal portfolio showcasing frontend skills, technical stack, and academic projects.</p>
                    </div>
                    <a href="https://jayeshdhumal355.github.io/digital-hub/" target="_blank" class="project-link"><i class="fab fa-github"></i> Live Portfolio <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
        </section>

        <!-- Education Section -->
        <section id="education" class="section-card">
            <h2 class="section-title"><i class="fas fa-graduation-cap"></i> Education & Training</h2>
            
            <div class="edu-item">
                <h3>Python Full-Stack Development Course</h3>
                <p>NetTech India, Thane <em>(Ongoing - Frontend Completed)</em></p>
            </div>

            <div class="edu-item">
                <h3>Bachelor of Science in Information Technology (B.Sc. IT - Final Year)</h3>
                <p>Shantaram Bhu Gholap Arts, Science and Gotiram Bhu Pawar Commerce College, Shivle</p>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="section-card">
            <h2 class="section-title"><i class="fas fa-paper-plane"></i> Get In Touch</h2>
            <div class="contact-grid">
                <div class="contact-info">
                    <p><i class="fas fa-envelope"></i> <strong>Email:</strong> <a href="mailto:jayeshdhumal355@gmail.com" style="color: var(--primary); text-decoration: none;">jayeshdhumal355@gmail.com</a></p>
                    <p><i class="fas fa-phone"></i> <strong>Mobile:</strong> <a href="tel:+917774044098" style="color: var(--primary); text-decoration: none;">+91 7774044098</a></p>
                    <p><i class="fas fa-map-pin"></i> <strong>Location:</strong> Thane, Maharashtra, India</p>
                </div>
                <div class="social-links">
                    <a href="tel:+917774044098" class="social-btn" style="background: var(--primary);"><i class="fas fa-phone-alt"></i> Call Now</a>
                    <a href="https://github.com/jayeshdhumal355" target="_blank" class="social-btn"><i class="fab fa-github"></i> GitHub</a>
                    <a href="https://www.linkedin.com/feed?contentTrackingId=MDclgP4LToy0qLX0bt2%2FCg%3D%3D&viewName=premium-nav-upsell-text&upsellOrderOrigin=Tracking%3Av1%3Apremium_nav_upsell_text%3ANav%3AIn-Product" target="_blank" class="social-btn"><i class="fab fa-linkedin"></i> LinkedIn</a>
                </div>
            </div>
        </section>

    </div>

    <!-- Footer -->
    <footer>
        <p>© 2026 Jayesh Jagan Dhumal | Built with ❤️ & Code</p>
    </footer>

</body>
</html>
