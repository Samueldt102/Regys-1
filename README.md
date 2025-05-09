# Regys-1
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RegyPos - Especialistas en Celulares TECNO</title>
    <style>
        /* Estilos generales */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            scroll-behavior: smooth;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        /* Header y navegación */
        header {
            background-color: #000;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            height: 60px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 2rem;
        }
        
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            font-size: 1.1rem;
        }
        
        nav ul li a:hover {
            color: #00b4ff;
        }
        
        /* Hero section */
        .hero {
            height: 80vh;
            background: linear-gradient(135deg, #000 0%, #222 100%);
            color: white;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><circle cx="50" cy="50" r="40" stroke="%2300b4ff" stroke-width="1" fill="none" opacity="0.2"/></svg>');
            background-size: 300px 300px;
            opacity: 0.3;
        }
        
        .hero-content {
            width: 50%;
            position: relative;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            line-height: 1.2;
        }
        
        .hero h1 span {
            color: #00b4ff;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            max-width: 600px;
        }
        
        .btn {
            display: inline-block;
            background-color: #00b4ff;
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            border: 2px solid #00b4ff;
        }
        
        .btn:hover {
            background-color: transparent;
            color: #00b4ff;
        }
        
        .btn-secondary {
            background-color: transparent;
            color: white;
            border: 2px solid white;
            margin-left: 1rem;
        }
        
        .btn-secondary:hover {
            background-color: white;
            color: #000;
        }
        
        .hero-image {
            position: absolute;
            right: 5%;
            bottom: 0;
            width: 40%;
            max-width: 500px;
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        
        /* Sección de video destacado */
        .featured-video {
            padding: 5rem 0;
            background-color: #000;
            color: white;
        }
        
        .video-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .video-wrapper {
            width: 100%;
            max-width: 900px;
            margin: 2rem auto;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            position: relative;
        }
        
        .video-wrapper video {
            width: 100%;
            display: block;
        }
        
        .video-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto 2rem;
        }
        
        .video-content h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #fff;
        }
        
        .video-content p {
            font-size: 1.2rem;
            color: #ccc;
            margin-bottom: 2rem;
        }
        
        /* Sección de características */
        .features {
            padding: 5rem 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: #333;
            margin-bottom: 1rem;
        }
        
        .section-title p {
            color: #777;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .feature-card {
            background-color: #f9f9f9;
            border-radius: 10px;
            padding: 2rem;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: #00b4ff;
            margin-bottom: 1.5rem;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }
        
        /* Sección de productos */
        .products {
            padding: 5rem 0;
            background-color: #f5f5f5;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }
        
        .product-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
        }
        
        .product-image {
            height: 300px;
            width: 100%;
            object-fit: contain;
            border-bottom: 1px solid #eee;
            padding: 1rem;
            background-color: #f9f9f9;
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }
        
        .product-info p {
            color: #777;
            margin-bottom: 1rem;
        }
        
        .product-price {
            font-size: 1.5rem;
            font-weight: bold;
            color: #00b4ff;
            margin-bottom: 1rem;
        }
        
        /* Sección de testimonios */
        .testimonials {
            padding: 5rem 0;
            background-color: #000;
            color: white;
        }
        
        .testimonials .section-title h2 {
            color: white;
        }
        
        .testimonials .section-title p {
            color: #ccc;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .testimonial-card {
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 2rem;
            position: relative;
        }
        
        .testimonial-card::before {
            content: '"';
            position: absolute;
            top: 10px;
            left: 10px;
            font-size: 5rem;
            color: rgba(255, 255, 255, 0.1);
            font-family: Georgia, serif;
        }
        
        .testimonial-text {
            margin-bottom: 1.5rem;
            font-style: italic;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-image {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin-right: 1rem;
        }
        
        .author-info h4 {
            margin-bottom: 0.2rem;
        }
        
        .author-info p {
            color: #00b4ff;
            font-size: 0.9rem;
        }
        
        /* Sección de contacto */
        .contact {
            padding: 5rem 0;
            background-color: white;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: #333;
        }
        
        .contact-info p {
            margin-bottom: 1.5rem;
            color: #666;
        }
        
        .contact-details {
            margin-top: 2rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .contact-icon {
            width: 40px;
            height: 40px;
            background-color: #00b4ff;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 1rem;
            color: white;
            font-size: 1.2rem;
        }
        
        .contact-form {
            background-color: #f9f9f9;
            padding: 2rem;
            border-radius: 10px;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        textarea.form-control {
            height: 150px;
            resize: vertical;
        }
        
        .form-btn {
            background-color: #00b4ff;
            color: white;
            border: none;
            padding: 0.8rem 2rem;
            border-radius: 30px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .form-btn:hover {
            background-color: #0090cc;
        }
        
        /* Footer */
        footer {
            background-color: #111;
            color: white;
            padding: 3rem 0 1rem;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-logo {
            height: 50px;
            margin-bottom: 1rem;
        }
        
        .footer-about p {
            color: #ccc;
            margin-bottom: 1.5rem;
        }
        
        .social-links {
            display: flex;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 0.5rem;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .social-link:hover {
            background-color: #00b4ff;
        }
        
        .footer-links h3, .footer-contact h3, .footer-newsletter h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            color: white;
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links ul li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links ul li a:hover {
            color: #00b4ff;
        }
        
        .footer-contact p {
            color: #ccc;
            margin-bottom: 0.8rem;
            display: flex;
            align-items: center;
        }
        
        .footer-contact p i {
            margin-right: 0.5rem;
            color: #00b4ff;
        }
        
        .newsletter-form {
            display: flex;
        }
        
        .newsletter-input {
            flex: 1;
            padding: 0.8rem;
            border: none;
            border-radius: 5px 0 0 5px;
            font-size: 0.9rem;
        }
        
        .newsletter-btn {
            background-color: #00b4ff;
            color: white;
            border: none;
            padding: 0 1rem;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #ccc;
            font-size: 0.9rem;
        }
        
        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animate {
            animation: fadeIn 1s ease forwards;
        }
        
        /* Controles de video personalizados */
        .video-controls {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            padding: 10px;
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .video-wrapper:hover .video-controls {
            opacity: 1;
        }
        
        .play-btn {
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            margin-right: 10px;
        }
        
        .progress-bar {
            flex: 1;
            height: 5px;
            background: rgba(255, 255, 255, 0.3);
            cursor: pointer;
            position: relative;
        }
        
        .progress {
            height: 100%;
            background: #00b4ff;
            width: 0;
        }
        
        /* Bienvenida */
        .welcome-banner {
            background-color: #00b4ff;
            color: white;
            text-align: center;
            padding: 1rem 0;
            font-size: 1.2rem;
            font-weight: bold;
            position: relative;
            overflow: hidden;
        }
        
        .welcome-banner::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 50%;
            height: 100%;
            background: rgba(255, 255, 255, 0.2);
            transform: skewX(-25deg);
            animation: shine 3s infinite;
        }
        
        @keyframes shine {
            0% { left: -100%; }
            20% { left: 100%; }
            100% { left: 100%; }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .nav-container {
                flex-direction: column;
                padding: 1rem 0;
            }
            
            nav ul {
                margin-top: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0.5rem;
            }
            
            .hero {
                height: auto;
                padding: 4rem 0;
            }
            
            .hero-content {
                width: 100%;
                text-align: center;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-image {
                position: relative;
                width: 80%;
                margin: 3rem auto 0;
                right: auto;
                bottom: auto;
            }
            
            .btn {
                display: block;
                margin: 1rem auto;
                width: 80%;
                text-align: center;
            }
            
            .btn-secondary {
                margin-left: 0;
            }
            
            .video-wrapper {
                margin: 1rem auto;
            }
        }
        
        /* Estilos para el botón de menú móvil */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
                position: absolute;
                top: 1.5rem;
                right: 1.5rem;
            }
            
            nav ul {
                display: none;
                width: 100%;
                flex-direction: column;
                text-align: center;
            }
            
            nav ul.show {
                display: flex;
            }
            
            nav ul li {
                margin: 0.5rem 0;
            }
        }
    </style>
</head>
<body>
    <!-- Banner de bienvenida -->
    <div class="welcome-banner">
        ¡Bienvenidos a RegyPos! Distribuidor oficial de celulares TECNO
    </div>

    <!-- Header y navegación -->
    <header>
        <div class="container nav-container">
            <img src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/WhatsApp%20Image%202025-01-27%20at%208.54.59%20AM-2Gve46XEeGtGzFopYYceeOGFE2cgpl.jpeg" alt="RegyPos Logo" class="logo">
            <button class="menu-toggle" id="menuToggle">☰</button>
            <nav>
                <ul id="navMenu">
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#video">Video</a></li>
                    <li><a href="#productos">Productos</a></li>
                    <li><a href="#caracteristicas">Características</a></li>
                    <li><a href="#testimonios">Testimonios</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero section -->
    <section class="hero" id="inicio">
        <div class="container">
            <div class="hero-content">
                <h1>Descubre la Tecnología <span>TECNO</span> con RegyPos</h1>
                <p>Somos distribuidores oficiales de celulares TECNO. Ofrecemos los últimos modelos con la mejor tecnología y al mejor precio del mercado.</p>
                <a href="#productos" class="btn">Ver Productos</a>
                <a href="#contacto" class="btn btn-secondary">Contáctanos</a>
            </div>
            <img src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/Spark%2030C.jpg-urwYDOjTHW9vDtUXBOhKrWVZDhvC4n.jpeg" alt="Celular TECNO Spark 30C" class="hero-image">
        </div>
    </section>

    <!-- Sección de video destacado -->
    <section class="featured-video" id="video">
        <div class="container">
            <div class="video-content">
                <h2>Descubre el Nuevo TECNO Spark</h2>
                <p>Mira este increíble video del nuevo TECNO Spark y descubre todas sus características y funcionalidades. Un smartphone diseñado para superar tus expectativas.</p>
            </div>
            <div class="video-container">
                <div class="video-wrapper">
                    <video id="featured-video" controls>
                        <source src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/spark%20-pt44MADAvrqDQQGTSUct4GlFlZT5LS.mp4" type="video/mp4">
                        Tu navegador no soporta videos HTML5.
                    </video>
                </div>
                <a href="#productos" class="btn">Ver Detalles del Producto</a>
            </div>
        </div>
    </section>

    <!-- Sección de características -->
    <section class="features" id="caracteristicas">
        <div class="container">
            <div class="section-title">
                <h2>¿Por qué elegir RegyPos?</h2>
                <p>Somos especialistas en tecnología móvil y ofrecemos los mejores servicios para nuestros clientes.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">📱</div>
                    <h3>Últimos Modelos</h3>
                    <p>Tenemos los modelos más recientes de la marca TECNO con las mejores características del mercado.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💰</div>
                    <h3>Precios Competitivos</h3>
                    <p>Ofrecemos los mejores precios del mercado y promociones exclusivas para nuestros clientes.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🛠️</div>
                    <h3>Servicio Técnico</h3>
                    <p>Contamos con servicio técnico especializado para reparaciones y mantenimiento de tus dispositivos.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🚚</div>
                    <h3>Envío Gratuito</h3>
                    <p>Envío gratuito en compras superiores a $500 a cualquier parte del país.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🔒</div>
                    <h3>Garantía Oficial</h3>
                    <p>Todos nuestros productos cuentan con garantía oficial de la marca TECNO.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">👨‍💼</div>
                    <h3>Asesoría Personalizada</h3>
                    <p>Te asesoramos para que encuentres el dispositivo que mejor se adapte a tus necesidades.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección de productos -->
    <section class="products" id="productos">
        <div class="container">
            <div class="section-title">
                <h2>Nuestros Productos</h2>
                <p>Descubre nuestra selección de celulares TECNO con las mejores características y precios.</p>
            </div>
            <div class="products-grid">
                <div class="product-card">
                    <img src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/Spark%2030C.jpg-urwYDOjTHW9vDtUXBOhKrWVZDhvC4n.jpeg" alt="TECNO Spark 30C" class="product-image">
                    <div class="product-info">
                        <h3>TECNO Spark 30C</h3>
                        <p>Pantalla de 6.78", 8GB RAM, 128GB almacenamiento, cámara de 50MP</p>
                        <div class="product-price">$279.99</div>
                        <a href="#contacto" class="btn">Comprar Ahora</a>
                    </div>
                </div>
                <div class="product-card">
                    <img src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/camon%2030%20Pro.jpg-PLelM4TremXL9bCcL32wIktcLgHKUO.jpeg" alt="TECNO Camon 30 Pro" class="product-image">
                    <div class="product-info">
                        <h3>TECNO Camon 30 Pro</h3>
                        <p>Cámara de 108MP, 12GB RAM, 256GB almacenamiento, pantalla AMOLED</p>
                        <div class="product-price">$399.99</div>
                        <a href="#contacto" class="btn">Comprar Ahora</a>
                    </div>
                </div>
                <div class="product-card">
                    <img src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/Spark%20go%201-QowhzvaX4x4jV8nPVJQc9zmTfHlzb7.png" alt="TECNO Spark Go" class="product-image">
                    <div class="product-info">
                        <h3>TECNO Spark Go</h3>
                        <p>Disponible en blanco y negro, 4GB RAM, 64GB almacenamiento</p>
                        <div class="product-price">$149.99</div>
                        <a href="#contacto" class="btn">Comprar Ahora</a>
                    </div>
                </div>
                <div class="product-card">
                    <img src="/placeholder.svg?height=250&width=250" alt="TECNO Phantom X2" class="product-image">
                    <div class="product-info">
                        <h3>TECNO Phantom X2</h3>
                        <p>Procesador MediaTek, 8GB RAM, 256GB almacenamiento</p>
                        <div class="product-price">$399.99</div>
                        <a href="#contacto" class="btn">Comprar Ahora</a>
                    </div>
                </div>
                <div class="product-card">
                    <img src="/placeholder.svg?height=250&width=250" alt="TECNO Pova 5 Pro" class="product-image">
                    <div class="product-info">
                        <h3>TECNO Pova 5 Pro</h3>
                        <p>Batería 6000mAh, 8GB RAM, 128GB almacenamiento</p>
                        <div class="product-price">$279.99</div>
                        <a href="#contacto" class="btn">Comprar Ahora</a>
                    </div>
                </div>
                <div class="product-card">
                    <img src="/placeholder.svg?height=250&width=250" alt="TECNO Pop 7 Pro" class="product-image">
                    <div class="product-info">
                        <h3>TECNO Pop 7 Pro</h3>
                        <p>Pantalla HD+, 4GB RAM, 64GB almacenamiento</p>
                        <div class="product-price">$149.99</div>
                        <a href="#contacto" class="btn">Comprar Ahora</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección de testimonios -->
    <section class="testimonials" id="testimonios">
        <div class="container">
            <div class="section-title">
                <h2>Lo que dicen nuestros clientes</h2>
                <p>Opiniones de clientes satisfechos con nuestros productos y servicios.</p>
            </div>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">Compré mi TECNO Spark 30C en RegyPos y estoy encantado con el servicio. El teléfono es excelente y la atención fue impecable.</p>
                    <div class="testimonial-author">
                        <img src="/placeholder.svg?height=50&width=50" alt="Carlos Rodríguez" class="author-image">
                        <div class="author-info">
                            <h4>Carlos Rodríguez</h4>
                            <p>Cliente desde 2022</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">El servicio técnico de RegyPos es excelente. Repararon mi celular en tiempo récord y a un precio muy razonable.</p>
                    <div class="testimonial-author">
                        <img src="/placeholder.svg?height=50&width=50" alt="María López" class="author-image">
                        <div class="author-info">
                            <h4>María López</h4>
                            <p>Cliente desde 2021</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">Los precios de RegyPos son inmejorables. Comparé en varias tiendas y aquí encontré el mejor precio para mi TECNO Camon 30 Pro.</p>
                    <div class="testimonial-author">
                        <img src="/placeholder.svg?height=50&width=50" alt="Juan Pérez" class="author-image">
                        <div class="author-info">
                            <h4>Juan Pérez</h4>
                            <p>Cliente desde 2023</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección de contacto -->
    <section class="contact" id="contacto">
        <div class="container">
            <div class="section-title">
                <h2>Contáctanos</h2>
                <p>Estamos aquí para ayudarte. Ponte en contacto con nosotros para cualquier consulta o pedido.</p>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Información de Contacto</h3>
                    <p>Si tienes alguna pregunta sobre nuestros productos o servicios, no dudes en contactarnos. Estaremos encantados de atenderte.</p>
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">📍</div>
                            <p>Av. Principal #123, Ciudad</p>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">📞</div>
                            <p>+123 456 7890</p>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">✉️</div>
                            <p>info@regypos.com</p>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">🕒</div>
                            <p>Lun - Vie: 9:00 AM - 6:00 PM</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Nombre</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Correo Electrónico</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Teléfono</label>
                            <input type="tel" id="phone" class="form-control">
                        </div>
                        <div class="form-group">
                            <label for="message">Mensaje</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="form-btn">Enviar Mensaje</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-about">
                    <img src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/WhatsApp%20Image%202025-01-27%20at%208.54.59%20AM-2Gve46XEeGtGzFopYYceeOGFE2cgpl.jpeg" alt="RegyPos Logo" class="footer-logo">
                    <p>RegyPos es distribuidor oficial de celulares TECNO. Ofrecemos los últimos modelos con la mejor tecnología y al mejor precio del mercado.</p>
                    <div class="social-links">
                        <a href="#" class="social-link">FB</a>
                        <a href="#" class="social-link">IG</a>
                        <a href="#" class="social-link">TW</a>
                        <a href="#" class="social-link">YT</a>
                    </div>
                </div>
                <div class="footer-links">
                    <h3>Enlaces Rápidos</h3>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#video">Video</a></li>
                        <li><a href="#productos">Productos</a></li>
                        <li><a href="#caracteristicas">Características</a></li>
                        <li><a href="#testimonios">Testimonios</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </div>
                <div class="footer-contact">
                    <h3>Contacto</h3>
                    <p><i>📍</i> Av. Principal #123, Ciudad</p>
                    <p><i>📞</i> +123 456 7890</p>
                    <p><i>✉️</i> info@regypos.com</p>
                </div>
                <div class="footer-newsletter">
                    <h3>Boletín Informativo</h3>
                    <p>Suscríbete para recibir las últimas novedades y ofertas especiales.</p>
                    <form class="newsletter-form">
                        <input type="email" placeholder="Tu correo electrónico" class="newsletter-input" required>
                        <button type="submit" class="newsletter-btn">→</button>
                    </form>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 RegyPos. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript para el menú móvil y navegación suave -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const menuToggle = document.getElementById('menuToggle');
            const navMenu = document.getElementById('navMenu');
            
            menuToggle.addEventListener('click', function() {
                navMenu.classList.toggle('show');
            });
            
            // Cerrar menú al hacer clic en un enlace
            const navLinks = document.querySelectorAll('nav ul li a');
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    // Navegación suave
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetSection = document.querySelector(targetId);
                    
                    window.scrollTo({
                        top: targetSection.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    navMenu.classList.remove('show');
                });
            });
            
            // Navegación suave para botones
            const actionButtons = document.querySelectorAll('.btn');
            actionButtons.forEach(button => {
                if (button.getAttribute('href') && button.getAttribute('href').startsWith('#')) {
                    button.addEventListener('click', function(e) {
                        e.preventDefault();
                        const targetId = this.getAttribute('href');
                        const targetSection = document.querySelector(targetId);
                        
                        window.scrollTo({
                            top: targetSection.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    });
                }
            });
            
            // Animación al hacer scroll
            const animateElements = document.querySelectorAll('.feature-card, .product-card, .testimonial-card');
            
            function checkScroll() {
                animateElements.forEach(element => {
                    const elementPosition = element.getBoundingClientRect().top;
                    const screenPosition = window.innerHeight / 1.3;
                    
                    if (elementPosition < screenPosition) {
                        element.classList.add('animate');
                    }
                });
            }
            
            window.addEventListener('scroll', checkScroll);
            checkScroll(); // Verificar elementos visibles al cargar la página
            
            // Reproducción automática del video cuando está en el viewport
            const video = document.getElementById('featured-video');
            
            function checkVideoVisibility() {
                const videoPosition = video.getBoundingClientRect();
                const isVisible = (
                    videoPosition.top >= 0 &&
                    videoPosition.bottom <= window.innerHeight
                );
                
                if (isVisible) {
                    if (video.paused) {
                        // Reproducir solo si el usuario ha interactuado con la página
                        if (document.documentElement.classList.contains('user-interacted')) {
                            video.play();
                        }
                    }
                } else {
                    if (!video.paused) {
                        video.pause();
                    }
                }
            }
            
            // Marcar que el usuario ha interactuado con la página
            document.addEventListener('click', function() {
                document.documentElement.classList.add('user-interacted');
            });
            
            window.addEventListener('scroll', checkVideoVisibility);
            window.addEventListener('resize', checkVideoVisibility);
            checkVideoVisibility();
        });
    </script>
</body>
</html>
