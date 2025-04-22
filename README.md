<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DreamTrip Planner</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #f2f2f2;
      color: #333;
    }

    header {
      background-color: #000;
      color: white;
      padding: 40px 20px;
      text-align: center;
    }

    header h1 {
      font-size: 2.5em;
      margin: 0;
    }

    .email-box {
      margin: 30px auto;
      max-width: 400px;
      background-color: #ffffff;
      padding: 25px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 10px;
      text-align: center;
    }

    .email-box input[type=email],
    .email-box input[type=password] {
      padding: 12px;
      width: 80%;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    .email-box button {
      padding: 12px 20px;
      background-color: #28a745;
      border: none;
      color: white;
      font-weight: bold;
      cursor: pointer;
      border-radius: 5px;
    }

    .section {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin: 60px auto;
      max-width: 900px;
      padding: 20px;
      background-color: white;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }

    .section:nth-child(even) {
      flex-direction: row-reverse;
    }

    .section-text {
      flex: 1;
      padding: 20px;
    }

    .section-text h2 {
      margin-top: 0;
    }

    .section-icon {
      font-size: 60px;
      padding: 20px;
      color: #3498db;
    }

    footer {
      text-align: center;
      padding: 30px;
      background-color: #222;
      color: white;
    }
  </style>
</head>
<body>
  <header>
    <h1>Plan Your Dream Vacation with AI</h1>
    <p>Smart recommendations. Real results.</p>
  </header>

  <div class="email-box">
    <h2>Start Planning Now</h2>
    <input type="email" placeholder="Enter your email" />
    <br />
    <input type="password" placeholder="Create a password" />
    <br />
    <button>Register</button>
  </div>

  <div class="section">
    <div class="section-icon">🤖</div>
    <div class="section-text">
      <h2>Smart AI Assistant</h2>
      <p>Just tell us where and when — our AI does the rest. Weather, budget, and vibes? We’ve got it all figured out for you.</p>
    </div>
  </div>

  <div class="section">
    <div class="section-icon">🌍</div>
    <div class="section-text">
      <h2>Worldwide Destinations</h2>
      <p>Paris? Tokyo? Cape Town? Wherever you want to go, we can help you make it happen – with the best prices and packages.</p>
    </div>
  </div>

  <div class="section">
    <div class="section-icon">📆</div>
    <div class="section-text">
      <h2>Perfect Timing</h2>
      <p>Our system checks the seasons, local events and weather trends to recommend the perfect time to fly.</p>
    </div>
  </div>

  <footer>
    &copy; 2025 DreamTrip | Designed for travelers by travelers ❤️
  </footer>
</body>
</html>
