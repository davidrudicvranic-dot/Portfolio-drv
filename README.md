<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mein Design-Portfolio</title>
  <style>
    /* --- Grundstil --- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }

    body {
      background-color: #000;
      color: #fff;
      line-height: 1.6;
    }

    a {
      color: #fff;
      text-decoration: none;
    }

    header {
      position: fixed;
      width: 100%;
      top: 0;
      left: 0;
      background: rgba(0, 0, 0, 0.8);
      backdrop-filter: blur(8px);
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      z-index: 10;
    }

    header h1 {
      font-size: 1.5rem;
      letter-spacing: 1px;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 2rem;
    }

    nav ul li a {
      font-weight: 500;
      transition: opacity 0.3s;
    }

    nav ul li a:hover {
      opacity: 0.6;
    }

    /* --- Hero Section --- */
    section#hero {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 2rem;
    }

    #hero h2 {
      font-size: 3rem;
      font-weight: 700;
      margin-bottom: 1rem;
    }

    #hero p {
      font-size: 1.2rem;
      color: #aaa;
      max-width: 600px;
    }

    /* --- Portfolio --- */
    section#portfolio {
      padding: 6rem 2rem;
      background-color: #111;
    }

    #portfolio h2 {
      text-align: center;
      font-size: 2rem;
      margin-bottom: 3rem;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }

    .grid-item {
      background: #000;
      border: 1px solid #222;
      border-radius: 12px;
      overflow: hidden;
      transition: transform 0.3s;
    }

    .grid-item img {
      width: 100%;
      display: block;
    }

    .grid-item:hover {
      transform: scale(1.03);
    }

    /* --- About --- */
    section#about {
      padding: 6rem 2rem;
      text-align: center;
    }

    #about h2 {
      font-size: 2rem;
      margin-bottom: 1.5rem;
    }

    #about p {
      max-width: 600px;
      margin: 0 auto;
      color: #aaa;
    }

    /* --- Kontakt --- */
    section#contact {
      padding: 6rem 2rem;
      background-color: #111;
      text-align: center;
    }

    #contact h2 {
      font-size: 2rem;
      margin-bottom: 1.5rem;
    }

    #contact a {
      display: inline-block;
      margin-top: 1rem;
      padding: 0.75rem 2rem;
      border: 1px solid #fff;
      border-radius: 50px;
      transition: background 0.3s, color 0.3s;
    }

    #contact a:hover {
      background: #fff;
      color: #000;
    }

    footer {
      text-align: center;
      padding: 2rem;
      font-size: 0.9rem;
      color: #666;
    }

    /* --- Responsive Navigation --- */
    @media (max-width: 768px) {
      nav ul {
        flex-direction: column;
        background: #000;
        position: absolute;
        top: 70px;
        right: 0;
        width: 100%;
        display: none;
        text-align: center;
      }

      nav ul.active {
        display: flex;
      }

      .menu-toggle {
        display: block;
        cursor: pointer;
      }
    }

    .menu-toggle {
      display: none;
      font-size: 1.5rem;
    }
  </style>
</head>
<body>

  <header>
    <h1>Mein Portfolio</h1>
    <div class="menu-toggle">☰</div>
    <nav>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#about">Über mich</a></li>
        <li><a href="#contact">Kontakt</a></li>
      </ul>
    </nav>
  </header>

  <section id="hero">
    <h2>Willkommen in meinem Design-Portfolio</h2>
    <p>Ich bin Designer mit Fokus auf moderne, minimalistische Gestaltung. Hier findest du meine besten Arbeiten und kreativen Projekte.</p>
  </section>

  <section id="portfolio">
    <h2>Meine Arbeiten</h2>
    <div class="grid">
      <div class="grid-item"><img src="https://via.placeholder.com/400x300" alt="Design 1"></div>
      <div class="grid-item"><img src="https://via.placeholder.com/400x300" alt="Design 2"></div>
      <div class="grid-item"><img src="https://via.placeholder.com/400x300" alt="Design 3"></div>
      <div class="grid-item"><img src="https://via.placeholder.com/400x300" alt="Design 4"></div>
    </div>
  </section>

  <section id="about">
    <h2>Über mich</h2>
    <p>Ich bin ein kreativer Designer mit Leidenschaft für minimalistische Ästhetik und klare Linien. Mein Ziel ist es, funktionale und gleichzeitig ansprechende Designs zu schaffen, die inspirieren.</p>
  </section>

  <section id="contact">
    <h2>Kontakt</h2>
    <p>Interessiert an einer Zusammenarbeit oder Feedback zu meinen Arbeiten?</p>
    <a href="mailto:deine@email.de">Schreib mir</a>
  </section>

  <footer>
    © 2025 Mein Portfolio – Alle Rechte vorbehalten.
  </footer>

  <script>
    const toggle = document.querySelector('.menu-toggle');
    const nav = document.querySelector('nav ul');

    toggle.addEventListener('click', () => {
      nav.classList.toggle('active');
    });
  </script>
</body>
</html>
