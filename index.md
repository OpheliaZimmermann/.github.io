<!doctype html>
<html lang="fr">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>t'occupe — Accueil</title>

    <!-- Bootstrap 5 -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

    <!-- AOS (fade-up) -->
    <link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

    <style>
      :root { --bg1: #001F3F; --bg2: #17A2B8; --text: #fff; }
      html, body { height: 100%; margin: 0; padding: 0; }
      body { font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif; background: #0b0f14; color: var(--text); overflow-x: hidden; }

      .position-absolute-expand { position: fixed; inset: 0; pointer-events: none; z-index: 0; }
      .kapp-holder { min-height: 100%; }
      .kapp-holder-m1 { background: var(--bg1); }
      .kapp-holder-m2 { background: var(--bg2); }
      .row.position-absolute-expand > [class*="col-"] { padding: 0; }

      @media (max-width: 991.98px) {
        .row.position-absolute-expand { display: grid; grid-template-rows: 50vh 50vh; }
        .row.position-absolute-expand .col-12 { height: 50vh; }
      }

      main { position: relative; z-index: 1; min-height: 100vh; display: flex; align-items: center; }

      .display-4 { font-weight: 700; letter-spacing: .2px; }
      .leadish { font-size: 22px; line-height: 1.55; }
      .pe-lg-5 { padding-right: 3rem !important; }
      .ps-lg-5 { padding-left: 3rem !important; }

      .image-section { position: relative; z-index: 1; width: 100%; margin: 0; padding: 0; }
      .image-section img { width: 100%; height: auto; display: block; border: none; border-radius: 0; box-shadow: none; }

      .clickable { cursor: pointer; transition: transform 0.15s ease, box-shadow 0.2s ease; }
      .clickable:hover { transform: translateY(-4px); box-shadow: 0 6px 24px rgba(0,0,0,0.4); }
    </style>
  </head>
  <body>

    <div class="row position-absolute-expand">
      <div class="col-12 col-lg-6 kapp-holder kapp-holder-m1"><div data-app="background" class="kapp"></div></div>
      <div class="col-12 col-lg-6 kapp-holder kapp-holder-m2"><div data-app="background" class="kapp"></div></div>
    </div>

    <!-- Image pleine largeur -->
    <section class="image-section keditable keditable-auto">
      <img src="assets/photos/image.png" alt="Visuel principal" data-aos="fade-up" />
    </section>

    <main>
      <div class="container py-5 py-lg-0">
        <div class="row align-items-start">
          <div class="col-12 col-lg-6 pe-lg-5 pb-5 pb-lg-0 clickable" onclick="location.href='statistics/index.md'">
            <div data-aos="fade-up" class="display-4 mb-2"><strong><span style="font-size: 90%;">Data Science</span></strong><div><strong><span style="font-size: 90%;">Analyse de données</span></strong></div></div>
            <div data-aos="fade-up" class="leadish text-justify" style="text-align: justify;">
              Spécialisée en analyse de données biomédicales et comportementales, j'utilise mon savoir-faire pour donner du sens aux données, à travers des outils statistiques éprouvés et des approches de machine learning adaptées.
            </div>
          </div>

          <div class="col-12 col-lg-6 ps-lg-5 pt-5 pt-lg-0 clickable" onclick="location.href='photography/index.md'">
            <div data-aos="fade-up" class="display-4 mb-2">Photographie</div>
            <div data-aos="fade-up" class="leadish text-justify" style="text-align: justify;">
              La photographie est pour moi une autre façon d’explorer l’humain ; par la lumière, les regards et les gestes du quotidien. J’aime capturer la spontanéité et la sincérité plutôt que la perfection, pour raconter ce que les mots ne disent pas toujours.
            </div>
          </div>
        </div>
      </div>
    </main>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-HoA7YJQ5WDaFSC5U9n1K6bIYQz3sR2qN9c2b8w5Jt2oJw8zJ7nQn9v1+9Wtr1J1N" crossorigin="anonymous"></script>
    <script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>
    <script> AOS.init({ once: true, duration: 700, easing: 'ease-out-cubic' }); </script>
  </body>
</html>