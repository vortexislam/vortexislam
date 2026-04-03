<!DOCTYPE html>
<html lang="ar" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GitHub Profile — Developer Portfolio</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
<script src="https://unpkg.com/lucide@latest/dist/umd/lucide.js"></script>

<style>
:root {
  --text-xs:   clamp(0.75rem,  0.7rem  + 0.25vw, 0.875rem);
  --text-sm:   clamp(0.875rem, 0.8rem  + 0.35vw, 1rem);
  --text-base: clamp(1rem,     0.95rem + 0.25vw, 1.125rem);
  --text-lg:   clamp(1.125rem, 1rem    + 0.75vw, 1.5rem);
  --text-xl:   clamp(1.5rem,   1.2rem  + 1.25vw, 2.25rem);
  --text-2xl:  clamp(2rem,     1.2rem  + 2.5vw,  3.5rem);
  --space-1:0.25rem;--space-2:0.5rem;--space-3:0.75rem;--space-4:1rem;--space-5:1.25rem;
  --space-6:1.5rem;--space-8:2rem;--space-10:2.5rem;--space-12:3rem;--space-16:4rem;
  --radius-sm:0.375rem;--radius-md:0.5rem;--radius-lg:0.75rem;
  --radius-xl:1rem;--radius-2xl:1.5rem;--radius-full:9999px;
  --font-display:'Space Grotesk','Inter',sans-serif;
  --font-body:'Inter',sans-serif;
  --font-mono:'Fira Code','Courier New',monospace;
  --transition:200ms cubic-bezier(0.16,1,0.3,1);
}
[data-theme="dark"],:root{
  --color-bg:#0d1117;--color-surface:#161b22;--color-surface-2:#1c2128;
  --color-surface-offset:#21262d;--color-surface-dynamic:#30363d;
  --color-border:#30363d;--color-divider:#21262d;
  --color-text:#e6edf3;--color-text-muted:#7d8590;--color-text-faint:#484f58;
  --color-primary:#58a6ff;--color-primary-glow:rgba(88,166,255,0.15);
  --color-secondary:#3fb950;--color-purple:#bc8cff;
  --color-cyan:#39c5cf;--color-yellow:#d29922;
  --shadow-sm:0 1px 3px rgba(0,0,0,0.4);--shadow-md:0 4px 16px rgba(0,0,0,0.5);
  --shadow-lg:0 8px 32px rgba(0,0,0,0.6);--shadow-glow:0 0 30px rgba(88,166,255,0.12);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale}
