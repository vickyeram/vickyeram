<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vikram Sisodiya | Senior Mobile & Web Developer</title>

    <!-- Google Font -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
          rel="stylesheet">

    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <style>
        :root {
            --primary: #8b5cf6;
            --accent: #ec4899;
            --bg: #0f0f1a;
            --card-bg: rgba(30, 30, 50, 0.6);
            --border: rgba(139, 92, 246, 0.3);
            --text-main: #f3f4f6;
            --text-dim: #9ca3af;
            --glass: blur(16px);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: var(--bg);
            color: var(--text-main);
        }

        /* NAV */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.5rem 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(15, 15, 26, 0.85);
            backdrop-filter: var(--glass);
            border-bottom: 1px solid var(--border);
            z-index: 1000;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            background: linear-gradient(90deg, var(--accent), #fff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-main);
            text-decoration: none;
            font-weight: 500;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        /* HERO */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 0 8%;
            background: linear-gradient(135deg,
                rgba(139, 92, 246, 0.1),
                rgba(236, 72, 153, 0.1));
        }

        .hero-text {
            max-width: 900px;
            margin: auto;
            text-align: center;
        }

        .hero-text h1 {
            font-size: clamp(3rem, 6vw, 5rem);
            font-weight: 800;
            margin-bottom: 1rem;
        }

        .hero-text h1 span {
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-text p {
            font-size: 1.2rem;
            color: var(--text-dim);
            max-width: 750px;
            margin: auto;
        }

        .btn {
            display: inline-block;
            margin-top: 2rem;
            padding: 14px 36px;
            border-radius: 50px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            color: #fff;
            text-decoration: none;
            font-weight: 600;
        }

        /* SECTIONS */
        section {
            padding: 100px 8%;
        }

        .section-title {
            text-align: center;
            font-size: 2.8rem;
            font-weight: 700;
            margin-bottom: 3.5rem;
        }

        .section-title::after {
            content: '';
            width: 90px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            display: block;
            margin: 1rem auto;
        }

        /* CARDS */
        .card {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid var(--border);
            backdrop-filter: var(--glass);
        }

        /* ABOUT */
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        /* SKILLS */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .tag {
            background: rgba(139, 92, 246, 0.2);
            padding: 8px 12px;
            border-radius: 30px;
            font-size: 14px;
        }

        /* EXPERIENCE */
        .experience-grid {
            max-width: 900px;
            margin: auto;
            display: grid;
            gap: 2.5rem;
        }

        .exp-item {
            border-left: 4px solid var(--primary);
        }

        /* PROJECTS */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .project-header {
            background: linear-gradient(135deg, var(--primary), var(--accent));
            padding: 1rem;
            text-align: center;
            font-weight: 600;
        }

        /* FOOTER */
        footer {
            padding: 80px 8% 40px;
            text-align: center;
            border-top: 1px solid var(--border);
        }

        .contact-email {
            font-size: 2.2rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    </style>
</head>

<body>

<nav>
    <div class="logo">Vikram Sisodiya</div>
    <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>

<section class="hero" id="home">
    <div class="hero-text">
        <h1>Senior Mobile &<br><span>Web Developer</span></h1>
        <p>
            8+ years of experience delivering high-performance Flutter, Angular,
            React, and ASP .NET Core applications for global clients.
        </p>
        <a href="#contact" class="btn">Get In Touch</a>
    </div>
</section>

<section id="about">
    <h2 class="section-title">About Me</h2>
    <div class="about-grid">
        <div class="card">
            <h3>Profile</h3>
            <p>
                Senior Mobile & Web Developer with expertise in Flutter (iOS & Android),
                Angular, React, and ASP .NET Core. Strong background in scalable
                architecture, REST APIs, cloud services, secure payments, and UI/UX.
            </p>
        </div>
        <div class="card">
            <h3>Education</h3>
            <p>
                <strong>MCA</strong> – Gujarat Technological University (2009–2012)<br>
                <strong>BCA</strong> – Veer Narmad South Gujarat University (2005–2008)
            </p>
        </div>
    </div>
</section>

<section id="experience">
    <h2 class="section-title">Experience</h2>
    <div class="experience-grid">
        <div class="card exp-item">
            <h4>Freelancer / Team Lead</h4>
            <p><em>2024 – Present</em></p>
            <ul>
                <li>Leading Flutter & Web projects end-to-end</li>
                <li>Architecture, development & cloud deployment</li>
            </ul>
        </div>
        <div class="card exp-item">
            <h4>Natrix Software Pvt. Ltd.</h4>
            <p><em>2013 – 2024</em></p>
            <ul>
                <li>Enterprise mobile & web solutions</li>
                <li>Flutter, Angular, React, ASP .NET Core</li>
            </ul>
        </div>
    </div>
</section>

<section id="skills">
    <h2 class="section-title">Skills</h2>
    <div class="skills-grid">
        <div class="card">
            <h4>Mobile</h4>
            <div class="tags">
                <span class="tag">Flutter</span>
                <span class="tag">Dart</span>
                <span class="tag">iOS</span>
                <span class="tag">Android</span>
            </div>
        </div>
        <div class="card">
            <h4>Web</h4>
            <div class="tags">
                <span class="tag">Angular</span>
                <span class="tag">React</span>
                <span class="tag">HTML</span>
                <span class="tag">CSS</span>
            </div>
        </div>
        <div class="card">
            <h4>Backend & Cloud</h4>
            <div class="tags">
                <span class="tag">ASP .NET Core</span>
                <span class="tag">SQL Server</span>
                <span class="tag">Azure</span>
                <span class="tag">AWS</span>
            </div>
        </div>
    </div>
</section>

<section id="projects">
    <h2 class="section-title">Projects</h2>
    <div class="projects-grid">
        <div class="card">
            <div class="project-header">Colorex App</div>
            <p>Flutter-based eCommerce app for New Zealand trade industry.</p>
        </div>
        <div class="card">
            <div class="project-header">Super Kids App</div>
            <p>Educational app with animations and optimized performance.</p>
        </div>
        <div class="card">
            <div class="project-header">Mazoom Invitations</div>
            <p>Digital invitation & RSVP platform with QR codes.</p>
        </div>
    </div>
</section>

<footer id="contact">
    <h2 class="section-title">Contact</h2>
    <div class="contact-email">vickeyram61@gmail.com</div>
    <p>Available for freelance & remote opportunities</p>
    <p style="margin-top:3rem;">© 2026 Vikram Sisodiya</p>
</footer>

<script>
    lucide.createIcons();
</script>

</body>
</html>
