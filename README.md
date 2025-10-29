<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Viagens & Aventuras - Agência de Turismo</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
        }
        
        .hero-bg {
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><defs><linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" style="stop-color:%2387CEEB;stop-opacity:1" /><stop offset="50%" style="stop-color:%2320B2AA;stop-opacity:1" /><stop offset="100%" style="stop-color:%23FF6347;stop-opacity:1" /></linearGradient></defs><rect width="1200" height="600" fill="url(%23bg)"/><circle cx="200" cy="150" r="80" fill="white" opacity="0.1"/><circle cx="800" cy="300" r="120" fill="white" opacity="0.1"/><circle cx="1000" cy="100" r="60" fill="white" opacity="0.1"/></svg>');
            background-size: cover;
            background-position: center;
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
        }
        
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .destination-card {
            background-size: cover;
            background-position: center;
            position: relative;
        }
        
        .destination-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(to bottom, transparent, rgba(0,0,0,0.7));
        }
        
        .floating {
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        
        .whatsapp-float {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background-color: #25d366;
            color: #FFF;
            border-radius: 50px;
            text-align: center;
            font-size: 30px;
            box-shadow: 2px 2px 3px #999;
            z-index: 100;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
        }
        
        .whatsapp-float:hover {
            background-color: #128c7e;
            transform: scale(1.1);
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7);
            }
            70% {
                box-shadow: 0 0 0 10px rgba(37, 211, 102, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(37, 211, 102, 0);
            }
        }
        
        /* REMOVIDO: CSS de avaliação por estrelas */
    </style>
