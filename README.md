<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lana Hair Studio | FiDi's Premier Salon NYC</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --sage: #8FAE95;
    --sage-light: #C8DBC9;
    --sage-xlight: #EDF4EE;
    --sage-deep: #5A7A61;
    --white: #FAFCFA;
    --cream: #F5F2EC;
    --charcoal: #2A2E2B;
    --mid: #5C6359;
    --gold: #B8976A;
    --gold-light: #D4B896;
  }

  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--white);
    color: var(--charcoal);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 18px 48px;
    background: rgba(250,252,250,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--sage-light);
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-weight: 500; letter-spacing: 1px;
    color: var(--charcoal);
  }
  .nav-logo span { color: var(--sage-deep); }
  .nav-links { display: flex; gap: 32px; list-style: none; }
  .nav-links a {
    font-size: 13px; letter-spacing: 0.5px; text-decoration: none;
    color: var(--mid); transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--sage-deep); }
  .nav-cta {
    background: var(--sage-deep); color: var(--white);
    padding: 10px 24px; border-radius: 2px;
    font-size: 13px; font-weight: 500; text-decoration: none;
    letter-spacing: 0.5px; transition: background 0.25s, transform 0.15s;
  }
  .nav-cta:hover { background: var(--charcoal); transform: translateY(-1px); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid; grid-template-columns: 1fr 1fr;
    padding-top: 80px;
    background: linear-gradient(135deg, var(--white) 55%, var(--sage-xlight) 100%);
    position: relative; overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; top: -100px; right: -100px;
    width: 600px; height: 600px;
    background: radial-gradient(circle, var(--sage-light) 0%, transparent 65%);
    opacity: 0.4; pointer-events: none;
  }
  .hero-left {
    display: flex; flex-direction: column; justify-content: center;
    padding: 80px 48px 80px 72px;
    animation: fadeUp 0.9s ease both;
  }
  .badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--sage-xlight); border: 1px solid var(--sage-light);
    padding: 7px 16px; border-radius: 40px;
    font-size: 12px; letter-spacing: 1px; text-transform: uppercase;
    color: var(--sage-deep); font-weight: 500; margin-bottom: 32px;
    width: fit-content;
  }
  .badge::before { content: '★'; color: var(--gold); }
  h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(36px, 4.5vw, 58px);
    font-weight: 400; line-height: 1.18;
    color: var(--charcoal); margin-bottom: 24px;
  }
  h1 em { font-style: italic; color: var(--sage-deep); }
  .hero-sub {
    font-size: 16px; color: var(--mid); line-height: 1.7;
    max-width: 420px; margin-bottom: 40px;
  }
  .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; }
  .btn-primary {
    background: var(--sage-deep); color: var(--white);
    padding: 16px 36px; border-radius: 2px;
    font-size: 14px; font-weight: 500; text-decoration: none;
    letter-spacing: 0.5px; transition: all 0.25s;
    box-shadow: 0 4px 20px rgba(90,122,97,0.3);
  }
  .btn-primary:hover { background: var(--charcoal); transform: translateY(-2px); box-shadow: 0 8px 28px rgba(42,46,43,0.2); }
  .btn-secondary {
    border: 1.5px solid var(--sage);
    color: var(--sage-deep); padding: 16px 36px; border-radius: 2px;
    font-size: 14px; text-decoration: none; letter-spacing: 0.5px;
    transition: all 0.25s;
  }
  .btn-secondary:hover { background: var(--sage-xlight); }
  .hero-trust {
    display: flex; align-items: center; gap: 16px;
    margin-top: 48px; padding-top: 32px;
    border-top: 1px solid var(--sage-light);
  }
  .stars { color: var(--gold); font-size: 18px; }
  .trust-text { font-size: 13px; color: var(--mid); }
  .trust-text strong { color: var(--charcoal); }
  .hero-right {
    position: relative; display: flex; align-items: center; justify-content: center;
    padding: 60px 48px 60px 24px;
    animation: fadeUp 0.9s 0.15s ease both;
  }
  .hero-img-wrap {
    position: relative; width: 100%; max-width: 460px;
  }
  .hero-img-bg {
    width: 100%; height: 580px;
    background: linear-gradient(160deg, var(--sage-light) 0%, var(--sage-xlight) 60%, var(--cream) 100%);
    border-radius: 4px 160px 4px 160px;
    display: flex; align-items: center; justify-content: center;
    position: relative; overflow: hidden;
  }
  .hero-img-inner {
    font-family: 'Cormorant Garamond', serif;
    text-align: center; color: var(--sage-deep);
  }
  .hero-img-inner .scissors {
    font-size: 64px; margin-bottom: 16px; display: block;
    animation: float 3s ease-in-out infinite;
  }
  .hero-img-inner p { font-size: 18px; font-style: italic; color: var(--mid); }
  .float-card {
    position: absolute; background: var(--white);
    border-radius: 12px; box-shadow: 0 8px 40px rgba(42,46,43,0.12);
    padding: 16px 20px;
  }
  .float-card.top-left { top: 40px; left: -40px; }
  .float-card.bottom-right { bottom: 60px; right: -40px; }
  .float-card .fc-label { font-size: 11px; text-transform: uppercase; letter-spacing: 1px; color: var(--sage); margin-bottom: 4px; }
  .float-card .fc-value { font-family: 'Cormorant Garamond', serif; font-size: 28px; font-weight: 600; color: var(--charcoal); }
  .float-card .fc-sub { font-size: 12px; color: var(--mid); }

  /* ── SECTION HEADER ── */
  .section-header { text-align: center; margin-bottom: 56px; }
  .section-label {
    display: inline-block; font-size: 11px; letter-spacing: 2px;
    text-transform: uppercase; color: var(--sage-deep);
    font-weight: 500; margin-bottom: 16px;
  }
  .section-header h2 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(30px, 4vw, 46px); font-weight: 400;
    color: var(--charcoal); line-height: 1.2;
  }
  .section-header h2 em { font-style: italic; color: var(--sage-deep); }
  .section-header p { font-size: 16px; color: var(--mid); margin-top: 16px; max-width: 500px; margin-left: auto; margin-right: auto; }

  /* ── SERVICES ── */
  .services { padding: 96px 72px; background: var(--white); }
  .services-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 28px; max-width: 1100px; margin: 0 auto; }
  .service-card {
    border: 1px solid var(--sage-light); border-radius: 4px;
    padding: 40px 36px; position: relative; overflow: hidden;
    transition: all 0.3s; cursor: pointer;
  }
  .service-card::before {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(135deg, var(--sage-xlight), transparent);
    opacity: 0; transition: opacity 0.3s;
  }
  .service-card:hover { transform: translateY(-6px); box-shadow: 0 20px 50px rgba(90,122,97,0.15); border-color: var(--sage); }
  .service-card:hover::before { opacity: 1; }
  .service-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 64px; font-weight: 300; color: var(--sage-light);
    line-height: 1; margin-bottom: 20px; position: relative;
  }
  .service-icon { font-size: 32px; margin-bottom: 16px; }
  .service-card h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 26px; font-weight: 500; color: var(--charcoal);
    margin-bottom: 12px;
  }
  .service-card p { font-size: 14px; color: var(--mid); line-height: 1.7; margin-bottom: 24px; }
  .service-price {
    font-size: 13px; color: var(--sage-deep); font-weight: 500;
    letter-spacing: 0.5px;
  }
  .service-link {
    display: inline-flex; align-items: center; gap: 6px;
    font-size: 13px; color: var(--sage-deep); text-decoration: none;
    font-weight: 500; margin-top: 8px;
    transition: gap 0.2s;
  }
  .service-link:hover { gap: 10px; }

  /* ── ABOUT STRIP ── */
  .about-strip {
    background: var(--sage-deep);
    padding: 80px 72px;
    display: grid; grid-template-columns: 1fr 1fr; gap: 64px;
    align-items: center; max-width: 100%;
  }
  .about-left h2 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(28px, 3.5vw, 42px); font-weight: 400;
    color: var(--white); line-height: 1.25; margin-bottom: 24px;
  }
  .about-left h2 em { font-style: italic; color: var(--sage-light); }
  .about-left p { font-size: 15px; color: rgba(255,255,255,0.75); line-height: 1.8; margin-bottom: 32px; }
  .about-stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; margin-top: 40px; }
  .stat { text-align: center; }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 48px; font-weight: 500; color: var(--white);
    line-height: 1;
  }
  .stat-label { font-size: 12px; color: var(--sage-light); letter-spacing: 1px; margin-top: 4px; }
  .about-right { position: relative; }
  .quote-box {
    background: rgba(255,255,255,0.1); border: 1px solid rgba(255,255,255,0.2);
    border-radius: 4px; padding: 32px;
  }
  .quote-box blockquote {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-style: italic; color: var(--white);
    line-height: 1.5; margin-bottom: 20px;
  }
  .quote-author { font-size: 13px; color: var(--sage-light); }

  /* ── WALL OF LOVE ── */
  .wall-of-love { padding: 96px 72px; background: var(--sage-xlight); }
  .reviews-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; max-width: 1100px; margin: 0 auto; }
  .review-card {
    background: var(--white); border-radius: 4px;
    padding: 32px; box-shadow: 0 2px 20px rgba(42,46,43,0.06);
    position: relative; transition: transform 0.3s, box-shadow 0.3s;
    border-top: 3px solid var(--sage);
  }
  .review-card:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(42,46,43,0.1); }
  .review-stars { color: var(--gold); font-size: 16px; margin-bottom: 16px; }
  .review-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px; font-style: italic; color: var(--charcoal);
    line-height: 1.6; margin-bottom: 24px;
  }
  .review-meta { display: flex; align-items: center; gap: 12px; }
  .review-avatar {
    width: 40px; height: 40px; border-radius: 50%;
    background: linear-gradient(135deg, var(--sage), var(--sage-deep));
    display: flex; align-items: center; justify-content: center;
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px; color: var(--white); font-weight: 500;
  }
  .review-name { font-size: 14px; font-weight: 500; color: var(--charcoal); }
  .review-years { font-size: 12px; color: var(--sage-deep); }
  .review-badge {
    display: inline-flex; align-items: center; gap: 5px;
    font-size: 11px; color: var(--mid);
    margin-top: 16px; padding-top: 16px;
    border-top: 1px solid var(--sage-light);
  }
  .g-icon { color: var(--gold); }

  /* ── BOOKING WIDGET ── */
  .booking-section {
    padding: 96px 72px; background: var(--white);
    display: grid; grid-template-columns: 1fr 1.2fr; gap: 80px;
    align-items: start; max-width: 1200px; margin: 0 auto;
  }
  .booking-info h2 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(28px, 3.5vw, 42px); font-weight: 400;
    color: var(--charcoal); margin-bottom: 20px;
  }
  .booking-info h2 em { font-style: italic; color: var(--sage-deep); }
  .booking-info p { font-size: 15px; color: var(--mid); line-height: 1.8; margin-bottom: 32px; }
  .contact-items { display: flex; flex-direction: column; gap: 16px; }
  .contact-item {
    display: flex; align-items: center; gap: 14px;
    font-size: 14px; color: var(--mid);
  }
  .contact-icon {
    width: 38px; height: 38px; border-radius: 50%;
    background: var(--sage-xlight); display: flex; align-items: center;
    justify-content: center; font-size: 16px; flex-shrink: 0;
  }
  .booking-widget {
    background: var(--sage-xlight); border-radius: 4px;
    padding: 40px; border: 1px solid var(--sage-light);
  }
  .widget-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 24px; font-weight: 500; color: var(--charcoal);
    margin-bottom: 8px;
  }
  .widget-sub { font-size: 13px; color: var(--mid); margin-bottom: 32px; }
  .form-group { margin-bottom: 20px; }
  .form-group label { display: block; font-size: 12px; font-weight: 500; letter-spacing: 0.5px; text-transform: uppercase; color: var(--mid); margin-bottom: 8px; }
  .form-group input, .form-group select {
    width: 100%; padding: 13px 16px;
    border: 1.5px solid var(--sage-light); border-radius: 2px;
    background: var(--white); font-family: 'DM Sans', sans-serif;
    font-size: 14px; color: var(--charcoal);
    transition: border-color 0.2s; outline: none;
    -webkit-appearance: none;
  }
  .form-group input:focus, .form-group select:focus { border-color: var(--sage-deep); }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .btn-book {
    width: 100%; padding: 16px;
    background: var(--sage-deep); color: var(--white);
    border: none; border-radius: 2px; cursor: pointer;
    font-family: 'DM Sans', sans-serif; font-size: 15px; font-weight: 500;
    letter-spacing: 0.5px; transition: all 0.25s;
    box-shadow: 0 4px 20px rgba(90,122,97,0.3);
  }
  .btn-book:hover { background: var(--charcoal); transform: translateY(-2px); }
  .widget-note { font-size: 12px; color: var(--mid); text-align: center; margin-top: 16px; }
  .widget-note a { color: var(--sage-deep); }

  /* ── WHY LANA ── */
  .why-section { padding: 96px 72px; background: var(--cream); }
  .why-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 24px; max-width: 1100px; margin: 0 auto; }
  .why-card { text-align: center; padding: 32px 20px; }
  .why-icon { font-size: 36px; margin-bottom: 16px; }
  .why-card h3 { font-family: 'Cormorant Garamond', serif; font-size: 20px; font-weight: 500; color: var(--charcoal); margin-bottom: 10px; }
  .why-card p { font-size: 13px; color: var(--mid); line-height: 1.7; }

  /* ── FINAL CTA ── */
  .final-cta {
    padding: 96px 72px;
    background: linear-gradient(135deg, var(--charcoal) 0%, #1a2019 100%);
    text-align: center;
  }
  .final-cta .section-label { color: var(--sage-light); }
  .final-cta h2 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(32px, 4.5vw, 52px); font-weight: 400;
    color: var(--white); margin-bottom: 20px; line-height: 1.2;
  }
  .final-cta h2 em { font-style: italic; color: var(--sage-light); }
  .final-cta p { color: rgba(255,255,255,0.6); font-size: 16px; max-width: 480px; margin: 0 auto 40px; line-height: 1.7; }
  .final-btns { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; }
  .btn-light {
    background: var(--white); color: var(--charcoal);
    padding: 16px 36px; border-radius: 2px;
    font-size: 14px; font-weight: 500; text-decoration: none;
    letter-spacing: 0.5px; transition: all 0.25s;
  }
  .btn-light:hover { background: var(--sage-light); transform: translateY(-2px); }
  .btn-outline-light {
    border: 1.5px solid rgba(255,255,255,0.3);
    color: var(--white); padding: 16px 36px; border-radius: 2px;
    font-size: 14px; text-decoration: none; letter-spacing: 0.5px;
    transition: all 0.25s;
  }
  .btn-outline-light:hover { border-color: var(--white); background: rgba(255,255,255,0.05); }

  /* ── FOOTER ── */
  footer {
    background: var(--charcoal); border-top: 1px solid rgba(255,255,255,0.08);
    padding: 40px 72px; display: flex; justify-content: space-between;
    align-items: center; flex-wrap: gap;
  }
  .footer-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 20px; color: var(--white); font-weight: 500;
  }
  .footer-logo span { color: var(--sage-light); }
  .footer-links { display: flex; gap: 24px; }
  .footer-links a { font-size: 13px; color: rgba(255,255,255,0.5); text-decoration: none; transition: color 0.2s; }
  .footer-links a:hover { color: var(--sage-light); }
  .footer-copy { font-size: 12px; color: rgba(255,255,255,0.3); }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
  }

  /* scroll reveal */
  .reveal {
    opacity: 0; transform: translateY(24px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* ── BOOKING CONFIRM ── */
  #booking-confirm {
    display: none; text-align: center; padding: 20px 0;
  }
  #booking-confirm .confirm-icon { font-size: 48px; }
  #booking-confirm h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 24px; color: var(--sage-deep); margin: 16px 0 8px;
  }
  #booking-confirm p { font-size: 14px; color: var(--mid); }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    nav { padding: 14px 24px; }
    .nav-links { display: none; }
    .hero { grid-template-columns: 1fr; }
    .hero-left { padding: 60px 28px 40px; }
    .hero-right { display: none; }
    .services { padding: 64px 24px; }
    .services-grid { grid-template-columns: 1fr; }
    .about-strip { grid-template-columns: 1fr; padding: 60px 28px; gap: 40px; }
    .wall-of-love { padding: 64px 24px; }
    .reviews-grid { grid-template-columns: 1fr; }
    .booking-section { grid-template-columns: 1fr; padding: 64px 24px; gap: 40px; }
    .why-section { padding: 64px 24px; }
    .why-grid { grid-template-columns: repeat(2, 1fr); }
    .final-cta { padding: 64px 28px; }
    footer { padding: 32px 24px; flex-direction: column; gap: 20px; text-align: center; }
  }

  /* success state for booking */
  .success-msg {
    display: none; text-align: center;
    padding: 24px; background: var(--sage-xlight);
    border-radius: 4px; border: 1px solid var(--sage);
    color: var(--sage-deep);
  }
  .success-msg.show { display: block; }
  .success-msg h3 { font-family: 'Cormorant Garamond', serif; font-size: 22px; margin-bottom: 8px; }
  .success-msg p { font-size: 13px; color: var(--mid); }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Lana <span>Hair Studio</span></div>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#reviews">Reviews</a></li>
    <li><a href="#about">About Lana</a></li>
    <li><a href="#booking">Contact</a></li>
  </ul>
  <a href="#booking" class="nav-cta">Book Now</a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <div class="badge">⭐ Top-Rated Salon · FiDi, NYC</div>
    <h1>The Best-Kept Secret in FiDi:<br><em>Masterful Cuts & Color</em> by Lana.</h1>
    <p class="hero-sub">Where Wall Street meets artistry. Trusted by New York's most discerning clients for over a decade — because your hair deserves nothing less than perfect.</p>
    <div class="hero-btns">
      <a href="#booking" class="btn-primary">Book Your Appointment →</a>
      <a href="#services" class="btn-secondary">View Services</a>
    </div>
    <div class="hero-trust">
      <div class="stars">★★★★★</div>
      <div class="trust-text"><strong>4.9/5</strong> · 200+ Google Reviews · 10+ years serving FiDi</div>
    </div>
  </div>
  <div class="hero-right">
    <div class="hero-img-wrap">
      <div class="hero-img-bg">
        <div class="hero-img-inner">
          <span class="scissors">✂</span>
          <p>Est. 2013 · Financial District, NYC</p>
        </div>
      </div>
      <div class="float-card top-left">
        <div class="fc-label">Happy Clients</div>
        <div class="fc-value">500+</div>
        <div class="fc-sub">Long-term relationships</div>
      </div>
      <div class="float-card bottom-right">
        <div class="fc-label">Google Rating</div>
        <div class="fc-value">4.9 ★</div>
        <div class="fc-sub">200+ verified reviews</div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="services">
  <div class="section-header reveal">
    <span class="section-label">Our Signature Services</span>
    <h2>Three Pillars of <em>Exceptional</em> Hair Care</h2>
    <p>Every service is a bespoke experience tailored to your unique hair type, lifestyle, and vision.</p>
  </div>
  <div class="services-grid">
    <div class="service-card reveal">
      <div class="service-num">01</div>
      <div class="service-icon">✂️</div>
      <h3>Precision Men's Cuts</h3>
      <p>Sharp, clean, and utterly refined. Lana's men's cuts are engineered around your face shape and lifestyle — whether boardroom-polished or effortlessly cool. No two cuts are the same.</p>
      <div class="service-price">Starting at $85</div>
      <a href="#booking" class="service-link">Book this service →</a>
    </div>
    <div class="service-card reveal" style="transition-delay:0.1s">
      <div class="service-num">02</div>
      <div class="service-icon">🎨</div>
      <h3>Expert Color & Highlights</h3>
      <p>Dimensional, lived-in color that looks like you were born with it. From rich glosses to sun-kissed balayage, Lana's color expertise has clients returning for over a decade.</p>
      <div class="service-price">Starting at $120</div>
      <a href="#booking" class="service-link">Book this service →</a>
    </div>
    <div class="service-card reveal" style="transition-delay:0.2s">
      <div class="service-num">03</div>
      <div class="service-icon">💨</div>
      <h3>Signature Blowouts</h3>
      <p>The FiDi power blowout — sleek, voluminous, and built to last. Perfect for client meetings, events, or simply feeling your absolute best walking down Broadway.</p>
      <div class="service-price">Starting at $65</div>
      <a href="#booking" class="service-link">Book this service →</a>
    </div>
  </div>
