# v4-green-mart
Green Mart supermarket website concept demo

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#123b2a">
<meta name="description" content="Discover everyday grocery essentials in the V4 Green Mart website concept.">
<title>V4 Green Mart | Freshness for Every Day</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700;800&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --green:#176b45;
  --deep:#103c2b;
  --lime:#d8f36a;
  --cream:#faf9f3;
  --muted:#748078;
  --line:#e7e9df;
  --white:#fff;
  --shadow:0 15px 45px rgba(16,60,43,.08);
  --radius:22px;
}
* { box-sizing:border-box; }
html { scroll-behavior:smooth; scroll-padding-top:100px; }
body {
  margin:0;
  background:var(--cream);
  color:var(--deep);
  font-family:"DM Sans",sans-serif;
  line-height:1.6;
}
body,button,input,select { font-family:"DM Sans",sans-serif; }
button,input,select { font-size:inherit; }
button,a { -webkit-tap-highlight-color:transparent; }
button { cursor:pointer; }
a { color:inherit;text-decoration:none; }
img { display:block;max-width:100%; }
button:focus-visible,a:focus-visible,input:focus-visible,select:focus-visible {
  outline:3px solid #94c76a;outline-offset:3px;
}
.container { width:min(1160px,calc(100% - 40px));margin:auto; }
.announcement {
  background:var(--deep);color:#fff;text-align:center;
  padding:8px 12px;font-size:11px;letter-spacing:1.1px;
  font-weight:700;
}
.announcement span { color:var(--lime); }
header {
  background:rgba(255,255,255,.96);position:sticky;top:0;
  z-index:30;border-bottom:1px solid var(--line);
  backdrop-filter:blur(15px);
}
.nav {
  min-height:80px;display:flex;align-items:center;
  justify-content:space-between;gap:20px;
}
.brand { display:flex;align-items:center;gap:11px;flex-shrink:0; }
.brand-icon {
  display:grid;place-items:center;width:45px;height:45px;
  border-radius:15px;background:var(--lime);font-size:25px;
}
.brand-name { font:800 19px Manrope,sans-serif;letter-spacing:-.8px;line-height:1.2; }
.brand-sub { display:block;font-size:9px;letter-spacing:2px;color:var(--muted);font-weight:800;margin-top:3px; }
.nav-links { display:flex;gap:27px;align-items:center;font-size:13px;font-weight:700; }
.nav-links a:hover { color:var(--green); }
.nav-actions { display:flex;gap:10px;align-items:center; }
.icon-button,.cart-button {
  border:1px solid var(--line);background:white;color:var(--deep);
  border-radius:50px;padding:11px 15px;font-weight:800;
}
.cart-button { background:var(--green);color:white;border-color:var(--green); }
.cart-button:hover,.btn-primary:hover { background:var(--deep); }
.count {
  display:inline-grid;place-items:center;min-width:21px;height:21px;
  border-radius:50px;background:var(--lime);color:var(--deep);
  font-size:11px;margin-left:5px;padding:0 5px;
}
.mobile-menu { display:none; }
.demo-note {
  background:#f0f5e8;color:#45644d;text-align:center;
  padding:8px 14px;font-size:11px;
}
.hero { padding:36px 0 25px; }
.hero-layout {
  display:grid;grid-template-columns:1.04fr .96fr;
  background:#eff2e5;border-radius:32px;overflow:hidden;min-height:450px;
}
.hero-copy { padding:clamp(30px,5vw,65px);align-self:center; }
.eyebrow {
  display:inline-flex;align-items:center;gap:7px;
  color:var(--green);background:#e1ebd3;border-radius:50px;
  padding:8px 13px;font-size:10px;font-weight:800;
  text-transform:uppercase;letter-spacing:1px;
}
h1,h2,h3,p { margin-top:0; }
h1 {
  font:800 clamp(43px,5.6vw,69px)/1.02 Manrope,sans-serif;
  letter-spacing:-3.5px;margin:24px 0 17px;
}
h1 em { color:var(--green);font-style:normal; }
.hero-copy>p { max-width:430px;color:#657369;font-size:15px; }
.hero-buttons { display:flex;flex-wrap:wrap;gap:11px;margin:25px 0 20px; }
.btn {
  display:inline-flex;justify-content:center;align-items:center;gap:8px;
  border:0;border-radius:50px;padding:14px 20px;
  font-size:12px;font-weight:800;transition:.2s;
}
.btn-primary { background:var(--green);color:white; }
.btn-light { background:white;color:var(--deep);border:1px solid var(--line); }
.btn-light:hover { background:#f3f6ed; }
.trust-line { font-size:11px;color:var(--muted); }
.hero-image {
  position:relative;min-height:370px;
  background:#dfe8d2;
}
.hero-image img { width:100%;height:100%;position:absolute;inset:0;object-fit:cover; }
.image-overlay {
  position:absolute;inset:0;
  background:linear-gradient(0deg,rgba(13,46,31,.35),transparent 55%);
}
.floating-card {
  position:absolute;bottom:24px;left:22px;right:22px;
  display:flex;align-items:center;gap:12px;
  padding:15px;background:rgba(255,255,255,.95);
  border-radius:18px;box-shadow:var(--shadow);
}
.floating-emoji {
  width:44px;height:44px;display:grid;place-items:center;
  background:#e7f0da;border-radius:13px;font-size:22px;
}
.floating-card strong { display:block;font-size:13px; }
.floating-card small { color:var(--muted);font-size:11px; }
.benefits { display:grid;grid-template-columns:repeat(4,1fr);gap:12px;padding:20px 0 40px; }
.benefit {
  display:flex;align-items:center;gap:12px;background:white;
  border:1px solid var(--line);padding:17px;border-radius:17px;
}
.benefit-icon {
  display:grid;place-items:center;flex-shrink:0;
  width:40px;height:40px;border-radius:13px;background:#eff4e8;font-size:20px;
}
.benefit strong { display:block;font-size:12px; }
.benefit small { color:var(--muted);font-size:10px; }
.section { padding:48px 0; }
.section-head {
  display:flex;justify-content:space-between;align-items:end;
  gap:20px;margin-bottom:25px;
}
.kicker { color:var(--green);font-size:10px;font-weight:900;letter-spacing:2px; }
h2 { font:800 clamp(29px,4vw,41px)/1.15 Manrope,sans-serif;letter-spacing:-1.7px;margin:8px 0; }
.section-head p { color:var(--muted);font-size:13px;margin:6px 0 0; }
.text-link { font-size:12px;font-weight:800;color:var(--green);white-space:nowrap; }
.category-grid { display:grid;grid-template-columns:repeat(5,1fr);gap:15px; }
.category-card {
  border:1px solid var(--line);border-radius:21px;overflow:hidden;
  background:white;text-align:left;padding:0;transition:.2s;color:var(--deep);
}
.category-card:hover { transform:translateY(-4px);box-shadow:var(--shadow); }
.category-card img { width:100%;aspect-ratio:1.2;object-fit:cover;background:#edf0e6; }
.category-caption { padding:13px; }
.category-caption strong { display:block;font-size:13px; }
.category-caption small { font-size:10px;color:var(--muted); }
.shop-section { background:#f0f3e9;padding:60px 0; }
.shop-toolbar {
  display:flex;justify-content:space-between;align-items:center;
  gap:15px;flex-wrap:wrap;margin:25px 0 18px;
}
.search-wrap { position:relative;flex:1;min-width:220px;max-width:420px; }
.search-wrap span { position:absolute;left:15px;top:10px; }
.search {
  width:100%;border:1px solid #dfe4d7;border-radius:50px;
  padding:12px 16px 12px 42px;background:white;outline-color:var(--green);
}
.toolbar-right { display:flex;gap:9px;align-items:center;flex-wrap:wrap; }
.select {
  padding:11px 14px;border:1px solid #dfe4d7;
  border-radius:50px;background:white;color:var(--deep);
  font-size:12px;font-weight:700;
}
.categories { display:flex;gap:9px;flex-wrap:wrap;margin-bottom:24px; }
.category-pill {
  border:1px solid #dfe4d7;background:white;color:#526256;
  border-radius:50px;padding:9px 15px;font-size:11px;font-weight:800;
}
.category-pill.active,.category-pill:hover {
  background:var(--deep);border-color:var(--deep);color:white;
}
.product-grid { display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:17px; }
.product {
  background:white;border:1px solid #e5e9df;border-radius:20px;
  overflow:hidden;transition:transform .2s,box-shadow .2s;
}
.product:hover { transform:translateY(-4px);box-shadow:var(--shadow); }
.product-photo { position:relative;background:#f3f2e9;overflow:hidden; }
.product-photo img { width:100%;aspect-ratio:1.18;object-fit:cover;transition:transform .35s; }
.product:hover .product-photo img { transform:scale(1.04); }
.product-tag {
  position:absolute;top:11px;left:11px;background:var(--lime);
  padding:5px 9px;border-radius:50px;font-size:9px;font-weight:900;
}
.favorite {
  position:absolute;top:10px;right:10px;width:33px;height:33px;
  border:0;border-radius:50%;background:white;color:#526256;font-size:17px;
}
.favorite.active { color:#dc4e62; }
.product-info { padding:15px; }
.product-category { color:var(--muted);font-size:10px; }
.product-info h3 { font-size:14px;margin:5px 0 3px;letter-spacing:-.2px; }
.product-unit { color:var(--muted);font-size:10px;margin-bottom:13px; }
.product-bottom { display:flex;justify-content:space-between;align-items:center;gap:8px; }
.price { font-size:17px;font-weight:900;letter-spacing:-.5px; }
.price small { display:block;color:var(--muted);font-size:9px;font-weight:500;letter-spacing:0; }
.add-button {
  border:0;background:var(--green);color:white;border-radius:50px;
  padding:9px 13px;font-size:11px;font-weight:800;white-space:nowrap;
}
.add-button:hover { background:var(--deep); }
.empty-state {
  grid-column:1/-1;text-align:center;background:white;
  border:1px dashed #cdd8c7;border-radius:20px;padding:50px 20px;color:var(--muted);
}
.empty-state strong { display:block;color:var(--deep);font-size:18px;margin:8px; }
.promo { padding:42px 0; }
.promo-inner {
  border-radius:27px;background:var(--lime);padding:35px 42px;
  display:flex;align-items:center;justify-content:space-between;gap:25px;
}
.promo-inner h2 { font-size:clamp(25px,3vw,34px); }
.promo-inner p { margin:0;color:#46572e;font-size:13px; }
.promo-inner .btn { background:var(--deep);color:white;white-space:nowrap; }
.basket-section { padding:55px 0;background:#eaf0e3; }
.basket-layout { display:grid;grid-template-columns:1.4fr .6fr;gap:22px;align-items:start; }
.panel { background:white;border:1px solid var(--line);border-radius:22px;padding:24px; }
.panel h3 { font:800 19px Manrope,sans-serif;letter-spacing:-.5px;margin-bottom:16px; }
.basket-row {
  display:grid;grid-template-columns:1fr auto auto;align-items:center;
  gap:15px;padding:14px 0;border-bottom:1px solid #edf0e9;
}
.basket-product { display:flex;align-items:center;gap:11px;min-width:0; }
.basket-thumb { width:48px;height:48px;object-fit:cover;border-radius:12px;background:#f1f2e9; }
.basket-product strong { display:block;font-size:12px; }
.basket-product small { color:var(--muted);font-size:10px; }
.qty { display:flex;align-items:center;gap:9px; }
.qty button {
  width:28px;height:28px;border-radius:9px;border:1px solid var(--line);
  background:white;font-weight:800;color:var(--deep);
}
.line-price { font-size:12px;font-weight:800;white-space:nowrap; }
.basket-empty { text-align:center;color:var(--muted);padding:20px 0;font-size:13px; }
.summary-line { display:flex;justify-content:space-between;gap:10px;font-size:12px;padding:9px 0;color:#647267; }
.summary-line.total { border-top:1px solid var(--line);margin-top:9px;padding-top:18px;color:var(--deep);font-size:18px;font-weight:900; }
.summary-note { font-size:10px;color:var(--muted);margin:14px 0; }
.full-width { width:100%; }
.about-grid { display:grid;grid-template-columns:1fr 1fr;gap:30px;align-items:center; }
.about-visual { border-radius:25px;overflow:hidden;min-height:300px;background:#e8eddc; }
.about-visual img { width:100%;height:100%;min-height:300px;object-fit:cover; }
.about-copy p { color:var(--muted);font-size:14px; }
.about-list { display:grid;gap:13px;margin-top:20px; }
.about-list div { display:flex;gap:11px;align-items:center;font-size:12px;font-weight:700; }
.check {
  display:grid;place-items:center;width:28px;height:28px;border-radius:50%;
  background:#e5f0d8;color:var(--green);flex-shrink:0;
}
.contact-strip { padding:15px 0 55px; }
.contact-inner {
  border:1px solid var(--line);border-radius:23px;background:white;
  padding:25px;display:flex;justify-content:space-between;align-items:center;gap:20px;
}
.contact-inner p { color:var(--muted);font-size:12px;margin:5px 0 0; }
footer { background:var(--deep);color:white;padding:42px 0 22px; }
.footer-grid { display:grid;grid-template-columns:1.4fr 1fr 1fr;gap:30px;padding-bottom:30px; }
.footer-brand p { max-width:300px;color:#bdcfc1;font-size:12px;margin-top:15px; }
.footer-title { font-weight:800;font-size:12px;margin-bottom:12px; }
.footer-links { display:grid;gap:8px;font-size:11px;color:#bdcfc1; }
.footer-links a:hover { color:var(--lime); }
.footer-bottom {
  border-top:1px solid #315343;padding-top:20px;
  display:flex;justify-content:space-between;gap:12px;
  color:#bdcfc1;font-size:10px;
}
.toast {
  position:fixed;bottom:24px;left:50%;transform:translate(-50%,20px);
  background:var(--deep);color:white;padding:13px 20px;border-radius:50px;
  font-size:12px;font-weight:700;box-shadow:var(--shadow);
  opacity:0;pointer-events:none;transition:.25s;z-index:100;
  width:max-content;max-width:calc(100% - 30px);
}
.toast.show { opacity:1;transform:translate(-50%,0); }
.mobile-bottom {
  display:none;position:fixed;bottom:0;left:0;right:0;z-index:25;
  background:white;border-top:1px solid var(--line);
  padding:10px 15px calc(10px + env(safe-area-inset-bottom));
}
.mobile-bottom button { width:100%; }
@media(max-width:900px) {
  .nav-links { gap:15px; }
  .hero-layout { grid-template-columns:1fr 1fr; }
  .hero-copy { padding:32px; }
  .benefits { grid-template-columns:repeat(2,1fr); }
  .category-grid { grid-template-columns:repeat(3,1fr); }
  .product-grid { grid-template-columns:repeat(3,minmax(0,1fr)); }
}
@media(max-width:650px) {
  .container { width:calc(100% - 28px); }
  .announcement { font-size:9px; }
  .nav { min-height:68px;gap:8px; }
  .brand-icon { width:38px;height:38px;font-size:21px;border-radius:12px; }
  .brand-name { font-size:15px; }
  .brand-sub { font-size:8px;letter-spacing:1.3px; }
  .nav-links { display:none; }
  .nav-actions { gap:6px; }
  .icon-button { display:none; }
  .cart-button { padding:10px 12px;font-size:11px; }
  .demo-note { font-size:10px; }
  .hero { padding-top:18px; }
  .hero-layout { grid-template-columns:1fr;border-radius:24px; }
  .hero-copy { padding:30px 24px 23px; }
  h1 { font-size:48px;letter-spacing:-2.8px;margin:20px 0 14px; }
  .hero-copy>p { font-size:13px; }
  .hero-image { min-height:270px; }
  .floating-card { bottom:15px;left:15px;right:15px;padding:11px; }
  .benefits { gap:8px;padding:15px 0 28px; }
  .benefit { padding:11px;gap:8px; }
  .benefit-icon { width:33px;height:33px;font-size:17px; }
  .benefit strong { font-size:10px; }
  .benefit small { font-size:9px; }
  .section { padding:35px 0; }
  .section-head { align-items:start; }
  .section-head p { font-size:11px; }
  .category-grid { grid-template-columns:repeat(2,minmax(0,1fr));gap:10px; }
  .category-card img { aspect-ratio:1.4; }
  .category-caption { padding:10px; }
  .shop-section { padding:38px 0; }
  .shop-toolbar { align-items:stretch; }
  .search-wrap { min-width:100%;max-width:none; }
  .toolbar-right { justify-content:space-between; }
  .categories { gap:7px; }
  .category-pill { padding:8px 11px;font-size:10px; }
  .product-grid { grid-template-columns:repeat(2,minmax(0,1fr));gap:10px; }
  .product-info { padding:11px; }
  .product-info h3 { font-size:12px; }
  .product-unit { font-size:9px; }
  .price { font-size:15px; }
  .add-button { padding:9px 10px;font-size:10px; }
  .product-tag { top:7px;left:7px;font-size:8px;padding:4px 7px; }
  .favorite { top:7px;right:7px;width:29px;height:29px; }
  .promo { padding:25px 0; }
  .promo-inner { padding:26px 23px;align-items:start;flex-direction:column; }
  .promo-inner p { font-size:11px; }
  .basket-section { padding:38px 0 90px; }
  .basket-layout { grid-template-columns:1fr;gap:13px; }
  .panel { padding:17px; }
  .basket-row { grid-template-columns:1fr auto;gap:10px; }
  .line-price { grid-column:2; }
  .about-grid { grid-template-columns:1fr;gap:20px; }
  .about-visual,.about-visual img { min-height:230px; }
  .contact-inner { align-items:start;flex-direction:column;padding:21px; }
  .footer-grid { grid-template-columns:1fr 1fr;gap:25px; }
  .footer-brand { grid-column:1/-1; }
  .footer-bottom { flex-direction:column; }
  .mobile-bottom { display:block; }
  body { padding-bottom:67px; }
}
@media(prefers-reduced-motion:reduce) {
  *,*::before,*::after { scroll-behavior:auto!important;transition:none!important; }
}
</style>
</head>

<body>
<div class="announcement">
  A FRESHER WAY TO SHOP <span>✦</span> EVERYDAY ESSENTIALS, MADE SIMPLE
</div>

<header>
  <div class="container nav">
    <a class="brand" href="#home" aria-label="V4 Green Mart home">
      <span class="brand-icon">🌿</span>
      <span class="brand-name">V4 GREEN MART
        <small class="brand-sub">FRESHNESS FOR EVERY DAY</small>
      </span>
    </a>
    <nav class="nav-links" aria-label="Main navigation">
      <a href="#home">Home</a>
      <a href="#categories">Categories</a>
      <a href="#shop">Shop</a>
      <a href="#about">Our story</a>
    </nav>
    <div class="nav-actions">
      <button class="icon-button" onclick="showFavorites()" aria-label="Show favourites">♡ Favourites</button>
      <button class="cart-button" onclick="goToBasket()">Basket <span class="count" id="cartCount">0</span></button>
    </div>
  </div>
</header>

<div class="demo-note">
  ✨ Independent website concept · Sample products and prices · Not an official store website
</div>

<main id="home">
  <section class="hero">
    <div class="container">
      <div class="hero-layout">
        <div class="hero-copy">
          <span class="eyebrow">🌱 YOUR EVERYDAY GROCERY DESTINATION</span>
          <h1>Fresh finds.<br><em>Happy homes.</em></h1>
          <p>
            Discover a thoughtfully designed grocery shopping experience,
            bringing everyday essentials together in one simple place.
          </p>
          <div class="hero-buttons">
            <a class="btn btn-primary" href="#shop">Explore the shop <span>↗</span></a>
            <a class="btn btn-light" href="#categories">Browse categories</a>
          </div>
          <div class="trust-line">Fresh ideas · Everyday favourites · Easy browsing</div>
        </div>
        <div class="hero-image">
          <img
            src="https://images.unsplash.com/photo-1542838132-92c53300491e?auto=format&fit=crop&w=1100&q=85"
            alt="Colourful fresh produce displayed at a grocery market"
            fetchpriority="high">
          <div class="image-overlay"></div>
          <div class="floating-card">
            <div class="floating-emoji">🥬</div>
            <div>
              <strong>A little goodness, every day</strong>
              <small>Your neighbourhood grocery concept</small>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="container benefits" aria-label="Shopping highlights">
    <div class="benefit">
      <div class="benefit-icon">🥑</div>
      <div><strong>Fresh favourites</strong><small>Produce inspiration</small></div>
    </div>
    <div class="benefit">
      <div class="benefit-icon">🧺</div>
      <div><strong>Daily essentials</strong><small>For every household</small></div>
    </div>
    <div class="benefit">
      <div class="benefit-icon">🔎</div>
      <div><strong>Easy discovery</strong><small>Find what you need</small></div>
    </div>
    <div class="benefit">
      <div class="benefit-icon">📱</div>
      <div><strong>Mobile friendly</strong><small>Shop from any screen</small></div>
    </div>
  </section>

  <section class="container section" id="categories">
    <div class="section-head">
      <div>
        <div class="kicker">EXPLORE YOUR FAVOURITES</div>
        <h2>Shop by category.</h2>
        <p>A little something for every kitchen and every craving.</p>
      </div>
      <a href="#shop" class="text-link">View all products ↗</a>
    </div>

    <div class="category-grid">
      <button class="category-card" onclick="chooseCategory('Fruits & Vegetables')">
        <img src="https://images.unsplash.com/photo-1540420773420-3366772f4999?auto=format&fit=crop&w=500&q=80" alt="Fresh vegetables" loading="lazy">
        <span class="category-caption"><strong>Fruits & vegetables</strong><small>Fresh inspiration</small></span>
      </button>
      <button class="category-card" onclick="chooseCategory('Dairy & Eggs')">
        <img src="https://images.unsplash.com/photo-1563636619-e9143da7973b?auto=format&fit=crop&w=500&q=80" alt="Milk and dairy products" loading="lazy">
        <span class="category-caption"><strong>Dairy & eggs</strong><small>Everyday essentials</small></span>
      </button>
      <button class="category-card" onclick="chooseCategory('Bakery')">
        <img src="https://images.unsplash.com/photo-1509440159596-0249088772ff?auto=format&fit=crop&w=500&q=80" alt="Freshly baked bread" loading="lazy">
        <span class="category-caption"><strong>Bakery</strong><small>Comforting classics</small></span>
      </button>
      <button class="category-card" onclick="chooseCategory('Pantry')">
        <img src="https://images.unsplash.com/photo-1586201375761-83865001e31c?auto=format&fit=crop&w=500&q=80" alt="Rice and pantry staples" loading="lazy">
        <span class="category-caption"><strong>Pantry</strong><small>Kitchen must-haves</small></span>
      </button>
      <button class="category-card" onclick="chooseCategory('Snacks')">
        <img src="https://images.unsplash.com/photo-1621939514649-280e2aa2c4c1?auto=format&fit=crop&w=500&q=80" alt="Snack selection" loading="lazy">
        <span class="category-caption"><strong>Snacks</strong><small>Little treats</small></span>
      </button>
    </div>
  </section>

  <section class="shop-section" id="shop">
    <div class="container">
      <div class="section-head">
        <div>
          <div class="kicker">THE GREEN MART EDIT</div>
          <h2>Everyday goodness.</h2>
          <p>Explore our sample collection of grocery favourites.</p>
        </div>
      </div>

      <div class="shop-toolbar">
        <label class="search-wrap">
          <span aria-hidden="true">⌕</span>
          <input id="search" class="search" type="search" placeholder="Search groceries..." aria-label="Search products">
        </label>
        <div class="toolbar-right">
          <label for="sort" class="trust-line">Sort by</label>
          <select id="sort" class="select" aria-label="Sort products">
            <option value="featured">Featured</option>
            <option value="low">Price: low to high</option>
            <option value="high">Price: high to low</option>
            <option value="az">Name: A to Z</option>
          </select>
        </div>
      </div>

      <div class="categories" id="categoryFilters" aria-label="Filter products">
        <button class="category-pill active" data-category="All">All products</button>
        <button class="category-pill" data-category="Fruits & Vegetables">Fruits & vegetables</button>
        <button class="category-pill" data-category="Dairy & Eggs">Dairy & eggs</button>
        <button class="category-pill" data-category="Bakery">Bakery</button>
        <button class="category-pill" data-category="Pantry">Pantry</button>
        <button class="category-pill" data-category="Snacks">Snacks</button>
      </div>

      <div class="product-grid" id="productGrid" aria-live="polite"></div>
      <p class="trust-line" style="margin-top:20px">
        Sample catalogue for demonstration only. All prices, product details and availability require store-owner approval.
      </p>
    </div>
  </section>

  <section class="promo">
    <div class="container">
      <div class="promo-inner">
        <div>
          <div class="kicker">GOOD THINGS START HERE</div>
          <h2>Your neighbourhood, made a little easier.</h2>
          <p>A fresh concept for a more convenient grocery experience.</p>
        </div>
        <a href="#shop" class="btn">Discover the collection ↗</a>
      </div>
    </div>
  </section>

  <section class="basket-section" id="basket">
    <div class="container">
      <div class="section-head">
        <div>
          <div class="kicker">YOUR SHOPPING SELECTION</div>
          <h2>Your basket.</h2>
          <p>Add a few favourites and see your sample total update.</p>
        </div>
      </div>
      <div class="basket-layout">
        <div class="panel">
          <h3>Selected products <span class="trust-line" id="basketItemCount"></span></h3>
          <div id="basketItems"><div class="basket-empty">Your basket is waiting for its first favourite. 🧺</div></div>
        </div>
        <aside class="panel">
          <h3>Order summary</h3>
          <div class="summary-line"><span>Sample subtotal</span><strong id="subtotal">₹0</strong></div>
          <div class="summary-line"><span>Delivery</span><span>Not calculated</span></div>
          <div class="summary-line total"><span>Sample total</span><span id="basketTotal">₹0</span></div>
          <p class="summary-note">This is a website demonstration. Prices are illustrative. No real order, payment or delivery is arranged.</p>
          <button class="btn btn-primary full-width" onclick="checkout()">Continue to demo checkout →</button>
          <button class="btn btn-light full-width" style="margin-top:9px" onclick="clearBasket()">Clear basket</button>
        </aside>
      </div>
    </div>
  </section>

  <section class="container section" id="about">
    <div class="about-grid">
      <div class="about-visual">
        <img src="https://images.unsplash.com/photo-1542838132-92c53300491e?auto=format&fit=crop&w=900&q=85" alt="Fresh produce at a market" loading="lazy">
      </div>
      <div class="about-copy">
        <div class="kicker">A THOUGHTFUL SHOPPING CONCEPT</div>
        <h2>Local shopping.<br>Beautifully simple.</h2>
        <p>
          V4 Green Mart is the inspiration for this independent website concept:
          a welcoming online space where customers could discover grocery
          essentials, explore categories and build a shopping basket.
        </p>
        <p>
          The goal is simple: bring the familiar feeling of neighbourhood
          shopping into a clean, convenient digital experience.
        </p>
        <div class="about-list">
          <div><span class="check">✓</span> An organised, searchable catalogue</div>
          <div><span class="check">✓</span> Simple shopping-basket controls</div>
          <div><span class="check">✓</span> A responsive mobile-first layout</div>
          <div><span class="check">✓</span> Room to grow with the store's needs</div>
        </div>
      </div>
    </div>
  </section>

  <section class="container contact-strip" id="contact">
    <div class="contact-inner">
      <div>
        <div class="kicker">LET'S MAKE GROCERY SHOPPING SIMPLER</div>
        <h2 style="font-size:25px;margin:8px 0">A concept with room to grow.</h2>
        <p>Store address, contact details, operating hours and ordering options can be added after approval.</p>
      </div>
      <a class="btn btn-primary" href="#home">Back to top ↑</a>
    </div>
  </section>
</main>

<footer>
  <div class="container">
    <div class="footer-grid">
      <div class="footer-brand">
        <a class="brand" href="#home">
          <span class="brand-icon">🌿</span>
          <span class="brand-name" style="color:white">V4 GREEN MART
            <small class="brand-sub" style="color:#bdcfc1">FRESHNESS FOR EVERY DAY</small>
          </span>
        </a>
        <p>An independently created website concept showcasing a possible online grocery-shopping experience. Not an official store website.</p>
      </div>
      <div>
        <div class="footer-title">Explore</div>
        <div class="footer-links">
          <a href="#home">Home</a>
          <a href="#categories">Categories</a>
          <a href="#shop">Sample catalogue</a>
          <a href="#basket">Shopping basket</a>
        </div>
      </div>
      <div>
        <div class="footer-title">Demo information</div>
        <div class="footer-links">
          <span>Illustrative products and prices</span>
          <span>No real orders or payments</span>
          <span>Store details pending approval</span>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© <span id="year"></span> V4 Green Mart website concept</span>
      <span>Designed with care 🌱 · Independent demo</span>
    </div>
  </div>
</footer>

<div class="toast" id="toast" role="status" aria-live="polite"></div>
<div class="mobile-bottom">
  <button class="btn btn-primary" onclick="goToBasket()">View basket · <span id="mobileCartCount">0</span> items</button>
</div>

<script>
"use strict";

// DEMO CATALOGUE: confirm all prices and products with the shop owner.
const products = [
  {id:1,name:"Fresh Tomatoes",category:"Fruits & Vegetables",price:40,unit:"per kg",tag:"Fresh pick",image:"https://images.unsplash.com/photo-1546094096-0df4bcaaa337?auto=format&fit=crop&w=600&q=80"},
  {id:2,name:"Yellow Bananas",category:"Fruits & Vegetables",price:60,unit:"per dozen",tag:"Everyday",image:"https://images.unsplash.com/photo-1571771894821-ce9b6c11b08e?auto=format&fit=crop&w=600&q=80"},
  {id:3,name:"Red Apples",category:"Fruits & Vegetables",price:180,unit:"per kg",tag:"Popular",image:"https://images.unsplash.com/photo-1560806887-1e4cd0b6cbd6?auto=format&fit=crop&w=600&q=80"},
  {id:4,name:"Fresh Spinach",category:"Fruits & Vegetables",price:30,unit:"per bunch",tag:"Fresh pick",image:"https://images.unsplash.com/photo-1576045057995-568f588f82fb?auto=format&fit=crop&w=600&q=80"},
  {id:5,name:"Fresh Milk",category:"Dairy & Eggs",price:32,unit:"500 ml",tag:"Daily essential",image:"https://images.unsplash.com/photo-1563636619-e9143da7973b?auto=format&fit=crop&w=600&q=80"},
  {id:6,name:"Farm Eggs",category:"Dairy & Eggs",price:90,unit:"6 pieces",tag:"Everyday",image:"https://images.unsplash.com/photo-1506976785307-8732e854ad03?auto=format&fit=crop&w=600&q=80"},
  {id:7,name:"Cheddar Cheese",category:"Dairy & Eggs",price:120,unit:"per pack",tag:"Popular",image:"https://images.unsplash.com/photo-1486297678162-eb2a19b0a32d?auto=format&fit=crop&w=600&q=80"},
  {id:8,name:"Fresh Bread",category:"Bakery",price:45,unit:"per loaf",tag:"Bakery",image:"https://images.unsplash.com/photo-1509440159596-0249088772ff?auto=format&fit=crop&w=600&q=80"},
  {id:9,name:"Butter Croissant",category:"Bakery",price:55,unit:"per piece",tag:"Bakery",image:"https://images.unsplash.com/photo-1555507036-ab1f4038808a?auto=format&fit=crop&w=600&q=80"},
  {id:10,name:"Basmati Rice",category:"Pantry",price:75,unit:"per kg",tag:"Pantry pick",image:"https://images.unsplash.com/photo-1586201375761-83865001e31c?auto=format&fit=crop&w=600&q=80"},
  {id:11,name:"Cooking Oil",category:"Pantry",price:140,unit:"1 litre",tag:"Kitchen staple",image:"https://images.unsplash.com/photo-1474979266404-7eaacbcd87c5?auto=format&fit=crop&w=600&q=80"},
  {id:12,name:"Potato Chips",category:"Snacks",price:30,unit:"per pack",tag:"Snack time",image:"https://images.unsplash.com/photo-1621939514649-280e2aa2c4c1?auto=format&fit=crop&w=600&q=80"},
  {id:13,name:"Chocolate Cookies",category:"Snacks",price:55,unit:"per pack",tag:"Treat yourself",image:"https://images.unsplash.com/photo-1499636136210-6f4ee915583e?auto=format&fit=crop&w=600&q=80"},
  {id:14,name:"Fresh Oranges",category:"Fruits & Vegetables",price:90,unit:"per kg",tag:"Citrus favourite",image:"https://images.unsplash.com/photo-1547514701-42782101795e?auto=format&fit=crop&w=600&q=80"},
  {id:15,name:"Green Broccoli",category:"Fruits & Vegetables",price:65,unit:"per piece",tag:"Fresh pick",image:"https://images.unsplash.com/photo-1459411621453-7b03977f4bfc?auto=format&fit=crop&w=600&q=80"},
  {id:16,name:"Peanut Butter",category:"Pantry",price:160,unit:"per jar",tag:"Pantry pick",image:"https://images.unsplash.com/photo-1589365278144-c9e705f843ba?auto=format&fit=crop&w=600&q=80"}
];

let selectedCategory = "All";
let basket = {};
let favorites = new Set();
let favoritesOnly = false;
let toastTimer;

const money = amount => new Intl.NumberFormat("en-IN", {
  style:"currency",currency:"INR",maximumFractionDigits:2
}).format(amount);

function escapeHTML(value) {
  return String(value).replace(/[&<>"']/g, char => ({
    "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"
  }[char]));
}

function showToast(message) {
  const toast = document.getElementById("toast");
  toast.textContent = message;
  toast.classList.add("show");
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => toast.classList.remove("show"),2400);
}

function renderProducts() {
  const query = document.getElementById("search").value.trim().toLowerCase();
  const sort = document.getElementById("sort").value;

  let shown = products.filter(product => {
    const categoryMatch = selectedCategory === "All" ||
      product.category === selectedCategory;
    const searchMatch = (product.name + " " + product.category).toLowerCase().includes(query);
    const favoriteMatch = !favoritesOnly || favorites.has(product.id);
    return categoryMatch && searchMatch && favoriteMatch;
  });

  if (sort === "low") shown.sort((a,b) => a.price-b.price);
  if (sort === "high") shown.sort((a,b) => b.price-a.price);
  if (sort === "az") shown.sort((a,b) => a.name.localeCompare(b.name));

  const grid = document.getElementById("productGrid");

  if (!shown.length) {
    grid.innerHTML = `<div class="empty-state">🔎<strong>No products found</strong>Try a different search or category.</div>`;
    return;
  }

  grid.innerHTML = shown.map(product => `
    <article class="product">
      <div class="product-photo">
        <img src="${escapeHTML(product.image)}" alt="${escapeHTML(product.name)}" loading="lazy">
        <span class="product-tag">${escapeHTML(product.tag)}</span>
        <button class="favorite ${favorites.has(product.id) ? "active" : ""}"
          onclick="toggleFavorite(${product.id})"
          aria-label="${favorites.has(product.id) ? "Remove from" : "Add to"} favourites"
          aria-pressed="${favorites.has(product.id)}">${favorites.has(product.id) ? "♥" : "♡"}</button>
      </div>
      <div class="product-info">
        <div class="product-category">${escapeHTML(product.category)}</div>
        <h3>${escapeHTML(product.name)}</h3>
        <div class="product-unit">${escapeHTML(product.unit)}</div>
        <div class="product-bottom">
          <div class="price">${money(product.price)}<small>Sample price</small></div>
          <button class="add-button" onclick="addToBasket(${product.id})">＋ Add</button>
        </div>
      </div>
    </article>
  `).join("");
}

function chooseCategory(category) {
  selectedCategory = category;
  favoritesOnly = false;
  document.querySelectorAll(".category-pill").forEach(button => {
    button.classList.toggle("active",button.dataset.category === category);
  });
  renderProducts();
  document.getElementById("shop").scrollIntoView({behavior:"smooth"});
}

function toggleFavorite(id) {
  if (favorites.has(id)) {
    favorites.delete(id);
    showToast("Removed from favourites");
  } else {
    favorites.add(id);
    showToast("Added to favourites ♥");
  }
  renderProducts();
}

function showFavorites() {
  favoritesOnly = !favoritesOnly;
  selectedCategory = "All";
  document.querySelectorAll(".category-pill").forEach(button => {
    button.classList.toggle("active",button.dataset.category === "All");
  });
  renderProducts();
  document.getElementById("shop").scrollIntoView({behavior:"smooth"});
  if (favoritesOnly) showToast("Showing your favourite products");
}

function addToBasket(id) {
  basket[id] = (basket[id] || 0) + 1;
  renderBasket();
  const product = products.find(item => item.id === id);
  showToast(product.name + " added to your basket");
}

function changeQuantity(id,change) {
  basket[id] = (basket[id] || 0) + change;
  if (basket[id] <= 0) delete basket[id];
  renderBasket();
}

function clearBasket() {
  basket = {};
  renderBasket();
  showToast("Basket cleared");
}

function renderBasket() {
  const ids = Object.keys(basket).filter(id => basket[id] > 0);
  const count = ids.reduce((sum,id) => sum + basket[id],0);
  const total = ids.reduce((sum,id) => {
    const product = products.find(item => item.id === Number(id));
    return sum + product.price * basket[id];
  },0);

  document.getElementById("cartCount").textContent = count;
  document.getElementById("mobileCartCount").textContent = count;
  document.getElementById("basketItemCount").textContent = `(${count} items)`;
  document.getElementById("subtotal").textContent = money(total);
  document.getElementById("basketTotal").textContent = money(total);

  const container = document.getElementById("basketItems");

  if (!ids.length) {
    container.innerHTML = `<div class="basket-empty">Your basket is waiting for its first favourite. 🧺<br><br><a class="text-link" href="#shop">Explore products ↗</a></div>`;
    return;
  }

  container.innerHTML = ids.map(id => {
    const product = products.find(item => item.id === Number(id));
    return `
      <div class="basket-row">
        <div class="basket-product">
          <img class="basket-thumb" src="${escapeHTML(product.image)}" alt="">
          <div><strong>${escapeHTML(product.name)}</strong><small>${money(product.price)} · ${escapeHTML(product.unit)}</small></div>
        </div>
        <div class="qty" aria-label="Quantity controls">
          <button onclick="changeQuantity(${id},-1)" aria-label="Remove one">−</button>
          <strong>${basket[id]}</strong>
          <button onclick="changeQuantity(${id},1)" aria-label="Add one">+</button>
        </div>
        <div class="line-price">${money(product.price * basket[id])}</div>
      </div>
    `;
  }).join("");
}

function goToBasket() {
  document.getElementById("basket").scrollIntoView({behavior:"smooth"});
}

function checkout() {
  alert(
    "Welcome to the V4 Green Mart website demo!\\n\\n" +
    "Your sample basket is working, but this is not a live store. " +
    "No order has been placed and no payment or customer details have been collected.\\n\\n" +
    "Real checkout and ordering can be added after the store owner approves the products, prices and business details."
  );
}

document.getElementById("search").addEventListener("input",renderProducts);
document.getElementById("sort").addEventListener("change",renderProducts);

document.getElementById("categoryFilters").addEventListener("click",event => {
  const button = event.target.closest("button[data-category]");
  if (!button) return;
  selectedCategory = button.dataset.category;
  favoritesOnly = false;
  document.querySelectorAll(".category-pill").forEach(item => {
    item.classList.toggle("active",item === button);
  });
  renderProducts();
});

document.getElementById("year").textContent = new Date().getFullYear();

renderProducts();
renderBasket();
</script>
</body>
</html>
