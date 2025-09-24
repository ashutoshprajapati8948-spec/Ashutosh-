<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Jagat Garments - Fancy E-commerce Site</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap');
        body {
            margin: 0; padding: 0;
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #2c3e50;
        }
        header {
            background: #34495e;
            color: white;
            padding: 20px 0;
            text-align: center;
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: 3px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
        }
        nav {
            background: #2c3e50;
            display: flex;
            justify-content: center;
            gap: 40px;
            padding: 15px 0;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        nav a {
            color: #ecf0f1;
            text-decoration: none;
            font-size: 1.1rem;
            font-weight: 600;
            padding: 8px 18px;
            transition: background 0.3s ease, color 0.3s ease;
            border-radius: 25px;
        }
        nav a:hover {
            background: #e67e22;
            color: white;
            box-shadow: 0 0 10px #e67e22;
        }
        .hero {
            background: url('https://images.unsplash.com/photo-1521335629791-ce4aec67dd8a?auto=format&fit=cover&w=1600&q=80') center/cover no-repeat;
            height: 400px;
            position: relative;
            display: flex; align-items: center; justify-content: center;
            color: #fff;
            text-align: center;
        }
        .hero::before {
            content: '';
            position: absolute; top: 0; bottom: 0; left: 0; right: 0;
            background: rgba(44,62,80,0.6);
            z-index: 1;
            border-radius: 0 0 40% 40% / 70%;
        }
        .hero-content {
            position: relative; z-index: 2;
            max-width: 700px;
        }
        .hero-content h1 {
            font-size: 3rem;
            font-weight: 800;
            margin-bottom: 15px;
            letter-spacing: 4px;
            text-shadow: 0 0 10px rgba(0,0,0,0.6);
        }
        .hero-content p {
            font-size: 1.4rem;
            font-weight: 500;
            margin-bottom: 30px;
            text-shadow: 0 0 8px rgba(0,0,0,0.5);
        }
        .hero-content button {
            background: #e67e22;
            border: none;
            padding: 15px 60px;
            font-size: 1.2rem;
            font-weight: 700;
            color: white;
            cursor: pointer;
            border-radius: 30px;
            box-shadow: 0 5px 18px #e67e22;
            transition: 0.3s ease background;
        }
        .hero-content button:hover {
            background: #d35400;
            box-shadow: 0 8px 35px #d35400;
        }
        .products {
            max-width: 1200px;
            margin: 60px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: repeat(auto-fill,minmax(250px,1fr));
            gap: 30px;
        }
        .product-card {
            background: white;
            border-radius: 18px;
            overflow: hidden;
            box-shadow: 0 8px 25px rgba(198,161,83,0.12);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }
        .product-card:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 14px 40px rgba(198,161,83,0.3);
        }
        .product-img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            transition: transform 0.4s ease;
        }
        .product-card:hover .product-img {
            transform: scale(1.1);
        }
        .product-info {
            padding: 15px 18px;
        }
        .product-name {
            font-size: 1.25rem;
            font-weight: 700;
            color: #34495e;
            margin-bottom: 8px;
        }
        .product-desc {
            font-size: 1rem;
            color: #7f8c8d;
            margin-bottom: 15px;
            height: 46px;
            overflow: hidden;
        }
        .product-price {
            font-size: 1.3rem;
            font-weight: 700;
            color: #e67e22;
        }
        .btn-buy {
            background: #34495e;
            color: white;
            border: none;
            padding: 12px 28px;
            border-radius: 22px;
            font-weight: 700;
            cursor: pointer;
            margin-top: 12px;
            width: 100%;
            transition: background 0.3s ease;
        }
        .btn-buy:hover {
            background: #e67e22;
            box-shadow: 0 0 12px #e67e22;
        }
        footer {
            background: #34495e;
            color: white;
            text-align: center;
            padding: 22px 10px;
            margin-top: 60px;
            font-weight: 600;
            font-size: 1rem;
            letter-spacing: 2px;
        }
        @media(max-width: 600px) {
            .hero-content h1 {
                font-size: 2rem;
            }
            .products {
                grid-template-columns: 1fr;
                margin: 40px auto;
                padding: 0 15px;
            }
            nav {
                flex-wrap: wrap;
                gap: 15px;
            }
        }
    </style>
