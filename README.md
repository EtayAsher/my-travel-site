<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>תכנון חופשה עם AI</title>
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
      z-index: -1;
      transition: background-image 1s ease-in-out;
    }

    .content {
      position: relative;
      z-index: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      padding-top: 80px;
      min-height: 100vh;
    }

    .email-box {
      background: rgba(255, 255, 255, 0.9);
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
      max-width: 400px;
      width: 90%;
      text-align: center;
    }

    .email-box input {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 16px;
    }

    .email-box button {
      padding: 12px 24px;
      font-size: 16px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    /* סגנון הריבועים האנכיים */
    .vertical-boxes-container {
      position: fixed;
      bottom: -400px; /* התחלה מחוץ למסך */
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      flex-direction: column;
      gap: 15px;
      z-index: 1000;
      padding: 20px;
      transition: bottom 0.7s cubic-bezier(.68,-0.55,.27,1.55);
    }

    .vertical-boxes-container.show {
      bottom: 30px; /* מיקום סופי */
    }

    .vertical-box {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      padding: 25px;
      border-radius: 12px;
      width: 220px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      text-align: center;
      transform: translateY(20px);
      opacity: 0;
      transition: all 0.6s ease-out;
    }

    .vertical-box.show {
      opacity: 1;
      transform: translateY(0);
    }

    .vertical-arrow {
      color: white;
      font-size: 28px;
      text-align: center;
      margin: 5px 0;
      opacity: 0;
      transition: opacity 0.4s;
    }

    .vertical-boxes-container.show .vertical-arrow {
      opacity: 0.7;
    }

    .vertical-box:nth-child(1) { transition-delay: 0.1s; }
    .vertical-box:nth-child(2) { transition-delay: 0.3s; }
    .vertical-box:nth-child(3) { transition-delay: 0.5s; }
    .vertical-box:nth-child(4) { transition-delay: 0.7s; }

    .content-below {
      position: relative;
      top: 100vh;
      padding: 20px;
      height: 200vh;
    }
  </style>
</head>
<body>
  <div class="background" id="background"></div>

  <div class="content">
    <div class="email-box">
      <h2>תכננו את החופשה שלכם</h2>
      <input type="email" placeholder="כתובת אימייל">
      <input type="password" placeholder="סיסמה">
      <button>הרשמה</button>
    </div>
  </div>

  <!-- 4 הריבועים האנכיים -->
  <div class="vertical-boxes-container" id="verticalBoxes">
    <div class="vertical-box">
      <h3>טיפ #1</h3>
      <p>מציאת מלונות במחירים משתלמים</p>
    </div>
    <div class="vertical-arrow">↓</div>
    
    <div class="vertical-box">
      <h3>טיפ #2</h3>
      <p>המלצות מותאמות אישית</p>
    </div>
    <div class="vertical-arrow">↓</div>
    
    <div class="vertical-box">
      <h3>טיפ #3</h3>
      <p>השוואת מחירים חכמה</p>
    </div>
    <div class="vertical-arrow">↓</div>
    
    <div class="vertical-box">
      <h3>טיפ #4</h3>
      <p>הנחות בלעדיות</p>
    </div>
  </div>

  <div class="content-below"></div>

  <script>
    // רקע מתחלף
    const images = [
      'https://images.unsplash.com/photo-1507525428034-b723cf961d3e',
      'https://images.unsplash.com/photo-1506744038136-46273834b3fb',
      'https://images.unsplash.com/photo-1505761671935-60b3a7427bad',
      'https://images.unsplash.com/photo-1493558103817-58b2924bce98'
    ];

    const background = document.getElementById('background');
    let current = 0;
    background.style.backgroundImage = `url('${images[current]}')`;

    setInterval(() => {
      current = (current + 1) % images.length;
      background.style.backgroundImage = `url('${images[current]}')`;
    }, 5000);

    // ניהול גלילה
    const verticalBoxes = document.getElementById('verticalBoxes');
    const boxes = document.querySelectorAll('.vertical-box');
    const arrows = document.querySelectorAll('.vertical-arrow');
    let lastScroll = 0;

    window.addEventListener('scroll', () => {
      const currentScroll = window.scrollY;
      
      // גלילה מטה
      if (currentScroll > lastScroll) {
        if (currentScroll > 100) {
          verticalBoxes.classList.add('show');
          boxes.forEach(box => box.classList.add('show'));
          arrows.forEach(arrow => arrow.style.opacity = '0.7');
        }
      } 
      // גלילה מעלה
      else {
        if (currentScroll < 50) {
          verticalBoxes.classList.remove('show');
          boxes.forEach(box => box.classList.remove('show'));
          arrows.forEach(arrow => arrow.style.opacity = '0');
        }
      }
      
      lastScroll = currentScroll;
    });
  </script>
</body>
</html>


