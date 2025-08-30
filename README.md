# Підказка по HTML

## Зміст
1. [Що таке HTML](#що-таке-html)
2. [Структура HTML-документа](#структура-html-документа)
3. [Елементи та теги HTML](#елементи-та-теги-html)
4. [Атрибути HTML](#атрибути-html)
5. [Текстові елементи](#текстові-елементи)
6. [Списки](#списки)
7. [Посилання](#посилання)
8. [Зображення](#зображення)
9. [Таблиці](#таблиці)
10. [Форми](#форми)
11. [Семантичні елементи HTML5](#семантичні-елементи-html5)
12. [Мультимедіа](#мультимедіа)
13. [Метадані](#метадані)
14. [API HTML5](#api-html5)
15. [Волідація та доступність](#валідація-і-доступність)

## Що таке HTML

HTML (HyperText Markup Language) —  це стандартна мова розмітки, яка використовується для створення вебсторінок і вебдодатків.

**Для чого потрібен HTML**

HTML виконує роль скелета вебсторінки. Він структурує контент, визначаючи, де мають 
бути заголовки, абзаци, списки, посилання, зображення, таблиці тощо. За допомогою тегів 
HTML браузер розуміє, як відображати інформацію користувачеві. Наприклад:

<p> для абзацу
<h1> для основного заголовка
<a> для посилання
<img> для зображення

## Структура HTML-документа

Базова структура HTML-документу:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Назва сторінки</title>
</head>
<body>
    <!-- Вміст сторінки -->
</body>
</html>
```

**Пояснення:**
- `<!DOCTYPE html>` — оголошення типу документа для HTML5
- `<html>` — кореневий елемент сторінки
- `<head>` — містить метадані, посилання на стилі та скрипти
- `<meta charset="UTF-8">` — вказує кодування документа
- `<meta name="viewport">` — налаштовує відображення на мобільних пристроях
- `<title>` — заголовок сторінки (відображається у заголовку вкладки браузера)
- `<body>` — містить видимий вміст сторінки
- `<!-- -->` — коментар (не відображається на сторінці)

## Елементи та теги HTML

HTML-елементи позначаються тегами, які полягають у кутові дужки.

**Типи тегів:**
1. **Парні теги**: мають теги, що відкривають і закривають
   ```html
   <h1>Заголовок</h1>
   ```

2. **Одиночні теги**: не мають тега, що закриває
   ```html
   <img src="image.jpg">
   <!-- В HTML5 можна також використовувати: -->
   <img src="image.jpg" />
   ```

**Вкладеність елементів:**
```html
<div>
    <p>Текст усередині параграфа, що знаходиться всередині div</p>
</div>
```

## Атрибути HTML

Атрибути надають додаткову інформацію щодо елементів.

**Синтаксис:**
```html
<тег атрибут="значення">Вміст</тег>
```

**Загальні атрибути:**
- `id` — унікальний ідентифікатор елемента
- `class` — визначає клас для CSS
- `style` — додає вбудовані стилі
- `title` — спливаюча підказка
- `data-*` — атрибути для зберігання даних

**Приклад:**
```html
<div id="container" class="main" style="color: blue;" title="Контейнер" data-info="custom">
    Вміст
</div>
```

## Текстові елементи

### Заголовки

HTML надає шість рівнів заголовків:

```html
<h1>Заголовок первого уровня</h1>
<h2>Заголовок второго уровня</h2>
<h3>Заголовок третьего уровня</h3>
<h4>Заголовок четвертого уровня</h4>
<h5>Заголовок пятого уровня</h5>
<h6>Заголовок шестого уровня</h6>
```

### Параграфы и форматирование текста

```html
<p>Это параграф текста.</p>

<!-- Разрыв строки -->
<p>Первая строка<br>Вторая строка</p>

<!-- Горизонтальная линия -->
<hr>

<!-- Выделение текста -->
<strong>Жирный текст</strong>
<em>Курсивный текст</em>
<mark>Выделенный текст</mark>
<small>Мелкий текст</small>
<del>Зачеркнутый текст</del>
<ins>Подчеркнутый текст</ins>
<sub>Подстрочный текст</sub>
<sup>Надстрочный текст</sup>
<code>Код</code>
<pre>Предварительно отформатированный текст
  с сохранением пробелов
    и переносов строк</pre>
```

## Списки

### Маркированный список (ненумерованный)

```html
<ul>
    <li>Элемент 1</li>
    <li>Элемент 2</li>
    <li>Элемент 3</li>
</ul>
```

### Нумерованный список

```html
<ol>
    <li>Первый элемент</li>
    <li>Второй элемент</li>
    <li>Третий элемент</li>
</ol>
```

**Атрибуты нумерованного списка:**
```html
<!-- Начать с определенного номера -->
<ol start="5">
    <li>Пятый элемент</li>
    <li>Шестой элемент</li>
</ol>

<!-- Изменить тип нумерации -->
<ol type="A">
    <li>Элемент A</li>
    <li>Элемент B</li>
</ol>
```

### Список определений

```html
<dl>
    <dt>Термин 1</dt>
    <dd>Определение термина 1</dd>
    <dt>Термин 2</dt>
    <dd>Определение термина 2</dd>
</dl>
```

### Вложенные списки

```html
<ul>
    <li>Элемент 1</li>
    <li>Элемент 2
        <ul>
            <li>Вложенный элемент 2.1</li>
            <li>Вложенный элемент 2.2</li>
        </ul>
    </li>
    <li>Элемент 3</li>
</ul>
```

## Ссылки

### Базовая ссылка

```html
<a href="https://example.com">Текст ссылки</a>
```

### Дополнительные атрибуты ссылок

```html
<!-- Открыть в новой вкладке -->
<a href="https://example.com" target="_blank">Открыть в новой вкладке</a>

<!-- Добавить подсказку -->
<a href="https://example.com" title="Посетить Example">Example</a>

<!-- Ссылка на email -->
<a href="mailto:example@example.com">Отправить email</a>

<!-- Ссылка на телефон -->
<a href="tel:+1234567890">Позвонить</a>

<!-- Ссылка на якорь (внутри страницы) -->
<a href="#section1">Перейти к разделу 1</a>

<!-- Якорь (место назначения) -->
<h2 id="section1">Раздел 1</h2>

<!-- Скачивание файла -->
<a href="file.pdf" download>Скачать PDF</a>
```

## Изображения

### Базовое изображение

```html
<img src="image.jpg" alt="Описание изображения">
```

### Дополнительные атрибуты изображений

```html
<!-- Установка размеров -->
<img src="image.jpg" alt="Описание" width="300" height="200">

<!-- Изображение с заголовком -->
<figure>
    <img src="image.jpg" alt="Описание">
    <figcaption>Подпись к изображению</figcaption>
</figure>

<!-- Изображение-ссылка -->
<a href="page.html">
    <img src="image.jpg" alt="Описание">
</a>

<!-- Адаптивное изображение -->
<picture>
    <source media="(min-width: 650px)" srcset="img_large.jpg">
    <source media="(min-width: 465px)" srcset="img_medium.jpg">
    <img src="img_small.jpg" alt="Описание">
</picture>
```

## Таблицы

### Базовая структура таблицы

```html
<table>
    <caption>Название таблицы</caption>
    <thead>
        <tr>
            <th>Заголовок 1</th>
            <th>Заголовок 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Ячейка 1</td>
            <td>Ячейка 2</td>
        </tr>
        <tr>
            <td>Ячейка 3</td>
            <td>Ячейка 4</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2">Итого</td>
        </tr>
    </tfoot>
</table>
```

### Дополнительные атрибуты таблиц

```html
<!-- Объединение ячеек по горизонтали -->
<td colspan="2">Объединенная ячейка</td>

<!-- Объединение ячеек по вертикали -->
<td rowspan="2">Объединенная ячейка</td>

<!-- Группировка столбцов для стилизации -->
<table>
    <colgroup>
        <col style="background-color: yellow">
        <col style="background-color: lightblue">
    </colgroup>
    <tr>
        <td>Ячейка 1</td>
        <td>Ячейка 2</td>
    </tr>
</table>
```

## Формы

### Базовая структура формы

```html
<form action="/submit" method="post">
    <label for="name">Имя:</label>
    <input type="text" id="name" name="name" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <input type="submit" value="Отправить">
</form>
```

### Типы полей ввода

```html
<!-- Текстовое поле -->
<input type="text" name="username" placeholder="Введите имя пользователя">

<!-- Пароль -->
<input type="password" name="password" placeholder="Введите пароль">

<!-- Email -->
<input type="email" name="email" placeholder="example@domain.com">

<!-- Телефон -->
<input type="tel" name="phone" pattern="[0-9]{10}" placeholder="1234567890">

<!-- Число -->
<input type="number" name="quantity" min="1" max="100" step="1" value="1">

<!-- Диапазон (слайдер) -->
<input type="range" name="rating" min="1" max="10" value="5">

<!-- Дата -->
<input type="date" name="birthdate">

<!-- Время -->
<input type="time" name="meeting-time">

<!-- Цвет -->
<input type="color" name="favorite-color" value="#ff0000">

<!-- Флажок (чекбокс) -->
<input type="checkbox" id="subscribe" name="subscribe" checked>
<label for="subscribe">Подписаться на рассылку</label>

<!-- Переключатель (радиокнопка) -->
<input type="radio" id="male" name="gender" value="male">
<label for="male">Мужской</label>
<input type="radio" id="female" name="gender" value="female">
<label for="female">Женский</label>

<!-- Выпадающий список -->
<label for="country">Страна:</label>
<select id="country" name="country">
    <option value="">Выберите страну</option>
    <option value="ru">Россия</option>
    <option value="us">США</option>
    <option value="gb">Великобритания</option>
</select>

<!-- Многострочное текстовое поле -->
<label for="message">Сообщение:</label>
<textarea id="message" name="message" rows="4" cols="50"></textarea>

<!-- Загрузка файлов -->
<input type="file" name="document" accept=".pdf,.doc,.docx">
<input type="file" name="images" accept="image/*" multiple>

<!-- Скрытое поле -->
<input type="hidden" name="user_id" value="123">

<!-- Кнопка отправки формы -->
<input type="submit" value="Отправить">

<!-- Кнопка сброса формы -->
<input type="reset" value="Сбросить">

<!-- Обычная кнопка -->
<button type="button">Нажми меня</button>
```

### Группировка элементов формы

```html
<form>
    <fieldset>
        <legend>Личная информация</legend>
        <label for="name">Имя:</label>
        <input type="text" id="name" name="name">
        
        <label for="email">Email:</label>
        <input type="email" id="email" name="email">
    </fieldset>
    
    <fieldset>
        <legend>Дополнительная информация</legend>
        <label for="comments">Комментарии:</label>
        <textarea id="comments" name="comments"></textarea>
    </fieldset>
    
    <input type="submit" value="Отправить">
</form>
```

### Атрибуты для валидации форм

```html
<!-- Обязательное поле -->
<input type="text" name="username" required>

<!-- Шаблон (регулярное выражение) -->
<input type="text" name="code" pattern="[A-Za-z]{3}-[0-9]{2}" title="Формат: XXX-00">

<!-- Минимальная и максимальная длина -->
<input type="text" name="username" minlength="3" maxlength="20">

<!-- Отключение автозаполнения -->
<input type="text" name="username" autocomplete="off">

<!-- Автофокус при загрузке страницы -->
<input type="text" name="search" autofocus>

<!-- Только для чтения -->
<input type="text" name="id" value="12345" readonly>

<!-- Отключенное поле -->
<input type="text" name="status" value="Неактивно" disabled>
```

## Семантические элементы HTML5

HTML5 ввел семантические элементы, которые более четко описывают свое содержимое:

```html
<header>Верхняя часть страницы или раздела</header>

<nav>
    <ul>
        <li><a href="/">Главная</a></li>
        <li><a href="/about">О нас</a></li>
        <li><a href="/contact">Контакты</a></li>
    </ul>
</nav>

<main>
    <article>
        <header>
            <h1>Заголовок статьи</h1>
            <p>Автор: Иван Иванов</p>
        </header>
        <section>
            <h2>Раздел 1</h2>
            <p>Содержимое раздела 1...</p>
        </section>
        <section>
            <h2>Раздел 2</h2>
            <p>Содержимое раздела 2...</p>
        </section>
        <footer>
            <p>Опубликовано: 28 апреля 2025</p>
        </footer>
    </article>
    
    <aside>
        <h3>Связанные статьи</h3>
        <ul>
            <li><a href="#">Статья 1</a></li>
            <li><a href="#">Статья 2</a></li>
        </ul>
    </aside>
</main>

<footer>
    <p>&copy; 2025 Моя компания. Все права защищены.</p>
</footer>
```

**Другие семантические элементы:**

```html
<!-- Определяет фигуру с подписью -->
<figure>
    <img src="image.jpg" alt="Описание">
    <figcaption>Подпись к изображению</figcaption>
</figure>

<!-- Определяет время/дату -->
<time datetime="2025-04-28">28 апреля 2025</time>

<!-- Определяет детали, которые пользователь может открывать и закрывать -->
<details>
    <summary>Нажмите, чтобы показать подробности</summary>
    <p>Дополнительная информация, которая будет показана при нажатии.</p>
</details>

<!-- Определяет прогресс задачи -->
<progress value="70" max="100">70%</progress>

<!-- Определяет измерение в известном диапазоне -->
<meter value="0.7" min="0" max="1">70%</meter>

<!-- Определяет отдельную часть текста, например, выделенную цитату -->
<blockquote cite="https://example.com/source">
    <p>Цитируемый текст</p>
    <footer>— <cite>Автор цитаты</cite></footer>
</blockquote>

<!-- Определяет короткую цитату -->
<p>Как сказал <q cite="https://example.com/source">автор</q>, это важно.</p>

<!-- Определяет текст, который был удален из документа -->
<p>Это <del datetime="2025-04-28">удаленный</del> <ins>добавленный</ins> текст.</p>

<!-- Определяет адрес -->
<address>
    <p>Иван Иванов</p>
    <p>ул. Примерная, д. 123</p>
    <p>Москва, Россия</p>
</address>
```

## Мультимедиа

### Видео

```html
<video width="640" height="360" controls>
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Ваш браузер не поддерживает тег video.
</video>
```

**Атрибуты видео:**
- `controls` — отображает элементы управления
- `autoplay` — автоматическое воспроизведение
- `loop` — зацикливание
- `muted` — без звука
- `poster="image.jpg"` — изображение до начала воспроизведения
- `preload="auto|metadata|none"` — предварительная загрузка

### Аудио

```html
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    <source src="audio.ogg" type="audio/ogg">
    Ваш браузер не поддерживает тег audio.
</audio>
```

### Встраивание контента

```html
<!-- Встраивание iframe (например, YouTube видео) -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe>

<!-- Встраивание карты Google Maps -->
<iframe src="https://www.google.com/maps/embed?pb=..." width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>

<!-- Встраивание SVG -->
<svg width="100" height="100">
    <circle cx="50" cy="50" r="40" stroke="black" stroke-width="2" fill="red" />
</svg>

<!-- Встраивание Canvas для JavaScript графики -->
<canvas id="myCanvas" width="200" height="100"></canvas>
```

## Метаданные

Метаданные размещаются в элементе `<head>` и предоставляют информацию о документе.

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <!-- Основные метаданные -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Название страницы</title>
    
    <!-- Описание страницы (для поисковых систем) -->
    <meta name="description" content="Описание страницы для поисковых систем">
    <meta name="keywords" content="ключевые, слова, через, запятую">
    <meta name="author" content="Имя автора">
    
    <!-- Управление индексацией поисковыми системами -->
    <meta name="robots" content="index, follow">
    
    <!-- Метаданные для социальных сетей (Open Graph) -->
    <meta property="og:title" content="Название для соцсетей">
    <meta property="og:description" content="Описание для соцсетей">
    <meta property="og:image" content="https://example.com/image.jpg">
    <meta property="og:url" content="https://example.com/page">
    <meta property="og:type" content="website">
    
    <!-- Метаданные для Twitter -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Название для Twitter">
    <meta name="twitter:description" content="Описание для Twitter">
    <meta name="twitter:image" content="https://example.com/image.jpg">
    
    <!-- Иконка сайта -->
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <link rel="apple-touch-icon" href="apple-touch-icon.png">
    
    <!-- Подключение CSS -->
    <link rel="stylesheet" href="styles.css">
    
    <!-- Подключение JavaScript -->
    <script src="script.js" defer></script>
    
    <!-- Предварительная загрузка ресурсов -->
    <link rel="preload" href="important-font.woff2" as="font" type="font/woff2" crossorigin>
    <link rel="preconnect" href="https://example.com">
    
    <!-- Альтернативные версии страницы -->
    <link rel="alternate" hreflang="en" href="https://example.com/en/page">
    <link rel="canonical" href="https://example.com/page">
</head>
<body>
    <!-- Содержимое страницы -->
</body>
</html>
```

## API HTML5

HTML5 предоставляет множество API для создания более интерактивных веб-приложений.

### Геолокация

```html
<button onclick="getLocation()">Определить местоположение</button>
<p id="demo"></p>

<script>
function getLocation() {
    if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(showPosition);
    } else {
        document.getElementById("demo").innerHTML = "Геолокация не поддерживается вашим браузером.";
    }
}

function showPosition(position) {
    document.getElementById("demo").innerHTML = 
    "Широта: " + position.coords.latitude + 
    "<br>Долгота: " + position.coords.longitude;
}
</script>
```

### Хранение данных

```html
<script>
// localStorage - данные сохраняются даже после закрытия браузера
localStorage.setItem("name", "Иван");
let name = localStorage.getItem("name");
localStorage.removeItem("name");
localStorage.clear(); // Удаляет все данные

// sessionStorage - данные удаляются при закрытии вкладки
sessionStorage.setItem("name", "Иван");
let sessionName = sessionStorage.getItem("name");
sessionStorage.removeItem("name");
sessionStorage.clear();
</script>
```

### Drag and Drop API

```html
<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)" style="width:200px; height:200px; border:1px solid black;"></div>
<img id="drag1" src="img.jpg" draggable="true" ondragstart="drag(event)" width="150" height="150">

<script>
function allowDrop(ev) {
    ev.preventDefault();
}

function drag(ev) {
    ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
    ev.preventDefault();
    var data = ev.dataTransfer.getData("text");
    ev.target.appendChild(document.getElementById(data));
}
</script>
```

### Web Workers

```html
<p>Считаем: <output id="result"></output></p>
<button onclick="startWorker()">Запустить Worker</button>
<button onclick="stopWorker()">Остановить Worker</button>

<script>
let w;

function startWorker() {
    if (typeof(Worker) !== "undefined") {
        if (typeof(w) == "undefined") {
            w = new Worker("worker.js");
        }
        w.onmessage = function(event) {
            document.getElementById("result").innerHTML = event.data;
        };
    } else {
        document.getElementById("result").innerHTML = "Web Workers не поддерживаются вашим браузером";
    }
}

function stopWorker() {
    if (w) {
        w.terminate();
        w = undefined;
    }
}
</script>
```

Содержимое файла worker.js:
```javascript
let i = 0;
function timedCount() {
    i = i + 1;
    postMessage(i);
    setTimeout(timedCount, 500);
}
timedCount();
```

## Валидация и доступность

### Валидация HTML

Всегда проверяйте валидность вашего HTML-кода с помощью [W3C Validator](https://validator.w3.org/).

### Доступность (Accessibility)

```html
<!-- Используйте правильную семантику -->
<button aria-label="Закрыть" aria-expanded="false">✕</button>

<!-- Добавляйте альтернативный текст для изображений -->
<img src="image.jpg" alt="Описание изображения">

<!-- Используйте ARIA-атрибуты для улучшения доступности -->
<div role="alert" aria-live="assertive">Важное сообщение</div>

<!-- Используйте правильную структуру заголовков -->
<h1>Главный заголовок</h1>
<section>
    <h2>Подзаголовок</h2>
    <p>Содержимое...</p>
</section>

<!-- Используйте правильную разметку для форм -->
<label for="name">Имя:</label>
<input type="text" id="name" name="name" required aria-required="true">

<!-- Используйте tabindex для управления навигацией с клавиатуры -->
<div tabindex="0">Этот элемент можно выбрать с помощью клавиши Tab</div>

<!-- Используйте lang атрибут для указания языка -->
<p lang="en">This is English text.</p>
<p lang="ru">Это русский текст.</p>
```

### Основные принципы доступности:

1. **Воспринимаемость**: информация должна быть представлена в форме, которую пользователи могут воспринимать.
2. **Управляемость**: компоненты интерфейса должны быть управляемыми.
3. **Понятность**: информация и операции должны быть понятными.
4. **Надежность**: контент должен быть достаточно надежным для интерпретации различными пользовательскими агентами.

---
