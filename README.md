<!DOCTYPE html>
<html lang="en">
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
    /* עיצוב הריבוע הירוק - מודרני ורחב יותר */
    .promo-box {
      position: fixed;
      top: 30%;
      left: -600px; /* מתחבא בצד שמאל */
      transform: translateY(-50%);
      background: linear-gradient(90deg, #43e97b 0%, #38f9d7 100%);
      color: #fff;
      padding: 30px 40px; /* יותר מרווח */
      border-radius: 15px;
      box-shadow: 0 8px 32px rgba(0,0,0,0.2);
      font-size: 1.2rem;
      font-weight: bold;
      z-index: 2;
      transition: left 0.7s cubic-bezier(.68,-0.55,.27,1.55), box-shadow 0.4s;
      width: 500px; /* יותר רחב */
      max-width: 90%;
      text-align: center;
      letter-spacing: 1px;
    }
    .promo-box.show {
      left: calc(50% - 250px); /* ממרכז בהתאם לרוחב החדש */
      box-shadow: 0 12px 40px 0 rgba(0,0,0,0.3);
    }
    @media (max-width: 600px) {
      .promo-box {
        width: 90%; /* תופס 90% מהמסך */
        left: -100%;
        padding: 20px;
        font-size: 1rem;
      }
      .promo-box.show {
        left: 5%; /* מוצג עם שוליים בצדדים */
        transform: translateY(-50%);
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
    <p>היי! רוצים לתכנן את החופשה המושלמת שלכם אבל לא יודעים איך? הירשמו ונעזור לכם למצוא את החופשה הכי טובה וזולה בשבילכם</p>
  </div>

  <script>
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

    window.addEventListener('scroll', () => {
      const promo = document.getElementById('promoBox');
      if (window.scrollY > 100) {
        promo.classList.add('show');
      }
    });
  </script>
</body>
</html>


