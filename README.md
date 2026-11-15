<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DreamWay Travels - आपकी यात्रा, हमारी जिम्मेदारी</title>
    <!-- Google Fonts -->
    <link href="https://googleapis.com" rel="stylesheet">
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cloudflare.com">
    
    <style>
        /* === CSS STYLING (यहाँ से आप रंग और डिज़ाइन बदल सकते हैं) === */
        :root {
            --primary-color: #ff6b35; /* मुख्य नारंगी रंग */
            --secondary-color: #004e89; /* गहरा नीला रंग */
            --light-bg: #f8f9fa;
            --dark-text: #2b2d42;
            --whatsapp-green: #25D366;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            color: var(--dark-text);
            line-height: 1.6;
        }

        /* Navbar */
        header {
            background: #fff;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--secondary-color);
            text-decoration: none;
        }

        .logo span {
            color: var(--primary-color);
        }

        nav a {
            margin-left: 25px;
            text-decoration: none;
            color: var(--dark-text);
            font-weight: 500;
            transition: 0.3s;
        }

        nav a:hover {
            color: var(--primary-color);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.55), rgba(0, 0, 0, 0.55)), url('https://unsplash.com') center/cover no-repeat;
            height: 85vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #fff;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin-bottom: 30px;
        }

        .btn {
            background: var(--primary-color);
            color: #fff;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: 0.3s;
            border: none;
            cursor: pointer;
            display: inline-block;
        }

        .btn:hover {
            background: #e55a2b;
            transform: translateY(-2px);
        }

        /* Packages Section */
        .section {
            padding: 70px 5%;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            color: var(--secondary-color);
            margin-bottom: 10px;
        }

        .section-subtitle {
            text-align: center;
            color: #666;
            margin-bottom: 40px;
        }

        /* Filter Buttons */
        .filter-buttons {
            text-align: center;
            margin-bottom: 40px;
        }

        .filter-btn {
            background: #eee;
            border: none;
            padding: 10px 25px;
            margin: 5px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: 600;
            transition: 0.3s;
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--secondary-color);
            color: #fff;
        }

        /* Package Cards Grid */
        .packages-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background: #fff;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-8px);
        }

        .card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }

        .card-content {
            padding: 20px;
        }

        .badge {
            background: #e0fbfc;
            color: var(--secondary-color);
            padding: 4px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .card h3 {
            margin: 10px 0;
            font-size: 1.4rem;
        }

        .card p {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 15px;
        }

        .price-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-top: 1px solid #eee;
            padding-top: 15px;
        }

        .price {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--primary-color);
        }

        .whatsapp-btn {
            background: var(--whatsapp-green);
            color: #fff;
            padding: 8px 15px;
            border-radius: 8px;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        /* Why Choose Us */
        .features {
            background: var(--light-bg);
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 25px;
            text-align: center;
        }

        .feature-box {
            background: #fff;
            padding: 30px 20px;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
        }

        .feature-box i {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }

        /* Inquiry Form */
        .inquiry-container {
            max-width: 600px;
            margin: 0 auto;
            background: #fff;
            padding: 35px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 600;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
        }

        /* Floating WhatsApp Button */
        .float-wa {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background: var(--whatsapp-green);
            color: #fff;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 30px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.25);
            z-index: 1000;
            text-decoration: none;
        }

        /* Footer */
        footer {
            background: var(--secondary-color);
            color: #fff;
            text-align: center;
            padding: 30px 20px;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2rem; }
            nav { display: none; } /* मोबाइल पर सिंपल लुक के लिए */
        }
    </style>
</head>
<body>

    <!-- Header / Navbar -->
    <header>
        <a href="#" class="logo">DreamWay<span>Travels</span></a>
        <nav>
            <a href="#home">Home</a>
            <a href="#packages">Tour Packages</a>
            <a href="#why-us">Why Us</a>
            <a href="#contact">Book Now</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <h1>अपनी सपनों की यात्रा शुरू करें</h1>
        <p>भारत और विदेश के सबसे बेहतरीन टूर पैकेज, शानदार होटल्स और सुरक्षित सफर के साथ।</p>
        <a href="#packages" class="btn">पैकेज देखें (Explore Packages)</a>
    </section>

    <!-- Tour Packages Section -->
    <section class="section" id="packages">
        <h2 class="section-title">पॉपुलर टूर पैकेज</h2>
        <p class="section-subtitle">अपने बजट और पसंद के अनुसार बेहतरीन डेस्टिनेशन चुनें</p>

        <!-- Filter Buttons -->
        <div class="filter-buttons">
            <button class="filter-btn active" onclick="filterPackages('all')">सभी (All)</button>
            <button class="filter-btn" onclick="filterPackages('domestic')">भारत (Domestic)</button>
            <button class="filter-btn" onclick="filterPackages('international')">विदेश (International)</button>
        </div>

        <!-- Packages Grid -->
        <div class="packages-grid">
            
            <!-- Package 1 -->
            <div class="card package-item" data-category="domestic">
                <img src="https://unsplash.com" alt="Manali Tour">
                <div class="card-content">
                    <span class="badge">5 Days / 4 Nights</span>
                    <h3>मनाली और सोलंग वैली स्पेशल</h3>
                    <p>3-स्टार होटल, सुबह का नाश्ता और डिनर, प्राइवेट कैब और सभी साइटसीइंग शामिल।</p>
                    <div class="price-row">
