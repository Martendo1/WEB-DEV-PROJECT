# WEB-DEV-PROJECT

##SECTION 1

<----1ST PAGE , PRODUCT SALES/ITEMS---->

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FoodieMart</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:Arial, sans-serif;
    }

    body{
      background:#f4f4f4;
    }

    header{
      background:#ff6600;
      color:white;
      padding:20px 8%;
      display:flex;
      justify-content:space-between;
      align-items:center;
      position:sticky;
      top:0;
    }

    .logo{
      font-size:32px;
      font-weight:bold;
    }

    nav a{
      color:white;
      text-decoration:none;
      margin:0 12px;
      font-size:18px;
    }

    .cart-btn{
      background:white;
      color:#ff6600;
      border:none;
      padding:12px 20px;
      border-radius:10px;
      font-weight:bold;
      cursor:pointer;
    }

    .hero{
      height:90vh;
      background:linear-gradient(rgba(0,0,0,.6), rgba(0,0,0,.6)),
      url('https://images.unsplash.com/photo-1504674900247-0877df9cc836?q=80&w=1600&auto=format&fit=crop');
      background-size:cover;
      background-position:center;
      display:flex;
      justify-content:center;
      align-items:center;
      text-align:center;
      color:white;
      padding:20px;
    }

    .hero h1{
      font-size:65px;
      margin-bottom:20px;
    }

    .hero p{
      font-size:22px;
      margin-bottom:25px;
    }

    .hero button{
      background:#ff6600;
      color:white;
      border:none;
      padding:15px 35px;
      font-size:20px;
      border-radius:10px;
      cursor:pointer;
    }

    .products{
      padding:80px 8%;
    }

    .section-title{
      text-align:center;
      margin-bottom:50px;
    }

    .section-title h2{
      font-size:50px;
      margin-bottom:10px;
    }

    .product-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit, minmax(280px,1fr));
      gap:30px;
    }

    .card{
      background:white;
      border-radius:20px;
      overflow:hidden;
      box-shadow:0 5px 15px rgba(0,0,0,.1);
      transition:.3s;
    }

    .card:hover{
      transform:translateY(-10px);
    }

    .card img{
      width:100%;
      height:250px;
      object-fit:cover;
    }

    .info{
      padding:20px;
    }

    .info h3{
      font-size:28px;
      margin-bottom:10px;
    }

    .price{
      color:#ff6600;
      font-size:24px;
      font-weight:bold;
      margin-bottom:15px;
    }

    .info p{
      color:#666;
      margin-bottom:20px;
    }

    .add-cart{
      width:100%;
      background:#ff6600;
      color:white;
      border:none;
      padding:14px;
      border-radius:10px;
      font-size:18px;
      cursor:pointer;
    }

    footer{
      background:#111;
      color:white;
      text-align:center;
      padding:30px;
      margin-top:60px;
    }
  </style>
</head>
<body>

<header>
  <div class="logo">FoodieMart</div>

  <nav>
    <a href="#">Home</a>
    <a href="#products">Products</a>
  </nav>

  <button class="cart-btn" onclick="goToCart()">
    Cart (<span id="cart-count">0</span>)
  </button>
</header>

<section class="hero">
  <div>
    <h1>Delicious Food Delivered Fast</h1>
    <p>Fresh meals at affordable prices.</p>
    <button onclick="scrollToProducts()">Shop Now</button>
  </div>
</section>

