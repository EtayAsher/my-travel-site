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
      background: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e') center/cover;
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

    /* תיבת האימייל המעודכנת */
    .email-box {
      background: rgba(255, 255, 255, 0.95);
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.25);
      max-width: 400px;
      width: 90%;
      text-align: center;
      backdrop-filter: blur(5px);
      margin: 20px;
      transform: scale(0.95);
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
      transition: box-shadow 0.3s;
    }

    .email-box input:focus {
      box-shadow: 0 0 0 3px rgba(76, 175, 80, 0.3);
      outline: none;
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
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .email-box button:hover {
      transform: translateY(-2px);
      box-shadow: 0 5px 15px rgba(46, 125, 50, 0.4);
    }

    /* הריבועים האנכיים במרכז */
    .vertical-boxes-container {
      position: fixed;
      bottom: -300px; /* התחלה מחוץ למסך */
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      flex-direction: column;
      gap: 15px;
      z-index: 1000;
      transition: bottom 0.7s cubic-bezier(.68,-0.55,.27,1.55);
      background: rgba(255,255,255,0.2);
      backdrop-filter: blur(10px);
      padding: 20px;
      border-radius: 25px;
      border: 1px solid rgba(255,255,255,0.3);
    }

    .vertical-boxes-container.show {
      bottom: 30px; /* מיקום סופי */
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

    .vertical-box:nth-child(1) { transition-delay: 0.1s; }
    .vertical-box:nth-child(2) { transition-delay: 0.3s; }
    .vertical-box:nth-child(3) { transition-delay: 0.5s; }
    .vertical-box:nth-child(4) { transition-delay: 0.7s; }

    @media (max-width: 768px) {
      .vertical-boxes-container {
        flex-direction: row;
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
  <div class="background"></div>

  <div class="content">
    <div class="email-box">
      <h2>תכננו את החופשה שלכם</h2>
      <input type="email" placeholder="כתובת אימייל">
      <input type="password" placeholder="סיסמה">
      <button>הרשמה</button>
    </div>
  </div>

  <!-- הריבועים האנכיים -->
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

