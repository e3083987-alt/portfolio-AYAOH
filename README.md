<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portfolio Académique — AYAOH Essodomna Jules — Semestre 6</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Source+Sans+3:wght@300;400;600&display=swap" rel="stylesheet">
<style>
  :root {
    --teal: #1749B8;
    --teal-light: #2F6FE0;
    --teal-pale: #EAF1FF;
    --teal-mid: #6E9CF2;
    --charcoal: #0B1E42;
    --charcoal-mid: #4C5C7C;
    --charcoal-light: #93A2C0;
    --sand: #F3F6FD;
    --sand-dark: #D3DEF5;
    --white: #FFFFFF;
    --accent: #1749B8;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Source Sans 3', sans-serif;
    font-weight: 300;
    color: var(--charcoal);
    background: var(--sand);
    font-size: 16px;
    line-height: 1.75;
  }

  /* ── COVER ── */
  .cover {
    background: var(--charcoal);
    color: white;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 4rem 2rem;
    position: relative;
    overflow: hidden;
  }

  .cover::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 340px; height: 340px;
    border: 1px solid rgba(110,156,242,0.22);
    border-radius: 50%;
  }
  .cover::after {
    content: '';
    position: absolute;
    bottom: -60px; left: -60px;
    width: 260px; height: 260px;
    border: 1px solid rgba(110,156,242,0.15);
    border-radius: 50%;
  }

  .cover-badge {
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--teal-mid);
    margin-bottom: 2rem;
    font-weight: 600;
  }

  .cover h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.2rem, 6vw, 4rem);
    font-weight: 700;
    line-height: 1.1;
    margin-bottom: 0.5rem;
    color: white;
  }

  .cover-name-line {
    width: 60px;
    height: 2px;
    background: var(--teal-mid);
    margin: 1.5rem auto;
  }

  .cover-sub {
    font-size: 1rem;
    color: rgba(255,255,255,0.55);
    letter-spacing: 0.5px;
    margin-bottom: 0.4rem;
  }

  .cover-institution {
    font-size: 0.85rem;
    color: var(--teal-mid);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-top: 2rem;
    font-weight: 600;
  }

  .cover-geo {
    font-size: 0.8rem;
    color: rgba(255,255,255,0.3);
    margin-top: 0.3rem;
    letter-spacing: 1px;
  }

  /* ── LAYOUT ── */
  .wrapper {
    max-width: 860px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  /* ── TABLE OF CONTENTS ── */
  .toc-section {
    background: var(--white);
    padding: 3.5rem 0;
    border-bottom: 1px solid var(--sand-dark);
  }

  .toc-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1px;
    background: var(--sand-dark);
    border: 1px solid var(--sand-dark);
  }

  .toc-item {
    background: var(--white);
    padding: 1.25rem 1.5rem;
    display: flex;
    align-items: center;
    gap: 1rem;
    text-decoration: none;
    color: var(--charcoal);
    transition: background 0.2s;
  }

  .toc-item:hover { background: var(--teal-pale); }

  .toc-num {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem;
    color: var(--sand-dark);
    font-weight: 700;
    min-width: 2rem;
    line-height: 1;
  }

  .toc-label {
    font-size: 0.82rem;
    line-height: 1.35;
    color: var(--charcoal-mid);
    font-weight: 400;
  }

  /* ── SECTIONS ── */
  .section {
    padding: 4.5rem 0;
    border-bottom: 1px solid var(--sand-dark);
    background: var(--white);
  }

  .section:nth-child(odd) { background: var(--sand); }

  .section-header {
    display: flex;
    align-items: flex-start;
    gap: 1.5rem;
    margin-bottom: 2.5rem;
  }

  .section-num {
    font-family: 'Playfair Display', serif;
    font-size: 3.5rem;
    color: var(--sand-dark);
    font-weight: 700;
    line-height: 1;
    min-width: 4rem;
    padding-top: 0.2rem;
  }

  .section-title-block h2 {
    font-family: 'Playfair Display', serif;
    font-size: 1.7rem;
    font-weight: 700;
    color: var(--charcoal);
    line-height: 1.2;
    margin-bottom: 0.3rem;
  }

  .section-title-block .sub {
    font-size: 0.82rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--teal);
    font-weight: 600;
  }

  .divider {
    width: 40px;
    height: 2px;
    background: var(--teal-mid);
    margin: 1.5rem 0;
  }

  p { margin-bottom: 1rem; color: var(--charcoal-mid); }
  p:last-child { margin-bottom: 0; }
  p strong { color: var(--charcoal); font-weight: 600; }

  /* ── MODULE CARDS ── */
  .module-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1rem;
    margin-top: 1.5rem;
  }

  .module-card {
    background: var(--white);
    border: 1px solid var(--sand-dark);
    padding: 1.25rem 1.5rem;
    position: relative;
    overflow: hidden;
  }

  .module-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 100%;
    background: var(--teal-light);
  }

  .module-card.pending::before { background: var(--charcoal-light); }

  .module-code {
    font-size: 0.7rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--charcoal-light);
    font-weight: 600;
    margin-bottom: 0.4rem;
  }

  .module-title {
    font-size: 0.9rem;
    font-weight: 600;
    color: var(--charcoal);
    margin-bottom: 0.75rem;
    line-height: 1.3;
  }

  .module-note {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
  }

  .note-value {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem;
    font-weight: 700;
    color: var(--teal);
    line-height: 1;
  }

  .note-value.pending { color: var(--charcoal-light); font-size: 1rem; }

  .note-bar-wrap {
    margin-top: 0.6rem;
    height: 3px;
    background: var(--sand-dark);
    border-radius: 2px;
    overflow: hidden;
  }

  .note-bar {
    height: 100%;
    background: var(--teal-light);
    border-radius: 2px;
    transition: width 0.5s;
  }

  /* ── COMPETENCIES ── */
  .competency-block {
    margin-bottom: 2rem;
  }

  .competency-title {
    font-size: 0.78rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--teal);
    font-weight: 600;
    margin-bottom: 0.75rem;
    padding-left: 0.75rem;
    border-left: 2px solid var(--teal-mid);
  }

  .competency-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.4rem;
  }

  .competency-list li {
    display: flex;
    align-items: flex-start;
    gap: 0.6rem;
    font-size: 0.9rem;
    color: var(--charcoal-mid);
    padding: 0.5rem 0.75rem;
    background: var(--sand);
  }

  .competency-list li::before {
    content: '→';
    color: var(--teal-mid);
    font-size: 0.8rem;
    margin-top: 1px;
    flex-shrink: 0;
  }

  /* ── TIMELINE ── */
  .timeline {
    position: relative;
    padding-left: 1.5rem;
    border-left: 1px solid var(--sand-dark);
  }

  .timeline-item {
    margin-bottom: 2rem;
    position: relative;
  }

  .timeline-item::before {
    content: '';
    position: absolute;
    left: -1.65rem; top: 0.35rem;
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--teal-light);
    border: 2px solid var(--white);
    box-shadow: 0 0 0 1px var(--teal-light);
  }

  .timeline-period {
    font-size: 0.72rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--teal);
    font-weight: 600;
    margin-bottom: 0.5rem;
  }

  .timeline-content h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    color: var(--charcoal);
    margin-bottom: 0.5rem;
  }

  /* ── QUOTE ── */
  .pull-quote {
    border-left: 3px solid var(--teal-mid);
    padding: 1rem 1.5rem;
    margin: 2rem 0;
    background: var(--teal-pale);
    font-family: 'Playfair Display', serif;
    font-size: 1.05rem;
    color: var(--teal);
    font-style: italic;
    line-height: 1.5;
  }

  /* ── OVERVIEW TABLE (S6 summary) ── */
  .ue-block {
    margin-bottom: 2rem;
  }

  .ue-label {
    font-size: 0.7rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--white);
    background: var(--charcoal);
    display: inline-block;
    padding: 0.3rem 0.9rem;
    font-weight: 600;
    margin-bottom: 0.75rem;
  }

  /* ── STAGE INFO CARD ── */
  .info-card {
    background: var(--white);
    border: 1px solid var(--sand-dark);
    padding: 1.75rem;
    margin-top: 1.5rem;
  }

  .info-row {
    display: flex;
    gap: 1rem;
    padding: 0.6rem 0;
    border-bottom: 1px solid var(--sand);
    font-size: 0.88rem;
  }
  .info-row:last-child { border-bottom: none; }

  .info-label {
    min-width: 150px;
    color: var(--teal);
    font-weight: 600;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    font-size: 0.72rem;
    padding-top: 0.15rem;
  }

  .info-value { color: var(--charcoal-mid); }

  /* ── SIGNATURE ── */
  .signature-block {
    background: var(--charcoal);
    color: white;
    padding: 3.5rem 0;
    text-align: center;
  }

  .signature-block h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
  }

  .signature-block p {
    color: rgba(255,255,255,0.45);
    font-size: 0.85rem;
    margin: 0;
  }

  .signature-teal {
    color: var(--teal-mid);
  }

  /* ── PRINT ── */
  @media print {
    .cover { min-height: auto; page-break-after: always; }
    .section { page-break-inside: avoid; }
  }
