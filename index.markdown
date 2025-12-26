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
<div id="screen">
  <div id="dvd">DVD</div>
</div>

<style>
  html, body {
    margin: 0;
    height: 100%;
    background: #0b0f17;
    overflow: hidden;
  }

  #screen {
    position: relative;
    width: 100%;
    height: 100%;
  }

  #dvd {
    position: absolute;
    font: 700 28px/1 system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    color: #e8eefc;
    padding: 10px 14px;
    border: 2px solid #e8eefc;
    border-radius: 4px;
    user-select: none;
  }
</style>

<script>
  const dvd = document.getElementById("dvd");

  let x = 50, y = 50;
  let vx = 2, vy = 2;

  function animate() {
    const rect = dvd.getBoundingClientRect();
    const maxX = window.innerWidth - rect.width;
    const maxY = window.innerHeight - rect.height;

    x += vx;
    y += vy;

    if (x <= 0 || x >= maxX) vx *= -1;
    if (y <= 0 || y >= maxY) vy *= -1;

    dvd.style.transform = `translate(${x}px, ${y}px)`;
    requestAnimationFrame(animate);
  }

  animate();
</script>
