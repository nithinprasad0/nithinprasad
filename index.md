---
layout: null
---
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nithin Prasad</title>
<link href="https://fonts.googleapis.com/css2?family=Azeret+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,300&display=swap" rel="stylesheet">
<style>
*,*::before,*::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg:        #0c1929;
  --bg2:       #0a1520;
  --glass:     rgba(14, 30, 54, 0.55);
  --glass2:    rgba(56, 189, 248, 0.04);
  --border:    rgba(56, 189, 248, 0.12);
  --border2:   rgba(56, 189, 248, 0.28);
  --ice:       #38bdf8;
  --ice-dim:   rgba(56, 189, 248, 0.55);
  --ice-ghost: rgba(56, 189, 248, 0.08);
  --white:     #e8f4fc;
  --muted:     #4a7a99;
  --faint:     #1a2d42;
  --text:      #c8dff0;
}

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Azeret Mono', monospace;
  font-weight: 300;
  overflow-x: hidden;
  cursor: none;
  line-height: 1.6;
}

/* ── Aurora background ── */
#aurora {
  position: fixed;
  inset: 0;
  z-index: 0;
  pointer-events: none;
  overflow: hidden;
}
.aurora-band {
  position: absolute;
  border-radius: 50%;
  filter: blur(80px);
  opacity: 0.07;
  animation: drift linear infinite;
}
.ab1 { width:600px;height:300px;background:#38bdf8;top:-80px;left:-100px;animation-duration:28s; }
.ab2 { width:500px;height:250px;background:#0ea5e9;top:20%;right:-120px;animation-duration:34s;animation-delay:-8s; }
.ab3 { width:400px;height:200px;background:#7dd3fc;bottom:10%;left:20%;animation-duration:40s;animation-delay:-14s; }
@keyframes drift {
  0%   { transform: translate(0,0) rotate(0deg); }
  33%  { transform: translate(40px, 30px) rotate(8deg); }
  66%  { transform: translate(-30px, 50px) rotate(-5deg); }
  100% { transform: translate(0,0) rotate(0deg); }
}

/* Hex grid overlay */
body::after {
  content: '';
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 1;
  background-image:
    linear-gradient(rgba(56,189,248,0.025) 1px, transparent 1px),
    linear-gradient(90deg, rgba(56,189,248,0.025) 1px, transparent 1px);
  background-size: 64px 64px;
}

/* ── CURSOR ── */
#cur {
  width: 4px; height: 4px;
  background: var(--ice);
  border-radius: 50%;
  position: fixed; top: 0; left: 0;
  pointer-events: none; z-index: 9999;
  box-shadow: 0 0 10px var(--ice), 0 0 20px rgba(56,189,248,0.4);
  transition: transform 0.05s linear;
}
#cur-ring {
  width: 28px; height: 28px;
  border: 1px solid rgba(56,189,248,0.5);
  border-radius: 50%;
  position: fixed; top: 0; left: 0;
  pointer-events: none; z-index: 9998;
  transition: transform 0.22s cubic-bezier(0.23,1,0.32,1), width 0.3s, height 0.3s, border-color 0.3s;
}
#cur-ring.expand { width: 52px; height: 52px; border-color: rgba(56,189,248,0.8); }

/* ── NAV ── */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 800;
  background: rgba(12, 25, 41, 0.75);
  backdrop-filter: blur(20px) saturate(1.4);
  -webkit-backdrop-filter: blur(20px) saturate(1.4);
  border-bottom: 1px solid var(--border);
}
.nav-inner {
  max-width: 1020px; margin: 0 auto; padding: 0 44px;
  height: 54px; display: flex; align-items: center; justify-content: space-between;
}
.nav-logo {
  font-size: 0.62rem; letter-spacing: 5px; color: var(--ice);
  text-decoration: none; font-weight: 500; text-transform: uppercase;
}
.nav-links { display: flex; gap: 36px; }
.nav-links a {
  font-size: 0.58rem; letter-spacing: 3px; text-transform: uppercase;
  color: var(--muted); text-decoration: none;
  transition: color 0.2s;
  position: relative;
}
.nav-links a::after {
  content: ''; position: absolute; bottom: -3px; left: 0;
  height: 1px; width: 0; background: var(--ice);
  transition: width 0.3s ease;
}
.nav-links a:hover { color: var(--ice); }
.nav-links a:hover::after { width: 100%; }

/* ── LAYOUT ── */
.wrap { max-width: 1020px; margin: 0 auto; padding: 0 44px; position: relative; z-index: 2; }

