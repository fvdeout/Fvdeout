<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Sycko - Luxury Gen Z Fashion</title>
  <style>
    /* Reset & Base Styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background-color: #0d0d0d;
      color: #f2f2f2;
      line-height: 1.6;
      scroll-behavior: smooth;
    }

    a {
      text-decoration: none;
      color: #00ffe7;
    }

    img {
      max-width: 100%;
      display: block;
    }

    /* Animations */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes glow {
      0% { text-shadow: 0 0 5px #00ffe7; }
      50% { text-shadow: 0 0 20px #00ffe7, 0 0 10px #ff4ecd; }
      100% { text-shadow: 0 0 5px #00ffe7; }
    }

    /* Hero Section */
    .hero {
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #000000, #1a1a1a);
      text-align: center;
      animation: fadeIn 2s ease-in-out;
    }

    .hero h1 {
      font-size: 3rem;
      margin-bottom: 1rem;
      animation: glow 2s infinite alternate;
    }

    .highlight {
      color: #00ffe7;
    }

    .hero p {
      font-size: 1.2rem;
      margin-bottom: 2rem;
      color: #ccc;
    }

    .btn {
      display: inline-block;
      padding: 0.8rem 1.5rem;
      background: #00ffe7;
      color: #000;
      border-radius: 30px;
      font-weight: bold;
      transition: all 0.3s ease;
    }

    .btn:hover {
      background: #0fffc1;
      transform: scale(1.05);
    }

    /* Sections */
    section {
      padding: 4rem 2rem;
      max-width: 1200px;
      margin: auto;
    }

    .section-title {
      text-align: center;
      font-size: 2rem;
      margin-bottom: 2rem;
      color: #fff;
      position: relative;
    }

    .section-title::after {
      content: '';
      width: 60px;
      height: 3px;
      background: #00ffe7;
      display: block;
      margin: 0.5rem auto 2rem;
    }

    /* Product Grid */
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
    }

    .product-card {
      background: #1a1a1a;
      border-radius: 10px;
      overflow: hidden;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .product-card img {
      width: 100%;
      height: auto;
      object-fit: cover;
      transition: transform 0.3s ease;
    }

    .product-card:hover img {
      transform: scale(1.1);
    }

    .product-card h3 {
      padding: 1rem;
      font-size: 1.2rem;
      color: #fff;
    }

    .product-card p {
      padding: 0 1rem 0.5rem;
      color: #ccc;
    }

    .caption {
      font-size: 0.9rem;
      color: #aaa;
      padding: 0 1rem 1rem;
    }

    /* Instagram Section */
    .instagram {
      background: #111;
      text-align: center;
      padding: 3rem 2rem;
    }

    .instagram .btn {
      background: #ff4ecd;
      color: #fff;
    }

    .instagram .btn:hover {
      background: #ff6ee2;
    }

    /* Contact Section */
    .contact {
      text-align: center;
    }

    .contact .btn {
      background: #ff4ecd;
      color: #fff;
    }

    .contact .btn:hover {
      background: #ff6ee2;
    }

    /* Chatbot Widget */
    .chatbot {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 1000;
    }

    .chatbot button {
      background: #00ffe7;
      color: #000;
      border: none;
      padding: 1rem;
      border-radius: 50%;
      font-size: 1.2rem;
      cursor: pointer;
      box-shadow: 0 0 15px #00ffe7;
      transition: transform 0.2s ease;
    }

    .chatbot button:hover {
      transform: scale(1.1);
    }

    .chatbot-window {
      position: absolute;
      bottom: 70px;
      right: 0;
      width: 280px;
      background: #1a1a1a;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 0 20px rgba(0, 255, 231, 0.3);
      display: none;
      animation: fadeIn 0.5s ease-in-out;
    }

    .chat-header {
      background: #111;
      padding: 1rem;
      text-align: center;
      font-weight: bold;
      color: #fff;
      border-bottom: 1px solid #333;
    }

    .chat-body {
      padding: 1rem;
      font-size: 0.95rem;
      color: #ccc;
    }

    .chat-link {
      display: block;
      margin-top: 1rem;
      background: #ff4ecd;
      color: #fff;
      padding: 0.6rem 1rem;
      border-radius: 30px;
      text-align: center;
      transition: background 0.3s ease;
    }

    .chat-link:hover {
      background: #ff6ee2;
    }

    /* Footer */
    .footer {
      text-align: center;
      padding: 2rem;
      background: #000;
      color: #666;
      font-size: 0.9rem;
    }

    /* Responsive Design */
    @media (max-width: 768px) {
      .hero h1 {
        font-size: 2rem;
      }

      .section-title {
        font-size: 1.5rem;
      }

      .product-card h3 {
        font-size: 1rem;
      }

      .chatbot-window {
        width: 240px;
      }
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header class="hero">
    <div class="hero-content">
      <h1>Welcome to <span class="highlight">Sycko</span></h1>
      <p>Luxury meets Gen Z fashion.</p>
      <a href="#products" class="btn">Shop Now</a>
    </div>
  </header>

  <!-- Products -->
  <section id="products" class="products">
    <h2 class="section-title">Featured Collections</h2>
    <div class="product-grid">
      <div class="product-card">
        <img src="product1.jpg" alt="Glow Hoodie" />
        <h3>Glow Hoodie</h3>
        <p>$99</p>
        <p class="caption">Streetwear with a glow-in-the-dark twist.</p>
      </div>
      <div class="product-card">
        <img src="product2.jpg" alt="Chrome Joggers" />
        <h3>Chrome Joggers</h3>
        <p>$89</p>
        <p class="caption">Shiny, stylish, and ultra-comfy.</p>
      </div>
      <div class="product-card">
        <img src="product3.jpg" alt="Neon Logo Tee" />
        <h3>Neon Logo Tee</h3>
        <p>$49</p>
        <p class="caption">Bold colors that turn heads.</p>
      </div>
      <div class="product-card">
        <img src="product4.jpg" alt="Mirror Sneakers" />
        <h3>Mirror Sneakers</h3>
        <p>$129</p>
        <p class="caption">Step into the future of footwear.</p>
      </div>
      <div class="product-card">
        <img src="product5.jpg" alt="Sleek Bomber" />
        <h3>Sleek Bomber</h3>
        <p>$149</p>
        <p class="caption">A modern take on classic outerwear.</p>
      </div>
      <div class="product-card">
        <img src="product6.jpg" alt="Cyber Denim" />
        <h3>Cyber Denim</h3>
        <p>$139</p>
        <p class="caption">Edgy, futuristic, and totally Sycko.</p>
      </div>
    </div>
  </section>

  <!-- Instagram CTA -->
  <section class="instagram">
    <h2 class="section-title">Follow Us @syckofashion</h2>
    <p>Tag us in your looks & get featured!</p>
    <a href="https://instagram.com/syckofashion" target="_blank" class="btn">Visit Instagram</a>
  </section>

  <!-- Contact -->
  <section id="contact" class="contact">
    <h2 class="section-title">Get In Touch</h2>
    <p>We’d love to hear from you. Questions? Orders? Collaborations?</p>
    <a href="mailto:hello@sycko.com" class="btn">Email Us</a>
  </section>

  <!-- Chatbot -->
  <div class="chatbot">
    <button id="chatbot-toggle"><i class="fas fa-comment-dots"></i></button>
    <div class="chatbot-window" id="chatbot-window">
      <div class="chat-header">Need help?</div>
      <div class="chat-body">
        <p>Hi 👋 How can we assist you today?</p>
        <a href="https://instagram.com/syckofashion" target="_blank" class="chat-link">Message us on Instagram</a>
      </div>
    </div>
  </div>

  <!-- Font Awesome Icons -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/js/all.min.js"></script>

  <!-- JavaScript for Chatbot -->
  <script>
    document.getElementById('chatbot-toggle').addEventListener('click', function () {
      const chatbotWindow = document.getElementById('chatbot-window');
      chatbotWindow.style.display = chatbotWindow.style.display === 'block' ? 'none' : 'block';
    });
  </script>

  <!-- Footer -->
  <footer class="footer">
    <p>&copy; 2025 Sycko. All rights reserved.</p>
  </footer>

</body>
</html>