</style>
</head>
<body>

<!-- COVER -->
<div class="cover">
  <div class="cover-badge">Portfolio Académique · Semestre 6</div>
  <h1>AYAOH<br>Essodomna Jules</h1>
  <div class="cover-name-line"></div>
  <p class="cover-sub">Licence Professionnelle — 3ème Année</p>
  <p class="cover-sub">Systèmes et Réseaux Informatiques</p>
  <p class="cover-institution">ESIG Global Success</p>
  <p class="cover-geo">Lomé, Togo · 2026</p>
</div>

<!-- TABLE OF CONTENTS -->
<div class="toc-section">
  <div class="wrapper">
    <div class="section-header" style="margin-bottom: 2rem;">
      <div class="section-title-block">
        <div class="sub">Sommaire</div>
        <h2>Table des matières</h2>
      </div>
    </div>
    <div class="toc-grid">
      <a class="toc-item" href="#section1">
        <div class="toc-num">1</div>
        <div class="toc-label">Présentation de l'étudiant</div>
      </a>
      <a class="toc-item" href="#section2">
        <div class="toc-num">2</div>
        <div class="toc-label">Présentation de l'établissement</div>
      </a>
      <a class="toc-item" href="#section3">
        <div class="toc-num">3</div>
        <div class="toc-label">Mot d'introduction</div>
      </a>
      <a class="toc-item" href="#section4">
        <div class="toc-num">4</div>
        <div class="toc-label">Récapitulatif Semestre 6</div>
      </a>
      <a class="toc-item" href="#section5">
        <div class="toc-num">5</div>
        <div class="toc-label">Analyse détaillée par UE et SAÉ</div>
      </a>
      <a class="toc-item" href="#section6">
        <div class="toc-num">6</div>
        <div class="toc-label">Stage professionnel — GO-NTIC</div>
      </a>
      <a class="toc-item" href="#section7">
        <div class="toc-num">7</div>
        <div class="toc-label">Mémoire de fin de parcours</div>
      </a>
      <a class="toc-item" href="#section8">
        <div class="toc-num">8</div>
        <div class="toc-label">Bilan des compétences</div>
      </a>
      <a class="toc-item" href="#section9">
        <div class="toc-num">9</div>
        <div class="toc-label">Axes de progression</div>
      </a>
      <a class="toc-item" href="#section10">
        <div class="toc-num">10</div>
        <div class="toc-label">Conclusion générale</div>
      </a>
    </div>
  </div>