body{font-family:var(--font-body);font-size:var(--text-base);color:var(--color-text);background:var(--color-bg);min-height:100dvh;line-height:1.6;overflow-x:hidden}
img{display:block;max-width:100%;height:auto}
a{color:var(--color-primary);text-decoration:none;transition:color var(--transition)}
a:hover{color:#79c0ff}
button{cursor:pointer;background:none;border:none;font:inherit;color:inherit}

/* ── BACKGROUND ── */
.bg-canvas{position:fixed;inset:0;z-index:0;pointer-events:none;overflow:hidden}
.bg-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(48,54,61,0.5) 1px,transparent 1px),linear-gradient(90deg,rgba(48,54,61,0.5) 1px,transparent 1px);background-size:40px 40px;mask-image:radial-gradient(ellipse 80% 80% at 50% 0%,black 20%,transparent 100%)}
.bg-glow{position:absolute;border-radius:50%;filter:blur(80px);opacity:0.15;animation:float 8s ease-in-out infinite}
.bg-glow-1{width:600px;height:600px;background:#58a6ff;top:-200px;left:50%;transform:translateX(-50%)}
.bg-glow-2{width:400px;height:400px;background:#bc8cff;top:40%;right:-100px;animation-delay:-3s}
.bg-glow-3{width:350px;height:350px;background:#3fb950;bottom:20%;left:-100px;animation-delay:-5s}
@keyframes float{0%,100%{transform:translateY(0) translateX(-50%)}50%{transform:translateY(-30px) translateX(-50%)}}
.bg-glow-2{animation:float2 10s ease-in-out infinite}
.bg-glow-3{animation:float3 12s ease-in-out infinite}
@keyframes float2{0%,100%{transform:translateY(0)}50%{transform:translateY(-40px)}}
@keyframes float3{0%,100%{transform:translateY(0)}50%{transform:translateY(25px)}}

/* ── LAYOUT ── */
.page{position:relative;z-index:1}
.container{max-width:900px;margin-inline:auto;padding-inline:var(--space-6)}
section{padding-block:var(--space-12)}

/* ── HERO ── */
.hero{padding-block:var(--space-16) var(--space-12);text-align:center}
.avatar-ring{position:relative;width:130px;height:130px;margin:0 auto var(--space-6)}
.avatar-ring::before{content:'';position:absolute;inset:-3px;border-radius:50%;background:conic-gradient(from 0deg,#58a6ff,#bc8cff,#3fb950,#58a6ff);animation:spin-slow 4s linear infinite;z-index:0}
@keyframes spin-slow{to{transform:rotate(360deg)}}
.avatar-ring::after{content:'';position:absolute;inset:0;border-radius:50%;background:var(--color-bg);z-index:0}
.avatar-img{position:relative;z-index:1;width:120px;height:120px;border-radius:50%;margin:5px;background:linear-gradient(135deg,var(--color-surface),var(--color-surface-2));display:flex;align-items:center;justify-content:center;font-size:3rem}
.status-badge{display:inline-flex;align-items:center;gap:var(--space-2);font-family:var(--font-mono);font-size:var(--text-xs);color:var(--color-secondary);background:color-mix(in srgb,var(--color-secondary) 12%,var(--color-surface));border:1px solid color-mix(in srgb,var(--color-secondary) 30%,transparent);padding:var(--space-1) var(--space-3);border-radius:var(--radius-full);margin-bottom:var(--space-4)}
.status-dot{width:6px;height:6px;border-radius:50%;background:var(--color-secondary);box-shadow:0 0 8px var(--color-secondary);animation:pulse-dot 2s ease-in-out infinite}
@keyframes pulse-dot{0%,100%{opacity:1;box-shadow:0 0 8px var(--color-secondary)}50%{opacity:0.6;box-shadow:0 0 16px var(--color-secondary)}}
.hero-name{font-family:var(--font-display);font-size:var(--text-2xl);font-weight:700;letter-spacing:-0.02em;line-height:1.1;margin-bottom:var(--space-3);background:linear-gradient(135deg,#e6edf3 0%,#58a6ff 40%,#bc8cff 100%);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.hero-username{font-family:var(--font-mono);font-size:var(--text-sm);color:var(--color-text-muted);margin-bottom:var(--space-4)}
.hero-username span{color:var(--color-primary)}
.typing-wrapper{font-family:var(--font-mono);font-size:var(--text-base);color:var(--color-text-muted);height:1.6em;margin-bottom:var(--space-6);display:flex;align-items:center;justify-content:center}
.typing-text{color:var(--color-cyan)}
.typing-cursor{display:inline-block;width:2px;height:1em;background:var(--color-primary);margin-left:2px;animation:blink 1s step-end infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0}}
.hero-bio{max-width:58ch;margin:0 auto var(--space-6);color:var(--color-text-muted);font-size:var(--text-sm);line-height:1.7}
.hero-bio strong{color:var(--color-text)}
.hero-meta{display:flex;flex-wrap:wrap;justify-content:center;gap:var(--space-4);margin-bottom:var(--space-8)}
.meta-item{display:flex;align-items:center;gap:var(--space-2);font-size:var(--text-xs);color:var(--color-text-muted)}
.social-links{display:flex;flex-wrap:wrap;justify-content:center;gap:var(--space-3)}
.social-btn{display:flex;align-items:center;gap:var(--space-2);padding:var(--space-2) var(--space-4);border-radius:var(--radius-full);font-size:var(--text-xs);font-weight:500;border:1px solid var(--color-border);background:var(--color-surface);color:var(--color-text-muted);transition:all var(--transition);text-decoration:none}
.social-btn:hover{border-color:var(--color-primary);color:var(--color-primary);background:var(--color-primary-glow);transform:translateY(-2px);box-shadow:0 4px 12px rgba(88,166,255,0.2)}

/* ── STATS ── */
.stats-banner{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:var(--space-4);margin-block:var(--space-8)}
.stat-card{background:var(--color-surface);border:1px solid var(--color-border);border-radius:var(--radius-xl);padding:var(--space-5) var(--space-4);text-align:center;position:relative;overflow:hidden;transition:all var(--transition)}
.stat-card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--color-primary),var(--color-purple));opacity:0;transition:opacity var(--transition)}
.stat-card:hover{transform:translateY(-3px);box-shadow:var(--shadow-glow)}
.stat-card:hover::before{opacity:1}
.stat-number{font-family:var(--font-display);font-size:var(--text-xl);font-weight:700;color:var(--color-text);line-height:1.1}
.stat-label{font-size:var(--text-xs);color:var(--color-text-muted);margin-top:var(--space-1)}

/* ── SECTION HEADER ── */
.section-header{display:flex;align-items:center;gap:var(--space-3);margin-bottom:var(--space-8)}
.section-tag{font-family:var(--font-mono);font-size:var(--text-xs);color:var(--color-primary);background:var(--color-primary-glow);border:1px solid color-mix(in srgb,var(--color-primary) 30%,transparent);padding:var(--space-1) var(--space-3);border-radius:var(--radius-full)}
.section-title{font-family:var(--font-display);font-size:var(--text-xl);font-weight:700;color:var(--color-text);letter-spacing:-0.01em}
.section-line{flex:1;height:1px;background:linear-gradient(90deg,var(--color-border),transparent)}

/* ── SKILLS ── */
.skills-categories{display:flex;flex-direction:column;gap:var(--space-8)}
.skill-category-title{font-family:var(--font-mono);font-size:var(--text-xs);color:var(--color-text-muted);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:var(--space-4);display:flex;align-items:center;gap:var(--space-2)}
.skill-category-title::before{content:'';width:16px;height:1px;background:var(--color-text-faint)}
.skills-grid{display:flex;flex-wrap:wrap;gap:var(--space-2)}
.skill-badge{display:flex;align-items:center;gap:var(--space-2);padding:var(--space-2) var(--space-3);background:var(--color-surface);border:1px solid var(--color-border);border-radius:var(--radius-lg);font-size:var(--text-xs);font-weight:500;color:var(--color-text-muted);transition:all var(--transition);cursor:default}
.skill-badge:hover{border-color:var(--badge-color,var(--color-primary));color:var(--badge-color,var(--color-primary));background:color-mix(in srgb,var(--badge-color,var(--color-primary)) 10%,var(--color-surface));transform:translateY(-2px) scale(1.02);box-shadow:0 4px 12px color-mix(in srgb,var(--badge-color,var(--color-primary)) 20%,transparent)}
.skill-icon{width:16px;height:16px;border-radius:3px;flex-shrink:0}
.skill-level{display:flex;gap:2px;margin-left:var(--space-1)}
.skill-dot{width:4px;height:4px;border-radius:50%}
.skill-dot.filled{background:var(--badge-color,var(--color-primary))}
.skill-dot.empty{background:var(--color-surface-dynamic)}

/* ── PROJECTS ── */
.projects-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(min(380px,100%),1fr));gap:var(--space-4)}
.project-card{background:var(--color-surface);border:1px solid var(--color-border);border-radius:var(--radius-xl);padding:var(--space-6);position:relative;overflow:hidden;transition:all var(--transition);display:flex;flex-direction:column;gap:var(--space-4)}
.project-card::before{content:'';position:absolute;inset:0;background:radial-gradient(circle at var(--mouse-x,50%) var(--mouse-y,50%),color-mix(in srgb,var(--project-color,#58a6ff) 5%,transparent),transparent 60%);opacity:0;transition:opacity 0.4s}
.project-card:hover{transform:translateY(-4px);box-shadow:var(--shadow-md);border-color:var(--project-color,var(--color-primary))}
.project-card:hover::before{opacity:1}
.project-header{display:flex;align-items:flex-start;justify-content:space-between;gap:var(--space-3)}
.project-icon{width:40px;height:40px;border-radius:var(--radius-lg);background:color-mix(in srgb,var(--project-color,#58a6ff) 15%,var(--color-surface-offset));border:1px solid color-mix(in srgb,var(--project-color,#58a6ff) 25%,transparent);display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:1.2rem}
.project-links{display:flex;gap:var(--space-2)}
.project-link{width:28px;height:28px;border-radius:var(--radius-md);background:var(--color-surface-offset);border:1px solid var(--color-border);display:flex;align-items:center;justify-content:center;color:var(--color-text-muted);transition:all var(--transition)}
.project-link:hover{color:var(--color-primary);border-color:var(--color-primary);background:var(--color-primary-glow)}
.project-title{font-family:var(--font-display);font-size:var(--text-base);font-weight:600;color:var(--color-text);line-height:1.3}
.project-desc{font-size:var(--text-xs);color:var(--color-text-muted);line-height:1.6;flex:1}
.project-footer{display:flex;align-items:center;justify-content:space-between;gap:var(--space-2);flex-wrap:wrap}
.project-tags{display:flex;flex-wrap:wrap;gap:var(--space-1)}
.project-tag{font-family:var(--font-mono);font-size:10px;color:var(--project-color,var(--color-primary));background:color-mix(in srgb,var(--project-color,var(--color-primary)) 10%,transparent);border:1px solid color-mix(in srgb,var(--project-color,var(--color-primary)) 25%,transparent);padding:2px 6px;border-radius:var(--radius-full)}
.project-meta{display:flex;gap:var(--space-3)}
.project-stat{display:flex;align-items:center;gap:4px;font-size:var(--text-xs);color:var(--color-text-muted)}

/* ── CONTRIBUTION GRAPH ── */
.contrib-grid{display:grid;grid-template-columns:repeat(52,1fr);gap:3px;margin-bottom:var(--space-4)}
.contrib-week{display:grid;grid-template-rows:repeat(7,1fr);gap:3px}
.contrib-day{width:100%;aspect-ratio:1;border-radius:2px;background:var(--color-surface-offset);transition:all var(--transition)}
.contrib-day:hover{transform:scale(1.4);z-index:2;position:relative}
.contrib-day[data-level="1"]{background:#0e4429}
.contrib-day[data-level="2"]{background:#006d32}
.contrib-day[data-level="3"]{background:#26a641}
.contrib-day[data-level="4"]{background:#39d353}
.contrib-legend{display:flex;align-items:center;gap:var(--space-2);justify-content:flex-end;font-size:var(--text-xs);color:var(--color-text-muted)}
.legend-box{width:12px;height:12px;border-radius:2px}

/* ── TECH MARQUEE ── */
.tech-marquee-wrapper{overflow:hidden;position:relative;margin-block:var(--space-6)}
.tech-marquee-wrapper::before,.tech-marquee-wrapper::after{content:'';position:absolute;top:0;bottom:0;width:80px;z-index:2}
.tech-marquee-wrapper::before{left:0;background:linear-gradient(90deg,var(--color-bg),transparent)}
.tech-marquee-wrapper::after{right:0;background:linear-gradient(-90deg,var(--color-bg),transparent)}
.tech-marquee{display:flex;gap:var(--space-3);animation:marquee 30s linear infinite;width:max-content}
.tech-marquee-2{animation-direction:reverse;animation-duration:25s}
.tech-marquee-wrapper:hover .tech-marquee{animation-play-state:paused}
@keyframes marquee{from{transform:translateX(0)}to{transform:translateX(-50%)}}
.tech-pill{display:flex;align-items:center;gap:var(--space-2);padding:var(--space-2) var(--space-4);background:var(--color-surface);border:1px solid var(--color-border);border-radius:var(--radius-full);white-space:nowrap;font-size:var(--text-xs);font-weight:500;color:var(--color-text-muted);transition:all var(--transition)}
.tech-pill img{width:16px;height:16px;border-radius:2px}
.tech-pill:hover{border-color:var(--color-primary);color:var(--color-primary);background:var(--color-primary-glow)}

/* ── NOW GRID ── */
.now-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(260px,100%),1fr));gap:var(--space-4)}
.now-card{background:var(--color-surface);border:1px solid var(--color-border);border-radius:var(--radius-xl);padding:var(--space-5);display:flex;gap:var(--space-4);align-items:flex-start;transition:all var(--transition)}
.now-card:hover{border-color:var(--now-color,var(--color-primary));transform:translateY(-2px)}
.now-icon{width:40px;height:40px;flex-shrink:0;border-radius:var(--radius-lg);background:color-mix(in srgb,var(--now-color,var(--color-primary)) 15%,var(--color-surface-offset));display:flex;align-items:center;justify-content:center;font-size:1.3rem}
.now-title{font-size:var(--text-sm);font-weight:600;color:var(--color-text);margin-bottom:var(--space-1)}
.now-desc{font-size:var(--text-xs);color:var(--color-text-muted);line-height:1.6}

/* ── TERMINAL ── */
.terminal-card{background:#010409;border:1px solid var(--color-border);border-radius:var(--radius-xl);overflow:hidden;font-family:var(--font-mono)}
.terminal-bar{display:flex;align-items:center;gap:var(--space-2);padding:var(--space-3) var(--space-4);background:var(--color-surface);border-bottom:1px solid var(--color-border)}
.terminal-dot{width:12px;height:12px;border-radius:50%}
.terminal-dot.red{background:#ff5f57}.terminal-dot.yellow{background:#ffbd2e}.terminal-dot.green{background:#28ca41}
.terminal-title{flex:1;text-align:center;font-size:var(--text-xs);color:var(--color-text-faint)}
.terminal-body{padding:var(--space-5)}
.terminal-line{font-size:var(--text-xs);line-height:2}
.t-prompt{color:#3fb950}.t-cmd{color:#79c0ff}.t-string{color:#a5d6ff}.t-num{color:#ff7b72}
.t-comment{color:var(--color-text-faint)}.t-output{color:var(--color-text-muted);padding-left:var(--space-4)}
.t-success{color:#3fb950}.t-highlight{color:var(--color-yellow)}
.lang-bar{margin-top:var(--space-4)}
.lang-row{display:flex;align-items:center;gap:var(--space-3);margin-bottom:var(--space-2)}
.lang-name{font-size:var(--text-xs);color:var(--color-text-muted);width:80px}
.lang-track{flex:1;height:6px;background:var(--color-surface-offset);border-radius:var(--radius-full);overflow:hidden}
.lang-fill{height:100%;border-radius:var(--radius-full)}
.lang-pct{font-size:var(--text-xs);color:var(--color-text-faint);width:35px;text-align:right}

/* ── SCROLL REVEAL ── */
.reveal{opacity:0;transform:translateY(20px);transition:opacity 0.6s cubic-bezier(0.16,1,0.3,1),transform 0.6s cubic-bezier(0.16,1,0.3,1)}
.reveal.visible{opacity:1;transform:translateY(0)}

/* ── FOOTER ── */
.footer{padding-block:var(--space-8);border-top:1px solid var(--color-divider);text-align:center;color:var(--color-text-faint);font-size:var(--text-xs);font-family:var(--font-mono)}
.footer span{color:var(--color-primary)}

@media(max-width:600px){
  .contrib-grid{grid-template-columns:repeat(26,1fr)}
  .projects-grid{grid-template-columns:1fr}
}
@media(prefers-reduced-motion:reduce){
  *,*::before,*::after{animation-duration:0.01ms!important;transition-duration:0.01ms!important}
}
</style>
</head>

<body>

<!-- BACKGROUND -->
<div class="bg-canvas" aria-hidden="true">
  <div class="bg-grid"></div>
  <div class="bg-glow bg-glow-1"></div>
  <div class="bg-glow bg-glow-2"></div>
  <div class="bg-glow bg-glow-3"></div>
  <canvas id="particle-canvas"></canvas>
</div>

<main class="page">
<div class="container">

<!-- ════ HERO ════ -->
<header class="hero">
  <div class="avatar-ring">
    <div class="avatar-img">🧑‍💻</div>
  </div>

  <div class="status-badge">
    <span class="status-dot"></span>
    Available for collaboration
  </div>

  <h1 class="hero-name">Your Name Here</h1>
  <p class="hero-username">@<span>your-github-username</span></p>

  <div class="typing-wrapper">
    <span id="typing-text" class="typing-text"></span>
    <span class="typing-cursor"></span>
  </div>

  <p class="hero-bio">
    Full-Stack Developer &amp; AI Engineer from <strong>🇪🇬 Egypt</strong>.
    Building <strong>intelligent automation systems</strong>, crypto trading bots,
    and SaaS platforms. Passionate about <strong>AI/ML</strong>, workflow orchestration,
    and turning complex ideas into production-grade tools.
  </p>

  <div class="hero-meta">
    <span class="meta-item"><i data-lucide="map-pin" width="14" height="14"></i> Dakahlia, Egypt</span>
    <span class="meta-item"><i data-lucide="building-2" width="14" height="14"></i> Open to opportunities</span>
    <span class="meta-item"><i data-lucide="graduation-cap" width="14" height="14"></i> Medicine Student &amp; Dev</span>
    <span class="meta-item"><i data-lucide="clock" width="14" height="14"></i> UTC+2 (EET)</span>
  </div>

  <nav class="social-links" aria-label="Social links">
    <a href="#" class="social-btn" target="_blank" rel="noopener noreferrer">
      <img src="https://cdn.simpleicons.org/github/8b949e" width="14" height="14" alt=""> GitHub
    </a>
    <a href="#" class="social-btn" target="_blank" rel="noopener noreferrer">
      <img src="https://cdn.simpleicons.org/telegram/229ED9" width="14" height="14" alt=""> Telegram
    </a>
    <a href="#" class="social-btn" target="_blank" rel="noopener noreferrer">
      <img src="https://cdn.simpleicons.org/linkedin/0A66C2" width="14" height="14" alt=""> LinkedIn
    </a>
    <a href="#" class="social-btn" target="_blank" rel="noopener noreferrer">
      <img src="https://cdn.simpleicons.org/x/ffffff" width="14" height="14" alt=""> Twitter / X
    </a>
  </nav>
</header>

<!-- ════ STATS ════ -->
<div class="stats-banner reveal">
  <div class="stat-card"><div class="stat-number">50+</div><div class="stat-label">Projects Built</div></div>
  <div class="stat-card"><div class="stat-number">3+</div><div class="stat-label">Years Experience</div></div>
  <div class="stat-card"><div class="stat-number">15+</div><div class="stat-label">Technologies</div></div>
  <div class="stat-card"><div class="stat-number">500+</div><div class="stat-label">GitHub Commits</div></div>
  <div class="stat-card"><div class="stat-number">10+</div><div class="stat-label">AI Integrations</div></div>
</div>

<!-- ════ MARQUEE ════ -->
<div class="tech-marquee-wrapper reveal" aria-hidden="true">
  <div class="tech-marquee" id="marquee-1"></div>
</div>
<div class="tech-marquee-wrapper reveal" aria-hidden="true">
  <div class="tech-marquee tech-marquee-2" id="marquee-2"></div>
</div>

<!-- ════ SKILLS ════ -->
<section class="reveal">
  <div class="section-header">
    <span class="section-tag">&lt;skills /&gt;</span>
    <h2 class="section-title">Tech Stack &amp; Expertise</h2>
    <div class="section-line"></div>
  </div>
  <div class="skills-categories">

    <!-- Languages -->
    <div class="skill-category">
      <div class="skill-category-title"><i data-lucide="code-2" width="12" height="12"></i> Languages</div>
      <div class="skills-grid">
        <div class="skill-badge" style="--badge-color:#3572A5">
          <img class="skill-icon" src="https://cdn.simpleicons.org/python" alt="">Python
          <span class="skill-level">
            <span class="skill-dot filled" style="--badge-color:#3572A5"></span>
            <span class="skill-dot filled" style="--badge-color:#3572A5"></span>
            <span class="skill-dot filled" style="--badge-color:#3572A5"></span>
            <span class="skill-dot filled" style="--badge-color:#3572A5"></span>
            <span class="skill-dot filled" style="--badge-color:#3572A5"></span>
          </span>
        </div>
        <div class="skill-badge" style="--badge-color:#f1e05a">
          <img class="skill-icon" src="https://cdn.simpleicons.org/javascript" alt="">JavaScript
          <span class="skill-level">
            <span class="skill-dot filled" style="--badge-color:#f1e05a"></span>
            <span class="skill-dot filled" style="--badge-color:#f1e05a"></span>
            <span class="skill-dot filled" style="--badge-color:#f1e05a"></span>
            <span class="skill-dot filled" style="--badge-color:#f1e05a"></span>
            <span class="skill-dot empty"></span>
          </span>
        </div>
        <div class="skill-badge" style="--badge-color:#89e051">
          <img class="skill-icon" src="https://cdn.simpleicons.org/gnubash" alt="">Bash / Shell
          <span class="skill-level">
            <span class="skill-dot filled" style="--badge-color:#89e051"></span>
            <span class="skill-dot filled" style="--badge-color:#89e051"></span>
            <span class="skill-dot filled" style="--badge-color:#89e051"></span>
            <span class="skill-dot filled" style="--badge-color:#89e051"></span>
            <span class="skill-dot empty"></span>
          </span>
        </div>
        <div class="skill-badge" style="--badge-color:#e8971e">
          <img class="skill-icon" src="https://cdn.simpleicons.org/json" alt="">JSON / YAML
          <span class="skill-level">
            <span class="skill-dot filled" style="--badge-color:#e8971e"></span>
            <span class="skill-dot filled" style="--badge-color:#e8971e"></span>
            <span class="skill-dot filled" style="--badge-color:#e8971e"></span>
            <span class="skill-dot filled" style="--badge-color:#e8971e"></span>
            <span class="skill-dot filled" style="--badge-color:#e8971e"></span>
          </span>
        </div>
        <div class="skill-badge" style="--badge-color:#e34c26"><img class="skill-icon" src="https://cdn.simpleicons.org/html5" alt="">HTML5</div>
        <div class="skill-badge" style="--badge-color:#563d7c"><img class="skill-icon" src="https://cdn.simpleicons.org/css3" alt="">CSS3</div>
        <div class="skill-badge" style="--badge-color:#00ADD8">SQL</div>
      </div>
    </div>

    <!-- AI / ML -->
    <div class="skill-category">
      <div class="skill-category-title"><i data-lucide="brain" width="12" height="12"></i> AI / Machine Learning</div>
      <div class="skills-grid">
        <div class="skill-badge" style="--badge-color:#FF6F00"><img class="skill-icon" src="https://cdn.simpleicons.org/anthropic" alt="">Claude / Anthropic</div>
        <div class="skill-badge" style="--badge-color:#412991"><img class="skill-icon" src="https://cdn.simpleicons.org/openai" alt="">OpenAI API</div>
        <div class="skill-badge" style="--badge-color:#4285F4"><img class="skill-icon" src="https://cdn.simpleicons.org/googlegemini" alt="">Gemini API</div>
        <div class="skill-badge" style="--badge-color:#58a6ff">OpenRouter API</div>
        <div class="skill-badge" style="--badge-color:#ff4b4b"><img class="skill-icon" src="https://cdn.simpleicons.org/ollama" alt="">Ollama (Local LLM)</div>
        <div class="skill-badge" style="--badge-color:#bc8cff">RAG Systems</div>
        <div class="skill-badge" style="--badge-color:#3fb950">Prompt Engineering</div>
        <div class="skill-badge" style="--badge-color:#ff7b72">Multi-Agent Systems</div>
        <div class="skill-badge" style="--badge-color:#58a6ff">LLM Optimization</div>
        <div class="skill-badge" style="--badge-color:#6e40c9">Vector Databases</div>
        <div class="skill-badge" style="--badge-color:#E62E2E"><img class="skill-icon" src="https://cdn.simpleicons.org/qdrant" alt="">Qdrant</div>
      </div>
    </div>

    <!-- Automation -->
    <div class="skill-category">
      <div class="skill-category-title"><i data-lucide="workflow" width="12" height="12"></i> Automation &amp; DevOps</div>
      <div class="skills-grid">
        <div class="skill-badge" style="--badge-color:#FF6D00"><img class="skill-icon" src="https://cdn.simpleicons.org/n8n" alt="">n8n Workflows</div>
        <div class="skill-badge" style="--badge-color:#2496ED"><img class="skill-icon" src="https://cdn.simpleicons.org/docker" alt="">Docker</div>
        <div class="skill-badge" style="--badge-color:#F05032"><img class="skill-icon" src="https://cdn.simpleicons.org/git" alt="">Git</div>
        <div class="skill-badge" style="--badge-color:#8b949e"><img class="skill-icon" src="https://cdn.simpleicons.org/github/8b949e" alt="">GitHub Actions</div>
        <div class="skill-badge" style="--badge-color:#FCA326">Linux / Ubuntu VPS</div>
        <div class="skill-badge" style="--badge-color:#0284C7">Webhook Integration</div>
        <div class="skill-badge" style="--badge-color:#00B4D8">API Design &amp; REST</div>
      </div>
    </div>

    <!-- Crypto -->
    <div class="skill-category">
      <div class="skill-category-title"><i data-lucide="trending-up" width="12" height="12"></i> Crypto &amp; Algorithmic Trading</div>
      <div class="skills-grid">
        <div class="skill-badge" style="--badge-color:#F7931A">Trading Bots (Python)</div>
        <div class="skill-badge" style="--badge-color:#F0B90B"><img class="skill-icon" src="https://cdn.simpleicons.org/binance" alt="">Binance API</div>
        <div class="skill-badge" style="--badge-color:#0ECB81">Technical Analysis (ICT)</div>
        <div class="skill-badge" style="--badge-color:#3fb950">Order Blocks / SMC</div>
        <div class="skill-badge" style="--badge-color:#2962FF"><img class="skill-icon" src="https://cdn.simpleicons.org/tradingview" alt="">TradingView</div>
        <div class="skill-badge" style="--badge-color:#bc8cff">Backtesting Strategies</div>
        <div class="skill-badge" style="--badge-color:#ff7b72">Risk Management</div>
      </div>
    </div>

    <!-- Frameworks -->
    <div class="skill-category">
      <div class="skill-category-title"><i data-lucide="package" width="12" height="12"></i> Frameworks &amp; Libraries</div>
      <div class="skills-grid">
        <div class="skill-badge" style="--badge-color:#009688"><img class="skill-icon" src="https://cdn.simpleicons.org/fastapi" alt="">FastAPI</div>
        <div class="skill-badge" style="--badge-color:#3776AB"><img class="skill-icon" src="https://cdn.simpleicons.org/pandas" alt="">Pandas</div>
        <div class="skill-badge" style="--badge-color:#4dabcf"><img class="skill-icon" src="https://cdn.simpleicons.org/numpy" alt="">NumPy</div>
        <div class="skill-badge" style="--badge-color:#8CAAE6">Matplotlib</div>
        <div class="skill-badge" style="--badge-color:#3ECF8E"><img class="skill-icon" src="https://cdn.simpleicons.org/supabase" alt="">Supabase</div>
        <div class="skill-badge" style="--badge-color:#47A248"><img class="skill-icon" src="https://cdn.simpleicons.org/mongodb" alt="">MongoDB</div>
        <div class="skill-badge" style="--badge-color:#336791"><img class="skill-icon" src="https://cdn.simpleicons.org/postgresql" alt="">PostgreSQL</div>
        <div class="skill-badge" style="--badge-color:#DC382D"><img class="skill-icon" src="https://cdn.simpleicons.org/redis" alt="">Redis</div>
      </div>
    </div>

    <!-- Integrations -->
    <div class="skill-category">
      <div class="skill-category-title"><i data-lucide="database" width="12" height="12"></i> Data &amp; Integrations</div>
      <div class="skills-grid">
        <div class="skill-badge" style="--badge-color:#0F9D58"><img class="skill-icon" src="https://cdn.simpleicons.org/googlesheets" alt="">Google Sheets API</div>
        <div class="skill-badge" style="--badge-color:#4285F4"><img class="skill-icon" src="https://cdn.simpleicons.org/googledrive" alt="">Google Drive API</div>
        <div class="skill-badge" style="--badge-color:#229ED9"><img class="skill-icon" src="https://cdn.simpleicons.org/telegram" alt="">Telegram Bot API</div>
        <div class="skill-badge" style="--badge-color:#58a6ff">Selenium / Scraping</div>
        <div class="skill-badge" style="--badge-color:#FF6D00">Airtable API</div>
      </div>
    </div>

  </div>
</section>

<!-- ════ PROJECTS ════ -->
<section class="reveal">
  <div class="section-header">
    <span class="section-tag">&lt;projects /&gt;</span>
    <h2 class="section-title">Featured Projects</h2>
    <div class="section-line"></div>
  </div>
  <div class="projects-grid">

    <article class="project-card" style="--project-color:#F7931A">
      <div class="project-header">
        <div class="project-icon">₿</div>
        <div class="project-links">
          <a href="#" class="project-link" aria-label="GitHub"><i data-lucide="github" width="14" height="14"></i></a>
          <a href="#" class="project-link" aria-label="Demo"><i data-lucide="external-link" width="14" height="14"></i></a>
        </div>
      </div>
      <div>
        <div class="project-title">Crypto Trading Bot</div>
        <p class="project-desc">Automated cryptocurrency trading system with ICT/SMC technical analysis, risk management, and real-time Telegram alerts. Multi-exchange support via CCXT.</p>
      </div>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">Python</span><span class="project-tag">Binance API</span><span class="project-tag">ICT</span>
        </div>
        <div class="project-meta">
          <span class="project-stat"><i data-lucide="star" width="12" height="12"></i> 48</span>
          <span class="project-stat"><i data-lucide="git-fork" width="12" height="12"></i> 12</span>
        </div>
      </div>
    </article>

    <article class="project-card" style="--project-color:#bc8cff">
      <div class="project-header">
        <div class="project-icon">🤖</div>
        <div class="project-links">
          <a href="#" class="project-link" aria-label="GitHub"><i data-lucide="github" width="14" height="14"></i></a>
          <a href="#" class="project-link" aria-label="Demo"><i data-lucide="external-link" width="14" height="14"></i></a>
        </div>
      </div>
      <div>
        <div class="project-title">Multi-Agent AI System</div>
        <p class="project-desc">Orchestrated multi-agent pipeline with n8n leveraging Claude, GPT-4, and Gemini for complex research, analysis, and content generation tasks.</p>
      </div>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">n8n</span><span class="project-tag">Claude API</span><span class="project-tag">RAG</span>
        </div>
        <div class="project-meta">
          <span class="project-stat"><i data-lucide="star" width="12" height="12"></i> 33</span>
          <span class="project-stat"><i data-lucide="git-fork" width="12" height="12"></i> 8</span>
        </div>
      </div>
    </article>

    <article class="project-card" style="--project-color:#3fb950">
      <div class="project-header">
        <div class="project-icon">💊</div>
        <div class="project-links">
          <a href="#" class="project-link" aria-label="GitHub"><i data-lucide="github" width="14" height="14"></i></a>
          <a href="#" class="project-link" aria-label="Demo"><i data-lucide="external-link" width="14" height="14"></i></a>
        </div>
      </div>
      <div>
        <div class="project-title">Pharmacy Management SaaS</div>
        <p class="project-desc">Full-stack SaaS for pharmacy inventory tracking, automated reordering, expiry alerts, and financial reporting with a clean dashboard UI.</p>
      </div>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">Python</span><span class="project-tag">FastAPI</span><span class="project-tag">PostgreSQL</span>
        </div>
        <div class="project-meta">
          <span class="project-stat"><i data-lucide="star" width="12" height="12"></i> 27</span>
          <span class="project-stat"><i data-lucide="git-fork" width="12" height="12"></i> 5</span>
        </div>
      </div>
    </article>

    <article class="project-card" style="--project-color:#FF6D00">
      <div class="project-header">
        <div class="project-icon">⚡</div>
        <div class="project-links">
          <a href="#" class="project-link" aria-label="GitHub"><i data-lucide="github" width="14" height="14"></i></a>
          <a href="#" class="project-link" aria-label="Demo"><i data-lucide="external-link" width="14" height="14"></i></a>
        </div>
      </div>
      <div>
        <div class="project-title">n8n Workflow Library</div>
        <p class="project-desc">Production-ready n8n workflows for AI automation: web scraping, data enrichment, CRM updates, Telegram bots, and scheduled reporting pipelines.</p>
      </div>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">n8n</span><span class="project-tag">Webhooks</span><span class="project-tag">Docker</span>
        </div>
        <div class="project-meta">
          <span class="project-stat"><i data-lucide="star" width="12" height="12"></i> 61</span>
          <span class="project-stat"><i data-lucide="git-fork" width="12" height="12"></i> 19</span>
        </div>
      </div>
    </article>

    <article class="project-card" style="--project-color:#229ED9">
      <div class="project-header">
        <div class="project-icon">📊</div>
        <div class="project-links">
          <a href="#" class="project-link" aria-label="GitHub"><i data-lucide="github" width="14" height="14"></i></a>
        </div>
      </div>
      <div>
        <div class="project-title">Telegram Crypto Monitor</div>
        <p class="project-desc">Real-time market monitoring bot tracking whale movements and funding rates, sending AI-generated analysis and trade signals to Telegram channels.</p>
      </div>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">Python</span><span class="project-tag">Telegram</span><span class="project-tag">AI</span>
        </div>
        <div class="project-meta">
          <span class="project-stat"><i data-lucide="star" width="12" height="12"></i> 19</span>
          <span class="project-stat"><i data-lucide="git-fork" width="12" height="12"></i> 4</span>
        </div>
      </div>
    </article>

    <article class="project-card" style="--project-color:#E62E2E">
      <div class="project-header">
        <div class="project-icon">🔍</div>
        <div class="project-links">
          <a href="#" class="project-link" aria-label="GitHub"><i data-lucide="github" width="14" height="14"></i></a>
          <a href="#" class="project-link" aria-label="Demo"><i data-lucide="external-link" width="14" height="14"></i></a>
        </div>
      </div>
      <div>
        <div class="project-title">RAG Financial Analyst</div>
        <p class="project-desc">Retrieval-Augmented Generation system for financial document analysis using Qdrant vector DB and Claude. Answers complex questions from reports and filings.</p>
      </div>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">Qdrant</span><span class="project-tag">RAG</span><span class="project-tag">Claude</span>
        </div>
        <div class="project-meta">
          <span class="project-stat"><i data-lucide="star" width="12" height="12"></i> 22</span>
          <span class="project-stat"><i data-lucide="git-fork" width="12" height="12"></i> 6</span>
        </div>
      </div>
    </article>

  </div>
</section>

<!-- ════ TERMINAL / CODING STATS ════ -->
<section class="reveal">
  <div class="section-header">
    <span class="section-tag">&lt;stats /&gt;</span>
    <h2 class="section-title">Coding Activity</h2>
    <div class="section-line"></div>
  </div>
  <div class="terminal-card">
    <div class="terminal-bar">
      <span class="terminal-dot red"></span>
      <span class="terminal-dot yellow"></span>
      <span class="terminal-dot green"></span>
      <span class="terminal-title">~/dev — bash — 80×24</span>
    </div>
    <div class="terminal-body">
      <div class="terminal-line"><span class="t-prompt">~</span> <span class="t-cmd">cat</span> <span class="t-string">coding-stats.json</span></div>
      <div class="terminal-line t-output">{</div>
      <div class="terminal-line t-output">&nbsp;&nbsp;<span class="t-string">"total_hours_2025"</span>: <span class="t-num">1420</span>,</div>
      <div class="terminal-line t-output">&nbsp;&nbsp;<span class="t-string">"daily_avg_hours"</span>: <span class="t-num">5.8</span>,</div>
      <div class="terminal-line t-output">&nbsp;&nbsp;<span class="t-string">"longest_session"</span>: <span class="t-string">"7h 30m"</span>,</div>
      <div class="terminal-line t-output">&nbsp;&nbsp;<span class="t-string">"favorite_editor"</span>: <span class="t-string">"VS Code + Terminal"</span>,</div>
      <div class="terminal-line t-output">&nbsp;&nbsp;<span class="t-string">"top_languages"</span>: [<span class="t-string">"Python"</span>, <span class="t-string">"JavaScript"</span>, <span class="t-string">"Bash"</span>]</div>
      <div class="terminal-line t-output">}</div>
      <br>
      <div class="terminal-line"><span class="t-prompt">~</span> <span class="t-cmd">python3</span> <span class="t-string">analyze_languages.py</span></div>
      <div class="terminal-line t-output"><span class="t-success">✓</span> Scanning repositories...</div>
      <br>
      <div class="lang-bar">
        <div class="lang-row">
          <span class="lang-name">Python</span>
          <div class="lang-track"><div class="lang-fill" style="width:62%;background:linear-gradient(90deg,#3572A5,#4fa3e0)"></div></div>
          <span class="lang-pct t-num">62%</span>
        </div>
        <div class="lang-row">
          <span class="lang-name">JavaScript</span>
          <div class="lang-track"><div class="lang-fill" style="width:18%;background:linear-gradient(90deg,#f1e05a,#f0b429)"></div></div>
          <span class="lang-pct t-num">18%</span>
        </div>
        <div class="lang-row">
          <span class="lang-name">Bash/Shell</span>
          <div class="lang-track"><div class="lang-fill" style="width:11%;background:linear-gradient(90deg,#89e051,#3fb950)"></div></div>
          <span class="lang-pct t-num">11%</span>
        </div>
        <div class="lang-row">
          <span class="lang-name">JSON/YAML</span>
          <div class="lang-track"><div class="lang-fill" style="width:6%;background:linear-gradient(90deg,#e8971e,#f7931a)"></div></div>
          <span class="lang-pct t-num">6%</span>
        </div>
        <div class="lang-row">
          <span class="lang-name">Other</span>
          <div class="lang-track"><div class="lang-fill" style="width:3%;background:linear-gradient(90deg,#7d8590,#58a6ff)"></div></div>
          <span class="lang-pct t-num">3%</span>
        </div>
      </div>
      <br>
      <div class="terminal-line">
        <span class="t-success">✓</span>
        <span class="t-highlight"> All systems operational.</span>
        <span class="t-comment"> # Let's build something amazing 🚀</span>
      </div>
    </div>
  </div>
</section>

<!-- ════ CONTRIBUTIONS ════ -->
<section class="reveal">
  <div class="section-header">
    <span class="section-tag">&lt;contributions /&gt;</span>
    <h2 class="section-title">Activity Graph</h2>
    <div class="section-line"></div>
  </div>
  <div id="contrib-container"></div>
  <div class="contrib-legend" style="margin-top:var(--space-3)">
    <span>Less</span>
    <div class="legend-box" style="background:var(--color-surface-offset)"></div>
    <div class="legend-box" style="background:#0e4429"></div>
    <div class="legend-box" style="background:#006d32"></div>
    <div class="legend-box" style="background:#26a641"></div>
    <div class="legend-box" style="background:#39d353"></div>
    <span>More</span>
  </div>
</section>

<!-- ════ NOW ════ -->
<section class="reveal">
  <div class="section-header">
    <span class="section-tag">&lt;now /&gt;</span>
    <h2 class="section-title">What I'm Up To</h2>
    <div class="section-line"></div>
  </div>
  <div class="now-grid">
    <div class="now-card" style="--now-color:#F7931A">
      <div class="now-icon">📈</div>
      <div>
        <div class="now-title">Building Algo Trading Systems</div>
        <p class="now-desc">Developing advanced cryptocurrency trading bots with ICT/SMC strategies, automated backtesting, and live execution via Binance API.</p>
      </div>
    </div>
    <div class="now-card" style="--now-color:#bc8cff">
      <div class="now-icon">🤖</div>
      <div>
        <div class="now-title">AI Automation Platforms</div>
        <p class="now-desc">Building production-grade multi-agent AI systems using n8n, Claude, and vector databases for complex business automation.</p>
      </div>
    </div>
    <div class="now-card" style="--now-color:#3fb950">
      <div class="now-icon">🎓</div>
      <div>
        <div class="now-title">Medicine Studies</div>
        <p class="now-desc">2nd year medical student at Al-Mansoura Private University, blending healthcare knowledge with health-tech development.</p>
      </div>
    </div>
    <div class="now-card" style="--now-color:#58a6ff">
      <div class="now-icon">🔬</div>
      <div>
        <div class="now-title">Exploring Advanced AI</div>
        <p class="now-desc">Deep diving into LLM fine-tuning, agent architectures, and efficient RAG pipelines with local models via Ollama.</p>
      </div>
    </div>
  </div>
</section>

<!-- ════ FOOTER ════ -->
<footer class="footer">
  <p>Crafted with <span>♥</span> and too much ☕ &nbsp;|&nbsp; <span>@your-username</span> on GitHub</p>
  <p style="margin-top:var(--space-2)"><span>Last updated: 2026</span></p>
</footer>

</div>
</main>

<!-- ════ SCRIPTS ════ -->
<script>
lucide.createIcons();

// ── Typing Animation
const phrases = [
  "AI Engineer & Automation Architect",
  "Crypto Trading Bot Developer",
  "n8n Workflow Specialist",
  "Full-Stack Python Developer",
  "RAG & LLM Integration Expert",
  "Multi-Agent AI Systems Builder"
];
let phraseIdx = 0, charIdx = 0, deleting = false;
const el = document.getElementById("typing-text");
function type() {
  const phrase = phrases[phraseIdx];
  if (!deleting) {
    el.textContent = phrase.slice(0, ++charIdx);
    if (charIdx === phrase.length) { deleting = true; setTimeout(type, 2000); return; }
  } else {
    el.textContent = phrase.slice(0, --charIdx);
    if (charIdx === 0) { deleting = false; phraseIdx = (phraseIdx + 1) % phrases.length; }
  }
  setTimeout(type, deleting ? 40 : 75);
}
type();

// ── Tech Marquee
const techs1 = [
  {name:"Python",icon:"python"},{name:"Docker",icon:"docker"},{name:"n8n",icon:"n8n"},
  {name:"Anthropic",icon:"anthropic"},{name:"OpenAI",icon:"openai"},{name:"Telegram",icon:"telegram"},
  {name:"PostgreSQL",icon:"postgresql"},{name:"Redis",icon:"redis"},{name:"Binance",icon:"binance"},
  {name:"FastAPI",icon:"fastapi"},{name:"MongoDB",icon:"mongodb"},{name:"GitHub",icon:"github/8b949e"}
];
const techs2 = [
  {name:"JavaScript",icon:"javascript"},{name:"Bash",icon:"gnubash"},{name:"Git",icon:"git"},
  {name:"Linux",icon:"linux"},{name:"Gemini",icon:"googlegemini"},{name:"Ollama",icon:"ollama"},
  {name:"Supabase",icon:"supabase"},{name:"TradingView",icon:"tradingview"},{name:"Qdrant",icon:"qdrant"},
  {name:"NumPy",icon:"numpy"},{name:"Pandas",icon:"pandas"},{name:"VS Code",icon:"visualstudiocode"}
];
function buildMarquee(el, techs) {
  const doubled = [...techs, ...techs];
  el.innerHTML = doubled.map(t =>
    `<div class="tech-pill"><img src="https://cdn.simpleicons.org/${t.icon}" width="16" height="16" alt="" loading="lazy">${t.name}</div>`
  ).join("");
}
buildMarquee(document.getElementById("marquee-1"), techs1);
buildMarquee(document.getElementById("marquee-2"), techs2);

// ── Contribution Graph
function buildContrib() {
  const cont = document.getElementById("contrib-container");
  const grid = document.createElement("div");
  grid.className = "contrib-grid";
  for (let w = 0; w < 52; w++) {
    const week = document.createElement("div");
    week.className = "contrib-week";
    for (let d = 0; d < 7; d++) {
      const day = document.createElement("div");
      day.className = "contrib-day";
      const r = Math.random();
      const level = r < 0.4 ? 0 : r < 0.6 ? 1 : r < 0.75 ? 2 : r < 0.88 ? 3 : 4;
      if (level > 0) day.setAttribute("data-level", level);
      week.appendChild(day);
    }
    grid.appendChild(week);
  }
  cont.appendChild(grid);
}
buildContrib();

// ── Scroll Reveal
const reveals = document.querySelectorAll(".reveal");
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) { e.target.classList.add("visible"); observer.unobserve(e.target); }
  });
}, { threshold: 0.1 });
reveals.forEach(r => observer.observe(r));

// ── Canvas Particles
const canvas = document.getElementById("particle-canvas");
const ctx = canvas.getContext("2d");
canvas.style.position = "absolute";
canvas.style.inset = "0";
canvas.style.width = "100%";
canvas.style.height = "100%";
function resizeCanvas() { canvas.width = window.innerWidth; canvas.height = window.innerHeight; }
resizeCanvas();
window.addEventListener("resize", resizeCanvas);
const particles = Array.from({length: 60}, () => ({
  x: Math.random() * window.innerWidth,
  y: Math.random() * window.innerHeight,
  r: Math.random() * 1.5 + 0.5,
  speed: Math.random() * 0.4 + 0.1,
  opacity: Math.random() * 0.5 + 0.1,
  color: ["#58a6ff","#bc8cff","#3fb950","#39c5cf"][Math.floor(Math.random() * 4)]
}));
function animateParticles() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  particles.forEach(p => {
    p.y -= p.speed;
    p.opacity -= 0.0008;
    if (p.y < 0 || p.opacity <= 0) {
      p.x = Math.random() * canvas.width;
      p.y = canvas.height + 10;
      p.opacity = Math.random() * 0.5 + 0.1;
    }
    ctx.beginPath();
    ctx.arc(p.x, p.y, p.r, 0, Math.PI * 2);
    ctx.fillStyle = p.color;
    ctx.globalAlpha = p.opacity;
    ctx.fill();
  });
  ctx.globalAlpha = 1;
  requestAnimationFrame(animateParticles);
}
animateParticles();

// ── Card Spotlight Effect
document.querySelectorAll(".project-card").forEach(card => {
  card.addEventListener("mousemove", e => {
    const rect = card.getBoundingClientRect();
    card.style.setProperty("--mouse-x", ((e.clientX - rect.left) / rect.width * 100) + "%");
    card.style.setProperty("--mouse-y", ((e.clientY - rect.top) / rect.height * 100) + "%");
  });
});
</script>
</body>
</html>
