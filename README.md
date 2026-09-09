<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CHAPTER STREET FOOD — Сочные бургеры и хот-доги в Караганде</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800;900&display=swap" rel="stylesheet">
<style>
:root {
    --primary: #ff471a;
    --primary-glow: rgba(255, 71, 26, 0.4);
    --accent: #ffb143;
    --dark: #0f1015;
    --card-bg: rgba(20, 22, 28, 0.85);
    --border: rgba(255, 177, 67, 0.2);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    background: #090a0f;
    color: #fff;
    font-family: 'Montserrat', sans-serif;
    position: relative;
    overflow-x: hidden;
}

/* Живой аппетитный фон с теплыми лучами */
body::before {
    content: "";
    position: fixed;
    inset: 0;
    background: 
        radial-gradient(circle at 10% 20%, rgba(255, 71, 26, 0.18) 0%, transparent 40%),
        radial-gradient(circle at 90% 80%, rgba(255, 177, 67, 0.15) 0%, transparent 40%),
        radial-gradient(circle at 50% 50%, rgba(15, 16, 21, 0.95) 0%, #090a0f 100%);
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
    background: rgba(15, 16, 21, 0.85);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid rgba(255, 177, 67, 0.15);
}

.nav {
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    font-size: 24px;
    font-weight: 900;
    letter-spacing: -0.5px;
    text-transform: uppercase;
    background: linear-gradient(45deg, #fff, #ffb143);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.logo span {
    background: linear-gradient(45deg, #ff471a, #ffb143);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.nav-links {
    display: flex;
    gap: 30px;
    color: #d1d5db;
    font-size: 14px;
    font-weight: 600;
}

.nav-links a {
    text-decoration: none;
    color: inherit;
    transition: color 0.2s;
}

.nav-links a:hover {
    color: var(--accent);
    text-shadow: 0 0 12px var(--primary-glow);
}

.cart-btn {
    background: linear-gradient(135deg, #ff471a, #ff6b3d);
    color: white;
    padding: 12px 24px;
    border-radius: 16px;
    font-weight: 800;
    border: none;
    cursor: pointer;
    box-shadow: 0 4px 20px var(--primary-glow);
    transition: all 0.3s ease;
}

.cart-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 25px rgba(255, 71, 26, 0.6);
}

/* HERO SECTION С БОЛЬШИМ АППЕТИТНЫМ БИЛДЕРОВ */
.hero {
    min-height: 90vh;
    display: flex;
    align-items: center;
    padding-top: 110px;
    position: relative;
}

.hero-grid {
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 50px;
    align-items: center;
}

.hero-content {
    background: var(--card-bg);
    padding: 50px;
    border-radius: 32px;
    border: 1px solid var(--border);
    backdrop-filter: blur(15px);
    box-shadow: 0 25px 50px rgba(0,0,0,0.6);
}

.badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 18px;
    border: 1px solid rgba(255, 177, 67, 0.4);
    border-radius: 30px;
    color: var(--accent);
    font-size: 13px;
    font-weight: 700;
    margin-bottom: 20px;
    background: rgba(255, 177, 67, 0.08);
}

.hero h1 {
    font-size: clamp(36px, 4.5vw, 56px);
    line-height: 1.1;
    font-weight: 900;
    letter-spacing: -1px;
}

.hero h1 span {
    background: linear-gradient(45deg, #ff471a, #ffb143);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.hero p {
    margin-top: 20px;
    color: #9ca3af;
    font-size: 16px;
    line-height: 1.6;
}

/* СЕТКА ИГРЕДИЕНТОВ И СТРИТФУДА С АППЕТИТНЫМИ ФОТО-ИЛЛЮСТРАЦИЯМИ */
.food-showcase {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
}

.food-card-preview {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 24px;
    overflow: hidden;
    backdrop-filter: blur(12px);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    box-shadow: 0 15px 35px rgba(0,0,0,0.4);
    position: relative;
}

.food-card-preview:hover {
    transform: translateY(-8px) scale(1.02);
    border-color: rgba(255, 71, 26, 0.6);
    box-shadow: 0 20px 40px rgba(255, 71, 26, 0.25);
}

.food-card-img {
    height: 130px;
    width: 100%;
    object-fit: cover;
    border-bottom: 1px solid var(--border);
}

.food-card-body {
    padding: 16px;
}

.food-card-body h4 {
    color: var(--accent);
    font-size: 15px;
    font-weight: 800;
    margin-bottom: 4px;
}

.food-card-body p {
    color: #9ca3af;
    font-size: 11px;
    line-height: 1.4;
}

/* MENU SECTION */
section {
    padding: 70px 0;
}

.section-title {
    font-size: 34px;
    font-weight: 900;
    letter-spacing: -1px;
    margin-bottom: 35px;
    color: #fff;
    display: flex;
    align-items: center;
    gap: 15px;
}

.section-title span {
    background: linear-gradient(45deg, #ff471a, #ffb143);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.section-title::after {
    content: "";
    flex: 1;
    height: 2px;
    background: linear-gradient(90deg, rgba(255, 71, 26, 0.5), transparent);
}

.menu-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 30px;
}

.menu-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 26px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    backdrop-filter: blur(12px);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    box-shadow: 0 15px 35px rgba(0,0,0,0.4);
}

.menu-card:hover {
    transform: translateY(-8px);
    border-color: rgba(255, 71, 26, 0.7);
    box-shadow: 0 20px 45px rgba(255, 71, 26, 0.3);
}

.menu-img-wrap {
    width: 100%;
    height: 190px;
    overflow: hidden;
    position: relative;
}

.menu-img-wrap img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.menu-card:hover .menu-img-wrap img {
    transform: scale(1.08);
}

.menu-content-box {
    padding: 24px;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    justify-content: space-between;
}

.menu-info h3 {
    font-size: 20px;
    font-weight: 800;
    margin-bottom: 8px;
    color: #fff;
}

.menu-info p {
    color: #9ca3af;
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
    font-size: 21px;
    font-weight: 900;
    color: var(--accent);
}

.add-btn {
    background: rgba(255, 71, 26, 0.15);
    color: #ff6b3d;
    border: 1px solid rgba(255, 71, 26, 0.4);
    padding: 10px 18px;
    border-radius: 14px;
    font-weight: 800;
    font-size: 13px;
    cursor: pointer;
    transition: all 0.2s;
}

.add-btn:hover {
    background: var(--primary);
    color: white;
    box-shadow: 0 4px 15px var(--primary-glow);
}

/* О НАС / ИНФО БЛОК */
.about-section {
    background: var(--card-bg);
    border: 1px solid var(--border);
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
    color: var(--primary);
    font-size: 26px;
    font-weight: 900;
    margin-bottom: 8px;
}

.about-item p {
    color: #9ca3af;
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
    background: #14161c;
    border: 1px solid rgba(255, 177, 67, 0.4);
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
    color: var(--primary);
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
    color: #d1d5db;
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
    color: #9ca3af;
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
    background: #090a0f;
    border: 1px solid rgba(255,255,255,0.12);
    color: white;
    border-radius: 14px;
    outline: none;
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    transition: border-color 0.2s;
}

input:focus {
    border-color: var(--primary);
    box-shadow: 0 0 10px var(--primary-glow);
}

/* FOOTER */
footer {
    padding: 40px 0;
    border-top: 1px solid rgba(255,255,255,0.08);
    color: #6b7280;
    font-size: 13px;
    text-align: center;
    background: rgba(15, 16, 21, 0.9);
}

@media(max-width: 900px) {
    .hero-grid { grid-template-columns: 1fr; }
    .menu-grid { grid-template-columns: 1fr; }
    .about-section { grid-template-columns: 1fr; }
    .food-showcase { grid-template-columns: 1fr; }
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
    <!-- HERO С АППЕТИТНЫМИ ПРЕВЬЮ ПРЕДМЕТОВ -->
    <section class="hero">
        <div class="container hero-grid">
            <div class="hero-content">
                <div class="badge">🔥 ул. Мустафина 24/1 • 11:00 - 23:00</div>
                <h1>Сочится соком,<br><span>манит ароматом</span> 🍔</h1>
                <p>Фирменный стритфуд в Караганде. Авторские рецепты, сочные котлеты из отборного мяса на гриле, тягучий сыр и хрустящая корочка.</p>
            </div>
            
            <!-- АППЕТИТНЫЕ ВИЗУАЛЬНЫЕ ПРЕДМЕТЫ -->
            <div class="food-showcase">
                <div class="food-card-preview">
                    <img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=500&q=80" alt="Бургер" class="food-card-img">
                    <div class="food-card-body">
                        <h4>Крафтовая булка</h4>
                        <p>С пылу с жару, подрумяненная на масле.</p>
                    </div>
                </div>
                <div class="food-card-preview">
                    <img src="https://images.unsplash.com/photo-1550547660-d9450f859349?auto=format&fit=crop&w=500&q=80" alt="Мясо гриль" class="food-card-img">
                    <div class="food-card-body">
                        <h4>Мраморный гриль</h4>
                        <p>Сочная говядина с дымком и специями.</p>
                    </div>
                </div>
                <div class="food-card-preview">
                    <img src="https://images.unsplash.com/photo-1573080496219-bb080dd4f877?auto=format&fit=crop&w=500&q=80" alt="Фри" class="food-card-img">
                    <div class="food-card-body">
                        <h4>Хрустящий фри</h4>
                        <p>Золотистые картофельные ломтики.</p>
                    </div>
                </div>
                <div class="food-card-preview">
                    <img src="https://images.unsplash.com/photo-1541658016709-82535e94bc69?auto=format&fit=crop&w=500&q=80" alt="Милкшейк" class="food-card-img">
                    <div class="food-card-body">
                        <h4>Ледяные шейки</h4>
                        <p>Густые милкшейки со взбитыми сливками.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- БУРГЕРЫ -->
    <div class="container" id="burgers">
        <h2 class="section-title">Фирменные <span>Бургеры</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80" alt="Вилладжио">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Вилладжио 🧀</h3>
                        <p>Говяжья котлета, соус Альфредо, картофельные рёсти, сыр моцарелла, красный лук, помидор</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Вилладжио', 2500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1625813506062-0aeb1d7a094b?auto=format&fit=crop&w=600&q=80" alt="Франческо">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Франческо 🧀</h3>
                        <p>Отбивная из куриного филе, соус Руй, ананас, сыр, красный лук, помидор</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Франческо', 2500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1586190848861-99aa4a171e90?auto=format&fit=crop&w=600&q=80" alt="Машрум">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Машрум 🍄</h3>
                        <p>Говяжья котлета, сливочно-грибной соус, шампиньоны, красный лук, помидор</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Машрум', 2500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1550547660-d9450f859349?auto=format&fit=crop&w=600&q=80" alt="Тарантино">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Тарантино 🌶️</h3>
                        <p>Говяжья котлета, соус Тар-Тар, копченые колбаски, халапеньо, красный лук, помидор</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Тарантино', 2500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1594212699903-ec8a3eca50f5?auto=format&fit=crop&w=600&q=80" alt="Итальяно">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Итальяно 🧀</h3>
                        <p>Говяжья котлета, томленые томаты, сыр моцарелла, сладко-пряный соус, красный лук</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Итальяно', 2500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1582196016297-f5c9bb0d473a?auto=format&fit=crop&w=600&q=80" alt="Чизи-Чиз">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Чизи-Чиз 🧀</h3>
                        <p>Говяжья котлета, сливочный соус Альфредо, сыр Чеддер, сыр моцарелла, сыр, красный лук, помидор</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Чизи-Чиз', 2500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1572802419224-296b0aeee0d9?auto=format&fit=crop&w=600&q=80" alt="Классик">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Классик 🧀</h3>
                        <p>Говяжья котлета, соус Руй, обжаренная курица, сыр, маринованные огурцы, красный лук, помидор</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2500 ₸</span><button class="add-btn" onclick="addToCart('Бургер Классик', 2500)">В корзину</button></div>
                </div>
            </div>
        </div>
    </div>

    <!-- ХОТ-ДОГИ -->
    <div class="container" id="hotdogs" style="margin-top: 50px;">
        <h2 class="section-title">Сочные <span>Хот-доги</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1619740455993-9e612b1af08a?auto=format&fit=crop&w=600&q=80" alt="Нью-Йорк">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Нью-Йорк</h3>
                        <p>Говяжья сосиска, обжаренная курица, маринованные огурцы, кетчуп, сладкий горчичный соус, чипсы</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Нью-Йорк', 1500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1627308595229-7830a5c91f9f?auto=format&fit=crop&w=600&q=80" alt="Тито">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Тито</h3>
                        <p>Говяжья сосиска, чесночный соус, красный лук, помидор, болгарский перец, чипсы</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Тито', 1500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1541214113247-2195a6ad17d4?auto=format&fit=crop&w=600&q=80" alt="Лучано">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Лучано</h3>
                        <p>Говяжья сосиска, карамелизированный лук, соус барбекю, сладкий горчичный соус, чипсы</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Лучано', 1500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1585238342024-78d387f4a707?auto=format&fit=crop&w=600&q=80" alt="Чизус">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Чизус 🧀</h3>
                        <p>Говяжья сосиска, омлет, сыр, сырный соус, чипсы</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Чизус', 1500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1619740455993-9e612b1af08a?auto=format&fit=crop&w=600&q=80" alt="Мачете">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Мачете 🌶️</h3>
                        <p>Говяжья сосиска, соус Тар-Тар, халапеньо, горчичный соус, чипсы</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Мачете', 1500)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1541214113247-2195a6ad17d4?auto=format&fit=crop&w=600&q=80" alt="Грибной">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Грибной 🍄</h3>
                        <p>Говяжья сосиска, сливочно-грибной соус, сырный соус, шампиньоны, чипсы</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1500 ₸</span><button class="add-btn" onclick="addToCart('Хот-дог Грибной', 1500)">В корзину</button></div>
                </div>
            </div>
        </div>
    </div>

    <!-- КОМБО -->
    <div class="container" id="combo" style="margin-top: 50px;">
        <h2 class="section-title">Выгодные <span>Комбо наборы</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1594212699903-ec8a3eca50f5?auto=format&fit=crop&w=600&q=80" alt="Макси Комбо">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Макси Комбо</h3>
                        <p>Бургер на выбор + Хот-Дог на выбор + Морс / Чай / Газировка</p>
                    </div>
                    <div class="menu-bottom"><span class="price">3900 ₸</span><button class="add-btn" onclick="addToCart('Комбо: Бургер+Хот-Дог+Напиток', 3900)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1550547660-d9450f859349?auto=format&fit=crop&w=600&q=80" alt="Комбо Бургер">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Комбо Бургер</h3>
                        <p>Бургер на выбор + Фри (+соус) + Морс / Чай / Газировка</p>
                    </div>
                    <div class="menu-bottom"><span class="price">3400 ₸</span><button class="add-btn" onclick="addToCart('Комбо Бургер', 3400)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80" alt="Комбо Хот-Дог">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Комбо Хот-Дог</h3>
                        <p>Хот-Дог на выбор + Фри (+соус) + Морс / Чай / Газировка</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2600 ₸</span><button class="add-btn" onclick="addToCart('Комбо Хот-Дог', 2600)">В корзину</button></div>
                </div>
            </div>
        </div>
    </div>

    <!-- СНЭКИ И НАПИТКИ -->
    <div class="container" id="snackset" style="margin-top: 50px;">
        <h2 class="section-title">Снэки и <span>Напитки</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1562967914-608f82629710?auto=format&fit=crop&w=600&q=80" alt="Наггетсы">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info"><h3>Наггетсы (6 шт)</h3><p>Хрустящие куриные наггетсы в панировке</p></div>
                    <div class="menu-bottom"><span class="price">1100 ₸</span><button class="add-btn" onclick="addToCart('Наггетсы 6 шт', 1100)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1573080496219-bb080dd4f877?auto=format&fit=crop&w=600&q=80" alt="Картофель фри">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info"><h3>Картофель фри</h3><p>Золотистые картофельные палочки с солью</p></div>
                    <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Картофель фри', 900)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1630384060421-cb20d0e0649d?auto=format&fit=crop&w=600&q=80" alt="Дольки">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info"><h3>Картофельные дольки</h3><p>Ароматные пряные дольки картофеля</p></div>
                    <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Картофельные дольки', 900)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1541658016709-82535e94bc69?auto=format&fit=crop&w=600&q=80" alt="Милкшейк">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info"><h3>Милкшейк (350 мл)</h3><p>Клубничный / Ванильный / Snickers / Банановый / Шоколадный / Oreo</p></div>
                    <div class="menu-bottom"><span class="price">1100 ₸</span><button class="add-btn" onclick="addToCart('Милкшейк', 1100)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1513558161293-cdaf765ed2fd?auto=format&fit=crop&w=600&q=80" alt="Морс">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info"><h3>Морс (350 мл)</h3><p>Фирменный освежающий ягодный морс</p></div>
                    <div class="menu-bottom"><span class="price">600 ₸</span><button class="add-btn" onclick="addToCart('Морс 350мл', 600)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap">
                    <img src="https://images.unsplash.com/photo-1576092768241-dec231879fc3?auto=format&fit=crop&w=600&q=80" alt="Чай">
                </div>
                <div class="menu-content-box">
                    <div class="menu-info"><h3>Чай (350 мл)</h3><p>Фруктовый / Ташкентский / Ягодный / Облепиховый</p></div>
                    <div class="menu-bottom"><span class="price">600 ₸</span><button class="add-btn" onclick="addToCart('Чай 350мл', 600)">В корзину</button></div>
                </div>
            </div>
        </div>
    </div>

    <!-- ИНФО О НАС -->
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
        
        <div style="font-weight: 900; font-size: 18px; margin-bottom: 15px; color: var(--accent);" id="cartTotal">Итого: 0 ₸</div>

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
