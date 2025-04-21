<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
    .promo-box {
      position: fixed;
      top: 30%;
      left: -600px;
      transform: translateY(-50%);
      background: linear-gradient(90deg, #43e97b 0%, #38f9d7 100%);
      color: #fff;
      padding: 30px 40px;
      border-radius: 15px;
      box-shadow: 0 8px 32px rgba(0,0,0,0.2);
      font-size: 1.2rem;
      font-weight: bold;
      z-index: 2;
      transition: left 0.7s cubic-bezier(.68,-0.55,.27,1.55), box-shadow 0.4s;
      width: 500px;
      max-width: 90%;
      text-align: center;
      letter-spacing: 1px;
    }
    .promo-box.show {
      left: calc(50% - 250px);
      box-shadow: 0 12px 40px 0 rgba(0,0,0,0.3);
    }
    @media (max-width: 600px) {
      .promo-box {
        width: 90%;
        left: -100%;
        padding: 20px;
        font-size: 1rem;
      }
      .promo-box.show {
        left: 5%;
        transform: translateY(-50%);
      }
    }

    /* עיצוב הריבועים האנכיים החדש */
    .vertical-boxes-container {
      position: fixed;
      right: -300px;
      top: 50%;
      transform: translateY(-50%);
      display: flex;
      flex-direction: column;
      gap: 15px;
      z-index: 1000;
      padding: 20px;
      background: rgba(255,255,255,0.15);
      backdrop-filter: blur(10px);
      border-radius: 25px;
      border: 1px solid rgba(255,255,255,0.2);
      transition: right 0.5s cubic-bezier(.68,-0.55,.27,1.55);
    }

    .vertical-boxes-container.show {
      right: 30px;
    }

    .vertical-box {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      padding: 25px;
      border-radius: 15px;
      width: 220px;
      box-shadow: 0 8px 25px rgba(0,0,0,0.15);
      text-align: center;
      border: 1px solid rgba(255,255,255,0.3);
      transition: all 0.3s ease;
    }

    .vertical-box:hover {
      transform: translateX(-5px);
      box-shadow: 0 12px 30px rgba(0,0,0,0.2);
    }

    .vertical-box h3 {
      font-size: 1.4rem;
      margin-bottom: 10px;
      text-shadow: 0 2px 4px rgba(0,0,0,0.2);
    }

    .vertical-box p {
      font-size: 0.95rem;
      line-height: 1.5;
      opacity: 0.9;
    }

    .vertical-arrow {
      color: white;
      font-size: 28px;
      opacity: 0.7;
      margin: 5px 0;
      text-align: center;
      transition: all 0.3s;
    }

    @media (max-width: 1000px) {
      .vertical-boxes-container {
        flex-direction: row;
        bottom: 20px;
        top: unset;
        right: unset;
        left: 50%;
        transform: translateX(-50%);
        width: 90%;
        overflow-x: auto;
        padding: 15px;
      }
      
      .vertical-box {
        min-width: 200px;
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

  <div class="content">
    <div class="email-box">
      <h2>תכננו את החופשה שלכם</h2>
      <input type="email" placeholder="כתובת אימייל">
      <input type="password" placeholder="סיסמה">
      <button>הרשמה</button>
    </div>
  </div>

  <div class="promo-box" id="promoBox">
    <p>היי! רוצים לתכנן את החופשה המושלמת שלכם אבל לא יודעים איך? הירשמו ונמצא עבורכם את החופשה הכי טובה וזולה עבורכם!</p>
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

  <script>
    // רקע מתחלף
    const images = [
      'https://images.unsplash.com/photo-1507525428034-b723cf961d3e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80',
      'https://images.unsplash.com/photo-1506744038136-46273834b3fb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80',
      'https://images.unsplash.com/photo-1505761671935-60b3a7427bad?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80',
      'https://images.unsplash.com/photo-1493558103817-58b2924bce98?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80',
      'https://images.unsplash.com/photo-1470770841072-f978cf4d019e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80'
    ];

    const background = document.getElementById('background');
    let current = 0;
    
    function preloadImages() {
      images.forEach(img => {
        const image = new Image();
        image.src = img;
      });
    }

    preloadImages();
    background.style.backgroundImage = `url('${images[current]}')`;

    setInterval(() => {
      current = (current + 1) % images.length;
      background.style.backgroundImage = `url('${images[current]}')`;
    }, 5000);

    // ריבוע ירוק
    const promo = document.getElementById('promoBox');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 100) {
        promo.classList.add('show');
      }
    });

    // 4 הריבועים האנכיים
    const verticalBoxes = document.getElementById('verticalBoxes');
    let lastScroll = 0;
    
    window.addEventListener('scroll', () => {
      const currentScroll = window.scrollY;
      
      if (currentScroll > lastScroll) {
        // גלילה למטה
        if (currentScroll > 50) {
          verticalBoxes.classList.add('show');
        }
      } else {
        // גלילה למעלה
        verticalBoxes.classList.remove('show');
      }
      
      lastScroll = currentScroll;
    });

    // שמירה על מצב הריבועים בעת גלילה למעלה/מטה
    window.addEventListener('wheel', (e) => {
      if (e.deltaY > 0 && window.scrollY > 50) {
        verticalBoxes.classList.add('show');
      } else if (e.deltaY < 0) {
        verticalBoxes.classList.remove('show');
      }
    });
  </script>
</body>
</html>


