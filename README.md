<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rozan Hakim Abyandhono — CV</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#F7F5EF;
    --ink:#1C2321;
    --sub:#5B655F;
    --accent:#2F6F5E;
    --accent-soft:#2F6F5E1a;
    --gold:#B98A2E;
    --line:#DAD5C8;
    --card:#FFFFFF;
  }
  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --bg:#14181A; --ink:#EDEAE1; --sub:#A6ADA6; --accent:#6FBFA6;
      --accent-soft:#6FBFA61a; --gold:#D8B15C; --line:#2C3330; --card:#1B211F;
    }
  }
  :root[data-theme="dark"]{
    --bg:#14181A; --ink:#EDEAE1; --sub:#A6ADA6; --accent:#6FBFA6;
    --accent-soft:#6FBFA61a; --gold:#D8B15C; --line:#2C3330; --card:#1B211F;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--bg);
    color:var(--ink);
    font-family:'Inter', system-ui, -apple-system, sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    transition:background .2s ease, color .2s ease;
  }
  a{color:var(--accent);}

  /* progress bar */
  #progress{
    position:fixed; top:0; left:0; height:3px; width:0%;
    background:var(--gold); z-index:60; transition:width .1s linear;
  }

  /* top bar */
  .topbar{
    position:sticky; top:0; z-index:50;
    display:flex; align-items:center; justify-content:space-between;
    padding:14px 24px;
    background:color-mix(in srgb, var(--bg) 88%, transparent);
    backdrop-filter:blur(8px);
    border-bottom:1px solid var(--line);
  }
  .topbar .brand{ font-family:'Fraunces', serif; font-size:1.05rem; font-weight:600; }
  .topbar nav{ display:flex; gap:4px; }
  .topbar nav a{
    text-decoration:none; color:var(--sub); font-size:0.86rem;
    padding:7px 12px; border-radius:20px; transition:.15s ease;
  }
  .topbar nav a.active{ color:var(--ink); background:var(--accent-soft); }
  .topbar nav a:hover{ color:var(--ink); }
  .controls{ display:flex; align-items:center; gap:8px; }
  .icon-btn{
    width:36px; height:36px; border-radius:50%;
    border:1px solid var(--line); background:var(--card);
    color:var(--ink); cursor:pointer; font-size:1rem;
    display:flex; align-items:center; justify-content:center;
    transition:.15s ease;
  }
  .icon-btn:hover{ border-color:var(--accent); color:var(--accent); }
  .dl-btn{
    display:flex; align-items:center; gap:6px;
    border:1px solid var(--accent); background:transparent;
    color:var(--accent); border-radius:20px; padding:7px 14px;
    font-size:0.86rem; font-weight:600; cursor:pointer; font-family:inherit;
    transition:.15s ease;
  }
  .dl-btn:hover{ background:var(--accent); color:var(--bg); }
  .dl-btn[disabled]{ opacity:.4; cursor:not-allowed; }

  @media (max-width:640px){
    .topbar nav{ display:none; }
  }

  .wrap{ max-width:760px; margin:0 auto; padding:56px 24px 100px; }

  header.hero{ margin-bottom:56px; }
  .eyebrow{ color:var(--gold); font-size:0.9rem; margin:0 0 10px; }
  h1{
    font-family:'Fraunces', serif; font-weight:500;
    font-size:clamp(2.2rem, 6vw, 3.2rem); line-height:1.05;
    margin:0 0 14px; letter-spacing:-0.01em;
  }
  .role{ font-size:1.1rem; color:var(--sub); margin:0 0 22px; max-width:46ch; }
  .contact{ display:flex; flex-wrap:wrap; gap:6px 18px; font-size:0.92rem; color:var(--sub); }
  .contact a{ color:var(--sub); text-decoration:none; border-bottom:1px solid var(--line); padding-bottom:1px; }
  .contact a:hover{ color:var(--accent); border-color:var(--accent); }

  section{ margin-bottom:52px; scroll-margin-top:78px; }
  h2{
    font-family:'Fraunces', serif; font-weight:500; font-size:1.3rem;
    margin:0 0 18px; padding-bottom:10px; border-bottom:1px solid var(--line);
  }
  p.lede{ max-width:64ch; }

  .edu-row{ display:flex; justify-content:space-between; gap:16px; padding:10px 0; border-bottom:1px dashed var(--line); }
  .edu-row:last-child{ border-bottom:none; }
  .edu-row .name{ font-weight:600; }
  .edu-row .meta{ color:var(--sub); font-size:0.9rem; }
  .edu-row .date{ color:var(--sub); font-size:0.9rem; white-space:nowrap; }

  .timeline{ position:relative; padding-left:26px; }
  .timeline::before{ content:""; position:absolute; left:6px; top:10px; bottom:10px; width:1px; background:var(--line); }
  .tl-item{ position:relative; padding-bottom:14px; }
  .tl-item::before{
    content:""; position:absolute; left:-26px; top:14px; width:9px; height:9px;
    border-radius:50%; background:var(--accent); border:2px solid var(--bg); box-shadow:0 0 0 1px var(--accent);
  }
  .tl-head{
    display:flex; align-items:flex-start; justify-content:space-between; gap:10px;
    cursor:pointer; padding:8px 0; user-select:none;
  }
  .tl-head-left{ display:flex; gap:10px; align-items:flex-start; }
  .chev{ color:var(--sub); transition:transform .2s ease; margin-top:3px; flex:none; }
  .tl-item.open .chev{ transform:rotate(90deg); color:var(--accent); }
  .tl-role{ font-weight:600; }
  .tl-org{ color:var(--sub); font-size:0.92rem; }
  .tl-date{ color:var(--sub); font-size:0.83rem; white-space:nowrap; }
  .tl-body{
    max-height:0; overflow:hidden; transition:max-height .25s ease;
    padding-left:0;
  }
  .tl-item.open .tl-body{ max-height:200px; }
  .tl-body ul{ margin:2px 0 12px; padding-left:18px; }
  .tl-body li{ margin-bottom:4px; color:var(--ink); font-size:0.95rem; }

  .skills-grid{ display:grid; grid-template-columns:1fr 1fr; gap:18px 28px; }
  @media (max-width:560px){ .skills-grid{ grid-template-columns:1fr; } }
  .skill-group h3{ font-size:0.78rem; color:var(--gold); margin:0 0 10px; font-weight:600; }
  .tags{ display:flex; flex-wrap:wrap; gap:7px; }
  .tag{
    font-size:0.82rem; padding:5px 11px; border-radius:20px;
    border:1px solid var(--line); color:var(--ink); background:var(--card);
    transition:.15s ease; cursor:default;
  }
  .tag:hover{ border-color:var(--accent); color:var(--accent); transform:translateY(-1px); }

  footer{ border-top:1px solid var(--line); padding-top:24px; color:var(--sub); font-size:0.85rem; }

  ::selection{ background:var(--gold); color:#1C2321; }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    *{ transition:none !important; }
  }
