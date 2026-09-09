<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CHAPTER STREET FOOD — Сочные бургеры и хот-доги в Караганде</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;800;900&display=swap" rel="stylesheet">
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    background: #0b0c0f url('bg.jpg') no-repeat center center fixed;
    background-size: cover;
    color: #fff;
    font-family: 'Montserrat', sans-serif;
    position: relative;
    overflow-x: hidden;
}

/* Яркий неоново-теплый оверлей для сочности */
body::before {
    content: "";
    position: fixed;
    inset: 0;
    background: radial-gradient(circle at 50% 20%, rgba(255, 92, 0, 0.22), rgba(11, 12, 15, 0.93) 70%);
    backdrop-filter: blur(5px);
    z-index: -1;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: auto;
}

/* HEADER */
header {
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
    background: rgba(11, 12, 15, 0.85);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid rgba(255, 92, 0, 0.2);
}

.nav {
    height: 75px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    font-size: 22px;
    font-weight: 900;
    letter-spacing: -0.5px;
    text-transform: uppercase;
    background: linear-gradient(45deg, #fff, #ff9f43);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.logo span {
    color: #ff5c00;
    -webkit-text-fill-color: #ff5c00;
}

.nav-links {
    display: flex;
    gap: 25px;
    color: #ccc;
    font-size: 14px;
    font-weight: 600;
}

.nav-links a:hover {
    color: #ff5c00;
    text-shadow: 0 0 10px rgba(255, 92, 0, 0.5);
}

.cart-btn {
    background: linear-gradient(135deg, #ff5c00, #ff8400);
    color: white;
    padding: 12px 22px;
    border-radius: 16px;
    font-weight: 800;
    border: none;
    cursor: pointer;
    box-shadow: 0 4px 20px rgba(255, 92, 0, 0.4);
    transition: all 0.3s ease;
}

.cart-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 25px rgba(255, 92, 0, 0.6);
}

/* HERO SECTION */
.hero {
    min-height: 85vh;
    display: flex;
    align-items: center;
    padding-top: 100px;
}

.hero-grid {
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    gap: 40px;
    align-items: center;
}

.hero-content {
    background: rgba(21, 23, 28, 0.75);
    padding: 45px;
    border-radius: 30px;
    border: 1px solid rgba(255, 92, 0, 0.3);
    backdrop-filter: blur(15px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.5);
}

.badge {
    display: inline-block;
    padding: 8px 16px;
    border: 1px solid rgba(255, 92, 0, 0.4);
    border-radius: 30px;
    color: #ff9f43;
    font-size: 13px;
    font-weight: 600;
    margin-bottom: 20px;
    background: rgba(255, 92, 0, 0.1);
}

.hero h1 {
    font-size: clamp(35px, 4.5vw, 55px);
    line-height: 1.1;
    font-weight: 900;
    letter-spacing: -1px;
}

.hero h1 span {
    background: linear-gradient(45deg, #ff5c00, #ffb143);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.hero p {
    margin-top: 20px;
    color: #ddd;
    font-size: 16px;
    line-height: 1.6;
}

/* ПРЕИМУЩЕСТВА (НОВОЕ) */
.features-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
}

.feature-card {
    background: rgba(21, 23, 28, 0.75);
    border: 1px solid rgba(255,255,255,0.08);
    padding: 20px;
    border-radius: 20px;
    backdrop-filter: blur(10px);
}

.feature-card h4 {
    color: #ff5c00;
    font-size: 16px;
    margin-bottom: 5px;
}

.feature-card p {
    color: #aaa;
    font-size: 13px;
}

/* MENU SECTION */
section {
    padding: 60px 0;
}

.section-title {
    font-size: 34px;
    font-weight: 900;
    letter-spacing: -1px;
    margin-bottom: 30px;
    color: #fff;
    display: flex;
    align-items: center;
    gap: 15px;
}

.section-title span {
    color: #ff5c00;
}

.section-title::after {
    content: "";
    flex: 1;
    height: 2px;
    background: linear-gradient(90deg, rgba(255,92,0,0.5), transparent);
}

.menu-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 25px;
}

.menu-card {
    background: rgba(21, 23, 28, 0.88);
    border: 1px solid rgba(255, 92, 0, 0.15);
    border-radius: 24px;
    padding: 25px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    backdrop-filter: blur(12px);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
}

