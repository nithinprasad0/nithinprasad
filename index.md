---
layout: null
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nithin Prasad</title>
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;700&family=Inter:wght@300;500;800&display=swap" rel="stylesheet">
    <style>
        :root { 
            --bg: #080808; 
            --card-bg: rgba(15, 15, 15, 0.9); 
            --text: #e0e0e0; 
            --accent: #22c55e; /* Ghost Emerald */
            --accent-dim: rgba(34, 197, 94, 0.1);
            --border: #1a1a1a;
        }

        @keyframes scanline {
            0% { transform: translateY(-100%); }
            100% { transform: translateY(100%); }
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        body { 
            background-color: var(--bg);
            color: var(--text); 
            font-family: 'Inter', sans-serif; 
            margin: 0; 
            padding: 0;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Scanline Overlay Effect */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
            background-size: 100% 2px, 3px 100%;
            z-index: 999;
            pointer-events: none;
            opacity: 0.3;
        }

        .container { max-width: 900px; margin: 0 auto; padding: 40px 20px; }
        
        header { margin-bottom: 60px; border-left: 2px solid var(--accent); padding-left: 20px; }
        .cmd { font-family: 'JetBrains Mono', monospace; color: var(--accent); font-size: 0.9rem; margin-bottom: 5px; }
        .cmd::after { content: "_"; animation: pulse 1s infinite; }
        
        h1 { font-size: clamp(2.5rem, 8vw, 4rem); margin: 10px 0; font-weight: 800; letter-spacing: -2px; color: #fff; }
        .tagline { font-size: 1rem; color: #888; max-width: 600px; font-weight: 300; }

        .section-label { 
            font-family: 'JetBrains Mono', monospace; 
            font-size: 0.7rem; 
            color: var(--accent); 
            text-transform: uppercase; 
            letter-spacing: 4px; 
            margin: 60px 0 20px 0;
            display: block; 
            opacity: 0.7;
        }

        /* Smartphone Friendly Grid */
        .grid { 
            display: grid; 
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); 
            gap: 15px; 
        }

        .card { 
            background: var(--card-bg); 
            padding: 30px; 
            border: 1px solid var(--border); 
            transition: all 0.3s ease;
            position: relative;
        }

        .card:hover { 
            border-color: var(--accent); 
            background: var(--accent-dim);
            transform: scale(1.02);
        }

        .card h3 { margin: 0 0 10px 0; font-size: 1.3rem; font-weight: 700; color: #fff; }
        .card p { color: #aaa; font-size: 0.9rem; margin-bottom: 20px; }
        
        .tags { display: flex; flex-wrap: wrap; gap: 8px; font-family: 'JetBrains Mono', monospace; font-size: 0.65rem; }
        .tags span { background: #000; padding: 4px 8px; border: 1px solid var(--border); color: var(--accent); }

        /* Timeline Items */
        .item { 
            padding: 20px; 
            border-bottom: 1px solid var(--border); 
            transition: 0.3s;
        }
        .item:hover { background: rgba(255,255,255,0.02); }
        .item h4 { margin: 0; font-size: 1.1rem; color: #fff; }
        .item-date { font-family: 'JetBrains Mono', monospace; font-size: 0.75rem; color: var(--accent); margin-bottom: 5px; }
        .item-sub { color: #777; font-size: 0.85rem; }

        /* Mobile Optimized Buttons */
        .btn { 
            display: block;
            text-align: center;
            margin-top: 40px; 
            padding: 18px; 
            background: transparent; 
            border: 1px solid var(--accent);
            color: var(--accent); 
            text-decoration: none; 
            font-family: 'JetBrains Mono', monospace;
            font-weight: 700;
            font-size: 0.9rem;
            transition: 0.3s;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .btn:hover { 
            background: var(--accent); 
            color: #000;
            box-shadow: 0 0 20px var(--accent);
        }

        @media (min-width: 600px) {
            .btn { display: inline-block; width: auto; padding: 18px 40px; }
        }

        footer { 
            margin-top: 100px; 
            padding: 40px 0; 
            border-top: 1px solid var(--border); 
            text-align: center; 
            color: #444; 
            font-family: 'JetBrains Mono', monospace; 
            font-size: 0.7rem; 
        }
    </style>
</head>
<body>

    <div class="container">
        <header>
            <span class="cmd">sudo systemctl start nithin.service</span>
            <h1>Nithin Prasad</h1>
            <p class="tagline">Master of Computer Applications student. Ambitious Software Developer proficient in Python and AI-driven automation focused on scalable project success.</p>
        </header>

        <span class="section-label">Deployment_Logs // Projects</span>
        <div class="grid">
            <div class="card">
                <h3>Insight Gen</h3>
                <p>An Agentic AI Analytics platform engineered for autonomous data analysis and professional report generation from natural language queries.</p>
                <div class="tags"><span>Python</span> <span>CrewAI</span> <span>Streamlit</span> <span>Pandas</span></div>
            </div>
            <div class="card">
                <h3>Revo</h3>
                <p>Android application featuring content rating systems and insightful discussions designed for social news delivery.</p>
                <div class="tags"><span>Java</span> <span>Android</span> <span>XML</span></div>
            </div>
            <div class="card">
                <h3>PROFEXIA</h3>
                <p>Web-based skill-barter platform developed for community-driven skill exchange without financial dependency.</p>
                <div class="tags"><span>Django</span> <span>Python</span> <span>SQL</span></div>
            </div>
            <div class="card">
                <h3>Vax_Manager</h3>
                <p>Digital management system developed to streamline tracking and notification for pediatric vaccination schedules.</p>
                <div class="tags"><span>JavaScript</span> <span>HTML5</span> <span>SQL</span></div>
            </div>
        </div>

        <span class="section-label">System_Stats // Education</span>
        <div class="item">
            <div class="item-date">2024 - Present // GPA: 7.9</div>
            <h4>Master of Computer Applications</h4>
            <p class="item-sub">Adi Shankara Institute of Engineering and Technology, Kalady.</p>
        </div>
        <div class="item">
            <div class="item-date">2021 - 2024 // GPA: 6.7</div>
            <h4>Bachelor of Computer Applications</h4>
            <p class="item-sub">DePaul Institute of Science and Technology, Aluva.</p>
        </div>

        <span class="section-label">Event_Buffer // Leadership</span>
        <div class="item">
            <div class="item-date">MAR 2026 // Hackathon</div>
            <h4>Main Coordinator | Hackastra 2026</h4>
            <p class="item-sub">Organized a 19-hour national-level hackathon themed "Design for Human Weakness", managing end-to-end execution.</p>
        </div>
        <div class="item">
            <div class="item-date">OCT 2025 // Dept Level</div>
            <h4>Main Coordinator | Pragyan Tech Fest</h4>
            <p class="item-sub">Led strategic planning, sponsorship acquisition, and execution for the departmental festival.</p>
        </div>
        <div class="item">
            <div class="item-date">APR 2025 // Computer Society of India</div>
            <h4>MCA Representative | CSI SB ASIET</h4>
            <p class="item-sub">Organizing technical symposiums and department workshops.</p>
        </div>

        <span class="section-label">Access_Protocol</span>
        <a href="./assets/docs/resume_tcs.pdf" class="btn">_EXEC_DOWNLOAD_RESUME</a>

        <footer>
            NITHIN_PRASAD_v4.0 // BUILT_WITH_GITHUB_PAGES
        </footer>
    </div>

</body>
</html>
