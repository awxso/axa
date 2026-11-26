<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="AXA مساحة رقمية تجمع التقنية والإبداع والمعرفة في مكان واحد.">
<meta name="theme-color" content="#080808">
<title>AXA | عالم التقنية والإبداع</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;800&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#080808; --bg2:#101010; --card:#141414; --line:#2e2718;
  --gold:#d4af37; --gold2:#f3d978; --text:#f5f1e6; --muted:#b5afa0;
  color-scheme:dark;
}
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth;scroll-padding-top:80px}
body{font-family:'Cairo',Tahoma,Arial,sans-serif;background:var(--bg);color:var(--text);line-height:1.9;overflow-x:hidden}
a{color:inherit;text-decoration:none}
.gold{background:linear-gradient(90deg,var(--gold),var(--gold2),var(--gold));-webkit-background-clip:text;background-clip:text;color:transparent}

/* Header */
header{position:fixed;inset:0 0 auto;z-index:50;background:rgba(8,8,8,.72);backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px);border-bottom:1px solid rgba(212,175,55,.25)}
.bar{max-width:1100px;margin:auto;display:flex;align-items:center;justify-content:space-between;padding:12px 20px}
.logo{font-size:28px;font-weight:800;letter-spacing:6px}
nav{display:flex;gap:6px}
nav a{padding:6px 16px;border-radius:999px;font-size:15px;color:var(--muted);transition:.25s}
nav a:hover{color:var(--bg);background:var(--gold)}
.menu{display:none;background:none;border:1px solid var(--line);color:var(--gold);width:42px;height:42px;border-radius:10px;font-size:20px;cursor:pointer}

