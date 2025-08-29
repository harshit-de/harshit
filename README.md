<!doctype html>

<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>My Simple Page</title>
    <style>
      /* --- Minimal, clean styles --- */
      :root {
        --bg: #f8fafc;
        --card: #ffffff;
        --text: #0f172a;
        --muted: #475569;
        --primary: #2563eb;
        --ring: rgba(37, 99, 235, 0.35);
      }
      * { box-sizing: border-box; }
      html, body { height: 100%; }
      body {
        margin: 0;
        font: 16px/1.5 system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, "Helvetica Neue", Arial, "Noto Sans", sans-serif;
        color: var(--text);
        background: radial-gradient(1200px 600px at 10% -10%, #e8eefc 0, transparent 60%), var(--bg);
      }
      .container { max-width: 960px; margin: 0 auto; padding: 24px; }
      header {
        position: sticky; top: 0; z-index: 10;
        backdrop-filter: saturate(180%) blur(8px);
        background: rgba(255,255,255,0.7);
        border-bottom: 1px solid #e5e7eb;
      }
      header .inner { display: flex; align-items: center; justify-content: space-between; padding: 14px 24px; }
      nav a { text-decoration: none; color: var(--muted); margin-left: 14px; }
      nav a:hover { color: var(--text); }
      .hero { padding: 56px 24px 32px; text-align: center; }
      .hero h1 { font-size: clamp(28px, 4vw, 40px); margin: 0 0 12px; }
      .hero p { color: var(--muted); margin: 0 0 20px; }
      .btn { display: inline-block; padding: 12px 18px; border-radius: 999px; border: 1px solid #dbeafe; background: var(--primary); color: #fff; text-decoration: none; box-shadow: 0 6px 16px -6px var(--ring); }
      .btn:hover { filter: brightness(0.95); }
      .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 16px; margin-top: 28px; }
      .card { background: var(--card); border: 1px solid #e5e7eb; border-radius: 16px; padding: 18px; box-shadow: 0 10px 20px -18px rgba(0,0,0,0.3); }
      .card h3 { margin: 0 0 6px; font-size: 18px; }
      footer { text-align: center; color: var(--muted); padding: 28px; }
      form { display: grid; gap: 12px; margin-top: 10px; }
      input, textarea { width: 100%; padding: 10px 12px; border: 1px solid #cbd5e1; border-radius: 10px; background: #fff; font: inherit; }
      input:focus, textarea:focus { outline: none; box-shadow: 0 0 0 4px var(--ring); border-color: var(--primary); }
    </style>
  </head>
  <body>
    <header>
      <div class="inner container">
        <strong>MySite</strong>
        <nav>
          <a href="#about">About</a>
          <a href="#features">Features</a>
          <a href="#contact">Contact</a>
        </nav>
      </div>
    </header><main class="container">
  <!-- Hero / intro section -->
  <section class="hero" id="about">
    <h1>Welcome to your simple HTML page 👋</h1>
    <p>A clean starter you can copy, edit, and learn from. No frameworks, just HTML + CSS.</p>
    <a class="btn" href="#features">Explore features</a>
  </section>

  <!-- Feature cards -->
  <section id="features" aria-labelledby="features-title">
    <h2 id="features-title">Features</h2>
    <div class="grid">
      <article class="card">
        <h3>Semantic layout</h3>
        <p>Uses <code>&lt;header&gt;</code>, <code>&lt;main&gt;</code>, <code>&lt;section&gt;</code>, and <code>&lt;footer&gt;</code> for accessibility.</p>
      </article>
      <article class="card">
        <h3>Responsive grid</h3>
        <p>Cards wrap automatically with <code>grid</code> and <code>minmax</code> for small screens.</p>
      </article>
      <article class="card">
        <h3>Minimal CSS</h3>
        <p>A tiny, readable stylesheet you can tweak in one place.</p>
      </article>
      <article class="card">
        <h3>Form example</h3>
        <p>Ready-made inputs with focus styles and a rounded submit button.</p>
      </article>
    </div>
  </section>

  <!-- Contact form -->
  <section id="contact" style="margin-top: 40px;">
    <h2>Contact</h2>
    <p>Send a quick message (no backend required for this demo).</p>
    <form onsubmit="event.preventDefault(); alert('Thanks! This demo form does not submit anywhere.');">
      <label>
        Name
        <input type="text" name="name" placeholder="Your name" required />
      </label>
      <label>
        Email
        <input type="email" name="email" placeholder="you@example.com" required />
      </label>
      <label>
        Message
        <textarea name="message" rows="4" placeholder="Say hello…" required></textarea>
      </label>
      <button class="btn" type="submit">Send message</button>
    </form>
  </section>
</main>

<footer>
  <small>© <span id="year"></span> MySite. Built with ♥ using plain HTML & CSS.</small>
</footer>

<script>
  // Tiny enhancement: keep copyright year current
  document.getElementById('year').textContent = new Date().getFullYear();
</script>

  </body>
</html>
