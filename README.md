<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
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
    }

    .background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-size: cover;
      background-position: center;
      z-index: -1;
      transition: background-image 1s ease-in-out;
    }

    .overlay {
      position: relative;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .login-box {
      background-color: rgba(255, 255, 255, 0.85);
      padding: 30px;
      border-radius: 15px;
      text-align: center;
      max-width: 400px;
      width: 80%;
      box-shadow: 0 0 15px rgba(0,0,0,0.3);
    }

    .login-box h2 {
      margin-bottom: 15px;
    }

    .login-box input {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: none;
      border-radius: 8px;
      font-size: 16px;
    }

    .login-box button {
      padding: 12px 20px;
      font-size: 16px;
      border: none;
      background-color: #007bff;
      color: white;
      border-radius: 8px;
      cursor: pointer;
    }

    .login-box button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>

  <div class="background" id="background"></div>

  <div class="overlay">
    <div class="login-box">
      <h2>מצא את החופשה המושלמת עם AI 🌍</h2>
      <input type="email" placeholder="הכנס כתובת אימייל" />
      <input type="password" placeholder="סיסמה" />
      <button>התחבר</button>
    </div>
  </div>

  <script>
    const background = document.getElementById('background');

    // תמונת ברירת מחדל שתופיע ישר
    background.style.backgroundImage = "url('https://images.unsplash.com/photo-1491553895911-0055eca6402d?auto=format&fit=crop&w=1400&q=80')";

    // מערך של תמונות ערים בעולם
    const images = [
      "https://images.unsplash.com/photo-1505765050516-f72dcac9c60b?auto=format&fit=crop&w=1400&q=80", // ניו יורק
      "https://images.unsplash.com/photo-1604147706288-84b9cd36f977?auto=format&fit=crop&w=1400&q=80", // רומא
      "https://images.unsplash.com/photo-1587049352846-e969fa03b1a7?auto=format&fit=crop&w=1400&q=80", // טוקיו
      "https://images.unsplash.com/photo-1505761671935-60b3a7427bad?auto=format&fit=crop&w=1400&q=80", // לונדון
      "https://images.unsplash.com/photo-1551854838-9b190edc5b53?auto=format&fit=crop&w=1400&q=80", // ברלין
      "https://images.unsplash.com/photo-1612488627497-6f08e4973e99?auto=format&fit=crop&w=1400&q=80", // איסלנד
      "https://images.unsplash.com/photo-1588459461920-8c07b2cfaad1?auto=format&fit=crop&w=1400&q=80"  // אפריקה
    ];

    let current = 0;

    // כל 5 שניות מחליפים רקע
    setInterval(() => {
      background.style.backgroundImage = `url('${images[current]}')`;
      current = (current + 1) % images.length;
    }, 5000);
  </script>

</body>
</html>

