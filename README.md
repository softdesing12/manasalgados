# manasalgados


<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Maná Salgados - Pirapozinho SP | 🔥 Salgadinhos 3D Deliciosos!</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #ff6b6b;
            --secondary: #ff9a56;
            --accent: #00b894;
            --dark: #2d3436;
            --light: #f8f9fa;
            --shadow: 0 25px 50px rgba(0,0,0,0.25);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            overflow-x: hidden;
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
            background-size: 400% 400%;
            animation: gradientShift 15s ease infinite;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header 3D */
        header {
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(20px);
            padding: 40px 30px;
            border-radius: 30px;
            box-shadow: var(--shadow);
            text-align: center;
            margin-bottom: 50px;
            transform: perspective(1000px) rotateX(5deg);
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        header:hover {
            transform: perspective(1000px) rotateX(0deg) translateY(-10px);
        }

        .logo {
            font-size: 3.5em;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 800;
            text-shadow: 0 10px 30px rgba(255,107,107,0.5);
            margin-bottom: 15px;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 20px var(--primary)); }
            to { filter: drop-shadow(0 0 30px var(--secondary)); }
        }

        .subtitle {
            font-size: 1.4em;
            color: var(--dark);
            font-weight: 600;
            margin-bottom: 20px;
        }

        .location {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 20px 30px;
            border-radius: 20px;
            margin: 20px 0;
            font-weight: 700;
            box-shadow: var(--shadow);
            transform: perspective(500px) rotateX(10deg);
        }

        .phone-display {
            font-size: 1.8em;
            background: rgba(255,255,255,0.3);
            padding: 10px 20px;
            border-radius: 50px;
            display: inline-block;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .phone-display:hover {
            background: rgba(255,255,255,0.5);
            transform: scale(1.1);
        }

        /* Botão WhatsApp 3D */
        .whatsapp-btn {
            display: inline-flex;
            align-items: center;
            gap: 15px;
            background: linear-gradient(45deg, #25D366, #128C7E);
            color: white;
            padding: 20px 40px;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.3em;
            font-weight: 700;
            box-shadow: var(--shadow), 0 0 30px rgba(37,211,102,0.5);
            transition: all 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            position: relative;
            overflow: hidden;
        }

        .whatsapp-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: left 0.5s;
        }

        .whatsapp-btn:hover::before {
            left: 100%;
        }

        .whatsapp-btn:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 35px 60px rgba(37,211,102,0.4);
        }

        /* Seções 3D */
        .section-3d {
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(20px);
            padding: 50px 40px;
            border-radius: 30px;
            margin: 50px 0;
            box-shadow: var(--shadow);
            transform: perspective(1000px) rotateX(8deg) rotateY(-5deg);
            transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;
        }

        .section-3d:hover {
            transform: perspective(1000px) rotateX(0deg) rotateY(0deg) translateY(-15px);
        }

        .promo-title {
            font-size: 2.8em;
            background: linear-gradient(45deg, #d63031, #fd79a8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 30px;
            font-weight: 800;
        }

        .promo-price {
            font-size: 4.5em;
            background: linear-gradient(45deg, var(--accent), #00cec9);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 900;
            text-shadow: 0 20px 40px rgba(0,184,148,0.4);
            margin: 30px 0;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        .deadline {
            background: linear-gradient(135deg, #ffeaa7, #fab1a0);
            padding: 20px 30px;
            border-radius: 20px;
            font-weight: 800;
            font-size: 1.3em;
            box-shadow: var(--shadow);
            display: inline-block;
        }

        /* Features 3D */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }

        .feature {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            border-radius: 20px;
            font-weight: 700;
            font-size: 1.1em;
            box-shadow: var(--shadow);
            transform: perspective(500px) rotateX(15deg);
            transition: all 0.4s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .feature::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.3), transparent);
            transform: rotate(45deg);
            transition: all 0.6s;
            opacity: 0;
        }

        .feature:hover::before {
            opacity: 1;
            animation: shine 0.6s ease;
        }

        @keyframes shine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }

        .feature:hover {
            transform: perspective(500px) rotateX(0deg) translateY(-10px) scale(1.05);
        }

        /* Cards 3D */
        .services {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            margin: 60px 0;
        }

        .service-card {
            background: linear-gradient(135deg, rgba(255,255,255,0.95), rgba(255,255,255,0.8));
            backdrop-filter: blur(20px);
            padding: 50px 30px;
            border-radius: 30px;
            box-shadow: var(--shadow);
            text-align: center;
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            transform-style: preserve-3d;
            position: relative;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            border-radius: 30px;
            opacity: 0;
            transition: opacity 0.5s;
            z-index: -1;
        }

        .service-card:hover::before {
            opacity: 0.1;
        }

        .service-card:hover {
            transform: translateY(-20px) rotateX(10deg) rotateY(10deg);
        }

        .service-icon {
            font-size: 4.5em;
            margin-bottom: 25px;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: drop-shadow(0 15px 30px rgba(0,0,0,0.2));
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, var(--dark), #636e72);
            color: white;
            text-align: center;
            padding: 50px 40px;
            border-radius: 30px;
            margin-top: 60px;
            box-shadow: var(--shadow);
        }

        /* Responsivo */
        @media (max-width: 768px) {
            .logo { font-size: 2.5em; }
            .promo-price { font-size: 3.5em; }
            .services { grid-template-columns: 1fr; }
            header, .section-3d { padding: 30px 20px; }
        }

        /* Partículas flutuantes */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .particle {
            position: absolute;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            animation: float 6s infinite linear;
        }

        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100px) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>
    <!-- Partículas de fundo -->
    <div class="particles" id="particles"></div>

    <div class="container">
        <header>
            <h1 class="logo">
                <i class="fas fa-drumstick-bite"></i> Maná Salgados <i class="fas fa-drumstick-bite"></i>
            </h1>
            <p class="subtitle">✨ O sabor que vai conquistar seu coração! ✨</p>
            <div class="location">
                📍 Pirapozinho - SP<br>
                📱 <span class="phone-display">(18) 99125-2835</span>
            </div>
            <a href="https://wa.me/5518991252835?text=🚀%20Olá!%20Cheguei%20pelo%20site%20do%20Maná%20Salgados!%20Quero%20fazer%20pedido!" 
               class="whatsapp-btn" target="_blank">
                <i class="fab fa-whatsapp"></i> Pedir pelo WhatsApp AGORA!
            </a>
        </header>

        <div class="section-3d">
            <h2 class="promo-title">🔥 PROMOÇÃO IMPERDÍVEL! 🔥</h2>
            <div style="font-size: 1.6em; margin: 30px 0; font-weight: 600;">
                🥟 Pastel de queijo ou pizza<br>
                🥤 + Guaraná 200ml
            </div>
            <div class="promo-price">SÓ R$11,00! 💥</div>
            <div class="deadline">
                ⏰ VÁLIDA ATÉ 18/03 - CORRE!
            </div>
            <p style="font-size: 1.3em; margin: 30px 0;">👇 Marca aquele amigo que vai dividir esse lanche com você!</p>
            <a href="https://wa.me/5518991252835?text=🥟%20Quero%20a%20PROMOÇÃO%20PASTEL%20%2B%20GUARANÁ%20R%2411!" 
               class="whatsapp-btn" target="_blank">
                <i class="fas fa-fire"></i> PEGAR PROMOÇÃO JÁ!
            </a>
        </div>

        <div class="section-3d">
            <h2 class="promo-title" style="background: linear-gradient(45deg, #00b894, #00cec9); -webkit-background-clip: text; -webkit-text-fill-color: transparent;">
                🎉 CENTRO DE SALGADO 2,5KG!
            </h2>
            <p style="font-size: 1.4em; margin-bottom: 30px;">Vai fazer festa, reunião ou comemoração? <strong>NÓS RESOLVEMOS!</strong></p>
            
            <div class="promo-price" style="font-size: 3.5em;">APENAS R$120,00! 🎂</div>
            
            <div class="features">
                <div class="feature">
                    <i class="fas fa-birthday-cake"></i><br>Ideal pra aniversários
                </div>
                <div class="feature">
                    <i class="fas fa-users"></i><br>Reuniões em família
                </div>
                <div class="feature">
                    <i class="fas fa-star"></i><br>Praticidade + Sabor
                </div>
            </div>
            
            <a href="https://wa.me/5518991252835?text=🎂%20Quero%20o%20CENTRO%20DE%20SALGADO%202%2C5KG%20R%24120!" 
               class="whatsapp-btn" target="_blank">
                <i class="fas fa-shopping-cart"></i> GARANTIR MEU CENTRO!
            </a>
        </div>

        <div class="services">
            <div class="service-card">
                <div class="service-icon">🥨</div>
                <h3><i class="fas fa-medal"></i> Especializados</h3>
                <p style="font-size: 1.2em; margin: 20px 0;">Salgadinhos frescos e congelados de QUALIDADE!</p>
                <a href="https://wa.me/5518991252835?text=Olá!%20Quero%20ver%20o%20cardápio%20completo!" class="whatsapp-btn" style="font-size: 1em; padding: 15px 30px;">
                    📋 Ver Cardápio
                </a>
            </div>
            <div class="service-card">
                <div class="service-icon">🧊</div>
                <h3><i class="fas fa-snowflake"></i> Congelados</h3>
                <p style="font-size: 1.2em; margin: 20px 0;">Leve pra casa e asse quando quiser! 😍</p>
                <a href="https://wa.me/5518991252835?text=🧊%20Quero%20salgados%20CONGELADOS!" class="whatsapp-btn" style="font-size: 1em; padding: 15px 30px;">
                    🛒 Comprar Agora
                </a>
            </div>
            <div class="service-card">
                <div class="service-icon">🎉</div>
                <h3><i class="fas fa-party-horn"></i> Festas</h3>
                <p style="font-size: 1.2em; margin: 20px 0;">Sua festa perfeita com nossos salgados! ✨</p>
                <a href="https://wa.me/5518991252835
