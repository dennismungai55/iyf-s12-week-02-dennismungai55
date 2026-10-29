# iyf-s12-week-02-dennismungai55

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>My Portfolio | Web Developer</title>
  <meta
    name="description"
    content="My personal portfolio showcasing my skills, projects, and contact information."
  >

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link
    href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;500;600;700&family=Poppins:wght@400;500;600;700&display=swap"
    rel="stylesheet"
  >

  <style>
    /* 1. Design system */
    :root {
      --color-primary: #2563EB;
      --color-secondary: #14B8A6;
      --color-background: #F8FAFC;
      --color-text: #0F172A;
      --color-muted: #64748B;
      --color-primary-light: #93C5FD;
      --color-primary-dark: #1D4ED8;
      --color-white: #FFFFFF;
      --color-border: #E2E8F0;

      --font-xs: 0.75rem;
      --font-sm: 0.875rem;
      --font-base: 1rem;
      --font-lg: 1.125rem;
      --font-xl: 1.25rem;
      --font-2xl: 1.5rem;
      --font-3xl: 1.875rem;
      --font-4xl: 2.25rem;

      --radius-sm: 8px;
      --radius-md: 16px;
      --radius-lg: 24px;

      --shadow-card: 0 10px 30px rgba(15, 23, 42, 0.06);
      --container-width: 1100px;
    }

    /* 2. Base styles */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 90px;
    }

    body {
      font-family: "Open Sans", sans-serif;
      font-size: var(--font-base);
      line-height: 1.7;
      color: var(--color-text);
      background: var(--color-background);
    }

    h1, h2, h3, h4 {
      font-family: "Poppins", sans-serif;
      line-height: 1.2;
      font-weight: 600;
    }

    h1 {
      font-size: clamp(2.4rem, 6vw, 4rem);
    }

    h2 {
      font-size: var(--font-3xl);
      margin-bottom: 1rem;
    }

    h3 {
      font-size: var(--font-xl);
    }

    p {
      color: var(--color-muted);
    }

    a {
      color: var(--color-primary);
      text-decoration: none;
    }

    a:hover {
      color: var(--color-primary-dark);
    }

    a:focus-visible,
    button:focus-visible {
      outline: 3px solid var(--color-secondary);
      outline-offset: 4px;
    }

    .container {
      width: min(90%, var(--container-width));
      margin-inline: auto;
    }

    .section {
      padding: 80px 0;
    }

    .section-heading {
      margin-bottom: 2.5rem;
    }

    .section-heading p {
      max-width: 600px;
    }

    .eyebrow {
      color: var(--color-primary);
      font-size: var(--font-sm);
      font-weight: 700;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-bottom: 1rem;
    }

    /* 3. Navigation */
    .navbar {
      position: sticky;
      top: 0;
      z-index: 10;
      background: rgba(255, 255, 255, 0.95);
      border-bottom: 1px solid var(--color-border);
      backdrop-filter: blur(12px);
    }

    .nav-content {
      min-height: 72px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
    }

    .logo {
      font-family: "Poppins", sans-serif;
      font-size: var(--font-xl);
      font-weight: 700;
      color: var(--color-text);
    }

    .logo span {
      color: var(--color-primary);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      list-style: none;
    }

    .nav-links a {
      color: var(--color-text);
      font-size: var(--font-sm);
      font-weight: 600;
    }

    .nav-links a:hover {
      color: var(--color-primary);
    }

    /* 4. Buttons */
    .button {
      display: inline-flex;
      justify-content: center;
      align-items: center;
      gap: 0.5rem;
      padding: 0.8rem 1.3rem;
      border-radius: var(--radius-sm);
      font-weight: 700;
      transition: transform 0.2s, background 0.2s;
    }

    .button:hover {
      transform: translateY(-2px);
    }

    .button-primary {
      color: var(--color-white);
      background: var(--color-primary);
    }

    .button-primary:hover {
      color: var(--color-white);
      background: var(--color-primary-dark);
    }

    .button-outline {
      border: 1px solid var(--color-border);
      color: var(--color-text);
      background: var(--color-white);
    }

    /* 5. Hero */
    .hero {
      padding: 100px 0;
      background:
        radial-gradient(
          circle at 85% 15%,
          rgba(147, 197, 253, 0.25),
          transparent 35%
        ),
        var(--color-background);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      align-items: center;
      gap: 3rem;
    }

    .hero-description {
      max-width: 580px;
      margin: 1.5rem 0 2rem;
      font-size: var(--font-lg);
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .code-card {
      padding: 1.5rem;
      border-radius: var(--radius-lg);
      background: #0F172A;
      box-shadow: var(--shadow-card);
      overflow: hidden;
    }

    .code-dots {
      display: flex;
      gap: 7px;
      margin-bottom: 1.5rem;
    }

    .code-dots span {
      width: 11px;
      height: 11px;
      border-radius: 50%;
      background: #64748B;
    }

    .code-dots span:first-child {
      background: #F87171;
    }

    .code-dots span:nth-child(2) {
      background: #FBBF24;
    }

    .code-dots span:nth-child(3) {
      background: #34D399;
    }

    .code-card pre {
      color: #CBD5E1;
      white-space: pre-wrap;
      overflow-wrap: anywhere;
      font-family: Consolas, monospace;
      font-size: var(--font-sm);
      line-height: 2;
    }

    .code-highlight {
      color: #93C5FD;
    }

    .code-green {
      color: #5EEAD4;
    }

    /* 6. About */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      align-items: start;
    }

    .about-text p + p {
      margin-top: 1rem;
    }

    .about-note {
      padding: 1.5rem;
      background: var(--color-white);
      border: 1px solid var(--color-border);
      border-left: 4px solid var(--color-secondary);
      border-radius: var(--radius-md);
    }

    .about-note h3 {
      margin-bottom: 0.75rem;
    }

    /* 7. Skills */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.5rem;
    }

    .skill-card,
    .project-card {
      padding: 1.5rem;
      border: 1px solid var(--color-border);
      border-radius: var(--radius-md);
      background: var(--color-white);
      box-shadow: var(--shadow-card);
    }

    .skill-card h3 {
      margin-bottom: 0.75rem;
    }

    .skill-card p {
      font-size: var(--font-sm);
    }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-top: 1rem;
    }

    .tag {
      padding: 0.35rem 0.7rem;
      border-radius: 999px;
      background: #EFF6FF;
      color: var(--color-primary-dark);
      font-size: var(--font-xs);
      font-weight: 700;
    }

    /* 8. Projects */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1.5rem;
    }

    .project-card {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
    }

    .project-number {
      display: inline-block;
      margin-bottom: 1rem;
      color: var(--color-secondary);
      font-family: "Poppins", sans-serif;
      font-size: var(--font-2xl);
      font-weight: 700;
    }

    .project-card h3 {
      margin-bottom: 0.75rem;
    }

    .project-card p {
      margin-bottom: 1rem;
    }

    .project-card .skill-tags {
      margin-top: auto;
      margin-bottom: 1.25rem;
    }

    .project-link {
      font-weight: 700;
    }

    /* 9. Contact */
    .contact-box {
      padding: 3rem;
      text-align: center;
      border-radius: var(--radius-lg);
      background: #EFF6FF;
    }

    .contact-box h2 {
      margin-bottom: 1rem;
    }

    .contact-box p {
      max-width: 580px;
      margin: 0 auto 1.5rem;
    }

    /* 10. Footer */
    .footer {
      padding: 2rem 0;
      border-top: 1px solid var(--color-border);
      background: var(--color-white);
    }

    .footer-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
    }

    .footer p {
      font-size: var(--font-sm);
    }

    .social-links {
      display: flex;
      gap: 1rem;
      font-size: var(--font-sm);
      font-weight: 600;
    }

    /* 11. Responsive design */
    @media (max-width: 800px) {
      .hero-grid,
      .about-grid {
        grid-template-columns: 1fr;
      }

      .hero {
        padding: 70px 0;
      }

      .skills-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .nav-links {
        gap: 0.8rem;
      }

      .nav-links a {
        font-size: var(--font-xs);
      }
    }

    @media (max-width: 560px) {
      .section {
        padding: 60px 0;
      }

      .nav-content {
        align-items: flex-start;
        flex-direction: column;
        justify-content: center;
        padding: 1rem 0;
      }

      .nav-links {
        flex-wrap: wrap;
      }

      .skills-grid,
      .projects-grid {
        grid-template-columns: 1fr;
      }

      .contact-box {
        padding: 2rem 1.25rem;
      }

      .footer-content {
        flex-direction: column;
        align-items: flex-start;
      }
    }
  </style>