/* ── HERO ── */
header {
  min-height: 100vh;
  display: flex; flex-direction: column; justify-content: center;
  padding: 110px 0 80px;
  position: relative;
}

.coord-tag {
  font-size: 0.58rem; letter-spacing: 5px; color: var(--muted);
  text-transform: uppercase; display: flex; align-items: center; gap: 12px;
  margin-bottom: 40px;
  opacity: 0; animation: fadeup 0.8s forwards 0.3s;
}
.coord-tag::before { content: '—'; color: var(--ice); }

h1 {
  font-size: clamp(3.8rem, 10vw, 8.5rem);
  font-weight: 200;
  letter-spacing: -2px;
  line-height: 0.92;
  color: var(--white);
  opacity: 0; animation: fadeup 1s forwards 0.5s;
}
h1 span.last { 
  display: block;
  font-weight: 600;
  color: var(--ice);
  letter-spacing: -3px;
}

.hero-rule {
  width: 80px; height: 1px;
  background: linear-gradient(to right, var(--ice), transparent);
  margin: 36px 0;
  opacity: 0; animation: fadeup 0.6s forwards 0.9s;
}

.hero-bio {
  max-width: 500px;
  font-size: 0.82rem; color: var(--muted); line-height: 1.9;
  font-weight: 300; letter-spacing: 0.3px;
  opacity: 0; animation: fadeup 0.8s forwards 1.1s;
}

/* Floating stat chips */
.hero-chips {
  display: flex; gap: 12px; margin-top: 52px; flex-wrap: wrap;
  opacity: 0; animation: fadeup 0.8s forwards 1.35s;
}
.chip {
  display: flex; flex-direction: column; gap: 2px;
  padding: 14px 22px;
  background: var(--glass);
  border: 1px solid var(--border);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  transition: border-color 0.3s, background 0.3s;
}
.chip:hover { border-color: var(--border2); background: var(--ice-ghost); }
.chip-val { font-size: 1.4rem; font-weight: 600; color: var(--ice); line-height: 1; }
.chip-key { font-size: 0.52rem; letter-spacing: 3px; color: var(--muted); text-transform: uppercase; margin-top: 4px; }

/* ── SECTION ── */
.sec { padding: 110px 0; }

.sec-label {
  display: flex; align-items: center; gap: 18px;
  margin-bottom: 60px;
}
.sec-num { font-size: 0.55rem; letter-spacing: 4px; color: var(--ice); font-weight: 500; }
.sec-line { flex: 1; height: 1px; background: var(--border); }
.sec-title {
  font-size: clamp(1.4rem, 3.5vw, 2.2rem);
  font-weight: 200; letter-spacing: 6px;
  text-transform: uppercase; color: var(--white);
}

/* ── FROSTED GLASS CARDS ── */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 16px;
}

.glass-card {
  background: var(--glass);
  border: 1px solid var(--border);
  backdrop-filter: blur(24px) saturate(1.5);
  -webkit-backdrop-filter: blur(24px) saturate(1.5);
  padding: 36px;
  position: relative; overflow: hidden;
  transition: border-color 0.4s, background 0.4s, transform 0.4s cubic-bezier(0.16,1,0.3,1);
}
.glass-card::before {
  content: '';
  position: absolute; top: 0; left: 0; right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(56,189,248,0.5), transparent);
  transform: scaleX(0); transform-origin: left;
  transition: transform 0.6s cubic-bezier(0.16,1,0.3,1);
}
/* inner frost sheen */
.glass-card::after {
  content: '';
  position: absolute; inset: 0;
  background: linear-gradient(135deg, rgba(56,189,248,0.04) 0%, transparent 60%);
  pointer-events: none;
}
.glass-card:hover {
  border-color: var(--border2);
  background: rgba(14, 30, 54, 0.7);
  transform: translateY(-4px);
}
.glass-card:hover::before { transform: scaleX(1); }

.card-idx {
  font-size: 0.52rem; letter-spacing: 4px; color: var(--muted);
  text-transform: uppercase; margin-bottom: 24px; display: block;
}
.glass-card h3 {
  font-size: 1.05rem; font-weight: 500; letter-spacing: 2px;
  color: var(--white); text-transform: uppercase; margin-bottom: 14px;
}
.glass-card p {
  font-size: 0.78rem; color: var(--muted); line-height: 1.8;
  margin-bottom: 26px; font-weight: 300;
}
.tags { display: flex; flex-wrap: wrap; gap: 8px; }
.tag {
  font-size: 0.55rem; letter-spacing: 2px; text-transform: uppercase;
  color: var(--ice); border: 1px solid var(--border);
  padding: 3px 10px; background: var(--ice-ghost);
}

