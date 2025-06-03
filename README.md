<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Sycko - Luxury Gen Z Fashion</title>
  <style>
    /* Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body, html {
      height: 100%;
      font-family: 'Poppins', sans-serif;
      background: url('https://images.unsplash.com/photo-1606079942367-d4a3875f5b9c?auto=format&fit=crop&w=1950&q=80') no-repeat center center fixed;
      background-size: cover;
      color: #fff;
      line-height: 1.6;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.6);
      z-index: 0;
    }

    .content {
      position: relative;
      z-index: 1;
      max-width: 1200px;
      margin: auto;
      padding: 2rem;
    }

    /* Navigation */
    nav.top-nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      background: rgba(0, 0, 0, 0.6);
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 999;
    }

    nav.top-nav .logo {
      font-size: 1.5rem;
      font-weight: bold;
      color: #00ffe7;
    }

    nav.top-nav .menu-toggle {
      display: none;
      font-size: 1.5rem;
      cursor: pointer;
    }

    nav.top-nav ul {
      list-style: none;
      display: flex;
      gap: 2rem;
    }

    nav.top-nav ul li a {
      color: #fff;
      text-decoration: none;
      font-weight: 500;
    }

    @media (max-width: 768px) {
      nav.top-nav ul {
        display: none;
        flex-direction: column;
        background: rgba(0, 0, 0, 0.95);
        position: absolute;
        top: 60px;
        right: 0;
        width: 200px;
      }

      nav.top-nav ul.show {
        display: flex;
      }

      nav.top-nav .menu-toggle {
        display: block;
      }
    }

    /* Hero Section */
    header.hero {
      text-align: center;
      padding: 8rem 2rem 4rem;
    }

    header h1 {
      font-size: 3rem;
      font-weight: 600;
      color: #fff;
      margin-bottom: 1rem;
    }

    header p {
      font-size: 1.2rem;
      color: #ccc;
      margin-bottom: 2rem;
    }

    .btn {
      display: inline-block;
      background: #fff;
      color: #000;
      padding: 0.8rem 2rem;
      border-radius: 30px;
      font-weight: bold;
      transition: all 0.3s ease;
      text-decoration: none;
    }

    .btn:hover {
      background: #f0f0f0;
      transform: translateY(-2px);
    }

    /* Product Grid */
    .products {
      display: flex;
      overflow-x: auto;
      gap: 1.5rem;
      padding-bottom: 1rem;
      scroll-snap-type: x mandatory;
      -webkit-overflow-scrolling: touch;
      margin-top: 4rem;
    }

    .product-card {
      min-width: 280px;
      background: rgba(255, 255, 255, 0.05);
      border-radius: 10px;
      overflow: hidden;
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      cursor: pointer;
      scroll-snap-align: start;
      transition: transform 0.2s ease;
    }

    .product-card:hover {
      transform: scale(1.03);
    }

    .product-card img {
      width: 100%;
      height: auto;
      object-fit: cover;
    }

    .product-info {
      padding: 1.5rem;
    }

    .product-info h3 {
      font-size: 1.2rem;
      margin-bottom: 0.5rem;
    }

    .product-info .price {
      color: #ccc;
      font-size: 1rem;
      margin-bottom: 0.5rem;
    }

    .product-info .caption {
      font-size: 0.9rem;
      color: #aaa;
      margin-bottom: 1rem;
    }

    .sizes {
      font-size: 0.85rem;
      color: #999;
      margin-bottom: 1rem;
    }

    .note {
      font-size: 0.8rem;
      color: #666;
    }

    /* Shopping Cart Modal */
    .cart-icon {
      cursor: pointer;
      font-size: 1.2rem;
      color: #fff;
      margin-left: 1rem;
    }

    .cart-modal {
      display: none;
      position: fixed;
      top: 60px;
      right: 20px;
      width: 300px;
      background: #111;
      border-radius: 10px;
      padding: 1rem;
      box-shadow: 0 0 10px rgba(0, 255, 231, 0.3);
      z-index: 999;
    }

    .cart-item {
      display: flex;
      justify-content: space-between;
      margin-bottom: 1rem;
    }

    .cart-total {
      text-align: right;
      margin-top: 1rem;
      font-weight: bold;
    }

    /* Popup Styles */
    .popup {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.85);
      z-index: 9999;
      justify-content: center;
      align-items: center;
      overflow-y: auto;
    }

    .popup-content {
      background: #111;
      color: #fff;
      padding: 2rem;
      border-radius: 10px;
      max-width: 600px;
      width: 90%;
      position: relative;
      text-align: center;
      margin: 2rem auto;
    }

    .popup-close {
      position: absolute;
      top: 10px;
      right: 20px;
      font-size: 1.5rem;
      color: #fff;
      cursor: pointer;
    }

    .popup img {
      max-width: 100%;
      border-radius: 8px;
      margin-bottom: 1rem;
    }

    footer.footer {
      margin-top: 4rem;
      text-align: center;
      font-size: 0.9rem;
      color: #555;
    }

    @media (max-width: 768px) {
      header h1 {
        font-size: 2rem;
      }

      .btn {
        font-size: 0.9rem;
      }

      .popup-content {
        margin: 1rem auto;
        padding: 1rem;
      }

      .popup img {
        width: 100%;
      }
    }
  </style>
