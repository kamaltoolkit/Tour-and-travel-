<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DreamWay Travels - आपकी यात्रा, हमारी जिम्मेदारी</title>
    <meta name="description" content="DreamWay Travels - भारत और विदेश के बेहतरीन टूर पैकेज। Manali, Goa, Kerala, Dubai, Thailand और भी बहुत कुछ।">
    <meta property="og:title" content="DreamWay Travels">
    <meta property="og:description" content="आपकी यात्रा, हमारी जिम्मेदारी">
    <meta property="og:type" content="website">
    <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>✈️</text></svg>">

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --primary-color: #ff6b35;
            --secondary-color: #004e89;
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
            overflow-x: hidden;
        }

        /* ---------- Navbar ---------- */
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

        .logo span { color: var(--primary-color); }

        nav {
            display: flex;
            align-items: center;
        }

        nav a {
            margin-left: 25px;
            text-decoration: none;
            color: var(--dark-text);
            font-weight: 500;
            transition: 0.3s;
        }

        nav a:hover { color: var(--primary-color); }

        .menu-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.6rem;
            color: var(--secondary-color);
            cursor: pointer;
        }

        /* ---------- Hero ---------- */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.55), rgba(0,0,0,0.55)),
                        url('https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=1600&q=80') center/cover no-repeat;
            min-height: 85vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #fff;
            padding: 20px;
        }

        .hero h1 { font-size: 3rem; margin-bottom: 15px; }
        .hero p { font-size: 1.2rem; max-width: 600px; margin-bottom: 30px; }

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

        /* ---------- Sections ---------- */
        .section { padding: 70px 5%; }

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

        /* ---------- Filter ---------- */
        .filter-buttons {
            text-align: center;
            margin-bottom: 40px;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 8px;
        }

        .filter-btn {
            background: #eee;
            border: none;
            padding: 10px 25px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: 600;
            transition: 0.3s;
            font-family: inherit;
        }

        .filter-btn.active,
        .filter-btn:hover {
            background: var(--secondary-color);
            color: #fff;
        }

        /* ---------- Cards ---------- */
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
            display: flex;
            flex-direction: column;
        }

        .card:hover { transform: translateY(-8px); }

        .card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }

        .card-content {
            padding: 20px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .badge {
            background: #e0fbfc;
            color: var(--secondary-color);
            padding: 4px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: 600;
            align-self: flex-start;
        }

        .card h3 { margin: 10px 0; font-size: 1.4rem; }
        .card p { color: #666; font-size: 0.9rem; margin-bottom: 15px; flex-grow: 1; }

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
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: 0.3s;
        }

        .whatsapp-btn:hover { background: #1eb356; }

        /* ---------- Features ---------- */
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
            transition: 0.3s;
        }

        .feature-box:hover { transform: translateY(-5px); }

        .feature-box i {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }

        .feature-box h3 { margin-bottom: 8px; color: var(--secondary-color); }
        .feature-box p { font-size: 0.9rem; color: #666; }

        /* ---------- Inquiry Form ---------- */
        .inquiry-section { background: var(--light-bg); }

        .inquiry-container {
            max-width: 600px;
            margin: 0 auto;
            background: #fff;
            padding: 35px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .form-group { margin-bottom: 20px; }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 600;
            font-size: 0.95rem;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            font-family: inherit;
            transition: 0.3s;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(255,107,53,0.15);
        }

        .form-group textarea { resize: vertical; min-height: 90px; }

        /* ---------- Floating WhatsApp ---------- */
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
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(37,211,102,0.5); }
            70% { box-shadow: 0 0 0 15px rgba(37,211,102,0); }
            100% { box-shadow: 0 0 0 0 rgba(37,211,102,0); }
        }

        /* ---------- Footer ---------- */
        footer {
            background: var(--secondary-color);
            color: #fff;
            padding: 50px 5% 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 30px;
            max-width: 1100px;
            margin: 0 auto;
        }

        .footer-col h4 {
            margin-bottom: 15px;
            color: var(--primary-color);
            font-size: 1.1rem;
        }

        .footer-col p,
        .footer-col a {
            color: #dce5ec;
            font-size: 0.9rem;
            text-decoration: none;
            display: block;
            margin-bottom: 8px;
            transition: 0.3s;
        }

        .footer-col a:hover { color: var(--primary-color); }

        .social-icons {
            display: flex;
            gap: 12px;
            margin-top: 10px;
        }

        .social-icons a {
            background: rgba(255,255,255,0.1);
            width: 38px;
            height: 38px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1rem;
        }

        .social-icons a:hover { background: var(--primary-color); }

        .copyright {
            text-align: center;
            margin-top: 35px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.15);
            font-size: 0.85rem;
            color: #c0cbd6;
        }

        /* ---------- Mobile ---------- */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2rem; }
            .hero p { font-size: 1rem; }
            .section-title { font-size: 1.7rem; }

            .menu-toggle { display: block; }

            nav {
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: #fff;
                flex-direction: column;
                align-items: flex-start;
                padding: 15px 5%;
                box-shadow: 0 5px 15px rgba(0,0,0,0.1);
                transform: translateY(-150%);
                opacity: 0;
                transition: 0.35s ease;
                pointer-events: none;
            }

            nav.open {
                transform: translateY(0);
                opacity: 1;
                pointer-events: auto;
            }

            nav a {
                margin: 10px 0;
                display: block;
                width: 100%;
            }

            .inquiry-container { padding: 25px 20px; }
        }
    </style>
