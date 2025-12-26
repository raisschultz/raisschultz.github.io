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
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Coming Soon</title>
  <meta name="description" content="Placeholder homepage" />

  <style>
    :root{
      --bg1: #0b1020;
      --bg2: #0f1733;
      --card: rgba(255,255,255,.08);
      --text: rgba(255,255,255,.92);
      --muted: rgba(255,255,255,.72);
      --ring: rgba(255,255,255,.14);
    }

    *{ box-sizing: border-box; }
    html, body { height: 100%; }
    
    .wrap{
      height: 100%;
      display: grid;
      place-items: center;
      padding: 24px;
    }

    .card{
      width: min(720px, 92vw);
      border: 1px solid var(--ring);
      background: linear-gradient(180deg, var(--card), rgba(255,255,255,.04));
      backdrop-filter: blur(10px);
      border-radius: 22px;
      box-shadow: 0 20px 70px rgba(0,0,0,.45);
      padding: 28px 28px 22px;
    }

    .status{
      display: flex;
      align-items: center;
      gap: 10px;
      margin: 14px 0 12px;
      color: rgba(255,255,255,.86);
      font-size: 14px;
    }

    .dot{
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: rgba(255,255,255,.9);
      box-shadow: 0 0 0 0 rgba(255,255,255,.5);
      animation: pulse 1.2s ease-out infinite;
    }

    .bar{
      height: 10px;
      border-radius: 999px;
      background: rgba(255,255,255,.08);
      border: 1px solid var(--ring);
      overflow: hidden;
    }

    .bar > span{
      display: block;
      height: 100%;
      width: 40%;
      border-radius: 999px;
      background: linear-gradient(90deg, rgba(255,255,255,.18), rgba(255,255,255,.55), rgba(255,255,255,.18));
      filter: saturate(1.2);
      animation: load 1.4s ease-in-out infinite;
    }

  </style>
</head>

<body>
  <main class="wrap">
    <section class="card" aria-label="Placeholder">
      </div>

      <div class="status">
        <span class="dot" aria-hidden="true"></span>
        <span id="statusText">Loading…</span>
      </div>

      <div class="bar" aria-label="Loading indicator"><span></span></div>
     
      </div>
    </section>
  </main>

  <script>
    const statuses = [
      "Loading…",
      "Building homepage…",
      "Organizing projects…",
      "Publishing updates…"
    ];

    const statusEl = document.getElementById("statusText");
    let i = 0;

    setInterval(() => {
      i = (i + 1) % statuses.length;
      statusEl.textContent = statuses[i];
    }, 1400);

  </script>
</body>
</html>
