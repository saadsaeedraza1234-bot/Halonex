# Halonex
A luxury payment wearable 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HALONEX · The future, refined.</title>
  <!-- Fonts & minimal reset -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,200;14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
  <style>
    /* ----- reset & base ----- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-color: #0b0a0a; /* obsidian black */
      color: #eae6df; /* soft ivory */
      font-family: 'Inter', sans-serif;
      font-weight: 300;
      line-height: 1.5;
      -webkit-font-smoothing: antialiased;
      overflow-x: hidden;
    }

    ::selection {
      background: #b79b6c; /* warm gold */
      color: #0b0a0a;
    }

    .container {
      max-width: 1320px;
      margin: 0 auto;
      padding: 0 40px;
    }

    /* ----- typography ----- */
    .section-title {
      font-size: clamp(2rem, 5vw, 3.8rem);
      font-weight: 300;
      letter-spacing: -0.02em;
      line-height: 1.1;
      color: #f0ebe3;
      margin-bottom: 1.2rem;
    }

    .section-sub {
      font-size: clamp(1rem, 1.4vw, 1.3rem);
      font-weight: 300;
      color: #a89f94;
      letter-spacing: 0.02em;
      max-width: 600px;
    }

    .gold-accent {
      color: #d4b68a; /* warm metallic gold */
    }

    /* ----- header / nav (ultra minimal) ----- */
    .navbar {
      padding: 32px 0 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid rgba(212, 182, 138, 0.1);
      margin-bottom: 10px;
    }

    .logo {
      font-size: 1.6rem;
      font-weight: 300;
      letter-spacing: 0.3em;
      color: #f0ebe3;
      text-transform: uppercase;
    }
    .logo span {
      color: #d4b68a;
      font-weight: 400;
    }

    .nav-links {
      display: flex;
      gap: 2.8rem;
      font-size: 0.8rem;
      font-weight: 400;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: #a89f94;
    }
    .nav-links a {
      color: inherit;
      text-decoration: none;
      transition: color 0.2s;
      border-bottom: 1px solid transparent;
      padding-bottom: 4px;
    }
    .nav-links a:hover {
      color: #d4b68a;
      border-bottom-color: #d4b68a;
    }

    /* ----- hero ----- */
    .hero {
      padding: 60px 0 100px;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      border-bottom: 1px solid rgba(212, 182, 138, 0.08);
    }

    .hero-badge {
      display: inline-block;
      border: 1px solid rgba(212, 182, 138, 0.25);
      padding: 8px 24px;
      border-radius: 40px;
      font-size: 0.7rem;
      letter-spacing: 0.25em;
      text-transform: uppercase;
      color: #b79b6c;
      margin-bottom: 48px;
      background: rgba(212, 182, 138, 0.03);
    }

    .hero h1 {
      font-size: clamp(3.2rem, 10vw, 7rem);
      font-weight: 200;
      letter-spacing: -0.03em;
      line-height: 1.05;
      color: #f5f0ea;
      margin-bottom: 24px;
    }
    .hero h1 .gold {
      color: #d4b68a;
      font-weight: 300;
    }

    .hero p {
      font-size: clamp(1rem, 1.5vw, 1.4rem);
      max-width: 620px;
      margin: 0 auto 48px;
      color: #b8ada1;
      font-weight: 300;
      letter-spacing: 0.02em;
    }

    .cta-button {
      display: inline-block;
      background: transparent;
      border: 1px solid #d4b68a;
      color: #f0ebe3;
      padding: 16px 56px;
      border-radius: 60px;
      font-size: 0.8rem;
      font-weight: 500;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      text-decoration: none;
      transition: all 0.3s ease;
      background: rgba(212, 182, 138, 0.02);
      backdrop-filter: blur(2px);
    }
    .cta-button:hover {
      background: #d4b68a;
      color: #0b0a0a;
      border-color: #d4b68a;
      box-shadow: 0 12px 30px rgba(212, 182, 138, 0.15);
    }

    /* ----- cinematic ring display (sculptural) ----- */
    .ring-display {
      margin: 60px 0 80px;
      display: flex;
      justify-content: center;
      position: relative;
    }

    .ring-artifact {
      width: 100%;
      max-width: 520px;
      aspect-ratio: 1/1;
      background: radial-gradient(circle at 40% 35%, #2a2620, #0b0a0a 80%);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 40px 80px rgba(0,0,0,0.8), 0 0 0 1px rgba(212, 182, 138, 0.08);
      position: relative;
    }

    .ring-object {
      width: 60%;
      height: 60%;
      border-radius: 50%;
      background: radial-gradient(circle at 30% 30%, #5a4d3a, #1f1b16 80%);
      box-shadow: 
        inset 0 -8px 20px rgba(0,0,0,0.8),
        0 20px 40px rgba(0,0,0,0.5),
        0 0 0 1px rgba(212, 182, 138, 0.15);
      position: relative;
      transform: rotate(10deg);
      transition: transform 0.8s ease;
    }
    .ring-object::after {
      content: '';
      position: absolute;
      top: 12%;
      left: 18%;
      width: 30%;
      height: 15%;
      background: radial-gradient(circle, rgba(212, 182, 138, 0.25) 0%, transparent 70%);
      border-radius: 50%;
      filter: blur(8px);
    }
    /* subtle halo */
    .ring-artifact::before {
      content: '';
      position: absolute;
      inset: -20px;
      border-radius: 50%;
      background: radial-gradient(circle at 30% 25%, rgba(212, 182, 138, 0.06), transparent 70%);
      z-index: -1;
    }

    .ring-caption {
      text-align: center;
      margin-top: 16px;
      font-size: 0.8rem;
      letter-spacing: 0.15em;
      color: #8a7f72;
      font-weight: 300;
    }
    .ring-caption span {
      color: #d4b68a;
      font-weight: 400;
    }

    /* ----- story / philosophy section ----- */
    .story-section {
      padding: 100px 0;
      border-top: 1px solid rgba(212, 182, 138, 0.06);
      border-bottom: 1px solid rgba(212, 182, 138, 0.06);
    }

    .story-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 80px;
      align-items: center;
    }

    .story-text .section-title {
      margin-bottom: 20px;
    }

    .story-text p {
      font-size: 1.1rem;
      color: #b8ada1;
      max-width: 460px;
      margin-bottom: 28px;
      font-weight: 300;
      letter-spacing: 0.01em;
    }

    .story-highlight {
      border-left: 2px solid #d4b68a;
      padding-left: 24px;
      font-style: normal;
      font-weight: 300;
      color: #e0d6ca;
      font-size: 1.2rem;
      margin: 32px 0;
    }

    .evolution-steps {
      display: flex;
      gap: 12px 20px;
      flex-wrap: wrap;
      margin-top: 24px;
      color: #8a7f72;
      font-size: 0.85rem;
      letter-spacing: 0.05em;
    }
    .evolution-steps span {
      background: rgba(212, 182, 138, 0.04);
      padding: 6px 18px;
      border-radius: 40px;
      border: 1px solid rgba(212, 182, 138, 0.08);
    }
    .evolution-steps .arrow {
      color: #d4b68a;
      font-weight: 200;
    }

    .story-image {
      background: #161311;
      aspect-ratio: 4/3;
      border-radius: 12px;
      background: radial-gradient(ellipse at 30% 40%, #2f2922, #0f0d0b);
      box-shadow: inset 0 0 0 1px rgba(212, 182, 138, 0.05);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #5a4d3a;
      font-weight: 200;
      letter-spacing: 0.2em;
      font-size: 0.9rem;
      position: relative;
      overflow: hidden;
    }
    .story-image .shimmer {
      position: absolute;
      top: -20%;
      left: -20%;
      width: 60%;
      height: 60%;
      background: radial-gradient(circle, rgba(212, 182, 138, 0.03), transparent 70%);
    }
    .story-image .label {
      z-index: 2;
      color: #b79b6c;
      opacity: 0.6;
    }

    /* ----- craftsmanship / product ----- */
    .craft-section {
      padding: 100px 0;
      border-bottom: 1px solid rgba(212, 182, 138, 0.06);
    }

    .craft-grid {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 40px;
      margin-top: 60px;
    }
    .craft-item {
      background: rgba(255,255,255,0.01);
      padding: 32px 20px 28px;
      border-radius: 8px;
      border: 1px solid rgba(212, 182, 138, 0.04);
      transition: all 0.3s ease;
    }
    .craft-item:hover {
      border-color: rgba(212, 182, 138, 0.15);
      background: rgba(212, 182, 138, 0.02);
    }
    .craft-item h4 {
      font-weight: 400;
      font-size: 1.2rem;
      letter-spacing: 0.05em;
      margin-bottom: 12px;
      color: #e0d6ca;
    }
    .craft-item p {
      font-size: 0.9rem;
      color: #9a8f82;
      font-weight: 300;
      line-height: 1.6;
    }

    /* ----- security vault ----- */
    .vault-section {
      padding: 100px 0;
      border-bottom: 1px solid rgba(212, 182, 138, 0.06);
      background: linear-gradient(180deg, #0b0a0a 0%, #0f0d0b 100%);
    }

    .vault-content {
      max-width: 760px;
      margin: 0 auto;
      text-align: center;
    }
    .vault-content .section-title {
      margin-bottom: 16px;
    }
    .vault-content p {
      color: #b8ada1;
      font-size: 1.1rem;
      max-width: 540px;
      margin: 0 auto 40px;
    }
    .vault-badge {
      display: inline-block;
      border: 1px solid rgba(212, 182, 138, 0.15);
      padding: 6px 28px;
      border-radius: 40px;
      font-size: 0.65rem;
      letter-spacing: 0.2em;
      color: #b79b6c;
      background: rgba(212, 182, 138, 0.02);
      margin-bottom: 12px;
    }

    /* ----- ownership experience ----- */
    .ownership-section {
      padding: 100px 0;
      border-bottom: 1px solid rgba(212, 182, 138, 0.06);
    }

    .ownership-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 60px;
      margin-top: 40px;
    }
    .ownership-item {
      border-left: 1px solid rgba(212, 182, 138, 0.08);
      padding-left: 28px;
    }
    .ownership-item h4 {
      font-weight: 400;
      font-size: 1.2rem;
      letter-spacing: 0.05em;
      color: #e0d6ca;
      margin-bottom: 8px;
    }
    .ownership-item p {
      color: #9a8f82;
      font-weight: 300;
      font-size: 0.95rem;
    }

    /* ----- final impression / footer ----- */
    .footer {
      padding: 80px 0 48px;
      text-align: center;
      border-top: 1px solid rgba(212, 182, 138, 0.04);
    }
    .footer .logo {
      font-size: 1.2rem;
      margin-bottom: 20px;
    }
    .footer p {
      color: #5a4d3a;
      font-size: 0.8rem;
      letter-spacing: 0.05em;
      max-width: 300px;
      margin: 0 auto;
    }
    .footer .tagline {
      color: #8a7f72;
      font-size: 0.9rem;
      margin-top: 12px;
      font-weight: 200;
      letter-spacing: 0.1em;
    }

    /* ----- responsive ----- */
    @media (max-width: 900px) {
      .story-grid, .craft-grid {
        grid-template-columns: 1fr;
        gap: 40px;
      }
      .ownership-grid {
        grid-template-columns: 1fr;
        gap: 28px;
      }
      .navbar {
        flex-direction: column;
        gap: 16px;
      }
      .nav-links {
        gap: 1.6rem;
        flex-wrap: wrap;
        justify-content: center;
      }
      .container {
        padding: 0 24px;
      }
      .hero {
        padding: 30px 0 60px;
      }
      .ring-artifact {
        max-width: 320px;
      }
    }

    @media (max-width: 480px) {
      .nav-links {
        font-size: 0.65rem;
        gap: 1rem;
      }
      .hero h1 {
        font-size: 2.8rem;
      }
      .cta-button {
        padding: 14px 32px;
        font-size: 0.7rem;
      }
    }

    /* subtle animation on load */
    .fade-in {
      animation: fadeIn 1.2s ease forwards;
      opacity: 0;
    }
    @keyframes fadeIn {
      0% { opacity: 0; transform: translateY(12px); }
      100% { opacity: 1; transform: translateY(0); }
    }
    .delay-1 { animation-delay: 0.2s; }
    .delay-2 { animation-delay: 0.4s; }
    .delay-3 { animation-delay: 0.6s; }
  </style>
</head>
<body>
  <div class="container">
    <!-- header -->
    <header class="navbar fade-in">
      <div class="logo">HALONEX <span>·</span></div>
      <div class="nav-links">
        <a href="#">The Ring</a>
        <a href="#">Craft</a>
        <a href="#">Security</a>
        <a href="#">Private</a>
      </div>
    </header>

    <!-- hero -->
    <section class="hero fade-in delay-1">
      <div class="hero-badge">Founder's Edition · 001/1000</div>
      <h1>THE FUTURE, <span class="gold">REFINED.</span></h1>
      <p>A new expression of personal finance. Crafted as jewelry. Engineered as technology.</p>
      <a href="#" class="cta-button">Request Private Access</a>

      <div class="ring-display">
        <div class="ring-artifact">
          <div class="ring-object"></div>
        </div>
      </div>
      <div class="ring-caption">HALONEX <span>·</span> sculpted ceramic · invisible payment</div>
    </section>

    <!-- story / philosophy -->
    <section class="story-section fade-in delay-2">
      <div class="story-grid">
        <div class="story-text">
          <div class="section-title">Technology <br>that <span class="gold">becomes</span> part of you.</div>
          <p>Technology should not demand attention. It should become part of you. HALONEX is the next evolution—from wallet to card to phone to wearable.</p>
          <div class="story-highlight">“Luxury that moves with you.”</div>
          <div class="evolution-steps">
            <span>Wallet</span> <span class="arrow">→</span> <span>Card</span> <span class="arrow">→</span> <span>Phone</span> <span class="arrow">→</span> <span style="color:#d4b68a; border-color:#d4b68a;">Wearable</span>
          </div>
        </div>
        <div class="story-image">
          <div class="shimmer"></div>
          <span class="label">Craft · Precision · Silence</span>
        </div>
      </div>
    </section>

    <!-- craftsmanship -->
    <section class="craft-section fade-in delay-3">
      <div style="text-align: center; max-width: 700px; margin: 0 auto;">
        <div class="section-title">Masterpiece <span class="gold">of</span> form</div>
        <p class="section-sub" style="margin: 0 auto 20px;">Seamless ceramic · sculpted surface · precision engineering. Not a gadget. A luxury object powered by advanced technology.</p>
      </div>
      <div class="craft-grid">
        <div class="craft-item"><h4>Seamless ceramic</h4><p>Monolithic surface, warm to the touch. Engineered for a lifetime.</p></div>
        <div class="craft-item"><h4>Sculpted form</h4><p>Architectural lines, ergonomic perfection. Worn with intent.</p></div>
        <div class="craft-item"><h4>Invisible payment</h4><p>Financial-grade technology, concealed within timeless design.</p></div>
      </div>
    </section>

    <!-- vault / security -->
    <section class="vault-section fade-in">
      <div class="vault-content">
        <div class="vault-badge">✦ vault-grade security</div>
        <div class="section-title">Protected <span class="gold">like</span> a vault</div>
        <p>Advanced payment protection, secure transactions, and financial-grade encryption. Quiet confidence, always.</p>
        <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin-top: 12px;">
          <span style="border:1px solid rgba(212,182,138,0.06); padding:4px 24px; border-radius:40px; font-size:0.7rem; color:#8a7f72;">Secure transactions</span>
          <span style="border:1px solid rgba(212,182,138,0.06); padding:4px 24px; border-radius:40px; font-size:0.7rem; color:#8a7f72;">Advanced protection</span>
          <span style="border:1px solid rgba(212,182,138,0.06); padding:4px 24px; border-radius:40px; font-size:0.7rem; color:#8a7f72;">Financial-grade</span>
        </div>
      </div>
    </section>

    <!-- ownership experience -->
    <section class="ownership-section fade-in">
      <div style="max-width: 800px; margin: 0 auto; text-align: center;">
        <div class="section-title">The <span class="gold">ownership</span> journey</div>
        <p class="section-sub" style="margin: 0 auto 20px;">Exclusive access, premium packaging, private relationship. Each ring arrives in an obsidian box with gold accents — like opening a rare timepiece.</p>
      </div>
      <div class="ownership-grid">
        <div class="ownership-item"><h4>Exclusive access</h4><p>Founder’s Edition. One thousand pieces worldwide.</p></div>
        <div class="ownership-item"><h4>Premium packaging</h4><p>Obsidian presentation box, tactile materials, invitation card.</p></div>
        <div class="ownership-item"><h4>Personalized experience</h4><p>Dedicated client relationship, concierge service.</p></div>
        <div class="ownership-item"><h4>Private customer</h4><p>Discreet, white-glove service from first contact.</p></div>
      </div>
    </section>

    <!-- footer -->
    <footer class="footer fade-in">
      <div class="logo">HALONEX <span>·</span></div>
      <p class="tagline">Luxury that moves with you.</p>
      <p style="margin-top: 28px; font-size: 0.65rem; letter-spacing: 0.1em;">© 2026 HALONEX · Private Collection</p>
      <p style="font-size:0.6rem; color:#3d352e; margin-top: 8px;">not something i use · something i own</p>
    </footer>
  </div>
</body>
</html>
