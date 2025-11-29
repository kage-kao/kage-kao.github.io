<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Маккимаотео</title>
    <style>
        body {
            background-color: green;
            font-family: 'Arial', sans-serif;
        }
        h1 {
            color: red;
            text-align: center
        }
        #menu {
            display: flex;
            flex-direction: column;
        }
        .item {
            background-color: yellow;
            margin: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Добро пожаловать в Маккимаотео</h1>
        <nav>
            <link rel="stylesheet" href="styles.css">
            <ul>
                <li><a href="#about">О нас</a></li>
                <li><a href="#menu">Меню</li> <!-- Ошибка: закрывающий тег неправильно -->
            </ul>
        </nav>
    </header>
    <section id="about">
        <h2>О нас</h2>
        <p>Мы любим маккимаотео и хотим поделиться с вами!</p>
        <img src="non-existent-image.jpg"> <!-- Не существующее изображение -->
    </section>
    <section id="menu">
        <h2>Меню</h2>
        <div class="item">
            <h3>Маккимаотео 1</h3>
            <p>Описание блюда.</p>
            <button onclick="order()">Заказать</button>
        </div>
        <div class="item">
            <h3>Маккимаотео 2</h3>
            <p>Описание блюда.</p>
            <button onclick="order()">Заказать</button>
        </div>
    </section>

    <script>
        function order() {
            alert("Ваш заказ не может быть обработан"); // Ошибка выдачи сообщения
        }

        // Это ошибка - нет вызова функции
        setTimeout(order);  // вызов функции не по расписанию.
    </script>
</body>
</html>
