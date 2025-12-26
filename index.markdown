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
<!-- Full-width DVD loading page (keeps navbar), overrides theme max-width containers -->
<div id="dvd-loading-page">
  <div id="dvd-stage" aria-label="Loading placeholder">
    <div id="dvd-logo">DVD</div>
  </div>
</div>

<style>
  /* --- 1) Kill the theme's centered max-width constraints (common Jekyll wrappers) --- */
  /* These selectors cover most GitHub Pages themes (minima/cayman/architect/slate/etc.) */
  #dvd-loading-page,
  #dvd-loading-page * {
    box-sizing: border-box;
  }

  /* Make the page content wrappers full-width */
  .container,
  .wrapper,
  .page-content,
  .main-content,
  .content,
  .inner,
  .markdown-body,
  main,
  article {
    max-width: none !important;
    width: 100% !important;
  }

  /* Remove side padding/margins that create the “middle column” look */
  .container,
  .wrapper,
  .page-content,
  .main-content,
  .content,
  .inner,
  main,
  article {
    margin-left: 0 !important;
    margin-right: 0 !important;
    padding-left: 0 !important;
    padding-right: 0 !important;
  }

  /* --- 2) Hide footers (common theme selectors), but leave navbar alone --- */
  footer,
  .site-footer,
  footer.site-footer,
  #footer,
  .page-footer {
    display: none !important;
  }

  /* --- 3) DVD stage: fixed full-width BELOW the navbar --- */
  :root { --navH: 0px; }

  #dvd-stage{
    position: fixed;
    left: 0;
    right: 0;
    top: var(--navH);
    height: calc(100vh - var(--navH));
    background: #0b0f17;
    overflow: hidden;          /* keeps logo inside bounds */
    z-index: 1;                /* below header (we bump header above in JS if needed) */
  }

  #dvd-logo{
    position: absolute;
    left: 0;
    top: 0;

    font: 800 28px/1 system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    color: #e8eefc;
    border: 2px solid #e8eefc;
    border-radius: 6px;
    padding: 10px 14px;

    user-select: none;
    -webkit-user-select: none;
    cursor: default;
  }
</style>

<script>
  (function () {
    // Identify header/nav (covers most themes). If your theme uses something else,
    // add its selector here.
    const headerEl = document.querySelector(
      "header, .site-header, .page-header, nav, .navbar, .top-nav, .masthead"
    );

    // Ensure header stays above the DVD stage (so navbar remains usable)
    if (headerEl) {
      const computed = window.getComputedStyle(headerEl);
      if (computed.position === "static") headerEl.style.position = "relative";
      headerEl.style.zIndex = "9999";
    }

    function setNavHeight() {
      const h = headerEl ? Math.ceil(headerEl.getBoundingClientRect().height) : 0;
      document.documentElement.style.setProperty("--navH", h + "px");
    }

    setNavHeight();
    window.addEventListener("resize", setNavHeight);

    // Bounce inside #dvd-stage bounds (not the theme container)
    const stage = document.getElementById("dvd-stage");
    const logo  = document.getElementById("dvd-logo");

    let x = 20, y = 20;
    let vx = 2.2, vy = 2.0;

    function step() {
      const maxX = Math.max(0, stage.clientWidth  - logo.offsetWidth);
      const maxY = Math.max(0, stage.clientHeight - logo.offsetHeight);

      x += vx; y += vy;

      if (x <= 0)    { x = 0;    vx = Math.abs(vx); }
      if (x >= maxX) { x = maxX; vx = -Math.abs(vx); }
      if (y <= 0)    { y = 0;    vy = Math.abs(vy); }
      if (y >= maxY) { y = maxY; vy = -Math.abs(vy); }

      logo.style.left = x + "px";
      logo.style.top  = y + "px";

      requestAnimationFrame(step);
    }

    requestAnimationFrame(step);
  })();
</script>
