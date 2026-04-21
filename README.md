# my-portfoil
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Anushka Nagtode | Portfolio</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }

    body {
      font-family: 'Georgia', serif;
      background-color: #f9f6f1;
      color: #2d2d2d;
    }

    /* NAV */
    nav {
      background-color: #1a1a1a;
      padding: 16px 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 2px 10px rgba(0,0,0,0.3);
    }
    nav .logo {
      color: #e8c97e;
      font-size: 1.5rem;
      font-weight: bold;
      letter-spacing: 1px;
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 32px;
    }
    nav ul li a {
      color: #f0ece4;
      text-decoration: none;
      font-size: 0.95rem;
      letter-spacing: 0.5px;
      transition: color 0.3s;
    }
    nav ul li a:hover { color: #e8c97e; }

    /* HERO */
    .hero {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 80px;
      padding: 100px 60px;
      background: linear-gradient(135deg, #1a1a1a 0%, #3a3a3a 100%);
      color: white;
      min-height: 90vh;
    }
    .hero-photo-wrapper {
      position: relative;
    }
    .hero-photo {
      width: 240px;
      height: 240px;
      border-radius: 50%;
      object-fit: cover;
      border: 6px solid #e8c97e;
      box-shadow: 0 12px 40px rgba(0,0,0,0.5);
    }
    .hero-badge {
      position: absolute;
      bottom: 10px;
      right: 10px;
      background: #e8c97e;
      color: #1a1a1a;
      padding: 6px 14px;
      border-radius: 20px;
      font-size: 0.78rem;
      font-weight: bold;
    }
    .hero-text h1 {
      font-size: 3.2rem;
      color: #e8c97e;
      margin-bottom: 8px;
      line-height: 1.2;
    }
    .hero-text h2 {
      font-size: 1.1rem;
      font-weight: normal;
      color: #aaa;
      margin-bottom: 20px;
      letter-spacing: 3px;
      text-transform: uppercase;
    }
    .hero-text p {
      font-size: 1.05rem;
      color: #ccc;
      max-width: 460px;
      line-height: 1.8;
      margin-bottom: 30px;
    }
    .hero-btns {
      display: flex;
      gap: 16px;
    }
    .btn-primary {
      background: #e8c97e;
      color: #1a1a1a;
      padding: 12px 28px;
      border-radius: 30px;
      text-decoration: none;
      font-size: 0.95rem;
      font-weight: bold;
      transition: transform 0.2s;
    }
    .btn-primary:hover { transform: scale(1.05); }
    .btn-outline {
      border: 2px solid #e8c97e;
      color: #e8c97e;
      padding: 12px 28px;
      border-radius: 30px;
      text-decoration: none;
      font-size: 0.95rem;
      transition: background 0.3s;
    }
    .btn-outline:hover { background: #e8c97e; color: #1a1a1a; }

    /* SECTIONS */
    section { padding: 80px 100px; }
    section:nth-child(even) { background-color: #f0ece4; }

    .section-title {
      font-size: 2rem;
      color: #2d2d2d;
      margin-bottom: 10px;
      position: relative;
      display: inline-block;
    }
    .section-title::after {
      content: '';
      display: block;
      width: 60px;
      height: 4px;
      background-color: #e8c97e;
      margin-top: 8px;
      border-radius: 2px;
    }
    .section-subtitle {
      color: #777;
      font-size: 1rem;
      margin-bottom: 40px;
      margin-top: 8px;
    }

    /* ABOUT */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      margin-top: 40px;
      align-items: start;
    }
    .about-text p {
      font-size: 1.05rem;
      line-height: 1.9;
      color: #444;
      margin-bottom: 16px;
    }
    .about-info-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }
    .about-info-item {
      background: white;
      padding: 16px 20px;
      border-radius: 12px;
      border-left: 4px solid #e8c97e;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    }
    .about-info-item .label {
      font-size: 0.78rem;
      color: #999;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 4px;
    }
    .about-info-item .value {
      font-size: 0.95rem;
      font-weight: bold;
      color: #2d2d2d;
    }

    /* SKILLS */
    .skills-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
      margin-top: 40px;
    }
    .skill-card {
      background: white;
      border-radius: 16px;
      padding: 28px 24px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.06);
      border: 1px solid #eee;
      transition: transform 0.2s;
    }
    .skill-card:hover { transform: translateY(-4px); }
    .skill-icon {
      font-size: 2rem;
      margin-bottom: 12px;
    }
    .skill-card h3 {
      font-size: 1.1rem;
      margin-bottom: 8px;
      color: #2d2d2d;
    }
    .skill-card p {
      font-size: 0.88rem;
      color: #777;
      line-height: 1.6;
    }
    .skill-bar-wrapper {
      margin-top: 12px;
    }
    .skill-bar-bg {
      background: #f0ece4;
      border-radius: 10px;
      height: 8px;
      overflow: hidden;
    }
    .skill-bar-fill {
      height: 100%;
      border-radius: 10px;
      background: linear-gradient(90deg, #e8c97e, #c9a74e);
    }
    .skill-percent {
      font-size: 0.78rem;
      color: #999;
      text-align: right;
      margin-top: 4px;
    }

    /* EDUCATION */
    .timeline {
      margin-top: 40px;
      position: relative;
      padding-left: 40px;
    }
    .timeline::before {
      content: '';
      position: absolute;
      left: 8px;
      top: 0;
      bottom: 0;
      width: 3px;
      background: #e8c97e;
      border-radius: 2px;
    }
    .timeline-item {
      position: relative;
      margin-bottom: 36px;
    }
    .timeline-dot {
      position: absolute;
      left: -36px;
      top: 6px;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      background: #e8c97e;
      border: 3px solid white;
      box-shadow: 0 0 0 3px #e8c97e;
    }
    .timeline-card {
      background: white;
      border-radius: 14px;
      padding: 24px 28px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.06);
    }
    .timeline-year {
      font-size: 0.8rem;
      color: #e8c97e;
      font-weight: bold;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 6px;
    }
    .timeline-card h3 {
      font-size: 1.1rem;
      color: #2d2d2d;
      margin-bottom: 4px;
    }
    .timeline-card p {
      font-size: 0.9rem;
      color: #777;
      line-height: 1.6;
    }

    /* PROJECTS */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 28px;
      margin-top: 40px;
    }
    .project-card {
      background: white;
      border-radius: 16px;
      padding: 32px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.07);
      border-top: 5px solid #e8c97e;
      transition: transform 0.2s;
    }
    .project-card:hover { transform: translateY(-4px); }
    .project-number {
      font-size: 2.5rem;
      font-weight: bold;
      color: #f0ece4;
      margin-bottom: 12px;
    }
    .project-card h3 {
      font-size: 1.2rem;
      color: #2d2d2d;
      margin-bottom: 10px;
    }
    .project-card p {
      color: #666;
      line-height: 1.7;
      font-size: 0.95rem;
      margin-bottom: 16px;
    }
    .project-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }
    .tag {
      background: #f0ece4;
      color: #555;
      padding: 4px 14px;
      border-radius: 20px;
      font-size: 0.78rem;
      font-weight: bold;
    }

    /* ACHIEVEMENTS */
    .achievements-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
      margin-top: 40px;
    }
    .achievement-card {
      background: white;
      border-radius: 16px;
      padding: 28px 20px;
      text-align: center;
      box-shadow: 0 4px 16px rgba(0,0,0,0.06);
    }
    .achievement-icon { font-size: 2.2rem; margin-bottom: 12px; }
    .achievement-card h3 { font-size: 1rem; color: #2d2d2d; margin-bottom: 6px; }
    .achievement-card p { font-size: 0.85rem; color: #888; line-height: 1.5; }

    /* INTERESTS */
    .interests-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      margin-top: 40px;
    }
    .interest-item {
      background: white;
      border: 2px solid #e8c97e;
      border-radius: 30px;
      padding: 10px 24px;
      font-size: 0.95rem;
      color: #2d2d2d;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    /* CONTACT */
    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      margin-top: 40px;
    }
    .contact-info { display: flex; flex-direction: column; gap: 20px; }
    .contact-item {
      display: flex;
      align-items: center;
      gap: 16px;
      background: white;
      padding: 18px 22px;
      border-radius: 14px;
      box-shadow: 0 4px 14px rgba(0,0,0,0.06);
    }
    .contact-icon {
      width: 48px;
      height: 48px;
      background: #1a1a1a;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.3rem;
      flex-shrink: 0;
    }
    .contact-item .label { font-size: 0.78rem; color: #999; margin-bottom: 2px; }
    .contact-item .value { font-size: 0.95rem; font-weight: bold; color: #2d2d2d; }

    .contact-message {
      background: white;
      border-radius: 16px;
      padding: 36px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.06);
    }
    .contact-message h3 { font-size: 1.3rem; margin-bottom: 8px; color: #2d2d2d; }
    .contact-message p { color: #777; font-size: 0.95rem; line-height: 1.7; margin-bottom: 24px; }
    .contact-message .input-field {
      width: 100%;
      background: #f9f6f1;
      border: 1px solid #ddd;
      border-radius: 10px;
      padding: 12px 16px;
      font-size: 0.95rem;
      margin-bottom: 12px;
      font-family: Georgia, serif;
      color: #2d2d2d;
    }
    .contact-message textarea {
      width: 100%;
      background: #f9f6f1;
      border: 1px solid #ddd;
      border-radius: 10px;
      padding: 12px 16px;
      font-size: 0.95rem;
      margin-bottom: 16px;
      font-family: Georgia, serif;
      height: 100px;
      resize: none;
      color: #2d2d2d;
    }
    .send-btn {
      background: #1a1a1a;
      color: #e8c97e;
      border: none;
      border-radius: 30px;
      padding: 12px 32px;
      font-size: 0.95rem;
      font-weight: bold;
      cursor: pointer;
      width: 100%;
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 30px;
      background-color: #1a1a1a;
      color: #777;
      font-size: 0.9rem;
    }
    footer span { color: #e8c97e; }

    /* QUOTE BANNER */
    .quote-banner {
      background: #1a1a1a;
      padding: 60px 100px;
      text-align: center;
    }
    .quote-banner blockquote {
      font-size: 1.6rem;
      color: #e8c97e;
      font-style: italic;
      max-width: 700px;
      margin: 0 auto;
      line-height: 1.6;
    }
    .quote-banner p {
      color: #777;
      margin-top: 16px;
      font-size: 0.95rem;
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <div class="logo">AN.</div>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#education">Education</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#achievements">Achievements</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <div class="hero">
    <div class="hero-photo-wrapper">
      <img class="hero-photo" src="data:image/jpeg;base64,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" alt="Anushka Nagtode" />
      <span class="hero-badge">Open to Opportunities</span>
    </div>
    <div class="hero-text">
      <h1>Anushka<br>Nagtode</h1>
      <h2>Student &nbsp;|&nbsp; Developer &nbsp;|&nbsp; Designer</h2>
      <p>A passionate and curious student from Pimpri, Maharashtra who loves building things with technology. Eager to learn, create, and make a difference through UI/UX design and Python development.</p>
      <div class="hero-btns">
        <a href="#projects" class="btn-primary">View My Work</a>
        <a href="#contact" class="btn-outline">Contact Me</a>
      </div>
    </div>
  </div>

  <!-- ABOUT -->
  <section id="about">
    <div class="section-title">About Me</div>
    <p class="section-subtitle">Get to know me better</p>
    <div class="about-grid">
      <div class="about-text">
        <p>Hi! I'm <strong>Anushka Nagtode</strong>, a dedicated and enthusiastic student from Pimpri, Maharashtra with a deep passion for technology, design, and innovation.</p>
        <p>I believe that great technology starts with understanding people. That's why I am drawn to UI/UX design — crafting experiences that are not just functional but also intuitive and beautiful.</p>
        <p>On the technical side, I enjoy working with Python to build creative solutions like bots and automation tools. I am always looking for opportunities to learn new things, participate in hackathons, and collaborate with like-minded people.</p>
        <p>My goal is to build products that solve real problems for real people — especially in the Indian context where technology can create enormous social impact.</p>
      </div>
      <div class="about-info-grid">
        <div class="about-info-item">
          <div class="label">Name</div>
          <div class="value">Anushka Nagtode</div>
        </div>
        <div class="about-info-item">
          <div class="label">Role</div>
          <div class="value">Student & Developer</div>
        </div>
        <div class="about-info-item">
          <div class="label">Location</div>
          <div class="value">Pimpri, Maharashtra</div>
        </div>
        <div class="about-info-item">
          <div class="label">Email</div>
          <div class="value">anushkanagtode@gmail.com</div>
        </div>
        <div class="about-info-item">
          <div class="label">Phone</div>
          <div class="value">7028732649</div>
        </div>
        <div class="about-info-item">
          <div class="label">Languages</div>
          <div class="value">Marathi, Hindi, English</div>
        </div>
        <div class="about-info-item">
          <div class="label">Available For</div>
          <div class="value">Internships & Projects</div>
        </div>
        <div class="about-info-item">
          <div class="label">Status</div>
          <div class="value">Currently Studying</div>
        </div>
      </div>
    </div>
  </section>

  <!-- QUOTE BANNER -->
  <div class="quote-banner">
    <blockquote>"The best way to predict the future is to create it."</blockquote>
    <p>— The motto I live by</p>
  </div>

  <!-- SKILLS -->
  <section id="skills">
    <div class="section-title">My Skills</div>
    <p class="section-subtitle">Technologies and tools I work with</p>
    <div class="skills-container">
      <div class="skill-card">
        <div class="skill-icon">🐍</div>
        <h3>Python</h3>
        <p>Building bots, automation scripts, and backend logic using Python programming language.</p>
        <div class="skill-bar-wrapper">
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:70%"></div></div>
          <div class="skill-percent">70%</div>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🌐</div>
        <h3>HTML</h3>
        <p>Structuring web pages with clean, semantic HTML5 code for modern websites.</p>
        <div class="skill-bar-wrapper">
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:75%"></div></div>
          <div class="skill-percent">75%</div>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">💅</div>
        <h3>CSS</h3>
        <p>Styling websites with beautiful, responsive layouts using modern CSS techniques.</p>
        <div class="skill-bar-wrapper">
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:70%"></div></div>
          <div class="skill-percent">70%</div>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🎨</div>
        <h3>UI/UX Design</h3>
        <p>Designing user-friendly interfaces and experiences using Figma and Canva tools.</p>
        <div class="skill-bar-wrapper">
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:65%"></div></div>
          <div class="skill-percent">65%</div>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🤖</div>
        <h3>Bot Development</h3>
        <p>Creating automated bots for WhatsApp and other platforms using Python libraries.</p>
        <div class="skill-bar-wrapper">
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:60%"></div></div>
          <div class="skill-percent">60%</div>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">💡</div>
        <h3>Problem Solving</h3>
        <p>Analytical thinking and creative problem solving — especially for real-world challenges.</p>
        <div class="skill-bar-wrapper">
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:80%"></div></div>
          <div class="skill-percent">80%</div>
        </div>
      </div>
    </div>
  </section>

  <!-- EDUCATION -->
  <section id="education">
    <div class="section-title">Education</div>
    <p class="section-subtitle">My academic journey</p>
    <div class="timeline">
      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-card">
          <div class="timeline-year">2023 — Present</div>
          <h3>Bachelor's Degree — Currently Pursuing</h3>
          <p>Pursuing higher education with a focus on technology and computer applications. Actively participating in hackathons, workshops, and tech events to build practical skills alongside academics.</p>
        </div>
      </div>
      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-card">
          <div class="timeline-year">2021 — 2023</div>
          <h3>Higher Secondary Certificate (HSC)</h3>
          <p>Completed 12th standard with interest in science and computers. Developed foundational knowledge in mathematics and logical reasoning that forms the backbone of my technical skills today.</p>
        </div>
      </div>
      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-card">
          <div class="timeline-year">Before 2021</div>
          <h3>Secondary School Certificate (SSC)</h3>
          <p>Completed schooling from Pimpri, Maharashtra. Discovered an early interest in computers and technology during school years which motivated me to pursue a technical career path.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects">
    <div class="section-title">My Projects</div>
    <p class="section-subtitle">Things I have built and worked on</p>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-number">01</div>
        <h3>🤖 WhatsApp Bot Formation</h3>
        <p>Designed and developed a fully automated WhatsApp bot using Python. The bot can handle automated messaging, respond to user queries intelligently, send scheduled messages, and perform repetitive tasks — eliminating manual effort and showcasing practical Python automation skills.</p>
        <div class="project-tags">
          <span class="tag">Python</span>
          <span class="tag">Automation</span>
          <span class="tag">Bot Development</span>
          <span class="tag">API Integration</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-number">02</div>
        <h3>🍱 FoodSave — Hackathon Project</h3>
        <p>A social impact app concept developed for NIRMAAN 4.0 Hackathon under the Sustainability & Smart Cities track. FoodSave connects restaurants and hotels with nearby NGOs and individuals to redistribute leftover food — reducing food waste and fighting hunger in Indian cities.</p>
        <div class="project-tags">
          <span class="tag">UI/UX Design</span>
          <span class="tag">Figma</span>
          <span class="tag">Social Impact</span>
          <span class="tag">Hackathon</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-number">03</div>
        <h3>🌐 Personal Portfolio Website</h3>
        <p>Designed and built this personal portfolio website from scratch using HTML and CSS. The portfolio showcases my skills, education, projects and contact information in a clean, elegant, and fully responsive layout.</p>
        <div class="project-tags">
          <span class="tag">HTML</span>
          <span class="tag">CSS</span>
          <span class="tag">Web Design</span>
          <span class="tag">Responsive</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-number">04</div>
        <h3>🎨 UI/UX Design Practice</h3>
        <p>Ongoing practice of designing mobile app screens and web interfaces using Canva and Figma. Focus on user research, wireframing, prototyping, and creating clean visual hierarchies that improve user experience.</p>
        <div class="project-tags">
          <span class="tag">Figma</span>
          <span class="tag">Canva</span>
          <span class="tag">Wireframing</span>
          <span class="tag">Prototyping</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ACHIEVEMENTS -->
  <section id="achievements">
    <div class="section-title">Achievements</div>
    <p class="section-subtitle">Milestones and recognitions</p>
    <div class="achievements-grid">
      <div class="achievement-card">
        <div class="achievement-icon">🏆</div>
        <h3>Hackathon Participant</h3>
        <p>Participated in NIRMAAN 4.0 Hackathon with an innovative sustainability solution</p>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">🤖</div>
        <h3>Bot Developer</h3>
        <p>Successfully built and deployed a working WhatsApp automation bot using Python</p>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">🎨</div>
        <h3>UI/UX Designer</h3>
        <p>Designed multiple app screens and prototypes with professional level UI quality</p>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">📚</div>
        <h3>Self Learner</h3>
        <p>Self-taught Python, HTML, CSS and UI/UX design through online resources and practice</p>
      </div>
    </div>
  </section>

  <!-- INTERESTS -->
  <section>
    <div class="section-title">Interests</div>
    <p class="section-subtitle">Things I love beyond technology</p>
    <div class="interests-grid">
      <div class="interest-item">💻 Web Development</div>
      <div class="interest-item">🎨 UI/UX Design</div>
      <div class="interest-item">🤖 Automation & Bots</div>
      <div class="interest-item">🏆 Hackathons</div>
      <div class="interest-item">📱 Mobile App Design</div>
      <div class="interest-item">🌱 Social Impact Tech</div>
      <div class="interest-item">📖 Self Learning</div>
      <div class="interest-item">🎯 Problem Solving</div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="section-title">Contact Me</div>
    <p class="section-subtitle">Let's connect and build something great together</p>
    <div class="contact-grid">
      <div class="contact-info">
        <div class="contact-item">
          <div class="contact-icon">📧</div>
          <div>
            <div class="label">Email</div>
            <div class="value">anushkanagtode@gmail.com</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">📞</div>
          <div>
            <div class="label">Phone / WhatsApp</div>
            <div class="value">7028732649</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">📍</div>
          <div>
            <div class="label">Location</div>
            <div class="value">Pimpri, Maharashtra, India</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">💼</div>
          <div>
            <div class="label">LinkedIn</div>
            <div class="value">Coming Soon</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">🐙</div>
          <div>
            <div class="label">GitHub</div>
            <div class="value">Coming Soon</div>
          </div>
        </div>
      </div>
      <div class="contact-message">
        <h3>Send a Message</h3>
        <p>Have a project idea, internship opportunity, or just want to say hi? Feel free to reach out!</p>
        <input class="input-field" type="text" placeholder="Your Name" />
        <input class="input-field" type="email" placeholder="Your Email" />
        <textarea placeholder="Your Message..."></textarea>
        <button class="send-btn">Send Message ✉️</button>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>Designed & Built with ❤️ by <span>Anushka Nagtode</span> &copy; 2026 · Pimpri, Maharashtra</p>
    <p style="margin-top:8px;font-size:0.8rem;">Open to Internships · Hackathons · Collaborations</p>
  </footer>

</body>
</html>
