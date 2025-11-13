# Bendito-portfolio
Bendito Engineering Consult portfolio
<!doctype html>

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Bendito Engineering Consult — Portfolio</title>
  <meta name="description" content="Bendito Engineering Consult — Electrical & Electronics Engineering portfolio. Design, solar systems, SMPS repair, embedded systems." />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#071021;
      --card:#0d1724;
      --muted:#9aa8bf;
      --accent:#ffd54a; /* warm yellow */
      --accent-2:#2bd4ff;
      --glass: rgba(255,255,255,0.03);
      --radius:14px;
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; background:linear-gradient(180deg,var(--bg),#020814 90%); color:#e6eef8; -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }
    .container{max-width:1100px;margin:0 auto;padding:28px}/* HEADER */
header{position:fixed;inset:18px 0 auto 0;z-index:40;backdrop-filter: blur(6px);}
.nav{display:flex;align-items:center;justify-content:space-between;padding:10px 22px;margin:0 12px;background:var(--glass);border-radius:16px}
.brand{display:flex;gap:12px;align-items:center}
.logo{width:48px;height:48px;border-radius:10px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;font-weight:800;color:#071021}
.title{font-weight:700}
nav a{color:var(--muted);text-decoration:none;margin-left:18px;font-weight:600}
.cta{background:linear-gradient(90deg,var(--accent),#ffb84d);color:#071021;padding:8px 14px;border-radius:10px;font-weight:700;text-decoration:none}

/* HERO */
.hero{display:grid;grid-template-columns:1fr 420px;gap:36px;align-items:center;padding-top:84px;padding-bottom:56px}
.hero-left h1{font-size: clamp(28px,4vw,44px);margin:0 0 8px}
.hero-left p.lead{color:var(--muted);margin:0 0 16px}
.badges{display:flex;gap:8px;flex-wrap:wrap}
.badge{background:rgba(255,255,255,0.03);padding:8px 12px;border-radius:10px;font-weight:600;color:var(--muted);}
.tagline-rotator{font-weight:700;color:var(--accent);min-height:28px}
.hero-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:18px;border-radius:16px;border:1px solid rgba(255,255,255,0.03)}
.profile-placeholder{width:100%;height:360px;border-radius:12px;background:linear-gradient(180deg,#081423,#042034);display:flex;align-items:center;justify-content:center;color:var(--muted);font-weight:700}

/* SECTIONS */
section{padding:28px 0}
h2.section-title{font-size:20px;margin:0 0 14px}
p.muted{color:var(--muted)}

/* ABOUT */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px}
.about-card{background:var(--card);padding:18px;border-radius:12px;border:1px solid rgba(255,255,255,0.02)}
.stat-row{display:flex;gap:18px;margin-top:12px}
.stat{background:rgba(0,0,0,0.15);padding:10px;border-radius:10px;text-align:center;flex:1}
.muted-small{color:var(--muted);font-size:13px}

/* PROJECTS */
.projects-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.project{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.04));padding:12px;border-radius:12px;border:1px solid rgba(255,255,255,0.02);min-height:160px;display:flex;flex-direction:column}
.project .thumb{height:110px;border-radius:8px;background:linear-gradient(90deg,#021225,#042a3a);display:flex;align-items:center;justify-content:center;color:var(--muted);font-weight:700;margin-bottom:8px}
.project h3{margin:0 0 6px}
.project p{margin:0;color:var(--muted);font-size:14px}

/* SKILLS */
.skills{display:flex;flex-wrap:wrap;gap:10px}
.skill{padding:8px 12px;border-radius:10px;background:rgba(255,255,255,0.02);font-weight:600;color:var(--muted)}

/* CONTACT */
.contact-grid{display:grid;grid-template-columns:1fr 360px;gap:18px}
.contact-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.04));padding:18px;border-radius:12px}
.contact-item{display:flex;align-items:center;gap:12px;margin-bottom:12px}
.icon{width:44px;height:44px;border-radius:8px;background:rgba(255,255,255,0.03);display:flex;align-items:center;justify-content:center}
.rc{font-size:12px;color:var(--muted);margin-top:10px}

footer{padding:24px 0;text-align:center;color:var(--muted);border-top:1px solid rgba(255,255,255,0.02);margin-top:36px}

/* Responsive */
@media (max-width:980px){
  .hero{grid-template-columns:1fr;}
  .projects-grid{grid-template-columns:repeat(2,1fr)}
  .about-grid{grid-template-columns:1fr}
  .contact-grid{grid-template-columns:1fr}
}
@media (max-width:560px){
  .projects-grid{grid-template-columns:1fr}
  .nav a{display:none}
  .nav .cta{display:none}
  header{left:12px;right:12px}
}

/* subtle animations */
.fade-in{opacity:0;transform:translateY(8px);transition:opacity .6s ease, transform .6s ease}
.fade-in.visible{opacity:1;transform:none}
.tilt{transform-origin:center}

/* tiny helper */
.muted-inline{color:var(--muted);font-weight:600}

  </style>
</head>
<body>
  <header>
    <div class="nav container">
      <div class="brand">
        <div class="logo">B</div>
        <div>
          <div class="title">Bendito Engineering Consult</div>
          <div class="muted-small">Electrical & Electronics Engineering</div>
        </div>
      </div>
      <div style="display:flex;align-items:center">
        <nav>
          <a href="#projects">Projects</a>
          <a href="#skills">Skills</a>
          <a href="#about">About</a>
          <a href="#contact">Contact</a>
        </nav>
        <a class="cta" href="#contact" style="margin-left:18px">Hire / Contact</a>
      </div>
    </div>
  </header>  <main class="container">
    <section class="hero">
      <div class="hero-left">
        <h1 class="fade-in">Concise & Technical<br><span style="color:var(--accent)">Designing the circuits of tomorrow.</span></h1>
        <p class="lead fade-in">Specialized in power systems, solar installations, SMPS repair, embedded solutions and practical electronics design.</p>
        <div class="badges fade-in">
          <div class="badge">RC: 3832347</div>
          <div class="badge">Electrical & Electronics</div>
          <div class="badge">Solar • SMPS • Embedded</div>
        </div><div style="margin-top:18px" class="fade-in">
      <div class="muted-small">Taglines</div>
      <div class="tagline-rotator" id="rotator">Harnessing the power of electrons.</div>
    </div>
  </div>

  <aside class="hero-card">
    <div class="profile-placeholder">
      Profile photo placeholder
    </div>
    <div style="display:flex;justify-content:space-between;align-items:center;margin-top:12px">
      <div>
        <div style="font-weight:700">Engr. Benedict Anyadiufu</div>
        <div class="muted-small">Founder — Bendito Engineering Consult</div>
      </div>
      <div style="text-align:right">
        <div style="font-weight:800;color:var(--accent)">+234 703 576 1443</div>
        <div class="muted-small">benditoengineering@gmail.com</div>
      </div>
    </div>
  </aside>
</section>

<section id="about">
  <h2 class="section-title">About</h2>
  <div class="about-grid">
    <div class="about-card fade-in">
      <p class="muted">Bendito Engineering Consult (RC: 3832347) is an Electrical & Electronics engineering practice focused on delivering pragmatic power and embedded solutions. We design, prototype and implement systems — from residential solar installs to SMPS repair and embedded controller integration.</p>
      <div class="stat-row">
        <div class="stat"><div style="font-weight:800">10+</div><div class="muted-small">Years experience</div></div>
        <div class="stat"><div style="font-weight:800">50+</div><div class="muted-small">Projects delivered</div></div>
        <div class="stat"><div style="font-weight:800">5</div><div class="muted-small">Core services</div></div>
      </div>
    </div>
    <div class="about-card fade-in">
      <h3 style="margin-top:0">Approach</h3>
      <p class="muted">We combine rigorous circuit-level engineering with field-tested installation practices. Our designs are optimised for reliability, serviceability and cost-effectiveness. Proofs of concept are validated on the bench before deployment.</p>

      <div style="margin-top:12px">
        <div class="muted-small">Core specialties</div>
        <div class="skills" style="margin-top:8px">
          <div class="skill">Power Systems</div>
          <div class="skill">Solar Installations</div>
          <div class="skill">SMPS Design & Repair</div>
          <div class="skill">Embedded Systems</div>
          <div class="skill">PCB Design</div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <h2 class="section-title">Projects</h2>
  <p class="muted">A curated selection of real projects and prototypes. Click any card to see more (replace placeholders with your project images / case studies).</p>
  <div class="projects-grid" style="margin-top:12px">
    <div class="project fade-in tilt" tabindex="0">
      <div class="thumb">Solar Mini-grid — Residential</div>
      <h3>Residential Solar + ESS</h3>
      <p>Design and installation of a 3.5kW solar array with battery energy storage, on-grid/off-grid hybrid system.</p>
    </div>
    <div class="project fade-in tilt" tabindex="0">
      <div class="thumb">SMPS Repair & Upgrade</div>
      <h3>SMPS Overhaul</h3>
      <p>Fault diagnosis and component-level repair of server-grade SMPS. Improved efficiency and stability.</p>
    </div>
    <div class="project fade-in tilt" tabindex="0">
      <div class="thumb">Embedded Control</div>
      <h3>Battery Management MCU</h3>
      <p>Custom BMS using STM32 with cell balancing and CAN bus telemetry for fleet monitoring.</p>
    </div>

    <div class="project fade-in tilt" tabindex="0">
      <div class="thumb">Prototype</div>
      <h3>Power Converter POC</h3>
      <p>Prototype of a 48V-to-12V high-efficiency converter for telecom applications.</p>
    </div>
    <div class="project fade-in tilt" tabindex="0">
      <div class="thumb">Site Work</div>
      <h3>Commercial Installation</h3>
      <p>Large rooftop solar array with structured cable management and protective earthing.</p>
    </div>
    <div class="project fade-in tilt" tabindex="0">
      <div class="thumb">PCB</div>
      <h3>Custom PCB Design</h3>
      <p>4-layer PCB for precision analog front-end used in sensor instrumentation.</p>
    </div>
  </div>
</section>

<section id="skills">
  <h2 class="section-title">Skills & Services</h2>
  <div style="display:flex;gap:18px;flex-wrap:wrap">
    <div class="about-card fade-in" style="flex:1;min-width:300px">
      <h3 style="margin-top:0">Services</h3>
      <ul class="muted-small">
        <li>Solar system design & installation</li>
        <li>SMPS diagnostics, repair & redesign</li>
        <li>Embedded firmware + MCU integration</li>
        <li>PCB layout & prototype</li>
        <li>Power system protection & earthing</li>
      </ul>
    </div>

    <div class="about-card fade-in" style="flex:1;min-width:280px">
      <h3 style="margin-top:0">Tools & Tech</h3>
      <div class="skills" style="margin-top:8px">
        <div class="skill">Altium / KiCad</div>
        <div class="skill">STM32 / AVR</div>
        <div class="skill">LTspice / PLECS</div>
        <div class="skill">MATLAB</div>
        <div class="skill">Oscilloscope / DMM</div>
      </div>
    </div>
  </div>
</section>

<section id="contact">
  <h2 class="section-title">Contact</h2>
  <div class="contact-grid">
    <div class="contact-card fade-in">
      <p class="muted">Get in touch for project enquiries, quotes, or site inspections. We offer free initial consultations for solar assessments.</p>

      <div class="contact-item">
        <div class="icon">📞</div>
        <div>
          <div style="font-weight:800">07035761443</div>
          <div class="muted-small">Phone</div>
        </div>
      </div>

      <div class="contact-item">
        <div class="icon">✉️</div>
        <div>
          <div style="font-weight:800">benditoengineering@gmail.com</div>
          <div class="muted-small">Email</div>
        </div>
      </div>

      <div class="contact-item">
        <div class="icon">💬</div>
        <div>
          <a href="https://wa.me/message/P3DFSX3OKFI6G1" style="color:var(--accent);font-weight:700;text-decoration:none">WhatsApp Chat</a>
          <div class="muted-small">Quickest way to reach us</div>
        </div>
      </div>

      <div class="muted-small rc">Company RC: 3832347</div>
    </div>

    <aside class="contact-card fade-in">
      <h3 style="margin-top:0">Send an email</h3>
      <form id="contactForm">
        <label class="muted-small">Your name</label><br>
        <input name="name" type="text" placeholder="Your name" required style="width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.03);background:transparent;color:inherit;margin-bottom:8px">
        <label class="muted-small">Message</label><br>
        <textarea name="message" rows="5" placeholder="Tell us about your project" required style="width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.03);background:transparent;color:inherit;margin-bottom:8px"></textarea>
        <button type="submit" class="cta" style="width:100%">Send Email</button>
      </form>

      <div style="margin-top:12px;font-size:13px;color:var(--muted)">Or message on Facebook: <a href="https://www.facebook.com/Bendito-Engineering-Consult-100148589921761" style="color:var(--accent);text-decoration:none">Bendito Engineering Consult</a></div>
    </aside>
  </div>
</section>

<footer>
  <div>© <strong>Bendito Engineering Consult</strong> — All rights reserved.</div>
  <div style="margin-top:8px" class="muted-small">Designed for an engineering-first audience. Built with clarity & performance in mind.</div>
</footer>

  </main>  <script>
    // Rotating taglines
    const taglines = [
      "Harnessing the power of electrons.",
      "Electrifying innovation, one project at a time.",
      "Where hardware meets ingenuity.",
      "Building the future, wired differently.",
      "Translating power into progress.",
      "The power behind the technology.",
      "Engineering solutions that light up the world."
    ];
    let idx = 0;
    const rot = document.getElementById('rotator');
    setInterval(()=>{
      idx = (idx+1) % taglines.length;
      rot.style.opacity = 0;setTimeout(()=>{rot.textContent = taglines[idx];rot.style.opacity=1},220)
    },3500);

    // Reveal on scroll
    const faders = document.querySelectorAll('.fade-in');
    const appearOptions = {threshold:0.12};
    const appearOnScroll = new IntersectionObserver(function(entries, appearOnScroll){
      entries.forEach(entry=>{
        if(!entry.isIntersecting) return;
        entry.target.classList.add('visible');
        appearOnScroll.unobserve(entry.target);
      });
    }, appearOptions);
    faders.forEach(fader => { appearOnScroll.observe(fader); });

    // Contact form -> mailto fallback
    document.getElementById('contactForm').addEventListener('submit', function(e){
      e.preventDefault();
      const name = this.name.value.trim();
      const msg = this.message.value.trim();
      const subject = encodeURIComponent('Website enquiry from ' + (name || 'Visitor'));
      const body = encodeURIComponent(msg + "\n\n--\nBendito Engineering Consult\nPhone: 07035761443");
      window.location.href = `mailto:benditoengineering@gmail.com?subject=${subject}&body=${body}`;
    });
  </script></body>
</html>
