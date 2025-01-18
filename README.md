<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Википедия о Rust</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            color: white;
            text-align: center;
            overflow: auto;
            background-image: url('https://cdn.discordapp.com/attachments/1314225469419294780/1330182485333508216/image.png?ex=678d0c7a&is=678bbafa&hm=bb7bf5255dbd43905abd8bbdf4ab4d4ceba0a7e21345f9d86fd7c21386841a62');
            background-size: cover;
            background-attachment: fixed;
        }

        h1 {
            margin-top: 20px;
            animation: fadeIn 2s;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .link {
            position: absolute;
            top: 20px;
            left: 20px;
            padding: 10px 20px;
            background-color: #ff5722; /* Ало-красный цвет */
            color: white;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s;
            z-index: 1000;
        }

        .link:hover {
            background-color: #e64a19;
        }

        .content {
            background-color: rgba(0, 0, 0, 0.7);
            padding: 20px;
            border-radius: 10px;
            margin: 40px auto;
            max-width: 800px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }

        .header-image {
            margin: 20px 0;
            max-width: 100%;
            height: auto;
        }

        .category {
            margin: 20px 0;
        }

        .category h2 {
            margin: 10px 0;
        }

        .category img {
            width: 80%; /* Уменьшение размера изображений */
            height: auto;
            margin: 10px 0;
            border: 2px solid white;
            border-radius: 10px;
            transition: transform 0.3s;
            cursor: pointer; /* Указатель при наведении */
        }

        .category img:hover {
            transform: scale(1.05);
        }

        /* Гамбургер меню */
        .menu {
            display: none;
            flex-direction: column;
            position: absolute;
            top: 60px;
            right: 20px;
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 5px;
            padding: 10px;
            z-index: 1000;
        }

        .menu a {
            color: white;
            text-decoration: none;
            padding: 10px;
            display: block;
            transition: background-color 0.3s;
        }

        .menu a:hover {
            background-color: #ff5722;
        }

        .hamburger {
            cursor: pointer;
            position: absolute;
            top: 20px;
            right: 20px;
            z-index: 1000;
        }

        .hamburger div {
            width: 30px;
            height: 3px;
            background-color: white;
            margin: 5px;
            transition: all 0.3s;
        }

        .hamburger.active div:nth-child(1) {
            transform: rotate(45deg) translate(5px, 5px);
        }

        .hamburger.active div:nth-child(2) {
            opacity: 0;
        }

        .hamburger.active div:nth-child(3) {
            transform: rotate(-45deg) translate(5px, -5px);
        }

        .dev-section {
            margin-top: 40px;
        }

        .language-switch {
            position: absolute;
            top: 20px;
            right: 100px;
            padding: 10px;
            background-color: #ff5722; /* Ало-красный цвет */
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            z-index: 1000;
        }

        .language-switch:hover {
            background-color: #e64a19;
        }

        @keyframes backgroundChange {
            0% { background-image: url('https://cdn.discordapp.com/attachments/1314225469419294780/1330182485333508216/image.png?ex=678d0c7a&is=678bbafa&hm=bb7bf5255dbd43905abd8bbdf4ab4d4ceba0a7e21345f9d86fd7c21386841a62'); }
        }

        body {
            animation: backgroundChange 15s infinite;
        }

        /* Модальное окно */
        .modal {
            display: none; /* Скрыто по умолчанию */
            position: fixed;
            z-index: 1001;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.9); /* Полупрозрачный фон */
        }

        .modal-content {
            margin: auto;
            display: block;
            width: 80%;
            max-width: 700px;
        }

        .close {
            position: absolute;
            top: 20px;
            right: 35px;
            color: white;
            font-size: 40px;
            font-weight: bold;
            transition: 0.3s;
        }

        .close:hover,
        .close:focus {
            color: #bbb;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <a class="link" href="https://store.steampowered.com/app/252490/Rust/" target="_blank">Ссылка на игру в Steam</a>
    <button class="language-switch" onclick="switchLanguage()">EN</button>

    <div class="hamburger" onclick="toggleMenu()">
        <div></div>
        <div></div>
        <div></div>
    </div>

    <div class="menu" id="menu">
        <a href="https://twitter.com/playrust" target="_blank">Twitter</a>
        <a href="https://www.facebook.com/playrust" target="_blank">Facebook</a>
        <a href="https://www.instagram.com/playrust" target="_blank">Instagram</a>
        <a href="https://www.reddit.com/r/playrust/" target="_blank">Reddit</a>
    </div>

    <div class="content">
        <h1>Википедия о Rust</h1>
        <img class="header-image" src="https://cdn.discordapp.com/attachments/1314225469419294780/1330183645377335357/latest.png?ex=678d0d8e&is=678bbc0e&hm=a69f4d791854a1c20fc613910b69fbc698ba963cfcd64acb7e310de395757f4a" alt="Rust Header">

        <div class="category">
            <h2><a href="https://rust.fandom.com/ru/wiki/%D0%A1%D1%82%D1%80%D0%BE%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D1%81%D1%82%D0%B2%D0%BE" target="_blank">Строительство</a></h2>
            <img src="https://cdn.discordapp.com/attachments/1314225469419294780/1329516092191670292/image.png?ex=678c9a19&is=678b4899&hm=446f26cbb5bc241c7f256d3f2810229e62c6c005ab6fbc73f92f08b0644c274a" alt="Строительство 1">
            <img src="https://cdn.discordapp.com/attachments/1314225469419294780/1328826537763672074/image.png?ex=678cbae7&is=678b6967&hm=290f765d65e8867aa5ea1b75e69eeabb22f85647188fcaf6aca95949ebb9a703" alt="Строительство 2">
        </div>

        <div class="category">
            <h2><a href="https://rust.fandom.com/ru/wiki/%D0%9E%D1%80%D1%83%D0%B6%D0%B8%D0%B5" target="_blank">Оружие</a></h2>
            <img src="https://cdn.discordapp.com/attachments/1314225469419294780/1330187700963250317/image.png?ex=678d1155&is=678bbfd5&hm=0729775c7f59b92d6b966d2e547fd6ccf157973cf7995b447f6a6ba138cf4f94" alt="Оружие">
        </div>

        <div class="category">
            <h2><a href="https://rust.fandom.com/ru/wiki/%D0%9F%D1%80%D0%B5%D0%B4%D0%BC%D0%B5%D1%82%D1%8B" target="_blank">Ресурсы и компоненты</a></h2>
            <img src="https://cdn.discordapp.com/attachments/1314225469419294780/1330107353160486934/image.png?ex=678cc681&is=678b7501&hm=ca5d62c144172afdc84304546757225d31fb94db7de49041216da6fe148de1fb" alt="Ресурсы">
        </div>

        <div class="category">
            <h2>Рейд Хелпер</h2>
            <img src="https://cdn.discordapp.com/attachments/1314225469419294780/1330189137264902206/A529CCA5C0B4F113FD3A45D53EC8BBA2EC8A3602.png?ex=678d12ac&is=678bc12c&hm=b7e25147e7d9832b67424d8008af506966c6dabd6326f9452ac13e9b756f5eaf" alt="Рейд Хелпер 2" onclick="openModal(this.src)">
        </div>
    </div>

    <div class="dev-section">
        <h3>Создатель сайта: Писька Грыз</h3>
    </div>

    <div id="myModal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="img01">
    </div>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('menu');
            const hamburger = document.querySelector('.hamburger');
            menu.style.display = menu.style.display === 'flex' ? 'none' : 'flex';
            hamburger.classList.toggle('active');
        }

        function switchLanguage() {
            const currentLang = document.querySelector('.language-switch').innerText;
            if (currentLang === 'EN') {
                document.querySelector('.language-switch').innerText = 'RU';
                document.querySelector('h1').innerText = 'Wikipedia about Rust';
                document.querySelector('.link').innerText = 'Link to the game on Steam';
                document.querySelectorAll('.category h2')[0].innerText = 'Building';
                document.querySelectorAll('.category h2')[1].innerText = 'Weapons';
                document.querySelectorAll('.category h2')[2].innerText = 'Resources and Components';
                document.querySelectorAll('.category h2')[3].innerText = 'Raid Helper';
                document.querySelector('.dev-section h3').innerText = 'Site Creator: Your Name';
            } else {
                document.querySelector('.language-switch').innerText = 'EN';
                document.querySelector('h1').innerText = 'Википедия о Rust';
                document.querySelector('.link').innerText = 'Ссылка на игру в Steam';
                document.querySelectorAll('.category h2')[0].innerText = 'Строительство';
                document.querySelectorAll('.category h2')[1].innerText = 'Оружие';
                document.querySelectorAll('.category h2')[2].innerText = 'Ресурсы и компоненты';
                document.querySelectorAll('.category h2')[3].innerText = 'Рейд Хелпер';
                document.querySelector('.dev-section h3').innerText = 'Создатель сайта: Писька Грыз';
            }
        }

        function openModal(src) {
            const modal = document.getElementById("myModal");
            const modalImg = document.getElementById("img01");
            modal.style.display = "block";
            modalImg.src = src;
        }

        function closeModal() {
            const modal = document.getElementById("myModal");
            modal.style.display = "none";
        }
    </script>

</body>
</html>
