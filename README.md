<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DreamTrip AI – Plan Your Perfect Vacation</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background: linear-gradient(to bottom, #ffffff, #f4f7fa);
      color: #333;
      overflow-x: hidden;
    }

    header {
      background-color: #4db8ff;
      color: white;
      padding: 40px 20px;
      text-align: center;
      animation: fadeIn 1s ease-in;
    }

    header h1 {
      font-size: 48px;
      margin-bottom: 10px;
    }

    header p {
      font-size: 18px;
    }

    .section {
      padding: 60px 20px;
      max-width: 1000px;
      margin: auto;
      text-align: center;
    }

    .section h2 {
      font-size: 36px;
      margin-bottom: 20px;
    }

    .section p {
      font-size: 18px;
      color: #555;
    }

    .email-box {
      margin-top: 30px;
    }

    input[type="email"] {
      padding: 12px;
      width: 300px;
      border: 1px solid #ccc;
      border-radius: 6px;
      margin-right: 10px;
    }

    button {
      padding: 12px 20px;
      background-color: #4db8ff;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    button:hover {
      background-color: #2c92cc;
    }

    .feature {
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
      margin-top: 50px;
    }

    .card {
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      padding: 30px;
      width: 300px;
      margin: 20px;
      text-align: left;
      animation: floatUp 1.2s ease;
    }

    .chat-box {
      background-color: #1f2d3d;
      color: white;
      padding: 20px;
      border-radius: 10px;
      text-align: left;
      font-family: monospace;
      margin-top: 40px;
    }

    .chat-box .user {
      color: #00ffbf;
    }

    .chat-box .ai {
      color: #ffd166;
    }

    footer {
      text-align: center;
      padding: 40px 20px;
      font-size: 14px;
      background: #f2f2f2;
      color: #555;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes floatUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>

<body>
  <header>
    <h1>DreamTrip AI</h1>
    <p>Your AI-powered travel planner to create your perfect vacation</p>
  </header>

  <section class="section">
    <h2>Start Planning Your Dream Trip</h2>
    <p>Tell us your destination, budget, and travel dates – we’ll handle the rest using smart AI technology.</p>
    <div class="email-box">
      <input type="email" placeholder="Enter your email..." />
      <button>Get Started</button>
    </div>
  </section>

  <section class="section">
    <h2>Why Travelers Love Us</h2>
    <div class="feature">
      <div class="card">
        <h3>Instant AI Suggestions</h3>
        <p>Get matched with destinations, hotels, and flights in seconds.</p>
      </div>
      <div class="card">
        <h3>Smart Budget Matching</h3>
        <p>Let AI find the best trip deals based on your preferences and price range.</p>
      </div>
      <div class="card">
        <h3>No Stress Planning</h3>
        <p>We take care of the research so you can enjoy your trip worry-free.</p>
      </div>
    </div>
  </section>

  <section class="section">
    <h2>Sample Chat with Our AI</h2>
    <div class="chat-box">
      <p><span class="user">You:</span> I want to go to Japan in spring.</p>
      <p><span class="ai">AI:</span> Cherry blossom season 🌸! I found a 5-star hotel in Kyoto with a direct flight from Tel Aviv. Want to book?</p>
    </div>
  </section>

  <footer>
    &copy; 2025 DreamTrip AI – All rights reserved
  </footer>
</body>
</html>





