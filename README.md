<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple E-commerce Website</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
        header, footer { background: #333; color: white; padding: 10px; text-align: center; }
        nav a { color: white; margin: 0 15px; text-decoration: none; }
        .container { width: 80%; margin: auto; }
        .products, .cart, .product-detail { margin: 20px 0; }
        .product, .cart-item { border: 1px solid #ddd; padding: 10px; margin: 10px 0; }
        .product img, .cart-item img { max-width: 100px; }
        .responsive { max-width: 100%; height: auto; }
        .form-group { margin: 15px 0; }
        .form-group label { display: block; margin-bottom: 5px; }
        .form-group input, .form-group textarea { width: 100%; padding: 10px; border: 1px solid #ddd; }
        .btn { padding: 10px 15px; background: #28a745; color: white; border: none; cursor: pointer; }
        .btn:hover { background: #218838; }
    </style>
</head>
<body>

<header>
    <nav>
        <a href="index.html">Home</a>
        <a href="products.html">Products</a>
        <a href="cart.html">Cart</a>
        <a href="login.html">Login</a>
        <a href="contact.html">Contact</a>
    </nav>
</header>

<div class="container">

    <!-- Home Page -->
    <section id="home">
        <h1>Welcome to Our Store</h1>
        <p>Shop the best products at unbeatable prices!</p>
    </section>

    <!-- Product Listing Page -->
    <section id="products">
        <h2>Product Listing</h2>
        <div class="product">
            <img src="/image/camera3.png" alt="Product 1" class="responsive">
            <h3>Product 1</h3>
            <p>$150</p>
            <button class="btn">Add to Cart</button>
        </div>
        <div class="product">
            <img src="/image/tv.jpeg" alt="Product 2" class="responsive">
            <h3>Product 2</h3>
            <p>$100</p>
            <button class="btn">Add to Cart</button>
        </div>
    </section>

    <!-- Product Details Page -->
    <section id="product-details">
        <div class="product-detail">
            <img src="/image/Laptop.jpg" alt="Product 1" class="responsive">
            <h2>Product 1</h2>
            <p>Description of Product 1.</p>
            <p>Price: $2000</p>
            <button class="btn">Add to Cart</button>
        </div>
    </section>

    <!-- Cart Page -->
    <section id="cart">
        <h2>Shopping Cart</h2>
        <div class="cart-item">
            <img src="/image/Smartphone.jpg" alt="Product 1" class="responsive">
            <h3>Product 1</h3>
            <p>Price: $200</p>
            <p>Quantity: 1</p>
            <button class="btn">Remove</button>
        </div>
        <button class="btn">Proceed to Checkout</button>
    </section>

    <!-- Checkout Page -->
    <section id="checkout">
        <h2>Checkout</h2>
        <form>
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="address">Address:</label>
                <textarea id="address" name="address" required></textarea>
            </div>
            <div class="form-group">
                <label for="payment">Payment Method:</label>
                <input type="text" id="payment" name="payment" required>
            </div>
            <button type="submit" class="btn">Place Order</button>
        </form>
    </section>

    <!-- Login Page -->
    <section id="login">
        <h2>Login</h2>
        <form>
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required>
            </div>
            <button type="submit" class="btn">Login</button>
        </form>
    </section>

    <!-- Registration Page -->
    <section id="register">
        <h2>Register</h2>
        <form>
            <div class="form-group">
                <label for="new-email">Email:</label>
                <input type="email" id="new-email" name="new-email" required>
            </div>
            <div class="form-group">
                <label for="new-password">Password:</label>
                <input type="password" id="new-password" name="new-password" required>
            </div>
            <button type="submit" class="btn">Register</button>
        </form>
    </section>

    <!-- Contact Page -->
    <section id="contact">
        <h2>Contact Us</h2>
        <form>
            <div class="form-group">
                <label for="contact-name">Name:</label>
                <input type="text" id="contact-name" name="contact-name" required>
            </div>
            <div class="form-group">
                <label for="contact-email">Email:</label>
                <input type="email" id="contact-email" name="contact-email" required>
            </div>
            <div class="form-group">
                <label for="message">Message:</label>
                <textarea id="message" name="message" required></textarea>
            </div>
            <button type="submit" class="btn">Send</button>
        </form>
    </section>

    <!-- Admin Dashboard Page -->
    <section id="admin-dashboard">
        <h2>Admin Dashboard</h2>
        <p>Manage your store's products, orders, and users from here.</p>
        <!-- Admin functionalities would be added here -->
    </section>

</div>

<footer>
    <p>&copy; 2024 Simple E-commerce Website</p>
</footer>

</body>
</html>

