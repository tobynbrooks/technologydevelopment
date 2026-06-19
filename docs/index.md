<style>
  :root {
    --ink: #0f1222;
    --muted: #6b7180;
    --line: #ececf1;
  }
  .hero-badge {
    display: inline-block;
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #5b54e6;
    background: linear-gradient(90deg, #eef0ff, #f3eeff);
    padding: 0.32rem 0.8rem;
    border-radius: 999px;
  }
  .hero-title {
    margin: 0.9rem 0 0.4rem;
    font-size: 2.1rem;
    font-weight: 700;
    letter-spacing: -0.02em;
    color: var(--ink);
  }
  .hero-sub {
    margin: 0 0 2rem;
    color: var(--muted);
    font-size: 1.05rem;
    max-width: 46rem;
  }
  .pillars-title {
    margin: 0 0 1.1rem;
    font-size: 1.5rem;
    font-weight: 700;
    letter-spacing: -0.01em;
    color: var(--ink);
  }
  .pillars {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.1rem;
    margin-bottom: 0;
  }
  .connectors {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.1rem;
    height: 30px;
  }
  .conn { position: relative; }
  .conn::before {
    content: "";
    position: absolute;
    top: 0; left: 50%; transform: translateX(-50%);
    width: 9px; height: 9px; border-radius: 50%;
    background: var(--accent);
  }
  .conn::after {
    content: "";
    position: absolute;
    top: 4px; left: 50%; transform: translateX(-50%);
    width: 2px; height: 30px;
    background: var(--accent);
    opacity: 0.45;
  }
  @media (max-width: 820px) {
    .pillars { grid-template-columns: 1fr; }
    .connectors { display: none; }
  }
  .card {
    position: relative;
    background: #fff;
    border: 1px solid var(--line);
    border-radius: 18px;
    padding: 1.6rem 1.5rem;
    overflow: hidden;
    box-shadow: 0 6px 18px rgba(16,18,34,0.08);
    transition: transform .18s ease, box-shadow .18s ease;
  }
  .card:hover {
    transform: translateY(-3px);
    box-shadow: 0 16px 38px rgba(16,18,34,0.13);
  }
  .card::before {
    content: "";
    position: absolute;
    inset: 0 0 auto 0;
    height: 4px;
    background: var(--accent);
  }
  .card .top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1.1rem;
  }
  .card .icon {
    width: 46px; height: 46px;
    border-radius: 13px;
    background: var(--accent-soft);
    display: flex; align-items: center; justify-content: center;
  }
  .card .icon svg { width: 23px; height: 23px; fill: none; stroke: var(--accent); stroke-width: 2; stroke-linecap: round; stroke-linejoin: round; }
  .card .num {
    font-size: 0.78rem;
    font-weight: 700;
    color: var(--accent);
    background: var(--accent-soft);
    border-radius: 999px;
    padding: 0.18rem 0.6rem;
  }
  .card h3 {
    margin: 0 0 0.5rem;
    font-size: 1.12rem;
    font-weight: 700;
    color: var(--ink);
    letter-spacing: -0.01em;
  }
  .card p { color: var(--muted); font-size: 0.92rem; line-height: 1.55; margin: 0 0 0.9rem; }
  .card .kicker {
    margin: 0;
    font-size: 0.85rem;
    font-weight: 700;
    color: var(--accent);
  }
  .c1 { --accent:#5b54e6; --accent-soft:#eeecff; }
  .c2 { --accent:#0ea5a3; --accent-soft:#e3f7f5; }
  .c3 { --accent:#e0791b; --accent-soft:#fdeede; }

  .platform {
    --accent:#5b54e6; --accent-soft:#eeecff;
    position: relative;
    border-radius: 18px;
    padding: 1.7rem 1.8rem;
    background: linear-gradient(105deg, #f1efff 0%, #f3f4fb 45%, #fdf1e7 100%);
    border: 1px solid var(--line);
    overflow: hidden;
    display: flex;
    align-items: center;
    gap: 1.3rem;
    box-shadow: 0 6px 18px rgba(16,18,34,0.08);
  }
  .platform::before {
    content: "";
    position: absolute;
    inset: 0 0 auto 0;
    height: 4px;
    background: linear-gradient(90deg, #5b54e6 0%, #0ea5a3 50%, #e0791b 100%);
  }
  .platform .icon {
    flex: 0 0 auto;
    width: 50px; height: 50px;
    border-radius: 14px;
    background: var(--accent-soft);
    display: flex; align-items: center; justify-content: center;
  }
  .platform .icon svg { width: 25px; height: 25px; fill: none; stroke: var(--accent); stroke-width: 2; stroke-linecap: round; stroke-linejoin: round; }
  .platform .ptag {
    font-size: 0.7rem; font-weight: 700; letter-spacing: 0.14em; text-transform: uppercase;
    color: var(--accent); margin: 0 0 0.25rem;
  }
  .platform h3 { margin: 0 0 0.35rem; font-size: 1.2rem; font-weight: 700; color: var(--ink); letter-spacing: -0.01em; }
  .platform p { margin: 0; color: var(--muted); font-size: 0.92rem; line-height: 1.55; max-width: 34rem; }
  .platform .tags {
    margin-left: auto;
    flex: 0 0 auto;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    align-items: flex-end;
  }
  .platform .tag {
    background: #fff;
    border: 1px solid var(--line);
    border-radius: 999px;
    padding: 0.34rem 0.85rem;
    font-size: 0.8rem;
    font-weight: 600;
    color: var(--ink);
    white-space: nowrap;
    box-shadow: 0 1px 2px rgba(16,18,34,0.05);
  }
  @media (max-width: 820px) {
    .platform { flex-wrap: wrap; }
    .platform .tags { flex-direction: row; flex-wrap: wrap; margin-left: 0; }
  }

  .section-title {
    margin: 0 0 0.4rem;
    font-size: 1.5rem;
    font-weight: 700;
    letter-spacing: -0.01em;
    color: var(--ink);
  }
  .section-sub {
    margin: 0 0 1.4rem;
    color: var(--muted);
    font-size: 1rem;
    max-width: 46rem;
  }
  .contributors {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.1rem;
  }
  .person {
    background: #fff;
    border: 1px solid var(--line);
    border-radius: 16px;
    padding: 1.4rem 1.4rem;
    box-shadow: 0 6px 18px rgba(16,18,34,0.08);
    transition: transform .18s ease, box-shadow .18s ease;
  }
  .person:hover {
    transform: translateY(-3px);
    box-shadow: 0 16px 38px rgba(16,18,34,0.13);
  }
  .person .avatar {
    width: 48px; height: 48px;
    border-radius: 50%;
    background: linear-gradient(135deg, #eeecff, #fdf1e7);
    display: flex; align-items: center; justify-content: center;
    font-weight: 700;
    color: #5b54e6;
    margin-bottom: 0.9rem;
  }
  .person h3 {
    margin: 0 0 0.2rem;
    font-size: 1.05rem;
    font-weight: 700;
    color: var(--ink);
    letter-spacing: -0.01em;
  }
  .person .role {
    margin: 0 0 0.7rem;
    font-size: 0.8rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: #5b54e6;
  }
  .person p { margin: 0; color: var(--muted); font-size: 0.92rem; line-height: 1.55; }
  @media (max-width: 820px) {
    .contributors { grid-template-columns: 1fr; }
  }

  .next-title {
    margin: 0 0 1.1rem;
    font-size: 1.5rem;
    font-weight: 700;
    letter-spacing: -0.01em;
    color: var(--ink);
  }
  .next {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 0.9rem;
  }
  .next a {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 0.8rem;
    background: #fff;
    border: 1px solid var(--line);
    border-left: 3px solid var(--accent);
    border-radius: 14px;
    padding: 1rem 1.1rem;
    text-decoration: none;
    box-shadow: 0 4px 12px rgba(16,18,34,0.06);
    transition: transform .18s ease, box-shadow .18s ease, border-color .18s ease;
  }
  .next a:hover {
    transform: translateY(-2px);
    box-shadow: 0 12px 26px rgba(16,18,34,0.12);
  }
  .next .label {
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
    margin: 0 0 0.2rem;
  }
  .next .name {
    font-size: 0.98rem;
    font-weight: 700;
    color: var(--ink);
    letter-spacing: -0.01em;
  }
  .next .arrow {
    flex: 0 0 auto;
    color: var(--accent);
    font-size: 1.1rem;
    line-height: 1;
    transition: transform .18s ease;
  }
  .next a:hover .arrow { transform: translateX(3px); }
  .next .n1 { --accent:#5b54e6; }
  .next .n2 { --accent:#0ea5a3; }
  .next .n3 { --accent:#e0791b; }
  .next .n4 { --accent:#5b54e6; }
  @media (max-width: 820px) {
    .next { grid-template-columns: 1fr 1fr; }
  }
  @media (max-width: 520px) {
    .next { grid-template-columns: 1fr; }
  }
  h1#overview-and-investment-thesis { display: none; }
</style>

# Autopic Technology Ltd



<p class="hero-sub">This website showcases the technology layer behind the thesis you have seen: the data and operations platform we are building on top of every garage we acquire. Everything in the site is already built and repositries are linked at the bottom of the pages.
<p>In the future this technology will be useful to more people than just our own network.  It will either offer demand to a broader garage network than our own, or become an operating system for our peers.
<p>It targets the parts of the value chain with the greatest upside, some with a direct, measurable impact on profit, others, like customer lifetime value, that compound more slowly. 
<p>The pages here set out the technical and strategic detail behind three pillars, each optimised through one technology led approach on a single data foundation.</p>

<h2 class="pillars-title">Three pillars and one foundation layer</h2>

<div class="pillars">

  <div class="card c1">
    <div class="top">
      <div class="icon"><svg viewBox="0 0 24 24"><path d="M4 19V5M4 19h16M8 16v-5M13 16V8M18 16v-3"/></svg></div>
      <span class="num">01</span>
    </div>
    <h3>Productive Work</h3>
    <p>Remove non-productive time so technicians spend more hours on billable work.</p>
    <p class="kicker">More output, same labour base.</p>
  </div>

  <div class="card c2">
    <div class="top">
      <div class="icon"><svg viewBox="0 0 24 24"><path d="M6 3h9l3 3v15H6zM9 9h6M9 13h6M9 17h4"/></svg></div>
      <span class="num">02</span>
    </div>
    <h3>Office &amp; Admin</h3>
    <p>Augment office teams to push more work through the workshop without added overhead.</p>
    <p class="kicker">More throughput, less overhead.</p>
  </div>

  <div class="card c3">
    <div class="top">
      <div class="icon"><svg viewBox="0 0 24 24"><path d="M9 11a3 3 0 1 0 0-6 3 3 0 0 0 0 6ZM3 20a6 6 0 0 1 12 0M17 7l2 2 3-3"/></svg></div>
      <span class="num">03</span>
    </div>
    <h3>Customer Relationship</h3>
    <p>Data-driven engagement that retains drivers across the whole vehicle lifecycle.</p>
    <p class="kicker">Stronger retention, higher value.</p>
  </div>

</div>

<div class="connectors">
  <div class="conn c1"></div>
  <div class="conn c2"></div>
  <div class="conn c3"></div>
</div>

<div class="platform">
  <div class="icon"><svg viewBox="0 0 24 24"><ellipse cx="12" cy="5" rx="8" ry="3"/><path d="M4 5v6c0 1.7 3.6 3 8 3s8-1.3 8-3V5M4 11v6c0 1.7 3.6 3 8 3s8-1.3 8-3v-6"/></svg></div>
  <div>
    <p class="ptag">The foundation</p>
    <h3>Unified Data Platform</h3>
    <p>One canonical record for every customer, vehicle and booking — a digital twin of the business, fully legible to AI.</p>
  </div>
  <div class="tags">
    <span class="tag">Digital twin</span>
    <span class="tag">Legible to AI</span>
    <span class="tag">Single source of truth</span>
  </div>
</div>

<br><br>



<h2 class="section-title">Contributors</h2>
<p class="section-sub">Industry and tehcnology experts.</p>

<div class="contributors">

  <div class="person">
    <div class="avatar">DT</div>
    <h3>Danil Topchii</h3>
    <p>AI engineer who has built production AI agentic systems, with a background founding and scaling tech startups.</p>
  </div>

  <div class="person">
    <div class="avatar">TB</div>
    <h3>Tobyn Brooks</h3>
    <p>Founder of Autopic, building the data and technology platform behind the network.</p>
  </div>

  <div class="person">
    <div class="avatar">JL</div>
    <h3>Josh Lawman</h3>
    <p>AI engineer and former principal data scientist, building secure generative AI products for enterprise.</p>
  </div>

  
</div>

<br>

<h2 class="next-title">Where to next</h2>

<div class="next">
  <a class="n1" href="productive%20work/">
    <span>
      <span class="label">Pillar 01</span><br>
      <span class="name">Productive work</span>
    </span>
    <span class="arrow">&rarr;</span>
  </a>
  <a class="n2" href="office%20and%20admin/">
    <span>
      <span class="label">Pillar 02</span><br>
      <span class="name">Office &amp; admin</span>
    </span>
    <span class="arrow">&rarr;</span>
  </a>
  <a class="n3" href="customer%20relationship/">
    <span>
      <span class="label">Pillar 03</span><br>
      <span class="name">Customer relationship</span>
    </span>
    <span class="arrow">&rarr;</span>
  </a>
  <a class="n4" href="unified%20database/database/">
    <span>
      <span class="label">Foundation</span><br>
      <span class="name">Unified database</span>
    </span>
    <span class="arrow">&rarr;</span>
  </a>
</div>