/* ── TIMELINE ── */
.timeline { display: flex; flex-direction: column; }
.tl-row {
  display: grid; grid-template-columns: 170px 1fr;
  gap: 0;
  border-bottom: 1px solid var(--border);
  position: relative;
  transition: background 0.3s;
}
.tl-row:first-child { border-top: 1px solid var(--border); }
.tl-row::before {
  content: '';
  position: absolute; left: 169px; top: 0; bottom: 0;
  width: 1px; background: var(--border);
}
.tl-row:hover { background: var(--ice-ghost); }

.tl-meta {
  padding: 32px 28px 32px 0;
  text-align: right;
  position: relative;
}
.tl-date { font-size: 0.58rem; letter-spacing: 3px; color: var(--ice); display: block; margin-bottom: 4px; }
.tl-cat  { font-size: 0.52rem; letter-spacing: 2px; color: var(--muted); }
.tl-dot  {
  width: 7px; height: 7px; border-radius: 50%;
  background: var(--bg); border: 1px solid var(--ice);
  position: absolute; right: -4px; top: 36px;
  transition: background 0.3s, box-shadow 0.3s;
}
.tl-row:hover .tl-dot { background: var(--ice); box-shadow: 0 0 10px rgba(56,189,248,0.6); }

.tl-body { padding: 32px 0 32px 36px; }
.tl-body h4 {
  font-size: 0.88rem; font-weight: 500; letter-spacing: 1.5px;
  color: var(--white); text-transform: uppercase; margin-bottom: 10px;
}
.tl-body p  { font-size: 0.78rem; color: var(--muted); line-height: 1.8; font-weight: 300; }
.tl-body .sub { font-size: 0.62rem; letter-spacing: 2px; color: var(--faint); margin-top: 6px; display: block; }

.gpa-tag {
  display: inline-block; margin-top: 10px;
  font-size: 0.55rem; letter-spacing: 3px;
  color: var(--ice); border: 1px solid var(--border);
  padding: 3px 12px; background: var(--ice-ghost);
}

/* ── CTA ── */
.cta-wrap { padding: 80px 0 40px; }

.btn {
  display: inline-flex; align-items: center; gap: 16px;
  font-family: 'Azeret Mono', monospace;
  font-size: 0.62rem; letter-spacing: 4px; text-transform: uppercase;
  color: var(--ice); text-decoration: none;
  border: 1px solid var(--border2);
  padding: 18px 48px;
  background: var(--glass);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  position: relative; overflow: hidden;
  transition: color 0.5s, border-color 0.3s;
}
.btn::before {
  content: '';
  position: absolute; inset: 0;
  background: var(--ice);
  transform: translateX(-101%);
  transition: transform 0.55s cubic-bezier(0.16,1,0.3,1);
  z-index: 0;
}
.btn span { position: relative; z-index: 1; }
.btn:hover { color: var(--bg); border-color: var(--ice); }
.btn:hover::before { transform: translateX(0); }

/* ── FOOTER ── */
footer {
  border-top: 1px solid var(--border);
  padding: 40px 0;
  display: flex; justify-content: space-between; align-items: center;
}
footer .f-left { font-size: 0.55rem; letter-spacing: 3px; color: var(--muted); }
.f-status { display: flex; align-items: center; gap: 8px; font-size: 0.55rem; letter-spacing: 3px; color: var(--ice); }
.f-dot {
  width: 5px; height: 5px; border-radius: 50%;
  background: var(--ice);
  box-shadow: 0 0 8px var(--ice);
  animation: blink-dot 2.5s ease-in-out infinite;
}
@keyframes blink-dot { 0%,100%{opacity:1} 50%{opacity:0.2} }

/* ── SCROLL REVEAL ── */
.sr { opacity: 0; transform: translateY(28px); transition: opacity 0.9s cubic-bezier(0.16,1,0.3,1), transform 0.9s cubic-bezier(0.16,1,0.3,1); }
.sr.on { opacity: 1; transform: translateY(0); }
.d1 { transition-delay: 0.06s; } .d2 { transition-delay: 0.13s; }
.d3 { transition-delay: 0.20s; } .d4 { transition-delay: 0.27s; }

/* ── KEYFRAMES ── */
@keyframes fadeup { to { opacity: 1; transform: translateY(0); } }
.coord-tag,.hero-rule,.hero-bio,.hero-chips { transform: translateY(16px); }

