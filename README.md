<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
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
      overflow: hidden;
    }

    .background {
      position: fixed;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      background-size: cover;
      background-position: center;
      transition: background-image 1s ease-in-out;
      z-index: -1;
    }

    .form-container {
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .form-box {
      background-color: rgba(255, 255, 255, 0.9);
      padding: 30px 40px;
      border-radius: 15px;
      box-shadow: 0 0 25px rgba(0,0,0,0.3);
      text-align: center;
      max-width: 400px;
      width: 90%;
    }

    .form-box h2 {
      margin-bottom: 20px;
      font-size: 22px;
      color: #333;
    }

    .form-box input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 16px;
    }

    .form-box button {
      width: 100%;
      padding: 10px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
    }

    .form-box button:hover {
      background-color: #0056b3;
    }

    .form-box p {
      margin-top: 15px;
      font-size: 14px;
      color: #666;
    }
  </style>
</head>
<body>

  <div class="background" id="background"></div>

  <div class="form-container">
    <div class="form-box">
      <h2>הכניסו אימייל כדי שנמצא לכם את החופשה המושלמת!</h2>
      <input type="email" placeholder="כתובת אימייל">
      <button>הצטרפו עכשיו</button>
      <p>הרשמו כדי לקבל הצעות לחופשות זולות ומדהימות!</p>
    </div>
  </div>

  <script>
    const images = [
      'https://source.unsplash.com/1600x900/?new-york',
      'https://source.unsplash.com/1600x900/?rome',
      'https://source.unsplash.com/1600x900/?madrid',
      'https://source.unsplash.com/1600x900/?berlin',
      'https://source.unsplash.com/1600x900/?japan',
      'https://source.unsplash.com/1600x900/?china',
      'https://source.unsplash.com/1600x900/?thailand',
      'https://source.unsplash.com/1600x900/?africa',
      'https://source.unsplash.com/1600x900/?iceland',
      'https://source.unsplash.com/1600x900/?paris'
    ];

    let current = 0;
    const background = document.getElementById('background');

    function changeBackground() {
      background.style.backgroundImage = `url('${images[current]}')`;
      current = (current + 1) % images.length;
    }

    // Show first background immediately
    changeBackground();

    // Change every 6 seconds
    setInterval(changeBackground, 6000);
  </script>

</body>
</html>







