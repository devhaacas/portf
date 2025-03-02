<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfólio - HAAC</title>
    <link href="https://fonts.googleapis.com/css2?family=Exo:wght@400;600&display=swap" rel="stylesheet">
    <meta name="description" content="Portfólio de HAAC, desenvolvedor Mobile e designer gráfico.">
    <style>
        /* Estilo Geral */
        body {
            margin: 0;
            font-family: 'Exo', sans-serif;
            background-color: #1E1E1E;
            color: white;
            overflow-x: hidden;
        }

        /* Botão do Menu */
        .menu-button {
            position: fixed;
            top: 20px;
            left: 20px;
            background: none;
            border: none;
            font-size: 24px;
            color: white;
            cursor: pointer;
            z-index: 1000;
            transition: opacity 0.3s ease;
        }

        .menu-button.hidden {
            opacity: 0.5;
        }

        /* Menu Lateral */
        .menu {
            position: fixed;
            top: 0;
            left: -250px;
            width: 250px;
            height: 100vh;
            background-color: #101010;
            padding-top: 50px;
            transition: left 0.3s ease-in-out, opacity 0.3s ease-in-out;
            opacity: 0;
            z-index: 999;
        }

        .menu.show {
            left: 0;
            opacity: 1;
        }

        .menu a {
            display: block;
            color: white;
            text-decoration: none;
            padding: 15px;
            border-bottom: 1px solid #333;
            transition: background 0.3s;
        }

        .menu a:hover {
            background: #52C6C6;
        }

        /* Botão de Fechar Menu */
        .close-menu {
            position: absolute;
            top: 10px;
            right: 10px;
            background: none;
            border: none;
            font-size: 20px;
            color: white;
            cursor: pointer;
        }

        /* Conteúdo Principal */
        .content {
            width: 100%;
            text-align: center;
            transition: margin-left 0.3s;
        }

        /* Header com Vídeo */
        header {
            width: 100%;
            text-align: center;
        }

        header video {
            width: 100%;
            max-height: 300px;
            object-fit: cover;
        }

        /* Seções */
        section {
            padding: 50px;
            text-align: center;
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.5s ease-out, transform 0.5s ease-out;
        }

        section.show {
            opacity: 1;
            transform: translateY(0);
        }

        h2 {
            color: #52C6C6;
        }

        /* Sobre Mim */
        .about-text {
            max-width: 800px;
            margin: auto;
            font-size: 18px;
            line-height: 1.6;
        }

        /* Barra de Habilidades */
        .skill {
            margin: 20px auto;
            width: 80%;
        }

        .progress {
            width: 100%;
            background-color: #444;
            border-radius: 10px;
            height: 25px;
            overflow: hidden;
        }

        .progress-bar {
            height: 25px;
            background-color: #52C6C6;
            text-align: center;
            line-height: 25px;
            font-weight: bold;
            width: 0;
            transition: width 2s ease-in-out;
        }

        /* Tabela de Projetos */
        table {
            width: 80%;
            margin: 20px auto;
            border-collapse: collapse;
            background-color: #222;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.5);
        }

        table, th, td {
            border: 1px solid #52C6C6;
            padding: 15px;
            text-align: center;
        }

        th {
            background-color: #333;
        }

        /* Contato */
        #contato p {
            font-size: 18px;
        }

        /* Rodapé */
        footer {
            background-color: #101010;
            text-align: center;
            padding: 20px;
        }

        footer .social img {
            width: 40px;
            margin: 0 10px;
        }

        footer .social a {
            text-decoration: none;
        }
    </style>
