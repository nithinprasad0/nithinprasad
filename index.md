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
            --bg: #0d0d0f; 
            --card-bg: #141417; 
            --text-primary: #ffffff; 
            --text-secondary: #94a3b8; 
            --accent: #10b981; /* Neon Emerald */
            --border: #26262a;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        body { 
            background: var(--bg); 
            color: var(--text-primary); 
            font-family: 'Inter', sans-serif; 
            margin: 0; 
            padding: 0;
            line-height: 1.6;
            animation: fadeIn 0.8s ease-out;
        }

        .container { max-width: 1000px; margin: 0 auto; padding: 60px 24px; }
        
        header { margin-bottom: 60px; }
        .terminal-text { font-family: 'JetBrains Mono', monospace; color: var(--accent); font-size: 0.85rem; margin-bottom: 10px; display: block; }
        h1 { font-size: 3.5rem; margin: 0; font-weight: 700; letter-spacing: -2px; }
        .header-bio { max-width: 700px; color: var(--text-secondary); font-size: 1.1rem; margin-top: 20px; }

        .section-tag { 
            font-family: 'JetBrains Mono', monospace; 
            font-size: 0.7rem; 
            color: #52525b; 
            text-transform: uppercase; 
            letter-spacing: 5px; 
            margin: 80px 0 30px 0;
            display: flex;
            align-items: center;
        }
        .section-tag::after { content: ""; flex: 1; height: 1px; background: var(--border); margin-left: 20px; }

        /* Project Cards */
        .project-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        .p-card { 
            background: var(--card-bg); 
            padding: 30px; 
            border: 1px solid var(--border); 
            border-radius: 4px;
            transition: all 0.3s cubic-bezier(0.23, 1, 0.32, 1);
        }
        .p-card:hover { 
            border-color: var(--accent); 
            transform: scale(1.02);
            box-shadow: 0 10px 30px rgba(16, 185, 129, 0.05);
        }
        .p-card h3 { margin: 0 0 10px 0; font-size: 1.3rem; }
        .p-card p { color: var(--text-secondary); font-size: 0.9rem; margin-bottom: 20px; }
        .stack { display: flex; flex-wrap: wrap; gap: 8px; font-family: 'JetBrains Mono', monospace; font-size: 0.7rem; color: var(--accent); }

        /* Experience & Education */
        .entry { margin-bottom: 30px; padding: 20px; border-left: 1px solid var(--border); transition: 0.3s; }
        .entry:hover { border-left: 1px solid var(--accent); background: rgba(16, 185, 129, 0.02); }
        .entry h4 { margin: 0; font-size: 1.1rem; }
        .entry-date { font-family: 'JetBrains Mono', monospace; font-size: 0.8rem; color: var(--accent); margin-bottom: 5px; }
        .entry-sub { color: var(--text-secondary); font-size: 0.9rem; }

        /* Certifications List */
        .cert-list { columns: 2; column-gap: 40px; list-style: none; padding: 0; }
        .cert-item { margin-bottom: 12px; font-size: 0.9rem; color: var(--text-secondary); border-bottom: 1px solid #1a1a1c; padding-bottom: 5px; }
        .cert-item b { color: #fff; }

        .btn-action { 
            display: inline-block; 
            margin-top: 50px; 
            padding: 15px 35px; 
            border: 1px solid var(--accent); 
            color: var(--accent); 
            text-decoration: none; 
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            transition: 0.3s;
        }
        .btn-action:hover { background: var(--accent); color: var(--bg); box-shadow: 0 0 20px rgba(16, 185, 129, 0.4); }

        footer { margin-top: 100px; padding: 40px 0; border-top: 1px solid var(--border); text-align: center; color: #333; font-size: 0.7rem; font-family: 'JetBrains Mono', monospace; }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <span class="terminal-text">init_portfolio_v3.0</span>
            <h1>Nithin Prasad</h1>
            <p class="header-bio">Software Developer specializing in Python and AI-driven automation. Experienced in building autonomous analytics systems and leading large-scale technical symposia.</p>
        </header>

        <span class="section-tag">Development_Projects</span>
        <div class="project-grid">
            <div class="p-card">
                <h3>Insight Gen</h3>
                <p>Agentic AI Analytics platform for autonomous data analysis and professional report generation from English queries.</p>
                <div class="stack"><span>Python</span> <span>CrewAI</span> <span>Streamlit</span></div>
            </div>
            <div class="p-card">
                <h3>Revo</h3>
                <p>Android social news application featuring content rating and insightful community discussions.</p>
                <div class="stack"><span>Java</span> <span>Android XML</span> <span>Firebase</span></div>
            </div>
            <div class="p-card">
                <h3>PROFEXIA</h3>
                <p>Web-based skill-barter platform designed for community-driven exchange without financial dependency.</p>
                <div class="stack"><span>Django</span> <span>Python</span> <span>SQL</span></div>
            </div>
            <div class="p-card">
                <h3>Vaccination Management</h3>
                <p>Application developed to streamline and enhance child vaccination tracking and notification processes.</p>
                <div class="stack"><span>HTML</span> <span>JavaScript</span> <span>SQL</span></div>
            </div>
        </div>

        <span class="section-tag">Certifications</span>
        <ul class="cert-list">
            <li class="cert-item"><b>Elite Silver</b> // Cloud Computing, NPTEL </li>
            <li class="cert-item"><b>Generative AI</b> // IBM </li>
            <li class="cert-item"><b>Front-End Apps</b> // React, IBM </li>
            <li class="cert-item"><b>Full Stack Python</b> // ICT Academy </li>
            <li class="cert-item"><b>AI for Everyone</b> // DeepLearning.AI </li>
            <li class="cert-item"><b>GitHub</b> // Version Control, IBM </li>
        </ul>

        <span class="section-tag">Leadership_&_Events</span>
        <div class="entry">
            <div class="entry-date">2026-03-24 // 19HR Hackathon</div>
            <h4>Main Coordinator | Hackastra 2026</h4>
            <div class="entry-sub">Managed end-to-end execution of a national hackathon themed "Design for Human Weakness".</div>
        </div>
        <div class="entry">
            <div class="entry-date">2025-10-16 // Dept. Fest</div>
            <h4>Main Coordinator | Pragyan Tech Fest</h4>
            <div class="entry-sub">Led strategic planning, sponsorship acquisition, and execution for the departmental tech fest.</div>
        </div>
        <div class="entry">
            <div class="entry-date">2025-04-01 // </div>
            <h4>MCA Representative | CSI SB ASIET</h4>
            <div class="entry-sub">Organizing technical symposiums and department-level workshops.</div>
        </div>

        <span class="section-tag">Education</span>
        <div class="entry">
            <div class="entry-date">2024 - Present // GPA: 7.9</div>
            <h4>Master of Computer Applications</h4>
            <div class="entry-sub">Adi Shankara Institute of Engineering and Technology, Kalady.</div>
        </div>
        <div class="entry">
            <div class="entry-date">2021 - 2024 // GPA: 6.7</div>
            <h4>Bachelor of Computer Applications</h4>
            <div class="entry-sub">DePaul Institute of Science and Technology, Angamaly.</div>
        </div>

        <a href="./assets/docs/resume_tcs.pdf" class="btn-action">Download_Full_Resume</a>

        <footer>
            NITHIN_PRASAD_DEV // 2026 // NO_EMOJIS_ALLOWED
        </footer>
    </div>
</body>
</html>
