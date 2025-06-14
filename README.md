# E-Commerce-Website
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trendy E-Commerce Store</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            line-height: 1.6;
            color: #333;
            background-color: #f9fafb;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, #1e3a8a, #3b82f6);
            color: white;
            padding: 2rem 1rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://via.placeholder.com/1920x200?text=Header+Pattern') no-repeat center/cover;
            opacity: 0.1;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            position: relative;
            animation: fadeIn 1s ease-in;
        }

        header p {
            font-size: 1.1rem;
            position: relative;
            animation: fadeIn 1.5s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        nav {
            background-color: #1e40af;
            padding: 1rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 2.5rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #93c5fd;
        }

        /* Main Content */
        .products {
            max-width: 1400px;
            margin: 3rem auto;
            padding: 0 1.5rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
        }

        .product-card {
            border: none;
            border-radius: 12px;
            overflow: hidden;
            background: white;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .product-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 8px 24px rgba(0,0,0,0.12);
        }

        .product-card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .product-card:hover img {
            transform: scale(1.05);
        }

        .product-info {
            padding: 1.5rem;
            text-align: center;
        }

        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #1e40af;
        }

        .product-info .description {
            color: #6b7280;
            font-size: 0.95rem;
            margin-bottom: 0.75rem;
            height: 60px;
            overflow: hidden;
        }

        .product-info .price {
            color: #16a34a;
            font-weight: bold;
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }

        .product-info .rating {
            color: #f59e0b;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .btn {
            background-color: #3b82f6;
            color: white;
            padding: 0.75rem 1.5rem;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            font-weight: 600;
            transition: background-color 0.3s;
        }

        .btn:hover {
            background-color: #2563eb;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, #1e3a8a, #1e40af);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }

        footer p {
            font-size: 1rem;
        }

        footer .social-links {
            margin-top: 1rem;
        }

        footer .social-links a {
            color: white;
            margin: 0 0.5rem;
            text-decoration: none;
            font-size: 1.2rem;
        }

        footer .social-links a:hover {
            color: #93c5fd;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .products {
                grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            }
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2rem;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
                gap: 1.5rem;
            }

            .products {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            header h1 {
                font-size: 1.5rem;
            }

            header p {
                font-size: 1rem;
            }

            .product-info h3 {
                font-size: 1.1rem;
            }

            .btn {
                padding: 0.6rem 1.2rem;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <h1>Trendy E-Commerce Store</h1>
        <p>Discover the latest trends in tech and lifestyle!</p>
    </header>

    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#products">Products</a></li>
            <li><a href="#cart">Cart</a></li>
            <li><a href="#contact">Contact</a></li>
            <li><a href="#about">About</a></li>
        </ul>
    </nav>

    <main class="products">
        <div class="product-card">
            <img src="https://via.placeholder.com/300x220?text=Wireless+Headphones" alt="Wireless Headphones">
            <div class="product-info">
                <h3>Wireless Headphones</h3>
                <p class="description">Premium sound quality with active noise cancellation and 20-hour battery life.</p>
                <p class="price">$79.99</p>
                <p class="rating">★★★★☆ (4.5)</p>
                <a href="#" class="btn">Add to Cart</a>
            </div>
        </div>

        <div class="product-card">
            <img src="https://via.placeholder.com/300x220?text=Smart+Watch" alt="Smart Watch">
            <div class="product-info">
                <h3>Smart Watch Pro</h3>
                <p class="description">Track fitness, heart rate, and notifications with a sleek design.</p>
                <p class="price">$129.99</p>
                <p class="rating">★★★★★ (4.8)</p>
                <a href="#" class="btn">Add to Cart</a>
            </div>
        </div>

        <div class="product-card">
            <img src="https://via.placeholder.com/300x220?text=Bluetooth+Speaker" alt="Bluetooth Speaker">
            <div class="product-info">
                <h3>Bluetooth Speaker</h3>
                <p class="description">Portable speaker with deep bass and waterproof design.</p>
                <p class="price">$49.99</p>
                <p class="rating">★★★★☆ (4.3)</p>
                <a href="#" class="btn">Add to Cart</a>
            </div>
        </div>

        <div class="product-card">
            <img src="https://via.placeholder.com/300x220?text=USB-C+Charger" alt="USB-C Charger">
            <div class="product-info">
                <h3>Fast USB-C Charger</h3>
                <p class="description">65W fast charging compatible with all modern devices.</p>
                <p class="price">$24.99</p>
                <p class="rating">★★★★☆ (4.4)</p>
                <a href="#" class="btn">Add to Cart</a>
            </div>
        </div>

        <div class="product-card">
            <img src="https://via.placeholder.com/300x220?text=Wireless+Mouse" alt="Wireless Mouse">
            <div class="product-info">
                <h3>Ergonomic Wireless Mouse</h3>
                <p class="description">Smooth, precise control with customizable buttons.</p>
                <p class="price">$34.99</p>
                <p class="rating">★★★★☆ (4.6)</p>
                <a href="#" class="btn">Add to Cart</a>
            </div>
        </div>

        <div class="product-card">
            <img src="https://via.placeholder.com/300x220?text=4K+Webcam" alt="4K Webcam">
            <div class="product-info">
                <h3>4K Ultra Webcam</h3>
                <p class="description">Crystal-clear video for streaming and video calls.</p>
                <p class="price">$89.99</p>
                <p class="rating">★★★★★ (4.7)</p>
                <a href="#" class="btn">Add to Cart</a>
            </div>
        </div>

        <div class="product-card">
            <img src="https://via.placeholder.com/300x220?text=Portable+SSD" alt="Portable SSD">
            <div class="product-info">
                <h3>1TB Portable SSD</h3>
                <p class="description">High-speed storage with durable, compact design.</p>
                <p class="price">$99.99</p>
                <p class="rating">★★★★★ (4.9)</p>
                <a href="#" class="btn">Add to Cart</a>
            </div>
        </div>

        <div class="product-card">
            <img src="https://via.placeholder.com/300x220?text=Wireless+Keyboard" alt="Wireless Keyboard">
            <div class="product-info">
                <h3>Wireless Keyboard</h3>
                <p class="description">Slim, quiet keys with long-lasting battery.</p>
                <p class="price">$59.99</p>
                <p class="rating">★★★★☆ (4.5)</p>
                <a href="#" class="btn">Add to Cart</a>
            </div>
        </div>
    </main>

    <footer>
        <p>© 2025 Trendy E-Commerce Store. All rights reserved.</p>
        <div class="social-links">
            <a href="#">Facebook</a> |
            <a href="#">Twitter</a> |
            <a href="#">Instagram</a>
        </div>
    </footer>
</body>
</html>
