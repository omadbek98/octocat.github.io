<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="styles.css" />
  <title>Omadbek va Mushtariyxonlarning nikoh to'yida faxriy mehmon bo'ling!</title>
</head>
<body>
  <div class="invitation">
    <header>
      <h1>Hurmatli mehmonlar!</h1>
      <p>
        Sizni Omadbek va Mushtariyxonlarning nikoh to'yida faxriy mehmon bo'lishga taklif qilamiz.
      </p>
      <p>
        Qalblar ezguliklarga to‘la bo‘lgan ushbu qutlug‘ kunda do‘stlar yonida bo‘ling!
      </p>
    </header>

    <section class="details">
      <p><strong>Bayramni boshlash vaqti:</strong> 23.08.2025 / soat 17:00</p>
      <p><strong>To'y manzili:</strong> Tarona to'yxonasi</p>
      <a href="https://yandex.uz/maps/-/CHHeUIpD" target="_blank" class="map-button">Karta orqali ochish</a>
    </section>

    <div class="countdown">
      <div id="days" class="time">00 <span>kun</span></div>
      <div id="hours" class="time">00 <span>soat</span></div>
      <div id="minutes" class="time">00 <span>daqiqlar</span></div>
      <div id="seconds" class="time">00 <span>soniyalar</span></div>
    </div>

    <audio autoplay muted loop id="bgMusic">
  <source src="audio.mp3" type="audio/mp3" />
</audio>

<script>
  // Foydalanuvchi sahifaga birinchi marta tegganida musiqani ovozli qilish
  window.addEventListener('click', function () {
    const audio = document.getElementById('bgMusic');
    audio.muted = false;
    audio.play();
  }, { once: true }); // faqat bir marta ishlaydi
</script>
  </div>

  <script src="script.js"></script>
</body>
</html>