</div>

<!-- SECTION 1 -->
<div class="section" id="section1">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">01</div>
      <div class="section-title-block">
        <div class="sub">Identité</div>
        <h2>Présentation de l'étudiant</h2>
      </div>
    </div>
    <div class="divider"></div>
    <p>Je m'appelle <strong>AYAOH Essodomna Jules</strong>, actuellement en troisième et dernière année de Licence Professionnelle, spécialité Systèmes et Réseaux Informatiques, à l'ESIG Global Success à Lomé. Le Semestre 6 marque l'aboutissement de ce parcours : il combine les derniers enseignements théoriques avec une mise en situation professionnelle réelle, à travers un stage en entreprise et la rédaction d'un mémoire de fin de parcours.</p>
    <p>Par rapport au Semestre 5, mon regard a évolué : les notions abordées en sécurité applicative et en administration système ne relèvent plus seulement de la théorie, elles trouvent désormais un écho direct dans les situations rencontrées sur le terrain, notamment à travers le stage effectué chez GO-NTIC. Cette bascule progressive de la salle de cours vers la pratique professionnelle constitue la principale transformation de cette fin de parcours.</p>
    <div class="pull-quote">
      « Le Semestre 6 n'est plus seulement un semestre de cours : c'est celui où la formation rencontre le terrain. »
    </div>
    <p>Ce semestre se distingue par son ouverture vers le monde professionnel : au-delà des unités d'enseignement techniques et transversales, j'effectue un stage au sein de l'entreprise <strong>GO-NTIC</strong>, une expérience qui vient directement nourrir mon mémoire de fin de parcours et confirmer mon orientation vers la sécurité des systèmes d'information.</p>
  </div>
