<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ריבועים אנכיים בגלילה</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body, html {
      height: 200vh; /* כדי שנוכל לגלול */
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
    }

    /* עיצוב הריבועים האנכיים */
    .vertical-boxes-container {
      position: fixed;
      right: -300px; /* התחלה מחוץ למסך */
      top: 50%;
      transform: translateY(-50%);
      display: flex;
      flex-direction: column;
      gap: 15px;
      z-index: 1000;
      transition: right 0.7s cubic-bezier(.68,-0.55,.27,1.55);
    }

    .vertical-boxes-container.show {
      right: 30px; /* מיקום סופי */
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
      transform: translateX(20px);
      transition: all 0.6s ease-out;
    }

    .vertical-box.show {
      opacity: 1;
      transform: translateX(0);
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
        bottom: 20px;
        top: unset;
        right: unset;
        left: 50%;
        transform: translateX(-50%);
        width: 90%;
        overflow-x: auto;
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

  <!-- תוכן דמה -->
  <div style="height: 200vh; padding: 50px;">
    <h1 style="color: white; text-align: center;">גלול מטה כדי לראות את הריבועים</h1>
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
        verticalBoxes.classList.remove('show');
        boxes.forEach(box => box.classList.remove('show'));
        arrows.forEach(arrow => arrow.style.opacity = '0');
      }
      
      lastScroll = currentScroll;
    });
  </script>
</body>
</html>

