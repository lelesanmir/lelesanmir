<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Leonardo Miranda - GitHub</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }

        .readme-container {
            max-width: 950px;
            border-top-right-radius: 4%;
            border-top-left-radius: 4%;
            border-bottom-left-radius: 4%;
            border-bottom-right-radius: 4%;
            margin: 0 auto;
            background-color: rgb(5, 0, 2);
            font-family: sans-serif;
            color: #325072;
            padding: 20px; /* Adicionei padding para melhor espaçamento */
        }

        h1, h2 {
            text-align: center;
            color: #325072;
        }

        p {
            margin: 8px;
        }

        a {
            display: flex;
            text-decoration: none;
            color: #325072;
        }

        a:hover {
            text-decoration: underline;
        }

        .profile-image {
            border-radius: 50%;
            width: 150px;
            height: 150px;
            margin: 20px auto;
            display: block;
        }

        button {
            background-color: #2c3e50;
            color: white;
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #34495e;
        }
    </style>
</head>
<body>

    

    <div class="readme-container">
        <button onclick="changeLanguage()">Mudar o Idioma</button>
        <img src="./img/leonardo.jpg" alt="Sua Imagem" class="profile-image">
        <h1 id="about-me">Sobre Mim</h1>
        <p id="about-me-text">Sou graduado em Análise e Desenvolvimento de Sistemas, atualmente focado em estudos e cursos para aprimorar minhas habilidades. Embora minha jornada profissional ainda esteja em fase inicial, venho dedicando esforços à realização de projetos significativos como parte do meu aprendizado contínuo.
            <br> Meus projetos variam de Java, PHP, JavaScript, React, Typescript, e envolvem bancos de dados PostgreSQL e MySQL.
            <br>Meus projetos mais básicos são de níveis acadêmicos e refletem meu aprendizado ao longo do tempo.</p>

        <h2 id="projects">Projetos</h2>
        <ul>
            <li><a href="https://github.com/lelesanmir/projeto-senac.git">projeto-senac</a></li>
            <li><a href="https://github.com/lelesanmir/collection-filmes.git">collection-filmes</a></li>
            <li><a href="https://github.com/lelesanmir/app-pedidos-pizzaStar.git">App de Pizzaria</a></li>
            <li><a href="https://github.com/lelesanmir/linksredessociais.git">Links para contatos</a></li>
        </ul>

        <h2 id="technologies">Tecnologias</h2>
        <ul>
            <li>Java</li>
            <li>TipeScript</li>
            <li>React</li>
            <li>NodeJS</li>
            <li>JavaScript</li>
            <li>Php</li>
            <li>Git e GitHub</li><br>
        </ul>
    </div>

    <script>
        const translations = {
    'pt-BR': {
        'about-me': 'Sobre Mim',
        'about-me-text': 'Sou graduado em Análise e Desenvolvimento de Sistemas, atualmente focado em estudos e cursos para aprimorar minhas habilidades. Embora minha jornada profissional ainda esteja em fase inicial, venho dedicando esforços à realização de projetos significativos como parte do meu aprendizado contínuo.',
        'projects': 'Projetos',
        'technologies': 'Tecnologias',
        'toggle-language': 'Mudar o Idioma'
    },
    'en-US': {
        'about-me': 'About Me',
        'about-me-text': 'I am a graduate in Analysis and Systems Development, currently focused on studies and courses to enhance my skills. Although my professional journey is still in its early stages, I have been dedicating efforts to the completion of significant projects as part of my continuous learning.',
        'projects': 'Projects',
        'technologies': 'Technologies',
        'toggle-language': 'Toggle Language'
    }
};

function changeLanguage() {
    var currentLang = document.documentElement.lang;
    var newLang = (currentLang === "pt-BR") ? "en-US" : "pt-BR";

    document.documentElement.lang = newLang;
    updateTranslations(newLang);
    updateLanguageButton(newLang);
}

function updateTranslations(lang) {
    Object.keys(translations[lang]).forEach(function(key) {
        var element = document.getElementById(key);
        if (element) {
            element.innerHTML = translations[lang][key];
        }
    });
}

function updateLanguageButton(lang) {
    var languageButton = document.getElementById('languageButton');
    if (languageButton) {
        languageButton.textContent = translations[lang]['toggle-language'];
    }
}

// Chamada inicial para garantir que o botão esteja correto ao carregar a página
updateLanguageButton(document.documentElement.lang);

    </script>
</body>
</html>

