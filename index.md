---
layout: null
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nithin Prasad | Systems Developer</title>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&family=Space+Mono&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
    <style>
        :root { 
            --bg: #030303; 
            --card-bg: rgba(10, 10, 10, 0.8); 
            --text: #ffffff; 
            --accent: #facc15; /* Cyber Yellow */
            --secondary: #64748b;
            --border: rgba(250, 204, 21, 0.2);
        }

        body { 
            background-color: var(--bg);
            color: var(--text); 
            font-family: 'Space Grotesk', sans-serif; 
            margin: 0; 
            padding: 0;
            line-height: 1.5;
            overflow-x: hidden;
        }

        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: -1;
            top: 0;
            left: 0;
        }

        .container { max-width: 1000px; margin: 0 auto; padding: 100px 24px; position: relative; z-index: 1; }
        
        header { margin-bottom: 100px; }
        .prefix { font-family: 'Space Mono', monospace; color: var(--accent); font-size: 0.9rem; letter-spacing: 2px; }
        h1 { font-size: clamp(3rem, 10vw, 5rem); margin: 10px 0; font-weight: 700; letter-spacing: -3px; }
        .tagline { font-size: 1.25rem; color: var(--secondary); max-width: 600px; border-left: 3px solid var(--accent); padding-left: 20px; }

        .label { font-family: 'Space Mono', monospace; font-size: 0.75rem; color: var(--accent); text-transform: uppercase; letter-spacing: 4px; display: block; margin: 80px 0 30px 0; }

        /* Animated Glass Cards */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 20px; }
        .card { 
            background: var(--card-bg); 
            padding: 40px; 
            border: 1px solid var(--border); 
            backdrop-filter: blur(12px);
            transition: all 0.4s cubic-bezier(0.19, 1, 0.22, 1);
            position: relative;
        }

        .card:hover { 
            border-color: var(--accent); 
            background: rgba(250, 204, 21, 0.03);
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
        }

        .card h3 { margin: 0 0 15px 0; font-size: 1.5rem; letter-spacing: -1px; }
        .card p { color: var(--secondary); font-size: 1rem; margin-bottom: 25px; }
        
        .tags { display: flex; flex-wrap: wrap; gap: 8px; font-family: 'Space Mono', monospace; font-size: 0.7rem; }
        .tags span { border: 1px solid var(--border); padding: 4px 10px; color: var(--accent); }

        /* Timeline Items */
        .item { margin-bottom: 40px; padding: 25px; border: 1px solid transparent; transition: 0.3s; }
        .item:hover { border-color: var(--border); background: var(--card-bg); }
        .item h4 { margin: 0; font-size: 1.2rem; }
        .item-date { font-family: 'Space Mono', monospace; font-size: 0.8rem; color: var(--accent); margin-bottom: 8px; }
        .item-sub { color: var(--secondary); font-size: 0.95rem; }

        /* Buttons & Footer */
        .btn { 
            display: inline-block; 
            margin-top: 60px; 
            padding: 20px 45px; 
            background: var(--accent); 
            color: #000; 
            text-decoration: none; 
            font-family: 'Space Mono', monospace;
            font-weight: 700;
            transition: 0.3s;
        }
        .btn:hover { background: #fff; transform: skewX(-5deg); box-shadow: 8px 8px 0 var(--accent); }

        footer { margin-top: 150px; padding: 50px 0; border-top: 1px solid var(--border); text-align: center; color: #444; font-family: 'Space Mono', monospace; font-size: 0.75rem; }
    </style>
</head>
<body>
    <div id="particles-js"></div>

    <div class="container">
        <header>
            <span class="prefix">_SYSTEM.INITIALIZE()</span>
            <h1>Nithin Prasad</h1>
            <p class="tagline">Software Developer. Proficient in Python and AI-driven automation. Focused on building data-centric projects and coordinating high-impact technical events.</p>
        </header>

        <span class="label">Primary_Deployments</span>
        <div class="grid">
            <div class="card">
                <h3>Insight Gen</h3>
                <p>An Agentic AI Analytics platform enabling autonomous data analysis and professional report generation from English queries.</p>
                <div class="tags"><span>Python</span> <span>CrewAI</span> <span>Streamlit</span></div>
            </div>
            <div class="card">
                <h3>Revo</h3>
                <p>Social news Android application featuring content rating and insightful community discussions.</p>
                <div class="tags"><span>Java</span> <span>Android</span> <span>Firebase</span></div>
            </div>
            <div class="card">
                <h3>PROFEXIA</h3>
                <p>A web-based skill-barter platform designed for community-driven skill exchange without financial dependency.</p>
                <div class="tags"><span>Django</span> <span>Python</span> <span>SQL</span></div>
            </div>
            <div class="card">
                <h3>Child_Vaccination_System</h3>
                <p>Digital management system developed to streamline tracking and notification processes for pediatric schedules.</p>
                <div class="tags"><span>JavaScript</span> <span>HTML5</span> <span>SQL</span></div>
            </div>
        </div>

        <span class="label">Technical_Certifications</span>
        <div class="grid" style="grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));">
            <div class="item" style="padding: 15px;">Elite Silver // Cloud Computing</div>
            <div class="item" style="padding: 15px;">Generative AI // IBM</div>
            <div class="item" style="padding: 15px;">React Apps // IBM</div>
            <div class="item" style="padding: 15px;">Full Stack Python // ICT Academy</div>
            <div class="item" style="padding: 15px;">AI for Everyone // DeepLearning.AI</div>
        </div>

        <span class="label">Events_&_Coordination</span>
        <div class="item">
            <div class="item-date">MAR 2026 // Hackathon</div>
            <h4>Main Coordinator | Hackastra 2026</h4>
            <p class="item-sub">Managed end-to-end execution of a 21-hour hackathon themed "Design for Human Weakness".</p>
        </div>
        <div class="item">
            <div class="item-date">OCT 2025 // Dept</div>
            <h4>Main Coordinator | Pragyan Tech Fest</h4>
            <p class="item-sub">Led strategic planning, sponsorship acquisition, and execution for the departmental tech fest.</p>
        </div>
        <div class="item">
            <div class="item-date">APR 2025 // Computer Society of India</div>
            <h4>MCA Representative | CSI SB ASIET</h4>
            <p class="item-sub">Organizing technical symposiums and department-level software workshops.</p>
        </div>

        <span class="label">Education_History</span>
        <div class="item">
            <div class="item-date">2024 - PRESENT // 7.9 GPA</div>
            <h4>Master of Computer Applications</h4>
            <p class="item-sub">Adi Shankara Institute of Engineering and Technology, Kalady.</p>
        </div>
        <div class="item">
            <div class="item-date">2021 - 2024 // 6.7 GPA</div>
            <h4>Bachelor of Computer Applications</h4>
            <p class="item-sub">DePaul Institute of Science and Technology, Angamaly.</p>
        </div>

        <a href="./assets/docs/resume_tcs.pdf" class="btn">_ACCESS_RESUME</a>

        <footer>
            NITHIN_PRASAD_CORE_v4  // 2026
        </footer>
    </div>

    <script>
        particlesJS("particles-js", {
            "particles": {
                "number": { "value": 80, "density": { "enable": true, "value_area": 800 } },
                "color": { "value": "#facc15" },
                "shape": { "type": "circle" },
                "opacity": { "value": 0.2, "random": false },
                "size": { "value": 2, "random": true },
                "line_linked": { "enable": true, "distance": 150, "color": "#facc15", "opacity": 0.1, "width": 1 },
                "move": { "enable": true, "speed": 2, "direction": "none", "random": false, "straight": false, "out_mode": "out", "bounce": false }
            },
            "interactivity": {
                "detect_on": "canvas",
                "events": { "onhover": { "enable": true, "mode": "grab" }, "onclick": { "enable": true, "mode": "push" }, "resize": true },
                "modes": { "grab": { "distance": 140, "line_linked": { "opacity": 0.5 } } }
            },
            "retina_detect": true
        });
    </script>
</body>
</html>