</style>
</head>
<body>
<div id="progress"></div>

<div class="topbar">
  <span class="brand">RHA</span>
  <nav id="sectionNav">
    <a href="#profile" data-target="profile">Profile</a>
    <a href="#education" data-target="education">Education</a>
    <a href="#experience" data-target="experience">Experience</a>
    <a href="#skills" data-target="skills">Skills</a>
  </nav>
  <div class="controls">
    <button class="dl-btn" id="downloadBtn">⬇ Download</button>
    <button class="icon-btn" id="themeToggle" aria-label="Toggle theme">🌙</button>
  </div>
</div>

<div class="wrap">

  <header class="hero">
    <p class="eyebrow">Curriculum Vitae</p>
    <h1>Rozan Hakim<br>Abyandhono</h1>
    <p class="role">Informatics Engineering student at ITS, with a track record of organizing and running student events.</p>
    <div class="contact">
      <span>+62 857-1550-9411</span>
      <a href="mailto:rozanhakim15@gmail.com">rozanhakim15@gmail.com</a>
      <a href="https://linkedin.com/in/rozanhakimabyandhono" target="_blank" rel="noopener">linkedin.com/in/rozanhakimabyandhono</a>
    </div>
  </header>

  <section id="profile">
    <h2>Profile</h2>
    <p class="lede">First-year Informatics Engineering student at Institut Teknologi Sepuluh Nopember (ITS). Built strong organizational and teamwork skills through active involvement in student committees throughout senior high school. Genuinely interested in informatics as well as management and leadership — enthusiastic, adaptable, and committed to continuous learning.</p>
  </section>

  <section id="education">
    <h2>Education</h2>
    <div class="edu-row">
      <div>
        <div class="name">Institut Teknologi Sepuluh Nopember (ITS)</div>
        <div class="meta">B.S. Informatics Engineering · TOEFL ITP 540</div>
      </div>
      <div class="date">2025 – Present</div>
    </div>
    <div class="edu-row">
      <div><div class="name">SMA Syafana Islamic School</div></div>
      <div class="date">2023 – 2025</div>
    </div>
  </section>

  <section id="experience">
    <h2>Organizational &amp; Event Experience</h2>
    <p style="color:var(--sub); font-size:0.85rem; margin:-8px 0 16px;">Tap an entry to see details</p>
    <div class="timeline" id="timeline">

      <div class="tl-item">
        <div class="tl-head">
          <div class="tl-head-left">
            <span class="chev">▸</span>
            <div>
              <div class="tl-role">Artistic Director (Set &amp; Props)</div>
              <div class="tl-org">Teater Tanah Air Beta, SMA Syafana Islamic School</div>
            </div>
          </div>
          <div class="tl-date">May 2025</div>
        </div>
        <div class="tl-body">
          <ul>
            <li>Planned, sourced, and managed props and stage elements required for the production.</li>
            <li>Coordinated with multiple parties involved in preparing and using production properties.</li>
          </ul>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-head">
          <div class="tl-head-left">
            <span class="chev">▸</span>
            <div>
              <div class="tl-role">Entertainment Division</div>
              <div class="tl-org">Syafana Tangerang 10K Run</div>
            </div>
          </div>
          <div class="tl-date">Feb 2025</div>
        </div>
        <div class="tl-body">
          <ul>
            <li>Helped design an energetic, engaging atmosphere for participants during the race event.</li>
          </ul>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-head">
          <div class="tl-head-left">
            <span class="chev">▸</span>
            <div>
              <div class="tl-role">Actor</div>
              <div class="tl-org">Teater Tanah Air Beta, SMA Syafana Islamic School</div>
            </div>
          </div>
          <div class="tl-date">Aug 2024</div>
        </div>
        <div class="tl-body">
          <ul>
            <li>Portrayed a character and helped bring the story to life through stage performance.</li>
          </ul>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-head">
          <div class="tl-head-left">
            <span class="chev">▸</span>
            <div>
              <div class="tl-role">Documentation Division</div>
              <div class="tl-org">Syafana Festival 2024</div>
            </div>
          </div>
          <div class="tl-date">Jan – Feb 2024</div>
        </div>
        <div class="tl-body">
          <ul>
            <li>Documented event activities through photography and videography.</li>
            <li>Managed and organized storage of photo and video files for the event.</li>
          </ul>
        </div>
      </div>

    </div>
  </section>

  <section id="skills">
    <h2>Skills</h2>
    <div class="skills-grid">
      <div class="skill-group">
        <h3>Core skills</h3>
        <div class="tags">
          <span class="tag">Team management</span><span class="tag">Coordination</span>
          <span class="tag">Critical thinking</span><span class="tag">Problem solving</span>
          <span class="tag">Works well under pressure</span>
        </div>
      </div>
      <div class="skill-group">
        <h3>Software</h3>
        <div class="tags">
          <span class="tag">Word</span><span class="tag">Excel</span><span class="tag">PowerPoint</span>
          <span class="tag">Google Docs</span><span class="tag">Sheets</span><span class="tag">Slides</span>
          <span class="tag">Drive</span>
        </div>
      </div>
      <div class="skill-group">
        <h3>Photography</h3>
        <div class="tags"><span class="tag">Camera</span><span class="tag">Smartphone photography</span></div>
      </div>
      <div class="skill-group">
        <h3>Editing tools</h3>
        <div class="tags"><span class="tag">Adobe Lightroom</span><span class="tag">CapCut</span></div>
      </div>
    </div>
  </section>

  <footer>Rozan Hakim Abyandhono · Surabaya, Indonesia</footer>