/* ── RESPONSIVE ── */
@media (max-width: 660px) {
  .wrap { padding: 0 22px; }
  .nav-inner { padding: 0 22px; }
  .nav-links { display: none; }
  .cards-grid { grid-template-columns: 1fr; }
  .tl-row { grid-template-columns: 1fr; }
  .tl-row::before,.tl-dot { display: none; }
  .tl-meta { text-align: left; padding: 24px 0 0; }
  .tl-body { padding: 12px 0 24px; }
  footer { flex-direction: column; gap: 12px; }
  .hero-chips { gap: 8px; }
}
</style>
</head>
<body>

<!-- Aurora -->
<div id="aurora">
  <div class="aurora-band ab1"></div>
  <div class="aurora-band ab2"></div>
  <div class="aurora-band ab3"></div>
</div>

<!-- Cursor -->
<div id="cur"></div>
<div id="cur-ring"></div>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a class="nav-logo" href="#">NP / Systems</a>
    <div class="nav-links">
      <a href="#projects">Projects</a>
      <a href="#leadership">Leadership</a>
      <a href="#education">Education</a>
      <a href="./assets/docs/resume_tcs.pdf">Résumé</a>
    </div>
  </div>
</nav>

<div class="wrap">

  <!-- HERO -->
  <header>
    <div class="coord-tag">10.53° N &nbsp;76.21° E &nbsp;&nbsp;·&nbsp;&nbsp; Kerala, India &nbsp;&nbsp;·&nbsp;&nbsp; MCA Candidate</div>

    <h1>NITHIN<span class="last">PRASAD</span></h1>

    <div class="hero-rule"></div>

    <p class="hero-bio">
      Software developer proficient in Python and AI-driven automation.
      Focused on autonomous data systems and national-level technical leadership.
      Currently pursuing MCA at ASIET Kalady.
    </p>

    <div class="hero-chips">
      <div class="chip"><span class="chip-val">04</span><span class="chip-key">Projects</span></div>
      <div class="chip"><span class="chip-val">03</span><span class="chip-key">Leadership</span></div>
      <div class="chip"><span class="chip-val">7.9</span><span class="chip-key">GPA</span></div>
      <div class="chip"><span class="chip-val">19h</span><span class="chip-key">Hackathon</span></div>
    </div>
  </header>

  <!-- PROJECTS -->
  <section class="sec" id="projects">
    <div class="sec-label sr">
      <span class="sec-num">01</span>
      <div class="sec-line"></div>
      <h2 class="sec-title">Projects</h2>
      <div class="sec-line"></div>
    </div>

    <div class="cards-grid">
      <div class="glass-card sr d1">
        <span class="card-idx">PRJ — 001</span>
        <h3>Insight Gen</h3>
        <p>Agentic AI platform for autonomous data analysis and professional report generation from natural language queries via multi-agent orchestration.</p>
        <div class="tags"><span class="tag">Python</span><span class="tag">CrewAI</span><span class="tag">Streamlit</span><span class="tag">Pandas</span></div>
      </div>
      <div class="glass-card sr d2">
        <span class="card-idx">PRJ — 002</span>
        <h3>Revo</h3>
        <p>Social news Android application with advanced content rating and real-time community discussion threads backed by Firebase infrastructure.</p>
        <div class="tags"><span class="tag">Java</span><span class="tag">Android</span><span class="tag">Firebase</span></div>
      </div>
      <div class="glass-card sr d3">
        <span class="card-idx">PRJ — 003</span>
        <h3>Profexia</h3>
        <p>Web-based skill-barter platform enabling community-driven exchange without financial dependency. Full-stack Django implementation.</p>
        <div class="tags"><span class="tag">Django</span><span class="tag">Python</span><span class="tag">SQL</span></div>
      </div>
      <div class="glass-card sr d4">
        <span class="card-idx">PRJ — 004</span>
        <h3>Vaccination Manager</h3>
        <p>Child vaccination tracking system with automated notification schedules, reducing missed immunizations through intelligent reminders.</p>
        <div class="tags"><span class="tag">JavaScript</span><span class="tag">HTML5</span><span class="tag">SQL</span></div>
      </div>
    </div>
  </section>

  <!-- LEADERSHIP -->
  <section class="sec" id="leadership">
    <div class="sec-label sr">
      <span class="sec-num">02</span>
      <div class="sec-line"></div>
      <h2 class="sec-title">Leadership</h2>
      <div class="sec-line"></div>
    </div>

    <div class="timeline">
      <div class="tl-row sr d1">
        <div class="tl-meta">
          <span class="tl-date">Mar 2026</span>
          <span class="tl-cat">Hackathon</span>
          <div class="tl-dot"></div>
        </div>
        <div class="tl-body">
          <h4>Main Coordinator — Hackastra 2026</h4>
          <p>Directed end-to-end execution of a 19-hour hackathon themed "Design for Human Weakness". Managed teams, judges, venues, and full logistics.</p>
        </div>
      </div>
      <div class="tl-row sr d2">
        <div class="tl-meta">
          <span class="tl-date">Oct 2025</span>
          <span class="tl-cat">Dept Fest</span>
          <div class="tl-dot"></div>
        </div>
        <div class="tl-body">
          <h4>Main Coordinator — Pragyan Tech Fest</h4>
          <p>Led strategic planning, sponsorship acquisition, and full multi-track execution for the departmental technical festival.</p>
        </div>
      </div>
      <div class="tl-row sr d3">
        <div class="tl-meta">
          <span class="tl-date">Apr 25–26</span>
          <span class="tl-cat">Ongoing</span>
          <div class="tl-dot"></div>
        </div>
        <div class="tl-body">
          <h4>MCA Representative — CSI SB ASIET</h4>
          <p>Coordinating technical symposiums and department workshops for the Computer Society of India student branch.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- EDUCATION -->
  <section class="sec" id="education">
    <div class="sec-label sr">
      <span class="sec-num">03</span>
      <div class="sec-line"></div>
      <h2 class="sec-title">Education</h2>
      <div class="sec-line"></div>
    </div>

    <div class="timeline">
      <div class="tl-row sr d1">
        <div class="tl-meta">
          <span class="tl-date">2024 – Now</span>
          <span class="tl-cat">Postgrad</span>
          <div class="tl-dot"></div>
        </div>
        <div class="tl-body">
          <h4>Master of Computer Applications</h4>
          <p>Adi Shankara Institute of Engineering and Technology, Kalady.</p>
          <span class="sub">Focused on AI systems and software architecture</span>
          <span class="gpa-tag">GPA 7.9 / 10</span>
        </div>
      </div>
      <div class="tl-row sr d2">
        <div class="tl-meta">
          <span class="tl-date">2021 – 2024</span>
          <span class="tl-cat">Undergrad</span>
          <div class="tl-dot"></div>
        </div>
        <div class="tl-body">
          <h4>Bachelor of Computer Applications</h4>
          <p>DePaul Institute of Science and Technology, Angamaly.</p>
          <span class="gpa-tag">GPA 6.7 / 10</span>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <div class="cta-wrap sr">
    <a href="./assets/docs/resume_tcs.pdf" class="btn"><span>Download Résumé</span></a>
  </div>

  <!-- FOOTER -->
  <footer>
    <span class="f-left">Nithin Prasad &nbsp;·&nbsp; 2026</span>
    <div class="f-status"><div class="f-dot"></div>Available for opportunities</div>
  </footer>

