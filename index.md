---
layout: null
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nithin Prasad | Developer Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <style>
        :root { 
            --bg: #0a0a0c; 
            --card-bg: #111114; 
            --text-primary: #f1f1f1; 
            --text-secondary: #94a3b8; 
            --accent: #60a5fa; 
            --border: #27272a;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }

        body { 
            background: var(--bg); 
            color: var(--text-primary); 
            font-family: 'Inter', sans-serif; 
            margin: 0; 
            padding: 0;
            line-height: 1.6;
            animation: fadeIn 1s ease-out;
        }

        .container { max-width: 950px; margin: 0 auto; padding: 80px 24px; }
        
        header { margin-bottom: 70px; }
        .tagline { font-family: 'JetBrains Mono', monospace; color: var(--accent); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 4px; margin-bottom: 12px; display: block; }
        h1 { font-size: 3.2rem; margin: 0; font-weight: 700; letter-spacing: -2px; color: #fff; }
        .objective { max-width: 650px; color: var(--text-secondary); font-size: 1.1rem; margin-top: 24px; }

        .section-header { 
            font-family: 'JetBrains Mono', monospace; 
            font-size: 0.75rem; 
            color: #4b5563; 
            text-transform: uppercase; 
            letter-spacing: 6px; 
            margin: 60px 0 30px 0;
            display: flex;
            align-items: center;
        }

        .section-header::after { content: ""; flex: 1; height: 1px; background: var(--border); margin-left: 20px; }

        /* Project Grid */
        .project-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 24px; }
        
        .project-card { 
            background: var(--card-bg); 
            padding: 35px; 
            border: 1px solid var(--border); 
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover { 
            border-color: var(--accent); 
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.4);
            transform: translateY(-4px);
        }

        .project-card h3 { margin: 0 0 12px 0; font-size: 1.4rem; font-weight: 600; color: #fff; }
        .project-card p { color: var(--text-secondary); font-size: 0.95rem; margin-bottom: 24px; flex-grow: 1; }
        
        .stack { display: flex; flex-wrap: wrap; gap: 8px; }
        .stack-item { font-family: 'JetBrains Mono', monospace; font-size: 0.7rem; color: var(--accent); background: rgba(96, 165, 250, 0.05); padding: 4px 10px; border: 1px solid rgba(96, 165, 250, 0.2); }

        /* Experience and Education */
        .entry { margin-bottom: 35px; border-left: 1px solid var(--border); padding-left: 25px; position: relative; }
        .entry::before { content: ""; position: absolute; left: -4px; top: 0; width: 7px; height: 7px; background: var(--accent); }
        .entry h4 { margin: 0; font-size: 1.15rem; color: #fff; }
        .entry-meta { font-family: 'JetBrains Mono', monospace; font-size: 0.8rem; color: var(--accent); margin-bottom: 8px; }
        .entry-sub { color: var(--text-secondary); font-size: 0.9rem; }

        .btn-container { margin-top: 60px; }
        .cta-btn { 
            display: inline-block; 
            padding: 16px 35px; 
            background: transparent;
            color: var(--accent); 
            border: 1px solid var(--accent);
            text-decoration: none; 
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.85rem;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .cta-btn:hover { 
            background: var(--accent);
            color: var(--bg);
            box-shadow: 0 0 25px rgba(96, 165, 250, 0.3);
        }

        footer { margin-top: 100px; padding: 40px 0; border-top: 1px solid var(--border); text-align: center; color: #3f3f46; font-family: 'JetBrains Mono', monospace; font-size: 0.7rem; }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <span class="tagline">Developer_Portfolio_v2.0</span>
            <h1>Nithin Prasad</h1>
            <p class="objective">Ambitious Software Developer with a strong proficiency in Python and AI-driven automation. Committed to delivering scalable, high-quality code and evolving with emerging technologies.</p>
        </header>

        <div class="section-header">Featured_Projects</div>
        <div class="project-grid">
            <div class="project-card">
                <h3>Insight Gen</h3>
                <p>An Agentic AI Analytics platform functioning as an autonomous system for data analysis and professional report generation.</p>
                <div class="stack">
                    <span class="stack-item">CrewAI</span>
                    <span class="stack-item">Streamlit</span>
                    <span class="stack-item">Pandas</span>
                </div>
            </div>

            <div class="project-card">
                <h3>Revo</h3>
                <p>Social news Android application featuring content rating and insightful discussions for real-time information delivery.</p>
                <div class="stack">
                    <span class="stack-item">Android</span>
                    <span class="stack-item">Java</span>
                    <span class="stack-item">XML</span>
                </div>
            </div>

            <div class="project-card">
                <h3>PROFEXIA</h3>
                <p>Community-driven skill barter platform designed for web-based exchange without financial dependency.</p>
                <div class="stack">
                    <span class="stack-item">Django</span>
                    <span class="stack-item">Python</span>
                    <span class="stack-item">SQL</span>
                </div>
            </div>
        </div>

        <div class="section-header">Education</div>
        <div class="entry">
            <div class="entry-meta">2024 - Present // GPA: 7.9</div>
            <h4>Master of Computer Applications (MCA)</h4>
            <div class="entry-sub">Adi Shankara Institute of Engineering and Technology, Kalady</div>
        </div>

        <div class="entry">
            <div class="entry-meta">2021 - 2024 // GPA: 6.7</div>
            <h4>Bachelor of Computer Applications (BCA)</h4>
            <div class="entry-sub">DePaul Institute of Science and Technology, Angamaly</div>
        </div>

        <div class="section-header">Leadership_and_Events</div>
        <div class="entry">
            <div class="entry-meta">March 2026</div>
            <h4>Main Coordinator // Hackastra 2026</h4>
            <div class="entry-sub">Managed execution of a national-level hackathon themed "Design for Human Weakness".</div>
        </div>

        <div class="entry">
            <div class="entry-meta">October 2025</div>
            <h4>Main Coordinator // Pragyan Tech Fest</h4>
            <div class="entry-sub">Strategic planning and sponsorship acquisition for departmental festival.</div>
        </div>

        <div class="btn-container">
            <a href="./assets/docs/resume_tcs.pdf" class="cta-btn">EXECUTE_RESUME_DOWNLOAD</a>
        </div>

        <footer>
            NITHIN_PRASAD // BUILT_WITH_GITHUB_PAGES // 2026
        </footer>
    </div>
</body>
</html>
