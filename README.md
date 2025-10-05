<!--
  Portfolio Beispiel: index.html
  Enthält: komplette HTML-Datei (responsive), Styling, kleines JS
  + eine sichtbare Schritt-für-Schritt-Anleitung (Git-Befehle, GitHub Pages, VS Code Hinweise)
  Anleitung kurz:
    1) Neues GitHub-Repo erstellen
    2) Diese Datei als index.html in dein Projektordner speichern
    3) In VS Code öffnen, Live Server installieren (optional)
    4) Git initialisieren, committen, remote hinzufügen, push
    5) GitHub Pages in den Repo-Settings aktivieren
  Ersetze <YOUR-NAME>, <username> und <repo> durch deine Werte.
-->
<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Portfolio von <YOUR-NAME> — Projekte, Über mich, Kontakt" />
  <title>Portfolio — &lt;YOUR-NAME&gt;</title>
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --accent:#7c3aed; --muted:#9aa4b2; --glass: rgba(255,255,255,0.03);
      --radius:16px; --maxwidth:1100px; --gap:20px; --fw: 400;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;background:linear-gradient(180deg,#071024 0%, #0b1220 100%);color:#e6eef6}
    a{color:inherit;text-decoration:none}
    .wrap{max-width:var(--maxwidth);margin:32px auto;padding:24px}
    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{font-weight:700;letter-spacing:0.4px}
    nav{display:flex;gap:12px;align-items:center}
    nav a{padding:8px 12px;border-radius:10px;background:transparent}
    nav a:hover{background:var(--glass)}

    /* Hero */
    .hero{display:grid;grid-template-columns:1fr 360px;gap:28px;align-items:center;margin:28px 0}
    .hero h1{font-size:clamp(28px,5vw,44px);margin:0}
    .hero p{color:var(--muted);margin-top:8px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:20px;border-radius:var(--radius);box-shadow:0 6px 18px rgba(2,6,23,0.6)}
    .avatar{height:200px;border-radius:18px;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,var(--accent),#4f46e5);font-weight:700;color:white}

    /* Sections */
    section{margin:22px 0}
    #projects .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
    .project{padding:16px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.01));min-height:140px}
    .project h3{margin:0 0 8px 0}
    .project p{margin:0;color:var(--muted)}

    /* Contact */
    .contact-row{display:flex;gap:12px;align-items:center}
    .btn{display:inline-block;padding:10px 14px;border-radius:10px;background:var(--accent);color:white;font-weight:600}

    footer{color:var(--muted);font-size:14px;margin-top:28px;padding-top:8px;border-top:1px solid rgba(255,255,255,0.03)}

    /* Responsive */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr}
      #projects .grid{grid-template-columns:repeat(2,1fr)}
    }
    @media (max-width:560px){
      #projects .grid{grid-template-columns:1fr}
      nav{display:none}
    }

    /* Anleitung styling */
    pre{background:#020617;color:#c9d6ff;padding:12px;border-radius:10px;overflow:auto}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">&lt;YOUR-NAME&gt; — Portfolio</div>
      <nav>
        <a href="#about">Über mich</a>
        <a href="#projects">Projekte</a>
        <a href="#contact">Kontakt</a>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div>
          <h1>Hi — ich bin &lt;YOUR-NAME&gt;.</h1>
          <p>Frontend-Entwickler · Designer · Ich baue Web‑Apps und schöne Interfaces. Hier sind einige meiner Projekte.</p>
          <div style="margin-top:18px">
            <a class="btn" href="#projects">Projekte ansehen</a>
            <a style="margin-left:10px;color:var(--muted)" href="mailto:your@email.de">Kontakt</a>
          </div>
        </div>
        <aside class="card">
          <div class="avatar">Avatar / Foto</div>
          <div style="margin-top:12px;color:var(--muted)">Kurze Stichworte: HTML · CSS · JavaScript · React</div>
        </aside>
      </section>

      <section id="about" class="card">
        <h2>Über mich</h2>
        <p style="color:var(--muted);margin-top:6px">Schreibe hier ein bis drei Sätze über dich: was du machst, welche Technologien du nutzt und was dich antreibt.</p>
      </section>

      <section id="projects">
        <h2>Projekte</h2>
        <div class="grid" style="margin-top:12px">
          <article class="project card">
            <h3>Projekt A</h3>
            <p>Kurze Beschreibung — Problem, Lösung, Technologien.</p>
            <div style="margin-top:12px">
              <a href="#" style="margin-right:8px">Live</a>
              <a href="#">Code</a>
            </div>
          </article>

          <article class="project card">
            <h3>Projekt B</h3>
            <p>Kurze Beschreibung — SPA, API, Design.</p>
          </article>

          <article class="project card">
            <h3>Projekt C</h3>
            <p>Kurze Beschreibung — Open Source, Tests, Deploy.</p>
          </article>
        </div>
      </section>

      <section id="contact" class="card">
        <h2>Kontakt</h2>
        <p style="color:var(--muted);margin-top:6px">Beste Wege — E‑Mail oder GitHub. Optional: Kontaktformular (hier nur Mailto als Beispiel).</p>
        <div style="margin-top:12px" class="contact-row">
          <a class="btn" href="mailto:your@email.de">E‑Mail senden</a>
          <a style="color:var(--muted)" href="https://github.com/<username>">GitHub</a>
        </div>
      </section>

      <section class="card" style="margin-top:18px">
        <h2>Schritt‑für‑Schritt: Von lokal → GitHub → GitHub Pages</h2>
        <ol style="color:var(--muted);margin-top:8px">
          <li>Erstelle ein neues Repository auf <strong>github.com</strong> (z. B. repo-portfolio).</li>
          <li>Speichere diese Datei als <code>index.html</code> in einem neuen Ordner auf deinem Rechner.</li>
          <li>Öffne den Ordner in Visual Studio Code (<code>code .</code> im Terminal). Empfohlen: Erweiterung <em>Live Server</em> installieren zum lokalen Testen.</li>
          <li>Git initialisieren &amp; pushen — öffne das Terminal in VS Code und führe aus:</li>
        </ol>
        <pre>
# Beispielbefehle - ersetze username und repo
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
        </pre>
        <ol start="5" style="color:var(--muted)">
          <li>Gehe auf GitHub → Einstellungen des Repos → "Pages" und wähle als Quelle <strong>Branch: main / Folder: / (root)</strong>. Speichere. Nach kurzer Zeit ist die Seite erreichbar unter <code>https://&lt;username&gt;.github.io/&lt;repo&gt;</code>.</li>
          <li>Optional: Wenn du eine eigene Domain nutzt, kannst du sie in den Pages-Einstellungen hinzufügen.</li>
        </ol>
        <p style="color:var(--muted)">Wenn du statische Assets (z. B. Bilder) hinzufügen willst, lege sie in einen Ordner <code>/assets</code> und verlinke relativ.</p>
      </section>

      <section class="card" style="margin-top:18px">
        <h2>Tipps &amp; Erweiterungen</h2>
        <ul style="color:var(--muted);margin-top:8px">
          <li>Setze semantische HTML-Elemente (article, section, header) für bessere Zugänglichkeit.</li>
          <li>Verwende kurze, aussagekräftige Commit-Nachrichten und Branches für neue Features.</li>
          <li>Füge ein README.md zu deinem Repo hinzu — es wird auf GitHub oben angezeigt.</li>
          <li>Wenn du React/Vite nutzen möchtest, kann ich dir ein Starter-Template erstellen.</li>
        </ul>
      </section>

      <footer>
        <div>© &lt;YOUR-NAME&gt; — Erstellt mit ❤️ • Anpassbar</div>
      </footer>
    </main>
  </div>

  <script>
    // kleines JS: smooth scroll (progressiv enhancement)
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click',e=>{
        const href = a.getAttribute('href');
        if(href.length>1){
          e.preventDefault();
          document.querySelector(href).scrollIntoView({behavior:'smooth'});
        }
      })
    })
  </script>
</body>
</html>
