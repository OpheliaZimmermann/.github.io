<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Projets — Sweet &amp; Co.</title>
  <meta name="description" content="Les projets de Sweet &amp; Co." />

  <!-- Minimal, self-contained styles (no CDNs, no images) -->
  <style>
    :root{
      --c1:#1c3144; /* bleu foncé */
      --c2:#618cc5; /* bleu clair */
      --text:#222;
      --muted:#6b7280;
      --bg:#f8f9fa;
      --maxw: 1000px;
    }
    * { box-sizing: border-box; }
    html, body { margin:0; padding:0; }
    body {
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, "Helvetica Neue", Arial, "Noto Sans", "Liberation Sans", sans-serif;
      color: var(--text);
      background: #fff;
      line-height: 1.6;
    }
    a { color: var(--c1); text-decoration: none; }
    a:hover { text-decoration: underline; }

    .container { width: 100%; max-width: var(--maxw); margin: 0 auto; padding: 0 16px; }

    header {
      background: var(--c1);
      color: #fff;
      border-bottom: 1px solid rgba(255,255,255,.1);
    }
    .header-inner {
      display: flex; align-items: center; justify-content: space-between;
      padding: 16px 0;
    }
    .brand { font-weight: 700; letter-spacing: .3px; }
    nav ul { list-style: none; margin: 0; padding: 0; display: flex; gap: 8px; flex-wrap: wrap; }
    nav a {
      display: inline-block; padding: 10px 14px; border-radius: 6px; color: #fff;
      text-transform: uppercase; font-size: 14px; letter-spacing: .4px;
    }
    nav a:hover, nav a.active { background: rgba(255,255,255,.12); }

    main { padding: 40px 0; background: var(--bg); }
    h1 {
      font-size: clamp(28px, 4vw, 40px);
      color: var(--c1);
      margin: 0 0 8px 0;
      line-height: 1.2;
      text-align: center;
    }
    .sep { width: 100px; height: 4px; margin: 12px auto 32px; background: var(--c1); border-radius: 2px; }

    .content { display: grid; grid-template-columns: 1fr; gap: 32px; }
    .lead { font-size: 18px; color: var(--text); }

    ol.projects { font-size: 20px; margin: 0; padding-left: 22px; }
    ol.projects li { margin: 10px 0; }
    ol.projects li strong { color: var(--c2); }

    footer { background: var(--bg); border-top: 1px solid #e5e7eb; }
    .footer-inner { padding: 32px 0; display: grid; grid-template-columns: 1fr; gap: 24px; }
    .footer-brand { font-weight: 700; color: var(--c1); }
    .muted { color: var(--muted); }

    .footer-links { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 16px; }
    .footer-links h5 { margin: 0 0 8px; color: var(--c1); font-size: 16px; }
    .footer-links ul { list-style: none; margin: 0; padding: 0; }
    .footer-links li { margin: 6px 0; }

    .footer-bottom {
      border-top: 1px solid #e5e7eb; padding: 16px 0; display: flex; gap: 12px;
      align-items: center; justify-content: space-between; flex-wrap: wrap;
    }
    .social { display: inline-flex; gap: 12px; }
    .social a { color: var(--c1); font-weight: 600; }
  </style>
</head>
<body>

  <!-- Header / Menu -->
  <header>
    <div class="container header-inner">
      <div class="brand">Sweet &amp; Co.</div>
      <nav aria-label="Menu principal">
        <ul>
          <li><a href="https://sweetandco.ch">Home</a></li>
          <li><a class="active" href="./projets.html">Projets</a></li>
          <li><a href="https://sweetandco.ch/ressources">Ressources</a></li>
          <li><a href="https://sweetandco.ch/team">Team</a></li>
          <li><a href="https://sweetandco.ch/nous-soutenir">Nous soutenir</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Main -->
  <main>
    <div class="container">
      <h1>Projets</h1>
      <div class="sep" aria-hidden="true"></div>

      <div class="content">
        <section class="lead">
          <ol class="projects">
            <li>
              <a href="./formulaire-bingo.html">Grand BINGO du diabète</a>
            </li>
            <li>
              <strong>Des ateliers Do-It-Yourself</strong><br />
              On prévoit d'organiser des ateliers pour démocratiser l'usage des techs et surtout s'amuser.
              Différents jeux vous seront également proposés.
            </li>
            <li>
              <strong>Soutien technique</strong><br />
              Si vous souhaitez une aide technique ponctuelle pour l'usage des applications open-source,
              n’hésitez pas à nous contacter. On fera de notre mieux pour vous aiguiller dans les limites de nos compétences.
            </li>
          </ol>
        </section>
      </div>
    </div>
  </main>

  <!-- Footer -->
  <footer>
    <div class="container footer-inner">
      <div>
        <div class="footer-brand">Sweet &amp; Co.</div>
        <div class="muted">contact@sweetandco.ch</div>
      </div>

      <div class="footer-links">
        <div>
          <h5>Main menu</h5>
          <ul>
            <li><a href="https://sweetandco.ch/">Home</a></li>
            <li><a href="./projets.html">Projets</a></li>
            <li><a href="https://sweetandco.ch/ressources">Ressources</a></li>
            <li><a href="https://sweetandco.ch/team">Team</a></li>
            <li><a href="https://sweetandco.ch/nous-soutenir">Nous soutenir</a></li>
          </ul>
        </div>
        <div>
          <h5>Legal</h5>
          <ul>
            <li><a href="https://sweetandco.ch/mentions-legales">Mentions légales</a></li>
            <li><a href="https://sweetandco.ch/politique-de-confidentialite">Politique de confidentialité</a></li>
            <li><a href="https://sweetandco.ch/nos-statuts">Nos Statuts</a></li>
          </ul>
        </div>
      </div>

      <div class="footer-bottom">
        <div class="muted">Copyright ©2025 — All rights reserved.</div>
        <div class="social">
          <a href="https://instagram.com/_sweet_and_co._" target="_blank" rel="noopener">Instagram</a>
          <span>•</span>
          <a href="mailto:contact@sweetandco.ch">Email</a>
        </div>
      </div>
    </div>
  </footer>

</body>
</html>