.menu-card:hover {
    transform: translateY(-6px);
    border-color: rgba(255, 92, 0, 0.6);
    box-shadow: 0 15px 35px rgba(255, 92, 0, 0.2);
    background: rgba(25, 28, 35, 0.95);
}

.menu-info h3 {
    font-size: 20px;
    font-weight: 800;
    margin-bottom: 8px;
    color: #fff;
}

.menu-info p {
    color: #b0b0b0;
    font-size: 13px;
    line-height: 1.5;
    margin-bottom: 20px;
}

.menu-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-top: 1px solid rgba(255,255,255,0.06);
    padding-top: 15px;
}

.price {
    font-size: 20px;
    font-weight: 900;
    color: #ffb143;
}

.add-btn {
    background: rgba(255, 92, 0, 0.15);
    color: #ff5c00;
    border: 1px solid rgba(255, 92, 0, 0.3);
    padding: 9px 16px;
    border-radius: 12px;
    font-weight: 800;
    font-size: 13px;
    cursor: pointer;
    transition: all 0.2s;
}

.add-btn:hover {
    background: #ff5c00;
    color: white;
    box-shadow: 0 4px 15px rgba(255, 92, 0, 0.4);
}

/* О НАС / ИНФО БЛОК */
.about-section {
    background: rgba(21, 23, 28, 0.8);
    border: 1px solid rgba(255, 92, 0, 0.2);
    border-radius: 30px;
    padding: 45px;
    margin-top: 50px;
    backdrop-filter: blur(15px);
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 30px;
    text-align: center;
}

.about-item h3 {
    color: #ff5c00;
    font-size: 28px;
    font-weight: 900;
    margin-bottom: 8px;
}

.about-item p {
    color: #aaa;
    font-size: 14px;
    line-height: 1.4;
}

/* MODAL */
.modal {
    position: fixed;
    inset: 0;
    background: rgba(0, 0, 0, 0.85);
    backdrop-filter: blur(12px);
    display: none;
    align-items: center;
    justify-content: center;
    z-index: 2000;
    padding: 20px;
}

.modal.active {
    display: flex;
}

.modal-box {
    width: 100%;
    max-width: 500px;
    background: #15171c;
    border: 1px solid rgba(255, 92, 0, 0.4);
    border-radius: 28px;
    padding: 30px;
    max-height: 90vh;
    overflow-y: auto;
    box-shadow: 0 25px 50px rgba(0,0,0,0.7);
}

.close {
    float: right;
    background: none;
    border: none;
    color: #888;
    font-size: 28px;
    cursor: pointer;
    transition: color 0.2s;
}

.close:hover {
    color: #ff5c00;
}

.modal-box h3 {
    font-size: 24px;
    font-weight: 900;
    margin-bottom: 20px;
    color: #fff;
}

.cart-items {
    max-height: 180px;
    overflow-y: auto;
    margin-bottom: 15px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
    padding-bottom: 10px;
}

.cart-item {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
    font-size: 14px;
    color: #ccc;
    font-weight: 600;
}

.kaspi-box {
    background: rgba(0, 133, 255, 0.12);
    border: 1px solid rgba(0, 133, 255, 0.35);
    border-radius: 16px;
    padding: 15px;
    margin: 15px 0;
    font-size: 13px;
    color: #ddd;
    line-height: 1.5;
}

.kaspi-box strong {
    color: #38bdf8;
}

