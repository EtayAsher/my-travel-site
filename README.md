<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>החופשה המושלמת</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      font-family: Arial, sans-serif;
      overflow-x: hidden;
    }

    .background {
      position: fixed;
      width: 100%;
      height: 100%;
      background-size: cover;
      background-position: center;
      z-index: -1;
      transition: background-image 1s ease-in-out;
    }

    .content {
      position: relative;
      min-height: 200vh;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding-top: 120px;
    }

    .email-box {
      background: rgba(255, 255, 255, 0.9);
      padding: 30px;
      border-radius: 16px;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
      max-width: 400px;
      text-align: center;
    }

    .email-box input[type="email"] {
      width: 90%;
      padding: 10px;
      margin-top: 10px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }

    .email-box input[type="submit"] {
      padding: 10px 20px;
      margin-top: 15px;
      background: #00aaff;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }

    .floating-box {
      position: fixed;
      left: -400px;
      bottom: 40px;
      background-color: #28a745;
      color: white;
      padding: 20px;
      border-radius: 12px;
      max-width: 300px;
      font-size: 16px;
      transition: left 1s ease;
      z-index: 1000;
    }

    .floating-box.visible {
      left: calc(50% - 150px);
    }
  </style>
</head>
<body>
  <div class="background" id="background"></div>

  <div class="content">
    <div class="email-box">
      <h2>הירשמו עכשיו</h2>
      <p>כדי שנתאים לכם את החופשה המושלמת!</p>
      <input type="email" placeholder="הכניסו אימייל">
      <br>
      <input type="submit" value="שליחה">
    </div>
  </div>

  <div class="floating-box" id="floatingBox">
    היי! רוצים לתכנן את החופשה המושלמת שלכם אבל לא יודעים איך? הירשמו ונעזור לכם למצוא את החופשה הכי טובה וזולה בשבילכם.
  </div>

  <script>
    const backgrounds = [
      "https://images.unsplash.com/photo-1507525428034-b723cf961d3e", // חוף
      "https://images.unsplash.com/photo-1549647316-e9fac1f88364", // ניו יורק
      "https://images.unsplash.com/photo-1568572933382-74d440642117", // יפן
      "https://images.unsplash.com/photo-1549647139-92b6cfefee31", // ברלין
      "https://images.unsplash.com/photo-1536129182218-cb5a1e0dcb9c", // וינה
      "https://images.unsplash.com/photo-1551887373-6d5b7dd6df03", // ונציה
      "https://images.unsplash.com/photo-1505761671935-60b3a7427bad", // לאס וגאס
      "https://images.unsplash.com/photo-1533090161767-e6ffed986c88"  // אוסטרליה
    ];

    let current = 0;
    const bg = document.getElementById("background");
    bg.style.backgroundImage = `url(${backgrounds[current]})`;

    setInterval(() => {
      current = (current + 1) % backgrounds.length;
      bg.style.backgroundImage = `url(${backgrounds[current]})`;
    }, 6000);

    // הופעת הריבוע הירוק בגלילה
    const floatingBox = document.getElementById("floatingBox");
    window.addEventListener("scroll", () => {
      if (window.scrollY > 300) {
        floatingBox.classList.add("visible");
      } else {
        floatingBox.classList.remove("visible");
      }
    });
  </script>
</body>
</html>




