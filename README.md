<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>João Guilherme (Raio) | Portfolio</title>
    <style>
        /* Reset and General Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary-color: rgb(32, 211, 91);
            --secondary-color: rgb(0, 160, 80);
            --highlight-color: rgb(255, 255, 255);
            --bg-color: rgb(0, 233, 116);
            --text-color: rgb(0, 0, 0);
            --light-bg: rgba(32, 211, 91, 0.1);
            --dark-bg: rgba(0, 160, 80, 0.9);
            --border-color: rgba(0, 160, 80, 0.3);
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            --border-radius: 8px;
        }
        
        body {
            font-family: 'Arial', 'Helvetica', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--highlight-color);
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        h1, h2, h3, h4, h5, h6 {
            margin-bottom: 15px;
            color: var(--text-color);
        }
        
        p {
            margin-bottom: 15px;
        }
        
        a {
            text-decoration: none;
            color: var(--secondary-color);
            transition: all 0.3s ease;
        }
        
        a:hover {
            color: var(--primary-color);
        }
        
        ul {
            list-style: none;
        }
        
        img {
            max-width: 100%;
            height: auto;
            display: block;
            border-radius: 8px;
        }
        
        /* Header and Navigation */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            border-bottom: 2px solid var(--primary-color);
            margin-bottom: 40px;
        }
        
        .logo {
            font-size: 2rem;
            font-weight: bold;
            color: var(--primary-color);
        }
        
        .logo span {
            color: var(--secondary-color);
        }
        
        nav ul {
            display: flex;
            gap: 20px;
        }
        
        nav ul li a {
            padding: 5px 10px;
            border-radius: 4px;
            transition: all 0.3s ease;
        }
        
        nav ul li a:hover {
            background-color: var(--light-bg);
        }
        
        /* Banner */
        .banner {
            margin-bottom: 40px;
            position: relative;
            overflow: hidden;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }
        
        .banner img {
            width: 100%;
            height: auto;
        }
        
        .banner-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(0, 160, 80, 0.8), rgba(32, 211, 91, 0.6));
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            color: var(--highlight-color);
        }
        
        .banner-overlay h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: var(--highlight-color);
        }
        
        .banner-overlay h2 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--highlight-color);
        }
        
        /* Section Styles */
        section {
            margin-bottom: 60px;
        }
        
        .section-title {
            font-size: 2rem;
            margin-bottom: 30px;
            padding-bottom: 10px;
            border-bottom: 3px solid var(--primary-color);
            display: inline-block;
        }
        
        /* Color Palette */
        .color-palette {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .color-item {
            flex: 1;
            min-width: 150px;
            padding: 15px;
            border-radius: var(--border-radius);
            color: var(--highlight-color);
            text-align: center;
        }
        
        .color-primary {
            background-color: rgb(32, 211, 91);
        }
        
        .color-secondary {
            background-color: rgb(0, 160, 80);
        }
        
        .color-highlight {
            background-color: rgb(255, 255, 255);
            color: var(--text-color);
            border: 1px solid #ddd;
        }
        
        .color-bg {
            background-color: rgb(0, 233, 116);
        }
        
        .color-text {
            background-color: rgb(0, 0, 0);
        }
        
        /* About Me */
        .about-content {
            display: flex;
            gap: 40px;
            margin-top: 20px;
        }
        
        .about-text {
            flex: 2;
        }
        
        .about-info {
            flex: 1;
            background-color: var(--light-bg);
            padding: 20px;
            border-radius: var(--border-radius);
        }
        
        .info-item {
            margin-bottom: 15px;
        }
        
        .info-item h3 {
            font-size: 1rem;
            color: var(--secondary-color);
            margin-bottom: 5px;
        }
        
        /* Skills */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .skill-category {
            background-color: var(--light-bg);
            padding: 20px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }
        
        .skill-category h3 {
            color: var(--secondary-color);
            margin-bottom: 20px;
            text-align: center;
        }
        
        .skill-item {
            margin-bottom: 15px;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }
        
        .progress-bar {
            width: 100%;
            height: 10px;
            background-color: var(--border-color);
            border-radius: 5px;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background-color: var(--primary-color);
        }
        
        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background-color: var(--light-bg);
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-content h3 {
            margin-bottom: 10px;
        }
        
        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
        }
        
        .tag {
            background-color: var(--primary-color);
            color: var(--highlight-color);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        /* Experience */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            width: 2px;
            background-color: var(--secondary-color);
            top: 0;
            bottom: 0;
            left: 20px;
        }
        
        .timeline-item {
            padding-left: 50px;
            position: relative;
            margin-bottom: 30px;
        }
        
        .timeline-dot {
            position: absolute;
            width: 16px;
            height: 16px;
            background-color: var(--primary-color);
            border-radius: 50%;
            left: 13px;
            top: 5px;
            z-index: 1;
        }
        
        .timeline-content {
            background-color: var(--light-bg);
            padding: 20px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }
        
        .timeline-date {
            font-weight: bold;
            color: var(--primary-color);
            margin-bottom: 10px;
        }
        
        /* Education */
        .education-item {
            background-color: var(--light-bg);
            padding: 20px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            margin-bottom: 20px;
        }
        
        .education-item h3 {
            color: var(--text-color);
        }
        
        .education-item h4 {
            color: var(--secondary-color);
            margin-bottom: 10px;
        }
        
        /* RPG Section */
        .rpg-section {
            background-color: var(--light-bg);
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }
        
        .rpg-list {
            margin: 20px 0;
        }
        
        .rpg-list li {
            margin-bottom: 15px;
            padding-left: 25px;
            position: relative;
        }
        
        .rpg-list li::before {
            content: '';
            position: absolute;
            left: 0;
            top: 8px;
            width: 8px;
            height: 8px;
            background-color: var(--primary-color);
            border-radius: 50%;
        }
        
        .rpg-list-title {
            font-weight: bold;
            display: block;
            margin-bottom: 5px;
            color: var(--secondary-color);
        }
        
        /* Contact */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .contact-info {
            background-color: var(--light-bg);
            padding: 20px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .contact-icon {
            width: 40px;
            height: 40px;
            background-color: var(--primary-color);
            color: var(--highlight-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.2rem;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-icon {
            width: 40px;
            height: 40px;
            background-color: var(--primary-color);
            color: var(--highlight-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }
        
        .social-icon:hover {
            background-color: var(--secondary-color);
            transform: translateY(-3px);
        }
        
        .contact-form {
            background-color: var(--light-bg);
            padding: 20px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid var(--border-color);
            border-radius: 4px;
            font-family: inherit;
        }
        
        .form-group textarea {
            height: 120px;
            resize: vertical;
        }
        
        .submit-btn {
            background-color: var(--primary-color);
            color: var(--highlight-color);
            border: none;
            padding: 12px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
        }
        
        .submit-btn:hover {
            background-color: var(--secondary-color);
        }
        
        /* Technologies */
        .tech-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }
        
        .tech-badge {
            background-color: var(--primary-color);
            color: var(--highlight-color);
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: bold;
        }
        
        /* Footer */
        footer {
            margin-top: 60px;
            padding-top: 20px;
            border-top: 2px solid var(--primary-color);
            text-align: center;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
                flex-wrap: wrap;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .banner-overlay h1 {
                font-size: 2rem;
            }
            
            .banner-overlay h2 {
                font-size: 1.2rem;
            }
        }
        
        @media (max-width: 480px) {
            .section-title {
                font-size: 1.5rem;
            }
            
            .banner-overlay h1 {
                font-size: 1.5rem;
            }
            
            .banner-overlay h2 {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header and Navigation -->
    <header>
        <div class="logo">Raio<span>Site</span></div>
        <nav>
            <ul>
                <li><a href="#about">Sobre</a></li>
                <li><a href="#skills">Habilidades</a></li>
                <li><a href="#projects">Projetos</a></li>
                <li><a href="#experience">Experiência</a></li>
                <li><a href="#education">Formação</a></li>
                <li><a href="#rpg">RPG & Computação</a></li>
                <li><a href="#contact">Contato</a></li>
            </ul>
        </nav>
    </header>

    <!-- Banner -->
    <div class="banner">
        <img src="https://static.wixstatic.com/media/2a3147_c8560f648b0240eeb3738b79b6d4199a~mv2.png/v1/fill/w_808,h_576,al_c,q_90,usm_0.66_1.00_0.01,enc_avif,quality_auto/o%20in%C3%ADcio%20(9).png" alt="Banner do Portfólio">
        <div class="banner-overlay">
            <h1>João Guilherme (Raio)</h1>
            <h2>Desenvolvedor & Game Designer</h2>
        </div>
    </div>

    <!-- Color Palette -->
    <section id="palette">
        <h2 class="section-title">🎨 Paleta de Cores</h2>
        <p>O site utiliza uma paleta de cores baseada em tons de ciano/verde, transmitindo modernidade e criatividade:</p>
        <div class="color-palette">
            <div class="color-item color-primary">
                <p><strong>Cor Principal:</strong><br>rgb(32, 211, 91)</p>
            </div>
            <div class="color-item color-secondary">
                <p><strong>Cor Secundária:</strong><br>rgb(0, 160, 80)</p>
            </div>
            <div class="color-item color-highlight">
                <p><strong>Cor de Destaque:</strong><br>rgb(255, 255, 255)</p>
            </div>
            <div class="color-item color-bg">
                <p><strong>Cor de Fundo:</strong><br>rgb(0, 233, 116)</p>
            </div>
            <div class="color-item color-text">
                <p><strong>Cor de Texto:</strong><br>rgb(0, 0, 0)</p>
            </div>
        </div>
    </section>

    <!-- About Me -->
    <section id="about">
        <h2 class="section-title">👨‍💻 Sobre Mim</h2>
        <div class="about-content">
            <div class="about-text">
                <p>Olá! Eu sou João Guilherme, mas pode me chamar de Raio. Sou dono da <strong>Lorde Tempus</strong>, uma empresa apaixonada por criar experiências únicas em jogos de tabuleiro e digitais.</p>
                
                <p>Nascido em Porto Velho, Rondônia, sempre fui movido pela paixão por jogos e pela criatividade. Essa energia me acompanhou até São Paulo, onde decidi mergulhar de cabeça no universo dos games e na criação de conteúdo.</p>
                
                <p>Hoje, estabelecido em João Pessoa, sigo firme na missão de inovar com a <strong>Lorde Tempus</strong>, conciliando minha trajetória empreendedora com os desafios e aprendizados do curso de Ciências da Computação.</p>
                
                <p>Minha jornada é marcada por coragem, resiliência e uma busca constante por unir a arte dos jogos com a precisão da tecnologia.</p>
            </div>
            <div class="about-info">
                <div class="info-item">
                    <h3>Nome:</h3>
                    <p>João Guilherme (Raio)</p>
                </div>
                <div class="info-item">
                    <h3>Empresa:</h3>
                    <p>Lorde Tempus</p>
                </div>
                <div class="info-item">
                    <h3>Localização:</h3>
                    <p>João Pessoa, PB</p>
                </div>
                <div class="info-item">
                    <h3>Email:</h3>
                    <p>Raiokan3223br@gmail.com</p>
                </div>
                <div class="info-item">
                    <h3>Discord:</h3>
                    <p>raiokan</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills -->
    <section id="skills">
        <h2 class="section-title">🛠️ Habilidades</h2>
        <div class="skills-container">
            <div class="skill-category">
                <h3>Desenvolvimento de Jogos</h3>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Game Design</span>
                        <span>95%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 95%"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Balanceamento</span>
                        <span>90%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 90%"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Narrativa</span>
                        <span>85%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 85%"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Prototipagem</span>
                        <span>80%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 80%"></div>
                    </div>
                </div>
            </div>
            
            <div class="skill-category">
                <h3>Programação</h3>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>HTML/CSS</span>
                        <span>85%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 85%"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>JavaScript</span>
                        <span>75%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 75%"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Python</span>
                        <span>70%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 70%"></div>
                    </div>
                </div>
            </div>
            
            <div class="skill-category">
                <h3>Soft Skills</h3>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Liderança</span>
                        <span>90%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 90%"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Criatividade</span>
                        <span>95%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 95%"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Resolução de Problemas</span>
                        <span>85%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 85%"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Comunicação</span>
                        <span>90%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 90%"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects -->
    <section id="projects">
        <h2 class="section-title">🎮 Projetos</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-content">
                    <h3>Sistema de RPG Personalizado</h3>
                    <p>Um sistema de RPG de mesa com regras personalizadas.</p>
                    <div class="project-tags">
                        <span class="tag">RPG</span>
                        <span class="tag">Game Design</span>
                        <span class="tag">Narrativa</span>
                    </div>
                </div>
            </div>
            
            <div class="project-card">
                <div class="project-content">
                    <h3>Estratégia Medieval</h3>
                    <p>Jogo de tabuleiro estratégico ambientado na era medieval com mecânicas inovadoras.</p>
                    <div class="project-tags">
                        <span class="tag">Tabuleiro</span>
                        <span class="tag">Estratégia</span>
                        <span class="tag">Medieval</span>
                    </div>
                </div>
            </div>
            
            <div class="project-card">
                <div class="project-content">
                    <h3>Aventura Fantástica</h3>
                    <p>Jogo digital de aventura com elementos de RPG e mundo aberto.</p>
                    <div class="project-tags">
                        <span class="tag">Digital</span>
                        <span class="tag">Aventura</span>
                    </div>
                </div>
            </div>
            
            <div class="project-card">
                <div class="project-content">
                    <h3>Assistente de Mestre</h3>
                    <p>Aplicativo para auxiliar mestres de RPG na gestão de campanhas e sessões.</p>
                    <div class="project-tags">
                        <span class="tag">Digital</span>
                        <span class="tag">RPG</span>
                        <span class="tag">Ferramenta</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience -->
    <section id="experience">
        <h2 class="section-title">💼 Experiência Profissional</h2>
        <div class="timeline">
            <div class="timeline-item">
                <div class="timeline-dot"></div>
                <div class="timeline-content">
                    <div class="timeline-date">2022 - Presente</div>
                    <h3>Dono & CEO</h3>
                    <h4>Lorde Tempus</h4>
                    <p>Gestão da empresa especializada em desenvolvimento de jogos de tabuleiro e digitais. Responsável pela direção criativa, desenvolvimento de produtos e estratégias de negócio.</p>
                </div>
            </div>
            
            <div class="timeline-item">
                <div class="timeline-dot"></div>
                <div class="timeline-content">
                    <div class="timeline-date">2019 - Presente</div>
                    <h3>Mestre de RPG Profissional</h3>
                    <h4>Eventos e Lojas Especializadas</h4>
                    <p>Condução de sessões de RPG para grupos diversos, criação de campanhas personalizadas e ensino das regras para novos jogadores. Participação em eventos e convenções de jogos.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Education -->
    <section id="education">
        <h2 class="section-title">🎓 Formação Acadêmica</h2>
        <div class="education-item">
            <h3>Bacharelado em Ciências da Computação</h3>
            <h4>UNIESP | 2025 - Presente</h4>
            <p>Foco em desenvolvimento de software, inteligência artificial e computação gráfica aplicada a jogos.</p>
        </div>
    </section>

    <!-- RPG and Computing -->
    <section id="rpg">
        <h2 class="section-title">🎲 RPG de Mesa e Ciências da Computação</h2>
        <div class="rpg-section">
            <p>O RPG de mesa é uma forma de jogo interativo onde os jogadores assumem personagens fictícios em um mundo imaginário, criando histórias e aventuras de forma colaborativa. Esse tipo de jogo envolve uma narrativa orientada por regras, com o auxílio de dados, mapas e outros materiais, proporcionando uma experiência imersiva que valoriza a criatividade e a tomada de decisões.</p>
            
            <p>Ao unir o RPG de mesa com as Ciências da Computação, surgem diversas possibilidades inovadoras:</p>
            
            <ul class="rpg-list">
                <li>
                    <span class="rpg-list-title">Automatizar e Personalizar Regras:</span>
                    <span>Sistemas digitais podem auxiliar no gerenciamento das regras do jogo, automatizando cálculos e monitorando estatísticas dos personagens.</span>
                </li>
                <li>
                    <span class="rpg-list-title">Criação de Mundos Dinâmicos:</span>
                    <span>Algoritmos de geração procedural criam cenários e desafios únicos a cada sessão, enriquecendo a experiência narrativa.</span>
                </li>
                <li>
                    <span class="rpg-list-title">Integração com Tecnologias Imersivas:</span>
                    <span>Ferramentas digitais, aplicativos e realidade virtual podem tornar o RPG mais interativo e acessível.</span>
                </li>
                <li>
                    <span class="rpg-list-title">Ferramentas para Mestres de Jogo:</span>
                    <span>Softwares especializados ajudam a organizar campanhas, criar mapas interativos e gerenciar a narrativa.</span>
                </li>
            </ul>
            
            <p>Essa fusão entre RPG de mesa e Ciências da Computação transforma uma simples sessão de jogo em uma experiência enriquecida, que alia tradição e modernidade, potencializando a criatividade dos jogadores e ampliando as possibilidades de inovação.</p>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact">
        <h2 class="section-title">📱 Contato</h2>
        <div class="contact-container">
            <div class="contact-info">
                <div class="contact-item">
                    <div class="contact-icon">📍</div>
                    <div>
                        <h3>Localização</h3>
                        <p>João Pessoa, Paraíba, Brasil</p>
                    </div>
                </div>
                
                <div class="contact-item">
                    <div class="contact-icon">✉️</div>
                    <div>
                        <h3>Email</h3>
                        <p>Raiokan3223br@gmail.com</p>
                    </div>
                </div>
                
                <div class="contact-item">
                    <div class="contact-icon">💬</div>
                    <div>
                        <h3>Discord</h3>
                        <p>raiokan</p>
                    </div>
                </div>
                
                <h3>Redes Sociais</h3>
                <div class="social-icons">
                    <a href="#" class="social-icon">📷</a>
                    <a href="#" class="social-icon">🐦</a>
                    <a href="#" class="social-icon">💼</a>
                    <a href="#" class="social-icon">🐙</a>
                    <a href="#" class="social-icon">👾</a>
                </div>
            </div>
            
            <div class="contact-form">
                <h3>Envie uma Mensagem</h3>
                <form>
                    <div class="form-group">
                        <label for="name">Nome</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="subject">Assunto</label>
                        <input type="text" id="subject" name="subject" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Mensagem</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Enviar Mensagem</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Technologies -->
    <section id="technologies">
        <h2 class="section-title">🚀 Tecnologias Utilizadas</h2>
        <p>Este portfólio foi desenvolvido utilizando exclusivamente:</p>
        <div class="tech-container">
            <span class="tech-badge">HTML5</span>
            <span class="tech-badge">CSS3</span>
        </div>
        <p>Sem o uso de frameworks ou bibliotecas externas, demonstrando o domínio das tecnologias fundamentais da web.</p>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2023 Lorde Tempus. Todos os direitos reservados.</p>
        <p>Desenvolvido por João Guilherme (Raio)</p>
    </footer>
</body>
</html>
