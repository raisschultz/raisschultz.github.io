---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
# THIS IS THE HOME PAGE. 
layout: home 

navbar-links: 
  Automated License Plate Readers: 
    - Introduction: "https://raisschultz.github.io/projectALPR/introduction/"
    - Example 1 - Flock Cameras: "https://raisschultz.github.io/projectALPR/flockalprs/"
    - Example 2 - Border Patrol Use: "https://raisschultz.github.io/projectALPR/borderpatrolalprs/"
    - Benefits: "https://raisschultz.github.io/projectALPR/benefits/"
    - Legal Concerns and Implications: "https://raisschultz.github.io/projectALPR/legalconcerns/"
    - Social and Political Concerns and Implications: "https://raisschultz.github.io/projectALPR/socialethicalconcerns/"
    - Technological Concerns and Implications: "https://raisschultz.github.io/projectALPR/technologicalconcerns/"
    - A Utilitarian Perspective on ALPRs: "https://raisschultz.github.io/projectALPR/utilitarianlens"
    - A Deontological Perspective on ALPRs: "https://raisschultz.github.io/projectALPR/deontologicallens"
    - Proposed Changes and Improvements: "https://raisschultz.github.io/projectALPR/proposedchanges/"
    - Bibliography: "https://raisschultz.github.io/projectALPR/bibliography/"
  Case Studies: 
    - Equifax: "https://raisschultz.github.io/casestudies/Equifax/"
    - Stuxnet: "https://raisschultz.github.io/casestudies/Stuxnet/"
    - FireEye: "https://raisschultz.github.io/casestudies/FireEye/"
  Extended Essay: "https://raisschultz.github.io/IB/ee/"
  Pedestrian Infrastructure: 
    - Research Proposal: "https://raisschultz.github.io/research/pedestrianinfrastructureproposal/"
    - Poster: "https://raisschultz.github.io/research/pedestrianinfrastructureposter/"
  Resume: "https://raisschultz.github.io/resume/december2025/"

