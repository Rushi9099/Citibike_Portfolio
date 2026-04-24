# Citi Bike DSS — Portfolio Site

> **Master's Research Project · Group 15 · Saint Louis University · Spring 2026**

Project portfolio site for the **Citi Bike Demand & Station-Imbalance Decision Support System**.
This is the 3.3 deliverable — the public-facing companion to the Power BI dashboard and React solution app.

---

## Live links

| Resource | URL |
|---|---|
| **Portfolio site** *(this repo)* | **[citibike-portfolio.vercel.app](https://citibike-portfolio.vercel.app/)** |
| **Solution App** | [citi-bike-dashboard.vercel.app](https://citi-bike-dashboard.vercel.app/) |
| **Power BI (.pbix)** | [Google Drive](https://drive.google.com/file/d/1sstMB7H-AJH3yhLMCLPFNX9jL8o-PNX1/view?usp=sharing) |
| **Dashboard source repo** | [github.com/Rushi9099/CitiBike_Dashboard](https://github.com/Rushi9099/CitiBike_Dashboard) |

---

## What's here

A single-page static site (`index.html`) covering the 12 sections required by the 3.3 rubric:

1. Hero / Cover (project title, team, CTAs)
2. Executive Summary (200–300 words)
3. Problem Context & Stakeholders
4. Research & Insights
5. Dataset & Design (ER diagram, data flow, cleaning steps)
6. Dashboard Insights (all 7 Power BI pages explained)
7. Proposed Solution (Enterprise Architecture diagram, key components)
8. Embedded Solution App (live iframe of Vercel deployment)
9. Benefits — Data 1 vs Data 2 (KPI before/after comparison)
10. Project Management (roadmap Gantt, RACI matrix)
11. Ethical & Social Considerations
12. Lessons Learned & Team Reflection
13. Team + Footer

---

## Tech

| Layer | Tool | Why |
|---|---|---|
| Markup | Vanilla HTML | No build, anyone can edit |
| Styling | Tailwind CSS via Play CDN | Utility classes, zero config |
| Typography | Google Fonts — Space Grotesk + DM Sans + JetBrains Mono | Modern, readable |
| Diagrams | [Mermaid.js](https://mermaid.js.org/) via CDN | ER + Enterprise Architecture — text-based, diff-friendly |
| Deploy | [Vercel](https://vercel.com/) (static hosting) | Global CDN, auto HTTPS, auto-redeploy on `git push` |

---

## Running locally

This is a static site — no build step. Just open the HTML in a browser:

```powershell
# Windows PowerShell
Start-Process index.html
```

Or serve it with any static file server for live-reload:

```bash
# Python 3
python -m http.server 8080

# Node
npx serve .
```

Then open http://localhost:8080/

---

## Editing

- **Content:** edit `index.html` directly. Each section is clearly delimited by a big comment block:
  ```
  <!-- ══════════════════ SECTION NAME ══════════════════ -->
  ```
- **Team names / roles:** search for "Group 15" or scroll to the Team section (near the bottom).
- **RACI matrix:** search for `<table` inside the "Project management" section.
- **Diagrams (Mermaid):** search for `<pre class="mermaid">`. The ER diagram, Enterprise Architecture flowchart, and Gantt roadmap are all text-based and easy to modify.
- **Images:** `assets/img/` — replace or add new screenshots here.

---

## Deployment

The site is deployed on **Vercel** and auto-redeploys on every push to `main`.

**Live URL:** [citibike-portfolio.vercel.app](https://citibike-portfolio.vercel.app/)

### First-time deploy (already done)

1. Sign in at [vercel.com](https://vercel.com/) with GitHub.
2. **Add New → Project → Import** `Rushi9099/Citibike_Portfolio`.
3. On the configuration screen:
   - **Framework Preset:** Other
   - **Root Directory:** `./`
   - **Build Command:** *(leave empty — no build step)*
   - **Output Directory:** *(leave empty)*
4. Click **Deploy**. Done in ~30 seconds.

### Subsequent deploys

Just push to `main`:

```bash
git add .
git commit -m "message"
git push
```

Vercel picks it up automatically. Preview deployments are created for every branch and PR.

### Alternative: GitHub Pages

If Vercel ever goes down, this site also works as-is on GitHub Pages (Settings → Pages → Deploy from branch → `main` / root). No code changes needed.

---

## File structure

```
citibike-portfolio/
├── index.html                 The entire portfolio site
├── README.md                  This file
├── .gitignore
└── assets/
    ├── favicon.svg
    └── img/
        ├── data-pipeline.png
        ├── pbi-home.png
        ├── pbi-demand.png
        ├── pbi-stations.png
        ├── pbi-riders.png
        ├── pbi-imbalance.png
        ├── pbi-dataflow.png
        └── pbi-comparison.png
```

---

## Team — Group 15

- Nithin Kumar Adki
- Aditya Anguri
- Rushi Chandra Gannamaneni
- Sandeep Eshwar Datta Narsin
- Bharat Reddy Palukuri

---

## License

Coursework prototype. Trip data © Lyft / Citi Bike, used under their public data license.
