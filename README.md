<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CHAPTER STREET FOOD — Меню Караганда</title>
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
    font-size: 22px;
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
    gap: 20px;
    color: #d1d5db;
    font-size: 13px;
    font-weight: 600;
}

.nav-links a {
    text-decoration: none;
    color: inherit;
    transition: color 0.2s;
}

.nav-links a:hover {
    color: var(--accent);
}

.cart-btn {
    background: linear-gradient(135deg, #ff471a, #ff6b3d);
    color: white;
    padding: 10px 20px;
    border-radius: 14px;
    font-weight: 800;
    border: none;
    cursor: pointer;
    box-shadow: 0 4px 20px var(--primary-glow);
    transition: all 0.3s ease;
}

.cart-btn:hover {
    transform: translateY(-2px);
}

.hero {
    min-height: 80vh;
    display: flex;
    align-items: center;
    padding-top: 110px;
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
    font-size: clamp(34px, 4.5vw, 52px);
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
    font-size: 15px;
    line-height: 1.6;
}

.hero-banner-img {
    width: 100%;
    height: 380px;
    object-fit: cover;
    border-radius: 28px;
    border: 1px solid var(--border);
    box-shadow: 0 20px 40px rgba(0,0,0,0.5);
}

section {
    padding: 60px 0;
}

.section-title {
    font-size: 32px;
    font-weight: 900;
    letter-spacing: -1px;
    margin-bottom: 30px;
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
    gap: 25px;
}

.menu-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 24px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    backdrop-filter: blur(12px);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    box-shadow: 0 15px 35px rgba(0,0,0,0.4);
}

.menu-card:hover {
    transform: translateY(-6px);
    border-color: rgba(255, 71, 26, 0.7);
    box-shadow: 0 20px 45px rgba(255, 71, 26, 0.25);
}

.menu-img-wrap {
    width: 100%;
    height: 180px;
    overflow: hidden;
    position: relative;
    background: #000;
}

.menu-img-wrap img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.menu-card:hover .menu-img-wrap img {
    transform: scale(1.06);
}

.menu-content-box {
    padding: 20px;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    justify-content: space-between;
}

.menu-info h3 {
    font-size: 18px;
    font-weight: 800;
    margin-bottom: 6px;
    color: #fff;
}

.menu-info p {
    color: #9ca3af;
    font-size: 12px;
    line-height: 1.5;
    margin-bottom: 15px;
}

.menu-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-top: 1px solid rgba(255,255,255,0.06);
    padding-top: 12px;
}

.price {
    font-size: 19px;
    font-weight: 900;
    color: var(--accent);
}

.add-btn {
    background: rgba(255, 71, 26, 0.15);
    color: #ff6b3d;
    border: 1px solid rgba(255, 71, 26, 0.4);
    padding: 8px 14px;
    border-radius: 12px;
    font-weight: 800;
    font-size: 12px;
    cursor: pointer;
    transition: all 0.2s;
}

.add-btn:hover {
    background: var(--primary);
    color: white;
    box-shadow: 0 4px 15px var(--primary-glow);
}

.about-section {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 28px;
    padding: 40px;
    margin-top: 40px;
    backdrop-filter: blur(15px);
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 25px;
    text-align: center;
}

.about-item h3 {
    color: var(--primary);
    font-size: 24px;
    font-weight: 900;
    margin-bottom: 6px;
}

.about-item p {
    color: #9ca3af;
    font-size: 13px;
    line-height: 1.4;
}

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
    max-width: 480px;
    background: #14161c;
    border: 1px solid rgba(255, 177, 67, 0.4);
    border-radius: 24px;
    padding: 25px;
    max-height: 90vh;
    overflow-y: auto;
    box-shadow: 0 25px 50px rgba(0,0,0,0.7);
}

.close {
    float: right;
    background: none;
    border: none;
    color: #888;
    font-size: 26px;
    cursor: pointer;
}

.close:hover {
    color: var(--primary);
}

.modal-box h3 {
    font-size: 22px;
    font-weight: 900;
    margin-bottom: 15px;
    color: #fff;
}

.cart-items {
    max-height: 160px;
    overflow-y: auto;
    margin-bottom: 15px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
    padding-bottom: 10px;
}

.cart-item {
    display: flex;
    justify-content: space-between;
    margin-bottom: 8px;
    font-size: 13px;
    color: #d1d5db;
    font-weight: 600;
}

