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
      font-family: Arial, sans-serif;
    }

    body {
      height: 100vh;
      background-size: cover;
      background-position: center;
      animation: backgroundFade 30s infinite;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      color: white;
    }

    @keyframes backgroundFade {
      0% { background-image: url('https://source.unsplash.com/1600x900/?rome'); }
      25% { background-image: url('https://source.unsplash.com/1600x900/?new-york'); }
      50% { background-image: url('https://source.unsplash.com/1600x900/?paris'); }
      75% { background-image: url('https://source.unsplash.com/1600x900/?london'); }
      100% { background-image: url('https://source.unsplash.com/1600x900/?rome'); }
    }

    .container {
      background-color: rgba(0, 0, 0, 0.6);
      padding: 40px;
      border-radius: 15px;
      text-align: center;
      width: 300px;
    }

    h1 {
      font-size: 26px;
      margin-bottom: 15px;
    }

    p {
      font-size: 14px;
      margin-bottom: 20px;
    }

    input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: none;
      border-radius: 8px;
    }

    button {
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      background-color: #00bcd4;
      color: white;
      font-weight: bold;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #0097a7;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>✈️ תכננו את החופשה המושלמת שלכם!</h1>
    <p>הכניסו אימייל וסיסמה כדי שה-AI שלנו ימצא לכם את החופשה הכי טובה והכי זולה 🌍</p>
    <form>
      <input type="email" placeholder="כתובת אימייל" required />
      <input type="password" placeholder="סיסמה" required />
      <button type="submit">התחברות</button>
    </form>
  </div>
</body>
</html>


