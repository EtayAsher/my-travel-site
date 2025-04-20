<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>תכנון חופשה עם AI</title>
  <style>
    body {
      min-height: 200vh;
      margin: 0;
      font-family: Arial, sans-serif;
    }
    /* עיצוב הריבוע הירוק */
    .fixed-message {
      position: fixed;
      top: 30%;
      left: -400px; /* מתחבא בצד שמאל */
      transform: translateY(-50%);
      background: linear-gradient(90deg, #43e97b 0%, #38f9d7 100%);
      color: #fff;
      padding: 30px 30px;
      border-radius: 15px;
      box-shadow: 0 4px 32px rgba(0,0,0,0.18);
      font-size: 1.2rem;
      font-weight: bold;
      z-index: 9999;
      transition: left 0.7s cubic-bezier(.68,-0.55,.27,1.55), box-shadow 0.4s;
      max-width: 350px;
      text-align: center;
      letter-spacing: 1px;
    }
    .fixed-message.show {
      left: 50%;
      transform: translate(-50%, -50%);
      box-shadow: 0 8px 40px 0 rgba(0,0,0,0.25);
    }
    @media (max-width: 600px) {
      .fixed-message {
        max-width: 90vw;
        font-size: 1rem;
        padding: 20px 10px;
      }
    }
  </style>
</head>
<body>

  <!-- ריבוע ירוק עיצובי -->
  <div class="fixed-message" id="fixedMessage">
    היי! רוצים לתכנן את החופשה המושלמת שלכם אבל לא יודעים איך?<br>
    הירשמו ונמצא עבורכם את החופשה הכי טובה וזולה עבורכם!
  </div>

  <script>
    // הצגת הריבוע כשגוללים חצי מסך ומעלה
    window.addEventListener('scroll', function() {
      const msg = document.getElementById('fixedMessage');
      if (window.scrollY > window.innerHeight / 2) {
        msg.classList.add('show');
      } else {
        msg.classList.remove('show');
      }
    });
  </script>
</body>
</html>






