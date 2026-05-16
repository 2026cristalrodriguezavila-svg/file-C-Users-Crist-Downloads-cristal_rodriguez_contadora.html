[cristal_rodriguez_contadora.html](https://github.com/user-attachments/files/27840602/cristal_rodriguez_contadora.html)
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cristal Rodríguez Ávila | Asesoría Contable & Administrativa</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0d1f4e;
    --blue: #1a3a8f;
    --mid-blue: #2756c5;
    --light-blue: #4a8eff;
    --accent: #c8a96e;
    --white: #ffffff;
    --off-white: #f5f7fc;
    --text: #1a1a2e;
    --muted: #6b7a99;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    color: var(--text);
    background: var(--white);
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 100;
    background: rgba(13, 31, 78, 0.95);
    backdrop-filter: blur(12px);
    padding: 18px 60px;
    display: flex; align-items: center; justify-content: space-between;
    border-bottom: 1px solid rgba(200,169,110,0.3);
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    color: var(--white);
    font-size: 1.15rem;
    letter-spacing: 0.04em;
  }
  .nav-logo span { color: var(--accent); }
  .nav-links { display: flex; gap: 36px; list-style: none; }
  .nav-links a {
    color: rgba(255,255,255,0.8);
    text-decoration: none;
    font-size: 0.875rem;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }
  .nav-cta {
    background: var(--accent);
    color: var(--navy) !important;
    padding: 10px 22px;
    border-radius: 4px;
    font-weight: 600 !important;
  }

  /* HERO */
  .hero {
    min-height: 100vh;
    background: var(--navy);
    display: flex; align-items: center;
    position: relative; overflow: hidden;
    padding-top: 80px;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background: 
      radial-gradient(ellipse 60% 80% at 80% 50%, rgba(39,86,197,0.25) 0%, transparent 70%),
      radial-gradient(ellipse 40% 60% at 20% 80%, rgba(200,169,110,0.08) 0%, transparent 60%);
  }
  .hero-grid {
    position: absolute; inset: 0; opacity: 0.04;
    background-image: linear-gradient(rgba(255,255,255,0.5) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.5) 1px, transparent 1px);
    background-size: 50px 50px;
  }
  .hero-content {
    position: relative; z-index: 2;
    max-width: 1200px; margin: 0 auto; padding: 0 60px;
    display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: center;
  }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(200,169,110,0.15);
    border: 1px solid rgba(200,169,110,0.4);
    padding: 8px 18px; border-radius: 100px;
    color: var(--accent); font-size: 0.8rem;
    font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase;
    margin-bottom: 28px;
    animation: fadeUp 0.6s ease both;
  }
  .hero-badge::before { content: '✦'; font-size: 0.7rem; }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 5vw, 4rem);
    color: var(--white);
    line-height: 1.15;
    margin-bottom: 12px;
    animation: fadeUp 0.7s 0.1s ease both;
  }
  .hero h1 em {
    font-style: italic;
    color: var(--accent);
  }
  .hero-subtitle {
    color: rgba(255,255,255,0.55);
    font-size: 0.8rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 24px;
    animation: fadeUp 0.7s 0.2s ease both;
  }
  .hero p {
    color: rgba(255,255,255,0.7);
    font-size: 1.05rem;
    line-height: 1.8;
    margin-bottom: 40px;
    animation: fadeUp 0.7s 0.3s ease both;
    font-weight: 300;
  }
  .hero-actions {
    display: flex; gap: 16px; flex-wrap: wrap;
    animation: fadeUp 0.7s 0.4s ease both;
  }
  .btn-primary {
    background: var(--accent);
    color: var(--navy);
    padding: 15px 32px;
    border: none; border-radius: 4px;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem; font-weight: 700;
    letter-spacing: 0.05em; text-transform: uppercase;
    cursor: pointer; text-decoration: none;
    transition: transform 0.2s, box-shadow 0.2s;
    display: inline-block;
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 10px 30px rgba(200,169,110,0.4); }
  .btn-outline {
    background: transparent;
    color: var(--white);
    padding: 15px 32px;
    border: 1px solid rgba(255,255,255,0.3);
    border-radius: 4px;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem; font-weight: 500;
    cursor: pointer; text-decoration: none;
    transition: border-color 0.2s, background 0.2s;
    display: inline-block;
  }
  .btn-outline:hover { border-color: var(--accent); background: rgba(200,169,110,0.08); }

  /* DROPDOWN */
  .dropdown-wrapper { position: relative; display: inline-block; }
  .dropdown-menu {
    display: none;
    position: absolute;
    top: calc(100% + 10px);
    left: 0;
    background: var(--white);
    border-radius: 10px;
    box-shadow: 0 20px 50px rgba(13,31,78,0.2);
    min-width: 240px;
    overflow: hidden;
    border: 1px solid rgba(26,58,143,0.1);
    z-index: 200;
    animation: dropIn 0.2s ease;
  }
  .dropdown-menu.open { display: block; }
  @keyframes dropIn {
    from { opacity: 0; transform: translateY(-8px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .dropdown-header {
    background: var(--navy);
    padding: 12px 20px;
    color: var(--accent);
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
  }
  .dropdown-item {
    display: flex; align-items: center; gap: 12px;
    padding: 13px 20px;
    color: var(--navy);
    text-decoration: none;
    font-size: 0.92rem;
    font-weight: 500;
    border-bottom: 1px solid rgba(0,0,0,0.05);
    transition: background 0.15s, color 0.15s;
  }
  .dropdown-item:last-child { border-bottom: none; }
  .dropdown-item:hover { background: var(--off-white); color: var(--mid-blue); }
  .dropdown-item-icon { font-size: 1rem; flex-shrink: 0; }
  .hero-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 16px;
    padding: 40px;
    backdrop-filter: blur(10px);
    animation: fadeUp 0.8s 0.2s ease both;
    position: relative;
  }
  .hero-card::before {
    content: '';
    position: absolute; top: -1px; left: 40px; right: 40px; height: 2px;
    background: linear-gradient(90deg, transparent, var(--accent), transparent);
  }
  .hero-name {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 2rem;
    color: var(--white);
    margin-bottom: 4px;
  }
  .hero-title {
    color: var(--accent);
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 24px;
  }
  .hero-divider {
    height: 1px;
    background: rgba(255,255,255,0.1);
    margin-bottom: 24px;
  }
  .hero-info-item {
    display: flex; align-items: center; gap: 14px;
    margin-bottom: 16px;
    color: rgba(255,255,255,0.75);
    font-size: 0.9rem;
  }
  .hero-info-icon {
    width: 36px; height: 36px;
    background: rgba(39,86,197,0.3);
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1rem; flex-shrink: 0;
  }
  .hero-cedula {
    display: flex; align-items: center; gap: 10px;
    margin-top: 20px;
    padding: 12px 16px;
    background: rgba(200,169,110,0.1);
    border: 1px solid rgba(200,169,110,0.25);
    border-radius: 8px;
    color: var(--accent);
    font-size: 0.8rem;
    font-weight: 600;
    letter-spacing: 0.05em;
  }
  .hero-stats {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; margin-top: 24px;
  }
  .hero-stat {
    text-align: center;
    padding: 16px 8px;
    background: rgba(255,255,255,0.04);
    border-radius: 8px;
    border: 1px solid rgba(255,255,255,0.07);
  }
  .hero-stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem; color: var(--accent); font-weight: 700;
  }
  .hero-stat-label { font-size: 0.7rem; color: rgba(255,255,255,0.5); text-transform: uppercase; letter-spacing: 0.05em; margin-top: 4px; }

  /* SERVICES */
  .services {
    padding: 110px 60px;
    background: var(--off-white);
    position: relative;
  }
  .section-tag {
    color: var(--mid-blue);
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    margin-bottom: 14px;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 3.5vw, 2.8rem);
    color: var(--navy);
    line-height: 1.2;
    margin-bottom: 16px;
  }
  .section-title em { font-style: italic; color: var(--mid-blue); }
  .section-subtitle {
    color: var(--muted);
    font-size: 1rem;
    line-height: 1.7;
    max-width: 500px;
    font-weight: 300;
  }
  .section-header {
    display: flex; justify-content: space-between; align-items: flex-end;
    margin-bottom: 60px; gap: 40px;
  }
  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
    max-width: 1200px; margin: 0 auto;
  }
  .service-card {
    background: var(--white);
    border-radius: 12px;
    padding: 36px 30px;
    border: 1px solid rgba(0,0,0,0.06);
    transition: transform 0.3s, box-shadow 0.3s, border-color 0.3s;
    position: relative; overflow: hidden;
  }
  .service-card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 3px;
    background: linear-gradient(90deg, var(--blue), var(--light-blue));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s;
  }
  .service-card:hover { transform: translateY(-6px); box-shadow: 0 20px 50px rgba(13,31,78,0.1); border-color: rgba(39,86,197,0.2); }
  .service-card:hover::before { transform: scaleX(1); }
  .service-icon {
    width: 54px; height: 54px;
    background: linear-gradient(135deg, rgba(26,58,143,0.1), rgba(74,142,255,0.1));
    border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.5rem;
    margin-bottom: 22px;
  }
  .service-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    color: var(--navy);
    margin-bottom: 10px;
  }
  .service-card p {
    color: var(--muted);
    font-size: 0.88rem;
    line-height: 1.75;
    font-weight: 300;
  }
  .service-tag {
    display: inline-block;
    margin-top: 16px;
    padding: 4px 12px;
    background: rgba(26,58,143,0.06);
    color: var(--mid-blue);
    font-size: 0.72rem;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    border-radius: 100px;
  }

  /* VALUES */
  .values {
    padding: 110px 60px;
    background: var(--navy);
    position: relative; overflow: hidden;
  }
  .values::before {
    content: '';
    position: absolute; top: -200px; right: -200px;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(39,86,197,0.2) 0%, transparent 70%);
    border-radius: 50%;
  }
  .values-inner { max-width: 1200px; margin: 0 auto; position: relative; z-index: 1; }
  .values .section-tag { color: var(--accent); }
  .values .section-title { color: var(--white); }
  .values-grid {
    display: grid; grid-template-columns: repeat(4, 1fr); gap: 24px; margin-top: 60px;
  }
  .value-card {
    text-align: center; padding: 36px 20px;
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 12px;
    transition: background 0.3s, border-color 0.3s, transform 0.3s;
  }
  .value-card:hover { background: rgba(255,255,255,0.08); border-color: rgba(200,169,110,0.3); transform: translateY(-4px); }
  .value-icon {
    font-size: 2rem; margin-bottom: 18px;
    width: 64px; height: 64px;
    background: rgba(39,86,197,0.2);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 18px;
  }
  .value-card h3 { color: var(--accent); font-family: 'Playfair Display', serif; font-size: 1.1rem; margin-bottom: 10px; }
  .value-card p { color: rgba(255,255,255,0.55); font-size: 0.85rem; line-height: 1.7; font-weight: 300; }

  /* CTA */
  .cta-section {
    padding: 110px 60px;
    background: var(--white);
  }
  .cta-inner {
    max-width: 1200px; margin: 0 auto;
    display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: center;
  }
  .cta-section .section-title { margin-bottom: 20px; }
  .cta-section p { color: var(--muted); font-size: 1rem; line-height: 1.8; font-weight: 300; margin-bottom: 36px; }
  .contact-methods { display: flex; flex-direction: column; gap: 16px; }
  .contact-item {
    display: flex; align-items: center; gap: 16px;
    padding: 20px 24px;
    background: var(--off-white);
    border-radius: 10px;
    border: 1px solid transparent;
    text-decoration: none;
    color: var(--text);
    transition: border-color 0.2s, background 0.2s;
  }
  .contact-item:hover { border-color: var(--mid-blue); background: rgba(26,58,143,0.04); }
  .contact-item-icon {
    width: 44px; height: 44px;
    background: var(--navy);
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.2rem;
    flex-shrink: 0;
  }
  .contact-item-label { font-size: 0.72rem; color: var(--muted); text-transform: uppercase; letter-spacing: 0.08em; font-weight: 600; }
  .contact-item-value { font-size: 0.95rem; font-weight: 500; color: var(--navy); margin-top: 2px; }
  .contact-coverage {
    display: flex; align-items: center; gap: 10px;
    color: var(--muted); font-size: 0.85rem;
    padding: 14px 20px;
    border: 1px solid rgba(0,0,0,0.08);
    border-radius: 8px;
    margin-top: 8px;
  }

  /* FOOTER */
  footer {
    background: var(--navy);
    border-top: 1px solid rgba(200,169,110,0.2);
    padding: 40px 60px;
    text-align: center;
    color: rgba(255,255,255,0.4);
    font-size: 0.82rem;
  }
  footer strong { color: var(--accent); }

  /* FLOATING WHATSAPP */
  .whatsapp-btn {
    position: fixed; bottom: 30px; right: 30px; z-index: 999;
    background: #25d366;
    color: white;
    width: 60px; height: 60px;
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.6rem;
    text-decoration: none;
    box-shadow: 0 4px 20px rgba(37,211,102,0.5);
    animation: pulse 2s ease infinite;
  }
  @keyframes pulse {
    0%, 100% { box-shadow: 0 4px 20px rgba(37,211,102,0.5); }
    50% { box-shadow: 0 4px 40px rgba(37,211,102,0.8); }
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @media (max-width: 900px) {
    nav { padding: 16px 24px; }
    .nav-links { display: none; }
    .hero-content, .cta-inner { grid-template-columns: 1fr; gap: 40px; padding: 0 24px; }
    .services, .values, .cta-section { padding: 70px 24px; }
    .services-grid { grid-template-columns: 1fr; }
    .values-grid { grid-template-columns: repeat(2, 1fr); }
    .section-header { flex-direction: column; }
    .hero { padding-top: 80px; }
    .hero-stats { grid-template-columns: repeat(3, 1fr); }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">CR <span>Asesoría</span></div>
  <ul class="nav-links">
    <li><a href="#servicios">Servicios</a></li>
    <li><a href="#valores">Valores</a></li>
    <li><a href="#contacto">Contacto</a></li>
    <li><a href="https://wa.me/524433544092" class="nav-cta">WhatsApp</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-grid"></div>
  <div class="hero-content">
    <div>
      <div class="hero-badge">Asesoría Contable & Administrativa</div>
      <p class="hero-subtitle">Soluciones claras para tu negocio</p>
      <h1>Tu <em>contabilidad</em>, en manos expertas</h1>
      <p>Te ayudo a mantener tu negocio en orden, cumplir con tus obligaciones fiscales y tomar decisiones financieras con seguridad. Atención personalizada en todo México.</p>
      <div class="hero-actions">
        <a href="https://wa.me/524433544092" class="btn-primary">Solicitar asesoría</a>
        <div class="dropdown-wrapper">
          <button class="btn-outline" onclick="toggleDropdown()" id="serviciosBtn">Ver servicios ▾</button>
          <div class="dropdown-menu" id="serviciosMenu">
            <div class="dropdown-header">Servicios</div>
            <a href="#servicios" class="dropdown-item" onclick="closeDropdown()"><span class="dropdown-item-icon">📋</span> Declaraciones SAT</a>
            <a href="#servicios" class="dropdown-item" onclick="closeDropdown()"><span class="dropdown-item-icon">💼</span> RESICO</a>
            <a href="#servicios" class="dropdown-item" onclick="closeDropdown()"><span class="dropdown-item-icon">🧾</span> Facturación CFDI</a>
            <a href="#servicios" class="dropdown-item" onclick="closeDropdown()"><span class="dropdown-item-icon">🏛️</span> Trámites SAT</a>
            <a href="#servicios" class="dropdown-item" onclick="closeDropdown()"><span class="dropdown-item-icon">📊</span> Administración para pequeños negocios</a>
          </div>
        </div>
      </div>
    </div>
    <div class="hero-card">
      <div class="hero-name">Cristal Rodríguez Ávila</div>
      <div class="hero-title">Contadora y Administradora de Empresas</div>
      <div class="hero-divider"></div>
      <div class="hero-info-item">
        <div class="hero-info-icon">📞</div>
        <span>44-33-54-40-92</span>
      </div>
      <div class="hero-info-item">
        <div class="hero-info-icon">✉️</div>
        <span>lic.cristal.rodriguez.avila@gmail.com</span>
      </div>
      <div class="hero-info-item">
        <div class="hero-info-icon">🌐</div>
        <span>Atención en línea en todo México</span>
      </div>
      <div class="hero-cedula">🎓 &nbsp; Cédula Profesional: 15403182</div>
      <div class="hero-stats">
        <div class="hero-stat">
          <div class="hero-stat-num">100%</div>
          <div class="hero-stat-label">Digital</div>
        </div>
        <div class="hero-stat">
          <div class="hero-stat-num">MX</div>
          <div class="hero-stat-label">Todo México</div>
        </div>
        <div class="hero-stat">
          <div class="hero-stat-num">SAT</div>
          <div class="hero-stat-label">Cumplimiento</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="servicios">
  <div style="max-width:1200px;margin:0 auto;">
    <div class="section-header">
      <div>
        <div class="section-tag">Lo que ofrezco</div>
        <h2 class="section-title">Servicios <em>especializados</em><br>para tu negocio</h2>
      </div>
      <p class="section-subtitle">Desde declaraciones hasta manuales administrativos, tengo todo lo que necesitas para mantener tu empresa en regla.</p>
    </div>
    <div class="services-grid">
      <div class="service-card">
        <div class="service-icon">👤</div>
        <h3>Declaraciones Personas Físicas</h3>
        <p>Resico, actividad empresarial, plataformas tecnológicas, arrendamiento y declaraciones anuales.</p>
        <span class="service-tag">SAT · Fiscal</span>
      </div>
      <div class="service-card">
        <div class="service-icon">🏛️</div>
        <h3>Trámites Administrativos</h3>
        <p>Gestión de trámites ante el Ayuntamiento, IMSS y SAT. Agilizo todos los procesos para ti.</p>
        <span class="service-tag">AYUNTAMIENTO · IMSS · SAT</span>
      </div>
      <div class="service-card">
        <div class="service-icon">🧾</div>
        <h3>Facturas Electrónicas</h3>
        <p>Emisión y gestión de CFDI. Facturación correcta y oportuna para que cumplas con el SAT sin complicaciones.</p>
        <span class="service-tag">CFDI · SAT</span>
      </div>
      <div class="service-card">
        <div class="service-icon">📊</div>
        <h3>Contabilidad en General</h3>
        <p>Registro contable completo, estados financieros, balances y toda la contabilidad de tu empresa.</p>
        <span class="service-tag">Contabilidad</span>
      </div>
      <div class="service-card">
        <div class="service-icon">📋</div>
        <h3>Manuales de Administración</h3>
        <p>Diseño y elaboración de manuales de procedimientos y organización para que tu empresa funcione con orden.</p>
        <span class="service-tag">Administración</span>
      </div>
      <div class="service-card">
        <div class="service-icon">⚙️</div>
        <h3>Costos de Producción</h3>
        <p>Análisis y cálculo de costos para que conozcas la rentabilidad real de tu negocio y tomes mejores decisiones.</p>
        <span class="service-tag">Costos · Rentabilidad</span>
      </div>
    </div>
  </div>
</section>

<!-- VALUES -->
<section class="values" id="valores">
  <div class="values-inner">
    <div class="section-tag">Por qué elegirme</div>
    <h2 class="section-title" style="color:var(--white);">Mi compromiso<br><em style="color:var(--accent);">contigo</em></h2>
    <div class="values-grid">
      <div class="value-card">
        <div class="value-icon">🔒</div>
        <h3>Confidencialidad</h3>
        <p>Tu información financiera y fiscal está protegida. Manejo de datos con total discreción y seguridad.</p>
      </div>
      <div class="value-card">
        <div class="value-icon">🤝</div>
        <h3>Compromiso</h3>
        <p>Me involucro en tu negocio como si fuera el mío. Tus metas son mis metas.</p>
      </div>
      <div class="value-card">
        <div class="value-icon">⏰</div>
        <h3>Puntualidad</h3>
        <p>Entrego en tiempo y forma. No hay excusas para perder fechas límite del SAT o reportes.</p>
      </div>
      <div class="value-card">
        <div class="value-icon">👩‍💼</div>
        <h3>Atención Personalizada</h3>
        <p>Cada cliente es único. Soluciones a la medida de tu situación y tipo de negocio.</p>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT CTA -->
<section class="cta-section" id="contacto">
  <div class="cta-inner">
    <div>
      <div class="section-tag">¿Lista para empezar?</div>
      <h2 class="section-title">Hablemos sobre<br>tu <em>negocio</em></h2>
      <p>Agenda una consulta sin costo y descubre cómo puedo ayudarte a tener tu contabilidad al día, cumplir con el SAT y hacer crecer tu empresa.</p>
      <a href="https://wa.me/524433544092?text=Hola%20Cristal%2C%20me%20interesa%20una%20asesor%C3%ADa%20contable" class="btn-primary">Escribir por WhatsApp →</a>
    </div>
    <div class="contact-methods">
      <a href="tel:4433544092" class="contact-item">
        <div class="contact-item-icon">📞</div>
        <div>
          <div class="contact-item-label">Teléfono / WhatsApp</div>
          <div class="contact-item-value">44-33-54-40-92</div>
        </div>
      </a>
      <a href="mailto:lic.cristal.rodriguez.avila@gmail.com" class="contact-item">
        <div class="contact-item-icon">✉️</div>
        <div>
          <div class="contact-item-label">Correo electrónico</div>
          <div class="contact-item-value">lic.cristal.rodriguez.avila@gmail.com</div>
        </div>
      </a>
      <div class="contact-coverage">
        🌎 &nbsp; Atención en línea disponible en todo México
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>© 2025 <strong>Cristal Rodríguez Ávila</strong> — Contadora y Administradora de Empresas &nbsp;·&nbsp; Cédula Profesional: 15403182</p>
</footer>

<script>
  function toggleDropdown() {
    document.getElementById('serviciosMenu').classList.toggle('open');
  }
  function closeDropdown() {
    document.getElementById('serviciosMenu').classList.remove('open');
  }
  document.addEventListener('click', function(e) {
    const wrapper = document.querySelector('.dropdown-wrapper');
    if (wrapper && !wrapper.contains(e.target)) closeDropdown();
  });
</script>

<!-- WhatsApp flotante -->
<a href="https://wa.me/524433544092?text=Hola%20Cristal%2C%20me%20interesa%20una%20asesor%C3%ADa%20contable" class="whatsapp-btn" title="Escríbeme por WhatsApp">💬</a>

</body>
</html>
