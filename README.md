<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CHAPTER STREET FOOD — Бургеры и хот-доги в Караганде</title>
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
    background: #0f1012 url('bg.jpg') no-repeat center center fixed;
    background-size: cover;
    color: #fff;
    font-family: Arial, Helvetica, sans-serif;
    position: relative;
}

/* Затемняющий оверлей для readability */
body::before {
    content: "";
    position: fixed;
    inset: 0;
    background: rgba(15, 16, 18, 0.88);
    backdrop-filter: blur(4px);
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
    background: rgba(15,16,18,.9);
    backdrop-filter: blur(15px);
    border-bottom: 1px solid rgba(255,255,255,.08);
}

.nav {
    height: 70px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    font-size: 20px;
    font-weight: 900;
    letter-spacing: -0.5px;
}

.logo span {
    color: #ff5c00;
}

.nav-links {
    display: flex;
    gap: 20px;
    color: #888;
    font-size: 14px;
}

.nav-links a:hover {
    color: white;
}

.cart-btn {
    background: #ff5c00;
    color: white;
    padding: 10px 18px;
    border-radius: 12px;
    font-weight: bold;
    border: none;
    cursor: pointer;
    transition: .2s;
}

.cart-btn:hover {
    transform: translateY(-2px);
}

/* HERO */
.hero {
    min-height: 75vh;
    display: flex;
    align-items: center;
    padding-top: 100px;
}

.hero-content {
    background: rgba(21, 23, 28, 0.6);
    padding: 40px;
    border-radius: 24px;
    border: 1px solid rgba(255,255,255,.08);
    backdrop-filter: blur(10px);
    max-width: 650px;
}

.badge {
    display: inline-block;
    padding: 6px 12px;
    border: 1px solid rgba(255,255,255,.15);
    border-radius: 20px;
    color: #ccc;
    font-size: 13px;
    margin-bottom: 20px;
    background: rgba(0,0,0,.4);
}

.hero h1 {
    font-size: clamp(35px, 5vw, 60px);
    line-height: 1.1;
    letter-spacing: -1px;
}

.hero h1 span {
    color: #ff5c00;
}

.hero p {
    margin-top: 15px;
    color: #aaa;
    font-size: 16px;
    line-height: 1.5;
}

/* MENU SECTION */
section {
    padding: 50px 0;
}

.section-title {
    font-size: 30px;
    letter-spacing: -1px;
    margin-bottom: 25px;
    color: #ff5c00;
    border-bottom: 2px solid rgba(255,92,0,.3);
    padding-bottom: 8px;
}

.menu-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.menu-card {
    background: rgba(21, 23, 28, 0.85);
    border: 1px solid rgba(255,255,255,.08);
    border-radius: 20px;
    padding: 22px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    backdrop-filter: blur(10px);
    transition: .2s;
}

.menu-card:hover {
    transform: translateY(-4px);
    border-color: rgba(255,92,0,.4);
    background: rgba(21, 23, 28, 0.95);
}

.menu-info h3 {
    font-size: 19px;
    margin-bottom: 6px;
}

.menu-info p {
    color: #888;
    font-size: 13px;
    line-height: 1.4;
    margin-bottom: 15px;
}

.menu-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 10px;
}

.price {
    font-size: 18px;
    font-weight: bold;
}

.add-btn {
    background: rgba(255,92,0,.2);
    color: #ff5c00;
    border: none;
    padding: 8px 14px;
    border-radius: 10px;
    font-weight: bold;
    cursor: pointer;
    transition: .2s;
}

.add-btn:hover {
    background: #ff5c00;
    color: white;
}

/* MODAL */
.modal {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,.85);
    backdrop-filter: blur(10px);
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
    background: #15171c;
    border: 1px solid rgba(255,255,255,.1);
    border-radius: 24px;
    padding: 25px;
    max-height: 90vh;
    overflow-y: auto;
}

.close {
    float: right;
    background: none;
    border: none;
    color: #777;
    font-size: 24px;
    cursor: pointer;
}

.modal-box h3 {
    font-size: 22px;
    margin-bottom: 15px;
}

.cart-items {
    max-height: 150px;
    overflow-y: auto;
    margin-bottom: 15px;
    border-bottom: 1px solid rgba(255,255,255,.08);
    padding-bottom: 10px;
}

.cart-item {
    display: flex;
    justify-content: space-between;
    margin-bottom: 8px;
    font-size: 14px;
    color: #aaa;
}

.kaspi-box {
    background: rgba(0, 133, 255, 0.12);
    border: 1px solid rgba(0, 133, 255, 0.3);
    border-radius: 12px;
    padding: 12px;
    margin: 12px 0;
    font-size: 13px;
    color: #ccc;
    line-height: 1.4;
}

.kaspi-box strong {
    color: #0085ff;
}

label {
    display: block;
    color: #888;
    font-size: 12px;
    margin-top: 8px;
    margin-bottom: 4px;
}

