<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Fenwick House Co. — Floor Plans</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,400&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --navy-0:#080E1A;
    --navy-1:#0A1424;
    --navy-2:#111E33;
    --navy-3:#16223A;
    --line:#28374F;
    --line-soft:rgba(150,165,194,0.18);
    --gold:#C4A468;
    --gold-bright:#D9BC85;
    --cream:#F2EFE6;
    --slate:#96A5C2;
    --slate-dim:#6E7C97;
    --radius-s:3px;
    --radius-m:6px;
    --maxw:1180px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--navy-1);
    color:var(--cream);
    font-family:'Inter',sans-serif;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,h4{
    font-family:'Fraunces',serif;
    font-weight:500;
    margin:0;
    letter-spacing:0.2px;
  }
  a{color:inherit;text-decoration:none;}
  img{max-width:100%;display:block;}
  button{font-family:inherit;cursor:pointer;}
  .wrap{max-width:var(--maxw);margin:0 auto;padding:0 32px;}
  @media(max-width:640px){.wrap{padding:0 20px;}}

  /* ---------- focus ---------- */
  a:focus-visible,button:focus-visible,input:focus-visible{
    outline:2px solid var(--gold);
    outline-offset:2px;
  }

  /* ---------- header ---------- */
  header{
    position:fixed;top:0;left:0;right:0;z-index:100;
    padding:22px 0;
    transition:background 0.35s ease, padding 0.35s ease, border-color .35s ease;
    border-bottom:1px solid transparent;
  }
  header.scrolled{
    background:rgba(8,14,26,0.92);
    backdrop-filter:blur(10px);
    padding:14px 0;
    border-bottom:1px solid var(--line-soft);
  }
  .nav-row{display:flex;align-items:center;justify-content:space-between;gap:24px;}
  .brand{display:flex;align-items:center;gap:10px;font-family:'Fraunces',serif;font-size:20px;letter-spacing:0.3px;color:var(--cream);}
  .brand-mark{
    width:30px;height:30px;flex:none;border:1px solid var(--gold);
    display:flex;align-items:center;justify-content:center;border-radius:2px;
  }
  .brand-mark svg{width:16px;height:16px;stroke:var(--gold);}
  .nav-links{display:flex;gap:34px;list-style:none;margin:0;padding:0;}
  .nav-links a{
    font-size:13.5px;color:var(--slate);letter-spacing:0.2px;
    transition:color 0.25s ease;position:relative;
  }
  .nav-links a:hover{color:var(--cream);}
  .nav-cta{
    border:1px solid var(--gold);color:var(--gold-bright);
    padding:10px 20px;font-size:13px;border-radius:2px;
    letter-spacing:0.3px;white-space:nowrap;
    transition:background 0.25s ease,color 0.25s ease;
  }
  .nav-cta:hover{background:var(--gold);color:var(--navy-0);}
  .nav-right{display:flex;align-items:center;gap:22px;}
  .hamburger{display:none;background:none;border:none;padding:6px;}
  .hamburger svg{width:22px;height:22px;stroke:var(--cream);}
  .mobile-panel{
    display:none;position:fixed;inset:0;background:var(--navy-0);z-index:99;
    padding:100px 28px 40px;flex-direction:column;gap:26px;
  }
  .mobile-panel.open{display:flex;}
  .mobile-panel a{font-family:'Fraunces',serif;font-size:26px;color:var(--cream);}
  .mobile-panel .nav-cta{align-self:flex-start;margin-top:10px;}

  @media(max-width:880px){
    .nav-links{display:none;}
    .hamburger{display:block;}
    .nav-right .nav-cta{display:none;}
  }

  /* ---------- hero ---------- */
  .hero{
    position:relative;
    min-height:560px;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:150px 24px 70px;
    background:
      linear-gradient(180deg, rgba(6,10,18,0.55) 0%, rgba(7,12,22,0.78) 55%, rgba(8,14,26,1) 100%),
      url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1800&q=80') center/cover no-repeat;
  }
  .hero-inner{max-width:760px;text-align:center;}
  .hero h1{
    font-size:clamp(42px,7vw,68px);
    color:var(--cream);
    font-weight:400;
    line-height:1.05;
  }
  .hero p.sub{
    margin:20px auto 0;
    max-width:520px;
    color:#D9DEE8;
    font-size:16px;
    line-height:1.6;
  }
  .cat-row{
    display:flex;flex-wrap:wrap;justify-content:center;gap:10px;
    margin:38px 0 0;
  }
  .cat-btn{
    background:rgba(10,16,28,0.35);
    border:1px solid rgba(196,164,104,0.45);
    color:var(--gold-bright);
    padding:10px 18px;
    font-size:13px;
    letter-spacing:0.3px;
    border-radius:2px;
    transition:background .25s ease, border-color .25s ease, color .25s ease;
    white-space:nowrap;
  }
  .cat-btn:hover{border-color:var(--gold);background:rgba(196,164,104,0.1);}
  .cat-btn.active{background:var(--gold);border-color:var(--gold);color:var(--navy-0);}

  .search-wrap{
    margin:30px auto 0;
    max-width:580px;
    position:relative;
  }
  .search-wrap svg{
    position:absolute;left:18px;top:50%;transform:translateY(-50%);
    width:16px;height:16px;stroke:var(--slate);
  }
  #search-input{
    width:100%;
    background:rgba(9,14,25,0.65);
    border:1px solid var(--line-soft);
    border-radius:3px;
    padding:15px 18px 15px 46px;
    color:var(--cream);
    font-size:14px;
    font-family:'Inter',sans-serif;
  }
  #search-input::placeholder{color:var(--slate-dim);}
  #search-input:focus{border-color:var(--gold);outline:none;}

  @media(max-width:640px){
    .cat-row{flex-wrap:nowrap;overflow-x:auto;justify-content:flex-start;padding-bottom:6px;-webkit-overflow-scrolling:touch;}
    .cat-row::-webkit-scrollbar{display:none;}
  }

  /* ---------- sections ---------- */
  main{padding-top:10px;}
  .plan-section{padding:78px 0;}
  .plan-section + .plan-section{border-top:1px solid var(--line-soft);}
  .section-head h2{font-size:32px;color:var(--cream);font-weight:400;}
  .section-head p{margin:10px 0 0;color:var(--slate);font-size:14.5px;max-width:520px;}
  .divider{height:1px;background:var(--line-soft);margin:26px 0 40px;}

  .card-grid{
    display:grid;grid-template-columns:repeat(3,1fr);gap:26px;
  }
  @media(max-width:980px){.card-grid{grid-template-columns:repeat(2,1fr);}}
  @media(max-width:640px){.card-grid{grid-template-columns:1fr;}}

  .plan-card{
    background:var(--navy-2);
    border:1px solid var(--line);
    border-radius:var(--radius-m);
    overflow:hidden;
    transition:transform .35s ease, box-shadow .35s ease, border-color .35s ease;
  }
  .plan-card:hover{
    transform:translateY(-4px);
    box-shadow:0 18px 34px rgba(0,0,0,0.35);
    border-color:rgba(196,164,104,0.4);
  }
  .card-img{position:relative;overflow:hidden;aspect-ratio:4/3;background:var(--navy-3);}
  .card-img img{width:100%;height:100%;object-fit:cover;transition:transform .6s ease;}
  .plan-card:hover .card-img img{transform:scale(1.06);}
  .badge{
    position:absolute;top:14px;left:14px;
    background:rgba(8,14,26,0.72);
    backdrop-filter:blur(3px);
    color:var(--gold-bright);
    font-size:12px;letter-spacing:0.3px;
    padding:6px 12px;border-radius:2px;
    border:1px solid rgba(196,164,104,0.35);
  }
  .card-body{padding:22px 22px 24px;}
  .card-body h3{font-size:20px;color:var(--cream);font-weight:500;}
  .meta-row{display:flex;gap:16px;margin:12px 0 14px;color:var(--slate);font-size:12.5px;letter-spacing:0.2px;}
  .meta-row span{display:flex;align-items:center;gap:5px;}
  .meta-row svg{width:13px;height:13px;stroke:var(--slate);}
  .card-desc{color:#AEB9CE;font-size:13.5px;line-height:1.55;margin:0 0 18px;}
  .view-link{
    font-size:13px;color:var(--gold-bright);letter-spacing:0.2px;
    display:inline-flex;align-items:center;gap:6px;
    border-top:1px solid var(--line-soft);padding-top:16px;width:100%;
    transition:gap .25s ease;
  }
  .plan-card:hover .view-link{gap:10px;}

  .no-results{
    text-align:center;padding:60px 20px;color:var(--slate);
    font-family:'Fraunces',serif;font-size:20px;grid-column:1/-1;
  }
  .hidden{display:none !important;}

  /* ---------- detail view ---------- */
  #detail-view{display:none;}
  #detail-view.active{display:block;}
  #detail-view .hero{
    min-height:420px;padding:150px 24px 60px;
  }
  .back-link{
    display:inline-flex;align-items:center;gap:8px;
    color:var(--slate);font-size:13px;margin:34px 0 0;
  }
  .back-link:hover{color:var(--gold-bright);}
  .back-link svg{width:14px;height:14px;stroke:currentColor;}

  .detail-head{display:flex;flex-wrap:wrap;justify-content:space-between;align-items:flex-end;gap:24px;margin:26px 0 40px;}
  .detail-head h1{font-size:clamp(32px,5vw,46px);font-weight:400;color:var(--cream);}
  .detail-stats{display:flex;flex-wrap:wrap;gap:28px;}
  .stat{min-width:80px;}
  .stat .num{font-family:'Fraunces',serif;font-size:24px;color:var(--gold-bright);}
  .stat .lab{font-size:11.5px;color:var(--slate);letter-spacing:0.3px;margin-top:4px;}

  .detail-actions{display:flex;flex-wrap:wrap;gap:12px;margin:0 0 50px;}
  .btn{
    padding:13px 24px;font-size:13px;letter-spacing:0.3px;border-radius:2px;
    border:1px solid var(--line-soft);color:var(--cream);
    transition:border-color .25s ease, background .25s ease;
  }
  .btn:hover{border-color:var(--gold);}
  .btn-primary{background:var(--gold);border-color:var(--gold);color:var(--navy-0);}
  .btn-primary:hover{background:var(--gold-bright);}

  .tabs{display:flex;gap:6px;border-bottom:1px solid var(--line-soft);margin-bottom:34px;flex-wrap:wrap;}
  .tab-btn{
    background:none;border:none;color:var(--slate);padding:12px 18px;font-size:13px;
    letter-spacing:0.2px;border-bottom:2px solid transparent;margin-bottom:-1px;
    transition:color .25s ease, border-color .25s ease;
  }
  .tab-btn.active{color:var(--gold-bright);border-color:var(--gold);}
  .tab-panel{display:none;padding-bottom:70px;}
  .tab-panel.active{display:block;}
  .tab-img{border-radius:var(--radius-m);overflow:hidden;border:1px solid var(--line);}
  .tab-img img{width:100%;}
  .spec-list{list-style:none;padding:0;margin:0;display:grid;grid-template-columns:1fr 1fr;gap:14px 40px;max-width:640px;}
  @media(max-width:560px){.spec-list{grid-template-columns:1fr;}}
  .spec-list li{display:flex;justify-content:space-between;padding-bottom:12px;border-bottom:1px solid var(--line-soft);font-size:14px;color:#CBD3E3;}
  .spec-list li b{color:var(--cream);font-weight:500;}

  .related-head{margin:0 0 30px;}
  .related-head h2{font-size:26px;color:var(--cream);font-weight:400;}

  /* ---------- footer ---------- */
  footer{background:var(--navy-0);border-top:1px solid var(--line-soft);padding:80px 0 30px;margin-top:20px;}
  .footer-cta{text-align:center;padding-bottom:70px;border-bottom:1px solid var(--line-soft);margin-bottom:60px;}
  .footer-cta h2{font-size:clamp(28px,4vw,40px);color:var(--cream);font-weight:400;max-width:620px;margin:0 auto;}
  .footer-cta p{color:var(--slate);margin:16px 0 30px;}
  .footer-grid{display:grid;grid-template-columns:1.4fr 1fr 1fr 1fr;gap:40px;}
  @media(max-width:800px){.footer-grid{grid-template-columns:1fr 1fr;}}
  @media(max-width:480px){.footer-grid{grid-template-columns:1fr;}}
  .footer-col h4{font-size:13px;color:var(--cream);letter-spacing:0.3px;margin-bottom:18px;}
  .footer-col p{color:var(--slate);font-size:13.5px;line-height:1.7;max-width:260px;}
  .footer-col ul{list-style:none;padding:0;margin:0;display:flex;flex-direction:column;gap:11px;}
  .footer-col a{color:var(--slate);font-size:13.5px;transition:color .25s ease;}
  .footer-col a:hover{color:var(--gold-bright);}
  .social-row{display:flex;gap:14px;margin-top:20px;}
  .social-row a{width:32px;height:32px;border:1px solid var(--line-soft);border-radius:50%;display:flex;align-items:center;justify-content:center;}
  .social-row svg{width:14px;height:14px;stroke:var(--slate);}
  .footer-bottom{margin-top:60px;padding-top:24px;border-top:1px solid var(--line-soft);display:flex;justify-content:space-between;flex-wrap:wrap;gap:10px;color:var(--slate-dim);font-size:12.5px;}

  /* fade-in */
  .fade-in{opacity:0;transform:translateY(16px);transition:opacity .7s ease, transform .7s ease;}
  .fade-in.visible{opacity:1;transform:translateY(0);}
  @media(prefers-reduced-motion:reduce){
    .fade-in{opacity:1;transform:none;transition:none;}
    *{scroll-behavior:auto !important;}
  }
</style>
</head>
<body>

<header id="site-header">
  <div class="wrap nav-row">
    <a href="#" class="brand" onclick="showList();window.scrollTo(0,0);">
      <span class="brand-mark"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.4"><path d="M3 11L12 4l9 7"/><path d="M5 10v9h14v-9"/></svg></span>
      Fenwick House Co.
    </a>
    <nav>
      <ul class="nav-links">
        <li><a href="#floorplans">Floor Plans</a></li>
        <li><a href="#collections">Collections</a></li>
        <li><a href="#custom">Custom Homes</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <div class="nav-right">
      <a href="#contact" class="nav-cta">Request a Consultation</a>
      <button class="hamburger" id="hamburger-btn" aria-label="Open menu">
        <svg viewBox="0 0 24 24" fill="none" stroke-width="1.6"><path d="M4 7h16M4 12h16M4 17h16"/></svg>
      </button>
    </div>
  </div>
</header>

<div class="mobile-panel" id="mobile-panel">
  <a href="#floorplans">Floor Plans</a>
  <a href="#collections">Collections</a>
  <a href="#custom">Custom Homes</a>
  <a href="#services">Services</a>
  <a href="#about">About</a>
  <a href="#contact">Contact</a>
  <a href="#contact" class="nav-cta">Request a Consultation</a>
</div>

<!-- =========== LIST VIEW =========== -->
<div id="list-view">
  <div class="hero">
    <div class="hero-inner">
      <h1>Floor Plans</h1>
      <p class="sub">Explore modern residential designs — from compact homes to expansive custom residences.</p>
      <div class="cat-row" id="cat-row"></div>
      <div class="search-wrap">
        <svg viewBox="0 0 24 24" fill="none" stroke-width="1.6"><circle cx="11" cy="11" r="7"/><path d="M21 21l-4.3-4.3"/></svg>
        <input id="search-input" type="text" placeholder="Search floor plans by name..." autocomplete="off">
      </div>
    </div>
  </div>

  <main id="floorplans">
    <div id="sections-container"></div>
  </main>
</div>

<!-- =========== DETAIL VIEW =========== -->
<div id="detail-view">
  <div class="hero" id="detail-hero">
    <div class="hero-inner" style="max-width:900px;">
    </div>
  </div>
  <div class="wrap">
    <a href="#" class="back-link" onclick="showList();return false;">
      <svg viewBox="0 0 24 24" fill="none" stroke-width="1.8"><path d="M15 18l-6-6 6-6"/></svg>
      Back to floor plans
    </a>

    <div class="detail-head">
      <h1 id="d-name"></h1>
      <div class="detail-stats" id="d-stats"></div>
    </div>

    <div class="detail-actions">
      <a class="btn btn-primary" href="#" onclick="return false;">Download Floor Plan</a>
      <a class="btn" href="#contact" onclick="showList();">Request More Information</a>
      <a class="btn" href="#contact" onclick="showList();">Customize This Plan</a>
    </div>

    <div class="tabs" id="d-tabs">
      <button class="tab-btn active" data-tab="exterior">Exterior</button>
      <button class="tab-btn" data-tab="floorplan">Floor Plans</button>
      <button class="tab-btn" data-tab="elevations">Elevations</button>
      <button class="tab-btn" data-tab="specs">Specifications</button>
    </div>

    <div class="tab-panel active" data-panel="exterior">
      <div class="tab-img"><img id="d-exterior-img" src="" alt=""></div>
    </div>
    <div class="tab-panel" data-panel="floorplan">
      <div class="tab-img" id="d-floorplan-svg-wrap"></div>
    </div>
    <div class="tab-panel" data-panel="elevations">
      <div class="tab-img"><img id="d-elevation-img" src="" alt=""></div>
    </div>
    <div class="tab-panel" data-panel="specs">
      <ul class="spec-list" id="d-specs"></ul>
    </div>

    <div class="related-head">
      <h2>Related Floor Plans</h2>
    </div>
    <div class="card-grid" id="related-grid" style="margin-bottom:80px;"></div>
  </div>
</div>

<footer id="contact">
  <div class="wrap">
    <div class="footer-cta">
      <h2>Have a vision for your home?</h2>
      <p>Let's create a plan designed around the way you live.</p>
      <a href="#contact" class="btn btn-primary">Start a Conversation</a>
    </div>
    <div class="footer-grid">
      <div class="footer-col">
        <h4>Fenwick House Co.</h4>
        <p>An architecture studio designing considered, livable homes — from compact retreats to custom residences, shaped around how people actually live.</p>
        <div class="social-row">
          <a href="#" aria-label="Instagram"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.5"><rect x="3" y="3" width="18" height="18" rx="4"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="0.8" fill="currentColor" stroke="none"/></svg></a>
          <a href="#" aria-label="Pinterest"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.5"><circle cx="12" cy="12" r="9"/><path d="M9 17c1-3 1.2-5 2-9a2.5 2.5 0 1 1 4 2c-.3 1.5-1.5 3-3 3"/></svg></a>
          <a href="#" aria-label="LinkedIn"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.5"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M8 10v6M8 7v.01M12 16v-3.5a2 2 0 0 1 4 0V16"/></svg></a>
        </div>
      </div>
      <div class="footer-col">
        <h4>Navigate</h4>
        <ul>
          <li><a href="#floorplans">Floor Plans</a></li>
          <li><a href="#custom">Custom Homes</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#about">About</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>Collections</h4>
        <ul>
          <li><a href="#compact-homes">Compact Homes</a></li>
          <li><a href="#modern-homes">Modern Homes</a></li>
          <li><a href="#luxury-homes">Luxury Homes</a></li>
          <li><a href="#pool-houses">Pool Houses &amp; Garden Suites</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>Contact</h4>
        <p>studio@fenwickhouseco.com<br>+1 (406) 555-0148<br>Bozeman, Montana</p>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 Fenwick House Co. All rights reserved.</span>
      <span>Original architectural plans, drawn and licensed in-house.</span>
    </div>
  </div>
</footer>

<script>
/* ---------------- DATA ---------------- */
const categories = [
  {key:'compact', label:'Compact Homes'},
  {key:'modern', label:'Modern Homes'},
  {key:'luxury', label:'Luxury Homes'},
  {key:'pool', label:'Pool Houses & Garden Suites'},
  {key:'commercial', label:'Commercial'},
  {key:'custom', label:'Custom Series'}
];

const sectionsMeta = [
  {id:'compact-homes', catKey:'compact', title:'Compact Homes', desc:'Efficient, thoughtfully designed homes under 1,200 sq ft.'},
  {id:'modern-homes', catKey:'modern', title:'Modern Homes', desc:'Clean lines and open living, built for contemporary family life.'},
  {id:'luxury-homes', catKey:'luxury', title:'Luxury Homes', desc:'Expansive residences with elevated finishes and generous proportions.'},
  {id:'pool-houses', catKey:'pool', title:'Pool Houses & Garden Suites', desc:'Standalone structures for guests, studios, and outdoor living.'},
  {id:'commercial-plans', catKey:'commercial', title:'Commercial Plans', desc:'Considered buildings for studios, offices, and small businesses.'}
];

const img = (id) => `https://images.unsplash.com/${id}?auto=format&fit=crop&w=1200&q=80`;

const plans = [
  {id:'willow-730', name:'Willow 730', category:'compact', sqft:730, beds:2, baths:1, stories:1, garage:0,
   desc:'A single-story retreat with an open kitchen and a covered porch, built for easy living in under 800 square feet.',
   hero:img('photo-1600585154340-be6161a56a0c'), exterior:img('photo-1600585154340-be6161a56a0c'), elevation:img('photo-1600566753086-00f18fb6b3ea')},
  {id:'meadow-800', name:'Meadow 800', category:'compact', sqft:800, beds:2, baths:1, stories:1, garage:0,
   desc:'Warm, light-filled interiors with a walk-out patio and a flexible bonus nook for a home office.',
   hero:img('photo-1600607687939-ce8a6c25118c'), exterior:img('photo-1600607687939-ce8a6c25118c'), elevation:img('photo-1600596542815-ffad4c1539a9')},
  {id:'ridge-805', name:'Ridge 805', category:'compact', sqft:805, beds:2, baths:2, stories:1, garage:0,
   desc:'Dual primary suites make this an easy fit for roommates, guests, or a growing family.',
   hero:img('photo-1600047509807-ba8f99d2cdde'), exterior:img('photo-1600047509807-ba8f99d2cdde'), elevation:img('photo-1583608205776-bfd35f0d9f83')},

  {id:'cedarline-1450', name:'Cedarline 1450', category:'modern', sqft:1450, beds:3, baths:2, stories:1, garage:1,
   desc:'An open-plan single story with vaulted ceilings and a kitchen island built for gathering.',
   hero:img('photo-1512917774080-9991f1c4c750'), exterior:img('photo-1512917774080-9991f1c4c750'), elevation:img('photo-1600585152915-d208bec867a1')},
  {id:'harlow-1620', name:'Harlow 1620', category:'modern', sqft:1620, beds:3, baths:2, stories:2, garage:2,
   desc:'A two-story layout that separates living and sleeping levels, with a private upstairs landing.',
   hero:img('photo-1523217582562-09d0def993a6'), exterior:img('photo-1523217582562-09d0def993a6'), elevation:img('photo-1613977257363-707ba9348227')},
  {id:'kestrel-1780', name:'Kestrel 1780', category:'modern', sqft:1780, beds:3, baths:2.5, stories:2, garage:2,
   desc:'A flexible loft space over the garage adapts easily into a studio, office, or guest suite.',
   hero:img('photo-1524230507669-475e94b73fc9'), exterior:img('photo-1524230507669-475e94b73fc9'), elevation:img('photo-1613490493576-7fde63acd811')},

  {id:'oakridge-2850', name:'Oakridge 2850', category:'luxury', sqft:2850, beds:4, baths:3.5, stories:2, garage:3,
   desc:'A grand entry hall leads into a great room with floor-to-ceiling glazing and a formal dining wing.',
   hero:img('photo-1600210492486-724fe5c67fb0'), exterior:img('photo-1600210492486-724fe5c67fb0'), elevation:img('photo-1600047509358-9dc75507daeb')},
  {id:'ashcombe-3400', name:'Ashcombe 3400', category:'luxury', sqft:3400, beds:5, baths:4, stories:2, garage:3,
   desc:'A resort-style primary suite and a dedicated media room round out this expansive family residence.',
   hero:img('photo-1502005229762-cf1b2da7c5d6'), exterior:img('photo-1502005229762-cf1b2da7c5d6'), elevation:img('photo-1570129477492-45c003edd2be')},
  {id:'wrenfield-3950', name:'Wrenfield 3950', category:'luxury', sqft:3950, beds:5, baths:4.5, stories:2, garage:3,
   desc:'Designed for entertaining, with an indoor-outdoor great room and a private guest wing.',
   hero:img('photo-1600566753190-17f0baa2a6c3'), exterior:img('photo-1600566753190-17f0baa2a6c3'), elevation:img('photo-1600585154340-be6161a56a0c')},

  {id:'willowbrook-480', name:'Willowbrook 480', category:'pool', sqft:480, beds:1, baths:1, stories:1, garage:0,
   desc:'A garden suite with a kitchenette and covered lounge, ideal for guests or multigenerational living.',
   hero:img('photo-1600596542815-ffad4c1539a9'), exterior:img('photo-1600596542815-ffad4c1539a9'), elevation:img('photo-1600607687939-ce8a6c25118c')},
  {id:'sablewood-620', name:'Sablewood 620', category:'pool', sqft:620, beds:1, baths:1, stories:1, garage:0,
   desc:'A pool house with a full bath and shaded outdoor kitchen, built for warm-weather living.',
   hero:img('photo-1583608205776-bfd35f0d9f83'), exterior:img('photo-1583608205776-bfd35f0d9f83'), elevation:img('photo-1600047509807-ba8f99d2cdde')},
  {id:'fernwood-540', name:'Fernwood 540', category:'pool', sqft:540, beds:1, baths:1, stories:1, garage:0,
   desc:'A quiet studio suite tucked at the edge of the garden, wired for a home office or art studio.',
   hero:img('photo-1600585152915-d208bec867a1'), exterior:img('photo-1600585152915-d208bec867a1'), elevation:img('photo-1512917774080-9991f1c4c750')},

  {id:'the-atrium-4200', name:'The Atrium 4200', category:'commercial', sqft:4200, beds:0, baths:2, stories:2, garage:0, use:'Office / Studio',
   desc:'A daylit workspace built around a central atrium, with private offices ringing an open floor.',
   hero:img('photo-1613977257363-707ba9348227'), exterior:img('photo-1613977257363-707ba9348227'), elevation:img('photo-1523217582562-09d0def993a6')},
  {id:'harborline-5600', name:'Harborline 5600', category:'commercial', sqft:5600, beds:0, baths:3, stories:1, garage:0, use:'Retail / Showroom',
   desc:'A single-level showroom with generous street-facing glazing and a flexible back-of-house.',
   hero:img('photo-1613490493576-7fde63acd811'), exterior:img('photo-1613490493576-7fde63acd811'), elevation:img('photo-1524230507669-475e94b73fc9')},
  {id:'the-foundry-3100', name:'The Foundry 3100', category:'commercial', sqft:3100, beds:0, baths:2, stories:1, garage:0, use:'Studio / Workshop',
   desc:'A converted-barn aesthetic with tall ceilings, built for a maker studio or small business.',
   hero:img('photo-1600047509358-9dc75507daeb'), exterior:img('photo-1600047509358-9dc75507daeb'), elevation:img('photo-1600210492486-724fe5c67fb0')},
];

/* ---------------- ICONS ---------------- */
const icoBed = `<svg viewBox="0 0 24 24" fill="none" stroke-width="1.6"><path d="M3 18v-6a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v6"/><path d="M3 18v2M21 18v2"/><path d="M3 12V8a1 1 0 0 1 1-1h4a1 1 0 0 1 1 1v2"/><path d="M13 10h6"/></svg>`;
const icoBath = `<svg viewBox="0 0 24 24" fill="none" stroke-width="1.6"><path d="M4 12h16v3a4 4 0 0 1-4 4H8a4 4 0 0 1-4-4v-3z"/><path d="M6 12V6a2 2 0 0 1 3-1.7"/><path d="M4 19v1.5M18 19v1.5"/></svg>`;
const icoStory = `<svg viewBox="0 0 24 24" fill="none" stroke-width="1.6"><rect x="4" y="4" width="16" height="7"/><rect x="4" y="13" width="16" height="7"/></svg>`;
const icoGarage = `<svg viewBox="0 0 24 24" fill="none" stroke-width="1.6"><path d="M3 10l9-6 9 6"/><path d="M5 10v10h14V10"/><path d="M9 20v-6h6v6"/></svg>`;

/* ---------------- RENDER: hero categories ---------------- */
const catRow = document.getElementById('cat-row');
categories.forEach(c=>{
  const b = document.createElement('button');
  b.className = 'cat-btn';
  b.textContent = c.label;
  b.dataset.key = c.key;
  b.addEventListener('click', ()=>{
    document.querySelectorAll('.cat-btn').forEach(x=>x.classList.remove('active'));
    b.classList.add('active');
    if(c.key==='custom'){
      document.getElementById('contact').scrollIntoView({behavior:'smooth'});
      return;
    }
    const sec = sectionsMeta.find(s=>s.catKey===c.key);
    if(sec){
      document.getElementById(sec.id).scrollIntoView({behavior:'smooth', block:'start'});
    }
  });
  catRow.appendChild(b);
});

/* ---------------- RENDER: sections & cards ---------------- */
function cardHTML(p){
  const bedBath = p.category === 'commercial'
    ? `<span>${p.use}</span><span>${icoStory}${p.stories} ${p.stories>1?'Stories':'Story'}</span>`
    : `<span>${icoBed}${p.beds} Bed${p.beds!==1?'s':''}</span><span>${icoBath}${p.baths} Bath${p.baths!==1?'s':''}</span><span>${icoStory}${p.stories} ${p.stories>1?'Stories':'Story'}</span>${p.garage?`<span>${icoGarage}${p.garage} Car</span>`:''}`;
  return `
  <div class="plan-card fade-in" data-name="${p.name.toLowerCase()}" data-desc="${p.desc.toLowerCase()}" data-cat="${p.category}" data-sqft="${p.sqft}">
    <a href="#" onclick="openDetail('${p.id}');return false;">
      <div class="card-img"><img src="${p.hero}" alt="${p.name}" loading="lazy">
        <span class="badge">${p.sqft.toLocaleString()} sq ft</span>
      </div>
    </a>
    <div class="card-body">
      <h3>${p.name}</h3>
      <div class="meta-row">${bedBath}</div>
      <p class="card-desc">${p.desc}</p>
      <a href="#" class="view-link" onclick="openDetail('${p.id}');return false;">View Plan →</a>
    </div>
  </div>`;
}

const sectionsContainer = document.getElementById('sections-container');
sectionsMeta.forEach(sec=>{
  const secPlans = plans.filter(p=>p.category===sec.catKey);
  const el = document.createElement('section');
  el.className = 'plan-section';
  el.id = sec.id;
  el.innerHTML = `
    <div class="wrap">
      <div class="section-head fade-in">
        <h2>${sec.title}</h2>
        <p>${sec.desc}</p>
      </div>
      <div class="divider"></div>
      <div class="card-grid" data-section="${sec.catKey}">
        ${secPlans.map(cardHTML).join('')}
      </div>
    </div>`;
  sectionsContainer.appendChild(el);
});

/* ---------------- SEARCH ---------------- */
const searchInput = document.getElementById('search-input');
searchInput.addEventListener('input', ()=>{
  const q = searchInput.value.trim().toLowerCase();
  let anyVisible = false;
  document.querySelectorAll('.card-grid[data-section]').forEach(grid=>{
    let visibleInGrid = 0;
    grid.querySelectorAll('.plan-card').forEach(card=>{
      const match = !q || card.dataset.name.includes(q) || card.dataset.desc.includes(q) || card.dataset.cat.includes(q) || card.dataset.sqft.includes(q);
      card.classList.toggle('hidden', !match);
      if(match){visibleInGrid++; anyVisible=true;}
    });
    const section = grid.closest('.plan-section');
    section.style.display = visibleInGrid===0 && q ? 'none' : '';
    let noMsg = grid.querySelector('.no-results');
    if(visibleInGrid===0 && q){
      section.style.display='';
      grid.querySelectorAll('.plan-card').forEach(c=>c.classList.add('hidden'));
      if(!noMsg){
        noMsg = document.createElement('div');
        noMsg.className='no-results';
        grid.appendChild(noMsg);
      }
      noMsg.textContent = 'No floor plans found. Try another search.';
    } else if(noMsg){
      noMsg.remove();
    }
  });
});

/* ---------------- DETAIL VIEW ---------------- */
function specsFor(p){
  const rows = [
    ['Square Footage', p.sqft.toLocaleString()+' sq ft'],
    ['Stories', p.stories],
  ];
  if(p.category==='commercial'){
    rows.splice(1,0,['Use', p.use]);
    rows.push(['Restrooms', p.baths]);
  } else {
    rows.splice(1,0,['Bedrooms', p.beds]);
    rows.splice(2,0,['Bathrooms', p.baths]);
    rows.push(['Garage', p.garage ? p.garage+' Car' : 'None']);
  }
  rows.push(['Foundation', 'Slab-on-grade']);
  rows.push(['Roof Pitch', '6:12']);
  return rows;
}

function floorplanSVG(p){
  return `<svg viewBox="0 0 600 420" xmlns="http://www.w3.org/2000/svg" style="background:#0E1830;width:100%;height:auto;">
    <rect x="30" y="30" width="540" height="360" fill="none" stroke="#96A5C2" stroke-width="1.5"/>
    <line x1="30" y1="180" x2="330" y2="180" stroke="#96A5C2" stroke-width="1"/>
    <line x1="330" y1="30" x2="330" y2="390" stroke="#96A5C2" stroke-width="1"/>
    <line x1="330" y1="260" x2="570" y2="260" stroke="#96A5C2" stroke-width="1"/>
    <line x1="450" y1="30" x2="450" y2="260" stroke="#96A5C2" stroke-width="1"/>
    <text x="150" y="110" fill="#C4A468" font-size="13" font-family="Inter" text-anchor="middle">Living Room</text>
    <text x="150" y="290" fill="#C4A468" font-size="13" font-family="Inter" text-anchor="middle">Kitchen / Dining</text>
    <text x="390" y="150" fill="#C4A468" font-size="13" font-family="Inter" text-anchor="middle">Primary Suite</text>
    <text x="510" y="150" fill="#C4A468" font-size="13" font-family="Inter" text-anchor="middle">Bedroom</text>
    <text x="450" y="330" fill="#C4A468" font-size="13" font-family="Inter" text-anchor="middle">${p.category==='commercial' ? 'Open Floor' : 'Bath / Utility'}</text>
    <text x="300" y="410" fill="#6E7C97" font-size="11" font-family="Inter" text-anchor="middle">Schematic layout — not to scale</text>
  </svg>`;
}

function openDetail(id){
  const p = plans.find(x=>x.id===id);
  if(!p) return;

  document.getElementById('list-view').style.display='none';
  const dv = document.getElementById('detail-view');
  dv.classList.add('active');
  window.scrollTo(0,0);

  document.getElementById('detail-hero').style.backgroundImage =
    `linear-gradient(180deg, rgba(6,10,18,0.35) 0%, rgba(7,12,22,0.7) 60%, rgba(8,14,26,1) 100%), url('${p.hero}')`;
  document.getElementById('detail-hero').querySelector('.hero-inner').innerHTML = `<h1 style="font-size:clamp(34px,5.5vw,54px);">${p.name}</h1>`;

  document.getElementById('d-name').textContent = p.name;

  const statHTML = p.category==='commercial'
    ? `<div class="stat"><div class="num">${p.sqft.toLocaleString()}</div><div class="lab">Sq Ft</div></div>
       <div class="stat"><div class="num">${p.use}</div><div class="lab">Use</div></div>
       <div class="stat"><div class="num">${p.stories}</div><div class="lab">Stories</div></div>`
    : `<div class="stat"><div class="num">${p.sqft.toLocaleString()}</div><div class="lab">Sq Ft</div></div>
       <div class="stat"><div class="num">${p.beds}</div><div class="lab">Bedrooms</div></div>
       <div class="stat"><div class="num">${p.baths}</div><div class="lab">Bathrooms</div></div>
       <div class="stat"><div class="num">${p.stories}</div><div class="lab">Stories</div></div>
       <div class="stat"><div class="num">${p.garage||0}</div><div class="lab">Car Garage</div></div>`;
  document.getElementById('d-stats').innerHTML = statHTML;

  document.getElementById('d-exterior-img').src = p.exterior;
  document.getElementById('d-exterior-img').alt = p.name + ' exterior';
  document.getElementById('d-elevation-img').src = p.elevation;
  document.getElementById('d-elevation-img').alt = p.name + ' elevation';
  document.getElementById('d-floorplan-svg-wrap').innerHTML = floorplanSVG(p);

  document.getElementById('d-specs').innerHTML = specsFor(p).map(([k,v])=>`<li><span>${k}</span><b>${v}</b></li>`).join('');

  // reset tabs
  document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
  document.querySelector('.tab-btn[data-tab="exterior"]').classList.add('active');
  document.querySelectorAll('.tab-panel').forEach(pnl=>pnl.classList.remove('active'));
  document.querySelector('.tab-panel[data-panel="exterior"]').classList.add('active');

  // related plans
  const related = plans.filter(x=>x.category===p.category && x.id!==p.id).slice(0,3);
  document.getElementById('related-grid').innerHTML = related.map(cardHTML).join('');
}

function showList(){
  document.getElementById('detail-view').classList.remove('active');
  document.getElementById('list-view').style.display='';
  window.scrollTo(0,0);
}

document.getElementById('d-tabs').addEventListener('click', e=>{
  const btn = e.target.closest('.tab-btn');
  if(!btn) return;
  document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  const tab = btn.dataset.tab;
  document.querySelectorAll('.tab-panel').forEach(p=>p.classList.toggle('active', p.dataset.panel===tab));
});

/* ---------------- HEADER SCROLL ---------------- */
const headerEl = document.getElementById('site-header');
window.addEventListener('scroll', ()=>{
  headerEl.classList.toggle('scrolled', window.scrollY > 40);
});

/* ---------------- MOBILE MENU ---------------- */
const hamburgerBtn = document.getElementById('hamburger-btn');
const mobilePanel = document.getElementById('mobile-panel');
hamburgerBtn.addEventListener('click', ()=>mobilePanel.classList.toggle('open'));
mobilePanel.querySelectorAll('a').forEach(a=>a.addEventListener('click', ()=>mobilePanel.classList.remove('open')));

/* ---------------- FADE-IN ON SCROLL ---------------- */
const io = new IntersectionObserver((entries)=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add('visible');
      io.unobserve(entry.target);
    }
  });
},{threshold:0.15});
document.querySelectorAll('.fade-in').forEach(el=>io.observe(el));
</script>
</body>
</html>
