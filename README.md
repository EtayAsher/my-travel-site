<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>DreamTrip AI</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f7faff;
      color: #333;
      line-height: 1.6;
    }

    header {
      background-color: #fff;
      padding: 60px 20px 30px;
      text-align: center;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    }

    header h1 {
      font-size: 38px;
      color: #2c3e50;
    }

    header p {
      color: #555;
      margin-top: 10px;
      font-size: 18px;
    }

    .section {
      max-width: 1100px;
      margin: 60px auto;
      padding: 0 20px;
    }

    .chat-demo {
      background-color: #ffffff;
      padding: 25px;
      border-radius: 12px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.05);
    }

    .bubble {
      max-width: 85%;
      padding: 14px 18px;
      border-radius: 20px;
      margin: 10px 0;
      font-size: 16px;
      display: inline-block;
    }

    .user {
      background-color: #d9f4ff;
      float: right;
      clear: both;
    }

    .ai {
      background-color: #f2f2ff;
      float: left;
      clear: both;
    }

    .email-section {
      text-align: center;
      margin-top: 80px;
    }

    .email-box {
      background-color: #ffffff;
      padding: 30px;
      border-radius: 14px;
      display: inline-block;
      box-shadow: 0 6px 20px rgba(0,0,0,0.08);
    }

    .email-box input {
      width: 90%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 16px;
    }

    .email-box button {
      padding: 12px 25px;
      background-color: #0077ff;
      color: #fff;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    .email-box button:hover {
      background-color: #005bcc;
    }

    .feature-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
      margin-top: 60px;
    }

    .card {
      background-color: #fff;
      padding: 25px;
      border-radius: 14px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.06);
      transition: transform 0.3s ease;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .testimonial {
      background-color: #eaf4ff;
      padding: 60px 20px;
      border-radius: 16px;
      margin-top: 80px;
      text-align: center;
    }

    .testimonial h2 {
      margin-bottom: 20px;
    }

    .testimonial p {
      font-style: italic;
      color: #444;
      font-size: 17px;
    }

    .footer {
      text-align: center;
      margin: 80px 0 30px;
      color: #888;
      font-size: 14px;
    }

    .tagline {
      margin: 100px 0 30px;
      font-size: 22px;
      text-align: center;
      color: #222;
      animation: fadeIn 2s ease-in-out;
    }

    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    @media (max-width: 600px) {
      header h1 { font-size: 30px; }
      .chat-demo, .email-box { margin: 0 15px; }
    }
  </style>
</head>
<body>

  <header>
    <h1>Plan Your Dream Vacation with AI</h1>
    <p>Your personalized travel assistant – simple, fast, smart</p>
  </header>

  <div class="section chat-demo">
    <div class="bubble user"><strong>You:</strong> I want to go to Greece in July</div>
    <div class="bubble ai"><strong>AI:</strong> Sounds amazing! How about a beach resort in Santorini with a direct flight?</div>
  </div>

  <div class="section email-section">
    <div class="email-box">
      <h3>Ready to plan your trip?</h3>
      <input type="email" placeholder="Your email">
      <input type="password" placeholder="Create a password">
      <button>Start Now</button>
    </div>
  </div>

  <div class="section feature-grid">
    <div class="card">
      <h3>Ask Anything</h3>
      <p>Where to go? When? Budget? We'll give you instant suggestions.</p>
    </div>
    <div class="card">
      <h3>Find Flights</h3>
      <p>Compare and book flights directly from the AI suggestions.</p>
    </div>
    <div class="card">
      <h3>Top Hotels</h3>
      <p>We’ll recommend beautiful and affordable hotels worldwide.</p>
    </div>
    <div class="card">
      <h3>Real-time Planning</h3>
      <p>All info is updated daily so you get the most accurate offers.</p>
    </div>
  </div>

  <div class="section testimonial">
    <h2>What travelers say</h2>
    <p>“Thanks to DreamTrip AI, I found a trip to Rome in 10 minutes – including hotel and flight. The AI was like talking to a travel expert!”</p>
  </div>

  <div class="tagline">
    Start exploring. The world is waiting.
  </div>

  <div class="footer">
    &copy; 2025 DreamTrip AI | Built with ❤️ by people who love to travel
  </div>

</body>
</html>


