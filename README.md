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
const weddingDate = new Date('August 23, 2025 17:00:00').getTime();

function updateCountdown() {
  const now = new Date().getTime();
  const distance = weddingDate - now;

  const days = Math.floor(distance / (1000 * 60 * 60 * 24));
  const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  const seconds = Math.floor((distance % (1000 * 60)) / 1000);

  document.getElementById('days').innerHTML = days + " <span>kun</span>";
  document.getElementById('hours').innerHTML = hours + " <span>soat</span>";
  document.getElementById('minutes').innerHTML = minutes + " <span>daqiqlar</span>";
  document.getElementById('seconds').innerHTML = seconds + " <span>soniyalar</span>";

  if (distance < 0) {
    clearInterval(interval);
    document.querySelector('.countdown').innerHTML = "To'y boshlandi!";
  }
}

const interval = setInterval(updateCountdown, 1000);
body, html {
  height: 100%;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Arial', sans-serif;
  background: url('https://i.pinimg.com/originals/cc/48/3b/cc483b945cf746255339655b2a5f25b3.jpg') no-repeat center center fixed;
  background-size: cover;
}

.invitation {
  width: 100%;
  max-width: 500px;
  margin: 20px auto;
  padding: 20px;
  background-color: rgba(255, 255, 255, 0.9);
  color: #444;
  text-align: center;
  border: 2px solid #f5f5f5;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.7);
}

header h1, .details h2 {
  color: #d60051;
}

.countdown {
  display: flex;
  justify-content: space-around;
  margin-top: 20px;
  font-size: 1.5em;
}

.time {
  background: rgba(254, 182, 182, 0.9);
  padding: 10px 20px;
  border-radius: 10px;
}

.time span {
  display: block;
  font-size: 0.5em;
}

.map-button {
  display: inline-block;
  margin-top: 10px;
  padding: 10px 20px;
  background-color: #d60051;
  color: white;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
  transition: background-color 0.3s;
}

.map-button:hover {
  background-color: #bf0040;
}
