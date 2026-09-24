<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Currículo Vitae - Vitor Gabriel Souza dos Santos</title>
    
    <!-- Fonte Google Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

    <style>
        :root {
            /* Tema Roxo Principal (Light Mode) */
            --bg-body: #f3f0ff;
            --bg-sidebar: #2e1065;
            --text-sidebar: #f5f3ff;
            --text-sidebar-muted: #c4b5fd;
            --bg-content: #ffffff;
            --text-main: #1e1b4b;
            --text-muted: #4c1d95;
            --primary: #7c3aed;
            --primary-hover: #6d28d9;
            --primary-light: #f3e8ff;
            --border-color: #e9d5ff;
            --card-bg: #faf5ff;
            --accent: #a855f7;
            --shadow: 0 10px 25px -5px rgba(124, 58, 237, 0.12), 0 8px 10px -6px rgba(124, 58, 237, 0.08);
            --radius: 16px;
            --transition: all 0.3s ease;
        }

        /* Tema Escuro */
        body.dark-mode {
            --bg-body: #0f0728;
            --bg-sidebar: #130938;
            --text-sidebar: #f5f3ff;
            --text-sidebar-muted: #a78bfa;
            --bg-content: #1a0b2e;
            --text-main: #f5f3ff;
            --text-muted: #ddd6fe;
            --primary: #a855f7;
            --primary-hover: #c084fc;
            --primary-light: rgba(168, 85, 247, 0.15);
            --border-color: #3b0764;
            --card-bg: #240e42;
            --shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.5);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-body);
            color: var(--text-main);
            line-height: 1.6;
            transition: var(--transition);
        }

        /* Barra Superior de Diagnóstico Responsivo */
        .debug-bar {
            background-color: #1e0e4a;
            color: #ffffff;
            padding: 10px 20px;
            font-size: 0.85rem;
            text-align: center;
            font-weight: 600;
            position: sticky;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 2px solid var(--accent);
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }

        .debug-badge {
            background-color: var(--accent);
            color: #ffffff;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.75rem;
            text-transform: uppercase;
            font-weight: 800;
            letter-spacing: 0.5px;
        }

        .action-btns {
            display: flex;
            gap: 10px;
        }

        .btn-tool {
            background-color: rgba(255, 255, 255, 0.12);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: white;
            padding: 6px 14px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.8rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: var(--transition);
        }

        .btn-tool:hover {
            background-color: var(--primary);
            border-color: var(--accent);
        }

        .cv-container {
            max-width: 1050px;
            margin: 2rem auto;
            background-color: var(--bg-content);
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            overflow: hidden;
            display: flex;
            min-height: 850px;
            transition: var(--transition);
            border: 1px solid var(--border-color);
        }

        /* BARRA LATERAL ROXA */
        .sidebar {
            width: 320px;
            background: linear-gradient(180deg, var(--bg-sidebar) 0%, #1e0e3e 100%);
            color: var(--text-sidebar);
            padding: 2.5rem 1.8rem;
            flex-shrink: 0;
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        /* CONTEÚDO PRINCIPAL */
        .main-content {
            flex: 1;
            padding: 3rem 2.5rem;
            display: flex;
            flex-direction: column;
            gap: 2.2rem;
            background-color: var(--bg-content);
        }

        .profile-container {
            text-align: center;
            position: relative;
        }

        .avatar-wrapper {
            position: relative;
            width: 140px;
            height: 140px;
            margin: 0 auto 1.2rem auto;
        }

        .avatar-img {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--accent);
            box-shadow: 0 8px 20px rgba(168, 85, 247, 0.3);
            display: block;
            background-color: #240e42;
        }

        .upload-btn-label {
            position: absolute;
            bottom: 0;
            right: 0;
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            width: 36px;
            height: 36px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0,0,0,0.3);
            border: 2px solid white;
            transition: var(--transition);
        }

        .upload-btn-label:hover {
            background-color: var(--accent);
            transform: scale(1.1);
        }

        #file-input {
            display: none;
        }

        .profile-name {
            font-size: 1.35rem;
            font-weight: 800;
            color: #ffffff;
            margin-bottom: 0.3rem;
            line-height: 1.25;
        }

        .profile-title {
            color: var(--text-sidebar-muted);
            font-size: 0.9rem;
            font-weight: 500;
        }

        .sidebar-title {
            font-size: 0.95rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--accent);
            margin-bottom: 1rem;
            border-bottom: 1px solid rgba(168, 85, 247, 0.25);
            padding-bottom: 0.4rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .contact-list {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 0.9rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 0.88rem;
            color: var(--text-sidebar);
            word-break: break-word;
        }

        .contact-icon {
            width: 18px;
            height: 18px;
            fill: var(--accent);
            flex-shrink: 0;
        }

        .badge-container {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .badge {
            background-color: rgba(168, 85, 247, 0.2);
            border: 1px solid rgba(168, 85, 247, 0.3);
            color: #ffffff;
            padding: 6px 12px;
            border-radius: 8px;
            font-size: 0.82rem;
            font-weight: 500;
        }

        .skills-list {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 0.6rem;
        }

        .skill-tag {
            background-color: rgba(255, 255, 255, 0.08);
            padding: 8px 12px;
            border-radius: 8px;
            font-size: 0.85rem;
            color: var(--text-sidebar);
            display: flex;
            align-items: center;
            gap: 10px;
            border-left: 3px solid var(--accent);
        }

        .section-header {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 1.2rem;
            border-bottom: 2px solid var(--border-color);
            padding-bottom: 0.6rem;
        }

        .section-header h2 {
            font-size: 1.25rem;
            color: var(--primary);
            text-transform: uppercase;
            letter-spacing: 0.5px;
            font-weight: 800;
        }

        .section-icon-svg {
            width: 22px;
            height: 22px;
            fill: var(--primary);
        }

        .summary-text {
            color: var(--text-muted);
            font-size: 0.98rem;
            line-height: 1.7;
            background-color: var(--card-bg);
            padding: 1.2rem;
            border-radius: 12px;
            border-left: 4px solid var(--primary);
        }

        /* SEÇÃO DE LINGUAGENS E TECNOLOGIAS */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 1.2rem;
        }

        .tech-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 1rem 1.2rem;
            transition: var(--transition);
        }

        .tech-card:hover {
            transform: translateY(-2px);
            border-color: var(--primary);
            box-shadow: var(--shadow);
        }

        .tech-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 0.5rem;
        }

        .tech-name {
            font-weight: 700;
            font-size: 0.95rem;
            color: var(--text-main);
        }

        .tech-level {
            font-size: 0.75rem;
            font-weight: 700;
            color: var(--primary);
            text-transform: uppercase;
        }

        .progress-bar-bg {
            width: 100%;
            height: 8px;
            background-color: rgba(124, 58, 237, 0.15);
            border-radius: 10px;
            overflow: hidden;
        }

        .progress-bar-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--primary) 0%, var(--accent) 100%);
            border-radius: 10px;
        }

        /* TIMELINE (FORMAÇÃO ACADÊMICA) */
        .timeline {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
            position: relative;
            padding-left: 1.2rem;
            border-left: 2px solid var(--border-color);
        }

        .timeline-item {
            position: relative;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -1.65rem;
            top: 5px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: var(--primary);
            border: 3px solid var(--bg-content);
        }

        .item-title {
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--text-main);
        }

        .item-subtitle {
            font-size: 0.92rem;
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 0.3rem;
        }

        .item-date {
            font-size: 0.8rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
            display: inline-block;
            background-color: var(--primary-light);
            padding: 3px 10px;
            border-radius: 6px;
            font-weight: 600;
        }

        .item-desc {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        /* GRID DE COMPETÊNCIAS */
        .competencies-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }

        .comp-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            padding: 1rem;
            border-radius: 10px;
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--text-main);
            transition: var(--transition);
        }

        .comp-card:hover {
            transform: translateY(-2px);
            border-color: var(--primary);
            box-shadow: var(--shadow);
        }

        .comp-bullet {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background-color: var(--primary);
            flex-shrink: 0;
        }

        /* BREAKPOINTS RESPONSIVOS */
        @media screen and (max-width: 850px) {
            .cv-container {
                flex-direction: column;
                margin: 0;
                border-radius: 0;
            }

            .sidebar {
                width: 100%;
                padding: 2rem 1.5rem;
            }

            .main-content {
                padding: 2rem 1.5rem;
            }
        }

        @media screen and (max-width: 500px) {
            .debug-bar {
                flex-direction: column;
                gap: 8px;
                padding: 10px;
            }

            .competencies-grid, .tech-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <div class="debug-bar">
        <div>
            <span>Breakpoint Atual: </span>
            <span class="debug-badge" id="screen-info">Carregando...</span>
        </div>
        <div class="action-btns">
            <button class="btn-tool" onclick="toggleDarkMode()">
                <!-- Ícone SVG de Sol/Lua -->
                <svg id="theme-svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path></svg>
                <span id="theme-text">Modo Escuro</span>
            </button>
        </div>
    </div>

    <div class="cv-container">

        <!-- BARRA LATERAL (FOTO E CONTATOS) -->
        <aside class="sidebar">
            
            <div class="profile-container">
                <div class="avatar-wrapper">
                    <img id="profile-img" src="C:\Users\Mary\Documents\.vscode\WhatsApp Image 2026-08-20 at 13.23.27.jpeg" alt="Foto de Vitor Gabriel Souza dos Santos" class="avatar-img">
                    <label for="file-input" class="upload-btn-label" title="Carregar sua Foto">
                        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2z"></path><circle cx="12" cy="13" r="4"></circle></svg>
                    </label>
                    <input type="file" id="file-input" accept="image/*" onchange="previewImage(event)">
                </div>
                <h1 class="profile-name">VITOR GABRIEL SOUZA DOS SANTOS</h1>
                <p class="profile-title">Estudante de Sistemas de Informação</p>
            </div>

            <!-- Dados de Contato com SVG -->
            <div>
                <h3 class="sidebar-title">Contato</h3>
                <ul class="contact-list">
                    <li class="contact-item">
                        <svg class="contact-icon" viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
                        Avenida Amélia Amado, Itabuna - BA[cite: 2]
                    </li>
                    <li class="contact-item">
                        <svg class="contact-icon" viewBox="0 0 24 24"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
                        (73) 98202-5497[cite: 2]
                    </li>
                    <li class="contact-item">
                        <svg class="contact-icon" viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
                        vg6588944@gmail.com[cite: 2]
                    </li>
                </ul>
            </div>

            <!-- Idiomas -->
            <div>
                <h3 class="sidebar-title">Idiomas</h3>
                <ul class="skills-list">
                    <li class="skill-tag">Português (Nativo)</li>
                    <li class="skill-tag">Inglês (Intermediário)</li>
                </ul>
            </div>

            <!-- Certificados -->
            <div>
                <h3 class="sidebar-title">Certificados</h3>
                <div class="badge-container">
                    <span class="badge">Logística</span>
                    <span class="badge">Informática Intermediária</span>
                    <span class="badge">Pacote Office</span>
                </div>
            </div>

            <!-- Atributos -->
            <div>
                <h3 class="sidebar-title">Atributos Profissionais</h3>
                <ul class="skills-list">
                    <li class="skill-tag">Proatividade</li>
                    <li class="skill-tag">Boa Comunicação</li>
                    <li class="skill-tag">Aprendizado Contínuo</li>
                    <li class="skill-tag">Organização e Gestão</li>
                </ul>
            </div>

        </aside>

        <main class="main-content">

            <!-- Resumo -->
            <section>
                <div class="section-header">
                    <svg class="section-icon-svg" viewBox="0 0 24 24"><path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/></svg>
                    <h2>Resumo Profissional</h2>
                </div>
                <p class="summary-text">
                    Tenho facilidade para aprender novas atividades, sou organizado, responsável e gosto de trabalhar em equipe. Possuo boa comunicação e busco uma oportunidade para desenvolver experiência profissional e contribuir com a empresa.
                </p>
            </section>

            <!-- Seção de Linguagens de Programação e Tecnologias -->
            <section>
                <div class="section-header">
                    <svg class="section-icon-svg" viewBox="0 0 24 24"><path d="M9.4 16.6L4.8 12l4.6-4.6L8 6l-6 6 6 6 1.4-1.4zm5.2 0l4.6-4.6-4.6-4.6L16 6l6 6-6 6-1.4-1.4z"/></svg>
                    <h2>Linguagens & Tecnologias</h2>
                </div>
                <div class="tech-grid">
                    
                    <div class="tech-card">
                        <div class="tech-info">
                            <span class="tech-name">HTML5 / CSS3</span>
                            <span class="tech-level">Intermediário</span>
                        </div>
                        <div class="progress-bar-bg">
                            <div class="progress-bar-fill" style="width: 75%;"></div>
                        </div>
                    </div>

                    <div class="tech-card">
                        <div class="tech-info">
                            <span class="tech-name">JavaScript</span>
                            <span class="tech-level">Intermediário</span>
                        </div>
                        <div class="progress-bar-bg">
                            <div class="progress-bar-fill" style="width: 65%;"></div>
                        </div>
                    </div>

                    <div class="tech-card">
                        <div class="tech-info">
                            <span class="tech-name">Python</span>
                            <span class="tech-level">Básico / Intermediário</span>
                        </div>
                        <div class="progress-bar-bg">
                            <div class="progress-bar-fill" style="width: 60%;"></div>
                        </div>
                    </div>

                    <div class="tech-card">
                        <div class="tech-info">
                            <span class="tech-name">C / C++</span>
                            <span class="tech-level">Básico</span>
                        </div>
                        <div class="progress-bar-bg">
                            <div class="progress-bar-fill" style="width: 50%;"></div>
                        </div>
                    </div>

                    <div class="tech-card">
                        <div class="tech-info">
                            <span class="tech-name">SQL / Banco de Dados</span>
                            <span class="tech-level">Básico</span>
                        </div>
                        <div class="progress-bar-bg">
                            <div class="progress-bar-fill" style="width: 55%;"></div>
                        </div>
                    </div>

                    <div class="tech-card">
                        <div class="tech-info">
                            <span class="tech-name">Git / GitHub</span>
                            <span class="tech-level">Básico</span>
                        </div>
                        <div class="progress-bar-bg">
                            <div class="progress-bar-fill" style="width: 60%;"></div>
                        </div>
                    </div>

                </div>
            </section>

            <!-- Formação Acadêmica -->
            <section>
                <div class="section-header">
                    <svg class="section-icon-svg" viewBox="0 0 24 24"><path d="M5 13.18v4L12 21l7-3.82v-4L12 17l-7-3.82zM12 3L1 9l11 6 9-4.91V17h2V9L12 3z"/></svg>
                    <h2>Formação Acadêmica</h2>
                </div>
                <div class="timeline">
                    
                    <div class="timeline-item">
                        <h3 class="item-title">Bacharelado em Sistemas de Informação</h3>
                        <div class="item-subtitle">Unex - Centro Universitário de Excelência (Itabuna)</div>
                        <span class="item-date">03/2026 - 03/2030 • Cursando</span>
                        <p class="item-desc">Formação superior focada em desenvolvimento de software, algoritmos, arquitetura de computadores e governança de tecnologia.</p>
                    </div>

                    <div class="timeline-item">
                        <h3 class="item-title">Ensino Médio: Formação Geral Básica</h3>
                        <div class="item-subtitle">Colégio Estadual Idelzito Eloy de Abréu (Ituberá)</div>
                        <span class="item-date">02/2023 - 12/2025 • Concluído</span>
                        <p class="item-desc">Conclusão do ensino médio com qualificação geral e bases fundamentais de raciocínio lógico.</p>
                    </div>

                </div>
            </section>

            <!-- Habilidades e Competências -->
            <section>
                <div class="section-header">
                    <svg class="section-icon-svg" viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-2 10h-4v4h-2v-4H7v-2h4V7h2v4h4v2z"/></svg>
                    <h2>Habilidades & Competências</h2>
                </div>
                <div class="competencies-grid">
                    <div class="comp-card">
                        <div class="comp-bullet"></div>
                        <span>Boa Comunicação</span>
                    </div>
                    <div class="comp-card">
                        <div class="comp-bullet"></div>
                        <span>Trabalho em Equipe</span>
                    </div>
                    <div class="comp-card">
                        <div class="comp-bullet"></div>
                        <span>Capacidade de Aprendizado</span>
                    </div>
                    <div class="comp-card">
                        <div class="comp-bullet"></div>
                        <span>Proatividade</span>
                    </div>
                    <div class="comp-card">
                        <div class="comp-bullet"></div>
                        <span>Organização & Tempo</span>
                    </div>
                    <div class="comp-card">
                        <div class="comp-bullet"></div>
                        <span>Responsabilidade e Ética</span>
                    </div>
                    <div class="comp-card">
                        <div class="comp-bullet"></div>
                        <span>Disciplina e Normas</span>
                    </div>
                </div>
            </section>

        </main>

    </div>

    <script>
        // Atualizador de indicador do tamanho de tela / breakpoint
        function updateScreenDebugInfo() {
            const width = window.innerWidth;
            const infoBadge = document.getElementById('screen-info');
            
            if (width < 500) {
                infoBadge.textContent = `Mobile Pequeno (${width}px)`;
                infoBadge.style.backgroundColor = '#ec4899';
            } else if (width < 850) {
                infoBadge.textContent = `Tablet / Mobile Largo (${width}px)`;
                infoBadge.style.backgroundColor = '#a855f7';
            } else {
                infoBadge.textContent = `Desktop (${width}px)`;
                infoBadge.style.backgroundColor = '#7c3aed';
            }
        }

        window.addEventListener('load', updateScreenDebugInfo);
        window.addEventListener('resize', updateScreenDebugInfo);

        // Função para alternar modo claro e escuro
        function toggleDarkMode() {
            const body = document.body;
            body.classList.toggle('dark-mode');
            
            const isDark = body.classList.contains('dark-mode');
            document.getElementById('theme-text').textContent = isDark ? 'Modo Claro' : 'Modo Escuro';
        }

        // Carregar foto escolhida pelo usuário
        function previewImage(event) {
            const reader = new FileReader();
            reader.onload = function(){
                const output = document.getElementById('profile-img');
                output.src = reader.result;
            };
            if(event.target.files[0]) {
                reader.readAsDataURL(event.target.files[0]);
            }
        }
    </script>
</body>
</html>
