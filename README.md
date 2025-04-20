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
    html, body {
      height: 100%;
      font-family: Arial, sans-serif;
      overflow-x: hidden;
    }

    body {
      position: relative;
    }

    .background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      background-size: cover;
      background-position: center;
      animation: fadein 1s ease-in-out;
    }

    @keyframes fadein {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .overlay {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: rgba(255, 255, 255, 0.9);
      padding: 30px;
      border-radius: 16px;
      box-shadow: 0 0 25px rgba(0,0,0,0.3);
      text-align: center;
      width: 90%;
      max-width: 400px;
    }

    .overlay h2 {
      margin-bottom: 15px;
      font-size: 24px;
    }

    .overlay input {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 16px;
    }

    .overlay button {
      padding: 12px 25px;
      border: none;
      background-color: #28a745;
      color: white;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .overlay button:hover {
      background-color: #218838;
    }

    .slideup-box {
      position: fixed;
      left: 0;
      bottom: -200px;
      width: 100%;
      display: flex;
      justify-content: center;
      animation: slideUp 1s 2s forwards;
      z-index: 2;
    }

    .slideup-content {
      background-color: #4CAF50;
      padding: 20px;
      color: white;
      border-radius: 16px;
      max-width: 500px;
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
      font-size: 18px;
      text-align: center;
    }

    @keyframes slideUp {
      to {
        bottom: 50px;
      }
    }
  </style>
</head>
<body>
  <div class="background" id="background"></div>

  <div class="overlay">
    <h2>תכננו את החופשה שלכם</h2>
    <input type="email" placeholder="האימייל שלך">
    <input type="password" placeholder="סיסמה">
    <button>הרשמה</button>
  </div>

  <div class="slideup-box">
    <div class="slideup-content">
      היי! רוצים לתכנן את החופשה המושלמת שלכם אבל לא יודעים איך? הירשמו ונעזור לכם למצוא את החופשה הכי טובה וזולה בשבילכם
    </div>
  </div>

  <script>
    const backgrounds = [
      "https://images.unsplash.com/photo-1505761671935-60b3a7427bad", // ניו יורק
      "https://images.unsplash.com/photo-1584043720379-99dedc0e4d29", // רומא
      "https://images.unsplash.com/photo-1496317899792-9d7dbcd928a1", // טוקיו
      "https://images.unsplash.com/photo-1532767153582-b1a0e5145001", // מדריד
      "https://images.unsplash.com/photo-1528297506728-c51c7a19d5f8", // לונדון
      "https://images.unsplash.com/photo-1600683121800-5e09806f894d", // תאילנד
      "https://images.unsplash.com/photo-1582719478181-d048a1f397f1", // איסלנד
      "https://images.unsplash.com/photo-1573495612937-040b232f9f5c"  // ברלין
    ];

    let index = 0;
    const background = document.getElementById("background");
    background.style.backgroundImage = `url(${backgrounds[0]})`;

    setInterval(() => {
      index = (index + 1) % backgrounds.length;
      const img = new Image();
      img.src = backgrounds[index];
      img.onload = () => {
        background.style.backgroundImage = `url(${img.src})`;
      };
    }, 5000);
  </script>
</body>
</html>