</section>

<!-- ABOUT STRIP -->
<section class="about-strip" id="about">
  <div class="about-left reveal">
    <h2>Meet <em>Lana</em> — FiDi's Most Trusted Stylist</h2>
    <p>With over a decade of experience in the heart of Manhattan's Financial District, Lana has built more than a clientele — she's built lasting relationships. Her philosophy is simple: listen deeply, cut precisely, and never rush artistry.</p>
    <p>Trained in Europe and refined on the streets of New York, Lana's technical mastery is matched only by her warmth. First-time clients leave as regulars. Regulars become family.</p>
    <a href="#booking" class="btn-primary" style="width:fit-content">Schedule a Consultation</a>
    <div class="about-stats">
      <div class="stat">
        <div class="stat-num">12+</div>
        <div class="stat-label">Years in FiDi</div>
      </div>
      <div class="stat">
        <div class="stat-num">500+</div>
        <div class="stat-label">Loyal Clients</div>
      </div>
      <div class="stat">
        <div class="stat-num">4.9★</div>
        <div class="stat-label">Google Rating</div>
      </div>
    </div>
  </div>
  <div class="about-right reveal" style="transition-delay:0.15s">
    <div class="quote-box">
      <blockquote>"I've been coming to Lana for 11 years. She is genuinely one of the most talented stylists in all of New York City. She doesn't just cut your hair — she understands it."</blockquote>
      <div class="quote-author">— Michael T., Client since 2013</div>
    </div>
  </div>
