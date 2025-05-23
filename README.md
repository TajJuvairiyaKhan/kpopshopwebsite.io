<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>K-Pop Merch Shop</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background-color: #fdf6f0;
      color: #333;
    }

    header {
      background-color: #ff7eb3;
      padding: 20px;
      text-align: center;
      color: white;
    }

    nav ul {
      list-style: none;
      padding: 0;
      display: flex;
      justify-content: center;
      gap: 20px;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }

    .hero {
      background-image: url('https://d31xsmoz1lk3y3.cloudfront.net/games/imgur/QWgiBqv.jpg');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      height: 400px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
      padding: 20px;
      position: relative;
    }

    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(0, 0, 0, 0.5);
      z-index: 1;
    }

    .hero h2,
    .hero p,
    .hero .btn {
      position: relative;
      z-index: 2;
    }

    .hero h2 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    .hero p {
      font-size: 1.2rem;
      margin-bottom: 20px;
    }

    .hero .btn {
      background-color: #ff69b4;
      color: white;
      padding: 12px 25px;
      border-radius: 25px;
      text-decoration: none;
      font-weight: bold;
      transition: background 0.3s ease;
    }

    .hero .btn:hover {
      background-color: #ff1493;
    }

    main {
      padding: 20px;
      text-align: center;
    }

    .products {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 30px;
      margin-top: 20px;
    }

    .product {
      background-color: white;
      padding: 15px;
      border-radius: 10px;
      width: 200px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }

    .product img {
      width: 100%;
      border-radius: 10px;
    }

    button {
      background-color: #ff69b4;
      color: white;
      border: none;
      padding: 10px;
      margin-top: 10px;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background-color: #ff1493;
    }

    .contact {
      background-color: #fff0f5;
      padding: 40px 20px;
      text-align: center;
    }

    .contact h2 {
      color: #ff1493;
      font-size: 2rem;
      margin-bottom: 10px;
    }

    .contact p {
      font-size: 1.1rem;
      margin-bottom: 30px;
    }

    .contact form {
      max-width: 500px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    .contact input,
    .contact textarea {
      padding: 10px;
      border: 2px solid #ffb6c1;
      border-radius: 8px;
      font-size: 1rem;
    }

    .contact button {
      background-color: #ff69b4;
      color: white;
      border: none;
      padding: 12px;
      border-radius: 25px;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    .contact button:hover {
      background-color: #ff1493;
    }

    footer {
      text-align: center;
      padding: 10px;
      background-color: #eee;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <header>
    <h1>K-POP Merch Store</h1>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Merch</a></li>
        <li><a href="#">Contact</a></li>
        <li><a href="#" id="cart-btn">🛒 Cart (<span id="cart-count">0</span>)</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <h2>Welcome to the Ultimate K-Pop Merch Shop 💜</h2>
    <p>Find albums, lightsticks, hoodies & more from your favorite groups!</p>
    <a href="#products" class="btn">Shop Now</a>
  </section>

  <main>
    <h2>Popular Items</h2>
    <div class="products" id="products">
      <div class="product">
        <img src="https://cdn.salla.sa/VwrlW/Bh2aCCGO7ysDfsojULblLI02AjAbzcpd8qi4UpGA.jpg" alt="BTS Lightstick"/>
        <h3>BTS Lightstick</h3>
        <p>$35.00</p>
        <button onclick="addToCart()">Add to Cart</button>
      </div>

      <div class="product">
        <img src="https://cdn.salla.sa/epeYR/34U9apnteSalghb5zl4NAXhWymkIcBe1YKPdxnYm.jpg" alt="BLACKPINK Hoodie"/>
        <h3>BLACKPINK Hoodie</h3>
        <p>$50.00</p>
        <button onclick="addToCart()">Add to Cart</button>
      </div>

      <div class="product">
        <img src="https://cdn.salla.sa/WqQEn/6991955b-bf8d-4e1b-89f4-2a9fef5e529f-1000x1000-zEUw9GfKY5Kkfv4lfBrIFpQmwRkAPQLNyxC54Tbn.png" alt="Stray Kids Album"/>
        <h3>Stray Kids Album</h3>
        <p>$25.00</p>
        <button onclick="addToCart()">Add to Cart</button>
      </div>
    </div>
  </main>

  <section class="contact" id="contact">
    <h2>Contact Us</h2>
    <p>Have questions about your order, merch, or just want to say hi? 💜</p>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message" rows="5" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2025 K-Pop Merch Store</p>
  </footer>

  <script>
    let cartCount = 0;

    function addToCart() {
      cartCount++;
      document.getElementById('cart-count').innerText = cartCount;
      alert("Item added to cart!");
    }
  </script>
</body>
</html> 




