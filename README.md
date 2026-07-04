<!DOCTYPE html>
<html lang="fr">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GHARAMI | Haute Parfumerie</title>
    <!-- Google Fonts for Luxury Typography -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        body { 
            background-color: #0b0b0b; 
            color: #ffffff; 
            font-family: 'Montserrat', sans-serif; 
            padding-bottom: 0;
            overflow-x: hidden;
        }
        
        /* Premium Announcement Bar */
        .top-bar { 
            background-color: #121212; 
            text-align: center; 
            padding: 10px 10px; 
            font-size: 11px; 
            letter-spacing: 2px; 
            text-transform: uppercase; 
            color: #d4af37; /* Gold */
            font-weight: 600; 
            border-bottom: 1px solid #1a1a1a; 
        }
        
        /* Ultra Luxury Navbar */
        header { 
            background-color: rgba(11, 11, 11, 0.95); 
            position: sticky; 
            top: 0; 
            z-index: 1000; 
            border-bottom: 1px solid #1c1c1c; 
            padding: 25px 50px; 
            display: flex; 
            justify-content: space-between; 
            align-items: center;
            backdrop-filter: blur(10px);
        }
        
        .nav-links { display: flex; gap: 30px; list-style: none; font-size: 12px; text-transform: uppercase; letter-spacing: 2px; }
        .nav-links a { text-decoration: none; color: #aaaaaa; transition: 0.3s; font-weight: 400; }
        .nav-links a:hover { color: #d4af37; }
        
        .logo h1 { 
            font-family: 'Cinzel', serif; 
            font-size: 28px; 
            color: #ffffff; 
            font-weight: 700; 
            letter-spacing: 6px; 
            text-align: center; 
            text-transform: uppercase; 
            background: linear-gradient(135deg, #ffffff 0%, #d4af37 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .header-icons { display: flex; gap: 20px; font-size: 18px; color: #aaaaaa; cursor: pointer; transition: 0.3s; }
        .header-icons span:hover { color: #d4af37; }

        /* Cinema Hero Banner */
        .hero { 
            position: relative; 
            height: 80vh; 
            background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1594035910387-fea47794261f?q=80&w=1200&auto=format&fit=crop'); 
            background-size: cover; 
            background-position: center; 
            display: flex; 
            align-items: center; 
            justify-content: center; 
            text-align: center; 
        }
        
        .hero-content h2 { 
            font-family: 'Cinzel', serif; 
            font-size: 55px; 
            font-weight: 400; 
            letter-spacing: 5px; 
            margin-bottom: 20px; 
            text-transform: uppercase;
            color: #ffffff;
        }
        
        .hero-content p { 
            font-size: 16px; 
            font-style: italic; 
            margin-bottom: 35px; 
            letter-spacing: 2px; 
            color: #cccccc;
        }
        
        .hero-btn { 
            display: inline-block; 
            padding: 14px 40px; 
            background-color: transparent; 
            color: #d4af37; 
            text-decoration: none; 
            text-transform: uppercase; 
            font-size: 12px; 
            letter-spacing: 3px; 
            font-weight: 600; 
            transition: 0.4s; 
            border: 1px solid #d4af37; 
        }
        
        .hero-btn:hover { 
            background-color: #d4af37; 
            color: #0b0b0b; 
            box-shadow: 0 0 15px rgba(212, 175, 55, 0.4);
        }

        /* Section Title Luxe */
        .section-title { text-align: center; margin: 80px 0 40px 0; }
        .section-title h3 { 
            font-family: 'Cinzel', serif;
            font-size: 28px; 
            text-transform: uppercase; 
            letter-spacing: 4px; 
            font-weight: 400; 
            position: relative; 
            display: inline-block; 
            padding-bottom: 15px;
            color: #ffffff;
        }
        .section-title h3::after { 
            content: ''; 
            width: 60px; 
            height: 1px; 
            background-color: #d4af37; 
            position: absolute; 
            bottom: 0; 
            left: 50%; 
            transform: translateX(-50%); 
        }

        /* Products Display */
        .container { max-width: 1200px; margin: 0 auto; padding: 0 25px 80px 25px; }
        .products-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 40px; }
        
        /* Elite Product Card */
        .product-card { 
            background: #111111; 
            text-align: center; 
            transition: 0.4s; 
            border: 1px solid #1a1a1a;
            border-radius: 4px;
            overflow: hidden;
        }
        .product-card:hover {
            border-color: #d4af37;
            box-shadow: 0 10px 30px rgba(0,0,0,0.7);
            transform: translateY(-5px);
        }
        
        .product-img-box { 
            width: 100%; 
            height: 400px; 
            background-size: cover; 
            background-position: center; 
            transition: transform 0.6s cubic-bezier(0.25, 1, 0.5, 1); 
        }
        .product-card:hover .product-img-box { transform: scale(1.05); }
        
        .product-info { padding: 25px 20px; }
        .product-category { 
            font-size: 10px; 
            text-transform: uppercase; 
            color: #d4af37; 
            letter-spacing: 2px; 
            margin-bottom: 10px; 
            font-weight: 600;
        }
        .product-title { 
            font-family: 'Cinzel', serif;
            font-size: 18px; 
            color: #ffffff; 
            font-weight: 600; 
            margin-bottom: 12px; 
            letter-spacing: 1px; 
        }
        .product-price { 
            font-size: 16px; 
            color: #ffffff; 
            font-weight: 600; 
            margin-bottom: 20px; 
            letter-spacing: 1px;
        }
        
        /* Pro Max Buy Button */
        .btn-buy { 
            display: block; 
            width: 100%; 
            text-align: center; 
            padding: 14px; 
            background-color: transparent; 
            color: #ffffff; 
            text-decoration: none; 
            font-size: 11px; 
            text-transform: uppercase; 
            letter-spacing: 2px; 
            font-weight: 600; 
            transition: 0.3s; 
            border: 1px solid #333333; 
        }
        .btn-buy:hover { 
            background-color: #ffffff; 
            color: #0b0b0b; 
            border-color: #ffffff;
        }

        /* Footer High-End */
        footer { 
            background-color: #070707; 
            text-align: center; 
            padding: 50px 20px; 
            font-size: 11px; 
            color: #666666; 
            border-top: 1px solid #111111; 
            letter-spacing: 2px; 
        }
        footer p { margin-bottom: 12px; }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            header { padding: 20px; }
            .hero-content h2 { font-size: 36px; }
            .nav-links { display: none; }
        }
    </style>
</head>
<body>

    <!-- Top Premium Bar -->
    <div class="top-bar">
        Livraison Prestige sur toute la Tunisie | Haute Parfumerie d'Ambiance
    </div>

    <!-- Luxury Header -->
    <header>
        <ul class="nav-links">
            <li><a href="#">Collections</a></li>
            <li><a href="#">L'Univers</a></li>
        </ul>
        <div class="logo">
            <h1>GHARAMI</h1>
        </div>
        <div class="header-icons">
            <span>🔍</span>
            <span>🛍️</span>
        </div>
    </header>

    <!-- Cinema Hero Banner -->
    <div class="hero">
        <div class="hero-content">
            <h2>L'Élégance Pure</h2>
            <p>Une signature olfactive unique pour votre espace</p>
            <a href="#collection" class="hero-btn">Explorer La Collection</a>
        </div>
    </div>

    <!-- Section Title -->
    <div class="section-title" id="collection">
        <h3>Les Créations</h3>
    </div>

    <!-- Products Grid Container -->
    <div class="container">
        <div class="products-grid">

            <!-- Article 1: Vénus (Taswira 7a9i9ya + Link WhatsApp jdid) -->
            <div class="product-card">
                <div class="product-img-box" style="background-image: url('1000010045.jpg');"></div>
                <div class="product-info">
                    <div class="product-category">Édition Prestige</div>
                    <h4 class="product-title">Vénus Signature</h4>
                    <div class="product-price">45.000 DT</div>
                    <a href="https://wa.me/21665037357?text=Bonjour,%20je%20souhaite%20commander%20le%20parfum%20Vénus" target="_blank" class="btn-buy">Commander via WhatsApp</a>
                </div>
            </div>

            <!-- Article 2: Fraise (Link WhatsApp jdid) -->
            <div class="product-card">
                <div class="product-img-box" style="background-image: url('https://images.unsplash.com/photo-1615485290382-441e4d049cb5?q=80&w=600&auto=format&fit=crop');"></div>
                <div class="product-info">
                    <div class="product-category">Brume d'ambiance</div>
                    <h4 class="product-title">Fraise Intense</h4>
                    <div class="product-price">25.000 DT</div>
                    <a href="https://wa.me/21665037357?text=Bonjour,%20je%20souhaite%20commander%20la%20brume%20Fraise" target="_blank" class="btn-buy">Commander via WhatsApp</a>
                </div>
            </div>

            <!-- Article 3: Mango & Papaya (Link WhatsApp jdid) -->
            <div class="product-card">
                <div class="product-img-box" style="background-image: url('https://images.unsplash.com/photo-1601924582970-9238b14e392e?q=80&w=600&auto=format&fit=crop');"></div>
                <div class="product-info">
                    <div class="product-category">Brume d'ambiance</div>
                    <h4 class="product-title">Mango & Papaya</h4>
                    <div class="product-price">25.000 DT</div>
                    <a href="https://wa.me/21665037357?text=Bonjour,%20je%20souhaite%20commander%20la%20brume%20Mango%20%26%20Papaya" target="_blank" class="btn-buy">Commander via WhatsApp</a>
                </div>
            </div>

        </div>
    </div>

    <!-- Footer -->
    <footer>
        <p>© 2026 GHARAMI STORE. ALL RIGHTS RESERVED.</p>
        <p style="font-size: 9px; color: #444; letter-spacing: 3px;">HAUTE PARFUMERIE & DESIGN</p>
    </footer>

</body>
</html>
