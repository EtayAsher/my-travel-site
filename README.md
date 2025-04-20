<!DOCTYPE html>
<html lang="he">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>החופשה שלך מתחילה כאן</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            direction: rtl;
        }

        body, html {
            height: 100%;
            font-family: Arial, sans-serif;
            overflow-x: hidden;
        }

        .background {
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

        .content {
            position: relative;
            min-height: 200vh; /* מאפשר גלילה למטה */
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .email-box {
            background: rgba(255, 255, 255, 0.9);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
            text-align: center;
            max-width: 400px;
            width: 100%;
        }

        .email-box h1 {
            font-size: 24px;
            margin-bottom: 20px;
        }

        .email-box input[type="email"] {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 10px;
            font-size: 16px;
        }

        .email-box button {
            padding: 12px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 16px;
            cursor: pointer;
        }

        .popup {
            position: fixed;
            bottom: 50px;
            right: -400px;
            background-color: #28a745;
            color: white;
            padding: 20px;
            border-radius: 15px;
            max-width: 300px;
            transition: right 1s ease-in-out;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
            font-size: 18px;
        }

        .popup.show {
            right: 50%;
            transform: translateX(50%);
        }
    </style>
</head>

<body>
    <div class="background" id="background"></div>

    <div class="content">
        <div class="email-box">
            <h1>התחילו לתכנן את החופשה שלכם</h1>
            <input type="email" placeholder="הכניסו את האימייל שלכם">
            <button>הרשמה</button>
        </div>
    </div>

    <div class="popup" id="popup">
        היי! רוצים לתכנן את החופשה המושלמת שלכם אבל לא יודעים איך? הירשמו ונעזור לכם למצוא את החופשה הכי טובה וזולה בשבילכם
    </div>

    <script>
        const backgrounds = [
            "https://images.unsplash.com/photo-1507525428034-b723cf961d3e", // חוף
            "https://images.unsplash.com/photo-1533106418989-88406c7cc8c3", // ניו יורק
            "https://images.unsplash.com/photo-1578898886410-48c894e741e4", // פריז
            "https://images.unsplash.com/photo-1587397845856-d372dfd00f76", // רומא
            "https://images.unsplash.com/photo-1526483360782-42c61f2762f8", // תאילנד
            "https://images.unsplash.com/photo-1570732369289-0b66e4a5dc99", // יפן
            "https://images.unsplash.com/photo-1504674900247-0877df9cc836", // איסלנד
            "https://images.unsplash.com/photo-1582719478170-2b3a84b5b6df", // ברלין
            "https://images.unsplash.com/photo-1590490360183-76c6dba248b4"  // אפריקה
        ];

        const bgDiv = document.getElementById("background");
        let current = 0;

        function preloadImages(urls) {
            for (let i = 0; i < urls.length; i++) {
                const img = new Image();
                img.src = urls[i];
            }
        }

        function changeBackground() {
            bgDiv.style.backgroundImage = `url('${backgrounds[current]}')`;
            current = (current + 1) % backgrounds.length;
        }

        // טען את התמונות מראש
        preloadImages(backgrounds);

        // הצג מיד רקע ראשון
        bgDiv.style.backgroundImage = `url('${backgrounds[0]}')`;

        // החלפת רקעים כל 6 שניות
        setInterval(changeBackground, 6000);

        // הצגת הריבוע הירוק כשגוללים למטה
        const popup = document.getElementById("popup");
        window.addEventListener("scroll", () => {
            if (window.scrollY > window.innerHeight / 2) {
                popup.classList.add("show");
            }
        });
    </script>
</body>

</html>



