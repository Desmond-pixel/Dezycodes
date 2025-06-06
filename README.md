<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Desmond — Fullstack Designer</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    :root {
      --bg: #0e0e0e;
      --fg: #ffffff;
      --accent: #00ffc8;
    }

    body.light {
      --bg: #ffffff;
      --fg: #111111;
      --accent: #ff7a00;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: var(--bg);
      color: var(--fg);
      transition: background 0.4s, color 0.4s;
    }

    nav {
      display: flex;
      justify-content: space-between;
      padding: 20px 30px;
      background: transparent;
    }

    nav a {
      color: var(--accent);
      text-decoration: none;
      font-weight: bold;
      font-size: 1.1rem;
    }

    .hero {
      text-align: center;
      padding: 60px 20px;
    }

    .hero h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    .hero p {
      font-size: 1.2rem;
      color: var(--accent);
    }

    .section {
      max-width: 900px;
      margin: 40px auto;
      padding: 0 20px;
    }

    .skills {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 15px;
      margin-top: 20px;
    }

    .skills div {
      background: rgba(255,255,255,0.05);
      padding: 15px;
      border-radius: 8px;
      text-align: center;
      transition: background 0.3s, transform 0.3s;
      box-shadow: 0 0 10px rgba(0, 255, 200, 0.2);
    }

    .skills div:hover {
      background: var(--accent);
      color: #000;
      transform: scale(1.05);
    }

    .toggle {
      position: fixed;
      top: 75px;
      right: 15px;
      background: var(--accent);
      border: none;
      padding: 10px;
      border-radius: 6px;
      cursor: pointer;
      font-weight: bold;
    }

    footer {
      text-align: center;
      padding: 30px;
      font-size: 0.9rem;
      opacity: 0.6;
    }
  </style>
</head>
<body>
  <nav>
    <a href="wend.html">🏠 Home</a>
    <a href="port.html">💼 Portfolio</a>
  </nav>

  <button class="toggle" onclick="toggleTheme()">🌓 Theme</button>

  <div class="hero">
    <h1>Hello, I'm Desmond</h1>
    <p>Fullstack Designer & Creative Developer</p>
  </div>

  <div class="section">
    <h2>👨‍💻 About Me</h2>
    <p>I design beautiful interfaces and develop powerful web applications. With 5+ years of experience, I blend design and development to build interactive, intuitive, and impactful digital experiences.</p>
  </div>

  <div class="section">
    <h2>⚙️ Skills</h2>
    <div class="skills">
      <div>HTML / CSS</div>
      <div>JavaScript / TypeScript</div>
      <div>React / Vue</div>
      <div>Node.js / Python</div>
      <div>Figma / Adobe XD</div>
      <div>MongoDB / MySQL</div>
    </div>
  </div>

  <footer>&copy; 2025 Desmond • Fullstack Designer</footer>

  <script>
    const isLight = localStorage.getItem("theme") === "light";
    if (isLight) document.body.classList.add("light");

    function toggleTheme() {
      document.body.classList.toggle("light");
      localStorage.setItem("theme", document.body.classList.contains("light") ? "light" : "dark");
    }
  </script>
</body>
</html>



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Portfolio — Desmond</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    :root {
      --bg: #0e0e0e;
      --fg: #ffffff;
      --accent: #00ffc8;
    }

    body.light {
      --bg: #ffffff;
      --fg: #111111;
      --accent: #ff7a00;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: var(--bg);
      color: var(--fg);
      transition: background 0.4s, color 0.4s;
    }

    nav {
      display: flex;
      justify-content: space-between;
      padding: 20px 30px;
    }

    nav a {
      color: var(--accent);
      text-decoration: none;
      font-weight: bold;
    }

    .section {
      max-width: 900px;
      margin: 40px auto;
      padding: 0 20px;
    }

    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }

    .project {
      background: rgba(255,255,255,0.05);
      padding: 20px;
      border-radius: 10px;
      transition: 0.3s;
      box-shadow: 0 0 15px rgba(0, 255, 200, 0.15);
    }

    .project:hover {
      background: var(--accent);
      color: #000;
      transform: scale(1.03);
    }

    .testimonials, .contact {
      margin-top: 50px;
    }

    .toggle {
      position: fixed;
      top: 75px;
      right: 15px;
      background: var(--accent);
      border: none;
      padding: 10px;
      border-radius: 6px;
      cursor: pointer;
      font-weight: bold;
    }

    footer {
      text-align: center;
      padding: 30px;
      font-size: 0.9rem;
      opacity: 0.6;
    }
  </style>
</head>
<body>
  <nav>
    <a href="wend.html">🏠 Home</a>
    <a href="port.html">💼 Portfolio</a>
  </nav>

  <button class="toggle" onclick="toggleTheme()">🌓 Theme</button>

  <div class="section">
    <h2>💼 Projects</h2>
    <div class="projects">
      <div class="project">
        <h3>Our Projects</h3>
        <p>Custom analytics platform with React, Chart.js, and Tailwind CSS</p>
      </div>
      <div class="project">
        <h3>E-commerce UI</h3>
        <p>Built responsive shop with cart, filters, Stripe payments.</p>
      </div>
      <div class="project">
        <h3>Portfolio Website</h3>
        <p>Animated, mobile-first personal site with dark mode toggle.</p>
      </div>
    </div>
  </div>

  <div class="section testimonials">
    <h2>💬 Testimonials</h2>
    <p>“Desmond took our web presence to the next level!” — Creative Studio</p>
    <p>“A developer with the mind of a designer. Highly recommended.” — CEO, TechNova</p>
  </div>

  <div class="section contact">
    <h2>📬 Contact</h2>
    <p>Email: <a href="ezikev3@gmail.com" style="color: var(--accent)">desmond@gmail.com</a></p>
    <p>GitHub: <a href="https://desmond-pixel.github.io/Fullstack-Designer" style="color: var(--accent)">github.com/desmond</a></p>
  
  </div>

  <footer>&copy; 2025 Desmond • Fullstack Designer</footer>

  <script>
    const isLight = localStorage.getItem("theme") === "light";
    if (isLight) document.body.classList.add("light");

    function toggleTheme() {
      document.body.classList.toggle("light");
      localStorage.setItem("theme", document.body.classList.contains("light") ? "light" : "dark");
    }
  </script>
</body>
</html>
