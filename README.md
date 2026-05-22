<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Score de Maturité Appels d'Offres — Aconia</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0B0F1A;
    --paper: #F5F2EC;
    --accent: #1A4FFF;
    --accent-dark: #0034CC;
    --muted: #6B7280;
    --border: #D6D0C4;
    --green: #00A878;
    --orange: #E87040;
    --red: #CC2B2B;
    --card: #FEFCF8;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--paper);
    color: var(--ink);
    font-size: 16px;
    line-height: 1.6;
  }

  h1, h2, h3, h4 {
    font-family: 'Syne', sans-serif;
    line-height: 1.15;
  }

  /* ── NAV ── */
  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 48px;
    border-bottom: 1px solid var(--border);
    background: var(--paper);
    position: sticky;
    top: 0;
    z-index: 100;
  }
  .logo {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 1.25rem;
    letter-spacing: -0.02em;
  }
  .logo span { color: var(--accent); }
  nav a {
    color: var(--muted);
    text-decoration: none;
    font-size: 0.9rem;
    font-weight: 500;
    transition: color 0.2s;
  }
  nav a:hover { color: var(--ink); }
  .nav-cta {
    background: var(--ink);
    color: var(--paper) !important;
    padding: 10px 22px;
    border-radius: 6px;
    font-size: 0.875rem !important;
  }
  .nav-cta:hover { background: var(--accent) !important; color: #fff !important; }

  /* ── SECTIONS ── */
  section { max-width: 1080px; margin: 0 auto; padding: 80px 24px; }

  /* ── HERO ── */
  .hero {
    padding: 100px 24px 80px;
    max-width: 1080px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 64px;
    align-items: center;
  }
  .hero-badge {
    display: inline-block;
    background: #E8EEFF;
    color: var(--accent);
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    padding: 6px 14px;
    border-radius: 4px;
    margin-bottom: 24px;
  }
  .hero h1 {
    font-size: clamp(2rem, 4vw, 3.2rem);
    font-weight: 800;
    letter-spacing: -0.03em;
    margin-bottom: 24px;
  }
  .hero h1 em {
    font-style: normal;
    color: var(--accent);
  }
  .hero p {
    color: var(--muted);
    font-size: 1.05rem;
    margin-bottom: 36px;
    max-width: 440px;
    font-weight: 300;
  }
  .hero-cta {
    display: inline-block;
    background: var(--accent);
    color: #fff;
    padding: 16px 32px;
    border-radius: 8px;
    text-decoration: none;
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 1rem;
    transition: all 0.2s;
    box-shadow: 0 4px 20px rgba(26,79,255,0.25);
  }
  .hero-cta:hover {
    background: var(--accent-dark);
    transform: translateY(-2px);
    box-shadow: 0 6px 28px rgba(26,79,255,0.35);
  }
  .hero-sub {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-top: 16px;
    font-size: 0.82rem;
    color: var(--muted);
  }
  .hero-sub span { font-weight: 500; }

  /* Hero card */
  .hero-visual {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 32px;
    position: relative;
  }
  .score-ring {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 8px solid #E8EEFF;
    border-top-color: var(--accent);
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 24px;
    position: relative;
    animation: spin-slow 6s linear infinite;
  }
  @keyframes spin-slow { to { transform: rotate(360deg); } }
  .score-inner {
    animation: counter-spin 6s linear infinite;
    text-align: center;
  }
  @keyframes counter-spin { to { transform: rotate(-360deg); } }
  .score-num {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    color: var(--accent);
  }
  .score-label { font-size: 0.7rem; color: var(--muted); font-weight: 500; }

  .dimension-list { list-style: none; }
  .dimension-list li {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 0;
    border-bottom: 1px solid var(--border);
    font-size: 0.88rem;
  }
  .dimension-list li:last-child { border-bottom: none; }
  .dim-bar {
    width: 80px;
    height: 6px;
    background: #E8EEFF;
    border-radius: 3px;
    overflow: hidden;
  }
  .dim-fill { height: 100%; border-radius: 3px; background: var(--accent); }

  /* ── PROBLEM ── */
  .problem-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
    margin-top: 48px;
  }
  .problem-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 28px;
  }
  .problem-icon {
    font-size: 1.5rem;
    margin-bottom: 16px;
  }
  .problem-card h3 {
    font-size: 1rem;
    font-weight: 700;
    margin-bottom: 10px;
  }
  .problem-card p {
    font-size: 0.88rem;
    color: var(--muted);
    font-weight: 300;
  }

  /* ── QUIZ SECTION ── */
  .quiz-section { background: var(--ink); color: var(--paper); }
  .quiz-section-inner {
    max-width: 1080px;
    margin: 0 auto;
    padding: 80px 24px;
  }
  .section-tag {
    display: inline-block;
    border: 1px solid rgba(255,255,255,0.2);
    color: rgba(255,255,255,0.6);
    font-size: 0.75rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 5px 12px;
    border-radius: 4px;
    margin-bottom: 20px;
  }
  .quiz-section-inner h2 {
    font-size: clamp(1.8rem, 3vw, 2.6rem);
    font-weight: 800;
    letter-spacing: -0.03em;
    max-width: 600px;
    margin-bottom: 16px;
  }
  .quiz-section-inner > p {
    color: rgba(255,255,255,0.55);
    max-width: 560px;
    font-weight: 300;
    margin-bottom: 48px;
  }

  .questions-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
  .q-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 10px;
    padding: 24px;
  }
  .q-num {
    font-family: 'Syne', sans-serif;
    font-size: 0.75rem;
    font-weight: 700;
    color: var(--accent);
    letter-spacing: 0.1em;
    margin-bottom: 10px;
  }
  .q-text {
    font-size: 0.95rem;
    font-weight: 500;
    color: #fff;
    margin-bottom: 14px;
    line-height: 1.4;
  }
  .q-options {
    display: flex;
    flex-direction: column;
    gap: 6px;
  }
  .q-opt {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(255,255,255,0.06);
    border-radius: 6px;
    padding: 8px 12px;
    font-size: 0.8rem;
    color: rgba(255,255,255,0.7);
  }
  .q-pts {
    font-family: 'Syne', sans-serif;
    font-size: 0.7rem;
    font-weight: 700;
    color: var(--accent);
    background: rgba(26,79,255,0.15);
    padding: 2px 7px;
    border-radius: 4px;
  }

  /* ── SCORING ── */
  .scoring-table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 40px;
    font-size: 0.9rem;
  }
  .scoring-table th {
    text-align: left;
    padding: 12px 16px;
    background: var(--ink);
    color: var(--paper);
    font-family: 'Syne', sans-serif;
    font-size: 0.8rem;
    letter-spacing: 0.05em;
  }
  .scoring-table td {
    padding: 14px 16px;
    border-bottom: 1px solid var(--border);
    vertical-align: top;
  }
  .scoring-table tr:last-child td { border-bottom: none; }
  .pts-badge {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 0.8rem;
    background: #E8EEFF;
    color: var(--accent);
    padding: 3px 8px;
    border-radius: 4px;
    white-space: nowrap;
  }

  /* ── RESULTS ── */
  .results-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
    margin-top: 48px;
  }
  .result-card {
    border-radius: 14px;
    padding: 32px 28px;
    border: 1px solid var(--border);
    position: relative;
    overflow: hidden;
  }
  .result-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 4px;
  }
  .result-low::before { background: var(--red); }
  .result-mid::before { background: var(--orange); }
  .result-high::before { background: var(--green); }

  .result-score {
    font-family: 'Syne', sans-serif;
    font-size: 2.2rem;
    font-weight: 800;
    margin-bottom: 4px;
  }
  .result-low .result-score { color: var(--red); }
  .result-mid .result-score { color: var(--orange); }
  .result-high .result-score { color: var(--green); }

  .result-label {
    font-size: 0.75rem;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 16px;
    color: var(--muted);
  }
  .result-card h3 {
    font-size: 1.15rem;
    font-weight: 700;
    margin-bottom: 12px;
  }
  .result-card p {
    font-size: 0.87rem;
    color: var(--muted);
    font-weight: 300;
    margin-bottom: 20px;
    line-height: 1.6;
  }
  .result-items {
    list-style: none;
    margin-bottom: 24px;
  }
  .result-items li {
    font-size: 0.84rem;
    padding: 6px 0;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: flex-start;
    gap: 8px;
  }
  .result-items li:last-child { border-bottom: none; }
  .result-items li::before { content: '→'; color: var(--accent); font-weight: 700; flex-shrink: 0; }
  .result-cta-btn {
    display: block;
    text-align: center;
    padding: 12px 20px;
    border-radius: 7px;
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 0.88rem;
    text-decoration: none;
    transition: all 0.2s;
    cursor: pointer;
    border: none;
  }
  .result-low .result-cta-btn { background: var(--red); color: #fff; }
  .result-mid .result-cta-btn { background: var(--orange); color: #fff; }
  .result-high .result-cta-btn { background: var(--green); color: #fff; }
  .result-cta-btn:hover { opacity: 0.85; transform: translateY(-1px); }

  /* ── CONVERSION STRATEGY ── */
  .conversion-section {
    background: #F0F3FF;
    border-top: 1px solid #D0D9FF;
    border-bottom: 1px solid #D0D9FF;
  }
  .funnel {
    display: flex;
    flex-direction: column;
    gap: 0;
    margin-top: 48px;
    position: relative;
  }
  .funnel::before {
    content: '';
    position: absolute;
    left: 35px;
    top: 0;
    bottom: 0;
    width: 2px;
    background: linear-gradient(to bottom, var(--accent), transparent);
  }
  .funnel-step {
    display: flex;
    gap: 24px;
    align-items: flex-start;
    padding-bottom: 36px;
    position: relative;
  }
  .funnel-num {
    width: 72px;
    height: 72px;
    border-radius: 50%;
    background: var(--accent);
    color: #fff;
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 1.4rem;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    position: relative;
    z-index: 1;
  }
  .funnel-content h3 {
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 6px;
    margin-top: 16px;
  }
  .funnel-content p {
    font-size: 0.88rem;
    color: var(--muted);
    font-weight: 300;
    max-width: 560px;
  }
  .funnel-tag {
    display: inline-block;
    background: #E8EEFF;
    color: var(--accent);
    font-size: 0.7rem;
    font-weight: 700;
    padding: 3px 10px;
    border-radius: 4px;
    margin-top: 8px;
    text-transform: uppercase;
    letter-spacing: 0.07em;
  }

  /* ── LANDING PAGE COPY ── */
  .copy-block {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 32px;
    margin-bottom: 24px;
  }
  .copy-block h3 {
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 16px;
    border-bottom: 1px solid var(--border);
    padding-bottom: 12px;
  }
  .copy-text {
    font-size: 0.9rem;
    line-height: 1.8;
    color: var(--ink);
    white-space: pre-wrap;
    font-weight: 300;
  }
  .copy-text strong { font-weight: 600; }
  .copy-note {
    font-size: 0.78rem;
    color: var(--muted);
    font-style: italic;
    margin-top: 12px;
    padding-top: 12px;
    border-top: 1px dashed var(--border);
  }

  /* ── SECTION HEADERS ── */
  .section-header { margin-bottom: 8px; }
  .section-eyebrow {
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 12px;
  }
  section h2 {
    font-size: clamp(1.8rem, 3vw, 2.4rem);
    font-weight: 800;
    letter-spacing: -0.03em;
    margin-bottom: 12px;
  }
  section > p {
    color: var(--muted);
    max-width: 560px;
    font-weight: 300;
    margin-bottom: 0;
  }

  /* ── FOOTER ── */
  footer {
    text-align: center;
    padding: 40px 24px;
    border-top: 1px solid var(--border);
    font-size: 0.82rem;
    color: var(--muted);
  }

  /* ── TABS ── */
  .tab-bar {
    display: flex;
    gap: 4px;
    background: var(--border);
    padding: 4px;
    border-radius: 8px;
    width: fit-content;
    margin-bottom: 32px;
  }
  .tab-btn {
    padding: 8px 20px;
    border-radius: 6px;
    border: none;
    background: transparent;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.85rem;
    font-weight: 500;
    color: var(--muted);
    cursor: pointer;
    transition: all 0.15s;
  }
  .tab-btn.active {
    background: var(--card);
    color: var(--ink);
    font-weight: 600;
    box-shadow: 0 1px 4px rgba(0,0,0,0.08);
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    nav { padding: 16px 20px; }
    .hero { grid-template-columns: 1fr; gap: 40px; }
    .hero-visual { display: none; }
    .problem-grid, .results-grid { grid-template-columns: 1fr; }
    .questions-grid { grid-template-columns: 1fr; }
    section { padding: 60px 20px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="logo">Aco<span>nia</span></div>
  <div style="display:flex;gap:32px;align-items:center;">
    <a href="#quiz">Le questionnaire</a>
    <a href="#scoring">Le scoring</a>
    <a href="#resultats">Les résultats</a>
    <a href="#typeform" class="nav-cta">Accéder au diagnostic →</a>
  </div>
</nav>

<!-- HERO -->
<div class="hero" id="hero">
  <div>
    <div class="hero-badge">Outil de diagnostic gratuit</div>
    <h1>Votre organisation est-elle <em>prête</em> à gagner des appels d'offres ?</h1>
    <p>En 4 minutes, évaluez votre maturité sur les appels d'offres B2B et identifiez vos leviers prioritaires pour augmenter votre taux de succès.</p>
    <a href="#typeform" class="hero-cta">Faire le diagnostic gratuit →</a>
    <div class="hero-sub">
      <span>✓ 7 questions</span>
      &nbsp;·&nbsp;
      <span>Résultats immédiats</span>
      &nbsp;·&nbsp;
      <span>Sans engagement</span>
    </div>
  </div>
  <div class="hero-visual">
    <div class="score-ring">
      <div class="score-inner">
        <div class="score-num">68</div>
        <div class="score-label">/100</div>
      </div>
    </div>
    <ul class="dimension-list">
      <li><span>Veille & détection</span><div class="dim-bar"><div class="dim-fill" style="width:45%"></div></div></li>
      <li><span>Qualification GO/NOGO</span><div class="dim-bar"><div class="dim-fill" style="width:80%"></div></div></li>
      <li><span>Structuration de l'offre</span><div class="dim-bar"><div class="dim-fill" style="width:60%"></div></div></li>
      <li><span>Pilotage commercial</span><div class="dim-bar"><div class="dim-fill" style="width:70%"></div></div></li>
    </ul>
  </div>
</div>

<!-- PROBLEM SECTION -->
<section id="probleme">
  <div class="section-eyebrow">Pourquoi ce diagnostic ?</div>
  <h2>La plupart des entreprises perdent des appels d'offres pour les mauvaises raisons</h2>
  <p>Pas par manque de compétences — mais par manque de méthode. Ce diagnostic vous aide à identifier exactement où vous perdez du terrain.</p>
  <div class="problem-grid">
    <div class="problem-card">
      <div class="problem-icon">📡</div>
      <h3>Détection tardive</h3>
      <p>Les opportunités sont identifiées trop tard pour construire une offre différenciée et crédible.</p>
    </div>
    <div class="problem-card">
      <div class="problem-icon">📋</div>
      <h3>Offres trop génériques</h3>
      <p>Les réponses ne parlent pas au décideur. Elles répondent au cahier des charges, pas aux enjeux réels.</p>
    </div>
    <div class="problem-card">
      <div class="problem-icon">🎯</div>
      <h3>Mauvais filtrage GO/NOGO</h3>
      <p>On répond à tout par principe, sans distinguer les appels d'offres qui méritent un investissement sérieux.</p>
    </div>
  </div>
</section>

<!-- QUIZ SECTION -->
<div class="quiz-section" id="quiz">
<div class="quiz-section-inner">
  <div class="section-tag">Questionnaire Typeform — Prêt à copier</div>
  <h2>Les 7 questions du diagnostic</h2>
  <p>Ce questionnaire est conçu pour qualifier précisément le niveau de maturité commercial d'un prospect sur les appels d'offres B2B.</p>

  <div class="questions-grid">

    <div class="q-card">
      <div class="q-num">Q1 — CONTEXTE (non noté)</div>
      <div class="q-text">Quelle est votre activité principale ?</div>
      <div class="q-options">
        <div class="q-opt"><span>Services / Conseil</span><span class="q-pts">Filtrage</span></div>
        <div class="q-opt"><span>Industrie / Fabrication</span><span class="q-pts">Filtrage</span></div>
        <div class="q-opt"><span>IT / Tech / SaaS</span><span class="q-pts">Filtrage</span></div>
        <div class="q-opt"><span>BTP / Travaux</span><span class="q-pts">Filtrage</span></div>
        <div class="q-opt"><span>Autre</span><span class="q-pts">Filtrage</span></div>
      </div>
    </div>

    <div class="q-card">
      <div class="q-num">Q2 — VOLUME (15 pts)</div>
      <div class="q-text">Combien d'appels d'offres répondez-vous par an ?</div>
      <div class="q-options">
        <div class="q-opt"><span>Moins de 5</span><span class="q-pts">0 pt</span></div>
        <div class="q-opt"><span>Entre 5 et 15</span><span class="q-pts">5 pts</span></div>
        <div class="q-opt"><span>Entre 15 et 40</span><span class="q-pts">10 pts</span></div>
        <div class="q-opt"><span>Plus de 40</span><span class="q-pts">15 pts</span></div>
      </div>
    </div>

    <div class="q-card">
      <div class="q-num">Q3 — VEILLE (15 pts)</div>
      <div class="q-text">Comment détectez-vous les appels d'offres qui vous correspondent ?</div>
      <div class="q-options">
        <div class="q-opt"><span>Au fil de l'eau / bouche à oreille</span><span class="q-pts">0 pt</span></div>
        <div class="q-opt"><span>Plateformes (BOAMP, Marchés Publics…)</span><span class="q-pts">5 pts</span></div>
        <div class="q-opt"><span>Outil de veille dédié</span><span class="q-pts">10 pts</span></div>
        <div class="q-opt"><span>Veille + réseau + ciblage proactif</span><span class="q-pts">15 pts</span></div>
      </div>
    </div>

    <div class="q-card">
      <div class="q-num">Q4 — SÉLECTION (15 pts)</div>
      <div class="q-text">Avez-vous un processus formalisé pour décider si vous répondez à un AO (GO/NOGO) ?</div>
      <div class="q-options">
        <div class="q-opt"><span>Non, on répond à tout</span><span class="q-pts">0 pt</span></div>
        <div class="q-opt"><span>Décision intuitive case par case</span><span class="q-pts">5 pts</span></div>
        <div class="q-opt"><span>Critères informels partagés en équipe</span><span class="q-pts">10 pts</span></div>
        <div class="q-opt"><span>Grille GO/NOGO structurée et validée</span><span class="q-pts">15 pts</span></div>
      </div>
    </div>

    <div class="q-card">
      <div class="q-num">Q5 — RÉDACTION (20 pts)</div>
      <div class="q-text">Comment construisez-vous vos réponses aux appels d'offres ?</div>
      <div class="q-options">
        <div class="q-opt"><span>Modèles génériques adaptés à la marge</span><span class="q-pts">0 pt</span></div>
        <div class="q-opt"><span>Personnalisation partielle des réponses</span><span class="q-pts">7 pts</span></div>
        <div class="q-opt"><span>Offre structurée + approche différenciée</span><span class="q-pts">14 pts</span></div>
        <div class="q-opt"><span>Process complet : analyse, diff., validation</span><span class="q-pts">20 pts</span></div>
      </div>
    </div>

    <div class="q-card">
      <div class="q-num">Q6 — TAUX DE SUCCÈS (20 pts)</div>
      <div class="q-text">Quel est votre taux de succès actuel sur les AO auxquels vous répondez ?</div>
      <div class="q-options">
        <div class="q-opt"><span>Inférieur à 10 %</span><span class="q-pts">0 pt</span></div>
        <div class="q-opt"><span>Entre 10 % et 25 %</span><span class="q-pts">7 pts</span></div>
        <div class="q-opt"><span>Entre 25 % et 40 %</span><span class="q-pts">14 pts</span></div>
        <div class="q-opt"><span>Plus de 40 %</span><span class="q-pts">20 pts</span></div>
      </div>
    </div>

    <div class="q-card">
      <div class="q-num">Q7 — PILOTAGE (15 pts)</div>
      <div class="q-text">Avez-vous un suivi structuré de vos AO (pipeline, KPIs, retours d'expérience) ?</div>
      <div class="q-options">
        <div class="q-opt"><span>Aucun suivi formalisé</span><span class="q-pts">0 pt</span></div>
        <div class="q-opt"><span>Tableau de bord basique</span><span class="q-pts">5 pts</span></div>
        <div class="q-opt"><span>Suivi régulier + analyse des perdus</span><span class="q-pts">10 pts</span></div>
        <div class="q-opt"><span>Pilotage complet + amélioration continue</span><span class="q-pts">15 pts</span></div>
      </div>
    </div>

    <div class="q-card" style="background:rgba(26,79,255,0.08);border-color:rgba(26,79,255,0.25);">
      <div class="q-num" style="color:var(--accent);">Q8 — COORDONNÉES (CTA)</div>
      <div class="q-text">Où souhaitez-vous recevoir votre rapport complet ?</div>
      <div class="q-options">
        <div class="q-opt" style="background:rgba(26,79,255,0.1)"><span>📧 Prénom / Nom</span><span class="q-pts">Requis</span></div>
        <div class="q-opt" style="background:rgba(26,79,255,0.1)"><span>📧 Email professionnel</span><span class="q-pts">Requis</span></div>
        <div class="q-opt" style="background:rgba(26,79,255,0.1)"><span>🏢 Entreprise</span><span class="q-pts">Requis</span></div>
        <div class="q-opt" style="background:rgba(26,79,255,0.1)"><span>📞 Téléphone</span><span class="q-pts">Optionnel</span></div>
      </div>
    </div>

  </div>
</div>
</div>

<!-- SCORING TABLE -->
<section id="scoring">
  <div class="section-eyebrow">Système de scoring</div>
  <h2>Comment le score est calculé</h2>
  <p>Chaque question est pondérée selon son impact réel sur le taux de succès en appels d'offres. Total : 100 points.</p>

  <table class="scoring-table">
    <thead>
      <tr>
        <th>Question</th>
        <th>Dimension évaluée</th>
        <th>Points max</th>
        <th>Justification</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Q1</td>
        <td>Contexte / Segmentation</td>
        <td><span class="pts-badge">0 pt</span></td>
        <td style="font-size:0.82rem;color:var(--muted)">Sert uniquement à personnaliser les résultats et qualifier le secteur.</td>
      </tr>
      <tr>
        <td>Q2</td>
        <td>Volume & exposition aux AO</td>
        <td><span class="pts-badge">15 pts</span></td>
        <td style="font-size:0.82rem;color:var(--muted)">Un volume faible révèle un sous-investissement commercial sur ce canal.</td>
      </tr>
      <tr>
        <td>Q3</td>
        <td>Veille & détection</td>
        <td><span class="pts-badge">15 pts</span></td>
        <td style="font-size:0.82rem;color:var(--muted)">Détecter tôt = plus de temps pour construire une offre gagnante.</td>
      </tr>
      <tr>
        <td>Q4</td>
        <td>Processus GO/NOGO</td>
        <td><span class="pts-badge">15 pts</span></td>
        <td style="font-size:0.82rem;color:var(--muted)">Répondre à tout dilue les ressources et fait baisser le taux de succès.</td>
      </tr>
      <tr>
        <td>Q5</td>
        <td>Qualité de rédaction des offres</td>
        <td><span class="pts-badge">20 pts</span></td>
        <td style="font-size:0.82rem;color:var(--muted)">C'est le levier n°1 de différenciation. Fortement pondéré.</td>
      </tr>
      <tr>
        <td>Q6</td>
        <td>Taux de succès actuel</td>
        <td><span class="pts-badge">20 pts</span></td>
        <td style="font-size:0.82rem;color:var(--muted)">Indicateur de résultat direct. Mesure l'efficacité globale réelle.</td>
      </tr>
      <tr>
        <td>Q7</td>
        <td>Pilotage & amélioration continue</td>
        <td><span class="pts-badge">15 pts</span></td>
        <td style="font-size:0.82rem;color:var(--muted)">Sans suivi, pas de progression. Clé pour monter en maturité.</td>
      </tr>
      <tr style="background:#F0F3FF;">
        <td colspan="2"><strong>TOTAL</strong></td>
        <td><span class="pts-badge" style="background:var(--accent);color:#fff;">100 pts</span></td>
        <td style="font-size:0.82rem;color:var(--muted)">Score calculé automatiquement à la fin du quiz.</td>
      </tr>
    </tbody>
  </table>
</section>

<!-- RESULTS SECTION -->
<section id="resultats">
  <div class="section-eyebrow">Pages de résultats</div>
  <h2>3 profils, 3 messages personnalisés</h2>
  <p>Chaque score déclenche une page de résultats différente, avec un message adapté et un appel à l'action spécifique.</p>

  <div class="results-grid">

    <!-- LOW -->
    <div class="result-card result-low">
      <div class="result-score">0 – 40</div>
      <div class="result-label">Profil Débutant</div>
      <h3>Vous partez avec un désavantage structurel</h3>
      <p>Votre organisation n'est pas encore outillée pour compétir efficacement sur les appels d'offres. La bonne nouvelle : les marges de progression sont importantes et rapides à activer.</p>
      <ul class="result-items">
        <li>Mettre en place une veille AO structurée</li>
        <li>Créer une grille GO/NOGO simple</li>
        <li>Former votre équipe à la rédaction d'offres</li>
        <li>Désigner un référent AO dans votre structure</li>
      </ul>
      <a href="#contact" class="result-cta-btn">Parler à un expert →</a>
    </div>

    <!-- MID -->
    <div class="result-card result-mid">
      <div class="result-score">40 – 70</div>
      <div class="result-label">Profil Intermédiaire</div>
      <h3>Vous avez des bases solides, mais des freins cachés</h3>
      <p>Votre organisation répond aux appels d'offres avec une certaine régularité, mais des inefficacités dans votre processus vous font perdre des marchés que vous méritez.</p>
      <ul class="result-items">
        <li>Affiner votre critère de sélection GO/NOGO</li>
        <li>Renforcer la personnalisation de vos offres</li>
        <li>Analyser systématiquement vos AO perdus</li>
        <li>Structurer un pipeline AO dédié</li>
      </ul>
      <a href="#contact" class="result-cta-btn">Voir les quick-wins →</a>
    </div>

    <!-- HIGH -->
    <div class="result-card result-high">
      <div class="result-score">70 – 100</div>
      <div class="result-label">Profil Avancé</div>
      <h3>Vous êtes mature — passez à la vitesse supérieure</h3>
      <p>Votre organisation a une vraie maturité sur les appels d'offres. L'enjeu est maintenant de scaler ce qui fonctionne et d'identifier les 5–10 % de progression qui feront la différence.</p>
      <ul class="result-items">
        <li>Identifier les segments AO les plus rentables</li>
        <li>Automatiser votre veille et votre pipeline</li>
        <li>Bâtir des partenariats stratégiques</li>
        <li>Passer d'un taux de 30 % à 50 %+</li>
      </ul>
      <a href="#contact" class="result-cta-btn">Optimiser la performance →</a>
    </div>

  </div>
</section>

<!-- CONVERSION STRATEGY -->
<div class="conversion-section">
<section id="conversion">
  <div class="section-eyebrow">Stratégie de conversion</div>
  <h2>Du quiz au rendez-vous commercial</h2>
  <p>Chaque lead est qualifié automatiquement. Voici comment transformer un score en opportunité commerciale.</p>

  <div class="funnel">
    <div class="funnel-step">
      <div class="funnel-num">1</div>
      <div class="funnel-content">
        <h3>Résultats immédiats sur la page de fin Typeform</h3>
        <p>Le prospect voit son score, son profil et 4 recommandations personnalisées. Le rapport complet est envoyé par email dans la foulée (automation Zapier/Make → CRM).</p>
        <span class="funnel-tag">Déclencheur : fin du quiz</span>
      </div>
    </div>
    <div class="funnel-step">
      <div class="funnel-num">2</div>
      <div class="funnel-content">
        <h3>Email de suivi J+0 (automatique)</h3>
        <p>Objet : "Votre Score Maturité AO : [score]/100 — 3 actions prioritaires". Corps : récapitulatif du score + lien Calendly segmenté selon le profil (urgence pour les scores faibles, conseil stratégique pour les avancés).</p>
        <span class="funnel-tag">Outil : HubSpot / Brevo / ActiveCampaign</span>
      </div>
    </div>
    <div class="funnel-step">
      <div class="funnel-num">3</div>
      <div class="funnel-content">
        <h3>Relance commerciale J+3 (manuelle ou séquencée)</h3>
        <p>Le commercial reçoit une alerte avec le profil et le score du lead. Il envoie un message court et personnalisé avec une proposition de 30 min de conseil offert, sans pitch produit.</p>
        <span class="funnel-tag">Priorité : scores 30–65 (zone d'urgence ressentie)</span>
      </div>
    </div>
    <div class="funnel-step">
      <div class="funnel-num">4</div>
      <div class="funnel-content">
        <h3>Nurturing J+7 et J+21 (non-convertis)</h3>
        <p>Envoi de 2 contenus ciblés selon le profil : benchmark sectoriel, guide de rédaction, ou étude de cas. L'objectif est de maintenir la relation jusqu'au moment d'achat.</p>
        <span class="funnel-tag">Contenu adapté au secteur (Q1)</span>
      </div>
    </div>
    <div class="funnel-step" style="padding-bottom:0">
      <div class="funnel-num" style="background:var(--green)">✓</div>
      <div class="funnel-content">
        <h3>Rendez-vous qualifié</h3>
        <p>Le commercial arrive en réunion avec le score du prospect, son profil et ses points de douleur identifiés. La conversation est déjà contextualisée avant même le premier mot.</p>
        <span class="funnel-tag">Objectif : 15–25 % de conversion quiz → RDV</span>
      </div>
    </div>
  </div>
</section>
</div>

<!-- LANDING PAGE COPY -->
<section id="landing">
  <div class="section-eyebrow">Textes prêts à copier</div>
  <h2>Landing page — Contenu complet</h2>
  <p>Tous les textes ci-dessous sont prêts à être utilisés directement dans votre page web ou Typeform.</p>

  <div class="copy-block">
    <h3>Titre principal (H1)</h3>
    <div class="copy-text">Votre organisation est-elle <strong>prête à gagner des appels d'offres ?</strong></div>
    <div class="copy-note">Variante A : "Testez votre maturité AO en 4 minutes" | Variante B : "Découvrez pourquoi vous perdez des marchés que vous mériteriez de gagner"</div>
  </div>

  <div class="copy-block">
    <h3>Sous-titre / Accroche</h3>
    <div class="copy-text">En répondant à 7 questions ciblées, obtenez votre <strong>Score de Maturité Appels d'Offres</strong> et un plan d'action personnalisé pour augmenter votre taux de succès.

Gratuit. Sans engagement. Résultats immédiats.</div>
  </div>

  <div class="copy-block">
    <h3>Section "Ce que vous allez obtenir"</h3>
    <div class="copy-text"><strong>Un diagnostic en 4 minutes chrono</strong>
Pas de formulaire interminable. 7 questions concrètes sur votre fonctionnement actuel.

<strong>Votre score sur 100 avec une analyse par dimension</strong>
Veille, sélection, rédaction, pilotage : vous saurez exactement où vous en êtes.

<strong>Un plan d'action prioritaire adapté à votre profil</strong>
3 à 5 actions concrètes à fort impact, ordonnées par priorité.

<strong>Un accès à un expert si vous le souhaitez</strong>
Pas de démarchage intempestif. Une proposition de 30 minutes offertes pour aller plus loin.</div>
  </div>

  <div class="copy-block">
    <h3>Preuve sociale / Chiffres clés</h3>
    <div class="copy-text">Les entreprises qui structurent leur approche AO augmentent leur taux de succès de <strong>40 % en moyenne</strong> sur 12 mois.

La plupart des entreprises répondent à des appels d'offres sans avoir évalué leur niveau de préparation réelle. Ce diagnostic change ça.</div>
    <div class="copy-note">À remplacer par de vraies données clients dès que disponibles</div>
  </div>

  <div class="copy-block">
    <h3>CTA principal</h3>
    <div class="copy-text"><strong>Bouton :</strong> → Faire le diagnostic gratuit

<strong>Texte sous le bouton :</strong> 7 questions · 4 minutes · Résultats immédiats · Sans engagement

<strong>Rassurance RGPD :</strong> Vos données restent confidentielles et ne sont jamais revendues.</div>
  </div>

  <div class="copy-block">
    <h3>Emails de résultats — Objets recommandés</h3>
    <div class="copy-text"><strong>Score faible (0–40) :</strong>
"[Prénom], votre score AO est de [X]/100 — voici ce qu'il faut faire en priorité"

<strong>Score intermédiaire (40–70) :</strong>
"[Prénom], vous êtes à [X]/100 — 3 freins cachés à lever rapidement"

<strong>Score avancé (70–100) :</strong>
"[Prénom], score [X]/100 — comment passer de bon à excellent sur les AO"</div>
  </div>

  <div class="copy-block">
    <h3>Message de relance commerciale J+3 (modèle)</h3>
    <div class="copy-text">Bonjour [Prénom],

J'ai vu que vous avez passé notre diagnostic AO il y a quelques jours — score [X]/100, profil [débutant / intermédiaire / avancé].

Sur la base de vos réponses, j'ai identifié 2 ou 3 points qui pourraient avoir un impact direct sur vos prochains appels d'offres.

Est-ce que 30 minutes cette semaine vous conviendrait pour en parler ? Je n'ai rien à vous vendre à ce stade — juste un échange de fond sur votre situation.

[Lien Calendly]

Cordialement,
[Prénom Nom]
[Aconia]</div>
    <div class="copy-note">Ton : direct, sans jargon, sans sur-promesse. Le score donne de la crédibilité à la démarche.</div>
  </div>

</section>

<!-- FOOTER -->
<footer id="contact">
  <p style="margin-bottom:8px;font-family:'Syne',sans-serif;font-weight:700;font-size:1rem;">Aconia — Appels d'offres B2B</p>
  <p>Ce document est un kit complet prêt à déployer dans Typeform + votre CRM.</p>
  <p style="margin-top:12px;font-size:0.75rem;">© 2025 Aconia · Tous droits réservés</p>
</footer>

</body>
</html>
