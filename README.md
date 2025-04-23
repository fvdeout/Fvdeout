<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FVDEØUT.CAL</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@700&display=swap');

    :root {
      --black: #000;
      --gray: #111;
      --white: #fff;
      --hotpink: #ff007f;
      --aqua: #00ffe0;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      font-family: 'Orbitron', sans-serif;
      background: var(--black);
      color: var(--white);
      overflow-x: hidden;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .hero {
      height: 100vh;
      background: linear-gradient(to bottom, #000, #111);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 2rem;
    }

    .hero h1 {
      font-size: clamp(2rem, 10vw, 6rem);
      color: var(--hotpink);
      letter-spacing: 6px;
    }

    .hero p {
      font-size: clamp(1rem, 4vw, 2rem);
      margin: 1rem 0;
    }

    .btn {
      margin-top: 1rem;
      padding: 1rem 2rem;
      border: 2px solid var(--white);
      font-size: 1rem;
      background: transparent;
      color: var(--white);
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .btn:hover {
      background: var(--white);
      color: var(--black);
    }

    .about {
      display: flex;
      flex-direction: column;
      padding: 3rem 1rem;
      background: var(--gray);
      gap: 2rem;
    }

    .about video {
      width: 100%;
      border-radius: 10px;
    }

    .about .text h2 {
      font-size: clamp(1.5rem, 5vw, 3rem);
      color: var(--aqua);
    }

    .about .text p {
      font-size: 1.1rem;
      margin-top: 1rem;
      line-height: 1.6;
    }

    .events, .sound, footer {
      padding: 3rem 1rem;
      text-align: center;
    }

    .events h2, .sound h2 {
      color: var(--hotpink);
      margin-bottom: 2rem;
      font-size: 2rem;
    }

    .event-card {
      background: #1c1c1c;
      border: 1px solid #333;
      padding: 2rem;
      border-radius: 10px;
      max-width: 400px;
      margin: 0 auto;
    }

    .event-card h3 {
      font-size: 1.5rem;
      color: var(--aqua);
    }

    .event-card p {
      margin: 0.5rem 0;
    }

    .sound iframe {
      width: 100%;
      max-width: 500px;
      height: 80px;
      border: none;
      border-radius: 8px;
    }

    footer .socials {
      margin: 1rem 0;
    }

    .socials a {
      margin: 0 1rem;
      color: var(--white);
      transition: color 0.3s;
    }

    .socials a:hover {
      color: var(--aqua);
    }

    footer p {
      font-size: 0.9rem;
      color: #888;
      margin-top: 1rem;
    }

    @media (min-width: 768px) {
      .about {
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
      }
      .about video, .about .text {
        width: 48%;
      }
    }
  </style>
</head>
<body>
  <section class="hero">
    <h1>FVDEØUT.CAL</h1>
    <p>IMMERSIVE. UNFORGETTABLE. UNDERGROUND.</p>
    <a href="#about" class="btn">ENTER THE VOID</a>
  </section>

  <section class="about" id="about">
    <video autoplay muted loop playsinline>
      <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
    </video>
    <div class="text">
      <h2>We don’t do events. We engineer <em>experiences</em>.</h2>
      <p>FVDEØUT.CAL is your gateway to curated clubbing chaos. Techno. House. Experimental. No rules, just energy.</p>
    </div>
  </section>

  <section class="events">
    <h2>Upcoming Events</h2>
    <div class="event-card">
      <h3>✹ FVD.RITUAL</h3>
      <p>Mumbai | 26.04.25</p>
      <p>Lineup: NASH | Xæon | Sifon</p>
      <a href="#" class="btn">RSVP</a>
    </div>
  </section>

  <section class="sound">
    <h2>PRESS PLAY. GET LOST.</h2>
    <iframe src="https://open.spotify.com/embed/playlist/37i9dQZF1DX6VdMW310YC7" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>
  </section>

  <footer>
    <div class="socials">
      <a href="#">Instagram</a>
      <a href="#">X</a>
      <a href="#">Mail</a>
    </div>
    <p>© 2025 FVDEØUT.CAL</p>
  </footer>
</body>
</html>
