---
layout: default
title: Notices on Factor Graphs
---

<style>
:root { --fg-accent: #0f766e; }
html { scroll-behavior: smooth; }
body { margin: 0; }

.navbar { position: sticky; top: 0; z-index: 1000; background: white; border-bottom: 1px solid #eee; }
.navbar-inner { max-width: 900px; margin: 0 auto; padding: 0.6rem 1rem; display: flex; gap: 1rem; align-items: center; justify-content: space-between; }
.nav-title { font-weight: 700; }
.nav-links a { text-decoration: none; padding: 0.4rem 0.6rem; border-radius: 6px; color: inherit; }
.nav-links a.active, .nav-links a:hover { background: var(--fg-accent); color: white; }

.wrapper { max-width: 900px; margin: 0 auto; padding: 0 1rem 3rem 1rem; }
.section { padding: 2.2rem 0 1rem 0; scroll-margin-top: 64px; }
.section h1, .section h2 { margin-top: 0; }
hr.section-divider { margin: 2.2rem 0; border: 0; border-top: 1px dashed #dcdcdc; }
.callout { border-left: 4px solid var(--fg-accent); background: #f7fdfa; padding: 0.8rem 1rem; border-radius: 6px; }
table { width: 100%; border-collapse: collapse; }
th, td { border-bottom: 1px solid #eee; padding: 0.5rem; text-align: left; }
</style>

<div class="navbar">
  <div class="navbar-inner">
    <div class="nav-title">Notices on Factor Graphs</div>
    <nav class="nav-links">
      <a href="#agenda">Agenda</a>
      <a href="#materials">Materials</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</div>

<div class="wrapper">
  <div class="section" id="intro">
    <h1>Notices on Factor Graphs</h1>
    <p>
      Welcome to <strong>Notices on Factor Graphs</strong> —
      a lightweight, single-page hub for an online colloquium and curated resources.
      Scroll or use the menu to jump between sections.
    </p>
    <div class="callout">
      <strong>What are factor graphs?</strong>
      Factor graphs are bipartite graphical models that make the factorization structure of functions explicit, enabling clear reasoning about inference, optimization, and message passing.
    </div>
  </div>

  <hr class="section-divider" />

  <div class="section" id="agenda">
    <h2>Agenda — Upcoming Meetings</h2>

    <h3>Next Meeting (Template)</h3>
    <ul>
      <li><strong>Title:</strong> <em>e.g., Expectation Propagation on Factor Graphs</em></li>
      <li><strong>Speaker:</strong> <em>Name, Affiliation</em></li>
      <li><strong>Date &amp; Time:</strong> <em>e.g., 2025-11-12, 15:00–16:00 UTC</em></li>
      <li><strong>Link:</strong> <em>Video / Zoom / Meet</em></li>
      <li><strong>Abstract:</strong> <em>2–6 lines</em></li>
      <li><strong>Materials:</strong> <em>slides / paper / code links</em></li>
    </ul>

    <h3>2025</h3>
    <table>
      <thead>
        <tr>
          <th>Date (UTC)</th><th>Speaker</th><th>Title</th><th>Link</th><th>Materials</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><em>YYYY-MM-DD</em></td>
          <td><em>Name</em></td>
          <td><em>Talk title</em></td>
          <td><em>Meeting URL</em></td>
          <td><em>Slides / Paper</em></td>
        </tr>
      </tbody>
    </table>

    <p><em>Tip:</em> Keep “three invited talks per year” as a rough target; stay informal and lean.</p>
  </div>

  <hr class="section-divider" />

  <div class="section" id="materials">
    <h2>Materials — Key Resources</h2>

    <h3>Tutorials &amp; Overviews</h3>
    <ul>
      <li>Add your favorite intro/tutorial links here.</li>
      <li>Short notes or slide decks are welcome.</li>
    </ul>

    <h3>Foundational &amp; Representative Papers</h3>
    <ul>
      <li>Classic works on factor graphs, sum–product / max–product, loopy BP, EP, etc.</li>
    </ul>

    <h3>Software</h3>
    <ul>
      <li>Libraries for modeling and inference on factor graphs; visualization tools.</li>
    </ul>

    <h3>Drawing Templates</h3>
    <ul>
      <li>TikZ styles for factor graphs; other diagramming snippets.</li>
    </ul>

    <h3>Related Topics</h3>
    <ul>
      <li>Probabilistic graphical models (PGMs); control/estimation; optimization &amp; message passing.</li>
    </ul>
  </div>

  <hr class="section-divider" />

  <div class="section" id="contact">
    <h2>Contact</h2>
    <p>For announcements, suggestions, and talk proposals:</p>
    <ul>
      <li><strong>Email:</strong> <em>notices.factor.graphs [at] example.org</em></li>
      <li><strong>Maintainer(s):</strong> <em>Name(s), Affiliation(s)</em></li>
      <li><strong>GitHub:</strong> Open an issue in this repo to suggest edits.</li>
    </ul>
  </div>
</div>

<script>
(function() {
  const links = document.querySelectorAll('.nav-links a');
  const sections = Array.from(links).map(a => document.querySelector(a.getAttribute('href'))).filter(Boolean);
  const activate = (id) => { links.forEach(a => a.classList.toggle('active', a.getAttribute('href') === '#' + id)); };
  const observer = new IntersectionObserver((entries) => {
    entries.sort((a,b) => b.intersectionRatio - a.intersectionRatio);
    const visible = entries.find(e => e.isIntersecting);
    if (visible && visible.target && visible.target.id) activate(visible.target.id);
  }, { rootMargin: "-40% 0px -50% 0px", threshold: [0, 0.25, 0.5, 0.75, 1] });
  sections.forEach(sec => sec && observer.observe(sec));
})();
</script>
