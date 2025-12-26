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
<div id="dvd-screen" aria-label="Loading placeholder">
  <div id="dvd-logo">DVD</div>
</div>

<style>
  /* Hide common Jekyll theme footers WITHOUT touching nav/header */
  footer,
  .site-footer,
  footer.site-footer,
  #footer,
  .page-footer {
    display: none !important;
  }

  /* Full-screen overlay so theme content (including the footer) can't sit "in the middle" */
  html, body {
    margin: 0;
    height: 100%;
    overflow: hidden;
    background: #0b0f17;
  }

  #dvd-screen {
    position: fixed;
    inset: 0;
    z-index: 999999; /* above theme content */
    background: #0b0f17;
  }

  #dvd-logo {
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
    const logo = document.getElementById("dvd-logo");

    // Start position & velocity
    let x = 30, y = 30;
    let vx = 2.2, vy = 2.0;

    function step() {
      const w = logo.offsetWidth;
      const h = logo.offsetHeight;

      const maxX = Math.max(0, window.innerWidth - w);
      const maxY = Math.max(0, window.innerHeight - h);

      x += vx;
      y += vy;

      // Bounce and CLAMP so it never goes out of bounds
      if (x <= 0) { x = 0; vx = Math.abs(vx); }
      if (x >= maxX) { x = maxX; vx = -Math.abs(vx); }
      if (y <= 0) { y = 0; vy = Math.abs(vy); }
      if (y >= maxY) { y = maxY; vy = -Math.abs(vy); }

      logo.style.left = x + "px";
      logo.style.top = y + "px";

      requestAnimationFrame(step);
    }

    // If viewport changes, force position back into bounds immediately
    window.addEventListener("resize", () => {
      const maxX = Math.max(0, window.innerWidth - logo.offsetWidth);
      const maxY = Math.max(0, window.innerHeight - logo.offsetHeight);
      x = Math.min(Math.max(0, x), maxX);
      y = Math.min(Math.max(0, y), maxY);
      logo.style.left = x + "px";
      logo.style.top = y + "px";
    });

    requestAnimationFrame(step);
  })();
</script>