.kaspi-box {
    background: rgba(0, 133, 255, 0.12);
    border: 1px solid rgba(0, 133, 255, 0.35);
    border-radius: 14px;
    padding: 14px;
    margin: 14px 0;
    font-size: 12px;
    color: #ddd;
    line-height: 1.5;
}

.kaspi-box strong {
    color: #38bdf8;
}

label {
    display: block;
    color: #9ca3af;
    font-size: 11px;
    font-weight: 600;
    margin-top: 10px;
    margin-bottom: 4px;
    text-transform: uppercase;
}

input {
    width: 100%;
    padding: 10px 14px;
    background: #090a0f;
    border: 1px solid rgba(255,255,255,0.12);
    color: white;
    border-radius: 12px;
    outline: none;
    font-family: 'Montserrat', sans-serif;
    font-size: 13px;
}

input:focus {
    border-color: var(--primary);
}

footer {
    padding: 30px 0;
    border-top: 1px solid rgba(255,255,255,0.08);
    color: #6b7280;
    font-size: 13px;
    text-align: center;
    background: rgba(15, 16, 21, 0.9);
}

.footer-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
}

.insta-link {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    color: #fff;
    text-decoration: none;
    font-weight: 700;
    background: linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888);
    padding: 8px 16px;
    border-radius: 50px;
    font-size: 13px;
    transition: transform 0.2s, opacity 0.2s;
    box-shadow: 0 4px 15px rgba(220, 39, 67, 0.3);
}

.insta-link:hover {
    transform: translateY(-2px);
    opacity: 0.9;
}

.insta-link svg {
    width: 18px;
    height: 18px;
    fill: #fff;
}

