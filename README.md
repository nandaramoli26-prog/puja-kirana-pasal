# puja-<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Puja Kirana Pasal - General Store | Gurbhakot 04, Sahare, Surkhet</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        header {
            background: linear-gradient(135deg, #ff6b6b, #feca57);
            color: white;
            padding: 1.5rem 0;
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);
            position: relative;
            z-index: 10;
        }
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }
        .logo {
            font-size: 2.2rem;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        .contact-info {
            text-align: right;
        }
        .contact-info p {
            margin: 0.2rem 0;
            font-size: 1.1rem;
            font-weight: 500;
        }
        nav {
            background: #2c3e50;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }
        nav li {
            margin: 0 1.5rem;
        }
        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 25px;
        }
        nav a:hover {
            color: #feca57;
            background: rgba(255,255,255,0.1);
        }
        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="1" fill="white" opacity="0.1"/><circle cx="75" cy="75" r="1.5" fill="white" opacity="0.05"/><circle cx="50" cy="10" r="0.8" fill="white" opacity="0.08"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
            animation: float 20s ease-in-out infinite;
        }
        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: 0 2rem;
        }
        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1.5rem;
            animation: fadeInUp 1s ease-out;
        }
        .hero p {
            font-size: 1.8rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease-out 0.3s both;
        }
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        .section {
            padding: 5rem 0;
        }
        .section h2 {
            text-align: center;
            font-size: 2.8rem;
            margin-bottom: 3.5rem;
            color: #2c3e50;
            position: relative;
        }
        .section h2::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: linear-gradient(135deg, #ff6b6b, #feca57);
            margin: 1rem auto 0;
            border-radius: 2px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            margin-top: 2rem;
        }
        .card {
            background: white;
            padding: 2.5rem 2rem;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            text-align: center;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            border: 1px solid rgba(255,255,255,0.2);
        }
        .card:hover {
            transform: translateY(-15px) scale(1.02);
            box-shadow: 0 25px 50px rgba(0,0,0,0.2);
        }
        .card-icon {
            width: 110px;
            height: 110px;
            margin: 0 auto 1.5rem;
            border-radius: 50%;
            background: linear-gradient(135deg, #ff6b6b, #feca57);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            box-shadow: 0 10px 25px rgba(255,107,107,0.4);
        }
        .card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #2c3e50;
        }
        .location-section {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
        }
        .location-section .section h2 {
            color: white;
        }
        .location-map {
            height: 450px;
            background: linear-gradient(135deg, rgba(255,255,255,0.2), rgba(255,255,255,0.1));
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            font-weight: bold;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
            margin-top: 2rem;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }
        .contact-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
            text-align: center;
        }
        .contact-item {
            background: rgba(255,255,255,0.15);
            padding: 2.5rem;
            border-radius: 20px;
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255,255,255,0.2);
            transition: all 0.3s ease;
        }
        .contact-item:hover {
            transform: translateY(-5px);
            background: rgba(255,255,255,0.25);
        }
        .contact-icon {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            display: block;
        }
        footer {
            background: linear-gradient(135deg, #2c3e50, #1a252f);
            color: white;
            text-align: center;
            padding: 3rem 0;
            box-shadow: 0 -5px 20px rgba(0,0,0,0.2);
        }
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.8rem;
            }
            .hero p {
                font-size: 1.4rem;
            }
            .header-content {
                flex-direction: column;
                text-align: center;
                gap: 1rem;
            }
            nav ul {
                flex-direction: column;
                gap: 0.5rem;
            }
            nav li {
                margin: 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">🛒 Puja Kirana Pasal</div>
                <div class="contact-info">
                    <p>📞 9858041949</p>
                    <p>✉️ nandaramoli26@gmail.com</p>
                </div>
            </div>
        </div>
    </header>

    <nav>
        <div class="container">
            <ul>
                <li><a href="#home">🏠 Home</a></li>
                <li><a href="#products">🛍️ Products</a></li>
                <li><a href="#beer">🍺 Beer & Cold Drinks</a></li>
                <li><a href="#chauchau">🍜 Chauchau & Biscuit</a></li>
                <li><a href="#location">📍 Location</a></li>
                <li><a href="#contact">📞 Contact</a></li>
            </ul>
        </div>
    </nav>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Puja Kirana Pasal</h1>
            <p>All Grocery Items, Jasma Beer, Cold Drinks, Chauchau, Biscuit & More</p>
        </div>
    </section>

    <section id="products" class="section">
        <div class="container">
            <h2>🔥 Popular Products</h2>
            <div class="grid">
                <div class="card">
                    <div class="card-icon">🍺</div>
                    <h3>Jasma Beer</h3>
                    <p>Chilled Jasma Beer always available!</p>
                </div>
                <div class="card">
                    <div class="card-icon">🥤</div>
                    <h3>Cold Drinks</h3>
                    <p>Coca Cola, Sprite, Fanta, Dew all cold drinks</p>
                </div>
                <div class="card">
                    <div class="card-icon">🍜</div>
                    <h3>Chauchau</h3>
                    <p>Wai Wai, Chao Chao, Maggi instant noodles</p>
                </div>
                <div class="card">
                    <div class="card-icon">🍪</div>
                    <h3>Biscuits</h3>
                    <p>Parle G, Monaco, Good Day, Marie all types</p>
                </div>
                <div class="card">
                    <div class="card-icon">🥛</div>
                    <h3>Dairy Products</h3>
                    <p>Milk, Yogurt, Paneer, Ghee</p>
                </div>
                <div class="card">
                    <div class="card-icon">🧂</div>
                    <h3>Masala & Spices</h3>
                    <p>Turmeric, Cumin, Coriander all masalas</p>
                </div>
            </div>
        </div>
    </section>

    <section id="beer" class="section">
        <div class="container">
            <h2>🍺 Beer & Cold Drinks</h2>
            <div class="grid">
                <div class="card">
                    <div class="card-icon">🍺</div>
                    <h3>Jasma Beer</h3>
                    <p>Always chilled and fresh!</p>
                </div>
                <div class="card">
                    <div class="card-icon">🥤</div>
                    <h3>Coca Cola</h3>
                    <p>1.5L, 2L, Can available</p>
                </div>
                <div class="card">
                    <div class="card-icon">🍹</div>
                    <h3>Sprite & Fanta</h3>
                    <p>Lemon lime and orange flavour</p>
                </div>
            </div>
        </div>
    </section>

    <section id="chauchau" class="section">
        <div class="container">
            <h2>🍜 Chauchau & Biscuit</h2>
            <div class="grid">
                <div class="card">
                    <div class="card-icon">🍜</div>
                    <h3>Wai Wai</h3>
                    <p>Chicken, Veg, Special flavours</p>
                </div>
                <div class="card">
                    <div class="card-icon">🍜</div>
                    <h3>Chao Chao</h3>
                    <p>Extra spicy and regular</p>
                </div>
                <div class="card">
                    <div class="card-icon">🍪</div>
                    <h3>Parle G</h3>
                    <p>Perfect biscuit for tea time</p>
                </div>
                <div class="card">
                    <div class="card-icon">🍪</div>
                    <h3>Good Day</h3>
                    <p>Butter, Chocolate flavours</p>
                </div>
            </div>
        </div>
    </section>

    <section id="location" class="section location-section">
        <div class="container">
            <h2>📍 Location</h2>
            <div class="location-map">
                Gurbhakot 04, Sahare<br>
                Surkhet, Nepal
            </div>
            <p style="text-align: center; margin-top: 2.5rem; font-size: 1.3rem; backdrop-filter: blur(10px); background: rgba(255,255,255,0.1); padding: 1.5rem; border-radius: 15px; border: 1px solid rgba(255,255,255,0.2);">
                Our store is located at Gurbhakot 04, Sahare, Surkhet. 
                Easily accessible location.
            </p>
        </div>
    </section>

    <section id="contact" class="section contact-section">
        <div class="container">
            <h2 style="color: white;">📞 Contact Us</h2>
            <div class="contact-grid">
                <div class="contact-item">
                    <span class="contact-icon">📱</span>
                    <h3>Phone</h3>
                    <p><strong>9858041949</strong></p>
                </div>
                <div class="contact-item">
                    <span class="contact-icon">✉️</span>
                    <h3>Email</h3>
                    <p><strong>nandaramoli26@gmail.com</strong></p>
                </div>
                <div class="contact-item">
                    <span class="contact-icon">👨‍💼</span>
                    <h3>Producer</h3>
                    <p><strong>Nandaramoli</strong></p>
                </div>
                <div class="contact-item">
                    <span class="contact-icon">🏪</span>
                    <h3>Store</h3>
                    <p><strong>Puja Kirana Pasal</strong></p>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2024 Puja Kirana Pasal. Produced by Nandaramoli. Gurbhakot 04, Sahare, Surkhet.</p>
            <p>All grocery items at one place | Jasma Beer Cold | Chauchau | Biscuit</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Navbar active on scroll
        window.addEventListener('scroll', () => {
            let current = '';
            document.querySelectorAll('section[id]').forEach(section => {
                const sectionTop = section.offsetTop;
                if (scrollY >= sectionTop - 300) {
                    current = section.getAttribute('id');
                }
            });
            
            document.querySelectorAll('nav a').forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>kirana-pasal
