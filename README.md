<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StyleHub | Premium Fashion Boutique</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        :root {
            --primary: #2c3e50;
            --secondary: #ff6b6b;
            --accent: #f39c12;
            --light: #f8f9fa;
            --dark: #2c3e50;
            --text: #333;
            --gray: #95a5a6;
            --success: #27ae60;
            --express: #1e88e5;
            --anniversary: #e91e63;
        }

        body {
            background-color: #f5f7fa;
            color: var(--text);
            line-height: 1.6;
        }

        /* Header Styles */
        header {
            background: linear-gradient(to right, var(--primary), #1a2530);
            color: white;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .logo {
            font-size: 28px;
            font-weight: 800;
            display: flex;
            align-items: center;
        }

        .logo span {
            color: var(--secondary);
        }

        .logo i {
            margin-right: 10px;
            color: var(--accent);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav li {
            margin: 0 15px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 8px 0;
            position: relative;
            transition: all 0.3s ease;
        }

        nav a:hover {
            color: var(--accent);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }

        nav a:hover::after {
            width: 100%;
        }

        .header-icons {
            display: flex;
            gap: 20px;
        }

        .header-icons a {
            color: white;
            font-size: 20px;
            position: relative;
            transition: transform 0.3s ease;
        }

        .header-icons a:hover {
            color: var(--accent);
            transform: translateY(-3px);
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -10px;
            background-color: var(--secondary);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            font-size: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), url('https://images.unsplash.com/photo-1483985988355-763728e1935b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            height: 400px;
            display: flex;
            align-items: center;
            color: white;
            text-align: center;
            margin-bottom: 50px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
            text-shadow: 0 1px 3px rgba(0,0,0,0.5);
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: 2px solid var(--secondary);
            font-size: 14px;
        }

        .btn:hover {
            background-color: transparent;
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
            margin-left: 15px;
        }

        .btn-outline:hover {
            background-color: white;
            color: var(--secondary);
        }

        /* Filter Section */
        .filter-section {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            max-width: 1200px;
            margin: 0 auto 30px;
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .filter-title {
            display: flex;
            align-items: center;
            font-weight: 600;
            color: var(--primary);
        }

        .filter-title i {
            margin-right: 10px;
            color: var(--accent);
        }

        .filter-options {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .filter-btn {
            background: #f0f2f5;
            border: none;
            padding: 8px 20px;
            border-radius: 30px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .filter-btn:hover, .filter-btn.active {
            background: var(--secondary);
            color: white;
        }

        /* Products Section */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }

        .section-title h2 {
            font-size: 32px;
            color: var(--primary);
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--secondary);
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .product-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 20px rgba(0,0,0,0.15);
        }

        .product-badges {
            position: absolute;
            top: 15px;
            left: 15px;
            display: flex;
            flex-direction: column;
            gap: 8px;
            z-index: 2;
        }

        .product-badge {
            padding: 5px 12px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: 600;
            color: white;
        }

        .badge-anniversary {
            background-color: var(--anniversary);
        }

        .badge-official {
            background-color: var(--primary);
        }

        .product-img {
            height: 200px;
            overflow: hidden;
            position: relative;
        }

        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .product-card:hover .product-img img {
            transform: scale(1.05);
        }

        .product-info {
            padding: 20px;
        }

        .product-title {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--primary);
            line-height: 1.4;
        }

        .product-category {
            color: var(--gray);
            font-size: 13px;
            margin-bottom: 10px;
        }

        .price-container {
            margin-bottom: 12px;
        }

        .current-price {
            font-weight: 700;
            font-size: 18px;
            color: var(--secondary);
            margin-right: 8px;
        }

        .original-price {
            text-decoration: line-through;
            color: var(--gray);
            font-size: 14px;
        }

        .price-range {
            font-weight: 600;
            color: var(--primary);
            font-size: 15px;
        }

        .rating-container {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .stars {
            color: #f8d71c;
            margin-right: 8px;
        }

        .stars i {
            font-size: 14px;
        }

        .rating-count {
            font-size: 13px;
            color: var(--gray);
        }

        .express-badge {
            display: inline-flex;
            align-items: center;
            background-color: #e3f2fd;
            color: var(--express);
            padding: 4px 10px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: 600;
            margin-bottom: 15px;
        }

        .express-badge i {
            margin-right: 5px;
        }

        .add-to-cart-btn {
            display: block;
            width: 100%;
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 10px;
            border-radius: 5px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .add-to-cart-btn:hover {
            background-color: var(--secondary);
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 60px 0 30px;
            margin-top: 50px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .footer-col h3 {
            font-size: 20px;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-col h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background-color: var(--secondary);
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 15px;
        }

        .footer-col ul li a {
            color: #ddd;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .footer-col ul li a:hover {
            color: var(--accent);
            padding-left: 5px;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            margin-top: 40px;
            border-top: 1px solid rgba(255,255,255,0.1);
            max-width: 1200px;
            margin: 40px auto 0;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
            justify-content: center;
        }

        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }

        .social-icons a:hover {
            background-color: var(--secondary);
            transform: translateY(-5px);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 15px;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav li {
                margin: 5px 10px;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .btn {
                display: block;
                margin: 10px auto;
                width: 80%;
            }
            
            .btn-outline {
                margin-left: 0;
            }
            
            .filter-section {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <div class="logo">
                <i class="fas fa-crown"></i>Style<span>Hub</span>
            </div>
            
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Women</a></li>
                    <li><a href="#">Men</a></li>
                    <li><a href="#">Shoes</a></li>
                    <li><a href="#">Jewelry</a></li>
                    <li><a href="#">Wedding</a></li>
                    <li><a href="#">Sale</a></li>
                </ul>
            </nav>
            
            <div class="header-icons">
                <a href="#"><i class="fas fa-search"></i></a>
                <a href="#"><i class="fas fa-user"></i></a>
                <a href="#">
                    <i class="fas fa-shopping-cart"></i>
                    <span class="cart-count">3</span>
                </a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Discover Your Perfect Style</h1>
            <p>Shop the latest trends in fashion for every occasion</p>
            <a href="#" class="btn">Shop Collection</a>
            <a href="#" class="btn btn-outline">New Arrivals</a>
        </div>
    </section>

    <!-- Filter Section -->
    <div class="filter-section">
        <div class="filter-title">
            <i class="fas fa-filter"></i> Filter by:
        </div>
        <div class="filter-options">
            <button class="filter-btn active">All Products</button>
            <button class="filter-btn">Women</button>
            <button class="filter-btn">Men</button>
            <button class="filter-btn">Shoes</button>
            <button class="filter-btn">Jewelry</button>
            <button class="filter-btn">On Sale</button>
        </div>
    </div>

    <!-- Products Section -->
    <div class="container">
        <div class="section-title">
            <h2>Featured Products</h2>
        </div>
        
        <div class="products-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <div class="product-badges">
                    <span class="product-badge badge-anniversary">Anniversary deal</span>
                    <span class="product-badge badge-official">Official Store</span>
                </div>
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1606107557195-0e29a4b5b4aa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=764&q=80" alt="Football Shoes">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Kipsta Mens Football Shoes Agility 100 Firm Ground</h3>
                    <div class="price-container">
                        <span class="price-range">KSh 2,950 - KSh 3,250</span>
                    </div>
                    <button class="add-to-cart-btn">
                        <i class="fas fa-shopping-cart"></i> Add to cart
                    </button>
                </div>
            </div>
            
            <!-- Product 2 -->
            <div class="product-card">
                <div class="product-badges">
                    <span class="product-badge badge-anniversary">Anniversary deal</span>
                    <span class="product-badge badge-official">Official Store</span>
                </div>
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1549298916-b41d501d3772?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1412&q=80" alt="Hiking Shoes">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Quechua Men's Mountain Hiking Shoes - Mn100 - Black</h3>
                    <div class="price-container">
                        <span class="price-range">KSh 6,950 - KSh 8,950</span>
                    </div>
                    <button class="add-to-cart-btn">
                        <i class="fas fa-shopping-cart"></i> Add to cart
                    </button>
                </div>
            </div>
            
            <!-- Product 3 -->
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1560343090-f0409e92791a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=764&q=80" alt="Soccer Shoes">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Men Cleats Soccer Shoes Team Sport Football Boots</h3>
                    <div class="price-container">
                        <span class="current-price">KSh 5,126</span>
                        <span class="original-price">KSh 7,746</span>
                    </div>
                    <div class="rating-container">
                        <div class="stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                        </div>
                        <div class="rating-count">(24 reviews)</div>
                    </div>
                    <div class="express-badge">
                        <i class="fas fa-bolt"></i> JUMIA EXPRESS
                    </div>
                    <button class="add-to-cart-btn">
                        <i class="fas fa-shopping-cart"></i> Add to cart
                    </button>
                </div>
            </div>
            
            <!-- Product 4 -->
            <div class="product-card">
                <div class="product-badges">
                    <span class="product-badge badge-anniversary">Anniversary deal</span>
                    <span class="product-badge badge-official">Official Store</span>
                </div>
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1600185365926-3a2ce3cdb9eb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1025&q=80" alt="Football Boots">
                </div>
                <div class="product-info">
                    <h3 class="product-title">KIPSTA by decathlon Hard Ground Football Boots</h3>
                    <div class="price-container">
                        <span class="price-range">KSh 2,950 - KSh 3,250</span>
                    </div>
                    <button class="add-to-cart-btn">
                        <i class="fas fa-shopping-cart"></i> Add to cart
                    </button>
                </div>
            </div>
            
            <!-- Product 5 -->
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1543503103-f94a0036ed9d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Running Shoes">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Men's Basketball Shoes PU Sports Running Shoes</h3>
                    <div class="price-container">
                        <span class="current-price">KSh 1,599</span>
                        <span class="original-price">KSh 2,743</span>
                    </div>
                    <div class="rating-container">
                        <div class="stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                        <div class="rating-count">(18 reviews)</div>
                    </div>
                    <div class="express-badge">
                        <i class="fas fa-bolt"></i> JUMIA EXPRESS
                    </div>
                    <button class="add-to-cart-btn">
                        <i class="fas fa-shopping-cart"></i> Add to cart
                    </button>
                </div>
            </div>
            
            <!-- Product 6 -->
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1608667508764-33cf0726b13a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1480&q=80" alt="Basketball Shoes">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Men's Basketball Shoes Breathable High Top Sneakers</h3>
                    <div class="price-container">
                        <span class="current-price">KSh 1,599</span>
                        <span class="original-price">KSh 1,999</span>
                    </div>
                    <div class="rating-container">
                        <div class="stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="far fa-star"></i>
                        </div>
                        <div class="rating-count">(22 reviews)</div>
                    </div>
                    <div class="express-badge">
                        <i class="fas fa-bolt"></i> JUMIA EXPRESS
                    </div>
                    <button class="add-to-cart-btn">
                        <i class="fas fa-shopping-cart"></i> Add to cart
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-grid">
            <div class="footer-col">
                <h3>StyleHub</h3>
                <p>Your premier destination for fashion, offering the latest trends in clothing, shoes, jewelry, and accessories.</p>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-pinterest-p"></i></a>
                </div>
            </div>
            
            <div class="footer-col">
                <h3>Shop</h3>
                <ul>
                    <li><a href="#">Women's Collection</a></li>
                    <li><a href="#">Men's Collection</a></li>
                    <li><a href="#">Shoes & Footwear</a></li>
                    <li><a href="#">Jewelry & Accessories</a></li>
                    <li><a href="#">Wedding Collection</a></li>
                    <li><a href="#">Sale</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h3>Customer Service</hh3>
                <ul>
                    <li><a href="#">Contact Us</a></li>
                    <li><a href="#">Shipping Policy</a></li>
                    <li><a href="#">Returns & Exchanges</a></li>
                    <li><a href="#">FAQ</a></li>
                    <li><a href="#">Size Guide</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h3>Newsletter</h3>
                <p>Subscribe to get special offers, free giveaways, and new product alerts.</p>
                <form>
                    <input type="email" placeholder="Your email address" style="padding: 10px; width: 100%; margin-bottom: 10px; border-radius: 5px; border: none;">
                    <button type="submit" class="btn" style="background-color: var(--secondary); width: 100%;">Subscribe</button>
                </form>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2023 StyleHub. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Simple JavaScript for interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            // Add to cart functionality
            const addToCartButtons = document.querySelectorAll('.add-to-cart-btn');
            const cartCount = document.querySelector('.cart-count');
            let count = 3;
            
            addToCartButtons.forEach(button => {
                button.addEventListener('click', function() {
                    count++;
                    cartCount.textContent = count;
                    
                    // Animation effect
                    const originalText = button.innerHTML;
                    button.innerHTML = '<i class="fas fa-check"></i> Added to cart';
                    button.style.backgroundColor = '#27ae60';
                    
                    setTimeout(() => {
                        button.innerHTML = originalText;
                        button.style.backgroundColor = '';
                    }, 2000);
                });
            });
            
            // Filter buttons
            const filterButtons = document.querySelectorAll('.filter-btn');
            
            filterButtons.forEach(button => {
                button.addEventListener('click', function() {
                    // Remove active class from all buttons
                    filterButtons.forEach(btn => btn.classList.remove('active'));
                    
                    // Add active class to clicked button
                    this.classList.add('active');
                });
            });
        });
    </script>
</body>
</html>