</head>
<body class="bg-gray-50">
    <nav class="fixed top-0 w-full bg-white/95 backdrop-blur-sm z-50 shadow-lg">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center py-4">
                <div class="flex items-center space-x-2">
                    <div class="text-3xl" aria-hidden="true">✈️</div>
                    <div class="text-2xl font-bold text-blue-600">Aladin Turismo</div>
                </div>
                <div class="hidden md:flex space-x-8">
                    <a href="#inicio" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">Início</a>
                    <a href="#destinos" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">Destinos & Pacotes</a>
                    <a href="#servicos" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">Serviços</a>
                    <a href="#mensagem" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">Fale com um Agente</a>
                    <a href="#contato" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">Contato</a>
                </div>
                <a href="https://wa.me/5554999173172?text=Ol%C3%A1!%20Gostaria%20de%20fazer%20uma%20reserva%20com%20a%20Aladin%20Turismo." 
                   target="_blank" rel="noopener" aria-label="Reservar agora pelo WhatsApp"
                   class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700 transition-colors font-medium inline-block">
                    Reservar Agora
                </a>
            </div>
        </div>
    </nav>

    <section id="inicio" class="hero-bg min-h-screen flex items-center justify-center text-white">
        <div class="text-center px-4 max-w-4xl mx-auto">
            <div class="floating text-8xl mb-8" aria-hidden="true">🌍</div>
            <h1 class="text-5xl md:text-7xl font-bold mb-6 fade-in">Descubra o Mundo</h1>
            <p class="text-xl md:text-2xl mb-8 fade-in">
                Experiências únicas, destinos incríveis e memórias inesquecíveis te aguardam
            </p>
            <p class="text-lg mb-12 max-w-2xl mx-auto fade-in">
                Há mais de 20 anos criando viagens dos sonhos para nossos clientes. 
                Deixe-nos planejar sua próxima aventura!
            </p>
            <div class="space-x-4 fade-in">
                <a href="#destinos" class="bg-blue-600 text-white px-8 py-4 rounded-full font-semibold text-lg hover:bg-blue-700 transition-colors inline-block">
                    Ver Destinos & Pacotes
                </a>
                <a href="#servicos" class="border-2 border-white text-white px-8 py-4 rounded-full font-semibold text-lg hover:bg-white hover:text-blue-600 transition-colors inline-block">
                    Nossos Serviços
                </a>
            </div>
        </div>
    </section>

    <section id="destinos" class="py-0 bg-black">
        <div class="text-center py-20 bg-white">
            <h2 class="text-4xl md:text-5xl font-bold text-gray-800 mb-4 fade-in">Nossos Destinos</h2>
            <div class="w-24 h-1 bg-blue-600 mx-auto mb-4 fade-in"></div>
            <p class="text-xl text-gray-600 fade-in">Explore a beleza dos nossos destinos</p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/INN2IdS.jpg" 
                     alt="Caldas Novas - GO - Águas Termais" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #FF6B6B, #4ECDC4)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">♨️</div>
                        <h3 class="text-4xl font-bold mb-2">Caldas Novas</h3>
                        <p class="text-xl opacity-90">Águas Termais</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/F2GfPBz.jpg" 
                     alt="Ametista do Sul - RS - Geodas e Cristais" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #9B59B6, #8E44AD)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">💎</div>
                        <h3 class="text-4xl font-bold mb-2">Ametista do Sul</h3>
                        <p class="text-xl opacity-90">Geodas e Cristais</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/cGzckDX.jpg" 
                     alt="Foz do Iguaçu - PR - Cataratas Majestosas" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #3498DB, #2ECC71)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">🌊</div>
                        <h3 class="text-4xl font-bold mb-2">Foz do Iguaçu</h3>
                        <p class="text-xl opacity-90">Cataratas Majestosas</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/RvHJSwl.jpg" 
                     alt="Águas de Palmas - TO - Águas Termais" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #E67E22, #F39C12)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">🏊</div>
                        <h3 class="text-4xl font-bold mb-2">Águas de Palmas</h3>
                        <p class="text-xl opacity-90">Águas Termais</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/s8xbRtq.jpg" 
                     alt="Ruínas Jesuíticas - Patrimônio Histórico" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #d4af37, #ffd700)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">🏛️</div>
                        <h3 class="text-4xl font-bold mb-2">Ruínas Jesuíticas</h3>
                        <p class="text-xl opacity-90">Patrimônio Histórico</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/CwMwSXx.jpg" 
                     alt="Termas Romanas - Relaxamento e Bem-estar" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #16A085, #27AE60)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">🛁</div>
                        <h3 class="text-4xl font-bold mb-2">Termas Romanas</h3>
                        <p class="text-xl opacity-90">Relaxamento Total</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/M5Cz7jj.jpg" 
                     alt="Trem dos Pampas - Viagem Histórica" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #8E44AD, #9B59B6)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">🚂</div>
                        <h3 class="text-4xl font-bold mb-2">Trem dos Pampas</h3>
                        <p class="text-xl opacity-90">Viagem Histórica</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/uTrw0fh.jpg" 
                     alt="Cristo Protetor - Vista Panorâmica" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #667eea, #764ba2)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">✝️</div>
                        <h3 class="text-4xl font-bold mb-2">Cristo Protetor</h3>
                        <p class="text-xl opacity-90">Vista Panorâmica</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/ogYdLmJ.jpg" 
                     alt="Bonito - MS - Águas cristalinas" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #4ECDC4, #44A08D)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">🐠</div>
                        <h3 class="text-4xl font-bold mb-2">Bonito - MS</h3>
                        <p class="text-xl opacity-90">Águas Cristalinas</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/QmOmuMA.jpg" 
                     alt="Itapema - SC - Praias Paradisíacas" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #FF9A8B, #A8E6CF)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">🏖️</div>
                        <h3 class="text-4xl font-bold mb-2">Itapema - SC</h3>
                        <p class="text-xl opacity-90">Praias Paradisíacas</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/tiGaxv2.jpg" 
                     alt="Aparecida - SP - Santuário Nacional" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #667eea, #764ba2)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">⛪</div>
                        <h3 class="text-4xl font-bold mb-2">Aparecida - SP</h3>
                        <p class="text-xl opacity-90">Santuário Nacional</p>
                    </div>
                </div>
            </div>

            <div class="relative h-screen group overflow-hidden cursor-pointer">
                <img src="https://i.imgur.com/fXKWRRb.jpg" 
                     alt="Gramado - RS - Serra Gaúcha" 
                     class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                     onerror="this.style.display='none'; this.parentElement.style.background='linear-gradient(45deg, #FFD93D, #FF6B6B)';">
                <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-500"></div>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center text-white transform group-hover:scale-105 transition-transform duration-500">
                        <div class="text-6xl mb-4" aria-hidden="true">🏔️</div>
                        <h3 class="text-4xl font-bold mb-2">Gramado - RS</h3>
                        <p class="text-xl opacity-90">Serra Gaúcha</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="servicos" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-bold text-gray-800 mb-4 fade-in">Nossos Serviços</h2>
                <div class="w-24 h-1 bg-blue-600 mx-auto mb-4 fade-in"></div>
                <p class="text-xl text-gray-600 fade-in">Tudo que você precisa para uma viagem perfeita</p>
            </div>
            <div class="grid md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-5 gap-8">
                <div class="text-center fade-in">
                    <div class="w-20 h-20 bg-blue-100 rounded-full flex items-center justify-center text-4xl text-blue-600 mx-auto mb-4" aria-hidden="true">
                        🎁
                    </div>
                    <h3 class="text-xl font-semibold text-gray-800 mb-2">Pacotes Exclusivos</h3>
                    <p class="text-gray-600">Descubra o mundo com nossos roteiros completos, que incluem transporte, hospedagem e atividades inesquecíveis</p>
                </div>
                <div class="text-center fade-in">
                    <div class="w-20 h-20 bg-green-100 rounded-full flex items-center justify-center text-4xl text-green-600 mx-auto mb-4" aria-hidden="true">
                        ✈️
                    </div>
                    <h3 class="text-xl font-semibold text-gray-800 mb-2">Pacotes Aéreos</h3>
                    <p class="text-gray-600">Encontre as melhores ofertas e garanta sua passagem com a gente, sem complicações e com total segurança</p>
                </div>
                <div class="text-center fade-in">
                    <div class="w-20 h-20 bg-purple-100 rounded-full flex items-center justify-center text-4xl text-purple-600 mx-auto mb-4" aria-hidden="true">
                        💼
                    </div>
                    <h3 class="text-xl font-semibold text-gray-800 mb-2">Consultoria de Viagem</h3>
                    <p class="text-gray-600">Precisa de ajuda para planejar sua viagem dos sonhos? Nossos especialistas estão prontos para te ajudar</p>
                </div>
                <div class="text-center fade-in">
                    <div class="w-20 h-20 bg-orange-100 rounded-full flex items-center justify-center text-4xl text-orange-600 mx-auto mb-4" aria-hidden="true">
                        🗺️
                    </div>
                    <h3 class="text-xl font-semibold text-gray-800 mb-2">Turismo Receptivo</h3>
                    <p class="text-gray-600">Conheça os melhores roteiros e pontos turísticos da região. Oferecemos guias especializados para explorar Vacaria e cidades próximas</p>
                </div>
                <div class="text-center fade-in">
                    <div class="w-20 h-20 bg-red-100 rounded-full flex items-center justify-center text-4xl text-red-600 mx-auto mb-4" aria-hidden="true">
                        🚌
                    </div>
                    <h3 class="text-xl font-semibold text-gray-800 mb-2">Turismo Rodoviário</h3>
                    <p class="text-gray-600">Viaje pelo Brasil com todo o conforto e segurança. Nossas viagens de ônibus são perfeitas para quem busca uma experiência completa, sem se preocupar com nada</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Depoimentos (mantidos) -->
    <section class="py-20 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-bold text-gray-800 mb-4 fade-in">O Que Dizem Nossos Clientes</h2>
                <div class="w-24 h-1 bg-blue-600 mx-auto fade-in"></div>
            </div>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="bg-white p-8 rounded-2xl shadow-lg fade-in">
                    <p class="text-gray-600 mb-6">"Experiência incrível! A equipe cuidou de todos os detalhes da nossa viagem para Bonito. Recomendo muito!"</p>
                </div>
                <div class="bg-white p-8 rounded-2xl shadow-lg fade-in">
                    <p class="text-gray-600 mb-6">"Viagem dos sonhos para Gramado! Tudo organizado perfeitamente, hotéis excelentes e roteiro impecável."</p>
                </div>
                <div class="bg-white p-8 rounded-2xl shadow-lg fade-in">
                    <p class="text-gray-600 mb-6">"Atendimento excepcional! Nos ajudaram em tudo, desde o planejamento até o retorno. Já estamos planejando a próxima!"</p>
                </div>
                <div class="bg-white p-8 rounded-2xl shadow-lg fade-in">
                    <p class="text-gray-600 mb-6">"Uma excelente empresa, apresenta um grande profissionalismo e preparo."</p>
                </div>
                <div class="bg-white p-8 rounded-2xl shadow-lg fade-in">
                    <p class="text-gray-600 mb-6">"Fomos muito bem atendidos e adoramos o passeio."</p>
                </div>
                <div class="bg-white p-8 rounded-2xl shadow-lg fade-in">
                    <p class="text-gray-600 mb-6">"Receptivo de excelência em Vacaria! Comprometidos e responsáveis, entregando trabalho de qualidade! Eu Recomendo!"</p>
                </div>
            </div>
        </div>
    </section>

    <!-- NOVA SEÇÃO: Fale com um Agente (substitui a avaliação) -->
    <section id="mensagem" class="py-20 bg-gray-100">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12 fade-in">
                <h2 class="text-4xl md:text-5xl font-bold text-gray-800 mb-4">Fale com um Agente</h2>
                <div class="w-24 h-1 bg-blue-600 mx-auto mb-4"></div>
                <p class="text-xl text-gray-600">Envie sua mensagem e respondemos pelo WhatsApp.</p>
            </div>
            
            <form id="form-whatsapp" class="bg-white p-8 rounded-2xl shadow-lg fade-in" autocomplete="on">
                <div class="grid md:grid-cols-2 gap-6">
                    <div>
                        <label for="wppNome" class="block text-gray-700 font-semibold mb-2">Seu Nome</label>
                        <input type="text" id="wppNome" name="nome" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500 transition-colors" placeholder="Ex.: Maria Silva" required>
                    </div>
                    <div>
                        <label for="wppDestino" class="block text-gray-700 font-semibold mb-2">Destino de Interesse</label>
                        <input type="text" id="wppDestino" name="destino" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500 transition-colors" placeholder="Ex.: Caldas Novas, Gramado">
                    </div>
                    <div>
                        <label for="wppData" class="block text-gray-700 font-semibold mb-2">Data aproximada</label>
                        <input type="date" id="wppData" name="data" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500 transition-colors">
                    </div>
                    <div>
                        <label for="wppAgente" class="block text-gray-700 font-semibold mb-2">Falar com</label>
                        <select id="wppAgente" name="agente" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500 transition-colors">
                            <option value="5554999173172">Aladin (Atendimento)</option>
                            <!-- Adicione outros agentes aqui, usando o formato com DDI 55 + DDD + número, por exemplo: 5554XXXXXXXXX -->
                        </select>
                    </div>
                </div>
                <div class="mt-6">
                    <label for="wppMensagem" class="block text-gray-700 font-semibold mb-2">Sua Mensagem</label>
                    <textarea id="wppMensagem" name="mensagem" rows="4" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500 transition-colors" placeholder="Conte um pouco sobre sua viagem (número de pessoas, preferências, orçamento...)" required></textarea>
                </div>
                <button type="submit" class="mt-6 w-full bg-green-600 text-white font-semibold py-3 rounded-full hover:bg-green-700 transition-colors">Enviar no WhatsApp</button>
                <p class="text-center text-gray-500 mt-4 text-sm">Abriremos o WhatsApp com a mensagem preenchida para você revisar e enviar.</p>
            </form>
        </div>
    </section>

    <section id="contato" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-bold text-gray-800 mb-4 fade-in">Entre em Contato</h2>
                <div class="w-24 h-1 bg-blue-600 mx-auto mb-4 fade-in"></div>
                <p class="text-xl text-gray-600 fade-in">Vamos planejar sua próxima aventura juntos!</p>
            </div>
            <div class="grid lg:grid-cols-2 gap-12">
                <div class="fade-in">
                    <h3 class="text-2xl font-semibold text-gray-800 mb-8">Informações de Contato</h3>
                    <div class="space-y-6">
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center text-blue-600 mr-4" aria-hidden="true">
                                📍
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-800">Endereço</h4>
                                <p class="text-gray-600">Rua Siqueira Campos N°44 - Jardim América - Vacaria, RS</p>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center text-blue-600 mr-4" aria-hidden="true">
                                📞
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-800">Telefone</h4>
                                <p class="text-gray-600">(54) 99917-3172</p>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center text-blue-600 mr-4" aria-hidden="true">
                                📧
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-800">Email</h4>
                                <p class="text-gray-600">aladinturismo@gmail.com</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mt-8">
                        <h4 class="font-semibold text-gray-800 mb-4">Nossa Localização</h4>
                        <div class="bg-gray-100 rounded-lg overflow-hidden shadow-lg">
                            <iframe 
                                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3466.012571212879!2d-50.9328247!3d-28.5135502!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x951c6c5478d10b87%3A0xf6758c0c9f131102!2sRua%20Siqueira%20Campos%2C%2044%20-%20Jardim%20Am%C3%A9rica%2C%20Vacaria%20-%20RS%2C%2095200-000%2C%20Brasil!5e0!3m2!1spt-BR!2sus!4v1628173456789!5m2!1spt-BR!2sus"
                                width="100%" 
                                height="250" 
                                style="border:0;" 
                                allowfullscreen="" 
                                loading="lazy" 
                                referrerpolicy="no-referrer-when-downgrade"
                                title="Localização da Aladin Turismo">
                            </iframe>
                        </div>
                        <div class="mt-4 text-center">
                            <a href="https://goo.gl/maps/YOUR_GOOGLE_MAPS_LINK" 
                               target="_blank" rel="noopener"
                               class="inline-flex items-center px-4 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors">
                                📍 Ver no Google Maps
                            </a>
                        </div>
                    </div>
                    <div class="mt-8">
                        <h4 class="font-semibold text-gray-800 mb-4">Redes Sociais</h4>
                        <div class="flex space-x-4">
                            <a href="https://www.facebook.com/aladinturismo" target="_blank" rel="noopener"
                               class="w-12 h-12 bg-blue-600 text-white rounded-full hover:bg-blue-700 transition-colors text-xl flex items-center justify-center" aria-label="Facebook">
                                📘
                            </a>
                            <a href="https://www.instagram.com/aladinturismo" target="_blank" rel="noopener"
                               class="w-12 h-12 bg-pink-500 text-white rounded-full hover:bg-pink-600 transition-colors text-xl flex items-center justify-center" aria-label="Instagram">
                                📷
                            </a>
                            <a href="https://wa.me/5554999173172?text=Ol%C3%A1!%20Gostaria%20de%20saber%20mais%20sobre%20os%20pacotes%20de%20viagem." 
                               target="_blank" rel="noopener"
                               class="w-12 h-12 bg-green-500 text-white rounded-full hover:bg-green-600 transition-colors text-xl flex items-center justify-center" aria-label="WhatsApp">
                                📱
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <a href="https://wa.me/5554999173172?text=Ol%C3%A1!%20Gostaria%20de%20fazer%20uma%20reserva%20com%20a%20Aladin%20Turismo."
       class="whatsapp-float pulse" 
       target="_blank" rel="noopener" aria-label="Abrir WhatsApp da Aladin Turismo">
        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" fill="currentColor"><path d="M12.04 2.16c-5.46 0-9.91 4.45-9.91 9.91 0 1.75.46 3.44 1.35 4.93L.5 21.49l4.57-1.2A9.91 9.91 0 0 0 12.04 22c5.46 0 9.91-4.45 9.91-9.91C21.95 6.61 17.5 2.16 12.04 2.16zm-1.85 15.54a.79.79 0 0 1-.84-.5l-.83-1.87a.79.79 0 0 1 .5-.83l1.87-.83a.79.79 0 0 1 .84.5l.83 1.87a.79.79 0 0 1-.5.83l-1.87.83zm3.7-2.34a.79.79 0 0 1 .84.5l.83 1.87a.79.79 0 0 1-.5.83l-1.87.83a.79.79 0 0 1-.84-.5l-.83-1.87a.79.79 0 0 1 .5-.83l1.87-.83zm2.5-4.17a.79.79 0 0 1-.84.5l-.83 1.87a.79.79 0 0 1 .5.83l1.87.83a.79.79 0 0 1 .84-.5l.83-1.87a.79.79 0 0 1-.5-.83l-1.87-.83z"/></svg>
    </a>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                    } else {
                        entry.target.classList.remove('visible');
                    }
                });
            }, {
                threshold: 0.1
            });

            document.querySelectorAll('.fade-in').forEach(element => {
                observer.observe(element);
            });

            // Envio para WhatsApp
            const form = document.getElementById('form-whatsapp');
            form.addEventListener('submit', function(e) {
                e.preventDefault();
                const nome = document.getElementById('wppNome').value.trim();
                const destino = document.getElementById('wppDestino').value.trim();
                const data = document.getElementById('wppData').value;
                const mensagem = document.getElementById('wppMensagem').value.trim();
                const agente = document.getElementById('wppAgente').value.trim();

                const partes = [];
                if (nome) partes.push(`Olá! Meu nome é ${nome}.`);
                if (destino) partes.push(`Destino de interesse: ${destino}.`);
                if (data) {
                    try {
                        const d = new Date(data);
                        const dataBR = d.toLocaleDateString('pt-BR', { timeZone: 'America/Sao_Paulo' });
                        partes.push(`Data aproximada: ${dataBR}.`);
                    } catch (err) {}
                }
                if (mensagem) partes.push(`Mensagem: ${mensagem}`);

                const texto = partes.join('\n');
                const url = `https://wa.me/${agente}?text=${encodeURIComponent(texto)}`;
                window.open(url, '_blank');
            });
        });
    </script>
</body>
</html>
