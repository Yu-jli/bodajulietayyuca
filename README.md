<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Julieta & Yuca - Nuestra Boda</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Montserrat:wght@300;400;500&display=swap');
        
        :root {
            --color-primary: #556b2f;
            --color-secondary: #a8bba3;
            --color-light: #faf9f6;
            --color-dark: #3b4c35;
            --color-accent: #8a9a5b;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            color: var(--color-dark);
            background-color: var(--color-light);
            line-height: 1.6;
        }
        
        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
            font-weight: 600;
            color: var(--color-dark);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.3)), url('https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            height: 100vh;
            color: white;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
        }
        
        .header-content {
            z-index: 1;
            animation: fadeIn 2s;
        }
        
        .names {
            font-size: 5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            color: var(--color-light);
        }
        
        .date {
            font-size: 1.8rem;
            margin-bottom: 2rem;
            font-weight: 300;
            letter-spacing: 3px;
            color: var(--color-secondary);
        }
        
        .countdown {
            background: rgba(59, 76, 53, 0.8);
            padding: 20px;
            border-radius: 10px;
            margin-top: 30px;
            max-width: 600px;
            border: 1px solid var(--color-secondary);
        }
        
        .countdown-container {
            display: flex;
            justify-content: space-around;
        }
        
        .countdown-box {
            text-align: center;
        }
        
        .countdown-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--color-secondary);
        }
        
        .countdown-label {
            font-size: 0.9rem;
            text-transform: uppercase;
            color: var(--color-light);
        }
        
        /* Sections */
        section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        .section-title:after {
            content: "";
            position: absolute;
            width: 80px;
            height: 3px;
            background-color: var(--color-primary);
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        /* Location */
        #location {
            background-color: var(--color-light);
        }
        
        .venue-info {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .venue-name {
            color: var(--color-primary);
            font-size: 2.2rem;
            margin-bottom: 10px;
        }
        
        .venue-address {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: var(--color-dark);
        }
        
        .coordinates {
            background-color: var(--color-secondary);
            display: inline-block;
            padding: 8px 15px;
            border-radius: 20px;
            margin: 10px 0;
            font-size: 0.9rem;
        }
        
        .map-container {
            height: 400px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border: 1px solid var(--color-secondary);
            margin-top: 20px;
        }
        
        /* Directions */
        #directions {
            background-color: var(--color-secondary);
            color: var(--color-dark);
        }
        
        .directions-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }
        
        .direction-card {
            flex: 1;
            min-width: 300px;
            background: var(--color-light);
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 1px solid var(--color-primary);
        }
        
        .direction-icon {
            font-size: 2.5rem;
            color: var(--color-primary);
            margin-bottom: 20px;
        }
        
        /* Dress Code */
        #dress-code {
            background-color: var(--color-light);
        }
        
        .dress-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }
        
        .dress-images {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
            flex-wrap: wrap;
        }
        
        .dress-image {
            width: 200px;
            height: 250px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            border: 2px solid var(--color-primary);
        }
        
        .dress-image:after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, rgba(0, 0, 0, 0.1), rgba(0, 0, 0, 0.3));
        }
        
        .image-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            background: rgba(59, 76, 53, 0.8);
            color: var(--color-light);
            padding: 10px;
            text-align: center;
            z-index: 2;
            font-size: 0.9rem;
        }
        
        /* Accommodation */
        #accommodation {
            background-color: var(--color-secondary);
            color: var(--color-dark);
        }
        
        .accommodation-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .camping-info {
            background: var(--color-light);
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 40px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 1px solid var(--color-primary);
        }
        
        /* Footer */
        footer {
            background-color: var(--color-dark);
            color: var(--color-light);
            text-align: center;
            padding: 40px 0;
        }
        
        .footer-content {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .heart {
            color: var(--color-secondary);
        }
        
        /* Button */
        .btn {
            display: inline-block;
            background: var(--color-primary);
            color: white;
            padding: 12px 25px;
            border-radius: 30px;
            text-decoration: none;
            margin-top: 20px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-family: 'Montserrat', sans-serif;
        }
        
        .btn:hover {
            background: var(--color-dark);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .names {
                font-size: 3.5rem;
            }
            
            .date {
                font-size: 1.5rem;
            }
            
            .countdown-number {
                font-size: 2rem;
            }
            
            .dress-images {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header con cuenta regresiva -->
    <header>
        <div class="header-content">
            <h1 class="names">Julieta & Yuca</h1>
            <p class="date">6 de Diciembre, 2025</p>
            
            <div class="countdown">
                <h3>Faltan</h3>
                <div class="countdown-container">
                    <div class="countdown-box">
                        <div class="countdown-number" id="days">00</div>
                        <div class="countdown-label">Días</div>
                    </div>
                    <div class="countdown-box">
                        <div class="countdown-number" id="hours">00</div>
                        <div class="countdown-label">Horas</div>
                    </div>
                    <div class="countdown-box">
                        <div class="countdown-number" id="minutes">00</div>
                        <div class="countdown-label">Minutos</div>
                    </div>
                    <div class="countdown-box">
                        <div class="countdown-number" id="seconds">00</div>
                        <div class="countdown-label">Segundos</div>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Sección de Ubicación -->
    <section id="location">
        <div class="container">
            <h2 class="section-title">Nuestra Celebración</h2>
            
            <div class="venue-info">
                <h3 class="venue-name">Hacienda Villa Campestre</h3>
                <p class="venue-address">62536 Fraccionamiento Hacienda Villa Campestre, Tlanepantla, Morelos, México</p>
                <div class="coordinates">
                    <i class="fas fa-map-marker-alt"></i> 
                    19.049305830903958, -98.93301055037031
                </div>
                <p>6 de Diciembre, 2025 a las 16:00 horas</p>
                <a href="https://www.google.com/maps/place/19°02'57.5%22N+98°55'58.8%22W/@19.0493058,-98.9330106,17z/data=!3m1!4b1!4m4!3m3!8m2!3d19.0493058!4d-98.9330106?entry=ttu" class="btn" target="_blank">Abrir en Google Maps</a>
            </div>
            
            <div class="map-container">
                <iframe src="https://www.google.com/maps/embed?pb=!1m17!1m12!1m3!1d3780.489212303918!2d-98.9351855242691!3d19.04930578111393!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m2!1m1!2zMTnCsDAyJzU3LjUiTiA5OMKwNTUnNTguOCJX!5e0!3m2!1ses!2smx!4v1699123456789!5m2!1ses!2smx" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </div>
    </section>

    <!-- Sección de Direcciones -->
    <section id="directions">
        <div class="container">
            <h2 class="section-title">Cómo Llegar</h2>
            
            <div class="directions-container">
                <div class="direction-card">
                    <div class="direction-icon">
                        <i class="fas fa-car"></i>
                    </div>
                    <h3>En Coche desde CDMX</h3>
                    <p>Sal de la Ciudad de México rumbo al sur por Viaducto Tlalpan y toma la Autopista México-Cuernavaca (95D).</p>
                    <p>Continúa por la autopista pasando la caseta de Tlalpan y más adelante la de Alpuyeca.</p>
                    <p>Al llegar a Alpuyeca, toma la salida hacia Jojutla / Xoxocotla / Tequesquitengo (no seguir hacia Cuernavaca centro).</p>
                    <p>Sigue recto hasta llegar a Jojutla. Una vez allí, continúa en dirección a Tlatenchi.</p>
                    <p>Cruza Tlatenchi y sigue los señalamientos hacia Tlanepantla (Morelos).</p>
                    <p>Poco antes de llegar al centro de Tlanepantla, sigue las instrucciones de tu GPS para tomar el camino hacia la Hacienda Villa Campestre. El acceso es por una calle de terracería corta que lleva directamente al lugar.</p>
                </div>
                
                <div class="direction-card">
                    <div class="direction-icon">
                        <i class="fas fa-bus"></i>
                    </div>
                    <h3>En Autobús</h3>
                    <p>Empresas como Transportes Estrella Roja de Cuautla (integrada al Grupo Pullman de Morelos / ADO) operan rutas entre CDMX y ciudades en el sur de Morelos como Jojutla o Cuautla, con paradas en tramos cercanos a Tlanepantla.</p>
                    <p>No hay línea de autobús interurbano que llegue directamente a la Hacienda Villa Campestre, pero puedes pedir que te dejen en Jojutla o un punto cercano, y de ahí tomar transporte local hasta Tlanepantla.</p>
                    <p>Avisa con antelación al conductor del interurbano que necesitas bajarte en una parada cercana al transporte local.</p>
                    <p>Entre CDMX y Tlanepantla hay aproximadamente 60–75 km, y el viaje combinado puede tomar entre 2 h y 3 h dependiendo de conexiones.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección de Código de Vestimenta -->
    <section id="dress-code">
        <div class="container">
            <h2 class="section-title">Código de Vestimenta</h2>
            
            <div class="dress-content">
                <p>Nos encantará verlos luciendo radiantes en un día tan especial. Les pedimos con cariño que elijan atuendos formales:</p>
                <p>Los caballeros pueden llevar traje o esmoquin, y las damas, vestido de noche o de cóctel en tonos verde olivo y colores tierra.</p>
                <p>Tomen en cuenta que será invierno y estaremos en una zona boscosa y húmeda, así que les recomendamos llevar un abrigo para cuando caiga la madrugada.</p>
                <p>Y para quienes nos acompañen al desayuno del día siguiente, pueden considerar un segundo atuendo si desean lucir algo diferente.</p>
                
                <div class="dress-images">
                    <div class="dress-image" style="background: url('https://images.unsplash.com/photo-1594633312681-425c7b97ccd1?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80') center/cover;">
                        <div class="image-caption">Vestido Verde Olivo</div>
                    </div>
                    <div class="dress-image" style="background: url('https://images.unsplash.com/photo-1596726895343-5b2f2b1b9292?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80') center/cover;">
                        <div class="image-caption">Traje Formal</div>
                    </div>
                    <div class="dress-image" style="background: url('https://images.unsplash.com/photo-1580545999806-8c35a1c7cacc?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80') center/cover;">
                        <div class="image-caption">Esmóquin</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección de Alojamiento -->
    <section id="accommodation">
        <div class="container">
            <h2 class="section-title">Alojamiento</h2>
            
            <div class="accommodation-content">
                <div class="camping-info">
                    <h3>Zona de Acampada</h3>
                    <p>Sabemos que este lugar está alejado de la ciudad y que algunos vienen desde otros estados o incluso países. Por eso, hemos preparado una zona especial para acampar, con algunas carpas listas para que puedan quedarse a disfrutar toda la velada con nosotros y acompañarnos también en el desayuno del día siguiente.</p>
                    <p>Si lo desean, pueden traer su propia tienda de campaña, así como todo lo necesario para una noche cómoda bajo las estrellas.</p>
                </div>
                
                <p>Si lo tuyo no es la acampada, pero estás pensando en quedarte cerca para disfrutar con tranquilidad del evento, aquí te dejamos algunas opciones de hospedaje recomendadas por su cercanía, comodidad y encanto. Considera apartar con tiempo la fecha de tu reserva.</p>
                
                <a href="#" class="btn">Ver opciones de hospedaje</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <h3>¡Gracias por ser parte de este momento tan importante en nuestras vidas!</h3>
                <p>Con todo nuestro <span class="heart">❤</span>, Julieta & Yuca</p>
            </div>
        </div>
    </footer>

    <script>
        // Cuenta regresiva
        function updateCountdown() {
            const weddingDate = new Date('December 6, 2025 16:00:00').getTime();
            const now = new Date().getTime();
            const distance = weddingDate - now;
            
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            
            document.getElementById("days").innerText = days.toString().padStart(2, '0');
            document.getElementById("hours").innerText = hours.toString().padStart(2, '0');
            document.getElementById("minutes").innerText = minutes.toString().padStart(2, '0');
            document.getElementById("seconds").innerText = seconds.toString().padStart(2, '0');
        }
        
        setInterval(updateCountdown, 1000);
        updateCountdown();
    </script>
</body>
</html>
