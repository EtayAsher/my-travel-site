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
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
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
      background: rgba(255, 255, 255, 0.95);
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.15);
      max-width: 400px;
      width: 90%;
      text-align: center;
      backdrop-filter: blur(5px);
      border: 1px solid rgba(255,255,255,0.2);
    }

    .email-box input {
      width: 100%;
      padding: 14px;
      margin: 12px 0;
      border-radius: 10px;
      border: 1px solid #e0e0e0;
      font-size: 16px;
      transition: all 0.3s;
    }

    .email-box input:focus {
      border-color: #4CAF50;
      box-shadow: 0 0 0 3px rgba(76, 175, 80, 0.2);
    }

    .email-box button {
      padding: 14px 28px;
      font-size: 16px;
      background: linear-gradient(135deg, #4CAF50 0%, #2E7D32 100%);
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: all 0.3s;
      box-shadow: 0 4px 15px rgba(46, 125, 50, 0.3);
    }

    .email-box button:hover {
      transform: translateY(-2px);
      box-shadow: 0 6px 20px rgba(46, 125, 50, 0.4);
    }

    .promo-box {
      position: fixed;
      top: 30%;
      left: -600px;
      transform: translateY(-50%);
      background: linear-gradient(90deg, #43e97b 0%, #38f9d7 100%);
      color: #fff;
      padding: 30px 40px;
      border-radius: 20px;
      box-shadow: 0 12px 40px rgba(0,0,0,0.25);
      font-size: 1.2rem;
      font-weight: bold;
      z-index: 2;
      transition: left 0.7s cubic-bezier(.68,-0.55,.27,1.55), box-shadow 0.4s;
      width: 500px;
      max-width: 90%;
      text-align: center;
      letter-spacing: 1px;
      backdrop-filter: blur(5px);
    }

    .promo-box.show {
      left: calc(50% - 250px);
      box-shadow: 0 15px 45px 0 rgba(0,0,0,0.35);
    }

    /* עיצוב הריבועים החדש - מודרני ומושך */
    .horizontal-boxes-container {
      position: fixed;
      bottom: -200px;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      gap: 20px;
      align-items: center;
      z-index: 1000;
      padding: 25px;
      background: rgba(255,255,255,0.15);
      backdrop-filter: blur(12px);
      border-radius: 25px;
      border: 1px solid rgba(255,255,255,0.2);
      box-shadow: 0 15px 35px rgba(0,0,0,0.2);
      transition: bottom 0.5s cubic-bezier(.22,.61,.36,1), opacity 0.4s;
    }

    .horizontal-box {
      background: linear-gradient(135deg, rgba(102, 126, 234, 0.9) 0%, rgba(118, 75, 162, 0.9) 100%);
      color: white;
      padding: 25px;
      border-radius: 15px;
      width: 240px;
      box-shadow: 0 8px 25px rgba(0,0,0,0.15);
      text-align: center;
      border: 1px solid rgba(255,255,255,0.3);
      transition: all 0.4s ease;
    }

    .horizontal-box:hover {
      transform: translateY(-5px);
      box-shadow: 0 12px 30px rgba(0,0,0,0.25);
    }

    .horizontal-box h3 {
      font-size: 1.4rem;
      margin-bottom: 10px;
      text-shadow: 0 2px 4px rgba(0,0,0,0.2);
    }

    .horizontal-box p {
      font-size: 0.95rem;
      line-height: 1.5;
      opacity: 0.9;
    }

    .horizontal-arrow {
      color: white;
      font-size: 32px;
      opacity: 0.7;
      margin: 0 -15px;
      text-shadow: 0 2px 5px rgba(0,0,0,0.2);
      transition: all 0.3s;
    }

    .horizontal-boxes-container.show {
      bottom: 30px;
    }

    @media (max-width: 1000px) {
      .horizontal-boxes-container {
        width: 95%;
        gap: 10px;
        padding: 20px 15px;
      }
      
      .horizontal-box {
        min-width: 180px;
        padding: 20px;
      }
      
      .horizontal-arrow {
        font-size: 24px;
        margin: 0 -10px;
      }
    }

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

  <div class="promo-box" id="promoBox">
    <p>היי! רוצים לתכנן את החופשה המושלמת שלכם אבל לא יודעים איך? הירשמו ונמצא עבורכם את החופשה הכי טובה וזולה עבורכם!</p>
  </div>

  <!-- 4 הריבועים האופקיים -->
  <div class="horizontal-boxes-container" id="horizontalBoxes">
    <div class="horizontal-box">
      <h3>טיפ #1</h3>
      <p>מציאת מלונות במחירים משתלמים</p>
    </div>
    <div class="horizontal-arrow">→</div>
    
    <div class="horizontal-box">
      <h3>טיפ #2</h3>
      <p>המלצות מותאמות אישית</p>
    </div>
    <div class="horizontal-arrow">→</div>
    
    <div class="horizontal-box">
      <h3>טיפ #3</h3>
      <p>השוואת מחירים חכמה</p>
    </div>
    <div class="horizontal-arrow">→</div>
    
    <div class="horizontal-box">
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
      'https://images.unsplash.com/photo-1493558103817-58b2924bce98',
      'https://images.unsplash.com/photo-1470770841072-f978cf4d019e',
      'https://images.unsplash.com/photo-1469474968028-56623f02e42e',
      'https://images.unsplash.com/photo-1483683804023-6ccdb62f86ef',
      'https://images.unsplash.com/photo-1482192596544-9eb780fc7f66',
      'https://images.unsplash.com/photo-1447752875215-b2761acb3c5d',
      'https://images.unsplash.com/photo-1500530855697-b586d89ba3ee'
    ];

    const background = document.getElementById('background');
    let current = 0;
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

    // 4 הריבועים האופקיים - גרסה סופית
    const horizontalBoxes = document.getElementById('


