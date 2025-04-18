<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
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
      animation: slideShow 20s infinite;
      z-index: -1;
    }

    @keyframes slideShow {
      0%   { background-image: url('https://source.unsplash.com/1600x900/?paris'); }
      25%  { background-image: url('https://source.unsplash.com/1600x900/?newyork'); }
      50%  { background-image: url('https://source.unsplash.com/1600x900/?rome'); }
      75%  { background-image: url('https://source.unsplash.com/1600x900/?tokyo'); }
      100% { background-image: url('https://source.unsplash.com/1600x900/?london'); }
    }

    .login-box {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: rgba(255, 255, 255, 0.9);
      padding: 40px;
      border-radius: 10px;
      text-align: center;
    }

    .login-box h2 {
      margin-bottom: 20px;
    }

    .login-box input {
      display: block;
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border: none;
      border-radius: 5px;
    }

    .login-box button {
      padding: 10px 20px;
      background-color: #2196F3;
      border: none;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }

    .login-box p {
      margin-top: 10px;
      font-size: 14px;
      color: #333;
    }
  </style>
</head>
<body>

<div class="background"></div>

<div class="login-box">
  <h2>ברוכים הבאים</h2>
  <p>הכניסו את המייל והסיסמה שלכם כדי למצוא את החופשה הכי טובה וזולה עם בינה מלאכותית!</p>
  <input type="email" placeholder="אימייל">
  <input type="password" placeholder="סיסמה">
  <button>התחבר</button>
</div>

</body>
</html>



