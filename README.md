<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Explore the World with AI</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom right, #e0f7fa, #ffffff);
      color: #333;
      overflow-x: hidden;
    }

    header {
      background: linear-gradient(to right, #00bcd4, #2196f3);
      color: white;
      padding: 40px 20px;
      text-align: center;
      font-size: 2.5em;
      animation: fadeIn 1.2s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .section {
      padding: 60px 20px;
      text-align: center;
    }

    .email-box {
      background: white;
      padding: 30px;
      border-radius: 15px;
      max-width: 500px;
      margin: 0 auto 60px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.1);
      animation: bounceIn 1s ease;
    }

    @keyframes bounceIn {
      0% { transform: scale(0.9); opacity: 0; }
      50% { transform: scale(1.05); opacity: 1; }
      100% { transform: scale(1); }
    }

    .email-box input {
      padding: 12px;
      width: 70%;
      border: 1px solid #ccc;
      border-radius: 5px;
      margin-top: 15px;
    }

    .email-box button {
      padding: 12px 25px;
      background: #00bcd4;
      color: white;
      border: none;
      border-radius: 5px;
      margin-top: 15px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .email-box button:hover {
      background: #0097a7;
    }

    .cards {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 25px;
    }

    .card {
      background: white;
      border-radius: 15px;
      padding: 25px;
      width: 300px;
      box-shadow: 0 8px 25px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }

    .card:hover {
      transform: translateY(-10px);
      background: #e1f5fe;
    }

    .card h3 {
      margin-top: 0;
      color: #00bcd4;
    }

    footer {
      background: #2196f3;
      color: white;
      padding: 30px;
      text-align: center;
      margin-top: 40px;
    }
  </style>
</head>
<body>

  <header>
    Discover Your Dream Trip with AI
  </header>

  <section class="section">
    <div class="email-box">
      <h2>Get Personalized Travel Deals</h2>
      <p>Enter your email and let AI help you plan the perfect vacation.</p>
      <input type="email" placeholder="Your Email" />
      <br>
      <button>Start Planning</button>
    </div>

    <div class="cards">
      <div class="card">
        <h3>Smart AI Planner</h3>
        <p>Answer a few questions and let our AI build the perfect vacation for you in seconds.</p>
      </div>
      <div class="card">
        <h3>Live Flight Tracking</h3>
        <p>Get updated prices and book your flights through trusted partners at the best deals.</p>
      </div>
      <div class="card">
        <h3>Hidden Destinations</h3>
        <p>Discover secret spots around the globe most travelers don't know exist.</p>
      </div>
    </div>
  </section>

  <footer>
    &copy; 2025 MyTravelAI | Built for modern explorers.
  </footer>

</body>
</html>




