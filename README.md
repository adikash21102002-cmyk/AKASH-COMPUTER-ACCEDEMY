<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Computer Learning - Emergent Agent Preview</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Inter', sans-serif; background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 100%); color: white; overflow-x: hidden; }
        .hero { height: 100vh; display: flex; align-items: center; justify-content: space-between; max-width: 1400px; margin: 0 auto; padding: 0 5%; }
        .hero-content { max-width: 600px; }
        h1 { font-size: 4rem; font-weight: 800; line-height: 1.1; margin-bottom: 1.5rem; background: linear-gradient(135deg, #fff, #a0a0ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .subtitle { font-size: 1.3rem; margin-bottom: 2rem; opacity: 0.9; }
        .cta-button { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); padding: 1rem 2rem; border: none; border-radius: 50px; font-size: 1.1rem; font-weight: 600; cursor: pointer; transition: all 0.3s; box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4); }
        .cta-button:hover { transform: translateY(-3px); box-shadow: 0 20px 40px rgba(102, 126, 234, 0.6); }
        .demo-section { position: absolute; right: 5%; width: 500px; height: 70%; background: rgba(255,255,255,0.05); border-radius: 20px; backdrop-filter: blur(20px); border: 1px solid rgba(255,255,255,0.1); padding: 2rem; }
        .terminal { background: #000; border-radius: 10px; padding: 1.5rem; height: 60%; overflow: hidden; font-family: 'Courier New', monospace; font-size: 0.9rem; }
        .terminal-line { margin: 0.5rem 0; animation: type 0.5s ease-out; }
        @keyframes type { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }
        .features { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; max-width: 1200px; margin: 5rem auto; padding: 0 5%; }
        .feature-card { background: rgba(255,255,255,0.05); border-radius: 20px; padding: 2rem; backdrop-filter: blur(20px); border: 1px solid rgba(255,255,255,0.1); transition: transform 0.3s; }
        .feature-card:hover { transform: translateY(-10px); }
        .feature-icon { font-size: 3rem; margin-bottom: 1rem; }
    </style>
</head>
<body>
    <section class="hero">
        <div class="hero-content">
            <h1>Build AI Apps<br>that Actually Work</h1>
            <p class="subtitle">Computer Learning platform powered by Emergent Agent. Chat with AI agents that design, code, and deploy your app automatically.</p>
            <button class="cta-button" onclick="startDemo()">Start Building →</button>
        </div>
        <div class="demo-section">
            <h3 style="margin-bottom: 1rem; color: #667eea;">Live Preview</h3>
            <div class="terminal" id="terminal">
                <div class="terminal-line">emergent@computer-learning:~$ emergent init</div>
                <div class="terminal-line">> Creating project structure...</div>
                <div class="terminal-line">> Frontend agent: React + Tailwind</div>
                <div class="terminal-line">> Backend agent: Node + Express</div>
                <div class="terminal-line">✓ Deployment ready in 2:47</div>
                <div class="terminal-line">> Ready to deploy? (y/n)</div>
            </div>
        </div>
    </section>

    <section class="features">
        <div class="feature-card">
            <div class="feature-icon">🚀</div>
            <h3>Full-Stack Automation</h3>
            <p>AI agents handle frontend, backend, database, and deployment simultaneously.</p>
        </div>
        <div class="feature-card">
            <div class="feature-icon">⚡</div>
            <h3>Production Ready</h3>
            <p>No templates. Real apps with auth, payments, and hosting included.</p>
        </div>
        <div class="feature-card">
            <div class="feature-icon">🧠</div>
            <h3>Multi-Agent Teams</h3>
            <p>Specialized agents collaborate: Frontend, Backend, QA, DevOps.</p>
        </div>
    </section>

    <script>
        function startDemo() {
            const terminal = document.getElementById('terminal');
            terminal.innerHTML += '<div class="terminal-line">> Building your app...</div>';
            setTimeout(() => {
                terminal.innerHTML += '<div class="terminal-line">✓ App deployed: https://your-app.emergentagent.com</div>';
            }, 1500);
        }

        // Typewriter effect
        const lines = document.querySelectorAll('.terminal-line');
        lines.forEach((line, index) => {
            line.style.animationDelay = `${index * 0.2}s`;
        });
    </script>
</body>
</html>