<section class="products" id="products">

  <div class="section-title">
    <h2>Popular Foods</h2>
    <p>Choose your favorite meals</p>
  </div>

  <div class="product-grid">

    <div class="card">
      <img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?q=80&w=1200&auto=format&fit=crop">

      <div class="info">
        <h3>Burger</h3>
        <div class="price">₦7,500</div>
        <p>Juicy burger with cheese and fries.</p>
        <button class="add-cart" onclick="addToCart('Burger',7500)">
          Add To Cart
        </button>
      </div>
    </div>

    <div class="card">
      <img src="https://images.unsplash.com/photo-1513104890138-7c749659a591?q=80&w=1200&auto=format&fit=crop">

      <div class="info">
        <h3>Pizza</h3>
        <div class="price">₦13,400</div>
        <p>Hot pizza loaded with toppings.</p>
        <button class="add-cart" onclick="addToCart('Pizza',13400)">
          Add To Cart
        </button>
      </div>
    </div>

    <div class="card">
      <img src="https://images.unsplash.com/photo-1562967916-eb82221dfb92?q=80&w=1200&auto=format&fit=crop">

      <div class="info">
        <h3>Chicken</h3>
        <div class="price">₦6,600</div>
        <p>Crispy fried chicken combo.</p>
        <button class="add-cart" onclick="addToCart('Crispy Chicken',6600)">
          Add To Cart
        </button>
      </div>
    </div>

    <div class="card">
      <img src="https://images.unsplash.com/photo-1546069901-ba9599a7e63c?q=80&w=1200&auto=format&fit=crop">
      
      <div class="info">
        <h3>Salad</h3>
        <div class="price">₦5,000</div>
        <p>Healthy vegetable salad with fresh dressing.</p>
        <button class="add-cart" onclick="addToCart('Salad',5000)">
          Add To Cart
        </button>
      </div>
    </div>

    <div class="card">
      <img src="https://images.unsplash.com/photo-1600891964092-4316c288032e?q=80&w=1200&auto=format&fit=crop">
      <div class="info">
        <h3>Rice & Chicken</h3>
        <div class="price">₦9,500</div>
        <p>Delicious jollof rice with grilled chicken.</p>
        <button class="add-cart" onclick="addToCart('Rice & Chicken',9500)">
          Add To Cart
        </button>
      </div>
    </div>

    <div class="card">
      <img src="https://images.unsplash.com/photo-1626200419199-391ae4be7a41?q=80&w=1200&auto=format&fit=crop">
      <div class="info">
        <h3>Jollof Rice</h3>
        <div class="price">₦4,500</div>
        <p>Smoky Nigerian jollof rice with chicken.</p>
        <button class="add-cart" onclick="addToCart('Jollof Rice',4500)">
          Add To Cart
        </button>
      </div>
    </div>
    
    
    <div class="card">
      <img src="https://images.unsplash.com/photo-1604908554027-1c4d9f4c7c6b?q=80&w=1200&auto=format&fit=crop">
      <div class="info">
        <h3>Moi Moi</h3>
        <div class="price">₦2,500</div>
        <p>Soft steamed bean pudding with fish and egg.</p>
        <button class="add-cart" onclick="addToCart('Moi Moi',2500)">
          Add To Cart
        </button>
      </div>
    </div>
    
    
    <div class="card">
      <img src="https://images.unsplash.com/photo-1516685018646-549198525c1b?q=80&w=1200&auto=format&fit=crop">
      <div class="info">
        <h3>Pounded Yam & Egusi</h3>
        <div class="price">₦6,500</div>
        <p>Traditional pounded yam served with rich egusi soup.</p>
        <button class="add-cart" onclick="addToCart('Pounded Yam & Egusi',6500)">
          Add To Cart
        </button>
      </div>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1547592180-85f173990554?q=80&w=1200&auto=format&fit=crop">
      <div class="info">
        <h3>Suya</h3>
        <div class="price">₦3,500</div>
        <p>Spicy grilled beef suya with onions and pepper.</p>
        <button class="add-cart" onclick="addToCart('Suya',3500)">
          Add To Cart
        </button>
      </div>
    </div>
    
    
    <div class="card">
      <img src="https://images.unsplash.com/photo-1600335895229-6e75511892c8?q=80&w=1200&auto=format&fit=crop">
      <div class="info">
        <h3>Beans & Plantain</h3>
        <div class="price">₦3,000</div>
        <p>Delicious beans served with fried ripe plantain.</p>
        <button class="add-cart" onclick="addToCart('Beans & Plantain',3000)">
          Add To Cart
        </button>
      </div>
    </div>

</section>

<footer>
  © 2026 FoodieMart | Lagos, Nigeria
</footer>

<script>

localStorage.clear();

  let cart = JSON.parse(localStorage.getItem('cart')) || [];

  updateCartCount();

  function addToCart(name, price){

    cart.push({
      name:name,
      price:price
    });

    localStorage.setItem('cart', JSON.stringify(cart));

    updateCartCount();

    alert(name + ' added to cart');
  }

  function updateCartCount(){
    document.getElementById('cart-count').textContent = cart.length;
  }

  function goToCart(){
    window.location.href = 'jsProjectcart.html';

  }

  function scrollToProducts(){
    document.getElementById('products').scrollIntoView({
      behavior:'smooth'
    });
  }

