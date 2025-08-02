🔄 **HTML Edit Mode** - Processing your edit request...

Here are the changes needed to update the hero section with a fruit field background while keeping everything else intact:

```diff
<<<<<<< SEARCH
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ce81e5b4-3620-43fe-a86e-5709d85d43b5.png');
=======
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://placehold.co/1920x1080?text=Campo+de+Frutas+Frescas');
>>>>>>> REPLACE


```
```diff
<<<<<<< SEARCH
    <section class="hero" id="inicio">
=======
    <section class="hero" id="inicio" style="outline: rgb(0, 0, 0) dotted 3px; outline-offset: 1px;">
>>>>>>> REPLACE
```


Summary:
1. Changed hero section background image to a fruit field placeholder
2. Added temporary outline styling to highlight the hero section for visibilityHere is the updated HTML content after applying above edits:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verdulería Doña Lupita - Frutas y Verduras Frescas</title>
    <style>
        :root {
            --verde-primario: #4CAF50;
            --verde-secundario: #81C784;
            --verde-claro: #C8E6C9;
            --naranja: #FF9800;
            --blanco: #FFFFFF;
            --gris-claro: #F5F5F5;
            --texto-oscuro: #212121;
            --texto-claro: #757575;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--gris-claro);
            color: var(--texto-oscuro);
            line-height: 1.6;
        }
        
        header {
            background-color: var(--verde-primario);
            color: var(--blanco);
            padding: 1rem 2rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        .logo span {
            color: var(--naranja);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            color: var(--blanco);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--naranja);
        }
        
        .hero {
            height: 80vh;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://placehold.co/1920x1080?text=Campo+de+Frutas+Frescas');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--blanco);
            padding: 0 1rem;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.5rem;
            max-width: 800px;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--naranja);
            color: var(--blanco);
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: bold;
            text-decoration: none;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background-color: #F57C00;
            transform: translateY(-3px);
        }
        
        section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--verde-primario);
        }
        
        .about {
            background-color: var(--blanco);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .products {
            background-color: var(--verde-claro);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .product-card {
            background-color: var(--blanco);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .product-image {
            height: 200px;
            overflow: hidden;
        }
        
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-info h3 {
            margin-bottom: 0.5rem;
            color: var(--verde-primario);
        }
        
        .product-price {
            color: var(--naranja);
            font-weight: bold;
            font-size: 1.2rem;
            margin: 0.5rem 0;
        }
        
        .contact {
            background-color: var(--blanco);
        }
        
        .contact-content {
            display: flex;
            gap: 3rem;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-info p {
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }
        
        .contact-info i {
            margin-right: 0.5rem;
            color: var(--verde-primario);
        }
        
        .contact-form {
            flex: 1;
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
            min-height: 150px;
            resize: vertical;
        }
        
        footer {
            background-color: var(--verde-primario);
            color: var(--blanco);
            text-align: center;
            padding: 2rem;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            margin: 1rem 0;
        }
        
        .social-links a {
            color: var(--blanco);
            margin: 0 0.5rem;
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--naranja);
        }
        
        @media (max-width: 768px) {
            .about-content, .contact-content {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">Doña <span>Lupita</span></div>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#productos">Productos</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>
    
    <section class="hero" id="inicio" style="outline: rgb(0, 0, 0) dotted 3px; outline-offset: 1px;">
        <h1>Fruta y Verdura Fresca Directo del Campo</h1>
        <p>En Doña Lupita nos preocupamos por llevar a tu mesa los mejores productos naturales, seleccionados cuidadosamente para garantizar su frescura y sabor.</p>
        <a href="#productos" class="btn">Ver Productos</a>
    </section>
    
    <section class="about" id="nosotros">
        <h2 class="section-title">Nuestra Historia</h2>
        <div class="about-content">
            <div class="about-text">
                <p>Fundada en 1985, Verdulería Doña Lupita comenzó como un pequeño puesto de mercado en el barrio. Gracias a la calidad de nuestros productos y el trato personalizado, hemos crecido hasta convertirnos en un referente de confianza y calidad en la zona.</p>
                <p>Nuestros productos provienen directamente de pequeños productores locales, asegurando frescura y apoyando la economía de nuestra comunidad. Cada día seleccionamos personalmente las mejores frutas y verduras para ofrecerte solo lo mejor.</p>
                <p>Visítanos y descubre la diferencia de comprar en Doña Lupita, donde la tradición y la calidad se unen para ofrecerte lo mejor de la tierra.</p>
            </div>
            <div class="about-image">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/107b6e8d-c1bb-4209-b051-e2ae9260e31a.png" alt="Interior acogedor de la verdulería Doña Lupita, mostrando estantes llenos de frutas y verduras frescas con colores vibrantes y una atmósfera cálida y familiar">
            </div>
        </div>
    </section>
    
    <section class="products" id="productos">
        <h2 class="section-title">Nuestros Productos</h2>
        <div class="products-grid">
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ca867c44-5d66-4473-b17a-ca33e816ec9c.png" alt="Fresas rojas brillantes recién cosechadas con hojas verdes, dispuestas en cestas de mimbre sobre una mesa de madera">
                </div>
                <div class="product-info">
                    <h3>Fresas Frescas</h3>
                    <div class="product-price">$3.99 / lb</div>
                    <p>Fresas dulces y jugosas, cosechadas en su punto óptimo de maduración.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/e9c8ce8e-6a9c-4369-b87f-71738ecef156.png" alt="Tomates maduros de diferentes variedades, rojos, amarillos y verdes, organizados en cajas de madera bajo luz natural">
                </div>
                <div class="product-info">
                    <h3>Tomates Orgánicos</h3>
                    <div class="product-price">$2.49 / lb</div>
                    <p>Tomates cultivados sin pesticidas, con todo su sabor natural.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/8e5d9714-9854-49be-9102-acbf26c5e4ab.png" alt="Variedad de aguacates maduros y verdes cortados por la mitad mostrando su pulpa cremosa sobre una mesa rústica">
                </div>
                <div class="product-info">
                    <h3>Aguacates Hass</h3>
                    <div class="product-price">$2.99 / unidad</div>
                    <p>Aguacates cremosos, perfectos para guacamoles y ensaladas.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/dd7c9a13-39eb-4af8-bda5-9cf3e7cd8541.png" alt="Lechugas frescas de diferentes tipos (romana, iceberg, hoja roja) con gotas de agua brillando bajo la luz">
                </div>
                <div class="product-info">
                    <h3>Lechugas Frescas</h3>
                    <div class="product-price">$1.99 / unidad</div>
                    <p>Lechugas crujientes, recién cosechadas y prelavadas.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/aa220408-6c6f-475d-97d9-a8af97027e5c.png" alt="Manzanas rojas y verdes brillantes con gotas de rocío, apiladas en una canasta de mercería vintage">
                </div>
                <div class="product-info">
                    <h3>Manzanas Selectas</h3>
                    <div class="product-price">$1.49 / lb</div>
                    <p>Manzanas dulces y jugosas, perfectas para comer o cocinar.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/d4299073-687e-4e87-b446-362c60627aa4.png" alt="Zanahorias orgánicas recién cosechadas con tierra aún en sus raíces, mostrando sus hojas verdes sobre una mesa de madera rústica">
                </div>
                <div class="product-info">
                    <h3>Zanahorias Orgánicas</h3>
                    <div class="product-price">$1.29 / lb</div>
                    <p>Zanahorias dulces y crujientes, ricas en nutrientes.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="contact" id="contacto">
        <h2 class="section-title">Contáctanos</h2>
        <div class="contact-content">
            <div class="contact-info">
                <h3>Visítanos</h3>
                <p><i class="fas fa-map-marker-alt"></i> Calle Mercado 123, Barrio Central</p>
                <p><i class="fas fa-phone"></i> +56 2 2345 6789</p>
                <p><i class="fas fa-envelope"></i> hola@verdulerialupita.cl</p>
                <p><i class="fas fa-clock"></i> Lunes a Sábado: 8:00 - 20:00 hrs</p>
                <p><i class="fas fa-clock"></i> Domingo: 9:00 - 15:00 hrs</p>
            </div>
            <div class="contact-form">
                <h3>Envíanos un Mensaje</h3>
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Nombre</label>
                        <input type="text" id="name" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Mensaje</label>
                        <textarea id="message" class="form-control" required></textarea>
                    </div>
                    <button type="submit" class="btn">Enviar Mensaje</button>
                </form>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="footer-content">
            <h3>Verdulería Doña Lupita</h3>
            <p>Frescura Natural para tu Familia</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-whatsapp"></i></a>
            </div>
            <p>© 2023 Verdulería Doña Lupita. Todos los derechos reservados.</p>
        </div>
    </footer>
    
    <script>
        // Formulario de contacto
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('¡Gracias por tu mensaje! Nos pondremos en contacto contigo pronto.');
            this.reset();
        });
        
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
    
    <!-- Font Awesome for icons -->
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</body>
</html>

```

🎨 **Generating images based on descriptions...**

✅ **Images generated successfully! Here's your updated content:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verdulería Doña Lupita - Frutas y Verduras Frescas</title>
    <style>
        :root {
            --verde-primario: #4CAF50;
            --verde-secundario: #81C784;
            --verde-claro: #C8E6C9;
            --naranja: #FF9800;
            --blanco: #FFFFFF;
            --gris-claro: #F5F5F5;
            --texto-oscuro: #212121;
            --texto-claro: #757575;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--gris-claro);
            color: var(--texto-oscuro);
            line-height: 1.6;
        }
        
        header {
            background-color: var(--verde-primario);
            color: var(--blanco);
            padding: 1rem 2rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        .logo span {
            color: var(--naranja);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            color: var(--blanco);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--naranja);
        }
        
        .hero {
            height: 80vh;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/787108e6-1626-4caa-b22c-011249d0c107.png');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--blanco);
            padding: 0 1rem;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.5rem;
            max-width: 800px;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--naranja);
            color: var(--blanco);
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: bold;
            text-decoration: none;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background-color: #F57C00;
            transform: translateY(-3px);
        }
        
        section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--verde-primario);
        }
        
        .about {
            background-color: var(--blanco);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .products {
            background-color: var(--verde-claro);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .product-card {
            background-color: var(--blanco);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .product-image {
            height: 200px;
            overflow: hidden;
        }
        
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-info h3 {
            margin-bottom: 0.5rem;
            color: var(--verde-primario);
        }
        
        .product-price {
            color: var(--naranja);
            font-weight: bold;
            font-size: 1.2rem;
            margin: 0.5rem 0;
        }
        
        .contact {
            background-color: var(--blanco);
        }
        
        .contact-content {
            display: flex;
            gap: 3rem;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-info p {
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }
        
        .contact-info i {
            margin-right: 0.5rem;
            color: var(--verde-primario);
        }
        
        .contact-form {
            flex: 1;
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
            min-height: 150px;
            resize: vertical;
        }
        
        footer {
            background-color: var(--verde-primario);
            color: var(--blanco);
            text-align: center;
            padding: 2rem;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            margin: 1rem 0;
        }
        
        .social-links a {
            color: var(--blanco);
            margin: 0 0.5rem;
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--naranja);
        }
        
        @media (max-width: 768px) {
            .about-content, .contact-content {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">Doña <span>Lupita</span></div>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#productos">Productos</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>
    
    <section class="hero" id="inicio" style="outline: rgb(0, 0, 0) dotted 3px; outline-offset: 1px;">
        <h1>Fruta y Verdura Fresca Directo del Campo</h1>
        <p>En Doña Lupita nos preocupamos por llevar a tu mesa los mejores productos naturales, seleccionados cuidadosamente para garantizar su frescura y sabor.</p>
        <a href="#productos" class="btn">Ver Productos</a>
    </section>
    
    <section class="about" id="nosotros">
        <h2 class="section-title">Nuestra Historia</h2>
        <div class="about-content">
            <div class="about-text">
                <p>Fundada en 1985, Verdulería Doña Lupita comenzó como un pequeño puesto de mercado en el barrio. Gracias a la calidad de nuestros productos y el trato personalizado, hemos crecido hasta convertirnos en un referente de confianza y calidad en la zona.</p>
                <p>Nuestros productos provienen directamente de pequeños productores locales, asegurando frescura y apoyando la economía de nuestra comunidad. Cada día seleccionamos personalmente las mejores frutas y verduras para ofrecerte solo lo mejor.</p>
                <p>Visítanos y descubre la diferencia de comprar en Doña Lupita, donde la tradición y la calidad se unen para ofrecerte lo mejor de la tierra.</p>
            </div>
            <div class="about-image">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/107b6e8d-c1bb-4209-b051-e2ae9260e31a.png" alt="Interior acogedor de la verdulería Doña Lupita, mostrando estantes llenos de frutas y verduras frescas con colores vibrantes y una atmósfera cálida y familiar">
            </div>
        </div>
    </section>
    
    <section class="products" id="productos">
        <h2 class="section-title">Nuestros Productos</h2>
        <div class="products-grid">
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ca867c44-5d66-4473-b17a-ca33e816ec9c.png" alt="Fresas rojas brillantes recién cosechadas con hojas verdes, dispuestas en cestas de mimbre sobre una mesa de madera">
                </div>
                <div class="product-info">
                    <h3>Fresas Frescas</h3>
                    <div class="product-price">$3.99 / lb</div>
                    <p>Fresas dulces y jugosas, cosechadas en su punto óptimo de maduración.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/e9c8ce8e-6a9c-4369-b87f-71738ecef156.png" alt="Tomates maduros de diferentes variedades, rojos, amarillos y verdes, organizados en cajas de madera bajo luz natural">
                </div>
                <div class="product-info">
                    <h3>Tomates Orgánicos</h3>
                    <div class="product-price">$2.49 / lb</div>
                    <p>Tomates cultivados sin pesticidas, con todo su sabor natural.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/8e5d9714-9854-49be-9102-acbf26c5e4ab.png" alt="Variedad de aguacates maduros y verdes cortados por la mitad mostrando su pulpa cremosa sobre una mesa rústica">
                </div>
                <div class="product-info">
                    <h3>Aguacates Hass</h3>
                    <div class="product-price">$2.99 / unidad</div>
                    <p>Aguacates cremosos, perfectos para guacamoles y ensaladas.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/dd7c9a13-39eb-4af8-bda5-9cf3e7cd8541.png" alt="Lechugas frescas de diferentes tipos (romana, iceberg, hoja roja) con gotas de agua brillando bajo la luz">
                </div>
                <div class="product-info">
                    <h3>Lechugas Frescas</h3>
                    <div class="product-price">$1.99 / unidad</div>
                    <p>Lechugas crujientes, recién cosechadas y prelavadas.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/aa220408-6c6f-475d-97d9-a8af97027e5c.png" alt="Manzanas rojas y verdes brillantes con gotas de rocío, apiladas en una canasta de mercería vintage">
                </div>
                <div class="product-info">
                    <h3>Manzanas Selectas</h3>
                    <div class="product-price">$1.49 / lb</div>
                    <p>Manzanas dulces y jugosas, perfectas para comer o cocinar.</p>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/d4299073-687e-4e87-b446-362c60627aa4.png" alt="Zanahorias orgánicas recién cosechadas con tierra aún en sus raíces, mostrando sus hojas verdes sobre una mesa de madera rústica">
                </div>
                <div class="product-info">
                    <h3>Zanahorias Orgánicas</h3>
                    <div class="product-price">$1.29 / lb</div>
                    <p>Zanahorias dulces y crujientes, ricas en nutrientes.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="contact" id="contacto">
        <h2 class="section-title">Contáctanos</h2>
        <div class="contact-content">
            <div class="contact-info">
                <h3>Visítanos</h3>
                <p><i class="fas fa-map-marker-alt"></i> Calle Mercado 123, Barrio Central</p>
                <p><i class="fas fa-phone"></i> +56 2 2345 6789</p>
                <p><i class="fas fa-envelope"></i> hola@verdulerialupita.cl</p>
                <p><i class="fas fa-clock"></i> Lunes a Sábado: 8:00 - 20:00 hrs</p>
                <p><i class="fas fa-clock"></i> Domingo: 9:00 - 15:00 hrs</p>
            </div>
            <div class="contact-form">
                <h3>Envíanos un Mensaje</h3>
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Nombre</label>
                        <input type="text" id="name" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Mensaje</label>
                        <textarea id="message" class="form-control" required></textarea>
                    </div>
                    <button type="submit" class="btn">Enviar Mensaje</button>
                </form>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="footer-content">
            <h3>Verdulería Doña Lupita</h3>
            <p>Frescura Natural para tu Familia</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-whatsapp"></i></a>
            </div>
            <p>© 2023 Verdulería Doña Lupita. Todos los derechos reservados.</p>
        </div>
    </footer>
    
    <script>
        // Formulario de contacto
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('¡Gracias por tu mensaje! Nos pondremos en contacto contigo pronto.');
            this.reset();
        });
        
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
    
    <!-- Font Awesome for icons -->
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</body>
</html>

```










































</html>
