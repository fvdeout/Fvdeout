<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FVDEØUT.CAL</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      background-color: #000;
      color: #fff;
      font-family: 'Arial', sans-serif;
      overflow-x: hidden;
    }
    a {
      color: #fff;
      text-decoration: none;
    }
    .hero {
      height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      background: radial-gradient(#111, #000);
      text-align: center;
      padding: 2rem;
    }
    .hero h1 {
      font-size: 4rem;
      letter-spacing: 6px;
    }
    .hero p {
      font-size: 1.2rem;
      margin: 1rem 0;
    }
    .btn {
      padding: 12px 24px;
      border: 1px solid #fff;
      margin-top: 1rem;
      transition: 0.3s;
    }
    .btn:hover {
      background: #fff;
      color: #000;
    }
    .about {
      display: flex;
      flex-direction: column;
      padding: 4rem 2rem;
      background: #111;
    }
    .about-video video {
      width: 100%;
      height: auto;
      border-radius: 8px;
    }
    .about-text {
      padding: 2rem 0;
      font-size: 1.1rem;
    }
    .events {
      padding: 4rem 2rem;
      background: #000;
      text-align: center;
    }
    .event-grid {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 2rem;
      margin-top: 2rem;
    }
    .event-card {
      background: #222;
      padding: 2rem;
      border: 1px solid #444;
      border-radius: 8px;
      width: 300px;
      transition: 0.3s;
    }
    .event-card:hover {
      background: #fff;
      color: #000;
    }
    .sound {
      padding: 4rem 2rem;
      background: #111;
      text-align: center;
    }
    footer {
      padding: 2rem;
      background: #000;
      text-align: center;
    }
    .socials {
      margin: 1rem 0;
    }
    .socials a {
      margin: 0 1rem;
      transition: 0.2s;
    }
    .socials a:hover {
      color: #0ff;
    }
  </style>
</head>
<body>
  <section class="hero">
    <div class="hero-text">
      <h1>FVDEØUT.CAL</h1>
      <p>IMMERSIVE. UNFORGETTABLE. UNDERGROUND.</p>
      <a href="#about" class="btn">ENTER THE VOID</a>
    </div>
  </section>

  <section class="about" id="about">
    <div class="about-video">
      <video autoplay loop muted playsinline>
        <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
    <div class="about-text">
      <h2>We don’t do events. We engineer <em>experiences.</em></h2>
      <p>FVDEØUT.CAL is your gateway to curated clubbing chaos.<br>
      Techno. House. Experimental. No rules, just energy.</p>
    </div>
  </section>

  <section class="events">
    <h2>Upcoming Events</h2>
    <div class="event-grid">
      <div class="event-card">
        <h3>✹ FVD.RITUAL</h3>
        <p>Mumbai | 26.04.25</p>
        <p>Lineup: NASH | Xæon | Sifon</p>
        <a href="#" class="btn">RSVP</a>
      </div>
    </div>
  </section>

  <section class="sound">
    <h2>PRESS PLAY. GET LOST.</h2>
    <iframe src="https://open.spotify.com/embed/playlist/37i9dQZF1DX6VdMW310YC7" width="100%" height="80" frameborder="0" allowtransparency="true" allow="encrypted-media"></iframe>
  </section>

  <footer>
    <p>Stay plugged in.</p>
    <div class="socials">
      <a href="#">Instagram</a>
      <a href="#">X</a>
      <a href="#">Mail</a>
    </div>
    <p>© 2025 FVDEØUT.CAL</p>
  </footer>
</body>
</html>
