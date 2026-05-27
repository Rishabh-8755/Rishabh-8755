<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Rishabh Pathak — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,400&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d1117;
    --bg2: #161b22;
    --bg3: #21262d;
    --border: rgba(255,255,255,0.08);
    --border-hover: rgba(255,255,255,0.18);
    --text: #e6edf3;
    --text2: #8b949e;
    --text3: #6e7681;
    --accent: #58a6ff;
    --accent2: #f0883e;
    --accent3: #3fb950;
    --purple: #bc8cff;
    --pink: #ff7eb6;
    --yellow: #f9c74f;
    --card-bg: #161b22;
    --card-hover: #1c2230;
    --radius: 12px;
    --radius-sm: 8px;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    max-width: 860px;
    margin: 0 auto;
    padding: 2rem 1.5rem 4rem;
    line-height: 1.6;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 3rem 1rem 2rem;
    position: relative;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: 0; left: 50%;
    transform: translateX(-50%);
    width: 600px; height: 300px;
    background: radial-gradient(ellipse at 50% 0%, rgba(88,166,255,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .avatar-ring {
    width: 88px; height: 88px;
    border-radius: 50%;
    background: linear-gradient(135deg, #58a6ff, #bc8cff, #ff7eb6);
    padding: 3px;
    margin: 0 auto 1.2rem;
    display: flex; align-items: center; justify-content: center;
  }
  .avatar-inner {
    width: 100%; height: 100%;
    border-radius: 50%;
    background: var(--bg2);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Syne', sans-serif;
    font-size: 2rem; font-weight: 800;
    color: var(--accent);
    letter-spacing: -1px;
  }
  .hero h1 {
    font-family: 'Syne', sans-serif;
    font-size: 2rem; font-weight: 800;
    letter-spacing: -0.5px;
    color: var(--text);
    margin-bottom: 0.4rem;
  }
  .hero .tagline {
    font-size: 1rem;
    color: var(--text2);
    font-weight: 400;
    margin-bottom: 1.2rem;
  }
  .typing-row {
    display: flex;
    justify-content: center;
    gap: 8px;
    flex-wrap: wrap;
    margin-bottom: 1.5rem;
  }
  .badge-pill {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11.5px;
    padding: 4px 12px;
    border-radius: 20px;
    border: 1px solid var(--border);
    color: var(--text2);
    background: var(--bg2);
    transition: all 0.2s;
  }
  .badge-pill:hover {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(88,166,255,0.08);
    transform: translateY(-2px);
  }
  .badge-pill.purple:hover { border-color: var(--purple); color: var(--purple); background: rgba(188,140,255,0.08); }
  .badge-pill.orange:hover { border-color: var(--accent2); color: var(--accent2); background: rgba(240,136,62,0.08); }
  .badge-pill.green:hover { border-color: var(--accent3); color: var(--accent3); background: rgba(63,185,80,0.08); }

  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 2rem 0;
  }

  /* ── SECTION TITLES ── */
  .section-label {
    font-family: 'Syne', sans-serif;
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--text3);
    margin-bottom: 1rem;
  }
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 1rem;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  /* ── ABOUT GRID ── */
  .about-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(190px, 1fr));
    gap: 10px;
    margin-bottom: 2rem;
  }
  .about-item {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: var(--radius-sm);
    padding: 0.9rem 1rem;
    transition: all 0.2s;
    display: flex;
    align-items: flex-start;
    gap: 10px;
  }
  .about-item:hover {
    background: var(--card-hover);
    border-color: var(--border-hover);
    transform: translateY(-2px);
  }
  .about-icon {
    font-size: 1.1rem;
    flex-shrink: 0;
    margin-top: 1px;
  }
  .about-text {
    font-size: 13px;
    color: var(--text2);
    line-height: 1.4;
  }

  /* ── FEATURED PROJECTS ── */
  .projects-wrapper {
    background: linear-gradient(135deg, #0f1923 0%, #131d2e 50%, #0f1923 100%);
    border: 1px solid rgba(88,166,255,0.15);
    border-radius: 16px;
    padding: 1.8rem;
    margin-bottom: 2rem;
    position: relative;
    overflow: hidden;
  }
  .projects-wrapper::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 220px; height: 220px;
    background: radial-gradient(circle, rgba(88,166,255,0.08) 0%, transparent 70%);
    pointer-events: none;
  }
  .projects-wrapper::after {
    content: '';
    position: absolute;
    bottom: -60px; left: -40px;
    width: 200px; height: 200px;
    background: radial-gradient(circle, rgba(188,140,255,0.07) 0%, transparent 70%);
    pointer-events: none;
  }
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 14px;
    position: relative;
    z-index: 1;
  }
  .proj-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: var(--radius);
    padding: 1.2rem;
    cursor: default;
    transition: background 0.25s, border-color 0.25s, transform 0.25s, box-shadow 0.25s;
    position: relative;
    overflow: hidden;
  }
  .proj-card::before {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: var(--radius);
    background: linear-gradient(135deg, transparent, rgba(255,255,255,0.03));
    opacity: 0;
    transition: opacity 0.25s;
  }
  .proj-card:hover {
    background: rgba(255,255,255,0.08);
    border-color: rgba(88,166,255,0.35);
    transform: translateY(-4px);
    box-shadow: 0 8px 32px rgba(88,166,255,0.12), 0 2px 8px rgba(0,0,0,0.4);
  }
  .proj-card:hover::before { opacity: 1; }
  .proj-card.purple:hover { border-color: rgba(188,140,255,0.4); box-shadow: 0 8px 32px rgba(188,140,255,0.1), 0 2px 8px rgba(0,0,0,0.4); }
  .proj-card.green:hover { border-color: rgba(63,185,80,0.4); box-shadow: 0 8px 32px rgba(63,185,80,0.1), 0 2px 8px rgba(0,0,0,0.4); }

  .proj-category {
    font-size: 10.5px;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent2);
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .proj-category .dot {
    width: 5px; height: 5px;
    border-radius: 50%;
    background: currentColor;
    display: inline-block;
  }
  .proj-category.purple { color: var(--purple); }
  .proj-category.green { color: var(--accent3); }

  .proj-title {
    font-family: 'Syne', sans-serif;
    font-size: 15px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 6px;
    line-height: 1.3;
  }
  .proj-desc {
    font-size: 12.5px;
    color: var(--text2);
    margin-bottom: 14px;
    line-height: 1.55;
  }
  .proj-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
  }
  .proj-tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    color: var(--text3);
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 20px;
    padding: 2px 8px;
    transition: all 0.2s;
  }
  .proj-card:hover .proj-tag {
    color: var(--text2);
    border-color: rgba(255,255,255,0.18);
  }

  /* ── STATS GRID ── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 12px;
    margin-bottom: 2rem;
  }
  .stat-img-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 4px;
    overflow: hidden;
    transition: all 0.25s;
    text-align: center;
  }
  .stat-img-card:hover {
    border-color: rgba(88,166,255,0.3);
    transform: translateY(-3px);
    box-shadow: 0 6px 24px rgba(88,166,255,0.1);
  }
  .stat-img-card img {
    width: 100%;
    border-radius: 10px;
    display: block;
  }

  /* ── TECH STACK ── */
  .tech-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 2rem;
  }
  .tech-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: var(--radius-sm);
    padding: 6px 12px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    color: var(--text2);
    transition: all 0.2s;
    cursor: default;
  }
  .tech-badge:hover {
    border-color: var(--border-hover);
    color: var(--text);
    background: var(--bg3);
    transform: translateY(-2px);
  }
  .tech-badge img { width: 16px; height: 16px; object-fit: contain; }

  /* ── CONNECT ── */
  .connect-row {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
  }
  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border-radius: var(--radius-sm);
    font-family: 'DM Sans', sans-serif;
    font-size: 14px;
    font-weight: 500;
    text-decoration: none;
    transition: all 0.2s;
    border: 1px solid var(--border);
  }
  .connect-btn.email {
    background: rgba(240,136,62,0.1);
    color: var(--accent2);
    border-color: rgba(240,136,62,0.25);
  }
  .connect-btn.email:hover {
    background: rgba(240,136,62,0.18);
    border-color: rgba(240,136,62,0.5);
    transform: translateY(-2px);
    box-shadow: 0 4px 16px rgba(240,136,62,0.15);
  }
  .connect-btn.linkedin {
    background: rgba(88,166,255,0.1);
    color: var(--accent);
    border-color: rgba(88,166,255,0.25);
  }
  .connect-btn.linkedin:hover {
    background: rgba(88,166,255,0.18);
    border-color: rgba(88,166,255,0.5);
    transform: translateY(-2px);
    box-shadow: 0 4px 16px rgba(88,166,255,0.15);
  }

  /* ── FOOTER ── */
  .footer-note {
    text-align: center;
    font-size: 12px;
    color: var(--text3);
    margin-top: 2.5rem;
    font-family: 'JetBrains Mono', monospace;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .hero, .about-grid, .projects-wrapper, .stats-grid, .tech-grid, .connect-row {
    animation: fadeUp 0.5s ease both;
  }
  .about-grid { animation-delay: 0.05s; }
  .projects-wrapper { animation-delay: 0.1s; }
  .stats-grid { animation-delay: 0.15s; }
  .tech-grid { animation-delay: 0.2s; }
  .connect-row { animation-delay: 0.25s; }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="avatar-ring"><div class="avatar-inner">RP</div></div>
  <h1>Rishabh Pathak</h1>
  <p class="tagline">B.Tech CSE Student · Java Developer · Open Source Enthusiast</p>
  <div class="typing-row">
    <span class="badge-pill">☕ Java Developer</span>
    <span class="badge-pill purple">🧠 DSA Problem Solver</span>
    <span class="badge-pill orange">🤖 AI / ML Explorer</span>
    <span class="badge-pill green">🌱 Open Source Contributor</span>
  </div>
  <img src="https://komarev.com/ghpvc/?username=Rishabh-8755&label=Profile+Views&color=0d1117&style=flat" alt="profile views" style="opacity:0.5; height:20px;"/>
</div>

<div class="divider"></div>

<!-- ABOUT -->
<div class="section-label">🚀 About Me</div>
<div class="about-grid">
  <div class="about-item"><span class="about-icon">🎓</span><span class="about-text">B.Tech Computer Science Student</span></div>
  <div class="about-item"><span class="about-icon">☕</span><span class="about-text">Passionate Java + DSA Problem Solver</span></div>
  <div class="about-item"><span class="about-icon">🔐</span><span class="about-text">Building Security & Real-World Projects</span></div>
  <div class="about-item"><span class="about-icon">🤖</span><span class="about-text">Exploring AI / Machine Learning</span></div>
  <div class="about-item"><span class="about-icon">🌱</span><span class="about-text">Open Source Contributor in Progress</span></div>
</div>

<div class="divider"></div>

<!-- FEATURED PROJECTS -->
<div class="section-label">🔥 Featured Projects</div>
<div class="projects-wrapper">
  <div class="projects-grid">

    <div class="proj-card">
      <div class="proj-category"><span class="dot"></span>P2P · Security</div>
      <div class="proj-title">⛓ PeerLink</div>
      <div class="proj-desc">Direct encrypted peer-to-peer file sharing system built with Java TCP sockets and a modern Next.js frontend.</div>
      <div class="proj-tags">
        <span class="proj-tag">Java</span>
        <span class="proj-tag">Next.js</span>
        <span class="proj-tag">TCP Sockets</span>
        <span class="proj-tag">TypeScript</span>
        <span class="proj-tag">TailwindCSS</span>
      </div>
    </div>

    <div class="proj-card purple">
      <div class="proj-category purple"><span class="dot"></span>AI · Machine Learning</div>
      <div class="proj-title">❤️ Heart Disease Prediction</div>
      <div class="proj-desc">AI/ML based disease risk prediction system with a clean web interface for real-time patient input and output.</div>
      <div class="proj-tags">
        <span class="proj-tag">Python</span>
        <span class="proj-tag">ML</span>
        <span class="proj-tag">HTML</span>
        <span class="proj-tag">CSS</span>
        <span class="proj-tag">JavaScript</span>
      </div>
    </div>

    <div class="proj-card green">
      <div class="proj-category green"><span class="dot"></span>DSA · Algorithms</div>
      <div class="proj-title">☕ Java DSA Practice</div>
      <div class="proj-desc">Structured algorithms and data structures practice repository — solving real problems with clean Java code.</div>
      <div class="proj-tags">
        <span class="proj-tag">Java</span>
        <span class="proj-tag">Data Structures</span>
        <span class="proj-tag">Algorithms</span>
      </div>
    </div>

  </div>
</div>

<div class="divider"></div>

<!-- GITHUB STATS -->
<div class="section-label">📊 GitHub Stats</div>
<div class="stats-grid">
  <div class="stat-img-card">
    <img src="https://github-readme-stats.vercel.app/api?username=Rishabh-8755&show_icons=true&theme=github_dark&hide_border=true&bg_color=161b22&title_color=58a6ff&icon_color=bc8cff&text_color=8b949e" alt="GitHub Stats"/>
  </div>
  <div class="stat-img-card">
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=Rishabh-8755&theme=github-dark-blue&hide_border=true&background=161b22&ring=58a6ff&fire=f0883e&currStreakLabel=58a6ff" alt="Streak Stats"/>
  </div>
  <div class="stat-img-card" style="grid-column: 1 / -1; max-width: 360px; margin: 0 auto; width: 100%;">
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Rishabh-8755&layout=compact&theme=github_dark&hide_border=true&bg_color=161b22&title_color=58a6ff&text_color=8b949e" alt="Top Languages"/>
  </div>
</div>

<div class="divider"></div>

<!-- TECH STACK -->
<div class="section-label">🛠 Tech Stack</div>
<div class="tech-grid">
  <span class="tech-badge"><img src="https://img.shields.io/badge/-ED8B00?style=flat&logo=openjdk&logoColor=white&label=" alt=""/>Java</span>
  <span class="tech-badge"><img src="https://img.shields.io/badge/-3776AB?style=flat&logo=python&logoColor=white&label=" alt=""/>Python</span>
  <span class="tech-badge"><img src="https://img.shields.io/badge/-F7DF1E?style=flat&logo=javascript&logoColor=black&label=" alt=""/>JavaScript</span>
  <span class="tech-badge"><img src="https://img.shields.io/badge/-000000?style=flat&logo=nextdotjs&logoColor=white&label=" alt=""/>Next.js</span>
  <span class="tech-badge"><img src="https://img.shields.io/badge/-339933?style=flat&logo=nodedotjs&logoColor=white&label=" alt=""/>Node.js</span>
  <span class="tech-badge"><img src="https://img.shields.io/badge/-06B6D4?style=flat&logo=tailwindcss&logoColor=white&label=" alt=""/>TailwindCSS</span>
  <span class="tech-badge">🤖 Machine Learning</span>
  <span class="tech-badge"><img src="https://img.shields.io/badge/-F05032?style=flat&logo=git&logoColor=white&label=" alt=""/>Git</span>
  <span class="tech-badge"><img src="https://img.shields.io/badge/-181717?style=flat&logo=github&logoColor=white&label=" alt=""/>GitHub</span>
</div>

<div class="divider"></div>

<!-- CONNECT -->
<div class="section-label">🌐 Connect With Me</div>
<div class="connect-row">
  <a href="mailto:rp8585881@gmail.com" class="connect-btn email">
    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
    rp8585881@gmail.com
  </a>
  <a href="https://www.linkedin.com/in/rishabh-pathak-95a077379/" target="_blank" class="connect-btn linkedin">
    <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
    LinkedIn
  </a>
</div>

<div class="footer-note">// Built with ❤️ by Rishabh Pathak</div>

</body>
</html>