label {
    display: block;
    color: #aaa;
    font-size: 12px;
    font-weight: 600;
    margin-top: 10px;
    margin-bottom: 5px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

input {
    width: 100%;
    padding: 12px 16px;
    background: #0b0c0f;
    border: 1px solid rgba(255,255,255,0.12);
    color: white;
    border-radius: 14px;
    outline: none;
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    transition: border-color 0.2s;
}

input:focus {
    border-color: #ff5c00;
    box-shadow: 0 0 10px rgba(255, 92, 0, 0.3);
}

/* FOOTER */
footer {
    padding: 40px 0;
    border-top: 1px solid rgba(255,255,255,0.08);
    color: #777;
    font-size: 13px;
    text-align: center;
    background: rgba(11, 12, 15, 0.9);
}

@media(max-width: 900px) {
    .hero-grid { grid-template-columns: 1fr; }
    .menu-grid { grid-template-columns: 1fr; }
    .about-section { grid-template-columns: 1fr; }
    .features-grid { grid-template-columns: 1fr; }
    .nav-links { display: none; }
}
</style>
</head>
<body>

<header>
    <div class="container nav">
        <a href="#" class="logo">CHAPTER <span>STREET FOOD</span></a>
        <nav class="nav-links">
            <a href="#burgers">Бургеры</a>
            <a href="#hotdogs">Хот-доги</a>
            <a href="#combo">Комбо</a>
            <a href="#snackset">Снэки и напитки</a>
            <a href="#about">О нас</a>
        </nav>
        <button class="cart-btn" id="openCart">🛒 Корзина (<span id="cartCount">0</span>)</button>
    </div>
</header>

<main>
    <!-- HERO С ИНФОРМАЦИЕЙ И ПРЕИМУЩЕСТВАМИ -->
    <section class="hero">
        <div class="container hero-grid">
            <div class="hero-content">
                <div class="badge">📍 ул. Мустафина 24/1 • 11:00 - 23:00</div>
                <h1>У нас уютно,<br><span>вкусно и тепло</span> 🔥</h1>
                <p>Фирменный стритфуд в Караганде. Авторские рецепты, сочные котлеты из отборного мяса, свежие булочки и лучшие ингредиенты.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <h4>⚡ Быстро</h4>
                    <p>Готовим с любовью и отдаем заказ в кратчайшие сроки.</p>
                </div>
                <div class="feature-card">
                    <h4>🥩 100% Мясо</h4>
                    <p>Только свежие говяжьи котлеты и сосиски премиум класса.</p>
                </div>
                <div class="feature-card">
                    <h4>🥤 Напитки</h4>
                    <p>Фирменные милкшейки, освежающие морсы и согревающие чаи.</p>
                </div>
                <div class="feature-card">
                    <h4>🛵 Доставка</h4>
                    <p>Быстрая доставка по всему городу или самовывоз.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- БУРГЕРЫ -->
    <div class="container" id="burgers">
        <h2 class="section-title">Фирменные <span>Бургеры</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Вилладжио 🧀</h3>
                    <p>Говяжья котлета, соус Альфредо, картофельные рёсти, сыр моцарелла, красный лук, помидор</p>
                </div>
                <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Вилладжио', 2500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Франческо 🧀</h3>
                    <p>Отбивная из куриного филе, соус Руй, ананас, сыр, красный лук, помидор</p>
                </div>
                <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Франческо', 2500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Машрум 🍄</h3>
                    <p>Говяжья котлета, сливочно-грибной соус, шампиньоны, красный лук, помидор</p>
                </div>
                <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Машрум', 2500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Тарантино 🌶️</h3>
                    <p>Говяжья котлета, соус Тар-Тар, копченые колбаски, халапеньо, красный лук, помидор</p>
                </div>
                <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Тарантино', 2500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Итальяно 🧀</h3>
                    <p>Говяжья котлета, томленые томаты, сыр моцарелла, сладко-пряный соус, красный лук</p>
                </div>
                <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Итальяно', 2500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Чизи-Чиз 🧀</h3>
                    <p>Говяжья котлета, сливочный соус Альфредо, сыр Чеддер, сыр моцарелла, сыр, красный лук, помидор</p>
                </div>
                <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Чизи-Чиз', 2500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Классик 🧀</h3>
                    <p>Говяжья котлета, соус Руй, обжаренная курица, сыр, маринованные огурцы, красный лук, помидор</p>
                </div>
                <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Классик', 2500)">В корзину</button></div>
            </div>
        </div>
    </div>

    <!-- ХОТ-ДОГИ -->
    <div class="container" id="hotdogs" style="margin-top: 50px;">
        <h2 class="section-title">Сочные <span>Хот-доги</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Нью-Йорк</h3>
                    <p>Говяжья сосиска, обжаренная курица, маринованные огурцы, кетчуп, сладкий горчичный соус, чипсы</p>
                </div>
                <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Нью-Йорк', 1500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Тито</h3>
                    <p>Говяжья сосиска, чесночный соус, красный лук, помидор, болгарский перец, чипсы</p>
                </div>
                <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Тито', 1500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Лучано</h3>
                    <p>Говяжья сосиска, карамелизированный лук, соус барбекю, сладкий горчичный соус, чипсы</p>
                </div>
                <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Лучано', 1500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Чизус 🧀</h3>
                    <p>Говяжья сосиска, омлет, сыр, сырный соус, чипсы</p>
                </div>
                <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Чизус', 1500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Мачете 🌶️</h3>
                    <p>Говяжья сосиска, соус Тар-Тар, халапеньо, горчичный соус, чипсы</p>
                </div>
                <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Мачете', 1500)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Грибной 🍄</h3>
                    <p>Говяжья сосиска, сливочно-грибной соус, сырный соус, шампиньоны, чипсы</p>
                </div>
                <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Грибной', 1500)">В корзину</button></div>
            </div>
        </div>
    </div>

    <!-- КОМБО -->
    <div class="container" id="combo" style="margin-top: 50px;">
        <h2 class="section-title">Выгодные <span>Комбо наборы</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Макси Комбо</h3>
                    <p>Бургер на выбор + Хот-Дог на выбор + Морс / Чай / Газировка</p>
                </div>
                <div class="menu-bottom"><span class="price">3900 ₸</span><button class="add-btn" onclick="addToCart('Комбо: Бургер+Хот-Дог+Напиток', 3900)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Комбо Бургер</h3>
                    <p>Бургер на выбор + Фри (+соус) + Морс / Чай / Газировка</p>
                </div>
                <div class="menu-bottom"><span class="price">3400 ₸</span><button class="add-btn" onclick="addToCart('Комбо Бургер', 3400)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Комбо Хот-Дог</h3>
                    <p>Хот-Дог на выбор + Фри (+соус) + Морс / Чай / Газировка</p>
                </div>
                <div class="menu-bottom"><span class="price">2600 ₸</span><button class="add-btn" onclick="addToCart('Комбо Хот-Дог', 2600)">В корзину</button></div>
            </div>
        </div>
    </div>

    <!-- СНЭКИ И НАПИТКИ -->
    <div class="container" id="snackset" style="margin-top: 50px;">
        <h2 class="section-title">Снэки и <span>Напитки</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-info"><h3>Наггетсы (6 шт)</h3><p>Хрустящие куриные наггетсы в панировке</p></div>
                <div class="menu-bottom"><span class="price">1100 ₸</span><button class="add-btn" onclick="addToCart('Наггетсы 6 шт', 1100)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Картофель фри</h3><p>Золотистые картофельные палочки с солью</p></div>
                <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Картофель фри', 900)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Картофельные дольки</h3><p>Ароматные пряные дольки картофеля</p></div>
                <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Картофельные дольки', 900)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Милкшейк (350 мл)</h3><p>Клубничный / Ванильный / Snickers / Банановый / Шоколадный / Oreo</p></div>
                <div class="menu-bottom"><span class="price">1100 ₸</span><button class="add-btn" onclick="addToCart('Милкшейк', 1100)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Морс (350 мл)</h3><p>Фирменный освежающий ягодный морс</p></div>
                <div class="menu-bottom"><span class="price">600 ₸</span><button class="add-btn" onclick="addToCart('Морс 350мл', 600)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Чай (350 мл)</h3><p>Фруктовый / Ташкентский / Ягодный / Облепиховый</p></div>
                <div class="menu-bottom"><span class="price">600 ₸</span><button class="add-btn" onclick="addToCart('Чай 350мл', 600)">В корзину</button></div>
            </div>
        </div>
    </div>

    <!-- ДОПОЛНИТЕЛЬНАЯ ИНФОРМАЦИЯ О НАС -->
    <div class="container" id="about">
        <div class="about-section">
            <div class="about-item">
                <h3>11:00 — 23:00</h3>
                <p>Ежедневно без выходных и перерывов работаем для вас</p>
            </div>
            <div class="about-item">
                <h3>ул. Мустафина 24/1</h3>
                <p>Ждем вас в гости в нашем уютном заведении в Караганде</p>
            </div>
            <div class="about-item">
                <h3>+7 (775) 938-78-98</h3>
                <p>Рабочий номер для быстрых заказов и связи в WhatsApp</p>
            </div>
        </div>
    </div>
</main>

<footer>
    <div class="container" style="margin-top: 30px;">
        CHAPTER STREET FOOD • Караганда, ул. Мустафина 24/1 • Все права защищены © 2026
    </div>
</footer>

<!-- MODAL -->
<div class="modal" id="cartModal">
    <div class="modal-box">
        <button class="close" id="closeCart">×</button>
        <h3>Оформление заказа</h3>
        
        <div class="cart-items" id="cartItems">
            <p style="color: #666; font-size: 14px;">Корзина пуста</p>
        </div>
        
        <div style="font-weight: 900; font-size: 18px; margin-bottom: 15px; color: #ffb143;" id="cartTotal">Итого: 0 ₸</div>

        <div class="kaspi-box">
            💳 <strong>Оплата по номеру Kaspi Gold:</strong><br>
            Переведите точную сумму на рабочий номер: <strong>+7 (775) 938-78-98</strong><br>
            После оплаты нажмите кнопку отправки в WhatsApp и прикрепите скриншот чека.
        </div>

        <label>Ваше имя</label>
        <input id="clientName" placeholder="Введите ваше имя" />

        <label>Телефон / WhatsApp</label>
        <input id="clientPhone" placeholder="+7 700 000 00 00" />

        <label>Адрес доставки в Караганде</label>
        <input id="clientAddress" placeholder="Улица, дом, квартира" />

        <button class="cart-btn" style="width:100%; margin-top:20px; padding: 14px;" onclick="sendOrder()">Оплатил(а) • Отправить в WhatsApp</button>
    </div>
</div>

<script>
let cart = [];

const modal = document.getElementById("cartModal");
const openCartBtn = document.getElementById("openCart");
const closeCartBtn = document.getElementById("closeCart");
const cartCount = document.getElementById("cartCount");
const cartItems = document.getElementById("cartItems");
const cartTotal = document.getElementById("cartTotal");

openCartBtn.addEventListener("click", () => modal.classList.add("active"));
closeCartBtn.addEventListener("click", () => modal.classList.remove("active"));

function addToCart(name, price) {
    let item = cart.find(i => i.name === name);
    if (item) {
        item.qty++;
    } else {
        cart.push({ name, price, qty: 1 });
    }
    updateCartUI();
}

function updateCartUI() {
    cartCount.innerText = cart.reduce((sum, i) => sum + i.qty, 0);
    
    if (cart.length === 0) {
        cartItems.innerHTML = `<p style="color: #666; font-size: 14px;">Корзина пуста</p>`;
        cartTotal.innerText = "Итого: 0 ₸";
        return;
    }

    let html = "";
    let total = 0;
    cart.forEach(i => {
        total += i.price * i.qty;
        html += `<div class="cart-item"><span>${i.name} x${i.qty}</span> <span>${i.price * i.qty} ₸</span></div>`;
    });
    cartItems.innerHTML = html;
    cartTotal.innerText = `Итого: ${total} ₸`;
}

function sendOrder() {
    let name = document.getElementById("clientName").value.trim();
    let phone = document.getElementById("clientPhone").value.trim();
    let address = document.getElementById("clientAddress").value.trim();

    if (cart.length === 0) {
        alert("Добавьте блюда в корзину.");
        return;
    }
    if (!name || !phone || !address) {
        alert("Заполните имя, телефон и адрес доставки.");
        return;
    }

    let total = cart.reduce((sum, i) => sum + (i.price * i.qty), 0);
    let text = `🍔 НОВЫЙ ЗАКАЗ (CHAPTER STREET FOOD)\n\n`;
    cart.forEach(i => {
        text += `- ${i.name} x${i.qty} (${i.price * i.qty} ₸)\n`;
    });
    text += `\n💰 Итого к оплате: ${total} ₸\n💳 Оплата через Kaspi выполнена\n\n👤 Имя: ${name}\n📞 Телефон: ${phone}\n📍 Адрес: ${address}\n\n*(Обязательно прикрепите скриншот чека из Kaspi)*`;

    let myPhone = "77759387898";
    window.open(`https://wa.me/${myPhone}?text=${encodeURIComponent(text)}`, "_blank");
}
</script>

</body>
</html>