</div>

<script>
  // ---- scroll progress bar ----
  const progress = document.getElementById('progress');
  function updateProgress(){
    const h = document.documentElement;
    const scrolled = h.scrollTop;
    const max = h.scrollHeight - h.clientHeight;
    progress.style.width = (max > 0 ? (scrolled/max)*100 : 0) + '%';
  }
  document.addEventListener('scroll', updateProgress, { passive:true });
  updateProgress();

  // ---- scrollspy nav ----
  const navLinks = [...document.querySelectorAll('#sectionNav a')];
  const sections = navLinks.map(a => document.getElementById(a.dataset.target));
  const spy = new IntersectionObserver((entries)=>{
    entries.forEach(entry=>{
      const link = navLinks.find(a => a.dataset.target === entry.target.id);
      if(!link) return;
      if(entry.isIntersecting) {
        navLinks.forEach(a=>a.classList.remove('active'));
        link.classList.add('active');
      }
    });
  }, { rootMargin: '-40% 0px -55% 0px', threshold: 0 });
  sections.forEach(s => s && spy.observe(s));

  // ---- theme toggle ----
  const themeBtn = document.getElementById('themeToggle');
  function applyTheme(t){
    if(t === 'light'){ document.documentElement.setAttribute('data-theme','light'); themeBtn.textContent='☀️'; }
    else if(t === 'dark'){ document.documentElement.setAttribute('data-theme','dark'); themeBtn.textContent='🌙'; }
    else { document.documentElement.removeAttribute('data-theme'); themeBtn.textContent='🌓'; }
  }
  let saved = null;
  try{ saved = localStorage.getItem('rha-cv-theme'); }catch(e){}
  applyTheme(saved);
  themeBtn.addEventListener('click', ()=>{
    const current = document.documentElement.getAttribute('data-theme');
    const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
    const effectiveDark = current ? current === 'dark' : prefersDark;
    const next = effectiveDark ? 'light' : 'dark';
    applyTheme(next);
    try{ localStorage.setItem('rha-cv-theme', next); }catch(e){}
  });

  // ---- expandable timeline ----
  document.querySelectorAll('.tl-head').forEach(head=>{
    head.addEventListener('click', ()=>{
      head.closest('.tl-item').classList.toggle('open');
    });
  });
  // open the most recent entry by default
  document.querySelector('.tl-item')?.classList.add('open');

  // ---- download CV as HTML ----
  const dlBtn = document.getElementById('downloadBtn');
  dlBtn.addEventListener('click', async ()=>{
    try{
      const downloads = await claude.use('downloads');
      if(!downloads){ dlBtn.textContent = 'Unavailable'; setTimeout(()=>dlBtn.textContent='⬇ Download', 1800); return; }
      const html = '<!DOCTYPE html>\n' + document.documentElement.outerHTML;
      await downloads.save({ filename: 'Rozan_Hakim_Abyandhono_CV.html', data: html });
    }catch(e){
      dlBtn.textContent = 'Couldn\u2019t save';
      setTimeout(()=>dlBtn.textContent='⬇ Download', 1800);
    }
  });
</script>
</body>
</html>

