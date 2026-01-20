<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mitul Patel | Full Stack Developer</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
        rel="stylesheet">
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        :root {
            --primary: #8b5cf6;
            /* Violet */
            --primary-light: #a78bfa;
            --accent: #ec4899;
            /* Pink */
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

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.5rem 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(15, 15, 26, 0.8);
            backdrop-filter: var(--glass);
            border-bottom: 1px solid var(--border);
            z-index: 1000;
        }

        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: #f3f4f6;
            cursor: pointer;
            z-index: 1100;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            background: linear-gradient(90deg, #ec4899, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
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
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 0 8%;
            background: linear-gradient(135deg, rgba(139, 92, 246, 0.1), rgba(236, 72, 153, 0.1));
        }

        .hero-container {
            display: flex;
            justify-content: center;
            text-align: center;
            max-width: 1200px;
            margin: auto;
            width: 100%;
        }

        .hero-text h1 {
            font-size: clamp(3rem, 6vw, 5rem);
            font-weight: 800;
            line-height: 1.1;
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
            margin: 0 auto 2rem auto;
            max-width: 70%;
        }

        .hero-photo {
            text-align: center;
        }

        .hero-photo img {
            width: 350px;
            height: 350px;
            border-radius: 20px;
            object-fit: cover;
            border: 5px solid var(--primary);
            box-shadow: 0 20px 40px rgba(139, 92, 246, 0.3);
        }

        .btn {
            padding: 14px 32px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            display: inline-block;
            transition: 0.3s;
        }

        .btn-primary {
            background: linear-gradient(90deg, var(--primary), var(--accent));
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(139, 92, 246, 0.4);
        }

        section {
            padding: 100px 8%;
        }

        .section-title {
            text-align: center;
            font-size: 2.8rem;
            font-weight: 700;
            margin-bottom: 4rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            display: block;
            margin: 1rem auto;
            border-radius: 2px;
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .about-card {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid var(--border);
            backdrop-filter: var(--glass);
        }

        .about-card h3 {
            color: var(--primary);
            margin-bottom: 1rem;
            font-size: 1.4rem;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .skill-box {
            background: var(--card-bg);
            padding: 1rem;
            border-radius: 20px;
            border: 1px solid var(--border);
        }

        .skill-box h4 {
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .tag {
            background: rgba(139, 92, 246, 0.2);
            color: #fff;
            padding: 8px 10px;
            border-radius: 30px;
            font-size: 14px;
        }

        .experience-grid {
            display: grid;
            gap: 3rem;
            max-width: 900px;
            margin: auto;
        }

        .exp-item {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 20px;
            border-left: 4px solid var(--primary);
        }

        .exp-date {
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .projects-grid {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            column-gap: 2%;
            row-gap: 27px;
        }

        .project-card {
            width: 48%;
            background: var(--card-bg);
            border-radius: 20px;
            overflow: hidden;
            border: 1px solid var(--border);
            transition: 0.4s;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary);
        }

        .project-header {
            background: linear-gradient(135deg, var(--primary), var(--accent));
            padding: 1rem;
            color: white;
            text-align: center;
        }

        .project-body {
            padding: 1rem;
        }

        .project-body p {
            font-size: 15px;
        }

        .project-body .tags {
            margin: 10px 0;
        }

        .project-body a {
            text-decoration: none;
            color: #fff;
        }

        footer {
            background: var(--card-bg);
            padding: 80px 8% 40px;
            text-align: center;
            border-top: 1px solid var(--border);
        }

        .contact-email {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 2rem 0;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
        }

        .social-links a {
            color: var(--text-dim);
            transition: 0.3s;
        }

        .social-links a:hover {
            color: var(--primary);
            transform: scale(1.2);
        }

        @media (max-width: 992px) {
            .hero-container {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-photo img {
                width: 300px;
                height: 300px;
            }
            .section-title{
                margin-bottom: 2rem;
                font-size: 2.3rem;
            }
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
                /* Show button */
            }
            nav{
                padding: 1rem 5%;
            }
            .nav-links {
                position: fixed;
                top: 0;
                right: -100%;
                /* Hide off-screen */
                width: 80%;
                height: 100vh;
                background: rgba(15, 15, 26, 0.98);
                backdrop-filter: blur(20px);
                flex-direction: column;
                padding-top: 100px;
                align-items: center;
                transition: 0.4s ease-in-out;
                z-index: 1050;
            }

            .nav-links.active {
                right: 0;
                /* Slide in */
            }

            .project-card {
                width: 100%;
            }

            /* Prevent background scrolling when menu is open */
            body.no-scroll {
                overflow: hidden;
            }
            section {
                padding: 60px 5%;
            }
        }
        @media (max-width:568px){
            .contact-email{
                font-size: 20px;
                margin: 1rem 0;
            }
        }
    </style>
</head>

<body>

    <nav>
        <div class="logo">
            <a href="#home">
                Mitul Patel
            </a>
        </div>
        <button class="menu-toggle" id="menuToggle">
            <i data-lucide="menu" id="menuIcon"></i>
        </button>

        <ul class="nav-links" id="navLinks">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>

    </nav>

    <section class="hero" id="home">
        <div class="hero-container">
            <div class="hero-text">
                <h1>FULL STACK<br><span>DEVELOPER</span></h1>
                <p>8+ years building scalable web applications with Angular, .NET Core, and modern architecture.
                    Passionate about clean code and delivering high-impact solutions.</p>
                <a href="#contact" class="btn btn-primary">Get In Touch</a>
            </div>

        </div>
    </section>

    <section id="about">
        <h2 class="section-title">About Me</h2>
        <div class="about-grid">
            <div class="about-card">
                <h3>Profile</h3>
                <p>PPassionate Full stack development with 8+ years of experience in
                    developing web applications and backend systems. Skilled at
                    writing clear, concise code that is easy to maintain and
                    troubleshoot. Experienced in working with both small and large
                    teams across multiple projects and companies. Able to work
                    independently of remote locations or in office environments as
                    needed by the company.</p>
            </div>

            <div class="about-card">
                <h3>Awards & Certifications</h3>
                <ul>
                    <li>IBM CERTIFIED DATABASE
                        ASSOCIATE DB2 9 (Fundamentals)</li>
                    <li>IBM CEIBM CERTIFIED DEPLOYMENT
                        PROFESSIONAL TIVOLI DIRECTORY
                        SERVER V6.1 RTIFIED DATABASE
                        ASSOCIATE DB2 9</li>
                    <li>COMPARATIVE STUDY OF WEB
                        SEARCH ENGINES AND
                        USERCENTRIC SEARCH ENGINE</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="experience">
        <h2 class="section-title">Work Experience</h2>
        <div class="experience-grid">
            <div class="exp-item">
                <div class="exp-date">2018 — Present</div>
                <h3>Freelancing • Full Stack Developer</h3>
                <ul style="margin-top: 1rem; color: var(--text-dim);">
                    <li>Developed end-to-end web applications using Angular, React, .NET
                        Core, Node.js, and RESTful APIs.</li>
                    <li>Built scalable backend architectures, integrated third-party
                        services (Stripe, SendGrid, PSPDFKit), and optimized application
                        performance.</li>
                    <li>Collaborated with global clients, translated business requirements
                        into technical solutions, and ensured on-time delivery.</li>
                    <li>Maintained long-term client relationships through high-quality
                        code, clear communication, and reliable post-launch support.</li>
                </ul>
            </div>
            <div class="exp-item">
                <div class="exp-date">2014 — 2018</div>
                <h3>LaNet Software Solution Private Ltd • Senior Developer</h3>
                <ul style="margin-top: 1rem; color: var(--text-dim);">
                    <li>Led development of multiple enterprise web applications using
                        Angular.js, React.js, .NET, and Web API</li>
                    <li>Contributed to full development lifecycle: requirement gathering,
                        design, implementation, testing, and deployment.</li>
                    <li>Improved application performance and code quality through best
                        practices, modular architecture, and API optimization.</li>
                    <li>Worked closely with cross-functional teams to deliver robust,
                        scalable, and maintainable solutions.</li>
                    <li>Mentored junior developers and helped coordinate large-scale
                        team projects.</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="skills">
        <h2 class="section-title">Skills</h2>
        <div class="skills-grid">

            <div class="skill-box">
                <h4>Frontend</h4>
                <div class="tags">
                    <span class="tag">Angular</span>
                    <span class="tag">TypeScript</span>
                    <span class="tag">RxJS</span>
                    <span class="tag">NgRx</span>
                </div>
            </div>
            <div class="skill-box">
                <h4>Backend</h4>
                <div class="tags">
                    <span class="tag">ASP.NET Core</span>
                    <span class="tag">C#</span>
                    <span class="tag">Entity Framework</span>
                    <span class="tag">Node.js</span>
                </div>
            </div>
            <div class="skill-box">
                <h4>Architecture</h4>
                <div class="tags">
                    <span class="tag">Clean Architecture</span>
                    <span class="tag">Microservices</span>
                    <span class="tag">CQRS</span>
                </div>
            </div>
            <div class="skill-box">
                <h4>DevOps & Cloud</h4>
                <div class="tags">
                    <span class="tag">Docker</span>
                    <span class="tag">Kubernetes</span>
                    <span class="tag">Azure</span>
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <h2 class="section-title">Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-header">
                    <h3>Alundi</h3>
                </div>
                <div class="project-body">
                    <p>This is an employee management system where admin
                        can manage their employee details. he can share documents to a
                        group of employees. also, those employees have chat access they
                        can chat with each other. based on the role employee can perform
                        their activity. and they can update their profile detail also. In this
                        project, Customer admin can manage their employee details.</p>
                    <div class="tags">
                        <span class="tag">ANGULAR JS</span>

                    </div>
                    <a href="https://web.alundi.eu/#/login">View →</a>
                </div>
            </div>
            <div class="project-card">
                <div class="project-header">
                    <h3>Anython</h3>
                </div>
                <div class="project-body">
                    <p> Anython is an event-based fundraising platform that
                        allows users to create customized “Thons” to raise money through
                        activity-based pledges. Customers can organize events such as
                        Bike-a-Thon, Jog-a-Thon, or Free-Throw-a-Thon, where supporters
                        pledge donations based on completed activities (e.g., per mile, per
                        lap, or per shot). The platform enables users to manage events,
                        track progress, and collect pledges efficiently.</p>
                    <div class="tags">
                        <span class="tag">ASP.NET MVC</span>
                        <span class="tag">WEB API </span>
                        <span class="tag">ANGULARJS</span>
                        <span class="tag">JQUERY</span>
                        <span class="tag">JAVASCRIPT</span>
                        <span class="tag">BOOTSTRAP</span>
                    </div>
                    <a href="http://anython-staging.azurewebsites.net/Admin/index">View →</a>
                </div>
            </div>
            <div class="project-card">
                <div class="project-header">
                    <h3>IWriteMath Online</h3>
                </div>
                <div class="project-body">
                    <p> It's a nice SaaS based application for Digital learning
                        resources for at home and in the classroom at any place at any
                        time. Say goodbye to heavy books and find all your Math Workbooks
                        in one place online</p>
                    <div class="tags">
                        <span class="tag">Angular</span>
                        <span class="tag">.NET Core</span>
                        <span class="tag">Stripe</span>
                    </div>

                    <a href="https://avpbooks.com/digital/">View →</a>
                </div>
            </div>

            <div class="project-card">
                <div class="project-header">
                    <h3>Auger</h3>
                </div>
                <div class="project-body">
                    <p> Auger is a comprehensive platform designed to
                        streamline operational workflows, data management, and
                        communication processes for field service and insurance-related
                        services.</p>

                    <div class="tags">
                        <span class="tag">ASP.NET C# & VB</span>
                        <span class="tag">TELERIK RAD UI </span>
                        <span class="tag">PHP</span>
                        <span class="tag">AWS</span>
                        <span class="tag">SQL SERVER</span>
                        <span class="tag">JOTFORMS API</span>
                    </div>
                    <a href="https://auger.co.uk/">View →</a>
                </div>
            </div>
        </div>
    </section>

    <footer id="contact">
        <h2 class="section-title">Contact</h2>
        <div class="contact-email">mitulpatel1150@gmail.com</div>
        <p style="color: var(--text-dim); max-width: 600px; margin: auto;">Available for freelance and full-time
            opportunities</p>
        <div class="social-links">
            <a href="https://www.linkedin.com/in/mitul-patel-dev/"><i data-lucide="linkedin"></i></a>
        </div>
        <p style="margin-top: 4rem; color: var(--text-dim);">© 2025 Mitul Patel</p>
    </footer>

    <script>
        lucide.createIcons();
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');
        const body = document.body;

        menuToggle.addEventListener('click', () => {
            // Toggle classes
            navLinks.classList.toggle('active');
            body.classList.toggle('no-scroll');

            // Switch between Menu and X icon
            const isOpen = navLinks.classList.contains('active');
            menuToggle.innerHTML = isOpen
                ? '<i data-lucide="x"></i>'
                : '<i data-lucide="menu"></i>';

            // Refresh Lucide icons
            lucide.createIcons();
        });

        // Auto-close menu when a link is clicked
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                body.classList.remove('no-scroll');
                menuToggle.innerHTML = '<i data-lucide="menu"></i>';
                lucide.createIcons();
            });
        });
    </script>
</body>

</html>
