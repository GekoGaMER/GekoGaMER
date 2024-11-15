<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Torneos Gaming Pro</title>
    <!-- Estilos de AOS.js -->
    <link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            color: #f4f4f9;
            background: #000; /* Color base para el fondo */
        }
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: -1;
        }
        header {
            background-color: rgba(31, 31, 31, 0.8);
            color: #00d9ff;
            padding: 1rem;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.5);
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 10px;
        }
        .hero {
            text-align: center;
            margin: 2rem 0;
            background-color: rgba(0, 0, 0, 0.5);
            padding: 2rem;
            border-radius: 10px;
            animation: slideInUp 1s ease-out;
        }
        .hero h1 {
            font-size: 3rem;
            color: #ff007f;
            text-shadow: 0 0 10px #ff007f, 0 0 20px #ff007f, 0 0 30px #ff007f;
            animation: pulse 2s infinite;
        }
        .hero p {
            font-size: 1.2rem;
            color: #ccc;
        }
        .btn-primary {
            position: relative;
            overflow: hidden;
            background-color: #ff007f;
            color: white;
            padding: 0.8rem 1.5rem;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            cursor: pointer;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        .btn-primary::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(120deg, transparent, rgba(255, 255, 255, 0.5), transparent);
            transition: all 0.5s ease-in-out;
        }
        .btn-primary:hover::before {
            left: 100%;
        }
        .btn-primary:hover {
            background-color: #e60073;
        }
        .section h2 {
            text-align: center;
            margin-bottom: 1rem;
            color: #00d9ff;
            text-shadow: 0 0 10px #00d9ff, 0 0 20px #00d9ff, 0 0 30px #00d9ff;
        }
        .card {
            background: rgba(31, 31, 31, 0.9);
            border: 1px solid #333;
            border-radius: 10px;
            margin: 1rem;
            padding: 1rem;
            max-width: 300px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.5);
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .card:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 10px rgba(255, 0, 127, 0.5);
        }
        @keyframes pulse {
            0%, 100% {
                text-shadow: 0 0 10px #ff007f, 0 0 20px #ff007f, 0 0 30px #ff007f;
            }
            50% {
                text-shadow: 0 0 15px #ff3399, 0 0 30px #ff3399, 0 0 45px #ff3399;
            }
        }
        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <!-- Contenedor de partículas -->
    <div id="particles-js"></div>
    
    <header>
        <h1>Torneos Gaming Pro</h1>
        <p>¡Compite en retos y torneos para ganar premios en efectivo!</p>
    </header>
    
    <div class="container">
        <div class="hero">
            <h1 data-aos="zoom-in">¡Desafía a otros gamers y gana premios!</h1>
            <p>Participa en retos y torneos de tus videojuegos favoritos.</p>
            <a href="#registro" class="btn-primary" data-aos="fade-up">Registrarse</a>
        </div>

        <!-- Sección de Torneos -->
        <div class="section" data-aos="fade-up">
            <h2>Próximos Torneos</h2>
            <div class="event-list">
                <div class="card" data-aos="zoom-in">
                    <h3>Torneo de League of Legends</h3>
                    <p>Fecha: 20 de Noviembre, 2024</p>
                    <p>Premio: $5000</p>
                </div>
                <div class="card" data-aos="zoom-in" data-aos-delay="200">
                    <h3>Torneo de Fortnite</h3>
                    <p>Fecha: 25 de Noviembre, 2024</p>
                    <p>Premio: $3000</p>
                </div>
                <div class="card" data-aos="zoom-in" data-aos-delay="400">
                    <h3>Torneo de Brawl Stars</h3>
                    <p>Fecha: 10 de Diciembre, 2024</p>
                    <p>Premio: $2000</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/particles.js"></script>
    <script>
        particlesJS("particles-js", {
            "particles": {
                "number": { "value": 100, "density": { "enable": true, "value_area": 800 } },
                "color": { "value": "#ffffff" },
                "shape": { "type": "circle" },
                "opacity": { "value": 0.5, "random": true },
                "size": { "value": 5, "random": true },
                "line_linked": { "enable": true, "distance": 150, "color": "#ffffff", "opacity": 0.4, "width": 1 },
                "move": { "enable": true, "speed": 3 }
            },
            "interactivity": {
                "detect_on": "canvas",
                "events": {
                    "onhover": { "enable": true, "mode": "repulse" },
                    "onclick": { "enable": true, "mode": "push" }
                }
            },
            "retina_detect": true
        });
    </script>
    <script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
    <script>
        AOS.init();
    </script>
</body>
</html>
