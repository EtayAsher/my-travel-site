<!DOCTYPE html>
<html lang="he">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>תכנון חופשה עם AI</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            min-height: 200vh; /* גובה מינימלי כדי לאפשר גלילה */
            overflow-x: hidden; /* חוסם גלילה אופקית */
        }

        .slideshow {
            position: fixed; /* הרקע נשאר קבוע */
            width: 100%;
            height: 100vh;
            z-index: -1; /* שולח את הרקע לאחור */
        }

        .slide {
            position: absolute;
            width: 100%;
            height: 100%;
            opacity: 0;
            transition: opacity 1s ease-in-out;
            background-size: cover;
            background-position: center;
        }

        .slide.active {
            opacity: 1;
        }

        .form-container {
            position: absolute;
            top: 100vh; /* מתחיל מתחת לגובה המסך */
            left: 50%;
            transform: translateX(-50%);
            background: rgba(255, 255, 255, 0.9);
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
            width: 90%;
            max-width: 400px;
            margin: 2rem 0; /* מרווח גלילה */
        }

        /* הוספתי תוכן לדוגמה כדי ליצור גלילה */
        .content {
            padding: 120vh 1rem 2rem; /* מרווח גדול מעל התוכן */
            max-width: 800px;
            margin: 0 auto;
            background: white;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            border-radius: 8px;
        }

        /* שאר העיצובים נשארים כמו מקודם */
        .form-title {
            text-align: center;
            margin-bottom: 1.5rem;
            color: #333;
            font-size: 1.5rem;
        }

        .form-group {
            margin-bottom: 1rem;
        }

        input {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-bottom: 0.5rem;
        }

        button {
            width: 100%;
            padding: 1rem;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
        }

        @media (max-width: 768px) {
            .form-container {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="slideshow">
        <!-- תמונות הרקע עם הלינקים האמיתיים -->
        <div class="slide active" style="background-image: url('https://images.unsplash.com/photo-1485871983421-0a9b3d42d2a3?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')"></div>
        <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1552832230-c0197dd311b5?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')"></div>
        <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1539037116277-4db20889f2d4?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')"></div>
        <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1523531294919-4bcd7c65e216?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')"></div>
        <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1492571351370-481d0a0a4a6e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')"></div>
        <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1547981609-4b6bfe67ca0b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')"></div>
        <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1524820197278-540916411e20?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')"></div>
        <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1547471080-7cc2caa01a7e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')"></div>
    </div>

    <div class="form-container">
        <h2 class="form-title">רוצים לתכנן את החופשה המושלמת שלכם בעזרת בינה מלאכותית ועוד כלים נוספים?</h2>
        <form>
            <div class="form-group">
                <input type="email" placeholder="אימייל" required>
            </div>
            <div class="form-group">
                <input type="password" placeholder="סיסמה" required>
            </div>
            <button type="submit">הירשם עכשיו</button>
        </form>
    </div>

    <!-- תוכן לדוגמה שיוצר גלילה -->
    <div class="content">
        <h2>מידע נוסף על השירות שלנו</h2>
        <p>כאן יופיע תוכן נוסף שאתה רוצה שיגללו אליו...</p>
        <p>ניתן להוסיף תמונות, טקסטים, קישורים וכל אלמנט אחר</p>
        <p>גובה הדיב הזה יוצר גלילה אוטומטית במסך</p>
    </div>

    <script>
        const slides = document.querySelectorAll('.slide');
        let currentSlide = 0;

        function nextSlide() {
            slides[currentSlide].classList.remove('active');
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].classList.add('active');
        }

        setInterval(nextSlide, 4000);
    </script>
</body>
</html>