/* Hero */
.hero{position:relative;min-height:100vh;display:grid;place-items:center;text-align:center;padding:120px 20px 80px;overflow:hidden;
  background:radial-gradient(circle at 50% 0%,#2a2210 0%,transparent 60%),var(--bg)}
.hero::before,.hero::after{content:"";position:absolute;border-radius:50%;filter:blur(90px);opacity:.28;animation:float 9s ease-in-out infinite}
.hero::before{width:340px;height:340px;background:var(--gold);top:8%;right:-80px}
.hero::after{width:300px;height:300px;background:#8a6a12;bottom:5%;left:-80px;animation-delay:-4s}
@keyframes float{50%{transform:translateY(40px)}}
.hero-in{position:relative;z-index:1;max-width:720px}
.tag{display:inline-block;border:1px solid var(--gold);color:var(--gold);padding:4px 18px;border-radius:999px;font-size:14px;margin-bottom:22px;background:rgba(212,175,55,.07)}
.hero h2{font-size:clamp(32px,6vw,58px);line-height:1.4;font-weight:800;margin-bottom:16px}
.hero p{color:var(--muted);font-size:clamp(16px,2.4vw,20px);margin-bottom:34px}
.actions{display:flex;gap:14px;justify-content:center;flex-wrap:wrap}
.btn{display:inline-block;padding:12px 32px;border-radius:12px;font-weight:600;font-size:16px;transition:.25s}
.btn.primary{background:linear-gradient(135deg,var(--gold),var(--gold2));color:#080808;box-shadow:0 8px 28px rgba(212,175,55,.28)}
.btn.primary:hover{transform:translateY(-3px);box-shadow:0 12px 34px rgba(212,175,55,.45)}
.btn.ghost{border:1px solid var(--gold);color:var(--gold)}
.btn.ghost:hover{background:var(--gold);color:#080808}

/* Stats */
.stats{max-width:900px;margin:-50px auto 0;position:relative;z-index:2;display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:14px;padding:0 20px}
.stat{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:20px;text-align:center}
.stat b{display:block;font-size:30px;color:var(--gold);font-weight:800}
.stat span{color:var(--muted);font-size:14px}

/* Sections */
.section{padding:90px 20px;text-align:center;max-width:1100px;margin:auto}
.section h2{font-size:clamp(26px,4vw,38px);font-weight:800;margin-bottom:10px}
.section .sub{color:var(--muted);max-width:560px;margin:0 auto 46px}
.line{width:70px;height:3px;margin:14px auto 22px;border-radius:3px;background:linear-gradient(90deg,transparent,var(--gold),transparent)}
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:22px}
.card{position:relative;background:linear-gradient(160deg,#171717,#0f0f0f);border:1px solid var(--line);border-radius:18px;padding:34px 22px;transition:.35s;overflow:hidden}
.card::before{content:"";position:absolute;inset:0;background:radial-gradient(circle at 50% 0%,rgba(212,175,55,.16),transparent 65%);opacity:0;transition:.35s}
.card:hover{transform:translateY(-8px);border-color:var(--gold);box-shadow:0 18px 40px rgba(0,0,0,.5)}
.card:hover::before{opacity:1}
.icon{position:relative;width:64px;height:64px;margin:0 auto 16px;display:grid;place-items:center;font-size:30px;border-radius:18px;background:rgba(212,175,55,.1);border:1px solid rgba(212,175,55,.35)}
.card h3{position:relative;color:var(--gold);font-size:20px;margin-bottom:6px}
.card p{position:relative;color:var(--muted);font-size:15px}

/* About */
.about{background:var(--bg2);border-block:1px solid var(--line);max-width:none}
.about-in{max-width:720px;margin:auto}
.about p{color:#d6d0c0;font-size:18px}

/* Contact */
.contact-box{max-width:640px;margin:auto;background:var(--card);border:1px solid var(--line);border-radius:20px;padding:34px 24px}
.contact-box p{color:var(--muted);margin-bottom:22px}

footer{background:#000;border-top:1px solid rgba(212,175,55,.3);text-align:center;padding:28px 20px;color:var(--muted);font-size:14px}
footer b{color:var(--gold);letter-spacing:3px}

/* Reveal */
.reveal{opacity:0;transform:translateY(26px);transition:opacity .7s,transform .7s}
.reveal.in{opacity:1;transform:none}

@media(max-width:700px){
  .menu{display:block}
  nav{position:absolute;top:100%;inset-inline:0;flex-direction:column;background:rgba(8,8,8,.97);padding:10px 20px 18px;border-bottom:1px solid var(--line);display:none}
  nav.open{display:flex}
  nav a{padding:10px 14px}
}
@media(prefers-reduced-motion:reduce){
  *{animation:none!important;transition:none!important}
  html{scroll-behavior:auto}
  .reveal{opacity:1;transform:none}
}
</style>
</head>
<body>

<header>
  <div class="bar">
    <a href="#home" class="logo gold">AXA</a>
    <button class="menu" id="menu" aria-label="القائمة" aria-expanded="false">☰</button>
    <nav id="nav">
      <a href="#home">الرئيسية</a>
      <a href="#services">الخدمات</a>
      <a href="#about">من نحن</a>
      <a href="#contact">تواصل معنا</a>
    </nav>
  </div>
</header>

<main>
  <section class="hero" id="home">
    <div class="hero-in">
      <span class="tag">✦ التقنية · الإبداع · المعرفة</span>
      <h2>مرحباً بك في عالم <span class="gold">AXA</span></h2>
      <p>مساحتك الرقمية للتقنية والإبداع والمعرفة، في تجربة بسيطة ومميزة.</p>
      <div class="actions">
        <a href="#services" class="btn primary">اكتشف خدماتنا</a>
        <a href="#contact" class="btn ghost">تواصل معنا</a>
      </div>
    </div>
  </section>

  <div class="stats reveal">
    <div class="stat"><b>6</b><span>أقسام متنوعة</span></div>
    <div class="stat"><b>100%</b><span>مجاني وبسيط</span></div>
    <div class="stat"><b>24/7</b><span>متاح دائماً</span></div>
  </div>

  <section class="section" id="services">
    <h2 class="reveal">خدماتنا</h2>
    <div class="line"></div>
    <p class="sub reveal">كل ما تحتاجه من تقنية وإبداع ومعرفة في مكان واحد.</p>
    <div class="cards">
      <div class="card reveal"><div class="icon">🛠️</div><h3>الأدوات</h3><p>أدوات رقمية تساعدك في إنجاز مهامك بسهولة.</p></div>
      <div class="card reveal"><div class="icon">💻</div><h3>البرامج</h3><p>اكتشف البرامج والتطبيقات المفيدة.</p></div>
      <div class="card reveal"><div class="icon">📚</div><h3>التعليم</h3><p>تعلم مهارات جديدة واكتسب المعرفة.</p></div>
      <div class="card reveal"><div class="icon">🎨</div><h3>التصاميم</h3><p>مساحة للإبداع والأفكار والتصاميم.</p></div>
      <div class="card reveal"><div class="icon">📰</div><h3>المقالات</h3><p>اقرأ مقالات ومعلومات في مجالات متنوعة.</p></div>
      <div class="card reveal"><div class="icon">📩</div><h3>التواصل</h3><p>تواصل معنا للاستفسارات والمقترحات.</p></div>
    </div>
  </section>

  <section class="section about" id="about">
    <div class="about-in">
      <h2 class="reveal">من نحن</h2>
      <div class="line"></div>
      <p class="reveal">AXA مساحة رقمية تجمع التقنية والإبداع والمعرفة في مكان واحد، ونسعى إلى تقديم تجربة بسيطة ومميزة لكل زائر.</p>
    </div>
  </section>

  <section class="section" id="contact">
    <h2 class="reveal">تواصل معنا</h2>
    <div class="line"></div>
    <div class="contact-box reveal">
      <p>قريباً ستجد هنا وسائل التواصل الخاصة بنا. تابعنا لتصلك الإضافات الجديدة.</p>
      <a href="#home" class="btn primary">العودة للأعلى ↑</a>
    </div>
  </section>
</main>

<footer>© 2026 <b>AXA</b> - جميع الحقوق محفوظة</footer>

<script>
const nav=document.getElementById('nav'),menu=document.getElementById('menu');
menu.addEventListener('click',()=>{const o=nav.classList.toggle('open');menu.setAttribute('aria-expanded',o)});
nav.addEventListener('click',e=>{if(e.target.tagName==='A')nav.classList.remove('open')});
const io=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('in');io.unobserve(e.target)}}),{threshold:.15});
document.querySelectorAll('.reveal').forEach((el,i)=>{el.style.transitionDelay=(i%3)*90+'ms';io.observe(el)});
</script>
</body>
</html>
