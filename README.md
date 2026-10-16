<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>VaYu Solutions | Where Technology Meets Creativity</title>
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Outfit:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg-obsidian: #0b0d11;
      --bg-charcoal: #13161c;
      --bg-surface: #1a1e26;
      --orange-core: #ff6b00;
      --orange-bright: #ffa800;
      --orange-glow: rgba(255, 107, 0, 0.25);
      --silver-light: #f1f5f9;
      --silver-mid: #cbd5e1;
      --silver-muted: #94a3b8;
      --border-metallic: rgba(203, 213, 225, 0.12);
      --border-orange: rgba(255, 107, 0, 0.45);
      --grad-orange: linear-gradient(135deg, #ff5500 0%, #ff9900 100%);
      --grad-silver: linear-gradient(180deg, #ffffff 0%, #94a3b8 100%);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      background-color: var(--bg-obsidian);
      color: var(--silver-light);
      font-family: 'Inter', sans-serif;
      line-height: 1.65;
      width: 100%;
      overflow-x: hidden;
      background-image: 
        radial-gradient(circle at 85% 10%, rgba(255, 107, 0, 0.08) 0%, transparent 40%),
        radial-gradient(circle at 15% 80%, rgba(148, 163, 184, 0.05) 0%, transparent 40%);
    }

    h1, h2, h3, h4, .brand-font {
      font-family: 'Outfit', sans-serif;
    }

    /* Universal Content Wrapper to keep layouts clean & contained on large screens */
    .site-wrapper {
      width: 100%;
      max-width: 1320px;
      margin: 0 auto;
      padding: 0 5%;
    }

    /* Navigation Bar */
    header {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: rgba(11, 13, 17, 0.9);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid var(--border-metallic);
      width: 100%;
    }

    .nav-inner {
      max-width: 1320px;
      margin: 0 auto;
      padding: 1.1rem 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo-wrap {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      text-decoration: none;
    }

    .logo-mark {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background: var(--bg-charcoal);
      border: 1.5px solid var(--border-orange);
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 0 15px var(--orange-glow);
    }

    .logo-text {
      display: flex;
      flex-direction: column;
      line-height: 1;
    }

    .logo-main {
      font-family: 'Outfit', sans-serif;
      font-size: 1.45rem;
      font-weight: 800;
      letter-spacing: 1px;
    }

    .logo-va {
      background: var(--grad-silver);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .logo-yu {
      background: var(--grad-orange);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .logo-sub {
      font-size: 0.62rem;
      letter-spacing: 3.5px;
      color: var(--silver-muted);
      font-weight: 600;
      margin-top: 2px;
    }

    .nav-links {
      display: flex;
      gap: 2.25rem;
      list-style: none;
    }

    .nav-links a {
      color: var(--silver-mid);
      text-decoration: none;
      font-size: 0.9rem;
      font-weight: 500;
      letter-spacing: 0.3px;
      transition: color 0.25s ease;
    }

    .nav-links a:hover {
      color: var(--orange-bright);
    }

    .nav-btn {
      background: transparent;
      border: 1px solid var(--border-orange);
      color: var(--silver-light);
      padding: 0.6rem 1.35rem;
      border-radius: 6px;
      font-size: 0.88rem;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.25s ease;
    }

    .nav-btn:hover {
      background: var(--grad-orange);
      color: #0b0d11;
      border-color: transparent;
      box-shadow: 0 0 20px var(--orange-glow);
    }

    /* Hero Section */
    .hero-section {
      width: 100%;
      padding: 6.5rem 0 5.5rem;
    }

    .hero {
      display: grid;
      grid-template-columns: 1.15fr 0.85fr;
      gap: 3.5rem;
      align-items: center;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.35rem 0.9rem;
      background: rgba(255, 107, 0, 0.08);
      border-left: 3px solid var(--orange-core);
      color: var(--orange-bright);
      font-size: 0.8rem;
      font-weight: 600;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      margin-bottom: 1.5rem;
    }

    .hero h1 {
      font-size: clamp(2.4rem, 4.5vw, 3.6rem);
      font-weight: 800;
      line-height: 1.12;
      letter-spacing: -0.5px;
      margin-bottom: 1.5rem;
      color: #ffffff;
    }

    .hero h1 .accent-text {
      background: var(--grad-orange);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero p {
      font-size: 1.1rem;
      color: var(--silver-muted);
      margin-bottom: 2.25rem;
      max-width: 580px;
    }

    .hero-actions {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .btn-solid {
      background: var(--grad-orange);
      color: #0b0d11;
      padding: 0.95rem 1.85rem;
      border-radius: 6px;
      font-weight: 700;
      font-size: 0.95rem;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      transition: all 0.25s ease;
      box-shadow: 0 6px 24px var(--orange-glow);
    }

    .btn-solid:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 30px rgba(255, 107, 0, 0.4);
    }

    .btn-outline {
      background: var(--bg-charcoal);
      border: 1px solid var(--border-metallic);
      color: var(--silver-light);
      padding: 0.95rem 1.85rem;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.95rem;
      text-decoration: none;
      transition: all 0.25s ease;
    }

    .btn-outline:hover {
      border-color: var(--silver-mid);
      background: var(--bg-surface);
    }

    /* Hero Visual Emblem */
    .hero-visual {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .emblem-card {
      width: 100%;
      max-width: 400px;
      aspect-ratio: 1 / 1;
      border-radius: 50%;
      background: radial-gradient(circle at 30% 30%, #1e232d 0%, #0d1015 80%);
      border: 2px solid var(--border-metallic);
      box-shadow: 
        0 20px 50px rgba(0, 0, 0, 0.8),
        inset 0 0 35px rgba(255, 107, 0, 0.12);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
      padding: 2.5rem;
      text-align: center;
    }

    .emblem-card::before {
      content: '';
      position: absolute;
      inset: 10px;
      border-radius: 50%;
      border: 1px solid rgba(255, 107, 0, 0.3);
      pointer-events: none;
    }

    .emblem-svg {
      width: 135px;
      height: 135px;
      margin-bottom: 1rem;
      filter: drop-shadow(0 8px 16px rgba(0,0,0,0.6));
    }

    .emblem-title {
      font-family: 'Outfit', sans-serif;
      font-size: 2.1rem;
      font-weight: 800;
      letter-spacing: 2px;
      line-height: 1;
    }

    .emblem-subtitle {
      font-size: 0.78rem;
      letter-spacing: 6px;
      color: var(--silver-mid);
      margin-top: 0.35rem;
      font-weight: 600;
    }

    /* Section Containers */
    section {
      width: 100%;
      padding: 5rem 0;
    }

    .section-head {
      margin-bottom: 3.25rem;
    }

    .section-head h2 {
      font-size: clamp(1.85rem, 3vw, 2.4rem);
      font-weight: 700;
      color: #ffffff;
      margin-bottom: 0.6rem;
    }

    .section-head p {
      color: var(--silver-muted);
      max-width: 640px;
      font-size: 1rem;
    }

    /* Who We Are & Founder Section */
    .identity-panel {
      background: var(--bg-charcoal);
      border: 1px solid var(--border-metallic);
      border-radius: 12px;
      padding: 3.25rem;
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 3rem;
      align-items: center;
      position: relative;
    }

    .identity-panel::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 3px;
      background: var(--grad-orange);
      border-radius: 12px 12px 0 0;
    }

    .identity-copy h3 {
      font-size: 1.65rem;
      margin-bottom: 1.1rem;
      color: #fff;
    }

    .identity-copy p {
      color: var(--silver-mid);
      margin-bottom: 1.1rem;
      font-size: 1.02rem;
    }

    .metrics-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1rem;
    }

    .metric-box {
      background: var(--bg-surface);
      border: 1px solid var(--border-metallic);
      padding: 1.5rem 1.25rem;
      border-radius: 8px;
    }

    .metric-box strong {
      display: block;
      font-family: 'Outfit', sans-serif;
      font-size: 1.65rem;
      color: var(--orange-bright);
      margin-bottom: 0.25rem;
    }

    .metric-box span {
      font-size: 0.85rem;
      color: var(--silver-muted);
      font-weight: 500;
    }

    /* Founder Message Section */
    .founder-section {
      width: 100%;
      padding-bottom: 5rem;
    }

    .founder-card {
      background: linear-gradient(145deg, #161a22 0%, #0d1015 100%);
      border: 1px solid var(--border-orange);
      border-radius: 12px;
      padding: 3rem;
      display: grid;
      grid-template-columns: 0.35fr 0.65fr;
      gap: 2.5rem;
      align-items: center;
      box-shadow: 0 15px 40px rgba(0,0,0,0.6);
    }

    .founder-avatar-wrap {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
    }

    .founder-badge-icon {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      background: var(--grad-orange);
      color: #0b0d11;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Outfit', sans-serif;
      font-size: 1.8rem;
      font-weight: 800;
      margin-bottom: 1rem;
      box-shadow: 0 0 20px var(--orange-glow);
    }

    .founder-name {
      font-family: 'Outfit', sans-serif;
      font-size: 1.25rem;
      font-weight: 700;
      color: #fff;
    }

    .founder-title {
      font-size: 0.85rem;
      color: var(--orange-bright);
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-top: 0.2rem;
    }

    .founder-message-content h3 {
      font-size: 1.5rem;
      color: #fff;
      margin-bottom: 1rem;
    }

    .founder-message-content blockquote {
      font-style: italic;
      color: var(--silver-mid);
      font-size: 1.02rem;
      line-height: 1.7;
      border-left: 3px solid var(--orange-core);
      padding-left: 1.25rem;
      margin-bottom: 1.25rem;
    }

    .founder-signoff {
      font-size: 0.9rem;
      color: var(--silver-muted);
      font-weight: 500;
    }

    /* Core Services Grid */
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.5rem;
    }

    .service-item {
      background: var(--bg-charcoal);
      border: 1px solid var(--border-metallic);
      border-radius: 10px;
      padding: 2.25rem 1.85rem;
      transition: all 0.3s ease;
      position: relative;
    }

    .service-item:hover {
      transform: translateY(-4px);
      border-color: var(--border-orange);
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.5);
    }

    .icon-box {
      width: 46px;
      height: 46px;
      background: rgba(255, 107, 0, 0.1);
      border: 1px solid rgba(255, 107, 0, 0.3);
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 1.5rem;
      color: var(--orange-bright);
    }

    .service-item h3 {
      font-size: 1.2rem;
      margin-bottom: 0.75rem;
      color: #ffffff;
    }

    .service-item p {
      font-size: 0.92rem;
      color: var(--silver-muted);
    }

    /* Why VaYu Section */
    .why-panel {
      background: var(--bg-charcoal);
      border: 1px solid var(--border-metallic);
      border-radius: 12px;
      padding: 3.25rem;
      position: relative;
    }

    .why-panel::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 3px;
      background: var(--grad-orange);
      border-radius: 12px 12px 0 0;
    }

    .why-panel h3 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
      color: #fff;
    }

    .why-panel p {
      color: var(--silver-mid);
      margin-bottom: 2rem;
      font-size: 1.05rem;
      max-width: 800px;
    }

    .pillar-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 1.5rem;
    }

    .pillar-card {
      background: var(--bg-surface);
      border: 1px solid var(--border-metallic);
      padding: 1.75rem;
      border-radius: 8px;
    }

    .pillar-card h4 {
      font-size: 1.1rem;
      color: #fff;
      margin-bottom: 0.5rem;
    }

    .pillar-card p {
      font-size: 0.9rem;
      color: var(--silver-muted);
      margin-bottom: 0;
    }

    /* Contact Banner & Social Channels */
    .contact-banner {
      background: var(--bg-charcoal);
      border: 1px solid var(--border-metallic);
      border-radius: 12px;
      padding: 3.5rem;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      align-items: center;
    }

    .contact-pitch h2 {
      font-size: clamp(1.8rem, 3vw, 2.3rem);
      color: #fff;
      margin-bottom: 1rem;
    }

    .contact-pitch p {
      color: var(--silver-muted);
      margin-bottom: 1.5rem;
    }

    .contact-channels {
      display: grid;
      gap: 1rem;
    }

    .channel-card {
      background: var(--bg-surface);
      border: 1px solid var(--border-metallic);
      padding: 1rem 1.25rem;
      border-radius: 8px;
      display: flex;
      align-items: center;
      gap: 1rem;
      text-decoration: none;
      color: var(--silver-light);
      transition: border-color 0.25s ease, transform 0.25s ease;
    }

    .channel-card:hover {
      border-color: var(--orange-core);
      transform: translateX(4px);
    }

    .channel-icon {
      width: 36px;
      height: 36px;
      border-radius: 6px;
      background: rgba(255, 107, 0, 0.1);
      color: var(--orange-bright);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }

    .channel-meta small {
      display: block;
      font-size: 0.72rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--silver-muted);
    }

    .channel-meta strong {
      font-size: 0.92rem;
      font-weight: 600;
      color: #fff;
    }

    /* Social Media Strip */
    .social-section {
      width: 100%;
      padding-bottom: 5rem;
    }

    .social-strip {
      display: flex;
      justify-content: center;
      gap: 1.25rem;
      flex-wrap: wrap;
    }

    .social-pill {
      background: var(--bg-charcoal);
      border: 1px solid var(--border-metallic);
      padding: 0.85rem 1.5rem;
      border-radius: 50px;
      display: flex;
      align-items: center;
      gap: 0.75rem;
      text-decoration: none;
      color: var(--silver-light);
      font-size: 0.9rem;
      font-weight: 500;
      transition: all 0.25s ease;
    }

    .social-pill:hover {
      border-color: var(--orange-core);
      background: var(--bg-surface);
      transform: translateY(-2px);
    }

    .social-pill svg {
      width: 18px;
      height: 18px;
      fill: var(--orange-bright);
    }

    /* Footer */
    footer {
      border-top: 1px solid var(--border-metallic);
      padding: 2.25rem 0;
      text-align: center;
      color: var(--silver-muted);
      font-size: 0.85rem;
      width: 100%;
    }

    /* Responsive Media Queries */
    @media (max-width: 900px) {
      .hero,
      .identity-panel,
      .founder-card,
      .contact-banner {
        grid-template-columns: 1fr;
      }
      .hero-section {
        padding-top: 4rem;
      }
      .emblem-card {
        max-width: 300px;
        margin: 0 auto;
      }
      .nav-links {
        display: none;
      }
      .identity-panel,
      .founder-card,
      .why-panel,
      .contact-banner {
        padding: 2rem;
      }
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="nav-inner">
      <a href="#" class="logo-wrap">
        <div class="logo-mark">
          <svg width="24" height="24" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M6 10L15 30L22 14" stroke="#E2E8F0" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M18 14L25 24L34 10" stroke="#FF6B00" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M29 10H34V15" stroke="#FFA800" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div class="logo-text">
          <div class="logo-main"><span class="logo-va">VA</span><span class="logo-yu">YU</span></div>
          <div class="logo-sub">SOLUTIONS</div>
        </div>
      </a>

      <ul class="nav-links">
        <li><a href="#identity">Who We Are</a></li>
        <li><a href="#founder">Founder</a></li>
        <li><a href="#capabilities">Core Services</a></li>
        <li><a href="#why-vayu">Why VaYu</a></li>
      </ul>

      <a href="#inquire" class="nav-btn">Schedule a Consultation</a>
    </div>
  </header>

  <!-- Hero Section -->
  <div class="hero-section">
    <div class="site-wrapper">
      <div class="hero">
        <div class="hero-content">
          <div class="eyebrow">Where Technology Meets Creativity</div>
          <h1>High-Impact Digital Systems Built to <span class="accent-text">Accelerate Growth</span></h1>
          <p>Full-service partner for startups and growing enterprises. We combine cutting-edge technology and creative strategy across web, apps, SEO, ads, and marketing to elevate your visibility and attract qualified leads.</p>
          <div class="hero-actions">
            <a href="#capabilities" class="btn-solid">
              Explore Capabilities
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
            </a>
            <a href="tel:+919470011490" class="btn-outline">Direct Line: +91 94700 11490</a>
          </div>
        </div>

        <!-- Custom Vector Emblem Mirroring the VaYu Logo -->
        <div class="hero-visual">
          <div class="emblem-card">
            <svg class="emblem-svg" viewBox="0 0 120 100" fill="none" xmlns="http://www.w3.org/2000/svg">
              <defs>
                <linearGradient id="silverGrad" x1="0" y1="0" x2="0" y2="100" gradientUnits="userSpaceOnUse">
                  <stop offset="0%" stop-color="#FFFFFF"/>
                  <stop offset="100%" stop-color="#64748B"/>
                </linearGradient>
                <linearGradient id="orangeGrad" x1="40" y1="80" x2="110" y2="10" gradientUnits="userSpaceOnUse">
                  <stop offset="0%" stop-color="#FF5500"/>
                  <stop offset="100%" stop-color="#FFB800"/>
                </linearGradient>
              </defs>
              <path d="M12 20L38 82L62 28H48L38 56L26 20H12Z" fill="url(#silverGrad)"/>
              <path d="M52 28L70 54V82H82V54L96 36L104 44L114 14L84 22L90 28L76 44L64 28H52Z" fill="url(#orangeGrad)"/>
            </svg>
            <div class="emblem-title"><span class="logo-va">VA</span><span class="logo-yu">YU</span></div>
            <div class="emblem-subtitle">SOLUTIONS</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Who We Are Section -->
  <section id="identity">
    <div class="site-wrapper">
      <div class="identity-panel">
        <div class="identity-copy">
          <div class="eyebrow">Who We Are</div>
          <h3>Channeling the Elemental Force of Wind into Digital Architecture</h3>
          <p>In Sanskrit, <strong>Vayu</strong> signifies the fundamental elemental force of wind—limitless, swift, omnipresent, and vital for life.</p>
          <p>At <strong>VaYu Solutions</strong>, we channel this exact spirit into technology: delivering rapid, fluid, and robust digital systems that liberate companies from operational drag.</p>
        </div>

        <div class="metrics-grid">
          <div class="metric-box">
            <strong>100%</strong>
            <span>Custom-Engineered Architecture</span>
          </div>
          <div class="metric-box">
            <strong>100%</strong>
            <span>Pricing & Timeline Transparency</span>
          </div>
          <div class="metric-box">
            <strong>Zero</strong>
            <span>Generic Templates or Shortcuts</span>
          </div>
          <div class="metric-box">
            <strong>Dedicated</strong>
            <span>Startup & Enterprise Partner</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Founder Message Section -->
  <div class="founder-section" id="founder">
    <div class="site-wrapper">
      <div class="founder-card">
        <div class="founder-avatar-wrap">
          <div class="founder-badge-icon">SS</div>
          <div class="founder-name">Saloni Srivastava</div>
          <div class="founder-title">Founder, VaYu Solutions</div>
        </div>
        <div class="founder-message-content">
          <div class="eyebrow" style="margin-bottom: 0.75rem;">Leadership Message</div>
          <h3>Building Without Compromise</h3>
          <blockquote>"At VaYu Solutions, we founded this agency with a singular belief: true business growth requires zero shortcuts. When we combine high-performance custom web and mobile development with aggressive SEO and precision marketing strategies, we aren’t just writing code—we are building engines for scale. My personal commitment is that every single project we deliver remains custom-crafted, 100% transparent, and relentlessly focused on your ROI."</blockquote>
          <div class="founder-signoff">— Saloni Srivastava, Founder</div>
        </div>
      </div>
    </div>
  </div>

  <!-- Core Services Section -->
  <section id="capabilities">
    <div class="site-wrapper">
      <div class="section-head">
        <div class="eyebrow">Core Capabilities</div>
        <h2>End-to-End Digital Engineering & Growth</h2>
        <p>We build high-impact digital solutions designed to elevate your visibility, attract qualified leads, and accelerate business growth.</p>
      </div>

      <div class="services-grid">
        <div class="service-item">
          <div class="icon-box">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="3" width="20" height="14" rx="2"/><path d="M8 21h8M12 17v4M7 8l-3 2 3 2M17 8l3 2-3 2M13 7l-2 6"/></svg>
          </div>
          <h3>Custom Web Platforms</h3>
          <p>Bespoke, high-velocity web applications and enterprise portals engineered from the ground up for scalability, security, and conversion.</p>
        </div>

        <div class="service-item">
          <div class="icon-box">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="5" y="2" width="14" height="20" rx="2"/><path d="M12 18h.01"/></svg>
          </div>
          <h3>Mobile App Ecosystems</h3>
          <p>Fluid, native-grade iOS and Android applications built with resilient backend infrastructure to streamline customer and internal workflows.</p>
        </div>

        <div class="service-item">
          <div class="icon-box">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M3 3v18h18"/><path d="M18 9l-5 5-4-4-3 3"/></svg>
          </div>
          <h3>Technical SEO & Visibility</h3>
          <p>Search architecture optimization, semantic content strategy, and authority building to secure sustainable top-tier organic rankings.</p>
        </div>

        <div class="service-item">
          <div class="icon-box">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><circle cx="12" cy="12" r="6"/><circle cx="12" cy="12" r="2"/></svg>
          </div>
          <h3>Performance Ads & Marketing</h3>
          <p>Precision-targeted paid acquisition campaigns and creative brand strategies engineered to attract qualified leads and maximize return on ad spend.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Why VaYu Solutions Section -->
  <section id="why-vayu">
    <div class="site-wrapper">
      <div class="why-panel">
        <div class="eyebrow">Why VaYu Solutions</div>
        <h3>No Templates. No Shortcuts. Pure Engineering.</h3>
        <p>At VaYu Solutions, every project is custom-built for your business. From day one, we guarantee 100% transparency in pricing, timelines, and deliverables.</p>
        
        <div class="pillar-grid">
          <div class="pillar-card">
            <h4>Custom Architecture</h4>
            <p>Solutions tailored strictly to your operational logic, workflows, and business growth goals.</p>
          </div>
          <div class="pillar-card">
            <h4>Radical Transparency</h4>
            <p>Clear milestone schedules, itemized scopes, and zero unannounced fees from day one.</p>
          </div>
          <div class="pillar-card">
            <h4>Unified Strategy</h4>
            <p>Seamless alignment between advanced technical engineering and market-facing creative growth.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="inquire">
    <div class="site-wrapper">
      <div class="contact-banner">
        <div class="contact-pitch">
          <div class="eyebrow">Partner With Us</div>
          <h2>Start Your Project with VaYu</h2>
          <p>Connect directly with our engineering and strategy team in Patna to discuss your technical roadmap, timelines, and growth objectives.</p>
          <a href="mailto:info.vayusolutions@gmail.com" class="btn-solid">
            Request Project Proposal
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
          </a>
        </div>

        <div class="contact-channels">
          <a href="tel:+919470011490" class="channel-card">
            <div class="channel-icon">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
            </div>
            <div class="channel-meta">
              <small>Direct Phone / WhatsApp</small>
              <strong>+91 94700 11490</strong>
            </div>
          </a>

          <a href="mailto:info.vayusolutions@gmail.com" class="channel-card">
            <div class="channel-icon">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
            </div>
            <div class="channel-meta">
              <small>Official Email</small>
              <strong>info.vayusolutions@gmail.com</strong>
            </div>
          </a>

          <div class="channel-card">
            <div class="channel-icon">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
            </div>
            <div class="channel-meta">
              <small>Headquarters</small>
              <strong>Patna, Bihar, India</strong>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Social Media Strip -->
  <div class="social-section">
    <div class="site-wrapper">
      <div class="social-strip">
        <a href="https://instagram.com/vayusolutions.in" target="_blank" class="social-pill">
          <svg viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
          <span>Instagram: @vayusolutions.in</span>
        </a>

        <a href="https://facebook.com/vayusolutions" target="_blank" class="social-pill">
          <svg viewBox="0 0 24 24"><path d="M9 8H6v4h3v12h5V12h3.642L18 8h-4V6.333C14 5.375 14.5 5 15.5 5H18V0h-3.808C10.589 0 9 1.582 9 4.75V8z"/></svg>
          <span>Facebook: @vayusolutions</span>
        </a>

        <a href="https://youtube.com/@vayusolutions" target="_blank" class="social-pill">
          <svg viewBox="0 0 24 24"><path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/></svg>
          <span>YouTube: @vayusolutions</span>
        </a>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer>
    <div class="site-wrapper">
      <p>&copy; 2026 VaYu Solutions — Where Technology Meets Creativity. All rights reserved. | Patna, Bihar</p>
    </div>
  </footer>
</body>
</html>
