<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Anilov' Essentials</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background: #f5f5f5; }
    header { background: #222; color: #fff; padding: 15px; text-align: center; }
    nav { background: #444; padding: 10px; text-align: center; }
    nav a { color: #fff; margin: 0 10px; text-decoration: none; font-weight: bold; }
    nav a:hover { text-decoration: underline; }
    section { display: none; padding: 20px; }
    .active { display: block; }
    .container { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 20px; }
    .product { background: #fff; padding: 15px; border-radius: 10px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); transition: transform 0.2s; }
    .product:hover { transform: scale(1.03); }
    .product img { width: 100%; border-radius: 10px; height: 200px; object-fit: cover; }
    .price { color: green; font-weight: bold; }
    button { background: #222; color: #fff; border: none; padding: 10px; border-radius: 5px; cursor: pointer; width: 100%; }
    button:hover { background: #555; }
    footer { text-align: center; padding: 10px; background: #222; color: #fff; margin-top: 20px; }
  </style>
</head>
<body>

<header>
  <h1>Anilov' Essentials</h1>
  <p>Your daily needs in one place</p>
</header>

<nav>
  <a href="#" onclick="showSection('home')">Home</a>
  <a href="#" onclick="showSection('about')">About</a>
  <a href="#" onclick="showSection('products')">Products</a>
  <a href="#" onclick="showSection('contact')">Contact</a>
</nav>

<section id="home" class="active">
  <h2>Welcome</h2>
  <p>Welcome to Anilov' Essentials! We provide affordable and quality daily products for everyone.</p>
</section>

<section id="about">
  <h2>About Us</h2>
  <p>This website is created for educational purposes. Anilov' Essentials aims to deliver essential goods conveniently and efficiently.</p>
</section>

<section id="products">
  <h2>Our Products</h2>
  <div class="container">

    <div class="product">
      <img src="https://images.unsplash.com/photo-1600180758890-6b94519a8ba6" alt="Face Mask">
      <h3>Face Mask</h3>
      <p class="price">₱50</p>
      <button onclick="addToCart('Face Mask')">Add to Cart</button>
    </div>

    <div class="product">
      <img src="https://images.unsplash.com/photo-1583947581924-860bda6a26df" alt="Hand Sanitizer">
      <h3>Hand Sanitizer</h3>
      <p class="price">₱120</p>
      <button onclick="addToCart('Hand Sanitizer')">Add to Cart</button>
    </div>

    <div class="product">
      <img src="https://images.unsplash.com/photo-1620912189868-3a2b0d6d4e3a" alt="Toothpaste">
      <h3>Toothpaste</h3>
      <p class="price">₱80</p>
      <button onclick="addToCart('Toothpaste')">Add to Cart</button>
    </div>

    <div class="product">
      <img src="https://images.unsplash.com/photo-1596462502278-27bfdc403348" alt="Shampoo">
      <h3>Shampoo</h3>
      <p class="price">₱150</p>
      <button onclick="addToCart('Shampoo')">Add to Cart</button>
    </div>

  </div>
</section>

<section id="contact">
  <h2>Contact Us</h2>
  <p>Email: anilovrivera05@gmail.com</p>
  <p>Phone: 09244329315</p>
</section>

<footer>
  <p>© 2026 Anilov' Essentials</p>
</footer>

<script>
  function showSection(id) {
    document.querySelectorAll('section').forEach(sec => sec.classList.remove('active'));
    document.getElementById(id).classList.add('active');
  }

  function addToCart(product) {
    alert(product + " added to cart!");
  }
</script>

</body>
</html>
