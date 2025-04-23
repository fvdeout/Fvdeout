<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FVDEØUT.CAL</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@700&display=swap');

    :root {
      --black: #000000;
      --dark-gray: #111111;
      --white: #ffffff;
      --highlight: #ff0055;
      --accent: #00fff7;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Orbitron', sans-serif;
      background-color: var(--black);
      color: var(--white);
      overflow-x: hidden;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .hero {
      width: 100vw;
      height: 100vh;
      background: linear-gradient(180deg, #000000 0%, #0a0a0a 100%);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      text-align: center;
      padding: 2rem;
    }

    .hero h1 {
      font-size: 10vw;
      letter-spacing: 5px;
      color: var(--highlight);
    }

    .hero p {
      font-size: 4vw;
      margin-top: 1rem;
      color: var(--white);
    }

    .btn {
      margin-top: 2rem;
      padding: 1rem 2rem;
      font-size: 1.2rem;
      border: 2px solid var(--white);
      background: transparent;
      color: var(--white);
      transition: all 0.3s ease;
    }

    .btn:hover {
      background: var(--white);
      color: var(--black);
    }

    .about {
      padding: 5vw;
      background: var(--dark-gray);
      display: flex;
      flex-direction: column;
      gap: 2rem;
    }

    .about video {
      width: 100%;
      border-radius: 12px;
    }

    .about h2 {
      font-size: 6vw;
      color: var(--accent);
    }

    .about p {
      font-size: 1.2rem;
      line-height: 1.6;
      color: var(--white);
    }

    .events, .sound, footer {
      padding: 5vw;
      text-align: center;
    }

    .events h2, .sound h2 {
      font-size: 2rem;
      color: var(--highlight);
      margin-bottom: 2rem;
    }

    .event-card {
      background: #1a1a1a;
      border: 1px solid #333;
      padding: 2rem;
      border-radius: 8px;
      max-width: 400px;
      margin: 0 auto;
    }

    .event-card h3 {
      font-size: 1.5rem;
      color: var(--accent);
    }

    .event-card p {
      margin: 0.5rem 0;
    }

    .sound iframe {
      max-width: 100%;
      border-radius: 8px;
    }

    footer p {
      margin-top: 1rem;
      color: #888;
    }

    .socials a {
      margin: 0 1rem;
      color: var(--white);
      transition: color 0.3s;
    }

    .socials a:hover {
      color: var(--accent);
    }

    @media (min-width: 768px) {
      .hero h1 { font-size: 5vw; }
      .hero p { font-size: 2vw; }
      .about {
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
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
    <iframe src="https://open.spotify.com/embed/playlist/37i9dQZF1DX6VdMW310YC7" width="100%" height="80" frameborder="0" allowtransparency="true" allow="encrypted-media"></iframe>
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
