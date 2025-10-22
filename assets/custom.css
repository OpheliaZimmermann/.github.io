/* Two-panel landing for Cayman */
:root{
  --bg:#0f1115; --panel:#151a23; --text:#e8ecf3; --muted:#a4afc3;
  --brand:#8b9dff; --brand2:#9de1d6; --border:#202636;
}
@media (prefers-color-scheme: light){
  :root{ --bg:#f7f8fb; --panel:#ffffff; --text:#161922; --muted:#5a6478; --border:#e6e8ee; }
}
body{ font-family: 'Inter', system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif; color:var(--text); }

.split-landing{
  display:grid; grid-template-columns:1fr 1fr; gap:12px;
  width:min(1100px, 92%); margin:36px auto 0;
}
.panel{ position:relative; display:block; overflow:hidden; border-radius:16px; border:1px solid var(--border); }
.panel img{ width:100%; height:62vh; min-height:360px; object-fit:cover; transform:scale(1.02); transition:transform .35s ease; display:block; }
.panel .overlay{
  position:absolute; inset:0; display:grid; place-content:center; text-align:center;
  background:linear-gradient(180deg, rgba(0,0,0,.0), rgba(0,0,0,.35) 55%, rgba(0,0,0,.55));
  color:#fff; opacity:0; transition:opacity .25s ease, backdrop-filter .25s ease;
  padding:16px;
}
.panel h2{ margin:.2rem 0 0; font-size:clamp(22px,3.6vw,34px); }
.panel p{ margin:.2rem 0 0; opacity:.9 }
.panel:hover img, .panel:focus-visible img{ transform:scale(1.06); }
.panel:hover .overlay, .panel:focus-visible .overlay{ opacity:1; backdrop-filter: blur(2px); }
.panel.left .overlay h2{ text-shadow: 0 6px 24px rgba(139,157,255,.6); }
.panel.right .overlay h2{ text-shadow: 0 6px 24px rgba(157,225,214,.6); }

.center{ text-align:center } .small{ font-size:.92rem } .muted{ color:var(--muted) }

@media (max-width: 860px){
  .split-landing{ grid-template-columns:1fr; }
  .panel img{ height:46vh; }
}