</div>

<script>
// Cursor
const cur = document.getElementById('cur');
const ring = document.getElementById('cur-ring');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove', e => {
  mx = e.clientX; my = e.clientY;
  cur.style.transform = `translate(${mx-2}px,${my-2}px)`;
});
(function lp(){
  rx += (mx-rx)*0.11; ry += (my-ry)*0.11;
  ring.style.transform = `translate(${rx-14}px,${ry-14}px)`;
  requestAnimationFrame(lp);
})();
document.querySelectorAll('a,.glass-card,.tl-row,.chip,.btn').forEach(el=>{
  el.addEventListener('mouseenter',()=>ring.classList.add('expand'));
  el.addEventListener('mouseleave',()=>ring.classList.remove('expand'));
});

// Scroll reveal
const obs = new IntersectionObserver(entries=>{
  entries.forEach(e=>{ if(e.isIntersecting) e.target.classList.add('on'); });
},{threshold:0.1});
document.querySelectorAll('.sr').forEach(el=>obs.observe(el));

// Subtle aurora parallax on scroll
window.addEventListener('scroll',()=>{
  const y = window.scrollY * 0.04;
  document.querySelector('.ab1').style.transform = `translateY(${y}px)`;
  document.querySelector('.ab2').style.transform = `translateY(${-y*0.7}px)`;
  document.querySelector('.ab3').style.transform = `translateY(${y*0.5}px)`;
},{passive:true});
</script>
</body>
</html>
