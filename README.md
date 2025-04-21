<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DreamTrip AI</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body,
    html {
      height: 100%;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    .background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-size: cover;
      background-position: center;
      z-index: -1;
      animation: backgroundFade 20s infinite;
    }

    @keyframes backgroundFade {
      0% {
        background-image: url('https://source.unsplash.com/1600x900/?beach');
      }
      25% {
        background-image: url('https://source.unsplash.com/1600x900/?paris');
      }
      50% {
        background-image: url('https://source.unsplash.com/1600x900/?mountains');
      }
      75% {
        background-image: url('https://source.unsplash.com/1600x900/?newyork');
      }
      100% {
        background-image: url('https://source.unsplash.com/1600x900/?travel');
      }
    }

    .content {
      padding: 50px 20px;
      text-align: center;
      color: white;
      min-height: 120vh;
      background: rgba(0, 0, 0, 0.5);
    }

    h1 {
      font-size: 3em;
      margin-bottom: 0.5em;
    }

    p {
      font-size: 1.2em;
      max-width: 800px;
      margin: auto;
    }

    .email-box {
      margin-top: 40px;
    }

    input[type="email"] {
      padding: 10px;
      width: 250px;
      font-size: 1em;
      border-radius: 5px;
      border: none;
    }

    input[type="submit"] {
      padding: 10px 20px;
      font-size: 1em;
      background-color: green;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      margin-left: 10px;
    }

    .popup-box {
      position: fixed;
      bottom: 50px;
      left: -300px;
      background-color: #28a745;
      color: white;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
      font-size: 18px;
      transition: left 1s ease-in-out;
    }

    .popup-box.show {
      left: calc(50% - 150px);
    }
  </style>
</head>

<body>
  <div class="background"></div>
  <div class="content">
    <h1>Plan Your Dream Trip with AI</h1>
    <p>Our smart assistant helps you create your perfect vacation in seconds. Just answer a few questions and get a tailored travel package – instantly. Flights, hotels, and activities based on your preferences and budget.</p>

    <div class="email-box">
      <input type="email" placeholder="Enter your email" />
      <input type="submit" value="Get Started" />
    </div>
  </div>

  <div class="popup-box" id="popup">
    Hey! Want help planning your perfect trip but not sure how?
  </div>

  <script>
    // Popup animation
    window.addEventListener("scroll", function () {
      const popup = document.getElementById("popup");
      if (window.scrollY > 150) {
        popup.classList.add("show");
      }
    });
  </script>
</body>

</html>


