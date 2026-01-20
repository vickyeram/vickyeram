<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Vikram Sisodiya | Senior Mobile & Web Developer</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --primary: #8b5cf6;
  --accent: #ec4899;
  --bg: #0f0f1a;
  --card: rgba(30,30,50,0.6);
  --border: rgba(139,92,246,0.3);
  --text: #f3f4f6;
  --muted: #9ca3af;
}

* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'Poppins', sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
}

a { color: var(--primary); text-decoration: none; }

nav {
  position: fixed;
  top: 0;
  width: 100%;
  padding: 16px 8%;
  background: rgba(15,15,26,0.9);
  border-bottom: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 100;
}

.logo {
  font-size: 22px;
  font-weight: 800;
  background: linear-gradient(90deg,var(--accent),#fff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.nav-links {
  display: flex;
  gap: 24px;
  list-style: none;
}

section {
  padding: 100px 8%;
}

.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.hero h1 {
  font-size: clamp(36px,6vw,64px);
  font-weight: 800;
}

.hero h1 span {
  background: linear-gradient(90deg,var(--primary),var(--accent));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero p {
  max-width: 720px;
  margin: 20px auto;
  color: var(--muted);
}

.btn {
  display: inline-block;
  margin-top: 24px;
  padding: 14px 34px;
  border-radius: 50px;
  background: linear-gradient(90deg,var(--primary),var(--accent));
  color: #fff;
  font-weight: 600;
}

.section-title {
  text-align: center;
  font-size: 36px;
  margin-bottom: 50px;
}

.section-title::after {
  content: "";
  width: 80px;
  height: 4px;
  background: linear-gradient(90deg,var(--primary),var(--accent));
  display: block;
  margin: 16px auto 0;
  border-radius: 2px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(300px,1fr));
  gap: 30px;
}

.card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 24px;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.tag {
  background: rgba(139,92,246,0.2);
  padding: 8px 14px;
  border-radius: 30px;
  font-size: 14px;
}

.exp {
  border-left: 4px solid var(--primary);
}

footer {
  text-align: center;
  padding: 80px 8% 40px;
  border-top: 1px solid var(--border);
}

footer .email {
  font-size: 26px;
  font-weight: 700;
  background: linear-gradient(90deg,var(--primary),var(--accent));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

@media(max-width:768px){
  nav { padding: 16px 5%; }
  section { padding: 80px 5%; }
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
  <div>
    <h1>Senior Mobile &<br><span>Web Developer</span></h1>
    <p>
      8+ years of experience building scalable Flutter, Angular, React,
      and ASP .NET Core applications for global clients.
    </p>
    <a href="#contact" class="btn">Get In Touch</a>
  </div>
</section>

<section id="about">
  <h2 class="section-title">About Me</h2>
  <div class="grid">
    <div class="card">
      <h3>Profile</h3>
      <p>
        Senior Mobile & Web Developer specializing in Flutter (iOS & Android),
        Angular, React, and ASP .NET Core. Strong experience with REST APIs,
        cloud platforms, secure payments, and scalable architecture.
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
  <div class="grid">
    <div class="card exp">
      <h3>Freelancer / Team Lead</h3>
      <p><em>2024 – Present</em></p>
      <ul>
        <li>End-to-end Flutter & Web development</li>
        <li>Architecture, development, deployment</li>
      </ul>
    </div>
    <div class="card exp">
      <h3>Natrix Software Pvt. Ltd.</h3>
      <p><em>2013 – 2024</em></p>
      <ul>
        <li>Enterprise mobile & web applications</li>
        <li>Flutter, Angular, React, ASP .NET Core</li>
      </ul>
    </div>
  </div>
</section>

<section id="skills">
  <h2 class="section-title">Skills</h2>
  <div class="grid">
    <div class="card">
      <h3>Mobile</h3>
      <div class="tags">
        <span class="tag">Flutter</span>
        <span class="tag">Dart</span>
        <span class="tag">iOS</span>
        <span class="tag">Android</span>
      </div>
    </div>
    <div class="card">
      <h3>Web</h3>
      <div class="tags">
        <span class="tag">Angular</span>
        <span class="tag">React</span>
        <span class="tag">HTML</span>
        <span class="tag">CSS</span>
      </div>
    </div>
    <div class="card">
      <h3>Backend & Cloud</h3>
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
  <div class="grid">
    <div class="card">
      <h3>Colorex App</h3>
      <p>Flutter-based eCommerce app for New Zealand trade industry.</p>
    </div>
    <div class="card">
      <h3>Super Kids App</h3>
      <p>Educational app with animations and performance optimization.</p>
    </div>
    <div class="card">
      <h3>Mazoom Invitations</h3>
      <p>Digital invitation & RSVP platform with QR codes.</p>
    </div>
  </div>
</section>

<footer id="contact">
  <h2 class="section-title">Contact</h2>
  <div class="email">vickeyram61@gmail.com</div>
  <p style="margin-top:20px;color:var(--muted);">
    Available for freelance & remote opportunities
  </p>
  <p style="margin-top:40px;color:var(--muted);">
    © 2026 Vikram Sisodiya
  </p>
</footer>

</body>
</html>
