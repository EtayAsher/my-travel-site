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
      background-color: #000;
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
      border-radius: 12px;
      text-align: center;
      width: 300px;
      box-shadow: 0 0 20px rgba(0,0,0,0.4);
    }

    input[type="email"], input[type="password"] {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 6px;
    }

    button {
      padding: 12px 20px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-size: 16px;
      margin-top: 10px;
    }

    h2 {
      margin-bottom: 15px;
    }
  </style>
  <!-- טעינת התמונה הראשונה מראש -->
  <link rel="preload" as="image" href="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1400&q=80" />
</head>
<body>
  <div class="background" id="background"></div>
  <div class="overlay">
    <div class="login-box">
      <h2>Sign In</h2>
      <input type="email" placeholder="Enter your email" />
      <input type="password" placeholder="Enter your password" />
      <button>Login</button>
    </div>
  </div>

  <script>
    const background = document.getElementById("background");

    const images = [
      "https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1400&q=80", // default - ים
      "https://images.unsplash.com/photo-1543340900-74f240d74a40?auto=format&fit=crop&w=1400&q=80", // ניו יורק
      "https://images.unsplash.com/photo-1529612700005-e35377bf1415?auto=format&fit=crop&w=1400&q=80", // רומא
      "https://images.unsplash.com/photo-1549647190-376184a1eaf4?auto=format&fit=crop&w=1400&q=80", // ברלין
      "https://images.unsplash.com/photo-1512453979798-5ea266f8880c?auto=format&fit=crop&w=1400&q=80", // תאילנד
      "https://images.unsplash.com/photo-1576485291708-8d2b2c26348e?auto=format&fit=crop&w=1400&q=80", // יפן
      "https://images.unsplash.com/photo-1553413077-190dd3058716?auto=format&fit=crop&w=1400&q=80", // סין
      "https://images.unsplash.com/photo-1523978591478-c753949ff840?auto=format&fit=crop&w=1400&q=80", // אפריקה
      "https://images.unsplash.com/photo-1582471848501-3cc3419cf1c3?auto=format&fit=crop&w=1400&q=80"  // איסלנד
    ];

    let index = 0;

    // מיידית להגדיר את התמונה הראשונה
    background.style.backgroundImage = `url('${images[0]}')`;

    setInterval(() => {
      index = (index + 1) % images.length;
      background.style.backgroundImage = `url('${images[index]}')`;
    }, 6000); // כל 6 שניות מחליף תמונה
  </script>
</body>
</html>