</div>

<!-- SECTION 2 -->
<div class="section" id="section2">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">02</div>
      <div class="section-title-block">
        <div class="sub">Cadre académique</div>
        <h2>Présentation de l'établissement</h2>
      </div>
    </div>
    <div class="divider"></div>
    <p><strong>L'ESIG Global Success</strong> est un établissement d'enseignement supérieur privé situé à Lomé, capitale du Togo. Il propose des formations de niveau licence et master dans les domaines de l'informatique, des télécommunications, du management et de la gestion, avec une approche pédagogique orientée vers la professionnalisation.</p>
    <p>Le Semestre 6, dernier semestre de la Licence Professionnelle SRI, est structuré différemment des semestres précédents : la part des enseignements transversaux (entrepreneuriat, gestion, droit, culture d'entreprise) y est plus importante, en préparation à l'insertion professionnelle, et le stage en entreprise y occupe une place centrale, encadré par un tuteur académique et un tuteur professionnel.</p>
    <p>Ce dernier semestre est encadré conjointement par les enseignants référents des unités transversales et par un tuteur académique désigné pour le suivi du stage et du mémoire, garantissant une continuité entre les enseignements théoriques et l'expérience acquise en entreprise.</p>
  </div>
</div>

<!-- SECTION 3 -->
<div class="section" id="section3">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">03</div>
      <div class="section-title-block">
        <div class="sub">Avant-propos</div>
        <h2>Mot d'introduction</h2>
      </div>
    </div>
    <div class="divider"></div>
    <p>Ce portfolio prolonge la démarche entamée au Semestre 5, dans le cadre du module de démarche portfolio. Il couvre un semestre d'une nature différente : moins dense en volume horaire de cours magistraux, mais bien plus exigeant en autonomie, puisqu'il fait coexister le suivi des dernières unités d'enseignement, un stage en entreprise à temps partagé, et la rédaction d'un mémoire de fin de parcours.</p>
    <p>Ce portfolio se concentre sur la description des enseignements suivis, sur le contenu du stage à GO-NTIC, et sur le mémoire de fin de parcours.</p>
    <div class="pull-quote">
      « Ce portfolio documente le travail engagé — le stage, le mémoire, les enseignements suivis. »
    </div>
    <p>J'aborde ce dernier semestre avec la conscience qu'il s'agit d'une étape charnière : celle où trois années de formation doivent se traduire en compétences réellement mobilisables en entreprise, et où le mémoire vient formaliser une réflexion construite progressivement depuis le Semestre 5.</p>
  </div>
</div>

<!-- SECTION 4 -->
<div class="section" id="section4">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">04</div>
      <div class="section-title-block">
        <div class="sub">Vue d'ensemble</div>
        <h2>Récapitulatif des modules du Semestre 6</h2>
      </div>
    </div>
    <div class="divider"></div>

    <div class="ue-block">
      <div class="ue-label">SAÉ — Situations d'Apprentissage et d'Évaluation</div>
      <div class="module-grid">
        <div class="module-card">
          <div class="module-code">SAÉ 6.1</div>
          <div class="module-title">Réponse à un incident</div>
        </div>
        <div class="module-card">
          <div class="module-code">SAÉ 6.2</div>
          <div class="module-title">Réagir face à une cyber-attaque</div>
        </div>
        <div class="module-card">
          <div class="module-code">SAÉ 6.3</div>
          <div class="module-title">Réaliser une veille technologique</div>
        </div>
        <div class="module-card">
          <div class="module-code">SAÉ 6.4</div>
          <div class="module-title">Méthodologie de rédaction de mémoire pro — Partie I</div>
        </div>
        <div class="module-card">
          <div class="module-code">SAÉ 6.5</div>
          <div class="module-title">Méthodologie de rédaction de mémoire pro — Partie II</div>
        </div>
      </div>
    </div>

    <div class="ue-block">
      <div class="ue-label">UE — Unités d'Enseignement transversales</div>
      <div class="module-grid">
        <div class="module-card">
          <div class="module-code">UE 6.1</div>
          <div class="module-title">Initiation à l'entrepreneuriat</div>
        </div>
        <div class="module-card">
          <div class="module-code">UE 6.2</div>
          <div class="module-title">Propriété intellectuelle</div>
        </div>
        <div class="module-card">
          <div class="module-code">UE 6.3</div>
          <div class="module-title">Culture d'entreprise</div>
        </div>
        <div class="module-card">
          <div class="module-code">UE 6.4</div>
          <div class="module-title">Gestion</div>
        </div>
        <div class="module-card">
          <div class="module-code">UE 6.5</div>
          <div class="module-title">Économie</div>
        </div>
        <div class="module-card">
          <div class="module-code">UE 6.6</div>
          <div class="module-title">Droit de l'informatique</div>
        </div>
      </div>
    </div>

    <div class="ue-block">
      <div class="ue-label">Stage &amp; Mémoire</div>
      <div class="module-grid">
        <div class="module-card">
          <div class="module-code">STAGE S6</div>
          <div class="module-title">Stage professionnel — GO-NTIC</div>
        </div>
        <div class="module-card">
          <div class="module-code">MÉMOIRE</div>
          <div class="module-title">Mémoire de fin de parcours</div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- SECTION 5 -->
<div class="section" id="section5">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">05</div>
      <div class="section-title-block">
        <div class="sub">Analyse académique</div>
        <h2>Analyse détaillée par UE et SAÉ</h2>
      </div>
    </div>
    <div class="divider"></div>

    <h3 style="font-family:'Playfair Display',serif; font-size:1.2rem; color:var(--charcoal); margin-bottom:1rem; padding-bottom:0.5rem; border-bottom:1px solid var(--sand-dark);">5.1 — SAÉ : Sécurité opérationnelle et méthodologie</h3>

    <p><strong>SAÉ — Réponse à un incident :</strong> Ce module aborde la démarche de gestion d'incident de sécurité, depuis la détection jusqu'à la remédiation : qualification de l'incident, containment, éradication, retour à la normale et retour d'expérience (post-mortem), appliquée à un scénario d'attaque simulé traité en groupe et donnant lieu à un rapport d'intervention structuré.</p>

    <p><strong>SAÉ — Réagir face à une cyber-attaque :</strong> Ce module met l'accent sur la capacité à identifier une attaque en cours et à structurer une réponse adaptée — isolement des systèmes compromis, communication de crise, coordination des parties prenantes, à travers un exercice de simulation d'attaque mené en conditions proches du réel.</p>

    <p><strong>SAÉ — Réaliser une veille technologique :</strong> Ce module prolonge une pratique déjà engagée les semestres précédents : suivi structuré de sources techniques (CVE, publications spécialisées, flux RSS), synthèse et restitution des tendances observées dans le domaine de la cybersécurité, avec un périmètre centré cette fois sur les menaces touchant les objets connectés et les équipements de vidéosurveillance, en résonance directe avec le stage effectué chez GO-NTIC.</p>

    <p><strong>SAÉ — Méthodologie de rédaction de mémoire pro (Parties I et II) :</strong> Ces deux volets accompagnent directement la rédaction du mémoire de fin de parcours : structuration du plan, méthodologie de recherche documentaire, gestion bibliographique avec <strong>Zotero</strong>, normes de citation et de mise en forme académique. Ce module est directement mobilisé dans le travail présenté en section 7 de ce portfolio.</p>

    <h3 style="font-family:'Playfair Display',serif; font-size:1.2rem; color:var(--charcoal); margin: 2rem 0 1rem; padding-bottom:0.5rem; border-bottom:1px solid var(--sand-dark);">5.2 — UE : Enseignements transversaux et professionnalisants</h3>

    <p><strong>Initiation à l'entrepreneuriat :</strong> Ce module introduit les fondamentaux de la démarche entrepreneuriale — identification d'une opportunité, construction d'un modèle économique, étude de marché simplifiée — autant de notions utiles pour situer, à terme, une éventuelle activité indépendante dans le conseil en sécurité informatique.</p>

    <p><strong>Propriété intellectuelle :</strong> Ce module couvre les régimes de protection applicables aux créations informatiques — droit d'auteur sur les logiciels, brevets, marques, licences open source — avec une attention particulière aux enjeux propres au secteur numérique.</p>

    <p><strong>Culture d'entreprise :</strong> Ce module traite des codes, des usages et du fonctionnement interne d'une organisation — communication professionnelle, travail en équipe, positionnement d'un stagiaire ou jeune diplômé au sein d'une structure. Il trouve un écho direct dans l'expérience vécue chez GO-NTIC.</p>

    <p><strong>Gestion :</strong> Ce module introduit les bases de la gestion d'entreprise — comptabilité générale, gestion budgétaire, indicateurs de performance — nécessaires à la compréhension du fonctionnement économique d'une structure informatique.</p>

    <p><strong>Économie :</strong> Ce module aborde les grands mécanismes économiques généraux et leur application au secteur des technologies de l'information, notamment les dynamiques du marché numérique en Afrique de l'Ouest.</p>

    <p><strong>Droit de l'informatique :</strong> Ce module couvre le cadre juridique applicable aux activités informatiques : protection des données personnelles, responsabilité en matière de cybersécurité, contrats informatiques, cadre réglementaire togolais et régional. Ce module complète directement les compétences en sécurité acquises au Semestre 5.</p>

  </div>
</div>

<!-- SECTION 6 -->
<div class="section" id="section6">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">06</div>
      <div class="section-title-block">
        <div class="sub">Expérience professionnelle</div>
        <h2>Stage professionnel — GO-NTIC</h2>
      </div>
    </div>
    <div class="divider"></div>

    <p>Dans le cadre du Semestre 6, j'effectue un stage au sein de l'entreprise <strong>GO-NTIC</strong>, une société de prestation de services informatiques spécialisée dans l'installation et la maintenance de solutions techniques : caméras de vidéosurveillance, réseaux Wi-Fi, et objets intelligents (domotique / IoT).</p>

    <div class="info-card">
      <div class="info-row">
        <div class="info-label">Entreprise</div>
        <div class="info-value">GO-NTIC — prestation de services en installations informatiques</div>
      </div>
      <div class="info-row">
        <div class="info-label">Secteur d'activité</div>
        <div class="info-value">Vidéosurveillance, réseaux Wi-Fi, objets connectés / intelligents</div>
      </div>
      <div class="info-row">
        <div class="info-label">Poste / Fonction</div>
        <div class="info-value">Technicien stagiaire en installations informatiques et sécurité</div>
      </div>
      <div class="info-row">
        <div class="info-label">Période</div>
        <div class="info-value">Semestre 6 (année académique 2025-2026)</div>
      </div>
    </div>

    <h3 style="font-family:'Playfair Display',serif; margin: 2rem 0 0.75rem; color: var(--charcoal); font-size: 1.1rem;">Missions et activités</h3>
    <p>Au quotidien, mes missions couvrent l'installation et la configuration de caméras de vidéosurveillance IP chez les clients, le déploiement et le paramétrage de points d'accès Wi-Fi, ainsi que la mise en service d'objets connectés et d'équipements domotiques. Ce travail s'accompagne d'interventions de diagnostic en cas de panne, et de la rédaction de comptes rendus techniques à l'issue de chaque intervention.</p>

    <h3 style="font-family:'Playfair Display',serif; margin: 2rem 0 0.75rem; color: var(--charcoal); font-size: 1.1rem;">Apports pour ma formation</h3>
    <p>Ce stage constitue une opportunité précieuse de confronter les compétences réseaux et sécurité acquises durant la licence à des installations réelles chez des clients. La pose et la configuration de caméras de vidéosurveillance connectées, de réseaux Wi-Fi et d'objets intelligents soulèvent des enjeux directement liés à la sécurité des systèmes d'information : segmentation du réseau domestique ou professionnel, sécurisation des accès aux flux vidéo, mise à jour du firmware des équipements IoT, et sensibilisation des clients aux bonnes pratiques.</p>
    <div class="pull-quote">
      « Ce stage me permet de voir, du côté client, les failles de sécurité les plus courantes sur des équipements grand public et professionnels — un terrain d'observation qui alimente directement mon mémoire. »
    </div>
    <p>Certaines interventions m'ont notamment permis de constater, chez des clients, des équipements installés avec leurs identifiants d'usine par défaut ou des flux vidéo accessibles sans chiffrement — des observations concrètes qui viennent directement nourrir la réflexion menée dans le cadre du mémoire.</p>
  </div>
</div>

<!-- SECTION 7 -->
<div class="section" id="section7">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">07</div>
      <div class="section-title-block">
        <div class="sub">Travail de recherche</div>
        <h2>Mémoire de fin de parcours</h2>
      </div>
    </div>
    <div class="divider"></div>

    <p>Le mémoire de fin de parcours constitue le principal livrable académique du Semestre 6. Sa rédaction s'appuie en parallèle sur le stage à GO-NTIC et sur les modules de méthodologie de rédaction de mémoire pro qui en encadrent la méthodologie.</p>

    <div class="info-card">
      <div class="info-row">
        <div class="info-label">Sujet</div>
        <div class="info-value">Automatisation de la détection d'intrusion et intégration d'un SOC (Security Operations Center)</div>
      </div>
      <div class="info-row">
        <div class="info-label">Thématique</div>
        <div class="info-value">Sécurité opérationnelle, supervision et réponse automatisée aux incidents</div>
      </div>
      <div class="info-row">
        <div class="info-label">Outil de gestion bibliographique</div>
        <div class="info-value">Zotero — bibliographie vérifiée et citations conformes aux normes académiques</div>
      </div>
    </div>

    <h3 style="font-family:'Playfair Display',serif; margin: 2rem 0 0.75rem; color: var(--charcoal); font-size: 1.1rem;">Démarche méthodologique</h3>
    <p>La rédaction s'appuie sur les enseignements du module de méthodologie de rédaction de mémoire pro, avec une gestion bibliographique structurée via Zotero, garantissant des citations vérifiées et une traçabilité rigoureuse des sources mobilisées.</p>
    <p>La problématique retenue interroge la manière dont une PME de prestation de services informatiques peut intégrer des mécanismes de détection et de réponse automatisée aux incidents, à moindre coût, en s'appuyant sur des outils open source (Wazuh, TheHive, Cortex, Suricata). Le plan s'articule en trois grandes parties : un état de l'art de la supervision et de la réponse à incident, une présentation de l'architecture technique proposée, puis une mise en perspective avec les observations de terrain recueillies durant le stage chez GO-NTIC.</p>
  </div>
</div>

<!-- SECTION 8 -->
<div class="section" id="section8">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">08</div>
      <div class="section-title-block">
        <div class="sub">Synthèse</div>
        <h2>Bilan des compétences acquises</h2>
      </div>
    </div>
    <div class="divider"></div>

    <div class="competency-block">
      <div class="competency-title">Réponse aux incidents et gestion de crise cyber</div>
      <ul class="competency-list">
        <li>Démarche structurée de réponse à incident (détection, containment, remédiation)</li>
        <li>Réaction face à une cyber-attaque en cours et coordination des mesures d'urgence</li>
        <li>Rédaction de rapports d'intervention et de retours d'expérience post-incident</li>
      </ul>
    </div>

    <div class="competency-block">
      <div class="competency-title">Méthodologie et communication professionnelle</div>
      <ul class="competency-list">
        <li>Veille technologique structurée et restitution synthétique</li>
        <li>Méthodologie de recherche et de rédaction académique (Zotero, normes de citation)</li>
        <li>Culture d'entreprise et posture professionnelle en environnement de stage</li>
      </ul>
    </div>

    <div class="competency-block">
      <div class="competency-title">Environnement juridique et économique du numérique</div>
      <ul class="competency-list">
        <li>Cadre juridique de l'informatique : données personnelles, responsabilité, contrats</li>
        <li>Régimes de protection de la propriété intellectuelle appliqués au logiciel</li>
        <li>Bases de la gestion et de l'économie appliquées au secteur numérique</li>
        <li>Fondamentaux de la démarche entrepreneuriale</li>
      </ul>
    </div>

    <div class="competency-block">
      <div class="competency-title">Expérience terrain — Stage GO-NTIC</div>
      <ul class="competency-list">
        <li>Installation et configuration d'équipements de vidéosurveillance connectés</li>
        <li>Déploiement de réseaux Wi-Fi en environnement client</li>
        <li>Mise en œuvre d'objets intelligents / IoT et sensibilisation aux risques associés</li>
        <li>Diagnostic de pannes et relation client en environnement d'intervention réelle</li>
      </ul>
    </div>
  </div>
</div>

<!-- SECTION 9 -->
<div class="section" id="section9">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">09</div>
      <div class="section-title-block">
        <div class="sub">Perspective professionnelle</div>
        <h2>Axes de progression et objectifs futurs</h2>
      </div>
    </div>
    <div class="divider"></div>

    <div class="timeline">
      <div class="timeline-item">
        <div class="timeline-period">Court terme · 0 – 6 mois</div>
        <div class="timeline-content">
          <ul class="competency-list" style="margin-top:0.5rem;">
            <li>Finaliser la rédaction et soutenir le mémoire de fin de parcours</li>
            <li>Terminer le stage à GO-NTIC dans de bonnes conditions et obtenir l'attestation correspondante</li>
            <li>Valider l'ensemble des UE et SAÉ du Semestre 6</li>
            <li>Approfondir la maîtrise des outils SOC mobilisés dans le mémoire (Wazuh, TheHive, Cortex, Suricata)</li>
          </ul>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">Moyen terme · 6 mois – 2 ans</div>
        <div class="timeline-content">
          <ul class="competency-list" style="margin-top:0.5rem;">
            <li>Obtenir la Licence Professionnelle Systèmes et Réseaux Informatiques</li>
            <li>Envisager une poursuite d'études en Master (sécurité des systèmes d'information / SOC)</li>
            <li>Consolider les compétences en automatisation SOC (Wazuh, TheHive, Cortex, Suricata)</li>
            <li>Passer une première certification professionnelle (Cisco CCNA ou CompTIA Security+)</li>
          </ul>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">Long terme · 2 – 5 ans</div>
        <div class="timeline-content">
          <ul class="competency-list" style="margin-top:0.5rem;">
            <li>Se spécialiser en cybersécurité : SOC, réponse à incident, ou conseil en sécurité</li>
            <li>Viser des certifications avancées : CEH, OSCP</li>
            <li>Contribuer à la formation et à la sensibilisation en cybersécurité en Afrique de l'Ouest</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- SECTION 10 -->
