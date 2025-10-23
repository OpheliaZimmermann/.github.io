<!doctype html>
<html lang="fr">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>t'occupe — Page</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Playfair+Display:wght@600&display=swap" rel="stylesheet">
    <style>
      :root{
        --bg: #0f0f12;
        --panel: #141419;
        --muted: #a6a6b0;
        --text: #f2f2f7;
        --accent: #8ea6ff;
        --ring: 24, 24, 28;
        --radius: 18px;
        --maxw: 1080px;
      }
      * { box-sizing: border-box; }
      html, body { height: 100%; }
      body {
        margin: 0;
        background: radial-gradient(1200px 800px at 80% -10%, rgba(142,166,255,.15), transparent 60%),
                    radial-gradient(900px 600px at -10% 90%, rgba(142,166,255,.08), transparent 60%),
                    var(--bg);
        color: var(--text);
        font-family: Inter, ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Apple Color Emoji", "Segoe UI Emoji";
        line-height: 1.55;
        -webkit-font-smoothing: antialiased; -moz-osx-font-smoothing: grayscale;
      }
      .wrap { max-width: var(--maxw); margin: 0 auto; padding: 48px 20px 80px; }

      /* Hero */
      .hero { display: grid; grid-template-columns: 1.1fr .9fr; gap: 36px; align-items: center; }
      .brand { display:flex; align-items:center; gap:14px; margin-bottom: 18px; opacity:.9 }
      .logo { width: 40px; height: 40px; border-radius: 10px; background: linear-gradient(135deg, #8ea6ff, #b38bff); box-shadow: 0 8px 30px rgba(142,166,255,.35); }
      .brand h1 { font-family: "Playfair Display", serif; font-size: clamp(28px, 3.2vw, 44px); letter-spacing: .2px; margin: 0; }
      .tag { display:inline-block; font-size: 12px; text-transform: uppercase; letter-spacing:.12em; color: var(--muted); }
      .lead { font-size: clamp(16px, 1.6vw, 18px); color: #d8d8e1; margin: 14px 0 22px; }

      .hero img { width: 100%; height: auto; border-radius: var(--radius); display:block; border:1px solid rgba(255,255,255,.06); box-shadow: 0 12px 50px rgba(0,0,0,.45); }

      /* Sections */
      .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 26px; }
      .card { background: linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.0)); border: 1px solid rgba(255,255,255,.08); border-radius: var(--radius); padding: 22px; box-shadow: 0 6px 24px rgba(0,0,0,.35); }
      .card h2 { margin: 4px 0 8px; font-size: clamp(20px, 2.2vw, 26px); }
      .card h3 { margin: 0 0 6px; font-weight: 600; font-size: 14px; letter-spacing: .04em; color: var(--muted); text-transform: uppercase; }
      .card p { margin: 0; color: #e9e9f1; }

      /* Contact strip */
      .contact { margin-top: 36px; display:flex; flex-wrap:wrap; gap:12px; align-items:center; }
      .pill { background: rgba(255,255,255,.06); border:1px solid rgba(255,255,255,.08); color: #fff; padding: 10px 14px; border-radius: 999px; font-size: 14px; }
      .pill a { color: #fff; text-decoration: none; }
      .pill a:hover { text-decoration: underline; }

      /* Language switch (static, décoratif) */
      .langs { margin-left:auto; display:flex; gap:8px; align-items:center; }
      .langs a { font-size: 12px; color: var(--muted); text-decoration: none; border:1px solid rgba(255,255,255,.08); padding:6px 10px; border-radius: 999px; }
      .langs a.active { color: #111; background: #fff; border-color:#fff; }

      @media (max-width: 960px) {
        .hero { grid-template-columns: 1fr; }
        .grid { grid-template-columns: 1fr; }
        .langs { width: 100%; justify-content: flex-start; margin-top: 6px; }
      }
    </style>
  </head>
  <body>
    <div class="wrap">
      <!-- HERO -->
      <section class="hero">
        <div>
          <div class="brand">
            <div class="logo" aria-hidden="true"></div>
            <h1>t'occupe</h1>
          </div>
          <div class="tag">Français · English · Deutsch · Español</div>
          <p class="lead">Explorations en data science et photographie. Donner du sens aux données et raconter l'humain par la lumière et les gestes du quotidien.</p>
          <div class="grid">
            <article class="card">
              <h3>Data Science</h3>
              <h2>Analyse de données</h2>
              <p>Spécialisée en biomédical et comportemental, j'exploite des méthodes statistiques éprouvées et du machine learning adapté aux enjeux, de l'exploration à la mise en production.</p>
            </article>
            <article class="card">
              <h3>Photographie</h3>
              <h2>Regards et lumières</h2>
              <p>Une autre façon d’explorer l’humain : préférer la spontanéité à la perfection pour saisir ce que les mots ne disent pas toujours.</p>
            </article>
          </div>
        </div>
        <div>
          <!-- Remplacez la source par votre image locale (par ex. assets/visuel.jpg) -->
          <img src="https://picsum.photos/900/1200" alt="Visuel illustratif" />
        </div>
      </section>

      <!-- CONTACT (pas de menu ni de pied de page) -->
      <div class="contact" role="contentinfo" aria-label="Coordonnées">
        <span class="pill">t'occupe</span>
        <span class="pill"><a href="mailto:contact@example.com">contact@example.com</a></span>
        <nav class="langs" aria-label="Langues (démo)">
          <a class="active" href="#" aria-current="page">FR</a>
          <a href="#">EN</a>
          <a href="#">DE</a>
          <a href="#">ES</a>
        </nav>
      </div>
    </div>
  </body>
</html>