</head>
<body>

    <!-- ============ HEADER ============ -->
    <header>
        <a href="#" class="logo">DreamWay<span>Travels</span></a>
        <button class="menu-toggle" id="menuToggle" aria-label="Menu">
            <i class="fas fa-bars"></i>
        </button>
        <nav id="navMenu">
            <a href="#home">Home</a>
            <a href="#packages">Tour Packages</a>
            <a href="#why-us">Why Us</a>
            <a href="#contact">Book Now</a>
        </nav>
    </header>

    <!-- ============ HERO ============ -->
    <section class="hero" id="home">
        <h1>अपनी सपनों की यात्रा शुरू करें</h1>
        <p>भारत और विदेश के सबसे बेहतरीन टूर पैकेज, शानदार होटल्स और सुरक्षित सफर के साथ।</p>
        <a href="#packages" class="btn">पैकेज देखें (Explore Packages)</a>
    </section>

    <!-- ============ PACKAGES ============ -->
    <section class="section" id="packages">
        <h2 class="section-title">पॉपुलर टूर पैकेज</h2>
        <p class="section-subtitle">अपने बजट और पसंद के अनुसार बेहतरीन डेस्टिनेशन चुनें</p>

        <div class="filter-buttons">
            <button class="filter-btn active" onclick="filterPackages('all', this)">सभी (All)</button>
            <button class="filter-btn" onclick="filterPackages('domestic', this)">भारत (Domestic)</button>
            <button class="filter-btn" onclick="filterPackages('international', this)">विदेश (International)</button>
        </div>

        <div class="packages-grid" id="packagesGrid">

            <!-- Card 1: Manali -->
            <div class="card package-item" data-category="domestic">
                <img src="https://images.unsplash.com/photo-1626621341517-bbf3d9990a23?w=800&q=80" alt="Manali Tour" loading="lazy">
                <div class="card-content">
                    <span class="badge">5 Days / 4 Nights</span>
                    <h3>मनाली और सोलंग वैली स्पेशल</h3>
                    <p>3-स्टार होटल, सुबह का नाश्ता और डिनर, प्राइवेट कैब और सभी साइटसीइंग शामिल।</p>
                    <div class="price-row">
                        <span class="price">₹18,999</span>
                        <a href="https://wa.me/919876543210?text=नमस्ते! मुझे%20मनाली%20पैकेज%20की%20जानकारी%20चाहिए।"
                           target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Book
                        </a>
                    </div>
                </div>
            </div>

            <!-- Card 2: Goa -->
            <div class="card package-item" data-category="domestic">
                <img src="https://images.unsplash.com/photo-1512343879784-a960bf40e7f2?w=800&q=80" alt="Goa Tour" loading="lazy">
                <div class="card-content">
                    <span class="badge">4 Days / 3 Nights</span>
                    <h3>गोवा बीच पैराडाइज़</h3>
                    <p>बीच रिजॉर्ट, ब्रेकफास्ट, स्कूटर रेंटल और नॉर्थ-साउथ गोवा टूर शामिल।</p>
                    <div class="price-row">
                        <span class="price">₹14,499</span>
                        <a href="https://wa.me/919876543210?text=नमस्ते! मुझे%20गोवा%20पैकेज%20की%20जानकारी%20चाहिए।"
                           target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Book
                        </a>
                    </div>
                </div>
            </div>

            <!-- Card 3: Kerala -->
            <div class="card package-item" data-category="domestic">
                <img src="https://images.unsplash.com/photo-1602216056096-3b40cc0c9944?w=800&q=80" alt="Kerala Tour" loading="lazy">
                <div class="card-content">
                    <span class="badge">6 Days / 5 Nights</span>
                    <h3>केरल बैकवाटर्स</h3>
                    <p>हाउसबोट स्टे, मुन्नार टी गार्डन, आयुर्वेदिक स्पा और सभी मील्स शामिल।</p>
                    <div class="price-row">
                        <span class="price">₹24,999</span>
                        <a href="https://wa.me/919876543210?text=नमस्ते! मुझे%20केरल%20पैकेज%20की%20जानकारी%20चाहिए।"
                           target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Book
                        </a>
                    </div>
                </div>
            </div>

            <!-- Card 4: Dubai -->
            <div class="card package-item" data-category="international">
                <img src="https://images.unsplash.com/photo-1512453979798-5ea266f8880c?w=800&q=80" alt="Dubai Tour" loading="lazy">
                <div class="card-content">
                    <span class="badge">5 Days / 4 Nights</span>
                    <h3>दुबई सिटी ऑफ गोल्ड</h3>
                    <p>बुर्ज खलीफा, डेजर्ट सफारी, डीएचसीसी क्रूज़ और 4-स्टार होटल शामिल।</p>
                    <div class="price-row">
                        <span class="price">₹54,999</span>
                        <a href="https://wa.me/919876543210?text=नमस्ते! मुझे%20दुबई%20पैकेज%20की%20जानकारी%20चाहिए।"
                           target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Book
                        </a>
                    </div>
                </div>
            </div>

            <!-- Card 5: Thailand -->
            <div class="card package-item" data-category="international">
                <img src="https://images.unsplash.com/photo-1552465011-b4e21bf6e79a?w=800&q=80" alt="Thailand Tour" loading="lazy">
                <div class="card-content">
                    <span class="badge">6 Days / 5 Nights</span>
                    <h3>थाईलैंड फैंटेसी टूर</h3>
                    <p>बैंकॉक-पट्टाया, फ्लाइट, वीज़ा, होटल और सभी टूर शामिल।</p>
                    <div class="price-row">
                        <span class="price">₹42,999</span>
                        <a href="https://wa.me/919876543210?text=नमस्ते! मुझे%20थाईलैंड%20पैकेज%20की%20जानकारी%20चाहिए।"
                           target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Book
                        </a>
                    </div>
                </div>
            </div>

            <!-- Card 6: Bali -->
            <div class="card package-item" data-category="international">
                <img src="https://images.unsplash.com/photo-1537996194471-e657df975ab4?w=800&q=80" alt="Bali Tour" loading="lazy">
                <div class="card-content">
                    <span class="badge">7 Days / 6 Nights</span>
                    <h3>बाली हनीमून स्पेशल</h3>
                    <p>प्राइवेट विला, कपल स्पा, टैनाह लोट टूर और रोमांटिक डिनर शामिल।</p>
                    <div class="price-row">
                        <span class="price">₹68,999</span>
                        <a href="https://wa.me/919876543210?text=नमस्ते! मुझे%20बाली%20पैकेज%20की%20जानकारी%20चाहिए।"
                           target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Book
                        </a>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- ============ FEATURES ============ -->
    <section class="section features" id="why-us">
        <div class="feature-box">
            <i class="fas fa-shield-alt"></i>
            <h3>100% सुरक्षित</h3>
            <p>सभी ट्रिप्स verified होटल्स और trained गाइड्स के साथ।</p>
        </div>
        <div class="feature-box">
            <i class="fas fa-tags"></i>
            <h3>बेस्ट प्राइस</h3>
            <p>कोई hidden charges नहीं — जो दिखा वही final price।</p>
        </div>
        <div class="feature-box">
            <i class="fas fa-headset"></i>
            <h3>24×7 सपोर्ट</h3>
            <p>Trip के दौरान कभी भी help के लिए call/WhatsApp करें।</p>
        </div>
        <div class="feature-box">
            <i class="fas fa-undo"></i>
            <h3>Easy Cancellation</h3>
            <p>Flexible cancellation policy — बिना tension book करें।</p>
        </div>
    </section>

    <!-- ============ INQUIRY FORM ============ -->
    <section class="section inquiry-section" id="contact">
        <h2 class="section-title">Book Your Trip</h2>
        <p class="section-subtitle">फॉर्म भरें — हमारी टीम 24 घंटे में WhatsApp पर संपर्क करेगी</p>

        <div class="inquiry-container">
            <form id="inquiryForm">
                <div class="form-group">
                    <label for="name">आपका नाम *</label>
                    <input type="text" id="name" required placeholder="Full Name">
                </div>
                <div class="form-group">
                    <label for="phone">मोबाइल नंबर *</label>
                    <input type="tel" id="phone" required pattern="[0-9]{10}" placeholder="10-digit mobile number">
                </div>
                <div class="form-group">
                    <label for="destination">कहाँ जाना चाहते हैं? *</label>
                    <select id="destination" required>
                        <option value="">-- चुनें --</option>
                        <option>मनाली</option>
                        <option>गोवा</option>
                        <option>केरल</option>
                        <option>दुबई</option>
                        <option>थाईलैंड</option>
                        <option>बाली</option>
                        <option>अन्य</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="message">अतिरिक्त जानकारी (Optional)</label>
                    <textarea id="message" placeholder="कितने लोग, कब जाना है, बजट etc."></textarea>
                </div>
                <button type="submit" class="btn" style="width:100%;">
                    <i class="fab fa-whatsapp"></i> WhatsApp पर Enquiry भेजें
                </button>
            </form>
        </div>
    </section>

    <!-- ============ FOOTER ============ -->
    <footer>
        <div class="footer-grid">
            <div class="footer-col">
                <h4>DreamWay Travels</h4>
                <p>आपकी यात्रा, हमारी जिम्मेदारी। 10+ सालों से भरोसेमंद ट्रैवल पार्टनर।</p>
            </div>
            <div class="footer-col">
                <h4>Quick Links</h4>
                <a href="#home">Home</a>
                <a href="#packages">Packages</a>
                <a href="#why-us">Why Us</a>
                <a href="#contact">Contact</a>
            </div>
            <div class="footer-col">
                <h4>Contact</h4>
                <p><i class="fas fa-phone"></i> +91 98765 43210</p>
                <p><i class="fas fa-envelope"></i> hello@dreamwaytravels.in</p>
                <p><i class="fas fa-map-marker-alt"></i> Connaught Place, New Delhi</p>
            </div>
            <div class="footer-col">
                <h4>Follow Us</h4>
                <div class="social-icons">
                    <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
                    <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                    <a href="#" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
                    <a href="https://wa.me/919876543210" target="_blank" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
        </div>
        <div class="copyright">
            © 2025 DreamWay Travels. All Rights Reserved.
        </div>
    </footer>

    <!-- ============ FLOATING WHATSAPP ============ -->
    <a href="https://wa.me/919876543210?text=नमस्ते!%20मुझे%20tour%20package%20की%20जानकारी%20चाहिए।"
       class="float-wa" target="_blank" aria-label="WhatsApp">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- ============ JAVASCRIPT ============ -->
    <script>
        // Mobile Menu Toggle
        const menuToggle = document.getElementById('menuToggle');
        const navMenu = document.getElementById('navMenu');

        menuToggle.addEventListener('click', () => {
            navMenu.classList.toggle('open');
        });

        // Auto-close menu on link click (mobile)
        document.querySelectorAll('#navMenu a').forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('open');
            });
        });

        // Filter Packages
        function filterPackages(category, btn) {
            // Update active button
            document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
            btn.classList.add('active');

            // Show/Hide cards
            const items = document.querySelectorAll('.package-item');
            items.forEach(item => {
                const cat = item.dataset.category;
                if (category === 'all' || cat === category) {
                    item.style.display = 'block';
                    item.style.animation = 'fadeIn 0.4s ease';
                } else {
                    item.style.display = 'none';
                }
            });
        }

        // Fade animation (inject style)
        const style = document.createElement('style');
        style.textContent = `@keyframes fadeIn { from { opacity:0; transform: translateY(15px);} to {opacity:1; transform:translateY(0);} }`;
        document.head.appendChild(style);

        // Inquiry Form → WhatsApp
        document.getElementById('inquiryForm').addEventListener('submit', function(e) {
            e.preventDefault();

            const name = document.getElementById('name').value.trim();
            const phone = document.getElementById('phone').value.trim();
            const destination = document.getElementById('destination').value;
            const message = document.getElementById('message').value.trim();

            // Build WhatsApp message
            let waText = `*New Enquiry - DreamWay Travels*%0A%0A`;
            waText += `👤 Name: ${encodeURIComponent(name)}%0A`;
            waText += `📞 Phone: ${encodeURIComponent(phone)}%0A`;
            waText += `📍 Destination: ${encodeURIComponent(destination)}%0A`;
            if (message) waText += `📝 Message: ${encodeURIComponent(message)}%0A`;

            const waNumber = '919876543210'; // 👈 APNA NUMBER YAHAN DAALO
            const waURL = `https://wa.me/${waNumber}?text=${waText}`;

            window.open(waURL, '_blank');
        });
    </script>
</body>
</html>





