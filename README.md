<!DOCTYPE html>
<html lang="ru">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rust – Вики о игре</title>
    <link href="https://fonts.googleapis.com/css2?family=Fjalla+One&display=swap"
        rel="stylesheet">
    <style>
        body {
            background: url('https://cdn.discordapp.com/attachments/1314225469419294780/1330120080213934090/1625629126_18-kartinkin-com-p-rast-zadnii-fon-krasivie-foni-18.png?ex=678cd25b&is=678b80db&hm=7b1b58d248ce46f3807c23a48221d9a735b2058a4567b60b43ee5faaa6ec4ca1') no-repeat center center fixed;
            background-size: cover;
            color: #fff;
            font-family: 'Fjalla One', Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: rgba(34, 34, 34, 0.9);
            color: #ff0000;
            padding: 1em 0;
            text-align: center;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin-right: 1em;
        }

        nav ul li a {
            color: #ff0000;
            text-decoration: none;
            font-family: 'Fjalla One', Arial, sans-serif;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1em;
            background-color: rgba(0, 0, 0, 0.8);
        }

        h1,
        h2 {
            color: #ff0000;
            font-family: 'Fjalla One', Arial, sans-serif;
        }

        .image-container {
            display: flex;
            justify-content: center;
            margin: 1em 0;
            position: relative;
        }

        .image-container img {
            max-width: 100%;
            height: auto;
            opacity: 0.5;
        }

        video {
            display: block;
            margin: 0 auto;
            max-width: 100%;
        }

        .hamburger {
            cursor: pointer;
            width: 30px;
            height: 30px;
            margin: 20px;
            position: relative;
            z-index: 2;
        }

        .line {
            width: 100%;
            height: 4px;
            background-color: white;
            margin: 6px 0;
            transition: 0.4s;
        }

        .side-panel {
            height: 100%;
            width: 0;
            position: fixed;
            top: 0;
            left: 0;
            background-color: #333;
            overflow-x: hidden;
            transition: 0.5s;
            padding-top: 60px;
            z-index: 1;
        }

        .side-panel a {
            padding: 10px 15px;
            text-decoration: none;
            font-size: 22px;
            color: #818181;
            display: block;
            transition: 0.3s;
        }

        .side-panel a:hover {
            color: #f1f1f1;
        }

        .closebtn {
            position: absolute;
            top: 0;
            right: 25px;
            font-size: 36px;
            margin-left: 50px;
        }
    </style>
</head>

<body>
    <div class="hamburger" onclick="togglePanel()">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
    </div>
    <div id="sidePanel" class="side-panel">
        <a href="javascript:void(0)" class="closebtn" onclick="togglePanel()">&times;</a>
        <a href="#about">О игре</a>
        <a href="#gameplay">Геймплей</a>
        <a href="#resources">Ресурсы</a>
        <a href="#crafting">Крафтинг</a>
        <a href="#buildings">Строительство</a>
    </div>
    <header>
        <h1>Добро пожаловать в Вики по игре Rust</h1>
        <nav>
            <ul>
                <li><a href="#about">О игре</a></li>
                <li><a href="#gameplay">Геймплей</a></li>
                <li><a href="#resources">Ресурсы</a></li>
                <li><a href="#crafting">Крафтинг</a></li>
                <li><a href="#buildings">Строительство</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="about" class="container">
            <h2>О игре</h2>
            <div class="image-container">
                <img src="https://cdn.discordapp.com/attachments/1314225469419294780/1329516092191670292/image.png?ex=678c9a19&is=678b4899&hm=446f26cbb5bc241c7f256d3f2810229e62c6c005ab6fbc73f92f08b0644c274a&"
                    alt="Скриншот геймплея Rust">
            </div>
            <p>Rust - многопользовательская онлайн-игра на выживание от компании Facepunch Studios. Игроки должны выжить в
                дикой природе, собирая ресурсы, строя укрытия и сотрудничая или соперничая с другими игроками. Игра вышла в
                ранний доступ в 2013 году и быстро завоевала популярность своей жёсткой механикой выживания.</p>
        </section>
        <section id="gameplay" class="container">
            <h2>Геймплей</h2>
            <div class="image-container">
                <img src="https://cdn.discordapp.com/attachments/1314225469419294780/1328826537763672074/image.png?ex=678c1227&is=678ac0a7&hm=b0b379555250e86f9bda02c46af8e7568231317510ffbd90738f07276daff128&"
                    alt="Бой в Rust">
            </div>
            <p>Rust предлагает игрокам динамичный геймплей, сочетающий элементы выживания, строительства и сражений. Игроки
                начинают с минимальным набором инструментов и должны искать ресурсы, чтобы строить укрытия и изготавливать
                оружие.</p>
            <h3>Пища и Вода</h3>
            <p>Пища и вода жизненно необходимы для выживания. Игроки должны охотиться, собирать ягоды и искать источники
                воды, чтобы выжить.</p>
            <h3>Боевые действия</h3>
            <p>Игроки могут сражаться с другими игроками или NPC, используя разнообразное оружие и ловушки. В PvP режимах
                важно уметь хорошо стрелять и прятаться.</p>
        </section>
        <section id="resources" class="container">
            <h2>Ресурсы</h2>
            <div class="image-container">
                <img src="https://cdn.discordapp.com/attachments/1314225469419294780/1330107353160486934/image.png?ex=678cc681&is=678b7501&hm=ca5d62c144172afdc84304546757225d31fb94db7de49041216da6fe148de1fb&"
                    alt="Ресурсы в Rust">
            </div>
            <p>Сбор ресурсов является ключевым элементом геймплея Rust. Игроки могут добывать дерево, камень, металлы и
                другие материалы, необходимые для строительства и изготовления предметов.</p>
            <h3>Дерево</h3>
            <p>Дерево - это основной ресурс, используемый для строительства и крафтинга. Игроки могут рубить деревья или
                собирать палки.</p>
            <h3>Металлы</h3>
            <p>Металлы, такие как железо и медь, используются для создания более прочных предметов и построек. Их можно
                добывать из рудников или собирать с помощью инструментов.</p>
        </section>
        <section id="crafting" class="container">
            <h2>Крафтинг</h2>
            <div class="image-container">
                <img src