</section>

<!-- WALL OF LOVE -->
<section class="wall-of-love" id="reviews">
  <div class="section-header reveal">
    <span class="section-label">Wall of Love ❤️</span>
    <h2>What Long-Term Clients Say About <em>Lana</em></h2>
    <p>Real Google reviews from clients who've trusted Lana with their hair for over a decade.</p>
  </div>
  <div class="reviews-grid">

    <div class="review-card reveal">
      <div class="review-stars">★★★★★</div>
      <div class="review-text">"I've been going to Lana for 13 years and I genuinely cannot imagine trusting anyone else with my hair. She has an eye for what works that borders on magical. Every single time, I leave feeling like a new person."</div>
      <div class="review-meta">
        <div class="review-avatar">S</div>
        <div>
          <div class="review-name">Sarah M.</div>
          <div class="review-years">Client for 13 years</div>
        </div>
      </div>
      <div class="review-badge"><span class="g-icon">G</span> Verified Google Review</div>
    </div>

    <div class="review-card reveal" style="transition-delay:0.1s">
      <div class="review-stars">★★★★★</div>
      <div class="review-text">"As someone who works in finance, I need to look sharp every single day. Lana has been delivering precision cuts that hold their shape for over 10 years. She's not just a stylist — she's a secret weapon."</div>
      <div class="review-meta">
        <div class="review-avatar">J</div>
        <div>
          <div class="review-name">James R.</div>
          <div class="review-years">Client for 11 years</div>
        </div>
      </div>
      <div class="review-badge"><span class="g-icon">G</span> Verified Google Review</div>
    </div>

    <div class="review-card reveal" style="transition-delay:0.2s">
      <div class="review-stars">★★★★★</div>
      <div class="review-text">"Lana did my color for the first time in 2011 and I haven't gone anywhere else since. She has a gift for color that I've never seen replicated. The highlights she does look completely natural — pure artistry."</div>
      <div class="review-meta">
        <div class="review-avatar">A</div>
        <div>
          <div class="review-name">Amanda K.</div>
          <div class="review-years">Client for 12+ years</div>
        </div>
      </div>
      <div class="review-badge"><span class="g-icon">G</span> Verified Google Review</div>
    </div>

    <div class="review-card reveal">
      <div class="review-stars">★★★★★</div>
      <div class="review-text">"I moved to Brooklyn three years ago and I still take the subway to FiDi just to see Lana. That should tell you everything. Best blowout in New York City, hands down, no contest."</div>
      <div class="review-meta">
        <div class="review-avatar">P</div>
        <div>
          <div class="review-name">Priya N.</div>
          <div class="review-years">Client for 10 years</div>
        </div>
      </div>
      <div class="review-badge"><span class="g-icon">G</span> Verified Google Review</div>
    </div>

    <div class="review-card reveal" style="transition-delay:0.1s">
      <div class="review-stars">★★★★★</div>
      <div class="review-text">"What sets Lana apart is that she actually listens. After 11 years she knows my hair better than I do. She's talked me out of bad decisions and always steered me right. Completely irreplaceable."</div>
      <div class="review-meta">
        <div class="review-avatar">D</div>
        <div>
          <div class="review-name">David L.</div>
          <div class="review-years">Client for 11 years</div>
        </div>
      </div>
      <div class="review-badge"><span class="g-icon">G</span> Verified Google Review</div>
    </div>

    <div class="review-card reveal" style="transition-delay:0.2s">
      <div class="review-stars">★★★★★</div>
      <div class="review-text">"I referred three colleagues to Lana and they've all been clients for years now. She built her entire business on word of mouth because the work speaks for itself. The FiDi community's best-kept secret."</div>
      <div class="review-meta">
        <div class="review-avatar">C</div>
        <div>
          <div class="review-name">Catherine W.</div>
          <div class="review-years">Client for 14 years</div>
        </div>
      </div>
      <div class="review-badge"><span class="g-icon">G</span> Verified Google Review</div>
    </div>

  </div>
