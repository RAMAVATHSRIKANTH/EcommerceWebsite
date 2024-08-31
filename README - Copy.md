
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple eCommerce Store</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #333;
            color: white;
            padding: 10px;
            text-align: center;
        }
        nav ul {
            list-style-type: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin: 0 10px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
        }
        .container {
            padding: 20px;
        }
        .product {
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-bottom: 20px;
            padding: 15px;
            text-align: center;
        }
        .product img {
            max-width: 100px;
            height: auto;
        }
        .product button {
            background-color: #007bff;
            border: none;
            color: white;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
        }
        .product button:hover {
            background-color: #0056b3;
        }
        .cart {
            position: fixed;
            top: 10px;
            right: 10px;
            background-color: #f8f9fa;
            border: 1px solid #ddd;
            padding: 10px;
            border-radius: 5px;
        }
        .cart h2 {
            margin: 0;
        }
        .cart ul {
            list-style-type: none;
            padding: 0;
        }
        .cart ul li {
            margin: 5px 0;
        }
        .cart .total {
            font-weight: bold;
        }
    </style>
</head>
<body>

<header>
    <h1>Simple eCommerce Store</h1>
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#" id="view-cart">Cart (<span id="cart-count">0</span>)</a></li>
        </ul>
    </nav>
</header>

<div class="container">
    <div class="product">
        <img src="https://via.placeholder.com/100" alt="Product 1">
        <h3>Product 1</h3>
        <p>$10.00</p>
        <button onclick="addToCart('Product 1', 10.00)">Add to Cart</button>
    </div>
    <div class="product">
        <img src="https://via.placeholder.com/100" alt="Product 2">
        <h3>Product 2</h3>
        <p>$20.00</p>
        <button onclick="addToCart('Product 2', 20.00)">Add to Cart</button>
    </div>
    <div class="product">
        <img src="https://via.placeholder.com/100" alt="Product 3">
        <h3>Product 3</h3>
        <p>$30.00</p>
        <button onclick="addToCart('Product 3', 30.00)">Add to Cart</button>
    </div>
</div>

<div class="cart" id="cart">
    <h2>Shopping Cart</h2>
    <ul id="cart-items">
        <!-- Cart items will be added here -->
    </ul>
    <p class="total">Total: $<span id="cart-total">0.00</span></p>
</div>

<script>
    const cartItems = [];
    const cartCountElement = document.getElementById('cart-count');
    const cartItemsElement = document.getElementById('cart-items');
    const cartTotalElement = document.getElementById('cart-total');

    function addToCart(name, price) {
        cartItems.push({ name, price });
        updateCart();
    }

    function updateCart() {
        let total = 0;
        cartItemsElement.innerHTML = '';
        cartItems.forEach(item => {
            const li = document.createElement('li');
            li.textContent = `${item.name} - $${item.price.toFixed(2)}`;
            cartItemsElement.appendChild(li);
            total += item.price;
        });
        cartTotalElement.textContent = total.toFixed(2);
        cartCountElement.textContent = cartItems.length;
    }
</script>

</body>
</html>
