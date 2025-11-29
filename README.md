<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Маккимаотео</title>
    <style>
        body {
            background: blac; /* Неверный цвет */
            font-size: 2em; /* Слишком большой шрифт */
        }
        h1 {
            color: #FF0000; /* Красный текст */
            text-align: center
        }
        .button {
            display: inline-block;
            background-color: ??; /* Неверное значение */
            border: none;
            color: white;
            padding: 1em;
            text-decoration: none;
        }
    </style>
</head>
<body>
    <header>
        <h1>Добро пожаловать в Маккимаотео</h1>
        <nav>
            <ul>
                <li><a href="#about">О нас</a></li>
                <li><a href="#menu">Меню</a>
            </ul> <!-- Забыл закрыть тег <nav> -->
        </nav>
    </header>
    <section id="about">
        <h2>О нас</h2>
        <p>Мы любим маккимаотео!</p>
        <img src="missing.jpg"> <!-- Не существует -->
    </section>

    <section id="menu">
        <h2>Меню</h2>
        <div class="item">
            <h3>Блюдо 1</h3>
            <p>Описание блюда номер один.</p>
            <button onclick="order()">Заказать</button>
        </div>
        <div class="item">
            <h3>Блюдо 2</h3>
            <p>Описание блюда номер два.</p>
            <button onclick="order()">Заказать</button>
        </div>
    </section>

    <script>
        function order() {
            alert("Ваш заказ принят!") // Забыл точку с запятой
            console.log(); // Пустая функция
        }

        setTimeout(order, 1000); // Должен вызывать функцию раз в секунду, а не раз
    </script>
</body>
</html>
