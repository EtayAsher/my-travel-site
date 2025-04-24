<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Travel AI</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }
      body {
        font-family: 'Inter', sans-serif;
        background: linear-gradient(180deg, #dbeafe, #fdf2f8);
        color: #1f2937;
        line-height: 1.6;
        overflow-x: hidden;
      }
      .banner-popup {
        position: fixed;
        top: 20px;
        right: 20px;
        background-color: #3b82f6;
        color: white;
        padding: 1rem 1.5rem;
        border-radius: 0.75rem;
        box-shadow: 0 8px 16px rgba(0,0,0,0.1);
        font-size: 0.95rem;
        z-index: 1000;
        animation: fadeIn 1s ease-in-out;
        display: flex;
        align-items: center;
        gap: 0.75rem;
        transition: opacity 0.6s ease, transform 0.6s ease;
      }
      .banner-popup.hide {
        opacity: 0;
        transform: translateY(-20px);
      }
      .banner-popup button {
        background: none;
        border: none;
        color: white;
        font-size: 1rem;
        cursor: pointer;
      }
      @keyframes fadeIn {
        from { opacity: 0; transform: translateY(-10px); }
        to { opacity: 1; transform: translateY(0); }
      }
    </style>
    <script>
      window.onload = function() {
        setTimeout(function() {
          const popup = document.getElementById('popup');
          if (popup) popup.classList.add('hide');
        }, 7000); // נעלם אוטומטית אחרי 7 שניות
      };
      function closePopup() {
        const popup = document.getElementById('popup');
        if (popup) popup.classList.add('hide');
      }
    </script>
  </head>
  <body>
    <div class="banner-popup" id="popup">
      <span>ייעוץ דיגיטלי חכם מותאם לתיירות – קבל המלצות בהתאמה אישית!</span>
      <button onclick="closePopup()">✕</button>
    </div>
    <!-- שאר הקוד נשאר ללא שינוי -->
  </body>
</html>


