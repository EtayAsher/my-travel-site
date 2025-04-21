<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>אתר חופשות מתקדם</title>
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

    /* רקע מתחלף */
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

    /* תיבת האימייל */
    .email-box {
      position: relative;
      z-index: 1;
      background: rgba(255, 255, 255, 0.95);
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.25);
      max-width: 400px;
      width: 90%;
      text-align: center;
      margin: 80px auto 0;
      backdrop-filter: blur(5px);
      transform: scale(0.98);
      transition: transform 0.3s ease;
    }

    .email-box:hover {
      transform: scale(1);
    }

    .email-box input {
      width: 100%;
      padding: 14px;
      margin: 12px 0;
      border-radius: 10px;
      border: 1px solid #ddd;
      font-size: 16px;
    }

    .email-box button {
      padding: 14px 28px;
      font-size: 16px;
      background: linear-gradient(90deg, #4CAF50 0%, #2E7D32 100%);
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      margin-top: 10px;
    }

    /* ריבועי הטיפים האנכיים */
    .vertical-boxes-container {
      position: fixed;
      bottom: -400px; /* מחוץ למסך */
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      flex-direction: column;
      gap: 15px;
      z-index: 1000;
      transition: bottom 0.7s cubic-bezier(.68,-0.55,.27,1.55);
      padding: 20px;
    }

    .vertical-boxes-container.show {
      bottom: 30px; /* נכנס לתוך המסך */
    }

    .vertical-box {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      padding: 25px;
      border-radius: 15px;
      width: 220px;
      box-shadow: 0 8px 25px rgba(0,0,0,0.2);
      text-align: center;
      opacity: 0;
      transform: translateY(20px);
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

    /* אנימציות לדיליי בין ריבועים */
    .vertical-box:nth-child(1) { transition-delay: 0.1s; }
    .vertical-box:nth-child(2) { transition-delay: 0.3s; }
    .vertical-box:nth-child(3) { transition-delay: 0.5s; }
    .vertical-box:nth-child(4) { transition-delay: 0.7s; }

    /* תוכן דמה לגלילה */
    .content-below {
      height: 200vh;
      position: relative;
      top: 100vh;
    }

    @media (max-width: 768px) {
      .vertical-boxes-container {
        flex-direction: row;
        width: 90%;
        overflow-x: auto;
        padding: 15px;
        gap: 10px;
      }
      .vertical-arrow {
        transform: rotate(90deg);
        margin: 0 10px;
      }
    }
  </style>
</head>
<body>
  <div class="background" id="background"></div>

  <div class="email-box">
    <h2>תכננו את החופשה המושלמת</h2>
    <input type="email" placeholder="כתובת אימייל">
    <input type="password" placeholder="סיסמה">
    <button>הרשמה</button>
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
      'https://images.unsplash.com/photo-1507525428034-b723cf961d3e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80',
      'https://images.unsplash.com/photo-1506744038136-46273834b3fb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80',
      'https://images.unsplash.com/photo-1505761671935-60b3a7427bad?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80',
      'https://images.unsplash.com/photo-1493558103817-58b2924bce98?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80'
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


