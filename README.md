<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Dark & Lovely</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Playfair+Display:wght@500;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0b0b10;
      --card:#12121a;
      --accent:#ff4d8d;
      --accent-soft:#ff7aa8;
      --text:#e9e9f1;
      --muted:#a7a7c2;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      background: radial-gradient(1200px 600px at 10% 10%, #151526 0%, var(--bg) 45%),
                  radial-gradient(800px 400px at 90% 90%, #1a0f1f 0%, var(--bg) 55%);
      color:var(--text);
      font-family:Poppins, system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
      overflow-x:hidden;
    }
    header{
      position:sticky; top:0; z-index:10;
      backdrop-filter: blur(10px);
      background: linear-gradient(to bottom, rgba(11,11,16,.7), rgba(11,11,16,.35));
      border-bottom:1px solid rgba(255,255,255,.06);
    }
    nav{
      max-width:1100px; margin:auto; padding:16px 20px;
      display:flex; align-items:center; justify-content:space-between;
    }
    .logo{font-family:"Playfair Display"; letter-spacing:.5px}
    .logo span{color:var(--accent)}
    nav a{color:var(--muted); text-decoration:none; margin-left:18px}
    nav a:hover{color:var(--text)}

    .hero{
      max-width:1100px; margin:0 auto; padding:90px 20px 70px;
      display:grid; grid-template-columns:1.1fr .9fr; gap:40px; align-items:center;
    }
    .badge{display:inline-block; padding:8px 14px; border-radius:999px;
      background:rgba(255,77,141,.12); color:var(--accent-soft); border:1px solid rgba(255,77,141,.25)}
    h1{
      font-family:"Playfair Display"; font-size:52px; line-height:1.1; margin:18px 0 12px;
    }
    h1 em{color:var(--accent); font-style:normal}
    .hero p{color:var(--muted); max-width:520px}
    .cta{margin-top:26px; display:flex; gap:14px}
    .btn{
      padding:14px 20px; border-radius:14px; border:1px solid rgba(255,255,255,.12);
      background:linear-gradient(135deg, rgba(255,77,141,.25), rgba(255,77,141,.05));
      color:var(--text); cursor:pointer; transition:.25s ease; text-decoration:none
    }
    .btn.primary{background:linear-gradient(135deg, #ff4d8d, #ff7aa8); border:none}
    .btn:hover{transform:translateY(-2px); box-shadow:0 10px 30px rgba(0,0,0,.35)}

    .card{
      background:linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02));
      border:1px solid rgba(255,255,255,.08); border-radius:24px; padding:26px;
      box-shadow:0 20px 50px rgba(0,0,0,.45)
    }
    .orb{
      width:260px; height:260px; border-radius:50%; margin:auto;
      background: radial-gradient(circle at 30% 30%, #ff9cc2, #ff4d8d 40%, #7a1439 65%, #2b0a18 72%);
      filter: blur(0.2px);
      animation: float 6s ease-in-out infinite;
    }
    @keyframes float{50%{transform:translateY(-16px)}}

    section.features{max-width:1100px; margin:0 auto; padding:20px 20px 80px}
    .grid{display:grid; grid-template-columns:repeat(3,1fr); gap:20px}
    .feature h3{margin:10px 0}
    .feature p{color:var(--muted)}

    footer{
      border-top:1px solid rgba(255,255,255,.06);
      padding:26px 20px; text-align:center; color:var(--muted)
    }

    @media(max-width:900px){
      .hero{grid-template-columns:1fr}
      h1{font-size:40px}
      .grid{grid-template-columns:1fr}
    }
  </style>
</head>
<body>
  <header>
    <nav>
      <div class="logo">Dark<span>Lovely</span></div>
      <div>
        <a href="#">Home</a>
        <a href="#features">Features</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero">
      <div>
        <span class="badge">dark • romantic • elegant</span>
        <h1>A <em>dark</em> theme with a <em>lovely</em> heart</h1>
        <p>Soft glow, deep tones, and gentle motion. A calm, romantic space that feels modern and warm at the same time.</p>
        <div class="cta">
          <a class="btn primary" href="#features">Explore</a>
          <a class="btn" href="#contact">Say Hello</a>
        </div>
      </div>
      <div class="card"><div class="orb"></div></div>
    </section>

    <section id="features" class="features">
      <div class="grid">
        <div class="card feature">
          <h3>🌙 Dark Aesthetic</h3>
          <p>Comfortable on the eyes with deep gradients and soft highlights.</p>
        </div>
        <div class="card feature">
          <h3>💖 Lovely Touch</h3>
          <p>Romantic accent colors, smooth curves, and gentle animations.</p>
        </div>
        <div class="card feature">
          <h3>⚡ Fast & Clean</h3>
          <p>Simple HTML + CSS. Easy to customize and deploy anywhere.</p>
        </div>
      </div>
    </section>
  </main>

  <footer id="contact">
    Made with ❤️ in the dark · © 2026 DarkLovely
  </footer>
</body>
</html>
