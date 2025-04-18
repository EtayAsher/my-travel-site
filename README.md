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
            min-height: 200vh;
        }

        .slideshow-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
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

        /* כדי שהרקע יופיע מייד */
        .slide:first-child {
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
            max-width: 400px;
        }

        .form-container h2 {
            text-align: center;
            margin-bottom: 1.5rem;
            color: #333;
            font-size: 1.5rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #555;
        }

        input {
            width: 100%;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-bottom: 0.5rem;
            font-size: 1rem;
        }

        button {
            width: 100%;
            padding: 1.2rem;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1rem;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #0056b3;
        }

        .fixed-message {
            position: absolute;
            top: 120%;
            left: -50%;
            transform: translateX(0);
            background: linear-gradient(to right, #4CAF50, #8BC34A);
            color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
            opacity: 0;
            transition: all 1s ease-in-out;
            width: 60%;
            max-width: 600px;
            text-align: center;
            font-size: 1.2rem;
            font-weight: bold;
            letter-spacing: 1px;
        }

        .fixed-message.show {
            left: 50%;
            transform: translateX(-50%);
            opacity: 1;
        }

        .content-below {
            position: relative;
            top: 100vh;
            padding: 20px;
        }

        /* הסרת עיצוב לכותרת החדשה */
        /* הוספת עיצוב לכותרת החדשה */
        .typing-title {
            position: absolute;
            top: 20px;
            left: 20px;
            font-size: 1.5rem;
            color: white;
            overflow: hidden;
            white-space: nowrap;
            border-right: .15em solid white;
            animation: typing 4s steps(40, end), blink-caret .75s step-end infinite;
        }

        /* אנימציית הקלדה */
        @keyframes typing {
            from {
                width: 0
            }

            to {
                width: 100%
            }
        }

        /* אנימציית קו אנכי */
        @keyframes blink-caret {

            from,
            to {
                border-color: transparent
            }

            50% {
                border-color: white;
            }
        }

        @media (max-width: 768px) {
            .form-container {
                padding: 1rem;
            }

            .fixed-message {
                width: 90%;
            }
        }
    </style>
</head>

<body>
    <div class="slideshow-container">
        <div class="slide active"
            style="background-image: url('https://images.unsplash.com/photo-1485871983421-0a9b3d42d2a3?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1552832230-c0197dd311b5?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1539037116277-4db20889f2d4?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1523531294919-4bcd7c65e216?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1492571351370-481d0a0a4a6e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1547981609-4b6bfe67ca0b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1524820197278-540916411e20?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1547471080-7cc2caa01a7e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1519125323398-675f0ddb6308?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1506748686214-e9df14d4d9d0?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
        <div class="slide"
            style="background-image: url('https://images.unsplash.com/photo-1477959858617-67f85660d58e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80')">
        </div>
    </div>

    <div class="form-container">
        <h2>רוצים לתכנן את החופשה המושלמת שלכם בעזרת בינה מלאכותית ועוד כלים נוספים?</h2>
        <form>
            <div class="form-group">
                <label for="email">אימייל:</label>
                <input type="email" id="email" placeholder="הכנס אימייל" required>
            </div>
            <div class="form-group">
                <label for="password">סיסמה:</label>
                <input type="password" id="password" placeholder="הכנס סיסמה" required>
            </div>
            <button type="submit">הירשם עכשיו</button>
        </form>
    </div>

    <div class="fixed-message">
        היי! רוצים לתכנן את החופשה המשולמת שלכם אבל לא יודעים מאיפה להתחיל? נמאס לשבור את הכיס על מלונות? הירשמו ונעזור לכם למצוא בדיוק את מה שאתם רוצים!
    </div>

    <div class="content-below">
        <!-- תוכן נוסף כאן - ניתן להוסיף תוכן שגוללים -->
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

        const fixedMessage = document.querySelector('.fixed-message');

        window.addEventListener('scroll', () => {
            if (window.scrollY > window.innerHeight / 2) {
                fixedMessage.classList.add('show');
            } else {
                fixedMessage.classList.remove('show');
            }
        });
    </script>
</body>

</html>
