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
<!-- DVD bouncing placeholder that DOES NOT cover your navbar, and hides the footer -->
<div id="dvd-stage" aria-label="Loading placeholder">
  <div id="dvd-logo">DVD</div>
</div>

<style>
  /* Hide common Jekyll theme footers (navbar/header untouched) */
  footer,
  .site-footer,
  footer.site-footer,
  #footer,
  .page-footer {
    display: none !important;
  }

  /* Stage sits BELOW the navbar; JS sets --navH dynamically */
  :root { --navH: 0px; }

  #dvd-stage{
    position: relative;
    width: 100%;
    height: calc(100vh - var(--navH));
    margin-top: 0;
    background: #0b0f17;
    overflow: hidden;              /* critical: keeps logo inside bounds */
    border-radius: 8px;            /* optional */
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
    // 1) Compute navbar height so the stage begins BELOW it (navbar stays visible/clickable)
    const navLike = document.querySelector(
      "header, .site-header, .page-header, nav, .navbar, .top-nav, .masthead"
    );

    function setNavHeight() {
      const h = navLike ? Math.ceil(navLike.getBoundingClientRect().height) : 0;
      document.documentElement.style.setProperty("--navH", h + "px");
    }
    setNavHeight();
    window.addEventListener("resize", setNavHeight);

    // 2) Hide footer(s) via JS too (helps if theme injects/overrides footer styles)
    function removeFooters() {
      document.querySelectorAll("footer, .site-footer, #footer, .page-footer").forEach(el => {
        el.style.display = "none";
      });
    }
    removeFooters();
    // Run again shortly after load in case the theme renders late
    window.addEventListener("load", () => setTimeout(removeFooters, 50));

    // 3) Bounce the logo INSIDE the stage bounds (not the whole viewport)
    const stage = document.getElementById("dvd-stage");
    const logo  = document.getElementById("dvd-logo");

    let x = 20, y = 20;
    let vx = 2.2, vy = 2.0;

    function step() {
      const maxX = Math.max(0, stage.clientWidth  - logo.offsetWidth);
      const maxY = Math.max(0, stage.clientHeight - logo.offsetHeight);

      x += vx; y += vy;

      // bounce + clamp
      if (x <= 0)     { x = 0;    vx = Math.abs(vx); }
      if (x >= maxX)  { x = maxX; vx = -Math.abs(vx); }
      if (y <= 0)     { y = 0;    vy = Math.abs(vy); }
      if (y >= maxY)  { y = maxY; vy = -Math.abs(vy); }

      logo.style.left = x + "px";
      logo.style.top  = y + "px";

      requestAnimationFrame(step);
    }

    requestAnimationFrame(step);
  })();
</script>