</head>

<body>
  <!-- Navigation -->
  <header class="navbar">
    <nav class="container nav-content" aria-label="Main navigation">
      <a class="logo" href="#home">My<span>Portfolio.</span></a>

      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <!-- Hero section -->
    <section class="hero" id="home">
      <div class="container hero-grid">
        <div>
          <p class="eyebrow">Hello, welcome to my portfolio</p>

          <h1>Hi, I'm Alex Morgan.<br>
            I build for the web.</h1>

          <p class="hero-description">
            I'm a beginner web developer learning to create clean,
            responsive, and user-friendly websites with HTML and CSS.
          </p>

          <div class="hero-buttons">
            <a class="button button-primary" href="#projects">
              View My Projects
            </a>
            <a class="button button-outline" href="#contact">
              Contact Me
            </a>
          </div>
        </div>

        <div class="code-card" aria-label="Example code snippet">
          <div class="code-dots">
            <span></span><span></span><span></span>
          </div>

          <pre><span class="code-highlight">const</span> developer = {
  name: <span class="code-green">"Alex Morgan"</span>,
  skills: [
    "HTML",
    "CSS",
    "JavaScript"
  ],
  goal: <span class="code-green">"Build great websites"</span>,
  learning: <span class="code-green">true</span>
};</pre>
        </div>
      </div>
    </section>

    <!-- About section -->
    <section class="section" id="about">
      <div class="container about-grid">
        <div class="about-text">
          <p class="eyebrow">A little about me</p>
          <h2>Turning ideas into websites</h2>

          <p>
            I'm learning web development and enjoy turning ideas into
            useful digital experiences. I'm currently focusing on writing
            semantic HTML and styling pages with modern CSS.
          </p>

          <p>
            My goal is to keep improving, build practical projects, and
            create websites that work well on phones, tablets, and desktops.
          </p>
        </div>

        <div class="about-note">
          <h3>What I'm working toward</h3>
          <p>
            Building a strong foundation in frontend development,
            responsive layouts, accessibility, and clean code.
          </p>
        </div>
      </div>
    </section>

    <!-- Skills section -->
    <section class="section" id="skills">
      <div class="container">
        <div class="section-heading">
          <p class="eyebrow">My toolkit</p>
          <h2>Skills I'm developing</h2>
          <p>
            The technologies and concepts I'm using as I grow as a developer.
          </p>
        </div>

        <div class="skills-grid">
          <article class="skill-card">
            <h3>HTML</h3>
            <p>Structuring accessible, meaningful web pages.</p>
            <div class="skill-tags">
              <span class="tag">Semantic HTML</span>
              <span class="tag">Forms</span>
            </div>
          </article>

          <article class="skill-card">
            <h3>CSS</h3>
            <p>Creating layouts, visual styles, and responsive designs.</p>
            <div class="skill-tags">
              <span class="tag">Flexbox</span>
              <span class="tag">Grid</span>
              <span class="tag">Responsive</span>
            </div>
          </article>

          <article class="skill-card">
            <h3>JavaScript</h3>
            <p>Learning to add interaction and dynamic behavior.</p>
            <div class="skill-tags">
              <span class="tag">Fundamentals</span>
              <span class="tag">DOM basics</span>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- Projects section -->
    <section class="section" id="projects">
      <div class="container">
        <div class="section-heading">
          <p class="eyebrow">What I've built</p>
          <h2>Featured projects</h2>
          <p>
            A few examples of projects you can replace with your own work.
          </p>
        </div>

        <div class="projects-grid">
          <article class="project-card">
            <span class="project-number">01</span>
            <h3>Personal Portfolio</h3>
            <p>
              A responsive website introducing me, my skills, and my
              projects in one place.
            </p>

            <div class="skill-tags">
              <span class="tag">HTML</span>
              <span class="tag">CSS</span>
              <span class="tag">Responsive Design</span>
            </div>

            <a class="project-link" href="#contact">
              Ask about this project →
            </a>
          </article>

          <article class="project-card">
            <span class="project-number">02</span>
            <h3>Product Landing Page</h3>
            <p>
              A clean landing page with a clear heading, product details,
              and a call-to-action.
            </p>

            <div class="skill-tags">
              <span class="tag">HTML</span>
              <span class="tag">CSS Grid</span>
              <span class="tag">Typography</span>
            </div>

            <a class="project-link" href="#contact">
              Ask about this project →
            </a>
          </article>
        </div>
      </div>
    </section>

    <!-- Contact section -->
    <section class="section" id="contact">
      <div class="container">
        <div class="contact-box">
          <p class="eyebrow">Let's connect</p>
          <h2>Have a project in mind?</h2>

          <p>
            I'm open to learning opportunities, collaboration, and
            conversations about web development.
          </p>

          <a
            class="button button-primary"
            href="mailto:hello@example.com"
          >
            Email Me
          </a>
        </div>
      </div>
    </section>
  </main>

  <!-- Footer -->
  <footer class="footer">
    <div class="container footer-content">
      <p>
        © <span id="year"></span> Alex Morgan. Built with HTML and CSS.
      </p>

      <div class="social-links">
        <a href="https://github.com/" target="_blank"
           rel="noopener noreferrer">GitHub</a>
        <a href="https://www.linkedin.com/" target="_blank"
           rel="noopener noreferrer">LinkedIn</a>
      </div>
    </div>
  </footer>

  <script>
    document.getElementById("year").textContent =
      new Date().getFullYear();
  </script>
</body>
</html>
