<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Travel Site</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body, html {
      height: 100%;
      font-family: Arial, sans-serif;
      overflow-x: hidden;
    }
    .background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-size: cover;
      background-position: center;
      transition: background-image 1s ease-in-out;
      z-index: -1;
    }
    .email-box {
      position: relative;
      top: 30vh;
      margin: auto;
      width: 90%;
      max-width: 400px;
      padding: 30px;
      background: rgba(255, 255, 255, 0.85);
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 4px 20px rgba(0,0,0,0.2);
    }
    .email-box h2 {
      margin-bottom: 15px;
      font-size: 22px;
    }
    .email-box input {
      width: 80%;
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 10px;
    }
    .email-box button {
      padding: 10px 20px;
      background: #4CAF50;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    .popup {
      position: fixed;
      left: -400px;
      bottom: 20px;
      width: 300px;
      background: #4CAF50;
      color: white;
      padding: 20px;
      border-radius: 15px;
      transition: left 1s ease-in-out;
      z-index: 10;
    }
    .popup.active {
      left: 50%;
      transform: translateX(-50%);
    }
    .spacer {
      height: 150vh;
    }
  </style>
</head>
<body>
  <div class="background" id="background"></div>

  <div class="email-box">
    <h2>הכניסו את כתובת האימייל שלכם:</h2>
    <input type="email" placeholder="example@email.com" />
    <br />
    <button>הירשמו</button>
  </div>

  <div class="spacer"></div>

  <div class="popup" id="popup">
    היי! רוצים לתכנן את החופשה המושלמת שלכם אבל לא יודעים איך? הירשמו ונעזור לכם למצוא את החופשה הכי טובה וזולה בשבילכם.
  </div>

  <script>
    const images = [
      'https://images.unsplash.com/photo-1528909514045-2fa4ac7a08ba',
      'https://images.unsplash.com/photo-1507525428034-b723cf961d3e',
      'https://images.unsplash.com/photo-1549887534-4f09a761ab78',
      'https://images.unsplash.com/photo-1493558103817-58b2924bce98',
      'https://images.unsplash.com/photo-1607746882042-944635dfe10e',
      'https://images.unsplash.com/photo-1526772662000-3f88f10405ff',
      'https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05',
      'https://images.unsplash.com/photo-1535914254981-b5012eebbd15'
    ];

    const bg = document.getElementById('background');
    let currentIndex = 0;

    function changeBackground() {
      bg.style.backgroundImage = `url(${images[currentIndex]}?auto=compress&dpr=2&h=750&w=1260)`;
      currentIndex = (currentIndex + 1) % images.length;
    }

    window.addEventListener('load', () => {
      changeBackground();
      setInterval(changeBackground, 5000);
    });

    window.addEventListener('scroll', () => {
      const popup = document.getElementById('popup');
      const scrollY = window.scrollY;
      if (scrollY > 200) {
        popup.classList.add('active');
      }
    });
  </script>
</body>
</html>




