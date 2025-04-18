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
            min-height: 100vh; /* גובה מינימלי - אין צורך בגלילה */
            overflow-x: hidden; /* מניעת גלילה אופקית */
        }

        .slideshow-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
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
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(255, 255, 255, 0.9);
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
            width: 90%;
            max-width: 500px; /* הגדלת הריבוע הלבן */
            text-align: center;
        }

        .form-title {
            margin-bottom: 1.5rem;
            color: #333;
            font-size: 1.3rem; /* הקטנת הפונט */
            line-height: 1.4;
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
    <div class="slideshow-container">
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
        <h2 class="form-title">היי! רוצים לתכנן את החופשה המשולמת שלכם אבל לא יודעים מאיפה להתחיל? נמאס לשבור את הכיס על מלונות? הירשמו ונעזור לכם למצוא בדיוק את מה שאתם רוצים!</h2>
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


