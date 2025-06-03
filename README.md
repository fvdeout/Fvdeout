
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
      scroll-behavior: smooth;
    }

    body, html {
      height: 100%;
      font-family: 'Poppins', sans-serif;
      background-color: #000;
      color: #fff;
      overflow-x: hidden;
      background-size: cover;
      background-position: center;
      transition: background-image 0.5s ease;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.6);
      z-index: 0;
    }

    .content {
      position: relative;
      z-index: 1;
      opacity: 0;
      animation: fadeIn 1s ease forwards;
      animation-delay: 1s;
      animation-fill-mode: forwards;
    }

    @keyframes fadeIn {
      to { opacity: 1; }
    }

    /* Preloader */
    .preloader {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: #000;
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      animation: fadeOut 1s ease forwards;
    }

    @keyframes fadeOut {
      to { opacity: 0; visibility: hidden; }
    }

    /* Upload Background */
    .upload-bg {
      text-align: center;
      margin: 2rem auto;
    }

    .upload-bg input[type="file"] {
      display: none;
    }

    .upload-bg label {
      display: inline-block;
      padding: 0.6rem 1.2rem;
      background: #00ffe7;
      color: #000;
      border-radius: 30px;
      cursor: pointer;
      font-weight: bold;
      transition: 0.3s;
    }

    .upload-bg label:hover {
      background: #0fffc1;
    }

    .upload-bg button.reset-btn {
      margin-left: 1rem;
      background: transparent;
      border: 1px solid #ff4ecd;
      color: #ff4ecd;
      padding: 0.5rem 1rem;
      border-radius: 30px;
      cursor: pointer;
    }

    .upload-bg button.reset-btn:hover {
      background: #ff4ecd;
      color: #fff;
    }

    /* Floating Cart Icon */
    .cart-icon {
      position: fixed;
      bottom: 20px;
      right: 20px;
      cursor: pointer;
      font-size: 1.5rem;
      color: #00ffe7;
      background: #fff;
      padding: 1rem;
      border-radius: 50%;
      box-shadow: 0 0 10px #00ffe7;
      z-index: 999;
    }

    /* Product Filters */
    .filters {
      text-align: center;
      margin: 2rem 0;
    }

    .filters button {
      background: transparent;
      border: 1px solid #00ffe7;
      color: #00ffe7;
      padding: 0.5rem 1rem;
      margin: 0 0.5rem;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
    }

    .filters button.active,
    .filters button:hover {
      background: #00ffe7;
      color: #000;
    }

    /* Product Grid */
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      padding: 2rem;
    }

    .product-card {
      background: #111;
      border-radius: 10px;
      overflow: hidden;
      text-align: center;
      animation: fadeInUp 0.6s ease-in-out;
    }

    .product-card img {
      width: 100%;
      height: auto;
      object-fit: cover;
    }

    .product-info {
      padding: 1rem;
    }

    .product-info h3 {
      font-size: 1.1rem;
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

    .product-info button {
      background: #00ffe7;
      color: #000;
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 30px;
      cursor: pointer;
      font-weight: bold;
    }

    /* Shopping Cart Modal */
    .cart-modal {
      display: none;
      position: fixed;
      top: 20px;
      right: 80px;
      width: 300px;
      background: #111;
      border-radius: 10px;
      padding: 1rem;
      box-shadow: 0 0 10px rgba(0, 255, 231, 0.3);
      z-index: 999;
      max-height: 80vh;
      overflow-y: auto;
    }

    .cart-item {
      display: flex;
      justify-content: space-between;
      margin-bottom: 1rem;
      border-bottom: 1px solid #333;
      padding-bottom: 0.5rem;
    }

    .cart-item span {
      display: inline-block;
      margin: 0 0.5rem;
    }

    .cart-actions button {
      background: none;
      color: #00ffe7;
      border: none;
      font-size: 1.2rem;
      cursor: pointer;
    }

    .cart-total {
      text-align: right;
      margin-top: 1rem;
      font-weight: bold;
    }

    .checkout-btn {
      display: block;
      margin-top: 1rem;
      background: #ff4ecd;
      color: #fff;
      padding: 0.6rem 1rem;
      border-radius: 30px;
      text-align: center;
      font-weight: bold;
      transition: 0.3s;
    }

    .checkout-btn:hover {
      background: #ff6ee2;
    }

    /* Instagram Popup */
    .social-popup {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.9);
      z-index: 9999;
      justify-content: center;
      align-items: center;
    }

    .social-content {
      background: #111;
      color: #fff;
      padding: 2rem;
      border-radius: 10px;
      text-align: center;
    }

    .popup-close {
      position: absolute;
      top: 10px;
      right: 20px;
      font-size: 1.5rem;
      color: #fff;
      cursor: pointer;
    }

    footer.footer {
      text-align: center;
      margin: 4rem 0 2rem;
      font-size: 0.9rem;
      color: #555;
    }

    @media (max-width: 600px) {
      .cart-modal {
        right: 20px;
        width: 90%;
      }
    }
  </style>
