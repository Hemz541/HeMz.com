<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>HeMz - Spices & Clothing</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f8f8f8;
    }
    header {
      background-color: #d62828;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav {
      display: flex;
      justify-content: center;
      background: #f1f1f1;
      padding: 10px;
    }
    nav a {
      margin: 0 15px;
      color: #333;
      text-decoration: none;
      font-weight: bold;
    }
    .hero {
      background: url('https://via.placeholder.com/1200x400?text=Spices+%2B+Clothing+by+HeMz') center/cover no-repeat;
      height: 400px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 2em;
      font-weight: bold;
      text-shadow: 2px 2px 5px black;
    }
    section {
      padding: 40px 20px;
      max-width: 1200px;
      margin: auto;
    }
    .section-title {
      text-align: center;
      margin-bottom: 30px;
      font-size: 1.8em;
      color: #333;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
    }
    .product {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      text-align: center;
    }
    .product img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 8px;
    }
    .product h3 {
      margin: 10px 0 5px;
      font-size: 1.1em;
    }
    .product button {
      background: #d62828;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
      margin: 5px;
    }
    footer {
      background: #333;
      color: white;
      text-align: center;
      padding: 15px 0;
      margin-top: 40px;
    }
    #cart {
      position: fixed;
      top: 10px;
      right: 10px;
      background: #fff;
      border: 1px solid #ccc;
      padding: 10px;
      border-radius: 8px;
      z-index: 999;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }
    #whatsapp-button {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: #25d366;
      color: white;
      border-radius: 50%;
      padding: 15px;
      text-align: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.3);
      z-index: 999;
      font-size: 20px;
      text-decoration: none;
    }
  </style>
</head>
<body>
  <div id="cart">🛒 Cart: <span id="cart-count">0</span></div>
  <a href="https://wa.me/94XXXXXXXXX" target="_blank" id="whatsapp-button">💬</a>

  <header>
    <h1>HeMz - Natural Spices & Stylish Clothing</h1>
  </header>
  <nav>
    <a href="#spices">Spices</a>
    <a href="#clothing">Clothing</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
  <div class="hero">
    Pure Taste & True Style
  </div>

  <section id="spices">
    <h2 class="section-title">Our Spices</h2>
    <div class="products">
      <div class="product">
        <img src="https://via.placeholder.com/200x180?text=Curry+Masala" alt="Curry Masala">
        <h3>Curry Masala</h3>
        <button onclick="addToCart()">Add to Cart</button>
        <button onclick="payNow('Curry Masala', '5.00')">Pay Now</button>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/200x180?text=Pepper+Powder" alt="Pepper">
        <h3>Pepper Powder</h3>
        <button onclick="addToCart()">Add to Cart</button>
        <button onclick="payNow('Pepper Powder', '4.50')">Pay Now</button>
      </div>
    </div>
  </section>

  <section id="clothing">
    <h2 class="section-title">Our Clothing</h2>
    <div class="products">
      <div class="product">
        <img src="https://via.placeholder.com/200x180?text=HeMz+T-Shirt" alt="HeMz T-Shirt">
        <h3>HeMz Casual T-Shirt</h3>
        <button onclick="addToCart()">Add to Cart</button>
        <button onclick="payNow('HeMz T-Shirt', '8.00')">Pay Now</button>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/200x180?text=Gym+Wear" alt="Gym Wear">
        <h3>Gym Wear</h3>
        <button onclick="addToCart()">Add to Cart</button>
        <button onclick="payNow('Gym Wear', '10.00')">Pay Now</button>
      </div>
    </div>
  </section>

  <section id="about">
    <h2 class="section-title">About Us</h2>
    <p style="max-width: 800px; margin: auto; text-align: center;">
      Welcome to HeMz! We are a Sri Lankan home-based business offering naturally prepared spices and stylish casual wear. Every spice is ground with care, and every T-shirt is designed with passion. Join us in celebrating flavor and fashion together.
    </p>
  </section>

  <section id="contact">
    <h2 class="section-title">Contact Us</h2>
    <p style="text-align:center;">
      📞 WhatsApp: <a href="https://wa.me/94XXXXXXXXX">Chat Now</a><br>
      📧 Email: support@hemzstore.com
    </p>
  </section>

  <footer>
    &copy; 2025 HeMz Spices & Clothing. All rights reserved.
  </footer>

  <script>
    let cartCount = 0;
    function addToCart() {
      cartCount++;
      document.getElementById('cart-count').innerText = cartCount;
    }

    function payNow(item, price) {
      alert(`Redirecting to payment gateway for ${item} - $${price}`);
      // Simulate redirect or integrate real payment later
    }
  </script>
</body>
</html>
