<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }
    body {
      background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
      color: #f1f1f1;
      line-height: 1.6;
      padding: 2rem;
    }
    header {
      text-align: center;
      margin-bottom: 2rem;
    }
    h1 {
      font-size: 2.5rem;
      font-weight: 800;
    }
    section {
      margin-bottom: 2rem;
      background: rgba(255, 255, 255, 0.05);
      padding: 1.5rem;
      border-radius: 10px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    }
    h2 {
      font-size: 1.5rem;
      color: #00d4ff;
      margin-bottom: 1rem;
    }
    ul, p {
      margin-bottom: 1rem;
    }
    a {
      color: #00ffe1;
      text-decoration: none;
    }
    .cv-download {
      display: inline-block;
      padding: 0.5rem 1rem;
      background: #00d4ff;
      color: #000;
      font-weight: bold;
      border-radius: 5px;
      text-decoration: none;
    }
    form {
      display: flex;
      flex-direction: column;
    }
    input, textarea {
      margin-bottom: 1rem;
      padding: 0.75rem;
      border: none;
      border-radius: 5px;
      font-size: 1rem;
    }
    button {
      padding: 0.75rem;
      background: #00d4ff;
      color: #000;
      font-weight: bold;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <header>
    <h1>👨‍💻 Kefa Mwai's Portfolio</h1>
    <p>Developer • Creator • Problem Solver</p>
  </header>

  <section>
    <h2>About Me</h2>
    <p>I am a passionate developer driven by curiosity and creativity. I love solving real-world problems through code and building things that make an impact.</p>
  </section>

  <section>
    <h2>Programming Languages</h2>
    <ul>
      <li>JavaScript</li>
      <li>Python</li>
      <li>HTML/CSS</li>
      <li>SQL</li>
      <li>Java</li>
    </ul>
  </section>

  <section>
    <h2>Educational Background</h2>
    <p>BSc. in Computer Science, Tech University</p>
    <a class="cv-download" href="/files/Kefa Mwai_CV.pdf" download>📄 Download My CV</a>
  </section>

  <section>
    <h2>Interests</h2>
    <p>I am especially excited about AI, cybersecurity, and automation. I enjoy learning emerging tech trends and contributing to open-source projects.</p>
  </section>

  <section>
    <h2>Projects</h2>
    <ul>
      <li><strong><a href="https://github.com/mwaikefa05/project1">Project One</a></strong>: A smart to-do app with built-in productivity analysis.</li>
      <li><strong><a href="https://github.com/mwaikefa05/project2">Project Two</a></strong>: A chatbot powered by AI for real-time assistance.</li>
      <li><strong><a href="https://github.com/mwaikefa05/project3">Project Three</a></strong>: A weather dashboard using API integrations and geolocation.</li>
    </ul>
  </section>

  <section>
    <h2>Contact Me</h2>
    <form action="/submit-form" method="POST">
      <input type="text" name="name" placeholder="Your Name" required />
      <input type="email" name="email" placeholder="Your Email" required />
      <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>
</body>
</html>