</head>
<body id="page">

  <!-- Preloader -->
  <div class="preloader" id="preloader"></div>

  <!-- Upload Background -->
  <div class="upload-bg">
    <label for="bgUpload">Upload Background</label>
    <input type="file" id="bgUpload" accept="image/*" onchange="uploadBackground(this)">
    <button class="reset-btn" onclick="resetBackground()">Reset</button>
  </div>

  <!-- Main Content -->
  <div class="content" id="mainContent">

    <!-- Filters -->
    <div class="filters">
      <button onclick="filterProducts('all')" class="active">All</button>
      <button onclick="filterProducts('small')">S</button>
      <button onclick="filterProducts('medium')">M</button>
      <button onclick="filterProducts('large')">L</button>
    </div>

    <!-- Products -->
    <section class="products" id="products">
      <!-- Filled by JS -->
    </section>

    <!-- Footer -->
    <footer class="footer">
      &copy; 2025 Sycko. All rights reserved.
    </footer>

  </div>

  <!-- Floating Cart Icon -->
  <div class="cart-icon" onclick="toggleCart()">🛒 (<span id="cart-count">0</span>)</div>

  <!-- Cart Modal -->
  <div id="cartModal" class="cart-modal">
    <h3>Your Cart</h3>
    <div id="cartItems"></div>
    <div class="cart-total">Total: ₹<span id="cartTotal">0</span></div>
    <a href="#" id="checkoutBtn" class="checkout-btn" target="_blank">Checkout (DM us on Instagram)</a>
  </div>

  <!-- Instagram Modal -->
  <div id="socialPopup" class="social-popup">
    <div class="social-content">
      <span class="popup-close" onclick="closeSocialPopup()">&times;</span>
      <h2>Follow Us on Instagram</h2>
      <p>@syckofashion</p>
      <a href="https://instagram.com/syckofashion" target="_blank" class="btn">Send DM</a>
    </div>
  </div>

  <script>
    // Product Data
    const products = [
      {
        id: 1,
        name: "Stranger Things T-Shirt",
        price: 799,
        caption: "Immerse yourself in elevated comfort with this relaxed-fit Stranger Things tee—crafted from premium heavy gauge bio-cotton for a soft, breathable feel. Inspired by the Upside Down, designed for all-day luxury.",
        size: "small",
        image: "product1.jpg"
      },
      {
        id: 2,
        name: "Minecraft T-Shirt",
        price: 749,
        caption: "Built for real-world adventures—this relaxed-fit Minecraft tee is crafted from ultra-soft, heavy gauge bio-cotton, blending pixel-perfect design with all-day breathable comfort. Crafted to survive, styled to stand out.",
        size: "medium",
        image: "product2.jpg"
      },
      {
        id: 3,
        name: "Cyberpunk Jacket",
        price: 1299,
        caption: "Bold and futuristic jacket inspired by digital culture. Perfect for any streetwear look.",
        size: "large",
        image: "product3.jpg"
      },
      {
        id: 4,
        name: "Neon Logo Hoodie",
        price: 899,
        caption: "Stand out in our neon logo hoodie — ultra-comfy cotton with glowing details.",
        size: "small",
        image: "product4.jpg"
      },
      {
        id: 5,
        name: "Mirror Sneakers",
        price: 1499,
        caption: "Step into the future of footwear with these reflective mirror sneakers.",
        size: "medium",
        image: "product5.jpg"
      }
    ];

    let cart = [];

    window.onload = () => {
      const savedCart = localStorage.getItem("cart");
      if (savedCart) cart = JSON.parse(savedCart);

      const savedBg = localStorage.getItem("customBg");
      if (savedBg) document.body.style.backgroundImage = `url('${savedBg}')`;

      renderProducts();
      updateCart();
    };

    function saveCart() {
      localStorage.setItem("cart", JSON.stringify(cart));
    }

    function filterProducts(size) {
      const buttons = document.querySelectorAll(".filters button");
      buttons.forEach(btn => btn.classList.remove("active"));
      event.target.classList.add("active");

      const container = document.getElementById("products");
      container.innerHTML = "";
      products.filter(p => size === "all" || p.size === size).forEach(product => {
        const div = document.createElement("div");
        div.className = "product-card";
        div.innerHTML = `
          <img src="${product.image}" alt="${product.name}">
          <div class="product-info">
            <h3>${product.name}</h3>
            <div class="price">₹${product.price}</div>
            <button onclick="addToCart(${product.id})">Add to Cart</button>
          </div>
        `;
        container.appendChild(div);
      });
    }

    function renderProducts() {
      const container = document.getElementById("products");
      container.innerHTML = "";
      products.forEach(product => {
        const div = document.createElement("div");
        div.className = "product-card";
        div.innerHTML = `
          <img src="${product.image}" alt="${product.name}">
          <div class="product-info">
            <h3>${product.name}</h3>
            <div class="price">₹${product.price}</div>
            <button onclick="addToCart(${product.id})">Add to Cart</button>
          </div>
        `;
        container.appendChild(div);
      });
    }

    function addToCart(id) {
      const product = products.find(p => p.id === id);
      const existing = cart.find(item => item.id === id);
      if (existing) {
        existing.qty++;
      } else {
        cart.push({ ...product, qty: 1 });
      }
      saveCart();
      updateCart();
      toggleCart();
    }

    function updateCart() {
      const cartItems = document.getElementById("cartItems");
      const cartTotal = document.getElementById("cartTotal");
      const cartCount = document.getElementById("cart-count");
      cartItems.innerHTML = "";

      let total = 0;

      cart.forEach((item, index) => {
        total += item.price * item.qty;
        cartItems.innerHTML += `
          <div class="cart-item">
            <span>${item.name} x ${item.qty}</span>
            <div class="cart-actions">
              <button onclick="changeQty(${index}, 1)">+</button>
              <button onclick="changeQty(${index}, -1)">−</button>
              <button onclick="removeItem(${index})">🗑️</button>
            </div>
          </div>
        `;
      });

      cartTotal.textContent = total.toFixed(2);
      cartCount.textContent = cart.reduce((acc, item) => acc + item.qty, 0);
      document.getElementById("checkoutBtn").href = `https://instagram.com/direct/new?text=Hi+Sycko!+I+want+to+order:+${cart.map(i => i.name + ' x' + i.qty).join(', ')}`;
    }

    function changeQty(index, delta) {
      cart[index].qty += delta;
      if (cart[index].qty <= 0) cart.splice(index, 1);
      saveCart();
      updateCart();
    }

    function removeItem(index) {
      cart.splice(index, 1);
      saveCart();
      updateCart();
    }

    function toggleCart() {
      const cartModal = document.getElementById("cartModal");
      cartModal.style.display = cartModal.style.display === "block" ? "none" : "block";
    }

    // Instagram Scroll Popup
    window.addEventListener("scroll", () => {
      if (window.scrollY > 500 && !localStorage.getItem("instaShown")) {
        openSocialPopup();
        localStorage.setItem("instaShown", true);
      }
    });

    function openSocialPopup() {
      document.getElementById("socialPopup").style.display = "flex";
    }

    function closeSocialPopup() {
      document.getElementById("socialPopup").style.display = "none";
    }

    // Upload Background
    function uploadBackground(input) {
      const file = input.files[0];
      if (!file) return;

      const reader = new FileReader();
      reader.onload = function(e) {
        const url = e.target.result;
        document.body.style.backgroundImage = `url('${url}')`;
        localStorage.setItem("customBg", url);
      };
      reader.readAsDataURL(file);
    }

    function resetBackground() {
      document.body.style.backgroundImage = "none";
      localStorage.removeItem("customBg");
    }

    // Loader
    window.addEventListener("load", () => {
      document.getElementById("preloader").classList.add("loaded");
      document.getElementById("mainContent").style.opacity = "1";
    });
  </script>

</body>
</html>