</head>
<body>

    <!-- Botão do Menu -->
    <button class="menu-button" id="menu-button" onclick="toggleMenu()">☰</button>

    <!-- Menu Lateral -->
    <nav class="menu" id="menu">
        <button class="close-menu" onclick="toggleMenu()">×</button>
        <a href="#sobre">Sobre Mim</a>
        <a href="#habilidades">Habilidades</a>
        <a href="#projetos">Projetos</a>
        <a href="#contato">Contato</a>
    </nav>

    <div class="content">
        <header id="header">
            <video autoplay loop muted>
                <source src="Sapo./vidro.mp4" type="video/mp4">   
            </video>
        </header>

        <section id="sobre">
            <h2>Sobre Mim</h2>
            <div class="about-text">
                <p>Sou graduando em Análise e Desenvolvimento de Sistemas pela UniCesumar, apaixonado por tecnologia e inovação. Tenho experiência em desenvolvimento Mobile (Kotlin), além de habilidades em design gráfico e análise de sistemas.</p>
            </div>
        </section>

        <section id="habilidades">
            <h2>Minhas Habilidades</h2>
            <div class="skill">
                <p>Front-End: HTML,CSS,JS</p>
                <div class="progress"><div class="progress-bar" data-percent="90">0%</div></div>
            </div>
            <div class="skill">
                <p>SQL: Postgre, MongoDB</p>
                <div class="progress"><div class="progress-bar" data-percent="95">0%</div></div>
            </div>
            <div class="skill">
                <p>Python: Flask, Django</p>
                <div class="progress"><div class="progress-bar" data-percent="70">0%</div></div>
            </div>
            <div class="skill">
                <p>Microsoft Office:</p>
                <div class="progress"><div class="progress-bar" data-percent="95">0%</div></div>
            </div>
            <div class="skill">
                <p>Microsoft PowerBI:</p>
                <div class="progress"><div class="progress-bar" data-percent="80">0%</div></div>
            </div>
            <div class="skill">
                <p>Java: Spring Boot</p>
                <div class="progress"><div class="progress-bar" data-percent="30">0%</div></div>
            </div>
            <div class="skill">
                <p>Kotlin: Jetpack Compose</p>
                <div class="progress"><div class="progress-bar" data-percent="65">0%</div></div>
            </div>
            <div class="skill">
                <p>C#: Vb.NET</p>
                <div class="progress"><div class="progress-bar" data-percent="35">0%</div></div>
            </div>
            <div class="skill">
                <p>JavaScript: React, Angular</p>
                <div class="progress"><div class="progress-bar" data-percent="60">0%</div></div>
            </div>
            <div class="skill">
                <p>Ruby: ORM</p>
                <div class="progress"><div class="progress-bar" data-percent="20">0%</div></div>
            </div>
            <div class="skill">
                <p>Pentest</p>
                <div class="progress"><div class="progress-bar" data-percent="5">0%</div></div>
            </div>
        </section>

        <section id="projetos">
            <h2>Meus Projetos</h2>
            <table>
                <tr>
                    <th>Nome</th>
                    <th>Descrição</th>
                </tr>
                <tr>
                    <td>Projeto Shark-ira</td>
                    <td>Desenvolvimento de Bot Python</td>
                </tr>
                <tr>
                    <td>Designer Gráfico</td>
                    <td>Criação de Identidade Visual para organizações.</td>
                </tr>  
                <tr>
                    <td>CSE STORE</td>
                    <td>Aplicação Android para Dropshipping. (Kotlin)</td>
                </tr>                  
            </table>
        </section>

        <section id="contato">
            <h2>Contato</h2>
            <p>Email: haac777@gmail.com</p>
            <p>WhatsApp: (21)98404-7722</p>
        </section>

        <footer>
            <p>&copy; 2025 HAAC - Todos os direitos reservados</p>
            <div class="social">
                <a href="https://wa.me/+5521984047722" target="_blank"><img src="Sapo./zapzap.png" alt="WhatsApp"></a>
                <a href="https://linkedin.com/in/seu_perfil" target="_blank"><img src="Sapo./linkedinked.png" alt="LinkedIn"></a>
                <a href="https://github.com/seu_github" target="_blank"><img src="Sapo./github.png" alt="GitHub"></a>
            </div>
        </footer>
    </div>

    <script>
        function toggleMenu() {
            let menu = document.getElementById("menu");
            menu.classList.toggle("show");
        }

        document.addEventListener("scroll", function () {
            let sections = document.querySelectorAll("section");
            sections.forEach(section => {
                let rect = section.getBoundingClientRect();
                if (rect.top < window.innerHeight - 50) {
                    section.classList.add("show");
                }
            });

            document.querySelectorAll(".progress-bar").forEach(bar => {
                let percent = bar.getAttribute("data-percent");
                bar.style.width = percent + "%";
                bar.textContent = percent + "%";
            });
        });
    </script>
</body>
</html>