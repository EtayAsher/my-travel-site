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

    #background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-size: cover;
      background-position: center;
      transition: background-image 1s ease-in-out;
      z-index: -1;
    }

    .login-box {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: rgba(255, 255, 255, 0.9);
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
      width: 300px;
      text-align: center;
    }

    .login-box h2 {
      margin-bottom: 15px;
    }

    .login-box input {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .login-box button {
      padding: 10px 20px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .login-box button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>

<div id="background"></div>

<div class="login-box">
  <h2>הכניסו את המייל והסיסמה</h2>
  <p>כדי שנוכל למצוא לכם את החופשה הכי טובה והכי זולה עם AI!</p>
  <input type="email" placeholder="אימייל" required />
  <input type="password" placeholder="סיסמה" required />
  <br />
  <button>התחברות</button>
</div>

<script>
  const background = document.getElementById('background');

  // תמונת רקע ראשונה (מופיעה מיד)
  background.style.backgroundImage = "url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1400&q=80')";

  // כל שאר התמונות
  const images = [
    "https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1400&q=80", // Beach
    "https://images.unsplash.com/photo-1491553895911-0055eca6402d?auto=format&fit=crop&w=1400&q=80", // New York
    "https://images.unsplash.com/photo-1587502536263-9298d7a1c1e1?auto=format&fit=crop&w=1400&q=80", // Rome
    "https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?auto=format&fit=crop&w=1400&q=80", // Thailand
    "https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=1400&q=80", // Japan
    "https://images.unsplash.com/photo-1571501679680-de32f1e7aad4?auto=format&fit=crop&w=1400&q=80", // Iceland
    "https://images.unsplash.com/photo-1512453979798-5ea266f8880c?auto=format&fit=crop&w=1400&q=80"  // Africa
  ];

  let index = 0;
  setInterval(() => {
    index = (index + 1) % images.length;
    background.style.backgroundImage = `url('${images[index]}')`;
  }, 5000); // כל 5 שניות
</script>

</body>
</html>

