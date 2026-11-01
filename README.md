
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#080b14">
  <meta name="description" content="علی امانی، طراح وب و توسعه‌دهنده سایت با WordPress، Elementor و WooCommerce.">
  <title>ALI STUDIO | علی امانی</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg:#080b14;
      --panel:rgba(255,255,255,.055);
      --border:rgba(255,255,255,.12);
      --text:#f4f7ff;
      --muted:#9aa6bb;
      --blue:#42a5ff;
      --cyan:#71e2ff;
    }

    * { margin:0; padding:0; box-sizing:border-box; }
    html { scroll-behavior:smooth; }
    body {
      font-family:'Vazirmatn',sans-serif;
      background:var(--bg);
      color:var(--text);
      overflow-x:hidden;
      line-height:1.8;
    }

    body::before {
      content:"";
      position:fixed;
      inset:0;
      z-index:-2;
      background:
        radial-gradient(ellipse at 15% 15%,rgba(0,119,255,.18),transparent 35%),
        radial-gradient(ellipse at 85% 60%,rgba(0,220,255,.09),transparent 35%),
        linear-gradient(145deg,#080b14,#0d1424 55%,#080b14);
    }

    a { color:inherit; text-decoration:none; }
    .container { width:min(1120px,90%); margin:auto; }

    .navbar {
      position:sticky;
      top:12px;
      z-index:100;
      width:min(1120px,94%);
      margin:12px auto 0;
      padding:13px 22px;
      display:flex;
      justify-content:space-between;
      align-items:center;
      background:rgba(13,19,32,.78);
      border:1px solid var(--border);
      border-radius:18px;
      backdrop-filter:blur(18px);
    }

    .logo {
      font-family:Arial,sans-serif;
      font-size:23px;
      font-weight:800;
      letter-spacing:2px;
      direction:ltr;
    }
    .logo span { color:var(--blue); }

    .nav-links { display:flex; gap:24px; align-items:center; }
    .nav-links a {
      color:var(--muted);
      font-size:13px;
      transition:.3s;
    }
    .nav-links a:hover { color:var(--cyan); }

    .menu-btn {
      display:none;
      color:white;
      background:none;
      border:0;
      font-size:25px;
    }

    .hero {
      min-height:650px;
      display:grid;
      grid-template-columns:1.1fr .9fr;
      align-items:center;
      gap:55px;
      padding-top:65px;
      padding-bottom:80px;
    }

    .eyebrow {
      color:var(--cyan);
      font-size:13px;
      letter-spacing:2px;
      margin-bottom:16px;
    }

    h1 {
      font-size:clamp(38px,6vw,65px);
      line-height:1.35;
      margin-bottom:20px;
      font-weight:800;
    }

    h1 span {
      color:var(--blue);
      text-shadow:0 0 30px rgba(66,165,255,.35);
    }

    .hero-desc {
      color:var(--muted);
      max-width:560px;
      font-size:16px;
      margin-bottom:30px;
    }

    .actions { display:flex; gap:13px; flex-wrap:wrap; }

    .btn {
      padding:12px 23px;
      border-radius:12px;
      font-size:14px;
      display:inline-flex;
      justify-content:center;
      align-items:center;
      transition:.3s;
      border:1px solid var(--border);
    }

    .btn-primary {
      color:#06101c;
      background:linear-gradient(120deg,#55b5ff,#78e6ff);
      font-weight:800;
      box-shadow:0 8px 30px rgba(45,155,255,.2);
    }

    .btn:hover { transform:translateY(-4px); }

    .btn-outline { background:var(--panel); }

    .photo-wrap {
      position:relative;
      width:min(100%,390px);
      margin:auto;
      padding:12px;
      border:1px solid rgba(83,177,255,.4);
      border-radius:35px;
      background:linear-gradient(145deg,rgba(66,165,255,.16),rgba(255,255,255,.025));
      box-shadow:0 25px 80px rgba(0,0,0,.45),0 0 55px rgba(40,135,255,.12);
      transform:perspective(1000px) rotateY(-5deg);
      animation:float 6s ease-in-out infinite;
    }

    .photo-wrap img {
      width:100%;
      height:480px;
      display:block;
      object-fit:cover;
      object-position:center 35%;
      border-radius:25px;
      background:#111827;
    }

    .photo-label {
      position:absolute;
      bottom:28px;
      right:25px;
      left:25px;
      padding:12px;
      text-align:center;
      border:1px solid var(--border);
      border-radius:13px;
      background:rgba(8,12,24,.78);
      backdrop-filter:blur(12px);
    }

    @keyframes float {
      0%,100% { transform:perspective(1000px) rotateY(-5deg) translateY(0); }
      50% { transform:perspective(1000px) rotateY(-2deg) translateY(-12px); }
    }

    section { padding:75px 0; }

    .section-title {
      text-align:center;
      margin-bottom:42px;
    }

    .section-title h2 {
      font-size:32px;
      margin-bottom:8px;
    }

    .section-title p { color:var(--muted); font-size:14px; }

    .accent { color:var(--cyan); }

    .glass {
      background:var(--panel);
      border:1px solid var(--border);
      border-radius:20px;
      backdrop-filter:blur(15px);
      box-shadow:0 15px 45px rgba(0,0,0,.15);
    }

    .about-card { padding:30px; }
    .about-card p { color:var(--muted); font-size:15px; }

    .info-grid {
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:15px;
      margin-top:25px;
    }

    .info-item {
      padding:17px;
      text-align:center;
      background:rgba(255,255,255,.035);
      border:1px solid var(--border);
      border-radius:14px;
    }

    .info-item strong { display:block; color:var(--cyan); font-size:14px; }
    .info-item span { color:var(--muted); font-size:12px; }

    .skills-grid {
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:17px;
    }

    .skill {
      padding:23px;
      transition:.3s;
    }

    .skill:hover,.project:hover {
      transform:translateY(-7px);
      border-color:rgba(66,165,255,.55);
      box-shadow:0 18px 45px rgba(0,90,180,.13);
    }

    .skill-icon { font-size:27px; margin-bottom:10px; }
    .skill h3 { font-size:17px; margin-bottom:7px; }
    .skill p { color:var(--muted); font-size:13px; }

    .projects-grid {
      display:grid;
      grid-template-columns:repeat(2,1fr);
      gap:20px;
    }

    .project {
      padding:25px;
      transition:.3s;
    }

    .project-tag {
      display:inline-block;
      color:var(--cyan);
      background:rgba(66,165,255,.1);
      padding:5px 12px;
      border-radius:30px;
      font-size:11px;
      margin-bottom:14px;
    }

    .project h3 { font-size:20px; margin-bottom:10px; }
    .project p { color:var(--muted); font-size:14px; margin-bottom:17px; }

    .project a { color:var(--cyan); font-size:13px; }

    .timeline { display:grid; gap:15px; }
    .timeline-item { padding:23px; }
    .timeline-item h3 { font-size:17px; margin-bottom:7px; }
    .timeline-item p { color:var(--muted); font-size:14px; }
    .date { color:var(--cyan); font-size:12px; }

    .contact-card {
      text-align:center;
      padding:38px 25px;
    }

    .contact-card p {
      color:var(--muted);
      margin:12px auto 25px;
      max-width:600px;
    }

    .contact-links {
      display:flex;
      justify-content:center;
      flex-wrap:wrap;
      gap:12px;
    }

    footer {
      padding:25px 10px;
      text-align:center;
      color:var(--muted);
      border-top:1px solid var(--border);
      font-size:12px;
    }

    .reveal {
      opacity:0;
      transform:translateY(25px);
      transition:opacity .7s ease,transform .7s ease;
    }

    .reveal.show { opacity:1; transform:translateY(0); }

    @media(max-width:800px) {
      .hero { grid-template-columns:1fr; text-align:center; gap:35px; padding-top:55px; }
      .hero-desc { margin-left:auto; margin-right:auto; }
      .actions { justify-content:center; }
      .photo-wrap { width:min(85%,340px); }
      .photo-wrap img { height:410px; }
      .skills-grid { grid-template-columns:repeat(2,1fr); }
      .nav-links {
        display:none;
        position:absolute;
        top:65px;
        right:0;
        left:0;
        flex-direction:column;
        gap:0;
        padding:12px;
        border:1px solid var(--border);
        border-radius:15px;
        background:#101827;
      }
      .nav-links.open { display:flex; }
      .nav-links a { padding:10px; }
      .menu-btn { display:block; }
    }

    @media(max-width:520px) {
      .skills-grid,.projects-grid { grid-template-columns:1fr; }
      .info-grid { grid-template-columns:1fr; }
      .section-title h2 { font-size:26px; }
      .hero { min-height:auto; }
    }

    @media(prefers-reduced-motion:reduce) {
      *,*::before,*::after {
        animation-duration:.01ms !important;
        transition-duration:.01ms !important;
        scroll-behavior:auto !important;
      }
    }
  </style>
</head>

<body>

  <nav class="navbar">
    <a class="logo" href="#home">ALI <span>STUDIO</span></a>

    <button class="menu-btn" id="menuBtn" aria-label="باز کردن منو">☰</button>

    <div class="nav-links" id="navLinks">
      <a href="#home">خانه</a>
      <a href="#about">درباره من</a>
      <a href="#skills">مهارت‌ها</a>
      <a href="#projects">نمونه‌کارها</a>
      <a href="#education">تحصیلات</a>
      <a href="#contact">ارتباط</a>
    </div>
  </nav>

  <main>
    <div class="container">
      <header class="hero" id="home">

        <div class="hero-content">
          <div class="eyebrow">WELCOME TO MY DIGITAL WORLD</div>

          <h1>
            سلام، من<br>
            <span>علی امانی</span> هستم
          </h1>

          <p class="hero-desc">
            طراح وب در مسیر یادگیری و پیشرفت؛ علاقه‌مند به طراحی
            تجربه‌های دیجیتال مدرن با WordPress، Elementor و ابزارهای هوش مصنوعی.
          </p>

          <div class="actions">
            <a href="#projects" class="btn btn-primary">مشاهده نمونه‌کارها</a>
            <a href="#contact" class="btn btn-outline">ارتباط با من</a>
          </div>
        </div>

        <div class="photo-wrap">
          <img src="assets/profile.jpg" alt="عکس شخصی علی امانی">
          <div class="photo-label">
            <strong>ALI AMANI</strong><br>
            <span class="accent">JUNIOR WEB DESIGNER</span>
          </div>
        </div>

      </header>

      <section id="about" class="reveal">
        <div class="section-title">
          <h2>درباره <span class="accent">من</span></h2>
          <p>کمی بیشتر با من آشنا شوید</p>
        </div>

        <div class="glass about-card">
          <p>
            من علی امانی هستم؛ دانشجوی مقطع کاردانی تأسیسات مکانیکی و
            علاقه‌مند به دنیای فناوری و طراحی وب. در حال یادگیری و توسعه
            مهارت‌هایم در زمینه طراحی سایت با وردپرس، المنتور و ووکامرس هستم.
            هدف من ساخت وب‌سایت‌های حرفه‌ای، زیبا و کاربردی و تبدیل مهارت‌هایم
            به تجربه کاری و همکاری در پروژه‌های واقعی است.
          </p>

          <div class="info-grid">
            <div class="info-item">
              <strong>تحصیلات</strong>
              <span>دانشجوی کاردانی</span>
            </div>
            <div class="info-item">
              <strong>زمینه فعالیت</strong>
              <span>طراحی وب</span>
            </div>
            <div class="info-item">
              <strong>نوع همکاری</strong>
              <span>کارآموزی و فریلنسری</span>
            </div>
          </div>
        </div>
      </section>

      <section id="skills" class="reveal">
        <div class="section-title">
          <h2>مهارت‌های <span class="accent">من</span></h2>
          <p>ابزارها و زمینه‌هایی که با آن‌ها کار می‌کنم</p>
        </div>

        <div class="skills-grid">
          <article class="glass skill">
            <div class="skill-icon">🌐</div>
            <h3>WordPress</h3>
            <p>ساخت و مدیریت وب‌سایت با سیستم مدیریت محتوای وردپرس.</p>
          </article>

          <article class="glass skill">
            <div class="skill-icon">🎨</div>
            <h3>Elementor</h3>
            <p>طراحی صفحات سایت و رابط کاربری با المنتور.</p>
          </article>

          <article class="glass skill">
            <div class="skill-icon">🛒</div>
            <h3>WooCommerce</h3>
            <p>آشنایی با ساخت و مدیریت فروشگاه اینترنتی.</p>
          </article>

          <article class="glass skill">
            <div class="skill-icon">🤖</div>
            <h3>هوش مصنوعی</h3>
            <p>استفاده از ابزارهای هوش مصنوعی برای یادگیری و انجام پروژه‌ها.</p>
          </article>

          <article class="glass skill">
            <div class="skill-icon">💻</div>
            <h3>ICDL</h3>
            <p>مهارت‌های عمومی کامپیوتر و کار با نرم‌افزارهای اداری.</p>
          </article>

          <article class="glass skill">
            <div class="skill-icon">✨</div>
            <h3>طراحی دیجیتال</h3>
            <p>علاقه‌مند به طراحی مدرن، تجربه کاربری و توسعه وب.</p>
          </article>
        </div>
      </section>

      <section id="projects" class="reveal">
        <div class="section-title">
          <h2>نمونه <span class="accent">کارها</span></h2>
          <p>پروژه‌ها و فعالیت‌های من</p>
        </div>

        <div class="projects-grid">
          <article class="glass project">
            <span class="project-tag">WORDPRESS · WOOCOMMERCE</span>
            <h3>فروشگاه ورزشی اسپرتینو</h3>
            <p>
              پروژه شخصی طراحی و توسعه فروشگاه اینترنتی محصولات ورزشی
              با استفاده از وردپرس، المنتور و ووکامرس.
            </p>
            <a href="https://tehamani.ir" target="_blank" rel="noopener noreferrer">
              مشاهده وب‌سایت ←
            </a>
          </article>

          <article class="glass project">
            <span class="project-tag">PERSONAL BRAND</span>
            <h3>ALI STUDIO</h3>
            <p>
              وب‌سایت شخصی من برای معرفی مهارت‌ها، رزومه،
              نمونه‌کارها و مسیر حرفه‌ای در دنیای طراحی وب.
            </p>
            <a href="#home">مشاهده همین وب‌سایت ←</a>
          </article>
        </div>
      </section>

      <section id="education" class="reveal">
        <div class="section-title">
          <h2>تحصیلات و <span class="accent">مدارک</span></h2>
          <p>مسیر آموزشی و گواهینامه‌ها</p>
        </div>

        <div class="timeline">
          <div class="glass timeline-item">
            <span class="date">در حال تحصیل</span>
            <h3>مقطع کاردانی تأسیسات مکانیکی</h3>
            <p>دانشجوی رشته تأسیسات مکانیکی.</p>
          </div>

          <div class="glass timeline-item">
            <span class="date">گواهینامه مهارتی</span>
            <h3>توسعه‌دهنده سیستم‌های مدیریت محتوای WordPress</h3>
            <p>۳۴۰ ساعت آموزش تخصصی – آموزشگاه سرای دانش.</p>
          </div>

          <div class="glass timeline-item">
            <span class="date">گواهینامه مهارتی</span>
            <h3>ICDL</h3>
            <p>۱۳۰ ساعت آموزش – نمره ۸۱ از ۱۰۰.</p>
          </div>
        </div>
      </section>

      <section id="interests" class="reveal">
        <div class="section-title">
          <h2>علایق <span class="accent">من</span></h2>
          <p>چیزهایی که به من انگیزه یادگیری می‌دهند</p>
        </div>

        <div class="skills-grid">
          <div class="glass skill">
            <div class="skill-icon">📚</div>
            <h3>مطالعه</h3>
            <p>علاقه‌مند به کتاب و یادگیری موضوعات جدید.</p>
          </div>
          <div class="glass skill">
            <div class="skill-icon">🏐</div>
            <h3>والیبال</h3>
            <p>ورزش، تمرین و پیشرفت فردی.</p>
          </div>
          <div class="glass skill">
            <div class="skill-icon">🚀</div>
            <h3>فناوری</h3>
            <p>دنبال کردن تکنولوژی و ابزارهای جدید.</p>
          </div>
        </div>
      </section>

      <section id="contact" class="reveal">
        <div class="section-title">
          <h2>ارتباط با <span class="accent">من</span></h2>
          <p>برای همکاری، پروژه و فرصت‌های کاری</p>
        </div>

        <div class="glass contact-card">
          <h2>بیایید با هم کار کنیم!</h2>
          <p>
            برای همکاری در پروژه‌های طراحی سایت، کارآموزی
            یا فرصت‌های شغلی می‌توانید از راه‌های زیر با من در ارتباط باشید.
          </p>

          <div class="contact-links">
            <a class="btn btn-primary"
               href="mailto:aliamani.2020111@gmail.com">
              ارسال ایمیل
            </a>

            <a class="btn btn-outline"
               href="https://wa.me/989023853579"
               target="_blank" rel="noopener noreferrer">
              پیام در واتساپ
            </a>
          </div>
        </div>
      </section>
    </div>
  </main>

  <footer>
    <p>© <span id="year"></span> ALI STUDIO — طراحی و توسعه با علاقه و خلاقیت</p>
  </footer>

  <script>
    const menuBtn = document.getElementById('menuBtn');
    const navLinks = document.getElementById('navLinks');

    menuBtn.addEventListener('click', () => {
      navLinks.classList.toggle('open');
    });

    document.querySelectorAll('.nav-links a').forEach(link => {
      link.addEventListener('click', () => {
        navLinks.classList.remove('open');
      });
    });

    document.getElementById('year').textContent =
      new Date().getFullYear();

    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('show');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.12 });

    document.querySelectorAll('.reveal').forEach(element => {
      observer.observe(element);
    });
  </script>

</body>
</html>

