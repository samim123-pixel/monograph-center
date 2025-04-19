<!DOCTYPE html>
<html lang="ps">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>د مونوګراف جوړولو نړیوال مرکز</title>
  <style>
    :root {
      --main-color: #00796b;
      --light-color: #e0f2f1;
      --dark-color: #004d40;
      --text-color: #212121;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background: var(--light-color);
      color: var(--text-color);
      direction: rtl;
    }

    header, footer {
      background: var(--dark-color);
      color: white;
      padding: 1rem;
      text-align: center;
    }

    nav {
      background-color: white;
      text-align: center;
      padding: 0.5rem;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }

    nav a {
      margin: 0 1rem;
      text-decoration: none;
      color: var(--dark-color);
      font-weight: bold;
      font-size: 1.1rem;
    }

    .content {
      padding: 2rem;
      max-width: 1000px;
      margin: auto;
    }

    .form {
      background: white;
      padding: 2rem;
      border-radius: 15px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    input, textarea {
      width: 100%;
      margin-top: 0.5rem;
      padding: 0.75rem;
      font-size: 1rem;
      border-radius: 10px;
      border: 1px solid #ccc;
      margin-bottom: 1rem;
    }

    button {
      background: var(--main-color);
      color: white;
      padding: 0.75rem 1.5rem;
      border: none;
      border-radius: 10px;
      font-size: 1rem;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    button:hover {
      background: var(--dark-color);
    }

    .lang-switch {
      position: absolute;
      left: 10px;
      top: 10px;
    }

    ul {
      list-style-type: square;
      margin: 1rem 0;
      padding-right: 2rem;
    }

    @media (max-width: 600px) {
      .content {
        padding: 1rem;
      }
      nav a {
        display: block;
        margin: 0.5rem 0;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>د مونوګراف جوړولو نړیوال مرکز</h1>
    <div class="lang-switch">
      <a href="#" onclick="switchLang('en')" style="color:white;">English</a>
    </div>
  </header>

  <nav>
    <a href="#home">کور</a>
    <a href="#about">زموږ په اړه</a>
    <a href="#services">خدمتونه</a>
    <a href="#contact">اړیکه</a>
  </nav>

  <div class="content" id="home">
    <h2>ښه راغلاست!</h2>
    <p>موږ دلته یو څو تاسو ته د مونوګرافونو مسلکي، معیاري، او باور وړ خدمتونه وړاندې کړو. تاسو کولای شئ موضوع، معلومات او غوښتنې واستوئ او موږ به دا کار درته ترسره کړو.</p>
  </div>

  <div class="content" id="about">
    <h2>زموږ په اړه</h2>
    <p>موږ یو متخصص ټیم یو چې له اوږدې مودې راهیسې د مونوګرافونو، څېړنو او علمي پروژو په جوړولو کې تجربه لرو. د هر مشتری اړتیا ته ځانګړې پاملرنه کوو.</p>
  </div>

  <div class="content" id="services">
    <h2>خدمتونه</h2>
    <ul>
      <li>مونوګراف جوړول</li>
      <li>د موضوعاتو مشوره ورکول</li>
      <li>د څېړنې لیکنه، تنظیم او ترتیب</li>
      <li>بڼه: Word او PDF</li>
      <li>قیمت: ۱۵۰۰ افغانۍ</li>
      <li>وړیا مشوره</li>
    </ul>
  </div>

  <div class="content" id="contact">
    <h2>اړیکه</h2>
    <div class="form">
      <label for="name">ستاسو نوم:</label>
      <input type="text" id="name" placeholder="مثلاً احمد">

      <label for="subject">د مونوګراف موضوع:</label>
      <input type="text" id="subject" placeholder="مثلاً د افغانستان اقتصاد">

      <label for="message">نور معلومات:</label>
      <textarea id="message" rows="4" placeholder="خپله اړتیا، موضوع، یا ځانګړي غوښتنې ولیکئ..."></textarea>

      <button onclick="sendToWhatsApp()">واتساپ ته واستوه</button>
    </div>
  </div>

  <footer>
    &copy; 2025 - د مونوګراف نړیوال مرکز | جوړونکی: ساميم | واتساپ: 093711489188
  </footer>

  <script>
    function sendToWhatsApp() {
      const name = document.getElementById('name').value.trim();
      const subject = document.getElementById('subject').value.trim();
      const message = document.getElementById('message').value.trim();

      if (!name || !subject) {
        alert("مهرباني وکړئ نوم او موضوع ډک کړئ.");
        return;
      }

      const fullMsg = `سلام، زما نوم ${name} دی. زه غواړم یو مونوګراف جوړ کړم.\nموضوع: ${subject}\nنور معلومات: ${message}`;
      const url = `https://wa.me/93711489188?text=${encodeURIComponent(fullMsg)}`;
      window.open(url, '_blank');
    }

    function switchLang(lang) {
      alert('English version will be available soon.');
    }
  </script>
</body>
</html>
