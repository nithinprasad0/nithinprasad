---
layout: null
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nithin Prasad | Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <style>
        :root { 
            --bg: #050505; 
            --card-bg: rgba(255, 255, 255, 0.03); 
            --text-primary: #ffffff; 
            --text-secondary: #94a3b8; 
            --accent: #00f2ff; /* Cyber Cyan */
            --accent-glow: rgba(0, 242, 255, 0.3);
            --border: rgba(255, 255, 255, 0.1);
        }

        @keyframes fadeInScale {
            from { opacity: 0; transform: scale(0.98) translateY(20px); }
            to { opacity: 1; transform: scale(1) translateY(0); }
        }

        @keyframes backgroundPulse {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        body { 
            background: radial-gradient(circle at top right, #0a192f, #050505);
            color: var(--text-primary); 
            font-family: 'Inter', sans-serif; 
            margin: 0; 
            padding: 0;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container { max-width: 1000px; margin: 0 auto; padding: 60px 24px; animation: fadeInScale 1s cubic-bezier(0.2, 0.8, 0.2, 1); }
        
        header { margin-bottom: 80px; position: relative; }
        .scanline {
            width: 100%;
            height: 2px;
            background: var(--accent);
            position: absolute;
            top: -20px;
            box-shadow: 0 0 20px var(--accent);
            opacity: 0.5;
        }

        .terminal-text { font-family: 'JetBrains Mono', monospace; color: var(--accent); font-size: 0.85rem; margin-bottom: 10px; display: block; text-shadow: 0 0 10px var(--accent-glow); }
        h1 { font-size: 4rem; margin: 0; font-weight: 800; letter-spacing: -3px; }
        .header-bio { max-width: 700px; color: var(--text-secondary); font-size: 1.2rem; margin-top: 20px; border-left: 2px solid var(--accent); padding-left: 20px; }

        .section-tag { 
            font-family: 'JetBrains Mono', monospace; 
            font-size: 0.75rem; 
            color: var(--accent); 
            text-transform: uppercase; 
            letter-spacing: 5px; 
            margin: 100px 0 40px 0;
            display: flex;
            align-items: center;
            opacity: 0.6;
        }
        .section-tag::after { content: ""; flex: 1; height: 1px; background: linear-gradient(to right, var(--accent), transparent); margin-left: 20px; }

        /* Animated Project Cards */
        .project-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        .p-card { 
            background: var(--card-bg); 
            padding: 40px; 
            border: 1px solid var(--border); 
            border-radius: 12px;
            backdrop-filter: blur(10px);
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .p-card::before {
            content: "";
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(45deg, transparent, rgba(0, 242, 255, 0.05), transparent);
            transform: translateX(-100%);
            transition: 0.5s;
        }

        .p-card:hover { 
            border-color: var(--accent); 
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5), 0 0 20px rgba(0, 242, 255, 0.1);
        }

        .p-card:hover::before { transform: translateX(100%); }

        .p-card h3 { margin: 0 0 15px 0; font-size: 1.5rem; color: #fff; letter-spacing: -0.5px; }
        .p-card p { color: var(--text-secondary); font-size: 0.95rem; margin-bottom: 25px; line-height: 1.7; }
        .stack { display: flex; flex-wrap: wrap; gap: 10px; font-family: 'JetBrains Mono', monospace; font-size: 0.7rem; color: var(--accent); }
        .stack span { background: rgba(0, 242, 255, 0.1); padding: 4px 10px; border-radius: 4px; }

        /* Timeline Items with Motion */
        .entry { 
            margin-bottom: 40px; 
            padding: 30px; 
            border-radius: 8px;
            border-left: 2px solid var(--border);
            transition: 0.4s;
            background: transparent;
        }
        .entry:hover { 
            border-left-color: var(--accent); 
            background: rgba(0, 242, 255, 0.02);
            padding-left: 40px;
        }
        .entry h4 { margin: 0; font-size: 1.2rem; font-weight: 600; }
        .entry-date { font-family: 'JetBrains Mono', monospace; font-size: 0.8rem; color: var(--accent); margin-bottom: 8px; font-weight: 500; }
        .entry-sub { color: var(--text-secondary); font-size: 1rem; margin-top: 5px; }

        /* Certifications Mosaic */
        .cert-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 15px; list-style: none; padding: 0; }
        .cert-item { 
            background: var(--card-bg);
            border: 1px solid var(--border);
            padding: 15px;
            font-size: 0.85rem;
            border-radius: 6px;
            transition: 0.3s;
            text-align: center;
        }
        .cert-item:hover { border-color: var(--accent); color: var(--accent); transform: scale(1.05); }

        /* Dynamic Action Button */
        .btn-action { 
            display: inline-block; 
            margin-top: 60px; 
            padding: 20px 45px; 
            background: transparent;
            border: 1px solid var(--accent); 
            color: var(--accent); 
            text-decoration: none; 
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 4px;
            position: relative;
            z-index: 1;
            transition: 0.5s;
            overflow: hidden;
        }

        .btn-action::after {
            content: "";
            position: absolute;
            bottom: 0; left: 0; width: 100%; height: 0;
            background: var(--accent);
            z-index: -1;
            transition: 0.5s;
        }

        .btn-action:hover { color: var(--bg); }
        .btn-action:hover::after { height: 100%; }

        footer { margin-top: 150px; padding: 60px 0; border-top: 1px solid var(--border); text-align: center; color: #333; font-size: 0.75rem; font-family: 'JetBrains Mono', monospace; letter-spacing: 2px; }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="scanline"></div>
            <span class="terminal-text">PORTFOLIO_SYSTEM_ACTIVE // V4.0</span>
            <h1>Nithin Prasad</h1>
            <p class="header-bio">Software Developer specializing in Python and AI-driven automation. Building autonomous analytics systems and coordinating high-impact national technical events.</p>
        </header>

        <span class="section-tag">Current_Builds</span>
        <div class="project-grid">
            <div class="p-card">
                <h3>Insight Gen</h3>
                <p>An Agentic AI Analytics platform functioning as an autonomous system for data analysis and professional report generation.</p>
                <div class="stack"><span>Python</span> <span>CrewAI</span> <span>Streamlit</span> <span>Pandas</span></div>
            </div>
            <div class="p-card">
                <h3>Revo</h3>
                <p>Social news Android application featuring content rating systems and insightful real-time community discussions.</p>
                <div class="stack"><span>Java</span> <span>Android</span> <span>Firebase</span></div>
            </div>
            <div class="p-card">
                <h3>PROFEXIA</h3>
                <p>Web-based skill-barter platform designed for community-driven skill exchange without financial dependency.</p>
                <div class="stack"><span>Django</span> <span>Python</span> <span>SQL</span></div>
            </div>
            <div class="p-card">
                <h3>Child Vaccination</h3>
                <p>Digital management system developed to streamline tracking and notification for pediatric vaccination schedules.</p>
                <div class="stack"><span>JavaScript</span> <span>SQL</span> <span>HTML5</span></div>
            </div>
        </div>

        <span class="section-tag">Certifications_Validated</span>
        <div class="cert-grid">
            <div class="cert-item">Cloud Computing // <b>NPTEL</b></div>
            <div class="cert-item">Generative AI // <b>IBM</b></div>
            <div class="cert-item">Front-End React // <b>IBM</b></div>
            <div class="cert-item">Full Stack Python // <b>ICT</b></div>
            <div class="cert-item">AI Foundations // <b>DeepLearning</b></div>
            <div class="cert-item">Git & GitHub // <b>IBM</b></div>
        </div>

        <span class="section-tag">Leadership_Timeline</span>
        <div class="entry">
            <div class="entry-date">2026-03-24 // HACKATHON</div>
            <h4>Main Coordinator | Hackastra 2026</h4>
            <div class="entry-sub">Managing end-to-end execution of a 19-hour national hackathon themed "Design for Human Weakness".</div>
        </div>
        <div class="entry">
            <div class="entry-date">2025-10-16 // DEPARTMENT LEVEL</div>
            <h4>Main Coordinator | Pragyan Tech Fest</h4>
            <div class="entry-sub">Strategic planning, sponsorship acquisition, and execution for the departmental tech festival.</div>
        </div>
        <div class="entry">
            <div class="entry-date">2025-04-01 // COMPUTER SOCIETY OF INDIA</div>
            <h4>MCA Representative | CSI SB ASIET</h4>
            <div class="entry-sub">Organizing technical symposiums and coordinating department-level software workshops.</div>
        </div>

        <span class="section-tag">Educational_Credentials</span>
        <div class="entry">
            <div class="entry-date">2024 - PRESENT // GPA: 7.9</div>
            <h4>Master of Computer Applications</h4>
            <div class="entry-sub">Adi Shankara Institute of Engineering and Technology, Kalady.</div>
        </div>
        <div class="entry">
            <div class="entry-date">2021 - 2024 // GPA: 6.7</div>
            <h4>Bachelor of Computer Applications</h4>
            <div class="entry-sub">DePaul Institute of Science and Technology, Angamaly.</div>
        </div>

        <a href="./assets/docs/resume_tcs.pdf" class="btn-action">Download_Core_Resume</a>

        <footer>
            NITHIN_PRASAD_DEV // 2026 // SYST_READY
        </footer>
    </div>
</body>
</html>
