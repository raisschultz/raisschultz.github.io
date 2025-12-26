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

<div id="dvd-loading-page">
  <div id="dvd-stage" aria-label="Loading placeholder">

    <div id="dvd-logo" aria-hidden="true">DVD</div>

    <div id="video-box" aria-label="Embedded video">
     <iframe title="Euroleague: Partizan Mozzart Bet Belgrade vs Maccabi Rapyd Tel Aviv Player" marginheight="0" marginwidth="0" src="https://embedsports.top/embed/charlie/partizan-mozzart-bet-belgrade-vs-maccabi-tel-aviv-1629472649/1" scrolling="no" allowfullscreen="yes" allow="encrypted-media; picture-in-picture;" width="100%" height="100%" frameborder="0"></iframe>
    </div>

  </div>
</div>

<style>

  .container, .wrapper, .page-content, .main-content, .content, .inner,
  .markdown-body, main, article {
    max-width: none !important;
    width: 100% !important;
  }
  .container, .wrapper, .page-content, .main-content, .content, .inner,
  main, article {
    margin-left: 0 !important;
    margin-right: 0 !important;
    padding-left: 0 !important;
    padding-right: 0 !important;
  }


  footer, .site-footer, footer.site-footer, #footer, .page-footer {
    display: none !important;
  }

  :root { --navH: 0px; }


  #dvd-stage{
    position: fixed;
    left: 0;
    right: 0;
    top: var(--navH);
    height: calc(100vh - var(--navH));
    background: #0b0f17;
    overflow: hidden;          /* keeps DVD inside bounds */
    z-index: 1;                /* below navbar */
  }


  #dvd-logo{
    position: absolute;
    left: 0;
    top: 0;
    z-index: 1;                /* behind video-box (z=2) */
    font: 800 28px/1 system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    color: #e8eefc;
    border: 2px solid #e8eefc;
    border-radius: 6px;
    padding: 10px 14px;
    user-select: none;
    -webkit-user-select: none;
    cursor: default;
  }

  #video-box{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    z-index: 2;                 /* above DVD */
    width: min(960px, 92vw);
    aspect-ratio: 16 / 9;
    border-radius: 12px;
    overflow: hidden;
    background: rgba(0,0,0,0.35);
    border: 1px solid rgba(232,238,252,0.25);
    backdrop-filter: blur(6px);
    pointer-events: auto;       /* clickable player */
  }

  #video-box iframe{
    width: 100%;
    height: 100%;
    border: 0;
    display: block;
  }
</style>

<script>
  (function () {
    // Keep navbar visible by measuring it and positioning the stage below it.
    const headerEl = document.querySelector(
      "header, .site-header, .page-header, nav, .navbar, .top-nav, .masthead"
    );

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

    // Bounce INSIDE the stage bounds (not the viewport, not the theme container).
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
