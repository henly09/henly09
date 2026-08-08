<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800;900&family=JetBrains+Mono:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,700;0,800;1,700&display=swap');
  
  * {
    scroll-behavior: smooth;
  }
  
  .readme-container {
    text-align: center;
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    padding: 20px 0;
    max-width: 900px;
    margin: 0 auto;
    position: relative;
  }
  
  .doomer-gif {
    width: 100%;
    max-width: 400px;
    border-radius: 16px;
    margin: 10px auto;
    display: block;
    box-shadow: 0 10px 40px rgba(0,0,0,0.5);
    filter: grayscale(0.3);
    transition: all 0.5s ease;
  }
  
  .doomer-gif:hover {
    filter: grayscale(0);
    transform: scale(1.02);
    box-shadow: 0 15px 50px rgba(255, 87, 34, 0.15);
  }
  
  .title {
    font-family: 'Playfair Display', 'Georgia', serif;
    font-weight: 800;
    font-size: 44px;
    letter-spacing: 1px;
    margin-bottom: 4px;
    position: relative;
    display: inline-block;
  }
  
  .title::after {
    content: '';
    position: absolute;
    bottom: -8px;
    left: 50%;
    transform: translateX(-50%);
    width: 80px;
    height: 3px;
    border-radius: 2px;
    background: linear-gradient(90deg, #FF5722, #FF8A65);
    transition: width 0.4s ease;
  }
  
  .title:hover::after {
    width: 140px;
  }
  
  .subtitle {
    font-family: 'JetBrains Mono', monospace;
    font-weight: 400;
    font-size: 14px;
    letter-spacing: 2px;
    opacity: 0.5;
    margin-top: 16px;
    margin-bottom: 20px;
  }
  
  .status-bar {
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    letter-spacing: 1px;
    opacity: 0.4;
    margin-bottom: 20px;
    padding: 8px 20px;
    border-radius: 20px;
    display: inline-block;
  }
  
  .status-bar span {
    animation: blink 1.2s infinite;
  }
  
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }
  
  .matrix-line {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    letter-spacing: 4px;
    opacity: 0.15;
    margin: 5px 0;
    user-select: none;
  }
  
  /* Dark mode */
  @media (prefers-color-scheme: dark) {
    body {
      background: #0a0a0a;
    }
    .readme-container {
      background: #0a0a0a;
    }
    .title {
      color: #e6edf3;
      text-shadow: 0 2px 30px rgba(255, 87, 34, 0.05);
    }
    .title::after {
      background: linear-gradient(90deg, #ff6b35, #ff3d00);
    }
    .subtitle {
      color: #8b949e;
    }
    .status-bar {
      color: #58a6ff;
      border: 1px solid rgba(88, 166, 255, 0.1);
    }
    .url-link {
      color: #58a6ff !important;
      border: 1px solid rgba(88, 166, 255, 0.15);
      background: rgba(88, 166, 255, 0.03);
    }
    .url-link:hover {
      background: rgba(88, 166, 255, 0.08);
      box-shadow: 0 0 40px rgba(88, 166, 255, 0.05);
      border-color: rgba(88, 166, 255, 0.3);
    }
    .divider {
      border-color: #1a1a1a;
    }
    .stats-wrapper {
      background: rgba(255, 255, 255, 0.02);
      border: 1px solid #1a1a1a;
    }
    .footer-text {
      color: #8b949e;
    }
    .footer-text span {
      color: #ff6b35;
    }
    .matrix-line {
      color: #00ff41;
    }
  }
  
  /* Light mode */
  @media (prefers-color-scheme: light) {
    body {
      background: #0a0a0a;
    }
    .readme-container {
      background: #0a0a0a;
    }
    .title {
      color: #e6edf3;
      text-shadow: 0 2px 30px rgba(255, 87, 34, 0.05);
    }
    .title::after {
      background: linear-gradient(90deg, #ff6b35, #ff3d00);
    }
    .subtitle {
      color: #8b949e;
    }
    .status-bar {
      color: #58a6ff;
      border: 1px solid rgba(88, 166, 255, 0.1);
    }
    .url-link {
      color: #58a6ff !important;
      border: 1px solid rgba(88, 166, 255, 0.15);
      background: rgba(88, 166, 255, 0.03);
    }
    .url-link:hover {
      background: rgba(88, 166, 255, 0.08);
      box-shadow: 0 0 40px rgba(88, 166, 255, 0.05);
      border-color: rgba(88, 166, 255, 0.3);
    }
    .divider {
      border-color: #1a1a1a;
    }
    .stats-wrapper {
      background: rgba(255, 255, 255, 0.02);
      border: 1px solid #1a1a1a;
    }
    .footer-text {
      color: #8b949e;
    }
    .footer-text span {
      color: #ff6b35;
    }
    .matrix-line {
      color: #00ff41;
    }
  }
  
  .url-link {
    font-family: 'JetBrains Mono', 'Courier New', monospace;
    font-size: 16px;
    font-weight: 500;
    letter-spacing: 0.5px;
    text-decoration: none;
    padding: 10px 24px;
    border-radius: 8px;
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    display: inline-block;
    position: relative;
  }
  
  .url-link::before {
    content: '$ ';
    opacity: 0.5;
    font-weight: 300;
  }
  
  .badge-link {
    text-decoration: none;
    margin: 0 6px;
    display: inline-block;
  }
  
  .badge-link img {
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    border-radius: 6px;
    filter: grayscale(0.2);
  }
  
  .badge-link img:hover {
    transform: translateY(-3px) scale(1.02);
    box-shadow: 0 8px 30px rgba(255, 87, 34, 0.15);
    filter: grayscale(0);
  }
  
  .divider {
    border: 0;
    height: 1px;
    background: linear-gradient(to right, transparent, #ff6b35, transparent);
    opacity: 0.15;
    margin: 30px 0;
    position: relative;
  }
  
  .divider::after {
    content: '⚡';
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    top: -10px;
    font-size: 14px;
    opacity: 0.3;
  }
  
  .stats-wrapper {
    padding: 15px;
    border-radius: 12px;
    transition: all 0.4s ease;
    margin: 8px 0;
    position: relative;
    overflow: hidden;
  }
  
  .stats-wrapper::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(135deg, rgba(255, 87, 34, 0.02), transparent);
    pointer-events: none;
  }
  
  .stats-wrapper:hover {
    transform: scale(1.005);
    border-color: rgba(255, 87, 34, 0.15);
  }
  
  .stats-wrapper img {
    transition: all 0.3s ease;
    filter: grayscale(0.2);
  }
  
  .stats-wrapper:hover img {
    filter: grayscale(0);
  }
  
  .footer-text {
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    font-weight: 400;
    letter-spacing: 1px;
    opacity: 0.4;
    margin-top: 20px;
  }
  
  .footer-text span {
    font-weight: 600;
    opacity: 0.8;
  }
  
  .commit-counter {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    letter-spacing: 2px;
    opacity: 0.3;
    margin-top: 10px;
  }
  
  /* Responsive */
  @media (max-width: 600px) {
    .title {
      font-size: 28px;
    }
    .subtitle {
      font-size: 11px;
      letter-spacing: 1px;
    }
    .url-link {
      font-size: 13px;
      padding: 8px 16px;
    }
    .badge-link img {
      width: 110px;
    }
    .title::after {
      width: 50px;
    }
    .title:hover::after {
      width: 80px;
    }
    .doomer-gif {
      max-width: 280px;
    }
  }
</style>

<div class="readme-container">

<p align="center" class="matrix-line">> _ SYSTEM: ONLINE _</p>
<p align="center" class="matrix-line">> _ STATUS: DEPLOYING _</p>

<img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeGVocWZ4dnA1Nm5hNmU2eWQ1NGNpcnR1cWx4dzkxZ2ZkdmQ2N3Q5biZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/JIX9t2j0ZTN9S/giphy.gif" alt="Doomer" class="doomer-gif" />

<p align="center" class="status-bar">
  <span>●</span> /dev/henly09 <span>●</span> commit: 4a7f9d2 <span>●</span> branch: main
</p>

<h2 align="center" class="title">Fullstack Web Developer</h2>
<p align="center" class="subtitle">// building in the dark //</p>

<p align="center">
  <a href="https://akosihenz.shop" class="badge-link">
    <img src="https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Portfolio" />
  </a>
  <a href="mailto:monterahens@gmail.com" class="badge-link">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

<hr class="divider" />

<div class="stats-wrapper">
  <p align="center">
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=henly09&theme=radical&hide_border=true" alt="GitHub Streak" />
  </p>
</div>

<div class="stats-wrapper">
  <p align="center">
    <img src="https://github-readme-activity-graph.vercel.app/graph?username=henly09&theme=github-dark&hide_border=true&bg_color=0a0a0a" alt="Contribution Graph" width="100%" />
  </p>
</div>

<div class="stats-wrapper">
  <p align="center">
    <img src="https://ghchart.rshah.org/henly09" alt="Commit Tiles" width="100%" />
  </p>
</div>

<p align="center" class="commit-counter">
  > commits logged: <span style="color: #ff6b35;">∞</span>
</p>

<hr class="divider" />

<p align="center">
  <a href="https://akosihenz.shop" class="url-link">
    akosihenz.shop
  </a>
</p>

<p align="center" class="footer-text">
  <span>#</span> code.sleep.repeat <span>#</span>
</p>

<p align="center" class="matrix-line" style="margin-top: 15px; font-size: 10px;">
  > _ END_OF_FILE _________________________________________
</p>

</div>