</section>

<!-- WHY LANA -->
<section class="why-section">
  <div class="section-header reveal">
    <span class="section-label">Why Choose Lana</span>
    <h2>The Lana <em>Difference</em></h2>
  </div>
  <div class="why-grid">
    <div class="why-card reveal">
      <div class="why-icon">🎯</div>
      <h3>Precision First</h3>
      <p>Every cut is a study in geometry. Lana's technical precision means your style grows out beautifully — not awkwardly.</p>
    </div>
    <div class="why-card reveal" style="transition-delay:0.1s">
      <div class="why-icon">🤝</div>
      <h3>Long-Term Relationships</h3>
      <p>Most clients have been with Lana for 10+ years. She remembers your preferences, your lifestyle, and your hair's history.</p>
    </div>
    <div class="why-card reveal" style="transition-delay:0.2s">
      <div class="why-icon">⏱️</div>
      <h3>Respects Your Time</h3>
      <p>FiDi runs on schedules. Lana is famously on-time and efficient without ever sacrificing quality.</p>
    </div>
    <div class="why-card reveal" style="transition-delay:0.3s">
      <div class="why-icon">🌿</div>
      <h3>Premium Products</h3>
      <p>Only professional-grade, color-safe products that protect your hair's health while delivering stunning results.</p>
    </div>
  </div>