</script>

</body>
</html>


##SECTION 2

<----2ND PROJECT CART PAGE PLUS CARD PAYMENT---->


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cart & Payment</title>

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:Arial, sans-serif;
    }

    body{
      background:#f4f4f4;
      padding:40px 8%;
    }

    h1{
      margin-bottom:30px;
      color:#ff6600;
    }

    .container{
      display:grid;
      grid-template-columns:2fr 1fr;
      gap:30px;
    }

    .cart-box,
    .payment-box{
      background:white;
      padding:30px;
      border-radius:20px;
      box-shadow:0 5px 15px rgba(0,0,0,.1);
    }

    .cart-item{
      display:flex;
      justify-content:space-between;
      padding:15px 0;
      border-bottom:1px solid #ddd;
      font-size:18px;
    }

    .total{
      margin-top:20px;
      font-size:26px;
      font-weight:bold;
      color:#ff6600;
    }

    .payment-box h2{
      margin-bottom:20px;
    }

    input{
      width:100%;
      padding:15px;
      margin-bottom:15px;
      border:1px solid #ccc;
      border-radius:10px;
      font-size:16px;
    }

    .pay-btn{
      width:100%;
      background:#ff6600;
      color:white;
      border:none;
      padding:15px;
      font-size:18px;
      border-radius:10px;
      cursor:pointer;
    }

    .pay-btn:hover{
      background:#e65c00;
    }

    @media(max-width:900px){
      .container{
        grid-template-columns:1fr;
      }
    }

  </style>
</head>
<body>

<h1>Your Cart</h1>

<div class="container">

  <div class="cart-box">

    <div id="cart-items"></div>

    <div class="total">
      Total: ₦<span id="total-price">0</span>
    </div>

  </div>

  <div class="payment-box">

    <h2>Card Payment</h2>

    <input type="text" id="card-name" placeholder="Card Holder Name">

    <input type="text" id="card-number" placeholder="Card Number">

    <input type="text" id="expiry" placeholder="Expiry Date MM/YY">

    <input type="text" id="cvv" placeholder="CVV">

    <button class="pay-btn" onclick="makePayment()">
      Pay Now
    </button>

  </div>

</div>

<script>

  let cart = JSON.parse(localStorage.getItem('cart')) || [];
  let cartItems = document.getElementById('cart-items');
  let totalPrice = document.getElementById('total-price');
  let total = 0;

  function makePayment(){

  const name = document.getElementById('card-name').value.trim();
  const number = document.getElementById('card-number').value.trim();
  const expiry = document.getElementById('expiry').value.trim();
  const cvv = document.getElementById('cvv').value.trim();

  // 1. Check empty cart
  if(cart.length === 0){
    alert('Your cart is empty');
    return;
  }

  // 2. Validate name
  if(name === ''){
    alert('Enter card holder name');
    return;
  }

  // 3. Validate card number (16 digits)

  if (!/^\d{16}$/.test(number)) {
    alert('Card number must be exactly 16 digits (numbers only)');
    return;
  }

  // 4. Validate expiry format MM/YY
  if(!expiry.includes('/') || expiry.length !== 5){
    alert('Expiry must be in MM/YY format');
    return;
  }

  if (!/^\d{2}\/\d{2}$/.test(expiry)) {
    alert('Expiry must be in MM/YY format');
    return;
}
  // 5. Validate CVV (3 digits)
  if (!/^\d{3}$/.test(cvv)) {
    alert('CVV must be exactly 3 digits (numbers only)');
    return;
  }

  // SUCCESS
  alert('Payment Successful! Your order has been placed.');

  localStorage.removeItem('cart');

  window.location.href = 'jsProject.html';
}

  
  function loadCart(){

  cartItems.innerHTML = ""; // 🔥 IMPORTANT FIX
  total = 0;

  cart.forEach(item => {

    total += item.price;

    cartItems.innerHTML += `
      <div class="cart-item">
        <span>${item.name}</span>
        <span>₦${item.price.toLocaleString()}</span>
      </div>
    `;
  });

  totalPrice.textContent = total.toLocaleString();
}

window.onload = function(){
  loadCart();
};

  

</script>

</body>
</html>
