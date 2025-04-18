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
            height: 100vh;
            overflow: hidden;
        }

        .slideshow {
            position: relative;
            width: 100%;
            height: 100vh;
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
            max-width: 400px;
        }

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
        <div class="slide active" style="background-image: url('https://example.com/new-york.jpg')"></div>
        <div class="slide" style="background-image: url('https://example.com/rome.jpg')"></div>
        <div class="slide" style="background-image: url('https://example.com/madrid.jpg')"></div>
        <!-- הוסף כאן את שאר התמונות -->
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

    <script>
        const slides = document.querySelectorAll('.slide');
        let currentSlide = 0;

        function nextSlide() {
            slides[currentSlide].classList.remove('active');
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].classList.add('active');
        }

        // החלפת תמונה כל 5 שניות
        setInterval(nextSlide, 5000);
    </script>
</body>
</html>