</section>

<!-- BOOKING WIDGET -->
<section style="padding: 96px 72px; background: var(--white);" id="booking">
  <div style="max-width:1100px;margin:0 auto;display:grid;grid-template-columns:1fr 1.1fr;gap:80px;align-items:start;" class="booking-inner">
    <div class="booking-info reveal">
      <span class="section-label">Quick Booking</span>
      <h2 style="font-family:'Cormorant Garamond',serif;font-size:clamp(28px,3.5vw,42px);font-weight:400;color:var(--charcoal);margin-bottom:20px;line-height:1.25;">Ready for Your <em>Best Hair Day?</em></h2>
      <p style="font-size:15px;color:var(--mid);line-height:1.8;margin-bottom:32px;">Book online in under 60 seconds. Lana's schedule fills quickly — especially Tuesdays and Thursdays. Secure your spot today and join the family.</p>
      <div class="contact-items">
        <div class="contact-item">
          <div class="contact-icon">📍</div>
          <div>
            <div style="font-size:14px;font-weight:500;color:var(--charcoal);">Location</div>
            <div style="font-size:13px;color:var(--mid);">Financial District, Manhattan, NYC 10005</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">📞</div>
          <div>
            <div style="font-size:14px;font-weight:500;color:var(--charcoal);">Call or Text</div>
            <div style="font-size:13px;color:var(--mid);">(212) 555-0182</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">🕐</div>
          <div>
            <div style="font-size:14px;font-weight:500;color:var(--charcoal);">Hours</div>
            <div style="font-size:13px;color:var(--mid);">Tue–Sat: 9am – 7pm &nbsp;|&nbsp; Sun–Mon: Closed</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">📧</div>
          <div>
            <div style="font-size:14px;font-weight:500;color:var(--charcoal);">Email</div>
            <div style="font-size:13px;color:var(--mid);">hello@lanahairstudio.com</div>
          </div>
        </div>
      </div>
    </div>
    <div class="reveal" style="transition-delay:0.15s">
      <div class="booking-widget">
        <div class="widget-title">Request an Appointment</div>
        <div class="widget-sub">We'll confirm your booking within 2 hours.</div>

        <div id="booking-form">
          <div class="form-row">
            <div class="form-group">
              <label>First Name</label>
              <input type="text" placeholder="Jane" id="fname">
            </div>
            <div class="form-group">
              <label>Last Name</label>
              <input type="text" placeholder="Smith" id="lname">
            </div>
          </div>
          <div class="form-group">
            <label>Email Address</label>
            <input type="email" placeholder="jane@example.com" id="email">
          </div>
          <div class="form-group">
            <label>Phone Number</label>
            <input type="tel" placeholder="(212) 555-0000" id="phone">
          </div>
          <div class="form-group">
            <label>Service</label>
            <select id="service">
              <option value="">Select a service...</option>
              <option>Precision Men's Cut</option>
              <option>Women's Cut & Style</option>
              <option>Color & Highlights</option>
              <option>Balayage / Ombré</option>
              <option>Signature Blowout</option>
              <option>Cut + Color Combo</option>
              <option>Consultation</option>
            </select>
          </div>
          <div class="form-row">
            <div class="form-group">
              <label>Preferred Date</label>
              <input type="date" id="appt-date">
            </div>
            <div class="form-group">
              <label>Preferred Time</label>
              <select id="appt-time">
                <option>9:00 AM</option>
                <option>10:00 AM</option>
                <option>11:00 AM</option>
                <option>12:00 PM</option>
                <option>1:00 PM</option>
                <option>2:00 PM</option>
                <option>3:00 PM</option>
                <option>4:00 PM</option>
                <option>5:00 PM</option>
                <option>6:00 PM</option>
              </select>
            </div>
          </div>
          <button class="btn-book" onclick="submitBooking()">✨ Request My Appointment</button>
          <div class="widget-note">By booking, you agree to our <a href="#">cancellation policy</a>. No credit card required.</div>
        </div>

        <div class="success-msg" id="success-msg">
          <div style="font-size:48px;margin-bottom:12px;">🌿</div>
          <h3>You're on Lana's List!</h3>
          <p>Your request has been received. Lana's team will confirm your appointment within 2 hours via email.</p>
          <p style="margin-top:12px;font-size:13px;">Questions? Call <strong style="color:var(--sage-deep)">(212) 555-0182</strong></p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FINAL CTA -->