</head>
<body>

<header>Jagat Garments</header>

<nav>
    <a href="#products">Products</a>
    <a href="#about">About Us</a>
    <a href="#contact">Contact</a>
</nav>

<section class="hero">
    <div class="hero-content">
        <h1>Kapdon ki Duniya Mein Apka Swagat Hai!</h1>
        <p>Fancy aur stylish garments, behtareen daam par. Ek baar aayein, toh zaroor le jaayein!</p>
        <button onclick="document.location='#products'">Shopping Shuru Karo</button>
    </div>
</section>

<section id="products" class="products">
    <div class="product-card">
        <img src="https://images.unsplash.com/photo-1503342217505-b0a15ec3261c?auto=format&fit=cover&w=400&q=80" alt="Men's Shirt" class="product-img" />
        <div class="product-info">
            <div class="product-name">Mens Classic Shirt</div>
            <p class="product-desc">High quality cotton, perfect fit for har din ke liye.</p>
            <div class="product-price">₹799</div>
            <button class="btn-buy">Abhi Kharidein</button>
        </div>
    </div>
    <div class="product-card">
        <img src="https://images.unsplash.com/photo-1520975698518-9209bbb9d54a?auto=format&fit=cover&w=400&q=80" alt="Women Kurti" class="product-img" />
        <div class="product-info">
            <div class="product-name">Ladies Designer Kurti</div>
            <p class="product-desc">Stylish aur comfortable, har occasion ke liye.</p>
            <div class="product-price">₹599</div>
            <button class="btn-buy">Abhi Kharidein</button>
        </div>
    </div>
    <div class="product-card">
        <img src="https://images.unsplash.com/photo-1514996937319-344454492b37?auto=format&fit=cover&w=400&q=80" alt="Women Saree" class="product-img" />
        <div class="product-info">
            <div class="product-name">Elegant Saree</div>
            <p class="product-desc">Handcrafted silk, traditional yet modern design.</p>
            <div class="product-price">₹1,499</div>
            <button class="btn-buy">Abhi Kharidein</button>
        </div>
    </div>
    <div class="product-card">
        <img src="https://images.unsplash.com/photo-1512436991641-6745cdb1723f?auto=format&fit=cover&w=400&q=80" alt="Jeans" class="product-img" />
        <div class="product-info">
            <div class="product-name">Denim Jeans</div>
            <p class="product-desc">Comfortable fit, style ke saath durability.</p>
            <div class="product-price">₹899</div>
            <button class="btn-buy">Abhi Kharidein</button>
        </div>
    </div>
</section>

<section id="about" style="max-width: 900px; margin: 60px auto; padding: 20px;">
    <h2 style="text-align:center; color:#34495e; font-weight:700;">About Jagat Garments</h2>
    <p style="text-align:center; color:#34495e; font-size:1.1rem;">
        Jagat Garments bharosemand naam hai kapdon ki duniya mein.<br />
        Hum apne grahak ko quality aur stylish kapde behtareen daam par dete hain.<br />
        Ek baar aayen aur apna pasandida product lekar zaroor jayein!
    </p>
</section>

<section id="contact" style="background:#ecf0f1; padding: 40px 20px; max-width: 500px; margin: 50px auto; border-radius: 15px; box-shadow: 0 12px 32px rgba(0,0,0,0.05);">
    <h2 style="text-align:center; color:#34495e; font-weight:700; margin-bottom: 20px;">Contact Us</h2>
    <p style="text-align:center; font-size:1rem; color:#2c3e50;">Email: <strong>jagatgarments@email.com</strong></p>
    <p style="text-align:center; font-size:1rem; color:#2c3e50;">Phone: <strong>+91 98XXXXXXXX</strong></p>
    <p style="text-align:center; font-size:1rem; color:#2c3e50;">Instagram: <strong>@jagatgarments_official</strong></p>
</section>

<footer>
    &copy; 2025 Jagat Garments | Designed by Ashutosh Prajapati
</footer>

</body>
</html> cantrol+sift+m
