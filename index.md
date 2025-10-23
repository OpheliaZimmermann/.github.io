<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Réglages – Corps de page</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    html,body{background:#f7f7f9}
    .page{max-width:1100px;margin:40px auto;padding:24px;background:#fff;border:1px solid rgba(0,0,0,.06);border-radius:12px}
    .koMenuSectionTitle{font-weight:600;margin:24px 0 12px}
    .form-label{font-weight:500}
    .hint{font-size:.9rem;color:#6c757d}
  </style>
</head>
<body>
  <main class="page">
    <h1 class="h4 mb-4">Réglages d’apparence (corps de page uniquement)</h1>

    <div class="row g-4">

      <!-- Colonne 1 -->
      <div class="col-12 col-lg-6">
        <div class="koMenuSectionTitle">Propriétés du texte</div>

        <div class="mb-3">
          <label for="txtColor" class="form-label">Couleur du texte</label>
          <input type="color" class="form-control form-control-color" id="txtColor" value="#222222" title="Choisir une couleur">
        </div>

        <div class="koMenuSectionTitle">Arrière-plan</div>
        <div class="mb-3">
          <label for="bgColor" class="form-label">Couleur d'arrière-plan</label>
          <input type="color" class="form-control form-control-color" id="bgColor" value="#ffffff" title="Choisir une couleur">
        </div>

        <div class="koMenuSectionTitle">Bordure</div>
        <div class="row g-3">
          <div class="col-6">
            <label for="borderWidth" class="form-label">Largeur de bordure</label>
            <div class="input-group input-group-sm">
              <input type="number" class="form-control" id="borderWidth" min="0" max="20" step="1" value="0">
              <span class="input-group-text">px</span>
            </div>
          </div>
          <div class="col-6">
            <label for="borderRadius" class="form-label">Rayon</label>
            <div class="input-group input-group-sm">
              <input type="number" class="form-control" id="borderRadius" min="0" max="50" step="1" value="0">
              <span class="input-group-text">px</span>
            </div>
          </div>
          <div class="col-12">
            <label for="borderColor" class="form-label">Couleur de la bordure</label>
            <input type="color" class="form-control form-control-color" id="borderColor" value="#dddddd" title="Choisir une couleur">
          </div>
        </div>
      </div>

      <!-- Colonne 2 (états : hover / accent 2, etc.) -->
      <div class="col-12 col-lg-6">
        <div class="koMenuSectionTitle">État : survol (hover)</div>
        <div class="mb-3">
          <label for="txtColorHover" class="form-label">Couleur du texte (hover)</label>
          <input type="color" class="form-control form-control-color" id="txtColorHover" value="#000000">
        </div>
        <div class="mb-3">
          <label for="bgColorHover" class="form-label">Couleur d'arrière-plan (hover)</label>
          <input type="color" class="form-control form-control-color" id="bgColorHover" value="#f2f2f2">
        </div>
        <div class="mb-3">
          <label for="borderColorHover" class="form-label">Couleur de la bordure (hover)</label>
          <input type="color" class="form-control form-control-color" id="borderColorHover" value="#cccccc">
        </div>

        <div class="koMenuSectionTitle">Accent #2</div>
        <div class="mb-3">
          <label for="acc2Text" class="form-label">Couleur du texte (accent #2)</label>
          <input type="color" class="form-control form-control-color" id="acc2Text" value="#ffffff">
        </div>
        <div class="mb-3">
          <label for="acc2Bg" class="form-label">Couleur d’arrière-plan (accent #2)</label>
          <input type="color" class="form-control form-control-color" id="acc2Bg" value="#007bff">
        </div>
        <div class="mb-3">
          <label for="acc2Border" class="form-label">Couleur de la bordure (accent #2)</label>
          <input type="color" class="form-control form-control-color" id="acc2Border" value="#007bff">
        </div>
      </div>
    </div>

    <hr class="my-4">

    <div class="d-flex gap-2">
      <button id="apply" class="btn btn-primary">Appliquer au bloc d’exemple</button>
      <button id="reset" class="btn btn-outline-secondary">Réinitialiser</button>
    </div>

    <p class="hint mt-3">Astuce : cette page ne contient ni barre de menu ni pied de page – uniquement le corps.</p>

    <div id="preview" class="mt-4 p-4 border rounded">
      <strong>Bloc d’exemple</strong>
      <p class="mb-0">Survolez ce bloc pour tester les couleurs “hover”.</p>
    </div>
  </main>

  <script>
    const els = {
      txtColor: txtColor,
      bgColor: bgColor,
      borderWidth: borderWidth,
      borderRadius: borderRadius,
      borderColor: borderColor,
      txtColorHover: txtColorHover,
      bgColorHover: bgColorHover,
      borderColorHover: borderColorHover,
      acc2Text: acc2Text,
      acc2Bg: acc2Bg,
      acc2Border: acc2Border,
      preview: document.getElementById('preview'),
      apply: document.getElementById('apply'),
      reset: document.getElementById('reset')
    };

    function applyStyles() {
      const p = els.preview.style;
      p.color = els.txtColor.value;
      p.background = els.bgColor.value;
      p.borderWidth = (parseInt(els.borderWidth.value)||0) + 'px';
      p.borderStyle = 'solid';
      p.borderColor = els.borderColor.value;
      p.borderRadius = (parseInt(els.borderRadius.value)||0) + 'px';
    }

    function setHover() {
      const base = {
        color: els.txtColor.value,
        background: els.bgColor.value,
        borderColor: els.borderColor.value
      };
      const hover = {
        color: els.txtColorHover.value,
        background: els.bgColorHover.value,
        borderColor: els.borderColorHover.value
      };
      els.preview.onmouseenter = () => {
        els.preview.style.color = hover.color;
        els.preview.style.background = hover.background;
        els.preview.style.borderColor = hover.borderColor;
      };
      els.preview.onmouseleave = () => {
        els.preview.style.color = base.color;
        els.preview.style.background = base.background;
        els.preview.style.borderColor = base.borderColor;
      };
    }

    els.apply.addEventListener('click', () => { applyStyles(); setHover(); });
    els.reset.addEventListener('click', () => { document.querySelector('form')?.reset(); location.reload(); });

    // init
    applyStyles(); setHover();
  </script>
</body>
</html>
