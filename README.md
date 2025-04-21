<!DOCTYPE html>
<html lang="en">
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

    html, body {
      height: 100%;
      font-family: Arial, sans-serif;
      overflow-x: hidden;
    }

    body {
      background-size: cover;
      background-position: center;
      transition: background-image 1s ease-in-out;
    }

    .email-box {
      position: absolute;
      top: 20%;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(255, 255, 255, 0.9);
      padding: 2rem;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
      max-width: 400px;
      text-align: center;
    }

    .email-box h2 {
      margin-bottom: 1rem;
    }

    .email-box input {
      width: 100%;
      padding: 0.8rem;
      margin: 0.5rem 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    .email-box button {
      width: 100%;
      padding: 0.8rem;
      background-color: #28a745;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .promo-box {
      position: fixed;
      left: -400px;
      bottom: 20%;
      width: 300px;
      padding: 1rem;
      background-color: #28a745;
      color: white;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      transition: left 1s ease-in-out;
      z-index: 1000;
    }

    .promo-box.visible {
      left: 50%;
      transform: translateX(-50%);
    }
  </style>
</head>
<body>
  <div class="email-box">
    <h2>הירשמו עכשיו</h2>
    <input type="email" placeholder="הכנס את האימייל שלך" />
    <input type="password" placeholder="הכנס סיסמה" />
    <button>הרשמה</button>
  </div>

  <div class="promo-box" id="promoBox">
    היי! רוצים לתכנו את החופשה המושלמת שלכם אבל לא יודעים איך? הירשמו ונעזור לכם למצוא את החופשה הכי טובה וזולה בשבילכם
  </div>

  <script>
    const backgrounds = [
      "https://images.unsplash.com/photo-1507525428034-b723cf961d3e", // Beach
      "https://images.unsplash.com/photo-1549642046-39d96b6e78c1", // Mountains
      "https://images.unsplash.com/photo-1491553895911-0055eca6402d", // NYC
      "https://images.unsplash.com/photo-1505765050516-f72dcac9c60b", // Paris
      "https://images.unsplash.com/photo-1504198453319-5ce911bafcde", // Rome
      "https://images.unsplash.com/photo-1535914254981-b5012eebbd15", // Tokyo
      "https://images.unsplash.com/photo-1582719478250-c89cae4dc85f", // Iceland
      "https://images.unsplash.com/photo-1560347876-aeef00ee58a1", // Thailand
      "https://images.unsplash.com/photo-1580047095376-66159b2dbb62"  // Africa
    ];

    let currentIndex = 0;
    document.body.style.backgroundImage = `url(${backgrounds[currentIndex]})`;

    setInterval(() => {
      currentIndex = (currentIndex + 1) % backgrounds.length;
      const nextImage = new Image();
      nextImage.src = backgrounds[currentIndex];
      nextImage.onload = () => {
        document.body.style.backgroundImage = `url(${backgrounds[currentIndex]})`;
      };
    }, 6000);

    window.addEventListener("scroll", () => {
      const promo = document.getElementById("promoBox");
      if (window.scrollY > 200) {
        promo.classList.add("visible");
      } else {
        promo.classList.remove("visible");
      }
    });
  </script>
</body>
</html>