</head>
<body>

  <div class="overlay"></div>

  <!-- Top Navigation -->
  <nav class="top-nav">
    <div class="logo">Sycko</div>
    <div class="cart-icon" onclick="toggleCart()">🛒 (<span id="cart-count">0</span>)</div>
    <ul id="menu">
      <li><a href="#products">Shop</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="menu-toggle" onclick="toggleMenu()">&#9776;</div>
  </nav>

  <div class="content">

    <!-- Hero Section -->
    <header class="hero">
      <h1>Sycko</h1>
      <p>Where luxury meets Gen Z fashion.</p>
      <a href="#products" class="btn">Shop Now</a>
    </header>

    <!-- Products -->
    <section id="products" class="products">
      <!-- Product 1 -->
      <div class="product-card" onclick="openPopup('popup1')">
        <img src="https://via.placeholder.com/600x800?text=Stranger+Things+T-Shirt" alt="Stranger Things T-Shirt" />
        <div class="product-info">
          <h3>Stranger Things T-Shirt</h3>
          <div class="price">₹799</div>
          <div class="caption">Elevated comfort in premium bio-cotton, inspired by the Upside Down.</div>
          <div class="sizes">Sizes: Small | Medium | Large</div>
          <div class="note">Order via Instagram only</div>
        </div>
      </div>

      <!-- Product 2 -->
      <div class="product-card" onclick="openPopup('popup2')">
        <img src="https://via.placeholder.com/600x800?text=Minecraft+T-Shirt" alt="Minecraft T-Shirt" />
        <div class="product-info">
          <h3>Minecraft T-Shirt</h3>
          <div class="price">₹749</div>
          <div class="caption">Pixel-perfect design with breathable comfort. Crafted to stand out.</div>
          <div class="sizes">Sizes: Small | Medium | Large</div>
          <div class="note">Order via Instagram only</div>
        </div>
      </div>
    </section>

    <!-- Popups -->
    <div id="popup1" class="popup">
      <div class="popup-content">
        <span class="popup-close" onclick="closePopup('popup1')">&times;</span>
        <img src="https://via.placeholder.com/600x800?text=Stranger+Things+T-Shirt" alt="Stranger Things T-Shirt" />
        <h2>Stranger Things T-Shirt</h2>
        <p class="price">₹799</p>
        <p>Elevated comfort in premium bio-cotton, inspired by the Upside Down.</p>
        <p><strong>Sizes:</strong> Small, Medium, Large</p>
        <p><strong>Note:</strong> Orders accepted only through Instagram.</p>
        <button onclick="addToCart('Stranger Things T-Shirt', 799)">Add to Cart</button>
      </div>
    </div>

    <div id="popup2" class="popup">
      <div class="popup-content">
        <span class="popup-close" onclick="closePopup('popup2')">&times;</span>
        <img src="https://via.placeholder.com/600x800?text=Minecraft+T-Shirt" alt="Minecraft T-Shirt" />
        <h2>Minecraft T-Shirt</h2>
        <p class="price">₹749</p>
        <p>Pixel-perfect design with breathable comfort. Crafted to stand out.</p>
        <p><strong>Sizes:</strong> Small, Medium, Large</p>
        <p><strong>Note:</strong> Orders accepted only through Instagram.</p>
        <button onclick="addToCart('Minecraft T-Shirt', 749)">Add to Cart</button>
      </div>
    </div>

    <!-- Shopping Cart Modal -->
    <div id="cartModal" class="cart-modal">
      <h3>Your Cart</h3>
      <div id="cartItems"></div>
      <div class="cart-total">Total: ₹<span id="cartTotal">0</span></div>
    </div>

    <!-- Footer -->
    <footer class="footer">
      &copy; 2025 Sycko. All rights reserved.
    </footer>

  </div>

  <!-- JavaScript -->
  <script>
    // Mobile Menu Toggle
    function toggleMenu() {
      const menu = document.getElementById("menu");
      menu.classList.toggle("show");
    }

    // Popup Functions
    function openPopup(id) {
      document.getElementById(id).style.display = "flex";
    }

    function closePopup(id) {
      document.getElementById(id).style.display = "none";
    }

    // Shopping Cart Logic
    let cart = [];

    function addToCart(productName, price) {
      cart.push({ name: productName, price: price });
      updateCart();
      openCart();
    }

    function updateCart() {
      const cartItems = document.getElementById("cartItems");
      const cartTotal = document.getElementById("cartTotal");
      const cartCount = document.getElementById("cart-count");

      cartItems.innerHTML = "";
      let total = 0;

      cart.forEach((item, index) => {
        total += item.price;
        cartItems.innerHTML += `<div class="cart-item"><span>${item.name}</span><span>₹${item.price}</span></div>`;
      });

      cartTotal.textContent = total.toFixed(2);
      cartCount.textContent = cart.length;
    }

    function toggleCart() {
      const cartModal = document.getElementById("cartModal");
      cartModal.style.display = cartModal.style.display === "block" ? "none" : "block";
    }

    function openCart() {
      document.getElementById("cartModal").style.display = "block";
    }

    window.addEventListener("click", function(e){
      const cartModal = document.getElementById("cartModal");
      if (e.target == cartModal) {
        cartModal.style.display = "none";
      }
    });
  </script>

</body>
</html>
