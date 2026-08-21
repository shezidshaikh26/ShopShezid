<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="SHOPSHEZID — premium contemporary streetwear by SHEZID. T-Shirts, Hoodies and Shirts.">
<title>SHOPSHEZID — SHEZID</title>

<style>
:root{
  --black:#0b0b0b;
  --dark:#111;
  --muted:#777;
  --line:#e7e7e7;
  --soft:#f5f5f3;
  --white:#fff;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:Arial,Helvetica,sans-serif;background:#fff;color:var(--black);line-height:1.45}
a{text-decoration:none;color:inherit}
button,input{font:inherit}
button{cursor:pointer}

/* TOP BAR */
.topbar{
  background:#0b0b0b;color:#fff;text-align:center;
  padding:9px 15px;font-size:10px;letter-spacing:2px;font-weight:700
}

/* NAV */
.nav{
  height:78px;border-bottom:1px solid var(--line);display:flex;
  align-items:center;justify-content:space-between;padding:0 5%;
  position:sticky;top:0;z-index:100;background:rgba(255,255,255,.96);
  backdrop-filter:blur(16px)
}
.logo{font-size:25px;font-weight:900;letter-spacing:5px}
.nav-links{display:flex;gap:32px;list-style:none;font-size:11px;font-weight:800;letter-spacing:1.6px}
.nav-links a{position:relative;padding:29px 0}
.nav-links a:after{content:"";position:absolute;left:0;bottom:22px;width:0;height:1px;background:#111;transition:.25s}
.nav-links a:hover:after{width:100%}
.nav-actions{display:flex;align-items:center;gap:17px}
.nav-actions button{background:none;border:0;font-size:19px}
.cart-btn{position:relative}
.cart-count{
  position:absolute;top:-7px;right:-9px;background:#111;color:#fff;
  min-width:17px;height:17px;border-radius:50%;font-size:9px;
  display:flex;align-items:center;justify-content:center
}

/* HERO */
.hero{
  min-height:680px;display:flex;align-items:center;padding:70px 7%;
  color:#fff;position:relative;overflow:hidden;
  background:
    linear-gradient(90deg,rgba(0,0,0,.72) 0%,rgba(0,0,0,.35) 45%,rgba(0,0,0,.08) 100%),
    url("https://images.unsplash.com/photo-1529139574466-a303027c1d8b?auto=format&fit=crop&w=2200&q=90") center/cover;
}
.hero-content{max-width:720px}
.eyebrow{font-size:10px;letter-spacing:4px;font-weight:800}
.hero h1{
  font-size:clamp(60px,11vw,140px);line-height:.86;
  letter-spacing:12px;font-weight:900;margin:18px 0
}
.hero-sub{
  font-size:15px;letter-spacing:4px;font-weight:600;margin-bottom:30px
}
.primary-btn{
  display:inline-flex;align-items:center;gap:18px;background:#fff;color:#111;
  padding:16px 24px;font-size:11px;letter-spacing:1.5px;font-weight:900;
  transition:.25s;border:1px solid #fff
}
.primary-btn:hover{background:#111;color:#fff;border-color:#111}
.hero-note{margin-top:18px;font-size:10px;letter-spacing:1.5px;opacity:.75}

/* TRUST */
.trust{
  display:grid;grid-template-columns:repeat(4,1fr);border-bottom:1px solid var(--line);
}
.trust div{padding:22px;text-align:center;border-right:1px solid var(--line)}
.trust div:last-child{border-right:0}
.trust strong{display:block;font-size:11px;letter-spacing:1px}
.trust span{font-size:10px;color:#888}

/* GENERAL */
.section{padding:95px 6%}
.section-head{margin-bottom:40px}
.section-head.center{text-align:center}
.section-label{font-size:10px;letter-spacing:3px;font-weight:900;margin-bottom:10px}
.section-head h2{font-size:38px;letter-spacing:2px;font-weight:900}
.section-head p{color:var(--muted);font-size:14px;margin-top:10px}

/* CATEGORY CARDS */
.categories{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.category-card{
  height:530px;position:relative;overflow:hidden;background:#eee;color:#fff
}
.category-card img{width:100%;height:100%;object-fit:cover;transition:.7s}
.category-card:hover img{transform:scale(1.07)}
.category-card:after{
  content:"";position:absolute;inset:0;
  background:linear-gradient(transparent 40%,rgba(0,0,0,.78))
}
.category-copy{position:absolute;z-index:2;bottom:32px;left:32px}
.category-copy small{font-size:10px;letter-spacing:3px;font-weight:800}
.category-copy h3{font-size:39px;letter-spacing:1px;margin:7px 0 14px}
.category-copy a{
  display:inline-block;font-size:10px;letter-spacing:1.5px;font-weight:900;
  border-bottom:1px solid #fff;padding-bottom:6px
}

/* SHOP */
.shop-section{background:#fafafa}
.shop-toolbar{
  display:flex;justify-content:space-between;align-items:end;
  gap:25px;margin-bottom:32px
}
.filters{display:flex;gap:7px;flex-wrap:wrap}
.filter{
  border:1px solid #d7d7d7;background:#fff;padding:11px 15px;
  font-size:10px;font-weight:900;letter-spacing:1px
}
.filter.active,.filter:hover{background:#111;color:#fff;border-color:#111}

/* PRODUCTS */
.products{display:grid;grid-template-columns:repeat(4,1fr);gap:22px}
.product{min-width:0}
.product-media{
  height:440px;background:#eee;overflow:hidden;position:relative
}
.product-media img{width:100%;height:100%;object-fit:cover;transition:.5s}
.product:hover .product-media img{transform:scale(1.045)}
.product-badge{
  position:absolute;left:12px;top:12px;background:#fff;padding:7px 9px;
  font-size:9px;font-weight:900;letter-spacing:1px;z-index:2
}
.product-heart{
  position:absolute;right:12px;top:12px;background:#fff;border:0;
  width:34px;height:34px;border-radius:50%;font-size:18px;z-index:2
}
.quick-add{
  position:absolute;left:12px;right:12px;bottom:12px;background:#111;color:#fff;
  border:0;padding:13px;font-size:10px;font-weight:900;letter-spacing:1.2px;
  transform:translateY(65px);transition:.3s
}
.product:hover .quick-add{transform:translateY(0)}
.product-info{padding:15px 2px 8px}
.product-category{font-size:9px;letter-spacing:2px;color:#888;font-weight:800;text-transform:uppercase}
.product-info h3{font-size:15px;margin:6px 0 7px;font-weight:800}
.price{font-size:14px;font-weight:900}
.product-old{color:#aaa;text-decoration:line-through;font-size:12px;margin-left:7px;font-weight:500}
.hidden{display:none!important}

/* FEATURE */
.feature{
  display:grid;grid-template-columns:1fr 1fr;min-height:590px;
  background:#111;color:#fff
}
.feature-image{min-height:590px}
.feature-image img{width:100%;height:100%;object-fit:cover}
.feature-copy{display:flex;flex-direction:column;justify-content:center;padding:70px 9%}
.feature-copy .eyebrow{color:#aaa}
.feature-copy h2{font-size:clamp(38px,5vw,66px);line-height:1;margin:18px 0}
.feature-copy p{color:#aaa;max-width:450px;font-size:14px;line-height:1.8;margin-bottom:30px}
.feature-copy .primary-btn{align-self:flex-start}

/* PROMO */
.promo{
  margin:95px 6%;min-height:400px;display:flex;align-items:center;
  justify-content:center;text-align:center;color:#fff;
  background:
    linear-gradient(rgba(0,0,0,.52),rgba(0,0,0,.52)),
    url("https://images.unsplash.com/photo-1483985988355-763728e1935b?auto=format&fit=crop&w=2000&q=90") center/cover
}
.promo h2{font-size:clamp(35px,5vw,60px);letter-spacing:4px}
.promo p{margin:13px 0 26px;color:#ddd;font-size:14px}

/* NEWSLETTER */
.newsletter{background:#f2f2f0;text-align:center;padding:75px 20px}
.newsletter h2{font-size:30px;letter-spacing:2px}
.newsletter p{color:#777;margin:9px 0 25px;font-size:13px}
.email-form{max-width:510px;margin:auto;display:flex}
.email-form input{flex:1;border:1px solid #ccc;background:#fff;padding:15px;outline:0}
.email-form button{background:#111;color:#fff;border:1px solid #111;padding:15px 24px;font-size:10px;font-weight:900;letter-spacing:1px}

/* FOOTER */
footer{background:#0b0b0b;color:#fff;padding:65px 6% 25px}
.footer-grid{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:45px;margin-bottom:55px}
.footer-brand h2{letter-spacing:5px;margin-bottom:14px}
.footer-brand p{color:#888;max-width:330px;font-size:13px;line-height:1.7}
footer h3{font-size:10px;letter-spacing:2px;margin-bottom:18px}
footer ul{list-style:none}
footer li{color:#888;font-size:12px;margin-bottom:11px;cursor:pointer}
footer li:hover{color:#fff}
.copyright{border-top:1px solid #292929;padding-top:20px;color:#666;text-align:center;font-size:10px;letter-spacing:1px}

/* CART DRAWER */
.overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.45);z-index:2000}
.overlay.show{display:block}
.cart{
  position:fixed;right:0;top:0;height:100%;width:min(420px,92%);
  background:#fff;z-index:2001;transform:translateX(100%);transition:.35s;
  padding:25px;display:flex;flex-direction:column
}
.cart.show{transform:translateX(0)}
.cart-head{display:flex;justify-content:space-between;align-items:center;padding-bottom:20px;border-bottom:1px solid var(--line)}
.cart-head h2{font-size:18px;letter-spacing:2px}
.close-cart{border:0;background:none;font-size:26px}
.cart-items{flex:1;overflow:auto;padding:20px 0}
.cart-item{display:flex;gap:13px;border-bottom:1px solid var(--line);padding:12px 0}
.cart-item img{width:72px;height:90px;object-fit:cover}
.cart-item h4{font-size:13px;margin-bottom:7px}
.cart-item p{font-size:12px;color:#777}
.cart-remove{border:0;background:none;font-size:11px;color:#999;margin-top:10px}
.cart-total{border-top:1px solid #111;padding-top:18px}
.cart-total div{display:flex;justify-content:space-between;font-weight:900;margin-bottom:16px}
.checkout{width:100%;padding:15px;background:#111;color:#fff;border:0;font-size:11px;font-weight:900;letter-spacing:1px}

/* MOBILE */
@media(max-width:1000px){
  .nav-links{gap:18px}
  .products{grid-template-columns:repeat(2,1fr)}
  .product-media{height:390px}
  .categories{grid-template-columns:1fr}
  .category-card{height:500px}
}
@media(max-width:700px){
  .topbar{font-size:8px}
  .nav{height:68px;padding:0 4%}
  .logo{font-size:20px;letter-spacing:3px}
  .nav-links{display:none}
  .hero{min-height:610px;padding:50px 7%}
  .hero h1{font-size:62px;letter-spacing:6px}
  .trust{grid-template-columns:1fr 1fr}
  .trust div:nth-child(2){border-right:0}
  .trust div{padding:17px 8px}
  .section{padding:65px 5%}
  .section-head h2{font-size:29px}
  .shop-toolbar{display:block}
  .filters{margin-top:20px}
  .products{grid-template-columns:1fr 1fr;gap:14px}
  .product-media{height:285px}
  .quick-add{transform:translateY(0);padding:11px}
  .feature{grid-template-columns:1fr}
  .feature-image{min-height:430px}
  .feature-copy{padding:55px 8%}
  .promo{margin:65px 5%;min-height:330px}
  .footer-grid{grid-template-columns:1fr 1fr;gap:30px}
}
@media(max-width:430px){
  .products{grid-template-columns:1fr 1fr}
  .product-media{height:245px}
  .product-info h3{font-size:12px}
  .price{font-size:12px}
  .category-copy h3{font-size:32px}
}
</style>
</head>

<body>

<div class="topbar">FREE SHIPPING ON ORDERS ABOVE ₹1,999 &nbsp; • &nbsp; WELCOME TO SHEZID</div>

<nav class="nav">
  <a href="#" class="logo">SHEZID</a>
  <ul class="nav-links">
    <li><a href="#">HOME</a></li>
    <li><a href="#collections">COLLECTIONS</a></li>
    <li><a href="#shop">SHOP</a></li>
    <li><a href="#about">ABOUT</a></li>
  </ul>
  <div class="nav-actions">
    <button onclick="alert('Search is coming soon.')">⌕</button>
    <button onclick="alert('Wishlist is coming soon.')">♡</button>
    <button class="cart-btn" onclick="openCart()">🛒<span class="cart-count" id="cartCount">0</span></button>
  </div>
</nav>

<section class="hero">
  <div class="hero-content">
    <div class="eyebrow">SHOPSHEZID / NEW SEASON 01</div>
    <h1>SHEZID</h1>
    <div class="hero-sub">WEAR YOUR IDENTITY.</div>
    <a href="#shop" class="primary-btn">SHOP THE COLLECTION <span>→</span></a>
    <div class="hero-note">PREMIUM T-SHIRTS • HOODIES • SHIRTS</div>
  </div>
</section>

<div class="trust">
  <div><strong>PREMIUM QUALITY</strong><span>Built for everyday wear</span></div>
  <div><strong>SECURE CHECKOUT</strong><span>Safe & simple shopping</span></div>
  <div><strong>EASY RETURNS</strong><span>Shop with confidence</span></div>
  <div><strong>SHEZID STANDARD</strong><span>Designed to stand out</span></div>
</div>

<section class="section" id="collections">
  <div class="section-head center">
    <div class="section-label">THE SHEZID EDIT</div>
    <h2>SHOP BY CATEGORY</h2>
    <p>Everyday essentials with a premium streetwear attitude.</p>
  </div>

  <div class="categories">
    <div class="category-card">
      <img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?auto=format&fit=crop&w=1000&q=90" alt="SHEZID T-Shirts">
      <div class="category-copy">
        <small>01 / ESSENTIALS</small>
        <h3>T-SHIRTS</h3>
        <a href="#shop" onclick="filterProducts('tshirt')">SHOP T-SHIRTS →</a>
      </div>
    </div>

    <div class="category-card">
      <img src="https://images.unsplash.com/photo-1556821840-3a63f95609a7?auto=format&fit=crop&w=1000&q=90" alt="SHEZID Hoodies">
      <div class="category-copy">
        <small>02 / PREMIUM LAYERS</small>
        <h3>HOODIES</h3>
        <a href="#shop" onclick="filterProducts('hoodie')">SHOP HOODIES →</a>
      </div>
    </div>

    <div class="category-card">
      <img src="https://images.unsplash.com/photo-1598033129183-c4f50c736f10?auto=format&fit=crop&w=1000&q=90" alt="SHEZID Shirts">
      <div class="category-copy">
        <small>03 / MODERN FITS</small>
        <h3>SHIRTS</h3>
        <a href="#shop" onclick="filterProducts('shirt')">SHOP SHIRTS →</a>
      </div>
    </div>
  </div>
</section>

<section class="section shop-section" id="shop">
  <div class="shop-toolbar">
    <div class="section-head" style="margin:0">
      <div class="section-label">CURATED FOR YOU</div>
      <h2>NEW ARRIVALS</h2>
      <p>Fresh SHEZID pieces, ready for your rotation.</p>
    </div>
    <div class="filters">
      <button class="filter active" onclick="filterProducts('all')">ALL</button>
      <button class="filter" onclick="filterProducts('tshirt')">T-SHIRTS</button>
      <button class="filter" onclick="filterProducts('hoodie')">HOODIES</button>
      <button class="filter" onclick="filterProducts('shirt')">SHIRTS</button>
    </div>
  </div>

  <div class="products">

    <article class="product" data-category="tshirt">
      <div class="product-media">
        <span class="product-badge">BESTSELLER</span>
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?auto=format&fit=crop&w=800&q=90" alt="Essential White Tee">
        <button class="quick-add" onclick="addToCart('Essential White Tee',1499,'https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">T-Shirts</div>
        <h3>Essential White Tee</h3>
        <div class="price">₹1,499 <span class="product-old">₹1,799</span></div>
      </div>
    </article>

    <article class="product" data-category="tshirt">
      <div class="product-media">
        <span class="product-badge">NEW</span>
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1503341504253-dff4815485f1?auto=format&fit=crop&w=800&q=90" alt="Signature Black Tee">
        <button class="quick-add" onclick="addToCart('Signature Black Tee',1499,'https://images.unsplash.com/photo-1503341504253-dff4815485f1?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">T-Shirts</div>
        <h3>Signature Black Tee</h3>
        <div class="price">₹1,499</div>
      </div>
    </article>

    <article class="product" data-category="tshirt">
      <div class="product-media">
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1583743814966-8936f37f4678?auto=format&fit=crop&w=800&q=90" alt="Oversized Core Tee">
        <button class="quick-add" onclick="addToCart('Oversized Core Tee',1599,'https://images.unsplash.com/photo-1583743814966-8936f37f4678?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">T-Shirts</div>
        <h3>Oversized Core Tee</h3>
        <div class="price">₹1,599</div>
      </div>
    </article>

    <article class="product" data-category="hoodie">
      <div class="product-media">
        <span class="product-badge">NEW</span>
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1556821840-3a63f95609a7?auto=format&fit=crop&w=800&q=90" alt="Premium Black Hoodie">
        <button class="quick-add" onclick="addToCart('Premium Black Hoodie',2499,'https://images.unsplash.com/photo-1556821840-3a63f95609a7?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">Hoodies</div>
        <h3>Premium Black Hoodie</h3>
        <div class="price">₹2,499 <span class="product-old">₹2,999</span></div>
      </div>
    </article>

    <article class="product" data-category="hoodie">
      <div class="product-media">
        <span class="product-badge">LIMITED</span>
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=800&q=90" alt="Street Oversized Hoodie">
        <button class="quick-add" onclick="addToCart('Street Oversized Hoodie',2699,'https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">Hoodies</div>
        <h3>Street Oversized Hoodie</h3>
        <div class="price">₹2,699</div>
      </div>
    </article>

    <article class="product" data-category="hoodie">
      <div class="product-media">
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1551488831-00ddcb6c6bd3?auto=format&fit=crop&w=800&q=90" alt="SHEZID Heavyweight Hoodie">
        <button class="quick-add" onclick="addToCart('SHEZID Heavyweight Hoodie',2899,'https://images.unsplash.com/photo-1551488831-00ddcb6c6bd3?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">Hoodies</div>
        <h3>SHEZID Heavyweight Hoodie</h3>
        <div class="price">₹2,899</div>
      </div>
    </article>

    <article class="product" data-category="shirt">
      <div class="product-media">
        <span class="product-badge">NEW</span>
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1598033129183-c4f50c736f10?auto=format&fit=crop&w=800&q=90" alt="Premium Casual Shirt">
        <button class="quick-add" onclick="addToCart('Premium Casual Shirt',1899,'https://images.unsplash.com/photo-1598033129183-c4f50c736f10?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">Shirts</div>
        <h3>Premium Casual Shirt</h3>
        <div class="price">₹1,899</div>
      </div>
    </article>

    <article class="product" data-category="shirt">
      <div class="product-media">
        <span class="product-badge">BESTSELLER</span>
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1603252110481-7ba873bf42ab?auto=format&fit=crop&w=800&q=90" alt="SHEZID Signature Shirt">
        <button class="quick-add" onclick="addToCart('SHEZID Signature Shirt',1999,'https://images.unsplash.com/photo-1603252110481-7ba873bf42ab?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">Shirts</div>
        <h3>SHEZID Signature Shirt</h3>
        <div class="price">₹1,999</div>
      </div>
    </article>

    <article class="product" data-category="shirt">
      <div class="product-media">
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1602810318383-e386cc2a3ccf?auto=format&fit=crop&w=800&q=90" alt="Oversized Everyday Shirt">
        <button class="quick-add" onclick="addToCart('Oversized Everyday Shirt',1799,'https://images.unsplash.com/photo-1602810318383-e386cc2a3ccf?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">Shirts</div>
        <h3>Oversized Everyday Shirt</h3>
        <div class="price">₹1,799</div>
      </div>
    </article>

    <article class="product" data-category="tshirt">
      <div class="product-media">
        <span class="product-badge">ESSENTIAL</span>
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1562157873-818bc0726f68?auto=format&fit=crop&w=800&q=90" alt="SHEZID Premium White Tee">
        <button class="quick-add" onclick="addToCart('SHEZID Premium White Tee',1699,'https://images.unsplash.com/photo-1562157873-818bc0726f68?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">T-Shirts</div>
        <h3>SHEZID Premium White Tee</h3>
        <div class="price">₹1,699</div>
      </div>
    </article>

    <article class="product" data-category="hoodie">
      <div class="product-media">
        <span class="product-badge">ESSENTIAL</span>
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1578681994506-b8f463449011?auto=format&fit=crop&w=800&q=90" alt="Essential Grey Hoodie">
        <button class="quick-add" onclick="addToCart('Essential Grey Hoodie',2599,'https://images.unsplash.com/photo-1578681994506-b8f463449011?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">Hoodies</div>
        <h3>Essential Grey Hoodie</h3>
        <div class="price">₹2,599</div>
      </div>
    </article>

    <article class="product" data-category="shirt">
      <div class="product-media">
        <span class="product-badge">DROP 01</span>
        <button class="product-heart">♡</button>
        <img src="https://images.unsplash.com/photo-1610652492500-ded1f6c8b0a9?auto=format&fit=crop&w=800&q=90" alt="SHEZID Premium Overshirt">
        <button class="quick-add" onclick="addToCart('SHEZID Premium Overshirt',2199,'https://images.unsplash.com/photo-1610652492500-ded1f6c8b0a9?auto=format&fit=crop&w=800&q=90')">ADD TO CART</button>
      </div>
      <div class="product-info">
        <div class="product-category">Shirts</div>
        <h3>SHEZID Premium Overshirt</h3>
        <div class="price">₹2,199</div>
      </div>
    </article>

  </div>
</section>

<section class="feature">
  <div class="feature-image">
    <img src="https://images.unsplash.com/photo-1529139574466-a303027c1d8b?auto=format&fit=crop&w=1200&q=90" alt="SHEZID campaign">
  </div>
  <div class="feature-copy">
    <div class="eyebrow">THE SHEZID STANDARD</div>
    <h2>LESS NOISE.<br>MORE IDENTITY.</h2>
    <p>SHEZID is built around clean silhouettes, confident fits and pieces that feel effortless. From the Essential White Tee to heavyweight hoodies and signature shirts — build your own uniform.</p>
    <a href="#shop" class="primary-btn">EXPLORE SHEZID <span>→</span></a>
  </div>
</section>

<section class="promo">
  <div>
    <div class="eyebrow">SHOPSHEZID / DROP 01</div>
    <h2>MAKE YOUR FIT<br>YOUR SIGNATURE.</h2>
    <p>Premium essentials. Modern streetwear. SHEZID.</p>
    <a href="#shop" class="primary-btn">SHOP NOW <span>→</span></a>
  </div>
</section>

<section class="newsletter">
  <h2>JOIN THE SHEZID DROP</h2>
  <p>Be first to know about new collections, limited drops and offers.</p>
  <form class="email-form" onsubmit="subscribe(event)">
    <input type="email" placeholder="Enter your email address" required>
    <button type="submit">JOIN SHEZID</button>
  </form>
</section>

<footer id="about">
  <div class="footer-grid">
    <div class="footer-brand">
      <h2>SHEZID</h2>
      <p>Premium contemporary streetwear for people who wear their identity with confidence.</p>
    </div>
    <div>
      <h3>SHOP</h3>
      <ul>
        <li onclick="filterProducts('tshirt')">T-Shirts</li>
        <li onclick="filterProducts('hoodie')">Hoodies</li>
        <li onclick="filterProducts('shirt')">Shirts</li>
        <li onclick="filterProducts('all')">All Products</li>
      </ul>
    </div>
    <div>
      <h3>HELP</h3>
      <ul><li>Contact</li><li>Shipping</li><li>Returns</li><li>FAQ</li></ul>
    </div>
    <div>
      <h3>FOLLOW</h3>
      <ul><li>Instagram</li><li>Facebook</li><li>YouTube</li></ul>
    </div>
  </div>
  <div class="copyright">© 2026 SHEZID / SHOPSHEZID. ALL RIGHTS RESERVED.</div>
</footer>

<div class="overlay" id="overlay" onclick="closeCart()"></div>
<aside class="cart" id="cart">
  <div class="cart-head">
    <h2>YOUR BAG</h2>
    <button class="close-cart" onclick="closeCart()">×</button>
  </div>
  <div class="cart-items" id="cartItems">
    <p style="color:#888;font-size:13px">Your bag is empty.</p>
  </div>
  <div class="cart-total">
    <div><span>SUBTOTAL</span><span id="cartTotal">₹0</span></div>
    <button class="checkout" onclick="alert('Checkout can be connected to a payment gateway later.')">PROCEED TO CHECKOUT</button>
  </div>
</aside>

<script>
let cartItems=[];

function filterProducts(category){
  document.querySelectorAll('.product').forEach(p=>{
    p.classList.toggle('hidden', category!=='all' && p.dataset.category!==category);
  });
  document.querySelectorAll('.filter').forEach(b=>b.classList.remove('active'));
  const wanted={
    all:'ALL',tshirt:'T-SHIRTS',hoodie:'HOODIES',shirt:'SHIRTS'
  }[category];
  document.querySelectorAll('.filter').forEach(b=>{
    if(b.textContent===wanted)b.classList.add('active');
  });
  document.getElementById('shop').scrollIntoView({behavior:'smooth'});
}

function addToCart(name,price,image){
  cartItems.push({name,price,image});
  document.getElementById('cartCount').textContent=cartItems.length;
  renderCart();
  openCart();
}

function renderCart(){
  const box=document.getElementById('cartItems');
  if(!cartItems.length){
    box.innerHTML='<p style="color:#888;font-size:13px">Your bag is empty.</p>';
  }else{
    box.innerHTML=cartItems.map((item,i)=>`
      <div class="cart-item">
        <img src="${item.image}" alt="${item.name}">
        <div>
          <h4>${item.name}</h4>
          <p>₹${item.price.toLocaleString('en-IN')}</p>
          <button class="cart-remove" onclick="removeCart(${i})">REMOVE</button>
        </div>
      </div>`).join('');
  }
  const total=cartItems.reduce((sum,i)=>sum+i.price,0);
  document.getElementById('cartTotal').textContent='₹'+total.toLocaleString('en-IN');
}

function removeCart(i){
  cartItems.splice(i,1);
  document.getElementById('cartCount').textContent=cartItems.length;
  renderCart();
}

function openCart(){
  document.getElementById('cart').classList.add('show');
  document.getElementById('overlay').classList.add('show');
}
function closeCart(){
  document.getElementById('cart').classList.remove('show');
  document.getElementById('overlay').classList.remove('show');
}
function subscribe(e){
  e.preventDefault();
  alert('Welcome to SHEZID. You are on the list!');
  e.target.reset();
}
</script>

</body>
</html>
