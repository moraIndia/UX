<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Rakesh Mohan — Senior Designer & Creative Strategist</title>
<meta name="description" content="Senior Designer & Creative Strategist with 12+ years of cross-industry experience across Finance, Ecommerce, SaaS, Services, and Advertising." />

<!-- Poppins -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet" />

<style>
/* =========================================================
   Rakesh Mohan — Portfolio (single-file build)
   Theme: Black / White / Grey · Poppins · Minimal
   ========================================================= */
:root {
  --black: #0a0a0a;
  --white: #ffffff;
  --grey-100: #f6f6f6;
  --grey-300: #d1d1d1;
  --grey-500: #8a8a8a;
  --grey-700: #4a4a4a;
  --grey-900: #1a1a1a;
  --ease: cubic-bezier(0.22, 0.61, 0.36, 1);
}
* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }
body {
  font-family: 'Poppins', sans-serif;
  font-weight: 300;
  background: var(--white);
  color: var(--black);
  line-height: 1.7;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
a { color: inherit; text-decoration: none; }

/* 1/3-width centered column */
.container {
  width: 33vw;
  max-width: 720px;
  min-width: 280px;
  margin: 0 auto;
  padding: 0 24px;
  text-align: left;
}

/* HEADER */
.site-header {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 22px 40px;
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: saturate(180%) blur(14px);
  -webkit-backdrop-filter: saturate(180%) blur(14px);
}
.logo { font-weight: 600; font-size: 16px; letter-spacing: 2px; color: var(--black); }
.nav-center { display: flex; gap: 36px; }
.nav-center a, .nav-contact {
  font-weight: 300; font-size: 14px; color: var(--grey-700);
  transition: color 0.3s var(--ease);
}
.nav-center a:hover, .nav-contact:hover { color: var(--black); }
.nav-contact { font-size: 14px; cursor: pointer; }

/* HERO */
.hero {
  position: relative;
  height: 55vh;
  min-height: 360px;
  width: 100%;
  overflow: hidden;
  background: var(--black);
}
.hero-placeholder, .hero-video {
  position: absolute; inset: 0;
  width: 100%; height: 100%;
  object-fit: cover; display: block;
}
.hero-placeholder { z-index: 1; filter: grayscale(100%); }
.hero-video { z-index: 2; }

/* SECTIONS — consistent 70px rhythm */
section { padding: 70px 0; }
.section-label {
  font-weight: 600; font-size: 13px;
  letter-spacing: 3px; text-transform: uppercase;
  color: var(--grey-500); margin-bottom: 32px;
}

/* About (hover to expand) */
.about-block { cursor: pointer; border-top: 1px solid var(--grey-100); padding: 32px 0; }
.about-title {
  font-weight: 600; font-size: 22px; color: var(--black);
  letter-spacing: -0.2px; transition: color 0.4s var(--ease);
}
.about-block:hover .about-title, .about-block.is-open .about-title { color: var(--grey-500); }
.about-content {
  display: grid; grid-template-rows: 0fr;
  transition: grid-template-rows 0.5s var(--ease);
}
.about-block:hover .about-content, .about-block.is-open .about-content { grid-template-rows: 1fr; }
.about-inner {
  overflow: hidden; opacity: 0; transform: translateY(8px);
  transition: opacity 0.4s var(--ease) 0.1s, transform 0.4s var(--ease) 0.1s;
}
.about-block:hover .about-inner, .about-block.is-open .about-inner {
  opacity: 1; transform: translateY(0); padding-top: 18px;
}
.about-inner p { font-size: 14px; color: var(--grey-700); margin-bottom: 18px; }

/* COMPETENCIES */
.competency-list { display: flex; flex-direction: column; }
.competency {
  padding: 32px 0; cursor: pointer;
  border-top: 1px solid var(--grey-100);
}
.competency:first-child { border-top: none; }
.competency-title {
  font-weight: 600; font-size: 22px; color: var(--black);
  letter-spacing: -0.2px;
  transition: color 0.4s var(--ease), transform 0.4s var(--ease);
}
.competency:hover .competency-title, .competency.is-open .competency-title { color: var(--grey-500); }
.competency-content {
  display: grid; grid-template-rows: 0fr;
  transition: grid-template-rows 0.5s var(--ease);
}
.competency:hover .competency-content, .competency.is-open .competency-content { grid-template-rows: 1fr; }
.competency-inner {
  overflow: hidden; opacity: 0; transform: translateY(8px);
  transition: opacity 0.4s var(--ease) 0.1s, transform 0.4s var(--ease) 0.1s;
}
.competency:hover .competency-inner, .competency.is-open .competency-inner {
  opacity: 1; transform: translateY(0); padding-top: 18px;
}
.competency-inner p { font-size: 14px; color: var(--grey-700); margin-bottom: 18px; }

.cta {
  display: inline-flex; align-items: center; gap: 10px;
  margin-top: 6px;
  font-weight: 600; font-size: 12px;
  letter-spacing: 2px; text-transform: uppercase;
  color: var(--black);
  padding-bottom: 4px;
  border-bottom: 1px solid var(--black);
  background: none; border-top: none; border-left: none; border-right: none;
  cursor: pointer; font-family: inherit;
  transition: gap 0.3s var(--ease);
}
.cta .arrow { display: inline-block; transition: transform 0.3s var(--ease); }
.cta:hover { gap: 16px; }
.cta:hover .arrow { transform: translateX(4px); }

/* FOOTER */
.site-footer {
  display: flex; align-items: center; justify-content: space-between;
  padding: 32px 40px; background: var(--white);
  border-top: 1px solid var(--grey-100);
}
.site-footer .logo { color: var(--black); }
.site-footer .nav-center a, .site-footer .nav-contact { font-size: 13px; color: var(--grey-700); }
.site-footer .nav-center a:hover, .site-footer .nav-contact:hover { color: var(--black); }

/* PORTFOLIO MODAL (single-file replacement for separate portfolio pages) */
.portfolio-modal {
  position: fixed; inset: 0; z-index: 200;
  background: var(--white);
  overflow-y: auto;
  opacity: 0; visibility: hidden;
  transition: opacity 0.4s var(--ease), visibility 0.4s var(--ease);
}
.portfolio-modal.is-open { opacity: 1; visibility: visible; }
.portfolio-modal-inner {
  padding: 80px 40px 60px;
  display: flex; justify-content: center;
}
.portfolio-modal .container { width: 60vw; max-width: 1100px; }
.portfolio-back {
  display: inline-block; margin-bottom: 32px;
  font-size: 12px; letter-spacing: 2px; text-transform: uppercase;
  color: var(--grey-500); background: none; border: none;
  font-family: inherit; cursor: pointer;
  transition: color 0.3s var(--ease);
}
.portfolio-back:hover { color: var(--black); }
.portfolio-title {
  font-weight: 600; font-size: 28px; color: var(--black);
  margin-bottom: 12px; letter-spacing: -0.3px;
}
.portfolio-intro { font-size: 14px; color: var(--grey-700); margin-bottom: 48px; }
.portfolio-grid {
  display: grid; grid-template-columns: 1fr 1fr; gap: 24px; width: 100%;
}
.portfolio-item { width: 100%; background: var(--grey-100); overflow: hidden; }
.portfolio-item img {
  width: 100%; height: auto; display: block;
  filter: grayscale(20%);
  transition: filter 0.6s var(--ease), transform 0.6s var(--ease);
}
.portfolio-item:hover img { filter: grayscale(0%); transform: scale(1.01); }

/* RESPONSIVE */
@media (max-width: 1024px) { .container { width: 50vw; } }
@media (max-width: 768px) {
  .site-header, .site-footer { padding: 18px 22px; }
  .nav-center { gap: 22px; }
  .nav-center a, .nav-contact { font-size: 13px; }
  .container { width: 88vw; padding: 0 16px; }
  section { padding: 45px 0; }
  .section-label { margin-bottom: 22px; }
  .competency-title, .about-title { font-size: 19px; }
  .competency, .about-block { padding: 24px 0; }
  .portfolio-modal-inner { padding: 60px 22px 40px; }
  .portfolio-modal .container { width: 100%; }
  .portfolio-grid { grid-template-columns: 1fr; }
}
@media (max-width: 480px) {
  .logo { font-size: 14px; }
  .nav-center { gap: 16px; }
  .nav-center a, .nav-contact { font-size: 12px; }
}
</style>
</head>
<body>

<!-- HEADER -->
<header class="site-header">
  <a href="#top" class="logo">RM</a>
  <nav class="nav-center">
    <a href="#top">Home</a>
    <a href="#competencies">Competencies</a>
  </nav>
  <a href="https://wa.me/918884572044" target="_blank" rel="noopener" class="nav-contact">Contact</a>
</header>

<!-- HERO -->
<section class="hero" id="top">
  <img class="hero-placeholder" src="https://picsum.photos/seed/hero-banner/1920/900" alt="" />
  <video class="hero-video" autoplay muted loop playsinline>
    <source src="assets/hero.mp4" type="video/mp4" />
  </video>
</section>

<!-- ABOUT -->
<section id="about" class="about">
  <div class="container">
    <h2 class="section-label">About</h2>
    <article class="about-block">
      <h3 class="about-title">Senior Designer &amp; Creative Strategist</h3>
      <div class="about-content">
        <div class="about-inner">
          <p>Senior Designer &amp; Creative Strategist with 12+ years of cross-industry experience across Finance, Ecommerce, SaaS, Services, and Advertising. A multidisciplinary design leader specializing in Branding &amp; Identity, UX Strategy, Design Systems, UI Design, Interaction Design, Dashboard &amp; Platform UX, and AI Product UX, complemented by expertise in Marketing, Motion Design, and Digital Experiences.</p>
          <p>Proven ability to bridge strategic thinking and design execution, translating complex business objectives into intuitive, scalable, and high-impact brand and digital experiences. Experienced in building cohesive design languages, establishing scalable visual systems, shaping user-centric product experiences, and aligning design decisions with business goals. Combines creative vision, systems thinking, and emerging AI-driven design practices to deliver purposeful, consistent, and commercially effective solutions across the product lifecycle.</p>
        </div>
      </div>
    </article>
  </div>
</section>

<!-- COMPETENCIES -->
<section id="competencies" class="competencies">
  <div class="container">
    <h2 class="section-label">Competencies</h2>
    <div class="competency-list">

      <article class="competency">
        <h3 class="competency-title">Branding &amp; Identity</h3>
        <div class="competency-content">
          <div class="competency-inner">
            <p>Crafting enduring brand systems that translate vision into recognizable visual languages. From logo design and typography to color theory and brand guidelines, every element is engineered for coherence across touchpoints and built to endure beyond trend cycles.</p>
            <p>Strategic positioning meets aesthetic precision. Each identity system balances distinctiveness with adaptability, ensuring the brand remains consistent whether applied to a business card, a billboard, or a digital interface — and flexible enough to evolve with the business.</p>
            <button class="cta" data-portfolio="branding">View Portfolio <span class="arrow">&rarr;</span></button>
          </div>
        </div>
      </article>

      <article class="competency">
        <h3 class="competency-title">UX Strategy</h3>
        <div class="competency-content">
          <div class="competency-inner">
            <p>Translating business goals into research-backed user journeys. UX strategy begins with stakeholder alignment, competitive analysis, and qualitative research to define the problems worth solving before a single screen is designed.</p>
            <p>From information architecture to interaction flows, every decision is anchored in user needs and measurable outcomes. The result is product experiences that are intuitive, scalable, and aligned with commercial objectives — not just aesthetically pleasing.</p>
            <button class="cta" data-portfolio="ux-strategy">View Portfolio <span class="arrow">&rarr;</span></button>
          </div>
        </div>
      </article>

      <article class="competency">
        <h3 class="competency-title">Design Systems</h3>
        <div class="competency-content">
          <div class="competency-inner">
            <p>Building scalable design systems that unify product teams around a shared visual and functional language. Component libraries, token architectures, and documentation frameworks reduce redundancy, eliminate drift, and accelerate delivery across squads.</p>
            <p>A well-designed system evolves with the product. Through governance models, contribution workflows, and versioned releases, the system remains flexible enough to absorb new patterns while preserving consistency across every surface it touches.</p>
            <button class="cta" data-portfolio="design-systems">View Portfolio <span class="arrow">&rarr;</span></button>
          </div>
        </div>
      </article>

      <article class="competency">
        <h3 class="competency-title">UI Design</h3>
        <div class="competency-content">
          <div class="competency-inner">
            <p>Interfaces that prioritize clarity, hierarchy, and intent. Every layout decision considers cognitive load, accessibility, and the rhythm of user attention across the screen — so the right action always feels like the obvious one.</p>
            <p>Pixel-level precision combined with system-level thinking. From spacing scales to typographic rhythm, the goal is interfaces that feel inevitable, where every element earns its place and nothing is decorative for its own sake.</p>
            <button class="cta" data-portfolio="ui-design">View Portfolio <span class="arrow">&rarr;</span></button>
          </div>
        </div>
      </article>

      <article class="competency">
        <h3 class="competency-title">Interaction Design</h3>
        <div class="competency-content">
          <div class="competency-inner">
            <p>Designing motion and feedback that guide users through complex workflows. Micro-interactions, transitions, and state changes communicate system status, reduce uncertainty, and make digital products feel alive and responsive.</p>
            <p>Interaction design bridges the gap between interface and experience. Each gesture, hover, and click is choreographed to feel responsive, purposeful, and unmistakably human — never flashy, always in service of the task at hand.</p>
            <button class="cta" data-portfolio="interaction-design">View Portfolio <span class="arrow">&rarr;</span></button>
          </div>
        </div>
      </article>

      <article class="competency">
        <h3 class="competency-title">Dashboard &amp; Platform UX</h3>
        <div class="competency-content">
          <div class="competency-inner">
            <p>Structuring dense information environments so insights surface with ease. Dashboards balance data density with cognitive clarity, enabling users to act decisively without feeling overwhelmed by the volume of information on screen.</p>
            <p>Platform UX extends beyond the screen to consider workflow, role-based access, and configurable experiences. The architecture supports power users while remaining approachable for first-time visitors discovering the product for the first time.</p>
            <button class="cta" data-portfolio="dashboard-ux">View Portfolio <span class="arrow">&rarr;</span></button>
          </div>
        </div>
      </article>

      <article class="competency">
        <h3 class="competency-title">AI Product UX</h3>
        <div class="competency-content">
          <div class="competency-inner">
            <p>Shaping how humans collaborate with intelligent systems. AI product UX addresses trust, transparency, and control — designing interfaces where machine outputs feel explainable, actionable, and respectful of the user's autonomy.</p>
            <p>From prompt interfaces to generative workflows, the design challenge is making complex AI capabilities legible. The result is products where intelligence augments human judgment rather than replacing it, and where confidence is earned through clarity.</p>
            <button class="cta" data-portfolio="ai-product-ux">View Portfolio <span class="arrow">&rarr;</span></button>
          </div>
        </div>
      </article>

    </div>
  </div>
</section>

<!-- FOOTER -->
<footer class="site-footer">
  <a href="#top" class="logo">RM</a>
  <nav class="nav-center">
    <a href="#top">Home</a>
    <a href="#competencies">Competencies</a>
    <a href="https://www.linkedin.com/in/rakesh-mohan-a0275a35a/" target="_blank" rel="noopener">LinkedIn</a>
  </nav>
  <a href="https://wa.me/918884572044" target="_blank" rel="noopener" class="nav-contact">Contact</a>
</footer>

<!-- PORTFOLIO MODAL (single-file replacement for separate portfolio pages) -->
<div class="portfolio-modal" id="portfolio-modal">
  <div class="portfolio-modal-inner">
    <div class="container">
      <button class="portfolio-back" id="portfolio-close">&larr; Back</button>
      <h1 class="portfolio-title" id="portfolio-title"></h1>
      <p class="portfolio-intro" id="portfolio-intro"></p>
      <div class="portfolio-grid" id="portfolio-grid"></div>
    </div>
  </div>
</div>

<script>
(function () {
  /* Portfolio content (was 7 separate HTML pages; now inlined for single-file use) */
  var PORTFOLIOS = {
    'branding': {
      title: 'Branding & Identity',
      intro: 'Selected identity systems — logo design, typographic voice, color systems, and brand guidelines crafted for coherence across every touchpoint.',
      seed: 'branding'
    },
    'ux-strategy': {
      title: 'UX Strategy',
      intro: 'Research, journey maps, information architecture, and product frameworks that translate business goals into intuitive user experiences.',
      seed: 'uxstrategy'
    },
    'design-systems': {
      title: 'Design Systems',
      intro: 'Scalable component libraries, design tokens, and governance frameworks that keep product teams aligned and shipping consistently.',
      seed: 'systems'
    },
    'ui-design': {
      title: 'UI Design',
      intro: 'Pixel-precise interfaces built on typographic rhythm, spacing scales, and a disciplined sense of hierarchy.',
      seed: 'uidesign'
    },
    'interaction-design': {
      title: 'Interaction Design',
      intro: 'Micro-interactions, transitions, and motion choreography that make digital products feel responsive, purposeful, and human.',
      seed: 'interaction'
    },
    'dashboard-ux': {
      title: 'Dashboard & Platform UX',
      intro: 'Dense information environments engineered for clarity — dashboards and platforms where insight surfaces and action follows.',
      seed: 'dashboard'
    },
    'ai-product-ux': {
      title: 'AI Product UX',
      intro: 'Interfaces for human-AI collaboration — prompt surfaces, generative workflows, and explainable outputs that earn user trust.',
      seed: 'aiproduct'
    }
  };

  /* Touch fallback for competency & about hover */
  var items = document.querySelectorAll('.competency');
  items.forEach(function (item) {
    item.addEventListener('click', function (e) {
      if (e.target.closest('button, a')) return;
      var isOpen = item.classList.contains('is-open');
      items.forEach(function (i) { i.classList.remove('is-open'); });
      if (!isOpen) item.classList.add('is-open');
    });
  });

  var aboutBlock = document.querySelector('.about-block');
  if (aboutBlock) {
    aboutBlock.addEventListener('click', function (e) {
      if (e.target.closest('button, a')) return;
      aboutBlock.classList.toggle('is-open');
    });
  }

  /* Portfolio modal */
  var modal = document.getElementById('portfolio-modal');
  var titleEl = document.getElementById('portfolio-title');
  var introEl = document.getElementById('portfolio-intro');
  var gridEl = document.getElementById('portfolio-grid');
  var closeBtn = document.getElementById('portfolio-close');

  function openPortfolio(key) {
    var data = PORTFOLIOS[key];
    if (!data) return;
    titleEl.textContent = data.title;
    introEl.textContent = data.intro;
    var html = '';
    for (var i = 1; i <= 6; i++) {
      html += '<div class="portfolio-item"><img src="https://picsum.photos/seed/' + data.seed + '-' + i + '/1200/800" alt="' + data.title + ' project ' + i + '" loading="lazy" /></div>';
    }
    gridEl.innerHTML = html;
    modal.classList.add('is-open');
    document.body.style.overflow = 'hidden';
    modal.scrollTop = 0;
  }

  function closePortfolio() {
    modal.classList.remove('is-open');
    document.body.style.overflow = '';
  }

  document.querySelectorAll('.cta[data-portfolio]').forEach(function (btn) {
    btn.addEventListener('click', function (e) {
      e.stopPropagation();
      openPortfolio(btn.getAttribute('data-portfolio'));
    });
  });

  closeBtn.addEventListener('click', closePortfolio);
  document.addEventListener('keydown', function (e) {
    if (e.key === 'Escape') closePortfolio();
  });

  /* Subtle reveal-on-scroll */
  var observer = new IntersectionObserver(function (entries) {
    entries.forEach(function (entry) {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.08 });

  document.querySelectorAll('section').forEach(function (s) {
    s.style.opacity = '0';
    s.style.transform = 'translateY(20px)';
    s.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
    observer.observe(s);
  });
})();
</script>
</body>
</html>
