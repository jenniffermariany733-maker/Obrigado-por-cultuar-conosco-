# Convitecultoprecongresso
Geração kadosh 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VOCÊ FOI CONVIDADO - Culto Pré-Congresso Geração Kadosh</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0f1428 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 600px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        /* Initial Screen */
        .initial-screen {
            text-align: center;
            animation: fadeInDown 1s ease-out;
            opacity: 1;
            transition: opacity 0.8s ease-in-out;
        }

        .initial-screen.hidden {
            opacity: 0;
            pointer-events: none;
        }

        .invitation-text {
            font-size: 4rem;
            font-weight: 700;
            letter-spacing: 2px;
            margin-bottom: 60px;
            background: linear-gradient(135deg, #d4af37 0%, #f5e6d3 50%, #d4af37 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInDown 1.2s ease-out;
        }

        .click-button {
            padding: 18px 50px;
            font-size: 1.2rem;
            font-weight: 600;
            color: #0a0e27;
            background: linear-gradient(135deg, #d4af37 0%, #f5e6d3 100%);
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3);
            text-transform: uppercase;
            letter-spacing: 1px;
            animation: slideUp 1.2s ease-out;
        }

        .click-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(212, 175, 55, 0.5);
        }

        .click-button:active {
            transform: translateY(-1px);
        }

        /* Invitation Details */
        .invitation-details {
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.8s ease-in-out;
            animation: fadeInUp 1s ease-out forwards;
        }

        .invitation-details.show {
            opacity: 1;
            pointer-events: auto;
        }

        .banner {
            width: 100%;
            height: 250px;
            background: linear-gradient(135deg, #d4af37 0%, #f5e6d3 50%, #d4af37 100%);
            border-radius: 15px 15px 0 0;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 3.5rem;
            color: #0a0e27;
            font-weight: 700;
            text-align: center;
            padding: 20px;
            box-shadow: 0 10px 40px rgba(212, 175, 55, 0.3);
            margin-bottom: 0;
        }

        .invitation-card {
            background: linear-gradient(135deg, rgba(212, 175, 55, 0.1) 0%, rgba(212, 175, 55, 0.05) 100%);
            backdrop-filter: blur(10px);
            border: 2px solid rgba(212, 175, 55, 0.3);
            border-radius: 0 0 15px 15px;
            padding: 40px 30px;
            max-width: 500px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
            margin-bottom: 30px;
        }

        .event-title {
            font-size: 2rem;
            font-weight: 700;
            color: #d4af37;
            margin-bottom: 25px;
            text-align: center;
            line-height: 1.3;
        }

        .event-subtitle {
            font-size: 1.1rem;
            color: #b8860b;
            text-align: center;
            margin-bottom: 30px;
            font-style: italic;
        }

        .divider {
            height: 2px;
            background: linear-gradient(90deg, transparent, #d4af37, transparent);
            margin: 25px 0;
        }

        .event-info {
            margin-bottom: 20px;
        }

        .info-label {
            font-size: 0.9rem;
            color: #b8860b;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .info-content {
            font-size: 1.3rem;
            color: #f5e6d3;
            font-weight: 500;
            line-height: 1.6;
        }

        .theme-section {
            background: rgba(212, 175, 55, 0.1);
            padding: 20px;
            border-left: 4px solid #d4af37;
            border-radius: 8px;
            margin-top: 25px;
        }

        .theme-label {
            font-size: 0.85rem;
            color: #b8860b;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .theme-text {
            font-size: 1.2rem;
            color: #f5e6d3;
            font-weight: 500;
            margin-bottom: 10px;
            line-height: 1.6;
        }

        .theme-reference {
            font-size: 0.95rem;
            color: #d4af37;
            font-style: italic;
        }

        .instagram-button {
            width: 100%;
            padding: 16px;
            margin-top: 30px;
            background: linear-gradient(135deg, #d4af37 0%, #f5e6d3 100%);
            color: #0a0e27;
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            text-align: center;
            letter-spacing: 1px;
            box-shadow: 0 8px 25px rgba(212, 175, 55, 0.3);
        }

        .instagram-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 35px rgba(212, 175, 55, 0.5);
        }

        .instagram-button:active {
            transform: translateY(0);
        }

        /* Animations */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .invitation-text {
                font-size: 2.5rem;
                margin-bottom: 40px;
            }

            .click-button {
                padding: 16px 40px;
                font-size: 1rem;
            }

            .banner {
                height: 200px;
                font-size: 2.5rem;
            }

            .invitation-card {
                padding: 30px 20px;
                margin-bottom: 20px;
            }

            .event-title {
                font-size: 1.5rem;
            }

            .info-content {
                font-size: 1.1rem;
            }

            .theme-text {
                font-size: 1rem;
            }
        }

        @media (max-width: 480px) {
            .invitation-text {
                font-size: 2rem;
                margin-bottom: 30px;
            }

            .click-button {
                padding: 14px 35px;
                font-size: 0.95rem;
            }

            .banner {
                height: 150px;
                font-size: 2rem;
                padding: 15px;
            }

            .invitation-card {
                padding: 25px 15px;
            }

            .event-title {
                font-size: 1.3rem;
                margin-bottom: 15px;
            }

            .info-label {
                font-size: 0.8rem;
                margin-bottom: 5px;
            }

            .info-content {
                font-size: 1rem;
            }

            .theme-text {
                font-size: 0.95rem;
            }

            .instagram-button {
                font-size: 0.9rem;
                padding: 14px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Initial Screen -->
        <div class="initial-screen" id="initialScreen">
            <h1 class="invitation-text">VOCÊ FOI<br>CONVIDADO</h1>
            <button class="click-button" onclick="revealInvitation()">Clique e descubra</button>
        </div>

        <!-- Invitation Details -->
        <div class="invitation-details" id="invitationDetails">
            <div class="banner">🎉✨</div>
            <div class="invitation-card">
                <h2 class="event-title">Culto Pré-Congresso<br>Geração Kadosh</h2>
                
                <p class="event-subtitle">"Alegrem-se, mas lembrem-se"</p>

                <div class="divider"></div>

                <div class="event-info">
                    <p class="info-label">📅 Data e Hora</p>
                    <p class="info-content">26 de março às 19h</p>
                </div>

                <div class="event-info">
                    <p class="info-label">📍 Local</p>
                    <p class="info-content">Assembleia de Deus<br>Ministério Sal e Luz<br>Av. dos Trovadores, 286</p>
                </div>

                <div class="divider"></div>

                <div class="theme-section">
                    <p class="theme-label">💫 Tema</p>
                    <p class="theme-text">"Alegrem-se, mas lembrem-se"</p>
                    <p class="theme-reference">Eclesiastes 11:9</p>
                </div>

                <a href="https://www.instagram.com/kadosh_saleluz" target="_blank" class="instagram-button">
                    Siga no Instagram @kadosh_saleluz
                </a>
            </div>
        </div>
    </div>

    <script>
        function revealInvitation() {
            const initialScreen = document.getElementById('initialScreen');
            const invitationDetails = document.getElementById('invitationDetails');
            
            // Fade out initial screen
            initialScreen.classList.add('hidden');
            
            // Show invitation details
            setTimeout(() => {
                invitationDetails.classList.add('show');
            }, 100);
        }

        // Optional: Add scroll animation on page load
        document.addEventListener('DOMContentLoaded', function() {
            const initialScreen = document.getElementById('initialScreen');
            initialScreen.style.animation = 'fadeInDown 1s ease-out';
        });
    </script>
</body>
</html>
