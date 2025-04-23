<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DreamTrip AI</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background: linear-gradient(to bottom, #ffffff, #e6f0ff);
      color: #333;
      overflow-x: hidden;
    }

    header {
      background: #4bb5ff;
      color: white;
      text-align: center;
      padding: 40px 20px;
      animation: fadeIn 1s ease-in-out;
    }

    header h1 {
      font-size: 2.5rem;
    }

    .section {
      padding: 60px 20px;
      text-align: center;
    }

    .email-box {
      background: white;
      margin: 0 auto;
      max-width: 500px;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
      margin-bottom: 60px;
    }

    .email-box input {
      width: 80%;
      padding: 12px;
      margin-top: 15px;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .section-title {
      font-size: 2rem;
      margin-bottom: 20px;
    }

    .feature {
      margin: 20px auto;
      max-width: 800px;
      padding: 20px;
      background: #f9f9f9;
      border-left: 6px solid #4bb5ff;
      animation: slideIn 0.5s ease forwards;
      transition: transform 0.3s;
    }

    .feature:hover {
      transform: scale(1.02);
    }

    .chat-demo {
      margin: 50px auto;
      max-width: 700px;
      background: #222;
      color: white;
      border-radius: 15px;
      padding: 20px;
      font-family: monospace;
      animation: fadeInUp 1s ease;
    }

    .chat-demo p span {
      font-weight: bold;
      color: #4bb5ff;
    }

    footer {
      background: #f2f2f2;
      padding: 40px;
      text-align: center;
      font-size: 0.9rem;
    }

    /* אנימציות */
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes slideIn {
      from { transform: translateX(-100%); opacity: 0; }
      to { transform: translateX(0); opacity: 1; }
    }

    @keyframes fadeInUp {
      from { transform: translateY(20px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
  </style>
</head>
<body>

  <header>
    <h1>🌍 DreamTrip AI</h1>
    <p>Your smart travel planner powered by AI</p>
  </header>

  <div class="section">
    <div class="email-box">
      <h2>Start Planning Your Trip</h2>
      <p>Enter your email to get personalized vacation offers</p>
      <input type="email" placeholder="Your email..." />
    </div>

    <div class="section-title">🌟 Why Choose DreamTrip AI?</div>

    <div class="feature">🚀 Get trip suggestions instantly based on your budget, dates, and style!</div>
    <div class="feature">🌴 Discover hidden destinations that match your interests</div>
    <div class="feature">✈️ Save time and money using our AI-based planning system</div>
  </div>

  <div class="section">
    <div class="section-title">🤖 Sample Chat with DreamTrip AI</div>
    <div class="chat-demo">
      <p><span>User:</span> I want to go to Japan in spring.</p>
      <p><span>AI:</span> Great choice! I found a 5-star hotel in Kyoto with flights for only $1,750. Want to reserve?</p>
    </div>
  </div>

  <footer>
    &copy; 2025 DreamTrip AI. All rights reserved.
  </footer>

</body>
</html>