@media(max-width: 900px) {
    .hero-grid { grid-template-columns: 1fr; }
    .menu-grid { grid-template-columns: 1fr; }
    .about-section { grid-template-columns: 1fr; }
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
            <a href="#snacks">Закуски</a>
            <a href="#shakes">Милкшейки</a>
            <a href="#drinks">Напитки</a>
            <a href="#about">О нас</a>
        </nav>
        <button class="cart-btn" id="openCart">🛒 Корзина (<span id="cartCount">0</span>)</button>
    </div>
</header>

<main>
    <section class="hero">
        <div class="container hero-grid">
            <div class="hero-content">
                <div class="badge">🔥 ул. Мустафина 24/1 • 11:00 - 23:00</div>
                <h1>Сочное мясо,<br><span>фирменный стритфуд</span> 🍔</h1>
                <p>Лучшие бургеры, хот-доги, хрустящие закуски и густые милкшейки в Караганде. Свежие ингредиенты и авторские соусы.</p>
            </div>
            <div>
                <!-- Общее фото для всех бургеров -->
                <img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=800&q=80" alt="Бургер Chapter" class="hero-banner-img">
            </div>
        </div>
    </section>

    <!-- БУРГЕРЫ (одна фото на все позиции) -->
    <div class="container" id="burgers">
        <h2 class="section-title">Фирменные <span>Бургеры</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80" alt="Бургеры"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Бургер "Вилладжио" 🧀</h3>
                        <p>Говяжья котлета, соус Альфредо, картофельные рёсти, сыр моцарелла, красный лук, помидор.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2300 ₸</span><button class="add-btn" onclick="addToCart('Бургер Вилладжио', 2300)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80" alt="Бургеры"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Бургер "Франческо" 🧀</h3>
                        <p>Отбивная из куриного филе, соус Руй, ананас, сыр, красный лук, помидор.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2300 ₸</span><button class="add-btn" onclick="addToCart('Бургер Франческо', 2300)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80" alt="Бургеры"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Бургер "Машрум" 🍄</h3>
                        <p>Говяжья котлета, сливочно-грибной соус, шампиньоны, красный лук, помидор.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2300 ₸</span><button class="add-btn" onclick="addToCart('Бургер Машрум', 2300)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80" alt="Бургеры"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Бургер "Тарантино" 🌶️</h3>
                        <p>Говяжья котлета, соус Тар-Тар, копченые колбаски, халапеньо, красный лук, помидор.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2300 ₸</span><button class="add-btn" onclick="addToCart('Бургер Тарантино', 2300)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80" alt="Бургеры"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Бургер "Итальяно" 🧀</h3>
                        <p>Говяжья котлета, томленые томаты, сыр моцарелла, сладко-пряный соус, красный лук.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2300 ₸</span><button class="add-btn" onclick="addToCart('Бургер Итальяно', 2300)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80" alt="Бургеры"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Бургер "Чизи-Чиз" 🧀</h3>
                        <p>Говяжья котлета, сливочный соус Альфредо, сыр Чеддер, сыр моцарелла, красный лук, помидор.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">2300 ₸</span><button class="add-btn" onclick="addToCart('Бургер Чизи-Чиз', 2300)">В корзину</button></div>
                </div>
            </div>
        </div>
    </div>

    <!-- ХОТ-ДОГИ (единая фото хот-дога на все хот-доги) -->
    <div class="container" id="hotdogs" style="margin-top: 40px;">
        <h2 class="section-title">Сочные <span>Хот-доги</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1619740455993-9e412b1af1c1?auto=format&fit=crop&w=600&q=80" alt="Хот-доги"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Хот-дог "New York"</h3>
                        <p>Говяжья сосиска, обжаренная курица, маринованные огурцы, кетчуп, горчичный соус, хрустящие чипсы.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1400 ₸</span><button class="add-btn" onclick="addToCart('Хот дог New York', 1400)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1619740455993-9e412b1af1c1?auto=format&fit=crop&w=600&q=80" alt="Хот-доги"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Хот-дог "Лучано"</h3>
                        <p>Говяжья сосиска, карамелизированный лук, соус барбекю, сладкий горчичный соус, чипсы.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1400 ₸</span><button class="add-btn" onclick="addToCart('Хот дог Лучано', 1400)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1619740455993-9e412b1af1c1?auto=format&fit=crop&w=600&q=80" alt="Хот-доги"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Хот-дог "Чизус" 🧀</h3>
                        <p>Говяжья сосиска, нежный омлет, сыр, фирменный сырный соус, хрустящие чипсы.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1400 ₸</span><button class="add-btn" onclick="addToCart('Хот дог Чизус', 1400)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1619740455993-9e412b1af1c1?auto=format&fit=crop&w=600&q=80" alt="Хот-доги"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Хот-дог "Грибной" 🍄</h3>
                        <p>Говяжья сосиска, сливочно-грибной соус, сырный соус, шампиньоны, чипсы.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1400 ₸</span><button class="add-btn" onclick="addToCart('Хот дог Грибной', 1400)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1619740455993-9e412b1af1c1?auto=format&fit=crop&w=600&q=80" alt="Хот-доги"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Хот-дог "Тито" 🔥</h3>
                        <p>Фирменная сосиска, специальный авторский соус, хрустящий лук фри в золотистой булочке.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">1400 ₸</span><button class="add-btn" onclick="addToCart('Хот дог Тито', 1400)">В корзину</button></div>
                </div>
            </div>
        </div>
    </div>

    <!-- ЗАКУСКИ -->
    <div class="container" id="snacks" style="margin-top: 40px;">
        <h2 class="section-title">Хрустящие <span>Закуски</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1573080496219-bb080dd4f877?auto=format&fit=crop&w=600&q=80" alt="Картофель Фри"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Картофель Фри 🍟</h3>
                        <p>Золотистые картофельные ломтики с хрустящей корочкой и солью.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">700 ₸</span><button class="add-btn" onclick="addToCart('Картофель Фри', 700)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1562967914-608f82629710?auto=format&fit=crop&w=600&q=80" alt="Наггетсы"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Куриные Наггетсы 🍗</h3>
                        <p>Сочное куриное филе в хрустящей панировке, обжаренное до золотистого цвета.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Наггетсы', 900)">В корзину</button></div>
                </div>
            </div>
        </div>
    </div>

    <!-- МИЛКШЕЙКИ (единая фото милкшейка на все шейки) -->
    <div class="container" id="shakes" style="margin-top: 40px;">
        <h2 class="section-title">Густые <span>Милкшейки</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1572490122747-3968b75cc699?auto=format&fit=crop&w=600&q=80" alt="Милкшейк"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Милкшейк "Ваниль" 🍦</h3>
                        <p>Классический густой молочный коктейль с ванильным вкусом и шапкой из взбитых сливок.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Милкшейк Ваниль', 900)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1572490122747-3968b75cc699?auto=format&fit=crop&w=600&q=80" alt="Милкшейк"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Милкшейк "Клубничный" 🍓</h3>
                        <p>Нежный молочный коктейль с ароматным клубничным сиропом и взбитыми сливками.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Милкшейк Клубничный', 900)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1572490122747-3968b75cc699?auto=format&fit=crop&w=600&q=80" alt="Милкшейк"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Милкшейк "Сникерс" 🍫</h3>
                        <p>Насыщенный шоколадно-ореховый коктейль со взбитыми сливками и карамельным топпингом.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Милкшейк Сникерс', 900)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1572490122747-3968b75cc699?auto=format&fit=crop&w=600&q=80" alt="Милкшейк"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Милкшейк "Шоколад" 🍫</h3>
                        <p>Глубокий шоколадный вкус, густая текстура и пышная шапка из взбитых сливок.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Милкшейк Шоколад', 900)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1572490122747-3968b75cc699?auto=format&fit=crop&w=600&q=80" alt="Милкшейк"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Милкшейк "Oreo" 🍪</h3>
                        <p>Культовый коктейль с дробленым печеньем Oreo, сливками и шоколадной крошкой.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Милкшейк Oreo', 900)">В корзину</button></div>
                </div>
            </div>
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1572490122747-3968b75cc699?auto=format&fit=crop&w=600&q=80" alt="Милкшейк"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Милкшейк "Банановый" 🍌</h3>
                        <p>Сладкий сливочно-банановый милкшейк со взбитыми сливками.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Милкшейк Банановый', 900)">В корзину</button></div>
                </div>
            </div>
        </div>
    </div>

    <!-- НАПИТКИ -->
    <div class="container" id="drinks" style="margin-top: 40px;">
        <h2 class="section-title">Освежающие <span>Напитки</span></h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-img-wrap"><img src="https://images.unsplash.com/photo-1513558161293-cdaf765ed2fd?auto=format&fit=crop&w=600&q=80" alt="Морс"></div>
                <div class="menu-content-box">
                    <div class="menu-info">
                        <h3>Фирменный Морс 🥤</h3>
                        <p>Натуральный ягодный морс собственного приготовления в удобной бутылочке.</p>
                    </div>
                    <div class="menu-bottom"><span class="price">600 ₸</span><button class="add-btn" onclick="addToCart('Фирменный Морс', 600)">В корзину</button></div>
                </div>
            </div>
        </div>
    </div>

    <div class="container" id="about">
        <div class="about-section">
            <div class="about-item">
                <h3>11:00 — 23:00</h3>
                <p>Работаем ежедневно без перерывов</p>
            </div>
            <div class="about-item">
                <h3>ул. Мустафина 24/1</h3>
                <p>Ждем вас в Караганде</p>
            </div>
            <div class="about-item">
                <h3>+7 (775) 938-78-98</h3>
                <p>Номер для заказов и WhatsApp</p>
            </div>
        </div>
    </div>
</main>

<footer>
    <div class="container footer-content">
        <a href="https://www.instagram.com/chapter_streetfood?stkn=ZThrMGs1OWZtYXdy" target="_blank" class="insta-link">
            <svg viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
            Мы в Instagram
        </a>
        <span>CHAPTER STREET FOOD • Караганда, ул. Мустафина 24/1 • Все права защищены © 2026</span>
    </div>
</footer>

<div class="modal" id="cartModal">
    <div class="modal-box">
        <button class="close" id="closeCart">×</button>
        <h3>Оформление заказа</h3>
        
        <div class="cart-items" id="cartItems">
            <p style="color: #666; font-size: 13px;">Корзина пуста</p>
        </div>
        
        <div style="font-weight: 900; font-size: 17px; margin-bottom: 12px; color: var(--accent);" id="cartTotal">Итого: 0 ₸</div>

        <div class="kaspi-box">
            💳 <strong>Оплата по номеру Kaspi Gold:</strong><br>
            Переведите сумму на номер: <strong>+7 (775) 938-78-98</strong><br>
            После оплаты прикрепите чек в WhatsApp.
        </div>

        <label>Ваше имя</label>
        <input id="clientName" placeholder="Введите ваше имя" />

        <label>Телефон / WhatsApp</label>
        <input id="clientPhone" placeholder="+7 700 000 00 00" />

        <label>Адрес доставки</label>
        <input id="clientAddress" placeholder="Улица, дом, квартира" />

        <button class="cart-btn" style="width:100%; margin-top:16px; padding: 12px;" onclick="sendOrder()">Оплатил(а) • Отправить в WhatsApp</button>
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
        cartItems.innerHTML = `<p style="color: #666; font-size: 13px;">Корзина пуста</p>`;
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
    text += `\n💰 Итого: ${total} ₸\n💳 Оплата через Kaspi выполнена\n\n👤 Имя: ${name}\n📞 Телефон: ${phone}\n📍 Адрес: ${address}\n\n*(Прикрепите скриншот чека)*`;

    let myPhone = "77759387898";
    window.open(`https://wa.me/${myPhone}?text=${encodeURIComponent(text)}`, "_blank");
}
</script>

</body>
</html>