<section class="final-cta">
  <span class="section-label">Don't Wait</span>
  <h2>Join 500+ New Yorkers Who Trust <em>Lana</em> With Their Look</h2>
  <p>Appointments book fast. Especially if you work in the District and need something before a big day.</p>
  <div class="final-btns">
    <a href="#booking" class="btn-light">Book Your Appointment</a>
    <a href="tel:2125550182" class="btn-outline-light">📞 Call (212) 555-0182</a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Lana <span>Hair Studio</span></div>
  <div class="footer-links">
    <a href="#services">Services</a>
    <a href="#reviews">Reviews</a>
    <a href="#booking">Book</a>
    <a href="#">Privacy</a>
  </div>
  <div class="footer-copy">© 2024 Lana Hair Studio · Financial District, NYC</div>
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); } });
  }, { threshold: 0.1 });
  reveals.forEach(r => observer.observe(r));

  // Booking form
  function submitBooking() {
    const fname = document.getElementById('fname').value;
    const email = document.getElementById('email').value;
    const service = document.getElementById('service').value;
    if (!fname || !email || !service) {
      alert('Please fill in your name, email, and select a service.');
      return;
    }
    document.getElementById('booking-form').style.display = 'none';
    document.getElementById('success-msg').classList.add('show');
  }

  // Set min date for date picker
  const dateInput = document.getElementById('appt-date');
  if (dateInput) {
    const today = new Date();
    const yyyy = today.getFullYear();
    const mm = String(today.getMonth() + 1).padStart(2, '0');
    const dd = String(today.getDate() + 1).padStart(2, '0');
    dateInput.min = `${yyyy}-${mm}-${dd}`;
  }
</script>
</body>
</html>