---
<style>
  :root{
    --bg1:#0b1020;
    --bg2:#0f1733;
    --card: rgba(255,255,255,.08);
    --text: rgba(255,255,255,.92);
    --muted: rgba(255,255,255,.72);
    --ring: rgba(255,255,255,.14);
  }

  /* Take over the visible viewport while leaving the navbar intact */
  .placeholder{
    position: relative;
    min-height: calc(100vh - var(--nav-offset, 0px));
    overflow: hidden;
    color: var(--text);
    font: 500 16px/1.35 system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    background:
      radial-gradient(1200px 800px at 10% 10%, #22306a 0%, transparent 55%),
      radial-gradient(1100px 700px at 85% 20%, #6a2b5e 0%, transparent 55%),
      linear-gradient(120deg, var(--bg1), var(--bg2));
    background-size: 140% 140%;
    animation: bgShift 8s ease-in-out infinite alternate;
  }

  @keyframes bgShift{
    0%{ background-position: 0% 0%, 100% 0%, 0% 50%; }
    100%{ background-position: 15% 20%, 80% 10%, 100% 50%; }
  }

  .placeholder::before{
    content:"";
    position:absolute;
    inset:0;
    pointer-events:none;
    opacity:.22;
    mix-blend-mode: overlay;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='180' height='180'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='180' height='180' filter='url(%23n)' opacity='.22'/%3E%3C/svg%3E");
  }

  .blob{
    position:absolute;
    width: 52vmax;
    height: 52vmax;
    border-radius: 50%;
    filter: blur(28px);
    pointer-events:none;
    opacity:.26;
    animation: float 10s ease-in-out infinite;
  }
  .blob.b1{
    left:-18vmax; top:-18vmax;
    background:
      radial-gradient(circle at 30% 30%, #6bdcff 0%, transparent 55%),
      radial-gradient(circle at 70% 70%, #7c5cff 0%, transparent 55%);
    animation-duration: 10s;
  }
  .blob.b2{
    right:-22vmax; top:10vmax;
    background:
      radial-gradient(circle at 30% 30%, #ff6bd6 0%, transparent 55%),
      radial-gradient(circle at 70% 70%, #ffb86b 0%, transparent 55%);
    animation-duration: 12s;
    animation-direction: reverse;
    opacity:.24;
  }
  .blob.b3{
    left:10vmax; bottom:-26vmax;
    background:
      radial-gradient(circle at 30% 30%, #6bffb5 0%, transparent 55%),
      radial-gradient(circle at 70% 70%, #6b86ff 0%, transparent 55%);
    animation-duration: 11s;
    opacity:.20;
  }

  @keyframes float{
    0%   { transform: translate(0,0) scale(1); }
    50%  { transform: translate(4.5vmax, -3vmax) scale(1.05); }
    100% { transform: translate(-3vmax, 3.5vmax) scale(1); }
  }

  .wrap{
    position: relative;
    min-height: 100%;
    display:grid;
    place-items:center;
    padding: 24px;
    z-index:1;
  }

  .card{
    width: min(720px, 92vw);
    padding: 28px 28px 22px;
    border-radius: 22px;
    border: 1px solid var(--ring);
    background: linear-gradient(180deg, var(--card), rgba(255,255,255,.04));
    backdrop-filter: blur(10px);
    box-shadow: 0 20px 70px rgba(0,0,0,.45);
  }

  .topline{
    display:flex;
    align-items:center;
    justify-content: space-between;
    gap: 16px;
    margin-bottom: 10px;
  }

  .pill{
    font-size: 12px;
    letter-spacing: .2px;
    color: var(--muted);
    background: rgba(255,255,255,.06);
    border: 1px solid var(--ring);
    border-radius: 999px;
    padding: 6px 10px;
  }

  h1{
    margin: 6px 0 8px;
    font-size: clamp(28px, 4vw, 44px);
    line-height: 1.05;
    letter-spacing: -0.02em;
  }

  p{
    margin: 0 0 18px;
    max-width: 62ch;
    color: var(--muted);
    font-size: 15px;
  }

  .status{
    display:flex;
    align-items:center;
    gap: 10px;
    margin: 14px 0 12px;
    font-size: 14px;
    color: rgba(255,255,255,.86);
  }

  .dot{
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: rgba(255,255,255,.9);
    box-shadow: 0 0 0 0 rgba(255,255,255,.5);
    animation: pulse 1.2s ease-out infinite;
  }

  @keyframes pulse{
    0%{ box-shadow: 0 0 0 0 rgba(255,255,255,.55); }
    100%{ box-shadow: 0 0 0 14px rgba(255,255,255,0); }
  }

  .bar{
    height: 10px;
    border-radius: 999px;
    overflow: hidden;
    border: 1px solid var(--ring);
    background: rgba(255,255,255,.08);
  }
  .bar span{
    display:block;
    height: 100%;
    width: 40%;
    border-radius: 999px;
    filter: saturate(1.2);
    background: linear-gradient(90deg, rgba(255,255,255,.18), rgba(255,255,255,.55), rgba(255,255,255,.18));
    animation: load 1.4s ease-in-out infinite;
  }
  @keyframes load{
    0%{ transform: translateX(-120%); }
    100%{ transform: translateX(260%); }
  }

  .card-footer{
    display:flex;
    justify-content: space-between;
    gap: 14px;
    margin-top: 18px;
    font-size: 12px;
    color: rgba(255,255,255,.58);
  }

  .card-footer a{
    color: rgba(255,255,255,.78);
    text-decoration: none;
    border-bottom: 1px dotted rgba(255,255,255,.35);
  }
  .card-footer a:hover{ color: rgba(255,255,255,.95); }

  /* Try to reduce the theme footer impact without killing the navbar */
  footer, .site-footer, #footer { display:none; }

  @media (prefers-reduced-motion: reduce){
    *{ animation: none !important; transition: none !important; }
    .placeholder{ background-size: initial; }
  }
</style>

<div class="placeholder" id="placeholder">
  <div class="blob b1" aria-hidden="true"></div>
  <div class="blob b2" aria-hidden="true"></div>
  <div class="blob b3" aria-hidden="true"></div>

  <main class="wrap">
    <section class="card" aria-label="Placeholder">
      <div class="topline">
        <div class="pill" id="timestamp">Updated just now</div>
        <div class="pill">Placeholder Mode</div>
      </div>

      <h1>Site in progress.</h1>
      <p>This homepage is intentionally minimal while I build out the full layout and content. Check back soon.</p>

      <div class="status">
        <span class="dot" aria-hidden="true"></span>
        <span id="statusText">Loading layout…</span>
      </div>

      <div class="bar" aria-label="Loading indicator"><span></span></div>

      <div class="card-footer">
        <span>© <span id="year"></span></span>
        <span><a href="#" onclick="return false;">raisschultz.github.io</a></span>
      </div>
    </section>
  </main>
</div>

<script>
  const statuses = [
    "Loading layouts…",
    "Finding old papers…",
    "Tidying appearance…",
    "Deploying updates…"
  ];

  const statusEl = document.getElementById("statusText");
  let i = 0;

  setInterval(() => {
    i = (i + 1) % statuses.length;
    statusEl.textContent = statuses[i];
  }, 1400);

  const now = new Date();
  document.getElementById("year").textContent = now.getFullYear();
  document.getElementById("timestamp").textContent =
    "Updated " + now.toLocaleString(undefined, { dateStyle: "medium", timeStyle: "short" });
</script>
</html>