<div class="section" id="section10">
  <div class="wrapper">
    <div class="section-header">
      <div class="section-num">10</div>
      <div class="section-title-block">
        <div class="sub">Synthèse finale</div>
        <h2>Conclusion générale</h2>
      </div>
    </div>
    <div class="divider"></div>

    <p>Le Semestre 6 clôt trois années de formation à l'ESIG Global Success. Contrairement aux semestres précédents, dominés par l'acquisition de compétences techniques en salle de cours, ce dernier semestre m'installe directement au contact du monde professionnel, à travers le stage chez GO-NTIC, et me confronte à l'exercice académique le plus exigeant de mon cursus : la rédaction d'un mémoire de fin de parcours.</p>

    <p>Le stage chez GO-NTIC m'a confronté à la réalité du terrain, avec ses contraintes matérielles et humaines, tandis que la rédaction du mémoire m'a permis de prendre du recul sur ces observations pour les inscrire dans une réflexion plus large sur l'automatisation de la sécurité. C'est cette articulation entre pratique quotidienne et recul analytique qui, je crois, résume le mieux ce dernier semestre de licence.</p>
  </div>
</div>

<!-- SIGNATURE -->
<div class="signature-block">
  <div class="wrapper">
    <h3>AYAOH Essodomna Jules</h3>
    <p><span class="signature-teal">ESIG Global Success</span> · LP Systèmes et Réseaux Informatiques, Semestre 6</p>
    <p style="margin-top:0.4rem;">Lomé, Togo · 2026</p>
  </div>
</div>

</body>
</html>
