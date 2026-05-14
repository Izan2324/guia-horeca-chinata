<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;700;800&display=swap" rel="stylesheet">
    <link href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css" rel="stylesheet">
    <link rel="icon" type="image/x-icon" href="logo1.ico">
    <title>Guia HORECA Chinata | Malpartida de Plasencia</title>
    <style>
        /* ========== ESTILOS CON REDONDEO COMPLETO ========== */
        :root {
            --primary: #2e5c3d;
            --light: #f8f9f5;
            --mid: #5a6b5e;
            --dark: #1f2a24;
            --border: #cbd5e1;
            --radius: 20px;
        }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Segoe UI', system-ui, sans-serif;
            background: var(--light);
            color: var(--dark);
            min-height: 100vh;
            overflow-x: hidden;
        }
        #language-screen {
            position: fixed;
            inset: 0;
            background: linear-gradient(rgba(0, 0, 0, 0.18), rgba(0, 0, 0, 0.18)),
                url('https://turismomonfrague.es/wp-content/uploads/2021/12/Malpartida-de-Plasencia_PGE_ON-6.jpg') center/cover no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10000;
            overflow: hidden;
        }
        .lang-container {
            text-align: center;
            max-width: 460px;
            width: 90%;
            background: rgba(255, 255, 255, 0.96);
            backdrop-filter: blur(16px);
            padding: 2.8rem 2.2rem;
            border-radius: 32px;
            box-shadow: 0 25px 55px rgba(0, 0, 0, 0.4);
            margin: 20px;
        }
        .languages {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 32px 45px;
            justify-items: center;
            margin: 2rem auto 0;
        }
        .lang-option {
            background: none;
            border: none;
            cursor: pointer;
            padding: 0;
            width: 92px;
            height: 92px;
        }
        .lang-option img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.4), inset 0 0 0 5px rgba(255, 255, 255, 0.7);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            object-fit: cover;
        }
        .lang-option:hover img {
            transform: scale(1.22) rotate(10deg);
            box-shadow: 0 18px 35px rgba(0, 0, 0, 0.45);
        }
        .lang-option:nth-child(1) { animation: flagCircle1 1.1s cubic-bezier(0.25, 0.1, 0.25, 1) forwards; }
        .lang-option:nth-child(2) { animation: flagCircle2 1.1s cubic-bezier(0.25, 0.1, 0.25, 1) 0.1s forwards; }
        .lang-option:nth-child(3) { animation: flagCircle3 1.1s cubic-bezier(0.25, 0.1, 0.25, 1) 0.2s forwards; }
        .lang-option:nth-child(4) { animation: flagCircle4 1.1s cubic-bezier(0.25, 0.1, 0.25, 1) 0.3s forwards; }
        @keyframes flagCircle1 {
            0% { transform: translate(-220px, -180px) rotate(-45deg) scale(0.3); opacity: 0; }
            50% { transform: translate(30px, -60px) rotate(25deg) scale(1.15); }
            100% { transform: translate(0, 0) rotate(0deg) scale(1); opacity: 1; }
        }
        @keyframes flagCircle2 {
            0% { transform: translate(220px, -180px) rotate(45deg) scale(0.3); opacity: 0; }
            50% { transform: translate(-30px, -70px) rotate(-30deg) scale(1.12); }
            100% { transform: translate(0, 0) rotate(0deg) scale(1); opacity: 1; }
        }
        @keyframes flagCircle3 {
            0% { transform: translate(-200px, 220px) rotate(40deg) scale(0.3); opacity: 0; }
            50% { transform: translate(40px, 50px) rotate(-25deg) scale(1.1); }
            100% { transform: translate(0, 0) rotate(0deg) scale(1); opacity: 1; }
        }
        @keyframes flagCircle4 {
            0% { transform: translate(210px, 200px) rotate(-35deg) scale(0.3); opacity: 0; }
            50% { transform: translate(-35px, 45px) rotate(30deg) scale(1.15); }
            100% { transform: translate(0, 0) rotate(0deg) scale(1); opacity: 1; }
        }
        .page { display: none; position: relative; width: 100%; min-height: 100vh; }
        .page.active { display: block; }
        .slide-out { animation: slideOutLeft 0.3s ease forwards; }
        .slide-in { animation: slideInRight 0.3s ease forwards; }
        .slide-out-back { animation: slideOutRight 0.3s ease forwards; }
        .slide-in-back { animation: slideInLeft 0.3s ease forwards; }
        @keyframes slideOutLeft { from { transform: translateX(0); opacity: 1; } to { transform: translateX(-30px); opacity: 0; } }
        @keyframes slideInRight { from { transform: translateX(30px); opacity: 0; } to { transform: translateX(0); opacity: 1; } }
        @keyframes slideOutRight { from { transform: translateX(0); opacity: 1; } to { transform: translateX(30px); opacity: 0; } }
        @keyframes slideInLeft { from { transform: translateX(-30px); opacity: 0; } to { transform: translateX(0); opacity: 1; } }
        .ripple {
            position: absolute;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.6);
            transform: scale(0);
            animation: rippleAnim 0.6s linear;
            pointer-events: none;
            z-index: 20;
        }
        @keyframes rippleAnim { to { transform: scale(4); opacity: 0; } }
        header {
            background: white;
            padding: 1rem;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        .logo { font-size: 1.65rem; font-weight: 800; color: var(--primary); }
        .hero {
            background: var(--light);
            text-align: center;
            padding: 2.5rem 1rem 2rem;
        }
        .hero h2 { font-size: 1.8rem; color: var(--primary); margin-bottom: 0.5rem; }
        .cards-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            padding: 0 1rem;
            margin-bottom: 100px;
        }
        .card {
            border-radius: var(--radius);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.12);
            overflow: hidden;
            cursor: pointer;
            min-height: 165px;
            position: relative;
            transition: all 0.3s cubic-bezier(0.2, 0.9, 0.4, 1.1);
        }
        .card:hover {
            transform: translateY(-6px) scale(1.02);
            box-shadow: 0 18px 28px -8px rgba(0, 0, 0, 0.25);
            filter: brightness(1.02);
        }
        .card:hover .card-icon i {
            transform: scale(1.2) rotate(4deg);
            transition: transform 0.25s ease-out;
        }
        .card:hover .card-body h3 {
            text-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
            letter-spacing: 0.3px;
        }
        .card-conoce { background: #8AB0BE; color: white; }
        .card-hacer { background: #7A8C3E; color: white; }
        .card-comer { background: #C2603A; color: white; }
        .card-dormir { background: #e8c45a; color: #1f2a24; }
        .card-icon {
            height: 85px;
            font-size: 2.8rem;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.25);
            transition: background 0.2s;
        }
        .card-icon i { transition: transform 0.2s ease; }
        .card-body { padding: 0.9rem; text-align: center; transition: all 0.2s; }
        .card-body h3 { transition: all 0.2s ease; font-size: 0.95rem; }
        .global-footer {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: white;
            padding: 0.8rem 1rem;
            text-align: center;
            box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
            z-index: 9999;
        }
        .logos-container img { width: 100%; max-width: 350px; height: auto; display: block; margin: 0 auto; }
        .footer-text { font-size: 12px; color: var(--mid); margin-bottom: 4px; }
        .cards-grid { padding-bottom: 100px; }
        #detail-screen {
            background: var(--light);
            overflow-y: auto;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: 2000;
        }
        #detail-content { padding-bottom: 90px; }
        .detail-header {
            padding: 1rem 1.2rem;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            gap: 1rem;
            position: sticky;
            top: 0;
            z-index: 10;
            border-radius: 0 0 var(--radius) var(--radius);
        }
        .back-btn {
            display: flex;
            align-items: center;
            gap: 8px;
            background: rgba(255, 255, 255, 0.22);
            border: 2px solid rgba(255, 255, 255, 0.7);
            border-radius: 40px;
            padding: 6px 14px;
            font-size: 14px;
            font-weight: 700;
            color: white;
            cursor: pointer;
            transition: background 0.15s, transform 0.15s;
            font-family: inherit;
        }
        .back-btn i { font-size: 1.2rem; }
        .back-btn:hover { background: rgba(255, 255, 255, 0.38); transform: translateX(-2px); }
        .back-btn:active { transform: scale(0.94); }
        #detail-title { color: white; font-size: 1.2rem; margin: 0; font-weight: 700; }
        .screen { padding-bottom: 2rem; }
        .divider { height: 1px; background: rgba(0, 0, 0, 0.1); margin: 12px 0; }
        .scroll-body { padding: 0 1rem 0; }
        .section { padding: 14px 16px; }
        .info-card {
            background: #fff;
            border-radius: var(--radius);
            border: 1px solid var(--border);
            padding: 14px;
            margin-bottom: 10px;
            animation: fadeUp .35s both;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.04);
        }
        .info-card h3 {
            font-size: 14px;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 6px;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        .info-card p { font-size: 13px; color: var(--mid); line-height: 1.6; }
        .image-card {
            position: relative;
            background-size: cover;
            background-position: center;
            border-radius: var(--radius);
            padding: 14px;
            margin-bottom: 10px;
            overflow: hidden;
            animation: fadeUp .35s both;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            color: white;
            min-height: 110px;
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
        }
        .image-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(to bottom, rgba(30, 30, 35, 0.85), rgba(0, 0, 0, 0) 70%);
            border-radius: inherit;
            pointer-events: none;
            z-index: 1;
        }
        .image-card h3, .image-card p, .badge-group {
            position: relative;
            z-index: 2;
            text-shadow: 0 1px 3px rgba(0, 0, 0, 0.5);
        }
        .image-card h3 {
            font-size: 14px;
            font-weight: 800;
            margin-bottom: 6px;
            display: flex;
            align-items: center;
            gap: 6px;
            color: white;
        }
        .image-card p {
            font-size: 13px;
            line-height: 1.5;
            color: #f0f0f0;
            margin-bottom: 8px;
        }
        .badge-group {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 6px;
        }
        .badge {
            border-radius: 40px;
            padding: 4px 10px;
            font-size: 11px;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            color: white;
            border: none;
            backdrop-filter: blur(2px);
        }
        .badge-parking { background-color: #1E3A8A; }
        .badge-wifi { background-color: #4B5563; }
        .badge-pool { background-color: #14B8A6; }
        .badge i { font-size: 12px; color: inherit; }
        .desc-header {
            display: flex;
            align-items: center;
            gap: 16px;
            padding: 16px 20px;
            background: #ffffff;
            border-radius: var(--radius);
            margin: 10px 16px;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
        }
        .desc-header i { font-size: 40px; flex-shrink: 0; }
        .desc-header p { margin: 0; font-size: 14px; line-height: 1.4; color: var(--mid); }
        .section-title {
            font-weight: 700;
            font-size: 12px;
            color: var(--mid);
            letter-spacing: .06em;
            text-transform: uppercase;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        .info-card.hero {
            position: relative;
            padding: 0;
            overflow: hidden;
            min-height: 160px;
            border-radius: var(--radius);
            background: linear-gradient(rgba(0, 0, 0, 0.35), rgba(0, 0, 0, 0.75)),
                url('https://turismomonfrague.es/wp-content/uploads/2021/12/Malpartida-de-Plasencia_PGE_ON-2-e1643890328358.jpg') center/cover no-repeat;
            color: white;
        }
        .hero-content { position: relative; z-index: 2; padding: 28px 20px 32px; display: flex; flex-direction: column; justify-content: flex-end; }
        .info-card.hero h3 { color: white; margin-bottom: 12px; text-shadow: 0 2px 8px rgba(0, 0, 0, 0.8); font-size: 15.5px; }
        .info-card.hero p { color: #f0f0f0; text-shadow: 0 1px 3px rgba(0, 0, 0, 0.7); line-height: 1.55; font-size: 16px; font-weight: 400; }

        /* ESTILOS PARA EL ACORDEÓN DE ACTIVIDADES */
        .actividad-collapsible {
            margin-bottom: 12px;
            border-radius: var(--radius);
            overflow: hidden;
            background: #7A8C3E;
            transition: all 0.2s ease;
        }
        .actividad-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 16px;
            padding: 16px 18px;
            cursor: pointer;
            color: white;
            font-weight: 800;
            font-size: 1.05rem;
            background: #7A8C3E;
            transition: background 0.2s;
            border-radius: var(--radius);
        }
        .actividad-header:hover {
            background: #6a7c35;
        }
        .actividad-header-left {
            display: flex;
            align-items: center;
            gap: 16px;
        }
        .actividad-header-left i {
            font-size: 28px;
        }
        .actividad-toggle-icon {
            font-size: 24px;
            transition: transform 0.3s ease;
        }
        .actividad-collapsible.open .actividad-toggle-icon {
            transform: rotate(90deg);
        }
        .actividad-details {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s cubic-bezier(0.33, 1, 0.68, 1);
            background: white;
            color: var(--dark);
            border-radius: 0 0 var(--radius) var(--radius);
        }
        .actividad-collapsible.open .actividad-details {
            max-height: 800px;
        }
        .actividad-content {
            padding: 18px;
            font-size: 14px;
            line-height: 1.55;
            border-top: 1px solid #e0e5d8;
        }
        .actividad-content p {
            margin: 12px 0;
        }
        .actividad-content ul, .actividad-content ol {
            margin: 8px 0 12px 20px;
        }
        .actividad-content li {
            margin: 4px 0;
        }
        .actividad-content strong {
            color: #2e5c3d;
        }

        /* ESTILOS PARA FILTRO DORMIR */
        .filter-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 12px;
            margin: 0 0 20px 0;
            background: white;
            padding: 12px 16px;
            border-radius: var(--radius);
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
        }
        .filter-select {
            background: var(--light);
            border: 1px solid #ddd;
            padding: 8px 18px;
            border-radius: 40px;
            font-size: 13px;
            font-weight: 600;
            color: var(--dark);
            cursor: pointer;
            font-family: inherit;
            outline: none;
            transition: all 0.2s;
        }
        .filter-select:focus {
            border-color: var(--primary);
        }
        @media (max-width: 500px) {
            .filter-bar {
                flex-direction: column;
                align-items: stretch;
            }
            .filter-select {
                width: 100%;
                text-align: center;
            }
        }

        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: none; }
        }
        .main-entrance { animation: appEntrance 0.8s cubic-bezier(0.25, 0.1, 0.25, 1) forwards; }
        .cards-grid { animation: appEntrance 0.9s cubic-bezier(0.25, 0.1, 0.25, 1) 0.1s forwards; opacity: 0; }
        @keyframes appEntrance {
            0% { opacity: 0; transform: translateY(30px) scale(0.95); }
            100% { opacity: 1; transform: translateY(0) scale(1); }
        }
    </style>
</head>

<body>

    <div id="language-screen">
        <div class="lang-container">
            <img src="https://i.postimg.cc/KcdTXQvs/logo1.png" alt="Logo HORECA Chinata" style="width: 85%; max-width: 320px; height: auto; border-radius: 16px; box-shadow: 0 10px 30px rgba(0,0,0,0.15); margin-bottom: 1.5rem;">
            <p style="color: #1f2a24; font-weight: 700; font-size: 1.1rem; margin-bottom: 2rem;">Selecciona tu idioma / Select your language</p>
            <div class="languages">
                <button class="lang-option" onclick="changeLanguage('es', event)"><img src="https://flagcdn.com/es.svg" width="70" alt="Español"></button>
                <button class="lang-option" onclick="changeLanguage('en', event)"><img src="https://flagcdn.com/gb.svg" width="70" alt="English"></button>
                <button class="lang-option" onclick="changeLanguage('fr', event)"><img src="https://flagcdn.com/fr.svg" width="70" alt="Français"></button>
                <button class="lang-option" onclick="changeLanguage('pt', event)"><img src="https://flagcdn.com/pt.svg" width="70" alt="Português"></button>
            </div>
        </div>
    </div>

    <div id="main-app" class="page">
        <header><h1 id="app-title" class="logo">Guía HORECA Chinata</h1></header>
        <section class="hero">
            <h2 id="hero-title">Descubre Malpartida de Plasencia</h2>
            <p id="hero-subtitle">Tu guía completa de gastronomía, alojamiento y experiencias</p>
        </section>
        <div class="cards-grid">
            <div class="card card-conoce" onclick="openDetail(0, event)"><div class="card-icon"><i class="ti ti-map-pin" style="font-size: 3.2rem;"></i></div><div class="card-body"><h3 id="card1-title">Conoce Malpartida de Plasencia</h3></div></div>
            <div class="card card-hacer" onclick="openDetail(1, event)"><div class="card-icon"><i class="ti ti-compass" style="font-size: 3.2rem;"></i></div><div class="card-body"><h3 id="card2-title">¿Qué hacer?</h3></div></div>
            <div class="card card-comer" onclick="openDetail(2, event)"><div class="card-icon"><i class="ti ti-chef-hat" style="font-size: 3.2rem;"></i></div><div class="card-body"><h3 id="card3-title">¿Dónde comer?</h3></div></div>
            <div class="card card-dormir" onclick="openDetail(3, event)"><div class="card-icon"><i class="ti ti-bed" style="font-size: 3.2rem; color: #ffffff"></i></div><div class="card-body"><h3 id="card4-title" style="color: #ffffff">¿Dónde dormir?</h3></div></div>
        </div>
    </div>

    <div id="detail-screen" class="page">
        <div class="detail-header" id="detail-header">
            <button class="back-btn" id="back-btn" onclick="goHome(event)"><i class="ti ti-arrow-left"></i> <span id="back-text">Volver</span></button>
            <h2 id="detail-title"></h2>
        </div>
        <div class="main-content" id="detail-content"></div>
    </div>

    <div class="global-footer" id="global-footer">
        <div class="footer-text" id="footer-support">Con el apoyo de</div>
        <div class="logos-container"><img src="https://i.postimg.cc/HnVsVGYt/logos-(1).png" alt="Colaboradores"></div>
    </div>

    <script>
        // ==================== TRADUCCIONES COMPLETAS CON ACTIVIDADES, RESTAURANTES, ALOJAMIENTOS Y BADGES ====================
        const translations = {
            es: {
                back: "Volver",
                appTitle: "Guía HORECA Chinata",
                heroTitle: "Descubre Malpartida de Plasencia",
                heroSub: "Tu guía completa de gastronomía, alojamiento y experiencias",
                cards: ["Conoce Malpartida de Plasencia", "¿Qué hacer?", "¿Dónde comer?", "¿Dónde dormir?"],
                footer: "Con el apoyo de",
                who: "¿Quiénes somos?",
                whoDesc: "Municipio de la comarca de Monfragüe, en la provincia de Cáceres (Extremadura), enclavado entre dehesas centenarias y olivares. Con unos 4.600 habitantes, combina tradición agraria y creciente turismo rural.",
                historyTitle: "Historia",
                historyDesc: "El origen 'chinatos': defendieron el pueblo lanzando piedras (chinarros) ante los placentinos.",
                natureTitle: "Entorno natural",
                natureDesc: `<strong>🌿 Centro de Visitantes Norte del Parque Nacional de Monfragüe</strong><br>A 6 km del casco urbano, junto al camping y la estación de tren. Edificio moderno de 2.000 m² con sala expositiva, audiovisuales, interactivos y maquetas.<br><br>
                            <strong>🚂 Poblado de Estación empalme-Monfragüe</strong><br>Antigua estación de trenes con interesante arquitectura; llegó a tener cerca de 1000 habitantes.<br><br>
                            <strong>🌳 Dehesa Boyar el Robledo</strong><br>Espacio natural de robles y berrocales. Rutas para senderistas y aventureros. Destacan restos arqueológicos: Tumba de la Princesa, tumbas antropomorfas, menhires, cerro de los Castillejos.<br><br>
                            <strong>💧 Entorno de San Cristóbal - Pantano</strong><br>A 4 km del pueblo (Horco del Espino). Paraje de pinos con merendero e instalaciones. Embalse con embarcadero para piragüismo y kayak. En julio se celebra la fiesta de San Cristóbal.`,
                interestTitle: "Datos de interés",
                interestDesc: "Altitud 467m | Provincia Cáceres | Fiesta: Abril (La Luz)",
                visitTitle: "Qué visitar",
                churchDesc: "<strong>Iglesia Parroquial de San Juan Bautista</strong> – Principal monumento. Templo del siglo XVI (gótico decadente, renacentista y barroco). BIC desde octubre 2018.",
                museumDesc: "<strong>Museo Aire Libre Albañilería</strong> – Réplicas a tamaño real de los trabajos de los Concursos de Albañilería. Folleto con imágenes y callejero disponible.",
                hermitagesDesc: "<strong>Ermitas</strong> – San Blas, San Gregorio, Virgen de la Luz (Patrona) y San Cristóbal. Edificios actuales del siglo XX.",
                quehacerPlaceholder: "Descubre las mejores actividades al aire libre y patrimonio cultural en Malpartida de Plasencia. Haz clic en cada apartado para ver la información completa.",
                actividades: [
                    { nombre: "Avistamiento de Aves (Birding)", icono: "ti ti-feather", contenido: `<p>Al estar pegado a Monfragüe, es uno de los mejores lugares de Europa para ver rapaces.</p><p><strong>🔭 Qué ver:</strong> Buitre leonado, buitre negro, águila imperial ibérica, cigüeña negra y alimoche.</p><p><strong>🏢 Empresas locales:</strong> Puedes contratar rutas especializadas con <strong>Monfragüe Treasures</strong> (ubicada en el mismo pueblo) que ofrecen guías expertos y material óptico.</p><p><strong>📍 Puntos cercanos:</strong> El Salto del Gitano y la Portilla del Tiétar son los miradores más famosos a pocos minutos en coche.</p>` },
                    { nombre: "Patrimonio Cultural", icono: "ti ti-building", contenido: `<p>El pueblo cuenta con un rico legado histórico:</p><ul><li><strong>Iglesia de San Juan Bautista:</strong> Monumento del siglo XVI declarado Bien de Interés Cultural. Destaca por su coro y su arquitectura que mezcla gótico tardío y renacimiento.</li><li><strong>Cerro de los Castillejos:</strong> Un asentamiento vetón (pueblo prerromano) donde puedes ver restos de murallas, menhires y la curiosa "Tumba de la Princesa" (posible altar de sacrificios).</li><li><strong>Ermitas:</strong> Destacan las de San Blas, San Gregorio y la Virgen de la Luz.</li></ul>` },
                    { nombre: "Senderismo y Centro de Visitantes", icono: "ti ti-mountain", contenido: `<p><strong>🏛️ Centro de Visitantes Norte "Jesús Garzón":</strong> Situado en la carretera EX-208 (km 9), es fundamental visitarlo antes de entrar al Parque. Ofrece exposiciones sobre la flora y fauna y tiene un sendero interpretativo de 1 km ideal para familias. <strong>Antes de salir, pásate por el Centro de Visitantes donde te darán el folleto oficial con los mapas actualizados y te informarán sobre posibles cortes de senderos por época de cría de aves.</strong></p><p><strong>🗺️ Rutas destacadas:</strong></p><ul><li><strong>Cerro de los Castillejos:</strong> 5,8 km (ida y vuelta), dificultad baja. Visita al yacimiento vetón, menhires y "Tumba de la Princesa". Comienza en el km 1,8 de la carretera CC-18.1.</li><li><strong>Mirador de Valdeherrero:</strong> Dos opciones (5,7 km o 10 km), dificultad baja. Vistas panorámicas de La Vera.</li><li><strong>Ruta de "El Robledo" (PR-CC 69):</strong> Circular de unos 17 km por robledal y dehesa.</li><li><strong>Pico de San Gregorio:</strong> 5 km (ida y vuelta), vistas espectaculares de la llanura placentina.</li><li><strong>Ruta Azul (Parque Nacional):</strong> Malpartida - Villarreal de San Carlos, 4-5 horas. Conecta el pueblo con el centro del Parque.</li><li><strong>Vía Verde de Monfragüe:</strong> 17,5 km (Camping Monfragüe - Haza Concepción). <em>(Actualmente obras hasta mediados 2026, consultar estado)</em></li><li><strong>Rutas del Parque (desde Centro Visitantes):</strong> Ruta Roja (Castillo, 16 km), Ruta Verde (Cerro Gimio, 7,9 km), Ruta Amarilla (La Tajadilla, 8,9 km).</li></ul>` },
                    { nombre: "Rutas en Bicicleta", icono: "ti ti-bike", contenido: `<p><strong>🚵 Entorno de la Dehesa:</strong> Malpartida está rodeada de extensas dehesas con caminos públicos ideales para el cicloturismo de montaña (BTT) sin grandes desniveles.</p><p><strong>🌍 Rutas de larga distancia:</strong> Forma parte de redes que conectan con Plasencia y otras localidades de la Reserva de la Biosfera de Monfragüe.</p>` },
                    { nombre: "Piragüismo y Kayak", icono: "ti ti-sailboat", contenido: `<p>Las actividades acuáticas se realizan principalmente en los ríos y embalses cercanos:</p><p><strong>🌊 Río Tiétar:</strong> Se organizan descensos en piragua, especialmente en zonas de aguas tranquilas que permiten disfrutar del paisaje de Monfragüe desde el agua (fuera de las zonas de máxima protección).</p><p><strong>🏢 Empresas:</strong> Destino Activo (Monfragüe Vivo) organiza paseos en kayak y piragua por el entorno, generalmente operativos de junio a octubre.</p>` }
                ],
                comerDesc: "Disfruta de la gastronomía local en los mejores restaurantes y bares de Malpartida de Plasencia. Cocina tradicional extremeña, tapas y productos de la dehesa.",
                dormirDesc: "Encuentra tu alojamiento ideal en Malpartida de Plasencia y alrededores. Variedad de casas rurales, apartamentos y hoteles cerca del Parque Natural de Monfragüe.",
                comerSectionTitle: "Restaurantes y bares en Malpartida y alrededores",
                dormirSectionTitle: "Alojamientos en Malpartida y alrededores",
                filterOptions: { all: "Todos", parking: "Parking", wifi: "WiFi", pool: "Piscina" },
                badgeLabels: { parking: "Parking", wifi: "WiFi", pool: "Piscina" },
                restaurantes: [
                    { nombre: "Casa El Moreno", desc: "Bar con buena comida casera y ambiente local.", img: "https://images.unsplash.com/photo-1555939594-58d7cb561ad1?w=400&h=250&fit=crop" },
                    { nombre: "Café-Bar Burguer Orix", desc: "Hamburguesas y comida rápida. Ideal para un bocado rápido.", img: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?w=400&h=250&fit=crop" },
                    { nombre: "El Habana", desc: "Café-bar con tapas y raciones. Ambiente animado.", img: "https://images.unsplash.com/photo-1590846406792-0adc7f938f1d?w=400&h=250&fit=crop" },
                    { nombre: "El Antares", desc: "Café-bar con tapas y buen ambiente. Música y terraza.", img: "https://images.unsplash.com/photo-1506354666786-959d6d497f1a?w=400&h=250&fit=crop" },
                    { nombre: "El Oasis", desc: "Pub y restaurante. Cocina variada y bebidas.", img: "https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?w=400&h=250&fit=crop" },
                    { nombre: "Las Habazas", desc: "Restaurante de calidad junto al Parque Nacional de Monfragüe. Destaca por carnes y productos de la dehesa.", img: "https://images.unsplash.com/photo-1544025162-d76694265947?w=400&h=250&fit=crop" },
                    { nombre: "Camping de Monfragüe", desc: "Restaurante del camping con opción de menús y comida casera. Perfecto para familias.", img: "https://images.unsplash.com/photo-1504280390367-361c6d9f38f4?w=400&h=250&fit=crop" },
                    { nombre: "Bar-Restaurante La Piscina", desc: "Restaurante con terraza y piscina. Ideal para el verano.", img: "https://images.unsplash.com/photo-1537047902294-62a40c20a6ae?w=400&h=250&fit=crop" },
                    { nombre: "Churrería 3 Chocolates", desc: "Churros, desayunos y comida para llevar. Especialidad en chocolate.", img: "https://images.unsplash.com/photo-1584370848010-d7fe6bc767ec?w=400&h=250&fit=crop" }
                ],
                alojamientos: [
                    { nombre: "Apartamentos Rurales El Trillo", desc: "Acogedores apartamentos rurales con todas las comodidades.", img: "https://images.unsplash.com/photo-1560185007-5f0bb1866cab?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Posada de Monfragüe", desc: "Encantadora posada tradicional cerca del Parque Nacional.", img: "https://images.unsplash.com/photo-1571003123894-1f0594d2b5d9?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Hotel Puerta de Monfragüe", desc: "Hotel moderno con excelentes servicios.", img: "https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?w=400&h=250&fit=crop", parking: true, wifi: true, pool: true },
                    { nombre: "Casa Rural 2 habitaciones", desc: "Casa completa con dos dormitorios, chimenea y barbacoa.", img: "https://images.unsplash.com/photo-1542718610-a1d656d1884c?w=400&h=250&fit=crop", parking: true, wifi: false, pool: false },
                    { nombre: "Casa Rural del Corral y Apartamentos", desc: "Amplio complejo rural con jardín.", img: "https://images.unsplash.com/photo-1583847268964-b28dc8f51f92?w=400&h=250&fit=crop", parking: true, wifi: true, pool: true },
                    { nombre: "Casa Rural Fuente Vieja", desc: "Antigua casa rehabilitada con encanto rústico.", img: "https://images.unsplash.com/photo-1570129477492-45c003edd2be?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Casa Rural La Tomasa", desc: "Pequeña casa rural muy acogedora.", img: "https://images.unsplash.com/photo-1560185127-6ed189bf02f4?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Apartamentos Eras Centro", desc: "Apartamentos céntricos ideales para conocer el pueblo.", img: "https://images.unsplash.com/photo-1522708323590-d24dbb6b0267?w=400&h=250&fit=crop", parking: false, wifi: true, pool: false }
                ]
            },
            en: {
                back: "Back",
                appTitle: "HORECA Chinata Guide",
                heroTitle: "Discover Malpartida de Plasencia",
                heroSub: "Your complete guide",
                cards: ["Discover Malpartida", "What to do?", "Where to eat?", "Where to sleep?"],
                footer: "Supported by",
                who: "About us",
                whoDesc: "Municipality in the Monfragüe region, province of Cáceres (Extremadura), between centuries-old pastures and olive groves. With about 4,600 inhabitants, it combines agricultural tradition and growing rural tourism.",
                historyTitle: "History",
                historyDesc: "The origin of the nickname 'chinatos': they defended the town by throwing stones (chinarros) against the people of Plasencia.",
                natureTitle: "Natural surroundings",
                natureDesc: `<strong>🌿 Monfragüe National Park Northern Visitor Centre</strong><br>6 km from the town centre, next to the campsite and train station. Modern 2,000 m² building with exhibition hall, audiovisual rooms, interactive displays and models.<br><br>
                             <strong>🚂 Estación Empalme-Monfragüe Village</strong><br>Old railway station with interesting architecture; it once had nearly 1,000 inhabitants.<br><br>
                             <strong>🌳 Dehesa Boyar el Robledo</strong><br>Natural area of oak trees and rocky outcrops. Hiking routes for walkers and adventurers. Notable archaeological remains: Princess's Tomb, anthropomorphic tombs, menhirs, Cerro de los Castillejos.<br><br>
                             <strong>💧 San Cristóbal Area - Reservoir</strong><br>4 km from the village (Horco del Espino). Pine grove with picnic area and facilities. Reservoir with a pier for canoeing and kayaking. The festival of San Cristóbal is celebrated in July.`,
                interestTitle: "Interesting facts",
                interestDesc: "Altitude 467m | Province of Cáceres | Festival: April (La Luz)",
                visitTitle: "What to visit",
                churchDesc: "<strong>St. John the Baptist Parish Church</strong> – Main monument. 16th-century temple (Gothic, Renaissance and Baroque). BIC since 2018.",
                museumDesc: "<strong>Open-Air Masonry Museum</strong> – Full-scale replicas of the Masonry Competition works. Brochure and map available.",
                hermitagesDesc: "<strong>Hermitages</strong> – San Blas, San Gregorio, Virgen de la Luz (Patron Saint) and San Cristóbal. 20th-century buildings.",
                quehacerPlaceholder: "Discover the best outdoor activities and cultural heritage in Malpartida de Plasencia. Click on each section to see full details.",
                actividades: [
                    { nombre: "Birdwatching", icono: "ti ti-feather", contenido: `<p>Adjacent to Monfragüe, it's one of the best places in Europe to see birds of prey.</p><p><strong>🔭 What to see:</strong> Griffon vulture, cinereous vulture, Spanish imperial eagle, black stork and Egyptian vulture.</p><p><strong>🏢 Local companies:</strong> Hire specialized routes with <strong>Monfragüe Treasures</strong> (located in the village) offering expert guides and optical equipment.</p><p><strong>📍 Nearby spots:</strong> El Salto del Gitano and Portilla del Tiétar are the most famous viewpoints just a few minutes away by car.</p>` },
                    { nombre: "Cultural Heritage", icono: "ti ti-building", contenido: `<p>The village has a rich historical legacy:</p><ul><li><strong>St. John the Baptist Church:</strong> 16th-century monument declared Asset of Cultural Interest. Notable for its choir and architecture mixing late Gothic and Renaissance.</li><li><strong>Cerro de los Castillejos:</strong> A Vetton settlement (pre-Roman) where you can see wall remains, menhirs and the curious "Princess's Tomb" (possible sacrifice altar).</li><li><strong>Hermitages:</strong> San Blas, San Gregorio and Virgen de la Luz stand out.</li></ul>` },
                    { nombre: "Hiking & Visitor Centre", icono: "ti ti-mountain", contenido: `<p><strong>🏛️ Northern Visitor Centre "Jesús Garzón":</strong> Located on EX-208 road (km 9), essential to visit before entering the Park. It offers exhibitions on flora and fauna and has a 1-km interpretive trail ideal for families. <strong>Before heading out, stop by the Visitor Centre to get the official brochure with updated maps and information about possible trail closures due to bird breeding season.</strong></p><p><strong>🗺️ Featured trails:</strong></p><ul><li><strong>Cerro de los Castillejos:</strong> 5.8 km (round trip), low difficulty. Visit the Vetton settlement, menhirs and "Princess's Tomb". Starts at km 1.8 of CC-18.1 road.</li><li><strong>Valdeherrero Viewpoint:</strong> Two options (5.7 km or 10 km), low difficulty. Panoramic views of La Vera.</li><li><strong>"El Robledo" Trail (PR-CC 69):</strong> Circular about 17 km through oak forest and dehesa.</li><li><strong>San Gregorio Peak:</strong> 5 km (round trip), spectacular views of the Plasencia plain.</li><li><strong>Blue Route (National Park):</strong> Malpartida - Villarreal de San Carlos, 4-5 hours. Connects the village with the Park's hub.</li><li><strong>Monfragüe Greenway:</strong> 17.5 km (Camping Monfragüe - Haza Concepción). <em>(Currently under construction until mid-2026, check status)</em></li><li><strong>Park trails (from Visitor Centre):</strong> Red Route (Castle, 16 km), Green Route (Cerro Gimio, 7.9 km), Yellow Route (La Tajadilla, 8.9 km).</li></ul>` },
                    { nombre: "Cycling Routes", icono: "ti ti-bike", contenido: `<p><strong>🚵 Dehesa surroundings:</strong> Malpartida is surrounded by extensive dehesas with public paths ideal for mountain biking (MTB) without steep slopes.</p><p><strong>🌍 Long-distance routes:</strong> Part of networks connecting with Plasencia and other towns in the Monfragüe Biosphere Reserve.</p>` },
                    { nombre: "Canoeing & Kayaking", icono: "ti ti-sailboat", contenido: `<p>Water activities are mainly carried out in nearby rivers and reservoirs:</p><p><strong>🌊 Tiétar River:</strong> Canoe descents are organized, especially in calm water areas allowing you to enjoy Monfragüe's landscape from the water (outside maximum protection zones).</p><p><strong>🏢 Companies:</strong> Destino Activo (Monfragüe Vivo) organizes kayak and canoe trips in the area, generally operating from June to October.</p>` }
                ],
                comerDesc: "Enjoy local gastronomy at the best restaurants and bars in Malpartida de Plasencia. Traditional Extremaduran cuisine, tapas and dehesa products.",
                dormirDesc: "Find your ideal accommodation in Malpartida de Plasencia and surroundings. Variety of rural houses, apartments and hotels near the Monfragüe Natural Park.",
                comerSectionTitle: "Restaurants and bars in Malpartida and surroundings",
                dormirSectionTitle: "Accommodation in Malpartida and surroundings",
                filterOptions: { all: "All", parking: "Parking", wifi: "WiFi", pool: "Pool" },
                badgeLabels: { parking: "Parking", wifi: "WiFi", pool: "Pool" },
                restaurantes: [
                    { nombre: "Casa El Moreno", desc: "Bar with good homemade food and local atmosphere.", img: "https://images.unsplash.com/photo-1555939594-58d7cb561ad1?w=400&h=250&fit=crop" },
                    { nombre: "Burguer Orix Café-Bar", desc: "Burgers and fast food. Ideal for a quick bite.", img: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?w=400&h=250&fit=crop" },
                    { nombre: "El Habana", desc: "Café-bar with tapas and portions. Lively atmosphere.", img: "https://images.unsplash.com/photo-1590846406792-0adc7f938f1d?w=400&h=250&fit=crop" },
                    { nombre: "El Antares", desc: "Café-bar with tapas and good atmosphere. Music and terrace.", img: "https://images.unsplash.com/photo-1506354666786-959d6d497f1a?w=400&h=250&fit=crop" },
                    { nombre: "El Oasis", desc: "Pub and restaurant. Varied cuisine and drinks.", img: "https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?w=400&h=250&fit=crop" },
                    { nombre: "Las Habazas", desc: "Quality restaurant next to Monfragüe National Park. Known for meats and dehesa products.", img: "https://images.unsplash.com/photo-1544025162-d76694265947?w=400&h=250&fit=crop" },
                    { nombre: "Monfragüe Camping", desc: "Camping restaurant with menu options and homemade food. Perfect for families.", img: "https://images.unsplash.com/photo-1504280390367-361c6d9f38f4?w=400&h=250&fit=crop" },
                    { nombre: "La Piscina Bar-Restaurant", desc: "Restaurant with terrace and swimming pool. Ideal for summer.", img: "https://images.unsplash.com/photo-1537047902294-62a40c20a6ae?w=400&h=250&fit=crop" },
                    { nombre: "3 Chocolates Churrería", desc: "Churros, breakfasts and takeaway food. Chocolate specialty.", img: "https://images.unsplash.com/photo-1584370848010-d7fe6bc767ec?w=400&h=250&fit=crop" }
                ],
                alojamientos: [
                    { nombre: "El Trillo Rural Apartments", desc: "Cozy rural apartments with all amenities.", img: "https://images.unsplash.com/photo-1560185007-5f0bb1866cab?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Monfragüe Inn", desc: "Charming traditional inn near the National Park.", img: "https://images.unsplash.com/photo-1571003123894-1f0594d2b5d9?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Puerta de Monfragüe Hotel", desc: "Modern hotel with excellent services.", img: "https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?w=400&h=250&fit=crop", parking: true, wifi: true, pool: true },
                    { nombre: "2-bedroom Rural House", desc: "Complete house with two bedrooms, fireplace and barbecue.", img: "https://images.unsplash.com/photo-1542718610-a1d656d1884c?w=400&h=250&fit=crop", parking: true, wifi: false, pool: false },
                    { nombre: "Del Corral Rural House & Apartments", desc: "Spacious rural complex with garden.", img: "https://images.unsplash.com/photo-1583847268964-b28dc8f51f92?w=400&h=250&fit=crop", parking: true, wifi: true, pool: true },
                    { nombre: "Fuente Vieja Rural House", desc: "Renovated old house with rustic charm.", img: "https://images.unsplash.com/photo-1570129477492-45c003edd2be?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "La Tomasa Rural House", desc: "Very cozy small rural house.", img: "https://images.unsplash.com/photo-1560185127-6ed189bf02f4?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Eras Centro Apartments", desc: "Central apartments ideal for getting to know the village.", img: "https://images.unsplash.com/photo-1522708323590-d24dbb6b0267?w=400&h=250&fit=crop", parking: false, wifi: true, pool: false }
                ]
            },
            fr: {
                back: "Retour",
                appTitle: "Guide HORECA Chinata",
                heroTitle: "Découvrez Malpartida de Plasencia",
                heroSub: "Votre guide complet",
                cards: ["Découvrir Malpartida", "Que faire?", "Où manger?", "Où dormir?"],
                footer: "Avec le soutien de",
                who: "À propos",
                whoDesc: "Municipalité de la région de Monfragüe, province de Cáceres (Estrémadure), entre pâturages centenaires et oliveraies. Environ 4 600 habitants, alliant tradition agricole et tourisme rural.",
                historyTitle: "Histoire",
                historyDesc: "L'origine du surnom 'chinatos' : ils ont défendu le village en lançant des pierres (chinarros) contre les habitants de Plasencia.",
                natureTitle: "Environnement naturel",
                natureDesc: `<strong>🌿 Centre de Visiteurs Nord du Parc National de Monfragüe</strong><br>À 6 km du centre urbain, à côté du camping et de la gare. Bâtiment moderne de 2 000 m² avec salle d'exposition, espaces audiovisuels, interactifs et maquettes.<br><br>
                             <strong>🚂 Village de la Gare Empalme-Monfragüe</strong><br>Ancienne gare ferroviaire avec une architecture intéressante ; elle a compté près de 1 000 habitants.<br><br>
                             <strong>🌳 Dehesa Boyar el Robledo</strong><br>Espace naturel de chênes et rochers. Sentiers pour randonneurs et aventuriers. Restes archéologiques remarquables : Tombe de la Princesse, tombes anthropomorphes, menhirs, colline des Castillejos.<br><br>
                             <strong>💧 Environ de San Cristóbal - Réservoir</strong><br>À 4 km du village (Horco del Espino). Lieu boisé de pins avec aire de pique-nique et installations. Réservoir avec embarcadère pour canoë et kayak. La fête de San Cristóbal a lieu en juillet.`,
                interestTitle: "Informations pratiques",
                interestDesc: "Altitude 467m | Province de Cáceres | Fête : Avril (La Luz)",
                visitTitle: "Que visiter",
                churchDesc: "<strong>Église Paroissiale Saint-Jean-Baptiste</strong> – Principal monument. Temple du XVIe siècle (gothique, renaissance et baroque). Classé BIC depuis octobre 2018.",
                museumDesc: "<strong>Musée en plein air de la Maçonnerie</strong> – Répliques grandeur nature des œuvres des Concours de Maçonnerie. Dépliant avec images et plan de rue disponible.",
                hermitagesDesc: "<strong>Ermitages</strong> – San Blas, San Gregorio, Virgen de la Luz (Patronne) et San Cristóbal. Bâtiments actuels du XXe siècle.",
                quehacerPlaceholder: "Découvrez les meilleures activités de plein air et le patrimoine culturel à Malpartida de Plasencia. Cliquez sur chaque section pour voir tous les détails.",
                actividades: [
                    { nombre: "Observation des oiseaux", icono: "ti ti-feather", contenido: `<p>Limitrophe de Monfragüe, c'est l'un des meilleurs endroits d'Europe pour voir les rapaces.</p><p><strong>🔭 Ce qu'il faut voir:</strong> Vautour fauve, vautour moine, aigle impérial ibérique, cigogne noire et percnoptère.</p><p><strong>🏢 Entreprises locales:</strong> Vous pouvez réserver des circuits spécialisés avec <strong>Monfragüe Treasures</strong> (situé dans le même village) offrant des guides experts et du matériel optique.</p><p><strong>📍 Sites à proximité:</strong> El Salto del Gitano et la Portilla du Tiétar sont les points de vue les plus célèbres à quelques minutes en voiture.</p>` },
                    { nombre: "Patrimoine culturel", icono: "ti ti-building", contenido: `<p>Le village possède un riche héritage historique:</p><ul><li><strong>Église Saint-Jean-Baptiste:</strong> Monument du XVIe siècle classé Bien d'Intérêt Culturel. Remarquable pour son chœur et son architecture mêlant gothique tardif et renaissance.</li><li><strong>Cerro de los Castillejos:</strong> Un établissement vetton (peuple pré-romain) où l'on peut voir des restes de murailles, des menhirs et la curieuse "Tombe de la Princesse" (possible autel de sacrifices).</li><li><strong>Ermitages:</strong> San Blas, San Gregorio et Virgen de la Luz.</li></ul>` },
                    { nombre: "Randonnée et Centre de Visiteurs", icono: "ti ti-mountain", contenido: `<p><strong>🏛️ Centre de Visiteurs Nord "Jesús Garzón":</strong> Situé sur la route EX-208 (km 9), il est essentiel de le visiter avant d'entrer dans le Parc. Il propose des expositions sur la flore et la faune et possède un sentier interprétatif de 1 km idéal pour les familles. <strong>Avant de partir, passez au Centre de Visiteurs pour obtenir la brochure officielle avec les cartes à jour et des informations sur les éventuelles fermetures de sentiers en raison de la période de nidification.</strong></p><p><strong>🗺️ Sentiers remarquables:</strong></p><ul><li><strong>Cerro de los Castillejos:</strong> 5,8 km (aller-retour), faible difficulté. Visite de l'établissement vetton, menhirs et "Tombe de la Princesse". Départ au km 1,8 de la route CC-18.1.</li><li><strong>Mirador de Valdeherrero:</strong> Deux options (5,7 km ou 10 km), faible difficulté. Vues panoramiques sur La Vera.</li><li><strong>Sentier "El Robledo" (PR-CC 69):</strong> Boucle d'environ 17 km à travers chênaies et dehesa.</li><li><strong>Pic San Gregorio:</strong> 5 km (aller-retour), vues spectaculaires sur la plaine de Plasencia.</li><li><strong>Sentier Bleu (Parc National):</strong> Malpartida - Villarreal de San Carlos, 4-5 heures. Relie le village au cœur du Parc.</li><li><strong>Voie Verte de Monfragüe:</strong> 17,5 km (Camping Monfragüe - Haza Concepción). <em>(Actuellement travaux jusqu'à mi-2026, consulter l'état)</em></li><li><strong>Sentiers du Parc (depuis le Centre):</strong> Sentier Rouge (Château, 16 km), Sentier Vert (Cerro Gimio, 7,9 km), Sentier Jaune (La Tajadilla, 8,9 km).</li></ul>` },
                    { nombre: "Circuits à vélo", icono: "ti ti-bike", contenido: `<p><strong>🚵 Environs de la Dehesa:</strong> Malpartida est entourée de vastes dehesas avec des chemins publics idéaux pour le cyclotourisme VTT sans fortes pentes.</p><p><strong>🌍 Circuits longue distance:</strong> Fait partie de réseaux reliant Plasencia et d'autres localités de la Réserve de Biosphère de Monfragüe.</p>` },
                    { nombre: "Canoë et Kayak", icono: "ti ti-sailboat", contenido: `<p>Les activités nautiques se déroulent principalement dans les rivières et réservoirs proches:</p><p><strong>🌊 Rivière Tiétar:</strong> Des descentes en canoë sont organisées, surtout dans les zones d'eaux calmes permettant de profiter du paysage de Monfragüe depuis l'eau (en dehors des zones de protection maximale).</p><p><strong>🏢 Entreprises:</strong> Destino Activo (Monfragüe Vivo) organise des promenades en kayak et canoë dans les environs, généralement actives de juin à octobre.</p>` }
                ],
                comerDesc: "Dégustez la gastronomie locale dans les meilleurs restaurants et bars de Malpartida de Plasencia. Cuisine traditionnelle d'Estrémadure, tapas et produits de la dehesa.",
                dormirDesc: "Trouvez votre hébergement idéal à Malpartida de Plasencia et ses environs. Maisons rurales, appartements et hôtels près du Parc Naturel de Monfragüe.",
                comerSectionTitle: "Restaurants et bars à Malpartida et alentours",
                dormirSectionTitle: "Hébergements à Malpartida et alentours",
                filterOptions: { all: "Tous", parking: "Parking", wifi: "WiFi", pool: "Piscine" },
                badgeLabels: { parking: "Parking", wifi: "WiFi", pool: "Piscine" },
                restaurantes: [
                    { nombre: "Casa El Moreno", desc: "Bar avec bonne cuisine maison et ambiance locale.", img: "https://images.unsplash.com/photo-1555939594-58d7cb561ad1?w=400&h=250&fit=crop" },
                    { nombre: "Burguer Orix Café-Bar", desc: "Hamburgers et restauration rapide. Idéal pour un repas rapide.", img: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?w=400&h=250&fit=crop" },
                    { nombre: "El Habana", desc: "Café-bar avec tapas et portions. Ambiance animée.", img: "https://images.unsplash.com/photo-1590846406792-0adc7f938f1d?w=400&h=250&fit=crop" },
                    { nombre: "El Antares", desc: "Café-bar avec tapas et bonne ambiance. Musique et terrasse.", img: "https://images.unsplash.com/photo-1506354666786-959d6d497f1a?w=400&h=250&fit=crop" },
                    { nombre: "El Oasis", desc: "Pub et restaurant. Cuisine variée et boissons.", img: "https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?w=400&h=250&fit=crop" },
                    { nombre: "Las Habazas", desc: "Restaurant de qualité à côté du Parc National de Monfragüe. Réputé pour ses viandes et produits de la dehesa.", img: "https://images.unsplash.com/photo-1544025162-d76694265947?w=400&h=250&fit=crop" },
                    { nombre: "Camping de Monfragüe", desc: "Restaurant du camping avec menus et cuisine maison. Parfait pour les familles.", img: "https://images.unsplash.com/photo-1504280390367-361c6d9f38f4?w=400&h=250&fit=crop" },
                    { nombre: "Bar-Restaurant La Piscine", desc: "Restaurant avec terrasse et piscine. Idéal pour l'été.", img: "https://images.unsplash.com/photo-1537047902294-62a40c20a6ae?w=400&h=250&fit=crop" },
                    { nombre: "Churrería 3 Chocolats", desc: "Churros, petits déjeuners et plats à emporter. Spécialité de chocolat.", img: "https://images.unsplash.com/photo-1584370848010-d7fe6bc767ec?w=400&h=250&fit=crop" }
                ],
                alojamientos: [
                    { nombre: "Appartements Ruraux El Trillo", desc: "Appartements ruraux confortables avec tout le confort.", img: "https://images.unsplash.com/photo-1560185007-5f0bb1866cab?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Auberge de Monfragüe", desc: "Charmante auberge traditionnelle près du Parc National.", img: "https://images.unsplash.com/photo-1571003123894-1f0594d2b5d9?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Hôtel Puerta de Monfragüe", desc: "Hôtel moderne avec d'excellents services.", img: "https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?w=400&h=250&fit=crop", parking: true, wifi: true, pool: true },
                    { nombre: "Maison rurale 2 chambres", desc: "Maison complète avec deux chambres, cheminée et barbecue.", img: "https://images.unsplash.com/photo-1542718610-a1d656d1884c?w=400&h=250&fit=crop", parking: true, wifi: false, pool: false },
                    { nombre: "Maison rurale Del Corral et Appartements", desc: "Vaste complexe rural avec jardin.", img: "https://images.unsplash.com/photo-1583847268964-b28dc8f51f92?w=400&h=250&fit=crop", parking: true, wifi: true, pool: true },
                    { nombre: "Maison rurale Fuente Vieja", desc: "Ancienne maison rénovée avec charme rustique.", img: "https://images.unsplash.com/photo-1570129477492-45c003edd2be?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Maison rurale La Tomasa", desc: "Petite maison rurale très accueillante.", img: "https://images.unsplash.com/photo-1560185127-6ed189bf02f4?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Appartements Eras Centro", desc: "Appartements centraux idéaux pour découvrir le village.", img: "https://images.unsplash.com/photo-1522708323590-d24dbb6b0267?w=400&h=250&fit=crop", parking: false, wifi: true, pool: false }
                ]
            },
            pt: {
                back: "Voltar",
                appTitle: "Guia HORECA Chinata",
                heroTitle: "Descubra Malpartida de Plasencia",
                heroSub: "O seu guia completo",
                cards: ["Conhecer Malpartida", "O que fazer?", "Onde comer?", "Onde dormir?"],
                footer: "Com o apoio de",
                who: "Sobre nós",
                whoDesc: "Município da região de Monfragüe, província de Cáceres (Extremadura), entre dehesas centenárias e olivais. Cerca de 4.600 habitantes, combina tradição agrícola e turismo rural crescente.",
                historyTitle: "História",
                historyDesc: "A origem do apelido 'chinatos': defenderam o povo lançando pedras (chinarros) contra os placentinos.",
                natureTitle: "Ambiente natural",
                natureDesc: `<strong>🌿 Centro de Visitantes Norte do Parque Nacional de Monfragüe</strong><br>A 6 km do centro urbano, junto ao camping e à estação de trem. Edifício moderno de 2.000 m² com sala expositiva, audiovisuais, interativos e maquetes.<br><br>
                            <strong>🚂 Povoado da Estação Empalme-Monfragüe</strong><br>Antiga estação de trem com arquitetura interessante; chegou a ter cerca de 1.000 habitantes.<br><br>
                            <strong>🌳 Dehesa Boyar el Robledo</strong><br>Espaço natural de carvalhos e rochas. Rotas para caminhantes e aventureiros. Destacam-se restos arqueológicos: Tumba da Princesa, tumbas antropomórficas, menires, cerro dos Castillejos.<br><br>
                            <strong>💧 Entorno de San Cristóbal - Albufeira</strong><br>A 4 km do povoado (Horco del Espino). Bosque de pinheiros com merendeiro e instalações. Albufeira com embarcadouro para canoagem e caiaque. Em julho celebra-se a festa de San Cristóbal.`,
                interestTitle: "Dados de interesse",
                interestDesc: "Altitude 467m | Província de Cáceres | Festa: Abril (La Luz)",
                visitTitle: "O que visitar",
                churchDesc: "<strong>Igreja Paroquial de São João Batista</strong> – Principal monumento. Templo do séc. XVI (gótico, renascentista e barroco). BIC desde 2018.",
                museumDesc: "<strong>Museu ao Ar Livre de Alvenaria</strong> – Réplicas em tamanho real dos concursos. Folheto e mapa disponíveis.",
                hermitagesDesc: "<strong>Ermidas</strong> – San Blas, San Gregorio, Virgen de la Luz (Padroeira) e San Cristóbal. Edifícios do século XX.",
                quehacerPlaceholder: "Descubra as melhores atividades ao ar livre e património cultural em Malpartida de Plasencia. Clique em cada seção para ver as informações completas.",
                actividades: [
                    { nombre: "Observação de Aves", icono: "ti ti-feather", contenido: `<p>Por estar colado a Monfragüe, é um dos melhores lugares da Europa para ver aves de rapina.</p><p><strong>🔭 O que ver:</strong> Abutre-fouveiro, abutre-preto, águia-imperial-ibérica, cegonha-preta e britango.</p><p><strong>🏢 Empresas locais:</strong> Pode contratar rotas especializadas com <strong>Monfragüe Treasures</strong> (localizada na mesma vila) que oferecem guias especializados e material ótico.</p><p><strong>📍 Pontos próximos:</strong> El Salto del Gitano e Portilla del Tiétar são os miradouros mais famosos a poucos minutos de carro.</p>` },
                    { nombre: "Património Cultural", icono: "ti ti-building", contenido: `<p>A vila possui um rico legado histórico:</p><ul><li><strong>Igreja de São João Batista:</strong> Monumento do século XVI declarado Bem de Interesse Cultural. Destaca-se pelo seu coro e arquitetura que mistura gótico tardio e renascimento.</li><li><strong>Cerro de los Castillejos:</strong> Um assentamento vetão (povo pré-romano) onde se podem ver restos de muralhas, menires e a curiosa "Tumba da Princesa" (possível altar de sacrifícios).</li><li><strong>Ermidas:</strong> Destacam-se as de San Blas, San Gregorio e Virgen de la Luz.</li></ul>` },
                    { nombre: "Senderismo e Centro de Visitantes", icono: "ti ti-mountain", contenido: `<p><strong>🏛️ Centro de Visitantes Norte "Jesús Garzón":</strong> Situado na estrada EX-208 (km 9), é fundamental visitá-lo antes de entrar no Parque. Oferece exposições sobre a flora e fauna e tem uma trilha interpretativa de 1 km ideal para famílias. <strong>Antes de sair, passe pelo Centro de Visitantes para obter o folheto oficial com os mapas atualizados e informar-se sobre possíveis cortes de trilhos devido à época de nidificação.</strong></p><p><strong>🗺️ Rotas em destaque:</strong></p><ul><li><strong>Cerro de los Castillejos:</strong> 5,8 km (ida e volta), dificuldade baixa. Visita ao assentamento vetão, menires e "Tumba da Princesa". Começa no km 1,8 da estrada CC-18.1.</li><li><strong>Miradouro de Valdeherrero:</strong> Duas opções (5,7 km ou 10 km), dificuldade baixa. Vistas panorâmicas de La Vera.</li><li><strong>Rota "El Robledo" (PR-CC 69):</strong> Circular de cerca de 17 km por bosque de carvalhos e dehesa.</li><li><strong>Pico de San Gregorio:</strong> 5 km (ida e volta), vistas espetaculares da planície placentina.</li><li><strong>Rota Azul (Parque Nacional):</strong> Malpartida - Villarreal de San Carlos, 4-5 horas. Liga a vila ao centro do Parque.</li><li><strong>Via Verde de Monfragüe:</strong> 17,5 km (Camping Monfragüe - Haza Concepción). <em>(Atualmente obras até meados de 2026, consultar estado)</em></li><li><strong>Rotas do Parque (a partir do Centro):</strong> Rota Vermelha (Castelo, 16 km), Rota Verde (Cerro Gimio, 7,9 km), Rota Amarela (La Tajadilla, 8,9 km).</li></ul>` },
                    { nombre: "Rotas de Bicicleta", icono: "ti ti-bike", contenido: `<p><strong>🚵 Envolvente da Dehesa:</strong> Malpartida está rodeada por extensas dehesas com caminhos públicos ideais para o cicloturismo de montanha (BTT) sem grandes desníveis.</p><p><strong>🌍 Rotas de longa distância:</strong> Faz parte de redes que ligam Plasencia e outras localidades da Reserva da Biosfera de Monfragüe.</p>` },
                    { nombre: "Canoagem e Caiaque", icono: "ti ti-sailboat", contenido: `<p>As atividades aquáticas são realizadas principalmente nos rios e albufeiras próximas:</p><p><strong>🌊 Rio Tiétar:</strong> Organizam-se descidas de canoa, especialmente em zonas de águas calmas que permitem desfrutar da paisagem de Monfragüe a partir da água (fora das zonas de máxima proteção).</p><p><strong>🏢 Empresas:</strong> Destino Activo (Monfragüe Vivo) organiza passeios de caiaque e canoa pela região, geralmente operacionais de junho a outubro.</p>` }
                ],
                comerDesc: "Desfrute da gastronomia local nos melhores restaurantes e bares de Malpartida de Plasencia. Cozinha tradicional extremenha, tapas e produtos da dehesa.",
                dormirDesc: "Encontre o alojamento ideal em Malpartida de Plasencia e arredores. Casas rurais, apartamentos e hotéis perto do Parque Natural de Monfragüe.",
                comerSectionTitle: "Restaurantes e bares em Malpartida e arredores",
                dormirSectionTitle: "Alojamentos em Malpartida e arredores",
                filterOptions: { all: "Todos", parking: "Estacionamento", wifi: "WiFi", pool: "Piscina" },
                badgeLabels: { parking: "Estacionamento", wifi: "WiFi", pool: "Piscina" },
                restaurantes: [
                    { nombre: "Casa El Moreno", desc: "Bar com boa comida caseira e ambiente local.", img: "https://images.unsplash.com/photo-1555939594-58d7cb561ad1?w=400&h=250&fit=crop" },
                    { nombre: "Burguer Orix Café-Bar", desc: "Hambúrgueres e comida rápida. Ideal para uma refeição rápida.", img: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?w=400&h=250&fit=crop" },
                    { nombre: "El Habana", desc: "Café-bar com tapas e porções. Ambiente animado.", img: "https://images.unsplash.com/photo-1590846406792-0adc7f938f1d?w=400&h=250&fit=crop" },
                    { nombre: "El Antares", desc: "Café-bar com tapas e bom ambiente. Música e terraço.", img: "https://images.unsplash.com/photo-1506354666786-959d6d497f1a?w=400&h=250&fit=crop" },
                    { nombre: "El Oasis", desc: "Pub e restaurante. Cozinha variada e bebidas.", img: "https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?w=400&h=250&fit=crop" },
                    { nombre: "Las Habazas", desc: "Restaurante de qualidade junto ao Parque Nacional de Monfragüe. Conhecido por carnes e produtos da dehesa.", img: "https://images.unsplash.com/photo-1544025162-d76694265947?w=400&h=250&fit=crop" },
                    { nombre: "Camping de Monfragüe", desc: "Restaurante do camping com opções de menu e comida caseira. Perfeito para famílias.", img: "https://images.unsplash.com/photo-1504280390367-361c6d9f38f4?w=400&h=250&fit=crop" },
                    { nombre: "Bar-Restaurante La Piscina", desc: "Restaurante com terraço e piscina. Ideal para o verão.", img: "https://images.unsplash.com/photo-1537047902294-62a40c20a6ae?w=400&h=250&fit=crop" },
                    { nombre: "Churrería 3 Chocolates", desc: "Churros, pequenos-almoços e comida para levar. Especialidade em chocolate.", img: "https://images.unsplash.com/photo-1584370848010-d7fe6bc767ec?w=400&h=250&fit=crop" }
                ],
                alojamientos: [
                    { nombre: "Apartamentos Rurais El Trillo", desc: "Acolhedores apartamentos rurais com todas as comodidades.", img: "https://images.unsplash.com/photo-1560185007-5f0bb1866cab?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Estalagem de Monfragüe", desc: "Encantadora estalagem tradicional perto do Parque Nacional.", img: "https://images.unsplash.com/photo-1571003123894-1f0594d2b5d9?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Hotel Puerta de Monfragüe", desc: "Hotel moderno com excelentes serviços.", img: "https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?w=400&h=250&fit=crop", parking: true, wifi: true, pool: true },
                    { nombre: "Casa Rural 2 quartos", desc: "Casa completa com dois quartos, lareira e churrasqueira.", img: "https://images.unsplash.com/photo-1542718610-a1d656d1884c?w=400&h=250&fit=crop", parking: true, wifi: false, pool: false },
                    { nombre: "Casa Rural do Corral e Apartamentos", desc: "Amplo complexo rural com jardim.", img: "https://images.unsplash.com/photo-1583847268964-b28dc8f51f92?w=400&h=250&fit=crop", parking: true, wifi: true, pool: true },
                    { nombre: "Casa Rural Fuente Vieja", desc: "Antiga casa renovada com charme rústico.", img: "https://images.unsplash.com/photo-1570129477492-45c003edd2be?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Casa Rural La Tomasa", desc: "Pequena casa rural muito acolhedora.", img: "https://images.unsplash.com/photo-1560185127-6ed189bf02f4?w=400&h=250&fit=crop", parking: true, wifi: true, pool: false },
                    { nombre: "Apartamentos Eras Centro", desc: "Apartamentos centrais ideais para conhecer a vila.", img: "https://images.unsplash.com/photo-1522708323590-d24dbb6b0267?w=400&h=250&fit=crop", parking: false, wifi: true, pool: false }
                ]
            }
        };

        let currentLang = 'es';

        function addRipple(btn, e) {
            if (!btn || !e) return;
            const rect = btn.getBoundingClientRect();
            const size = Math.max(rect.width, rect.height);
            const x = e.clientX - rect.left - size / 2;
            const y = e.clientY - rect.top - size / 2;
            const ripple = document.createElement('span');
            ripple.className = 'ripple';
            ripple.style.cssText = `width:${size}px;height:${size}px;left:${x}px;top:${y}px`;
            btn.style.position = 'relative';
            btn.style.overflow = 'hidden';
            btn.appendChild(ripple);
            setTimeout(() => ripple.remove(), 600);
        }

        function transitionTo(fromId, toId, direction) {
            const from = document.getElementById(fromId);
            const to = document.getElementById(toId);
            if (!from || !to) return;
            const outClass = direction === 'forward' ? 'slide-out' : 'slide-out-back';
            const inClass = direction === 'forward' ? 'slide-in' : 'slide-in-back';
            from.classList.add(outClass);
            setTimeout(() => {
                from.classList.remove('active', outClass);
                to.classList.add('active', inClass);
                setTimeout(() => to.classList.remove(inClass), 350);
                const scrollArea = to.querySelector('.scroll-body, .main-content');
                if (scrollArea) scrollArea.scrollTop = 0;
            }, 70);
        }

        function changeLanguage(lang, event) {
            if (event && event.currentTarget) addRipple(event.currentTarget, event);
            currentLang = lang;
            const t = translations[lang];
            document.getElementById('app-title').textContent = t.appTitle;
            document.getElementById('hero-title').textContent = t.heroTitle;
            document.getElementById('hero-subtitle').textContent = t.heroSub;
            document.getElementById('card1-title').textContent = t.cards[0];
            document.getElementById('card2-title').textContent = t.cards[1];
            document.getElementById('card3-title').textContent = t.cards[2];
            document.getElementById('card4-title').textContent = t.cards[3];
            document.getElementById('footer-support').textContent = t.footer;
            document.getElementById('back-text').textContent = t.back;
            document.getElementById('language-screen').style.display = 'none';
            const mainApp = document.getElementById('main-app');
            mainApp.classList.add('active', 'main-entrance');
        }

        window.toggleActividad = function(index) {
            const element = document.getElementById(`act-${index}`);
            if (element) {
                element.classList.toggle('open');
                const header = element.querySelector('.actividad-header');
                if (header && window.event) addRipple(header, window.event);
            }
        };

        function filterAccommodations() {
            const select = document.getElementById('filter-select');
            if (!select) return;
            const filterValue = select.value;
            const cards = document.querySelectorAll('.accommodation-card');
            cards.forEach(card => {
                const parking = card.dataset.parking === 'true';
                const wifi = card.dataset.wifi === 'true';
                const pool = card.dataset.pool === 'true';
                let show = false;
                if (filterValue === 'all') show = true;
                else if (filterValue === 'parking') show = parking;
                else if (filterValue === 'wifi') show = wifi;
                else if (filterValue === 'pool') show = pool;
                card.style.display = show ? 'flex' : 'none';
            });
        }

        function openDetail(index, event) {
            if (event && event.currentTarget) addRipple(event.currentTarget, event);
            const t = translations[currentLang];
            const colors = ["#8AB0BE", "#7A8C3E", "#C2603A", "#e8c45a"];
            const textColor = index === 3 ? "#ffffff" : "white";
            document.getElementById('detail-title').textContent = t.cards[index];
            document.getElementById('detail-title').style.color = textColor;
            document.getElementById('detail-header').style.background = colors[index];
            document.getElementById('back-btn').style.color = textColor;

            const content = document.getElementById('detail-content');
            let html = '';

            if (index === 0) { // CONOCE
                html = `<div class="screen"><div class="divider"></div><div class="scroll-body"><div class="section"><div class="info-card hero"><div class="hero-content"><h3><i class="ti ti-info-circle"></i> ${t.who}</h3><p>${t.whoDesc}</p></div></div><div class="info-card"><h3><i class="ti ti-history"></i> ${t.historyTitle}</h3><p>${t.historyDesc}</p></div><div class="info-card"><h3><i class="ti ti-trees"></i> ${t.natureTitle}</h3><p>${t.natureDesc}</p></div><div class="info-card"><h3><i class="ti ti-calendar-event"></i> ${t.interestTitle}</h3><p>${t.interestDesc}</p></div><div class="info-card"><h3><i class="ti ti-camera"></i> ${t.visitTitle}</h3><p><strong>🏛️</strong> ${t.churchDesc}</p><p><strong>🛠️</strong> ${t.museumDesc}</p><p><strong>⛪</strong> ${t.hermitagesDesc}</p></div></div></div></div>`;
            } 
            else if (index === 1) { // QUÉ HACER - ACORDEÓN
                let accordionHtml = '';
                for (let i = 0; i < t.actividades.length; i++) {
                    const act = t.actividades[i];
                    accordionHtml += `
                        <div class="actividad-collapsible" id="act-${i}">
                            <div class="actividad-header" onclick="toggleActividad(${i})">
                                <div class="actividad-header-left">
                                    <i class="${act.icono}"></i>
                                    <span>${act.nombre}</span>
                                </div>
                                <i class="ti ti-chevron-right actividad-toggle-icon"></i>
                            </div>
                            <div class="actividad-details">
                                <div class="actividad-content">
                                    ${act.contenido}
                                </div>
                            </div>
                        </div>
                    `;
                }
                html = `<div class="screen"><div class="scroll-body"><div class="desc-header"><i class="ti ti-compass" style="color: #7a8c3e;"></i><p>${t.quehacerPlaceholder}</p></div><div class="divider"></div><div class="section">${accordionHtml}</div></div></div>`;
            } 
            else if (index === 2) { // COMER
                let cardsHtml = '';
                for (let r of t.restaurantes) {
                    cardsHtml += `<div class="image-card" style="background-image: url('${r.img}');"><h3><i class="ti ti-utensils"></i> ${r.nombre}</h3><p>${r.desc}</p></div>`;
                }
                html = `<div class="screen"><div class="scroll-body"><div class="desc-header"><i class="ti ti-chef-hat" style="color: #c2603a;"></i><p>${t.comerDesc}</p></div><div class="divider"></div><div class="section"><p class="section-title"><i class="ti ti-tool-kitchen-2"></i> ${t.comerSectionTitle}</p><div class="divider"></div>${cardsHtml}</div></div></div>`;
            } 
            else if (index === 3) { // DORMIR CON FILTRO Y BADGES TRADUCIDOS
                let cardsHtml = '';
                const badges = t.badgeLabels;
                for (let i = 0; i < t.alojamientos.length; i++) {
                    const a = t.alojamientos[i];
                    let badgesHtml = '';
                    if (a.parking) badgesHtml += `<span class="badge badge-parking"><i class="ti ti-car"></i> ${badges.parking}</span>`;
                    if (a.wifi) badgesHtml += `<span class="badge badge-wifi"><i class="ti ti-wifi"></i> ${badges.wifi}</span>`;
                    if (a.pool) badgesHtml += `<span class="badge badge-pool"><i class="ti ti-swimming"></i> ${badges.pool}</span>`;
                    cardsHtml += `
                        <div class="image-card accommodation-card" data-parking="${a.parking}" data-wifi="${a.wifi}" data-pool="${a.pool}" style="background-image: url('${a.img}');">
                            <h3><i class="ti ti-home"></i> ${a.nombre}</h3>
                            <p>${a.desc}</p>
                            <div class="badge-group">${badgesHtml}</div>
                        </div>
                    `;
                }
                const filterOptions = t.filterOptions;
                html = `<div class="screen"><div class="scroll-body"><div class="desc-header"><i class="ti ti-bed" style="color: #e8c45a;"></i><p>${t.dormirDesc}</p></div><div class="divider"></div><div class="section">
                            <div class="filter-bar">
                                <p class="section-title" style="margin-bottom:0;"><i class="ti ti-building-community"></i> ${t.dormirSectionTitle}</p>
                                <select id="filter-select" class="filter-select" onchange="filterAccommodations()">
                                    <option value="all">${filterOptions.all}</option>
                                    <option value="parking">${filterOptions.parking}</option>
                                    <option value="wifi">${filterOptions.wifi}</option>
                                    <option value="pool">${filterOptions.pool}</option>
                                </select>
                            </div>
                            <div id="accommodations-list">${cardsHtml}</div>
                        </div></div></div>`;
            }

            content.innerHTML = html;
            transitionTo('main-app', 'detail-screen', 'forward');
        }

        function goHome(event) {
            if (event && event.currentTarget) addRipple(event.currentTarget, event);
            transitionTo('detail-screen', 'main-app', 'back');
        }

        document.getElementById('language-screen').style.display = 'flex';
        document.getElementById('main-app').classList.remove('active');
    </script>
</body>

</html>
