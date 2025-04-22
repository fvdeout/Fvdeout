<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>FVDEØUT.CAL</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500&family=Montserrat:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }
    body {
      font-family: 'Montserrat', sans-serif;
      background-color: #0a0a0a;
      color: #ffffff;
      line-height: 1.8;
      transition: background-color 0.5s ease, color 0.5s ease;
    }
    header {
      padding: 100px 20px;
      text-align: center;
      background: url('your-image-path-here.jpg') no-repeat center center fixed;
      background-size: cover;
      transition: background 0.5s ease;
      color: #ffffff;
      text-shadow: 4px 4px 10px rgba(0, 0, 0, 0.7);
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.8);
    }
    header h1 {
      font-family: 'Orbitron', sans-serif;
      font-size: 5rem;
      margin-bottom: 15px;
      color: #ff00cc;
      text-transform: uppercase;
      letter-spacing: 3px;
      transition: color 0.3s ease;
    }
    header p {
      font-size: 1.5rem;
      color: #bbbbbb;
      transition: color 0.3s ease;
    }
    section {
      padding: 80px 20px;
      max-width: 1200px;
      margin: auto;
      opacity: 0;
      transform: translateY(40px);
      animation: fadeInUp 1.2s ease forwards;
      background-color: rgba(0, 0, 0, 0.7);
      border-radius: 10px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.7);
    }
    section:nth-of-type(2) {
      animation-delay: 0.3s;
    }
    section:nth-of-type(3) {
      animation-delay: 0.6s;
    }
    section:nth-of-type(4) {
      animation-delay: 0.9s;
    }
    section:nth-of-type(5) {
      animation-delay: 1.2s;
    }
    h2 {
      font-size: 3rem;
      margin-bottom: 25px;
      border-left: 6px solid #ff00cc;
      padding-left: 15px;
      color: #ffffff;
      text-transform: uppercase;
      font-weight: bold;
      letter-spacing: 2px;
    }
    p {
      font-size: 1.2rem;
      color: #dddddd;
      margin-bottom: 15px;
    }
    .contact a {
      color: #ff00cc;
      text-decoration: none;
      font-weight: bold;
      text-transform: uppercase;
      transition: all 0.3s ease;
    }
    .contact a:hover {
      color: #ffffff;
      text-shadow: 0 0 10px #ff00cc;
    }
    footer {
      text-align: center;
      padding: 40px 20px;
      background: #111;
      font-style: italic;
      color: #888;
      transition: background 0.5s ease;
      font-size: 1.1rem;
    }
    .image-border {
      border: 5px solid #ff00cc;
      border-radius: 10px;
      margin: 20px 0;
    }
    .image-cut {
      clip-path: polygon(0 0, 100% 0, 90% 100%, 10% 100%);
    }
    .bg-dark-overlay {
      background-color: rgba(0, 0, 0, 0.8);
      padding: 20px;
      border-radius: 10px;
    }
    .highlight {
      color: #ff00cc;
      font-weight: bold;
    }
    .bold-text {
      font-weight: 700;
    }
    .neon-text {
      color: #ff00cc;
      text-shadow: 0 0 10px #ff00cc, 0 0 20px #ff00cc, 0 0 30px #ff00cc;
    }
    .btn {
      background: #ff00cc;
      padding: 10px 30px;
      border-radius: 30px;
      color: #fff;
      text-decoration: none;
      font-weight: bold;
      transition: all 0.3s ease;
    }
    .btn:hover {
      background: #ffffff;
      color: #ff00cc;
      transform: scale(1.1);
    }
    @keyframes fadeInUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    @media (max-width: 768px) {
      header h1 {
        font-size: 3rem;
      }
      header p {
        font-size: 1.2rem;
      }
      h2 {
        font-size: 2rem;
      }
      section {
        padding: 40px 15px;
      }
      body {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>FVDEØUT.CAL</h1>
    <p class="neon-text">The night is limitless. We take you beyond the boundaries. Raw beats. Unforgettable moments. Energy that pulls you in.</p>
  </header>

  <section>
    <h2>About Us</h2>
    <p>
      FVDEØUT.CAL isn't just about parties; it's about crafting <span class="highlight">unforgettable experiences</span>. Our events are where the underground beats meet high-energy crowds and a world that pulsates with life. From secret locations to immersive soundscapes, we turn every night into a <span class="bold-text">masterpiece</span>.
    </p>
    <div class="bg-dark-overlay">
      <p>
        We don't just host events—we create worlds where every moment is etched into your memory. <span class="highlight">Step into the future of nightlife</span>, where you’re not just an attendee but part of the vibe.
      </p>
    </div>
  </section>

  <section>
    <h2>What We Do</h2>
    <p><strong>Immersive Techno Nights:</strong> Dive into a night filled with electrifying beats and mind-blowing visuals. We bring you the best underground and rising techno artists.</p>
    <p><strong>Exclusive DJ Lineups:</strong> Only the best. We work with top-tier DJs who command the decks and keep the crowd moving all night.</p>
    <p><strong>Secret, Hidden Venues:</strong> No boring venues here. From hidden clubs to rooftop raves, we create spaces that push the limits of imagination and make every night a celebration.</p>
    <div>
      <img src="your-image-path-here.jpg" alt="Techno DJ Set" class="image-border image-cut" style="width:100%; height:auto;">
    </div>
  </section>

  <section>
    <h2>Gallery</h2>
    <p>We capture the moments that make every night unforgettable. Coming soon: exclusive photos and videos from our electrifying events.</p>
    <div>
      <img src="your-image-path-here.jpg" alt="Club Party" class="image-border" style="width:100%; height:auto;">
      <img src="your-image-path-here.jpg" alt="Champagne Shower" class="image-border" style="width:100%; height:auto;">
    </div>
  </section>

  <section class="contact">
    <h2>Contact / Bookings</h2>
    <p>Want to be part of the magic? Collaborate with us, book a party, or ask about upcoming events. Let’s make it happen.</p>
    <p>📲 Instagram: <a href="https://instagram.com/fvdeout.cal" target="_blank">@fvdeout.cal</a></p>
    <p>📞 +91 62915 89401</p>
    <p>📍 Based in Kolkata</p>
    <a href="https://instagram.com/fvdeout.cal" class="btn">Follow us</a>
  </section>

  <footer>
    The night pulls you in, the rest fades out.
  </footer>
</body>
</html>