input {
    width: 100%;
    padding: 10px;
    background: #0b0c0e;
    border: 1px solid rgba(255,255,255,.1);
    color: white;
    border-radius: 10px;
    outline: none;
}

input:focus {
    border-color: #ff5c00;
}

footer {
    padding: 30px 0;
    border-top: 1px solid rgba(255,255,255,.08);
    color: #666;
    font-size: 13px;
    text-align: center;
}

@media(max-width: 800px) {
    .menu-grid { grid-template-columns: 1fr; }
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
        </nav>
        <button class="cart-btn" id="openCart">Корзина (<span id="cartCount">0</span>)</button>
    </div>
</header>

<main>
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="badge">📍 ул. Мустафина 24/1 • 11:00 - 23:00</div>
                <h1>У нас уютно,<br><span>вкусно и тепло</span></h1>
                <p>Сочные бургеры и фирменные хот-доги в Караганде. Заказывайте с доставкой прямо сейчас!</p>
            </div>
        </div>
    </section>

    <!-- БУРГЕРЫ -->
    <div class="container" id="burgers">
        <h2 class="section-title">Бургеры</h2>
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
    <div class="container" id="hotdogs" style="margin-top: 40px;">
        <h2 class="section-title">Хот-доги</h2>
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
    <div class="container" id="combo" style="margin-top: 40px;">
        <h2 class="section-title">Комбо наборы</h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-info">
                    <h3>Бургер + Хот-Дог + Напиток</h3>
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
    <div class="container" id="snackset" style="margin-top: 40px;">
        <h2 class="section-title">Снэки и напитки</h2>
        <div class="menu-grid">
            <div class="menu-card">
                <div class="menu-info"><h3>Наггетсы (6 шт)</h3><p>Хрустящие куриные наггетсы</p></div>
                <div class="menu-bottom"><span class="price">1100 ₸</span><button class="add-btn" onclick="addToCart('Наггетсы 6 шт', 1100)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Картофель фри</h3><p>Золотистые картофельные палочки</p></div>
                <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Картофель фри', 900)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Картофельные дольки</h3><p>Ароматные дольки картофеля</p></div>
                <div class="menu-bottom"><span class="price">900 ₸</span><button class="add-btn" onclick="addToCart('Картофельные дольки', 900)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Милкшейк (350 мл)</h3><p>Клубничный / Ванильный / Snickers / Банановый / Шоколадный / Oreo</p></div>
                <div class="menu-bottom"><span class="price">1100 ₸</span><button class="add-btn" onclick="addToCart('Милкшейк', 1100)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Морс (350 мл)</h3><p>Ягодный фирменный морс</p></div>
                <div class="menu-bottom"><span class="price">600 ₸</span><button class="add-btn" onclick="addToCart('Морс 350мл', 600)">В корзину</button></div>
            </div>
            <div class="menu-card">
                <div class="menu-info"><h3>Чай (350 мл)</h3><p>Фруктовый / Ташкентский / Ягодный / Облепиховый</p></div>
                <div class="menu-bottom"><span class="price">600 ₸</span><button class="add-btn" onclick="addToCart('Чай 350мл', 600)">В корзину</button></div>
            </div>
        </div>
    </div>
</main>

<footer>
    <div class="container" style="margin-top: 50px;">
        CHAPTER STREET FOOD • Караганда, ул. Мустафина 24/1 • 2026
    </div>
</footer>

<!-- MODAL -->
<div class="modal" id="cartModal">
    <div class="modal-box">
        <button class="close" id="closeCart">×</button>
        <h3>Ваш заказ</h3>
        
        <div class="cart-items" id="cartItems">
            <p style="color: #666; font-size: 14px;">Корзина пуста</p>
        </div>
        
        <div style="font-weight: bold; margin-bottom: 10px;" id="cartTotal">Итого: 0 ₸</div>

        <div class="kaspi-box">
            💳 <strong>Оплата по номеру Kaspi Gold:</strong><br>
            Переведите сумму на рабочий номер: <strong>+7 (775) 938-78-98</strong><br>
            После перевода нажмите кнопку отправки в WhatsApp и прикрепите скриншот чека.
        </div>

        <label>Ваше имя</label>
        <input id="clientName" placeholder="Имя" />

        <label>Телефон / WhatsApp</label>
        <input id="clientPhone" placeholder="+7 700 000 00 00" />

        <label>Адрес доставки в Караганде</label>
        <input id="clientAddress" placeholder="Улица, дом, квартира" />

        <button class="cart-btn" style="width:100%; margin-top:15px;" onclick="sendOrder()">Оплатил(а) • Отправить заказ в WhatsApp</button>
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
    text += `\n💰 Итого к оплате: ${total} ₸\n💳 Оплата через Kaspi выполнена\n\n👤 Имя: ${name}\n📞 Телефон: ${phone}\n📍 Адрес: ${address}\n\n*(Прикрепите скриншот чека из Kaspi)*`;

    let myPhone = "77759387898";
    window.open(`https://wa.me/${myPhone}?text=${encodeURIComponent(text)}`, "_blank");
}
</script>

</body>
</html>
