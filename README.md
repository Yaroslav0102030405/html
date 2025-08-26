# Повна шпаргалка по HTML

## Зміст
1. [Введення в HTML](#введення-в-html)
2. [Структура HTML-документа](#структура-html-документа)
3. [Елементи та теги HTML](#елементи-і-теги-html)
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

## Введення в HTML

HTML (HyperText Markup Language) – це стандартизована мова розмітки для створення веб-сторінок. Поточна версія - HTML5.

**Основні характеристики:**
- описує структуру веб-сторінки
- Складається з елементів, що позначені тегами
- Інтерпретується браузерами для відображення вмісту
- Працює разом з CSS (для стилів) та JavaScript (для інтерактивності)

## Структура HTML-документа

Базова структура HTML-документу:

``html
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
````

**Пояснення:**
- `<!DOCTYPE html>` - оголошення типу документа для HTML5
- `<html>` - кореневий елемент сторінки
- `<head>` - містить метадані, посилання на стилі та скрипти
- `<meta charset="UTF-8">` ​​- вказує кодування документа
- `<meta name="viewport">` - налаштовує відображення на мобільних пристроях
- `<title>` - заголовок сторінки (відображається в заголовку вкладки браузера)
- `<body>` - містить видимий вміст сторінки
- `<!-- -->` — коментар (не відображається на сторінці)

## Елементи та теги HTML

HTML-елементи позначаються тегами, які полягають у кутові дужки.

**Типи тегів:**
1. **Парні теги**: мають теги, що відкривають і закривають 
``html 
<h1>Заголовок</h1> 
````

2. **Одиночні теги**: не мають тега, що закриває 
``html 
<img src="image.jpg"> 
<!-- У HTML5 можна також використовувати: --> 
<img src="image.jpg" /> 
````

**Вкладеність елементів:**
``html
<div> 
<p>Текст всередині параграфа, який знаходиться всередині div</p>
</div>
````

## Атрибути HTML

Атрибути надають додаткову інформацію щодо елементів.

**Синтаксис:**
``html
<тег атрибут="значення">Вміст</тег>
````

**Загальні атрибути:**
- `id` - унікальний ідентифікатор елемента
- `class` - визначає клас для CSS
- `style` - додає вбудовані стилі
- `title` - спливаюча підказка
- `data-*` — атрибути користувача для зберігання даних

**Приклад:**
``html
<div id="container" class="main" style="color: blue;" title="Контейнер" data-info="custom"> 
Вміст
</div>
````

## Текстові елементи

### Заголовки

HTML надає шість рівнів заголовків:

``html
<h1>Заголовок першого рівня</h1>
<h2>Заголовок другого рівня</h2>
<h3>Заголовок третього рівня</h3>
<h4>Заголовок четвертого рівня</h4>
<h5>Заголовок п'ятого рівня</h5>
<h6>Заголовок шостого рівня</h6>
````

### Параграфи та форматування тексту

``html
<p>Це пункт тексту.</p>

<!-- Розрив рядка -->
<p>Перший рядок<br>Другий рядок</p>

<!-- Горизонтальна лінія -->
<hr>

<!-- Виділення тексту -->
<strong>Жирний текст</strong>
<em>Курсивний текст</em>
<mark>Виділений текст</mark>
<small>Дрібний текст</small>
<del>Закреслений текст</del>
<ins>Підкреслений текст</ins>
<sub>Підрядковий текст</sub>
<sup>Надрядковий текст</sup>
<code>Код</code>
<pre>Попередньо відформатований текст 
із збереженням прогалин 
та перенесення рядків</pre>
````

## Списки

### Маркований список (ненумерований)

``html
<ul> 
<li>Елемент 1</li> 
<li>Елемент 2</li> 
<li>Елемент 3</li>
</ul>
````

### Нумерований список

``html
<ol> 
<li>Перший елемент</li> 
<li>Другий елемент</li> 
<li>Третій елемент</li>
</ol>
````

**Атрибути нумерованого списку:**
``html
<!-- Почати з певного номера -->
<ol start="5"> 
<li>П'ятий елемент</li> 
<li>Шостий елемент</li>
</ol>

<!-- Змінити тип нумерації -->
<ol type="A"> 
<li>Елемент A</li> 
<li>Елемент B</li>
</ol>
````

### Список визначень

``html
<dl> 
<dt>Термін 1</dt> 
<dd>Визначення терміна 1</dd> 
<dt>Термін 2</dt> 
<dd>Визначення терміна 2</dd>
</dl>
````

### Вкладені списки

``html
<ul> 
<li>Елемент 1</li> 
<li>Елемент 2 
<ul> 
<li>Вкладений елемент 2.1</li> 
<li>Вкладений елемент 2.2</li> 
</ul> 
</li> 
<li>Елемент 3</li>
</ul>
````

## Посилання

### Базове посилання

``html
<a href="https://example.com">Текст посилання</a>
````

### Додаткові атрибути посилань

``html
<!-- Відкрити в новій вкладці -->
<a href="https://example.com" target="_blank">Відкрити у новій вкладці</a>

<!-- Додати підказку -->
<a href="https://example.com" title="Відвідати Example">Example</a>

<!-- Посилання на email -->
<a href="mailto:example@example.com">Надіслати email</a>

<!-- Посилання на телефон -->
<a href="tel:+1234567890">Зателефонувати</a>

<!-- Посилання на якір (всередині сторінки) -->
<a href="#section1">Перейти до розділу 1</a>

<!-- Якір (місце призначення) -->
<h2 id="section1">Розділ 1</h2>

<!-- Завантаження файлу -->
<a href="file.pdf" download>Завантажити PDF</a>
````

## Зображення

### Базове зображення

``html
<img src="image.jpg" alt="Опис зображення">
````

### Додаткові атрибути зображень

``html
<!-- Встановлення розмірів -->
<img src="image.jpg" alt="Опис" width="300" height="200">

<!-- Зображення із заголовком -->
<figure> 
<img src="image.jpg" alt="Опис"> 
<figcaption>Підпис до зображення</figcaption>
</figure>

<!-- Зображення-посилання -->
<a href="page.html"> 
<img src="image.jpg" alt="Опис">
</a>

<!-- Адаптивне зображення -->
<picture> 
<source media="(min-width: 650px)" srcset="img_large.jpg"> 
<source media="(min-width: 465px)" srcset="img_medium.jpg"> 
<img src="img_small.jpg" alt="Опис">
</picture>
````

## Таблиці

### Базова структура таблиці

``html
<table> 
<caption>Назва таблиці</caption> 
<thead> 
<tr> 
<th>Заголовок 1</th> 
<th>Заголовок 2</th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>Комірка 1</td> 
<td>Комірка 2</td> 
</tr> 
<tr> 
<td>Комірка 3</td> 
<td>Комірка 4</td> 
</tr> 
</tbody> 
<tfoot> 
<tr> 
<td colspan="2">Разом</td> 
</tr> 
</tfoot>
</table>
````

### Додаткові атрибути таблиць

``html
<!-- Об'єднання осередків по горизонталі -->
<td colspan="2">Об'єднаний осередок</td>

<!-- Об'єднання осередків по вертикалі -->
<td rowspan="2">Об'єднаний осередок</td>

<!-- Угруповання стовпців для стилізації -->
<table> 
<colgroup> 
<col style="background-color: yellow"> 
<col style="background-color: lightblue"> 
</colgroup> 
<tr> 
<td>Комірка 1</td> 
<td>Комірка 2</td> 
</tr>
</table>
````

## Форми

### Базова структура форми

``html
<form action="/submit" method="post"> 
<label for="name">Ім'я:</label> 
<input type="text" id="name" name="name" required> 

<label for="email">Email:</label> 
<input type="email" id="email" name="email" required> 

<input type="submit" value="Надіслати">
</form>
````

### Типи полів введення

``html
<!-- Текстове поле -->
<input type="text" name="username" placeholder="Введіть ім'я користувача">

<!-- Пароль -->
<input type="password" name="password" placeholder="Введіть пароль">

<!-- Email -->
<input type="email" name="email" placeholder="example@domain.com">

<!-- Телефон -->
<input type="tel" name="phone" pattern="[0-9]{10}" placeholder="1234567890">

<!-- Число -->
<input type="number" name="quantity" min="1" max="100" step="1" value="1">

<!-- Діапазон (слайдер) -->
<input type="range" name="rating" min="1" max="10" value="5">

<!-- Дата -->
<input type="date" name="birthdate">

<!-- Час -->
<input type="time" name="meeting-time">

<!-- Колір -->
<input type="color" name="favorite-color" value="#ff0000">

<!-- Прапорець (чекбокс) -->
<input type="checkbox" id="subscribe" name="subscribe" checked>
<label for="subscribe">Підписатися на розсилку</label>

<!-- Перемикач (радіокнопка) -->
<input type="radio" id="male" name="gender" value="male">
<label for="male">Чоловічий</label>
<input type="radio" id="female" name="gender" value="female">
<label for="female">Жіночий</label>

<!-- Список, що випадає -->
<label for="country">Країна:</label>
<select id="country" name="country"> 
<option value="">Виберіть країну</option> 
<option value="ru">Росія</option> 
<option value="us">США</option> 
<option value="gb">Велика Британія</option>
</select>

<!-- Багаторядкове текстове поле -->
<label for="message">Повідомлення:</label>
<textarea id="message" name="message" rows="4" cols="50"></textarea>

<!-- Завантаження файлів -->
<input type="file" name="document" accept=".pdf,.doc,.docx">
<input type="file" name="images" accept="image/*" multiple>

<!-- Приховане поле -->
<input type="hidden" name="user_id" value="123">

<!-- Кнопка відправки форми -->
<input type="submit" value="Надіслати">

<!-- Кнопка скидання форми -->
<input type="reset" value="Скинути">

<!-- Звичайна кнопка -->
<button type="button">Натисніть мене</button>
````

### Угруповання елементів форми

``html
<form> 
<fieldset> 
<legend>Особиста інформація</legend> 
<label for="name">Ім'я:</label> 
<input type="text" id="name" name="name"> 

<label for="email">Email:</label> 
<input type="email" id="email" name="email"> 
</fieldset> 

<fieldset> 
<legend>Додаткова інформація</legend> 
<label for="comments">Коментарі:</label> 
<textarea id="comments" name="comments"></textarea> 
</fieldset> 

<input type="submit" value="Надіслати">
</form>
````

### Атрибути для валідації форм

``html
<!-- Обов'язкове поле -->
<input type="text" name="username" required>

<!-- Шаблон (регулярний вираз) -->
<input type="text" name="code" pattern="[A-Za-z]{3}-[0-9]{2}" title="Формат: XXX-00">

<!-- Мінімальна та максимальна довжина -->
<input type="text" name="username" minlength="3" maxlength="20">

<!-- Вимкнення автозаповнення -->
<input type="text" name="username" autocomplete="off">

<!-- Автофокус під час завантаження сторінки -->
<input type="text" name="search" autofocus>

<!-- Тільки для читання -->
<input type="text" name="id" value="12345" readonly>

<!-- Відключене поле -->
<input type="text" name="status" value="Неактивно" disabled>
````

## Семантичні елементи HTML5

HTML5 ввів семантичні елементи, які чіткіше описують свій вміст:

``html
<header>Верхня частина сторінки або розділу</header>

<nav> 
<ul> 
<li><a href="/">Головна</a></li> 
<li><a href="/about">Про нас</a></li> 
<li><a href="/contact">Контакти</a></li> 
</ul>
</nav>

<main> 
<article> 
<header> 
<h1>Заголовок статті</h1> 
<p>Автор: Іван Іванов</p> 
</header> 
<section> 
<h2>Розділ 1</h2> 
<p>Вміст розділу 1...</p> 
</section> 
<section> 
<h2>Розділ 2</h2> 
<p>Вміст розділу 2...</p> 
</section> 
<footer> 
<p>Опубліковано: 28 квітня 2025 року</p> 
</footer> 
</article> 

<aside> 
<h3>Св'язані статті</h3> 
<ul> 
<li><a href="#">Стаття 1</a></li> 
<li><a href="#">Стаття 2</a></li> 
</ul> 
</aside>
</main>

<footer> 
<p>&copy; 2025 Моя компанія. Усі права захищені.</p>
</footer>
````

**Інші семантичні елементи:**

``html
<!-- Визначає фігуру з підписом -->
<figure> 
<img src="image.jpg" alt="Опис"> 
<figcaption>Підпис до зображення</figcaption>
</figure>

<!-- Визначає час/дату -->
<time datetime="2025-04-28">28 квітня 2025</time>

<!-- Визначає деталі, які користувач може відкривати та закривати -->
<details> 
<summary>Натисніть, щоб показати подробиці</summary> 
<p>Додаткова інформація, яка буде показана при натисканні.</p>
</details>

<!-- Визначає прогрес завдання -->
<progress value="70" max="100">70%</progress>

<!-- Визначає вимірювання у відомому діапазоні -->
<meter value="0.7" min="0" max="1">70%</meter>

<!-- Визначає окрему частину тексту, наприклад виділену цитату -->
<blockquote cite="https://example.com/source"> 
<p>Цитований текст</p> 
<footer>— <cite>Автор цитати</cite></footer>
</blockquote>

<!-- Визначає коротку цитату -->
<p>Як сказав <q cite="https://example.com/source">автор</q>, це важливо.</p>

<!-- Визначає текст, який було видалено з документа -->
<p>Це <del datetime="2025-04-28">віддалений</del> <ins>доданий</ins> текст.</p>

<!-- Визначає адресу -->
<address> 
<p>Іван Іванов</p> 
<p>вул. Орієнтовна, д. 123</p> 
<p>Москва, Росія</p>
</address>
````

## Мультимедіа

### Відео

``html
<video width="640" height="360" controls> 
<source src="video.mp4" type="video/mp4"> 
<source src="video.webm" type="video/webm"> 
Ваш браузер не підтримує тег відео.
</video>
````

**Атрибути відео:**
- `controls` - відображає елементи керування
- `autoplay` - автоматичне відтворення
- `loop` - зациклювання
- `muted` - без звуку
- `poster="image.jpg"` - зображення до початку відтворення
- `preload="auto|metadata|none"` - попереднє завантаження

### Аудіо

``html
<audio controls> 
<source src="audio.mp3" type="audio/mpeg"> 
<source src="audio.ogg" type="audio/ogg"> 
Ваш браузер не підтримує тег audio.
</audio>
````

### Вбудовування контенту

``html
<!-- Вбудовування iframe (наприклад, YouTube відео) -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe>

<!-- Вбудовування картки Google Maps -->
<iframe src="https://www.google.com/maps/embed?pb=..." width="600" height="450" ​​style="border:0;" allowfullscreen="" loading="lazy"></iframe>

<!-- Вбудовування SVG -->
<svg width="100" height="100"> 
<circle cx="50" cy="50" r="40" stroke="black" stroke-width="2" fill="red" />
</svg>

<!-- Вбудовування Canvas для JavaScript графіки -->
<canvas id="myCanvas" width="200" height="100"></canvas>
````

## Метадані

Метадані розміщуються в елементі `<head>` та надають інформацію про документ.

``html
<!DOCTYPE html>
<html lang="ru">
<head> 
<!-- Основні метадані --> 
<meta charset="UTF-8"> 
<meta name="viewport" content="width=device-width, initial-scale=1.0"> 
<title>Назва сторінки</title> 

<!-- Опис сторінки (для пошукових систем) --> 
<meta name="description" content="Опис сторінки для пошукових систем"> 
<meta name="keywords" content="ключові, слова, через, кому"> 
<meta name="author" content="Ім'я автора"> 

<!-- Управління індексацією пошуковими системами --> 
<meta name="robots" content="index, follow"> 

<!-- Метадані для соціальних мереж (Open Graph) --> 
<meta property="og:title" content="Назва для соціальних мереж"> 
<meta property="og:description" content="Опис для соцмереж"> 
<meta property="og:image" content="https://example.com/image.jpg"> 
<meta property="og:url" content="https://example.com/page"> 
<meta property="og:type" content="website"> 

<!-- Метадані для Twitter --> 
<meta name="twitter:card" content="summary_large_image"> 
<meta name="twitter:title" content="Назва для Twitter"> 
<meta name="twitter:description" content="Опис для Twitter"> 
<meta name="twitter:image" content="https://example.com/image.jpg"> 

<!-- Іконка сайту --> 
<link rel="icon" href="favicon.ico" type="image/x-icon"> 
<link rel="apple-touch-icon" href="apple-touch-icon.png"> 

<!-- Підключення CSS --> 
<link rel="stylesheet" href="styles.css"> 

<!-- Підключення JavaScript --> 
<script src="script.js" defer></script> 

<!-- Попереднє завантаження ресурсів --> 
<link rel="preload" href="important-font.woff2" as="font" type="font/woff2" crossorigin> 
<link rel="preconnect" href="https://example.com"> 

<!-- Альтернативні версії сторінки --> 
<link rel="alternate" hreflang="en" href="https://example.com/en/page"> 
<link rel="canonical" href="https://example.com/page">
</head>
<body> 
<!-- Вміст сторінки -->
</body>
</html>
````

## API HTML5

HTML5 надає безліч API для створення більш інтерактивних веб-застосунків.

### Геолокація

``html
<button onclick="getLocation()">Визначити розташування</button>
<p id="demo"></p>

<script>
function getLocation() { 
if (navigator.geolocation) { 
navigator.geolocation.getCurrentPosition(showPosition); 
} else { 
document.getElementById("demo").innerHTML = "Геолокація не підтримується вашим браузером."; 
}
}

function showPosition(position) { 
document.getElementById("demo").innerHTML = 
"Широта:" + position.coords.latitude + 
<br>Довгота: + position.coords.longitude;
}
</script>
````

### Зберігання даних

``html
<script>
//localStorage - дані зберігаються навіть після закриття браузера
localStorage.setItem("name", "Іван");
let name = localStorage.getItem("name");
localStorage.removeItem("name");
localStorage.clear(); // Видаляє всі дані

// sessionStorage - дані видаляються при закритті вкладки
sessionStorage.setItem("name", "Іван");
let sessionName = sessionStorage.getItem("name");
sessionStorage.removeItem("name");
sessionStorage.clear();
</script>
````

### Drag and Drop API

``html
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
````

### Web Workers

``html
<p>Вважаємо: <output id="result"></output></p>
<button onclick="startWorker()">Запустити Worker</button>
<button onclick="stopWorker()">Зупинити Worker</button>

<script>
let w;

function startWorker() { 
if (typeof(Worker) !== "undefined") { 
if (typeof(w) == "undefined") { 
w = новий Worker("worker.js"); 
} 
w.onmessage = function(event) { 
document.getElementById("result").innerHTML = event.data; 
}; 
} else { 
document.getElementById("result").innerHTML = "Web Workers не підтримуються вашим браузером"; 
}
}

function stopWorker() { 
if (w) { 
w.terminate(); 
w = undefined; 
}
}
</script>
````

Вміст файлу worker.js:
```javascript
let i = 0;
function timedCount() { 
i = i + 1; 
postMessage(i); 
setTimeout(timedCount, 500);
}
timedCount();
````

## Валідація та доступність

### Валідація HTML

Завжди перевіряйте валідність HTML-коду за допомогою [W3C Validator](https://validator.w3.org/).

### Доступність (Accessibility)

``html
<!-- Використовуйте правильну семантику -->
<button aria-label="Закрити" aria-expanded="false">✕</button>

<!-- Додайте альтернативний текст для зображень -->
<img src="image.jpg" alt="Опис зображення">

<!-- Використовуйте ARIA-атрибути для покращення доступності -->
<div role="alert" aria-live="assertive">Важливе повідомлення</div>

<!-- Використовуйте правильну структуру заголовків -->
<h1>Головний заголовок</h1>
<section> 
<h2>Підзаголовок</h2> 
<p>Вміст...</p>
</section>

<!-- Використовуйте правильну розмітку для форм -->
<label for="name">Ім'я:</label>
<input type="text" id="name" name="name" required aria-required="true">

<!-- Використовуйте tabindex для керування навігацією з клавіатури -->
<div tabindex="0">Цей елемент можна вибрати за допомогою клавіші Tab</div>

<!-- Використовуйте lang атрибут для вказівки мови -->
<p lang="en">This is English text.</p>
<p lang="ru">Це російський текст.</p>
````

### Основні принципи доступності:

1. **Сприймання**: інформація має бути подана у формі, яку користувачі можуть сприймати.
2. **Керування**: компоненти інтерфейсу повинні бути керованими.
3. **Зрозумілість**: інформація та операції мають бути зрозумілими.
4. **Надійність**: контент повинен бути достатньо надійним для інтерпретації різними користувачами агентами.

---
