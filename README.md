<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>DreamTrip AI</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    /* Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background: linear-gradient(to bottom, #ffffff, #f5f5f5);
      overflow-x: hidden;
    }

    header {
      background: #4bb5ff;
      color: white;
      text-align: center;
      padding: 40px 20px;
      animation: slideIn 1s ease-out;
    }

    header h1 {
      font-size: 48px;
    }

    header p {
      font-size: 20px;
      margin-top: 10px;
    }

    .section {
      padding: 60px 20px;
      text-align: center;
    }

    .card {
      background: white;
      border-radius: 10px;
      padding: 30px;
      margin: 30px auto;
      width: 90%;
      max-width: 800px;
      box-shadow: 0 0 20px rgba(0,0,0,0.1);
      animation: fadeIn 1.5s ease;
      transition: transform 0.3s ease;
    }

    .card:hover {
      transform: scale(1.03);
    }

    .chat-preview {
      background: #f1f1f1;
      border-radius: 10px;
      padding: 20px;
      margin-top: 20px;
      text-align: left;
      font-size: 16px;
      box-shadow: inset 0 0 10px rgba(0,0,0,0.05);
    }

    .chat-preview .user {
      color: #007BFF;
      font-weight: bold;
    }

    .chat-preview .bot {
      color: #28a745;
      font-weight: bold;
    }

    .testimonial {
      background: #fff9e6;
      padding: 25px;
      border-radius: 10px;
      margin: 20px auto;
      width: 80%;
      max-width: 700px;
      font-style: italic;
      box-shadow: 0 0 10px rgba(0,0,0,0.05);
    }

    footer {
      background: #333;
      color: white;
      text-align: center;
      padding: 30px 10px;
      margin-top: 50px;
    }

    @keyframes slideIn {
      from { transform: translateY(-100%); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>

  <header>
    <h1>🌍 DreamTrip AI</h1>
    <p>Your personal travel planner powered by smart AI</p>
  </header>

  <div class="section">
    <div class="card">
      <h2>Start Your Dream Vacation</h2>
      <p>Get personalized suggestions based on your budget, destination, and preferences.</p>
      <input type="email" placeholder="Enter your email..." style="padding: 10px; margin-top: 20px; width: 60%; border-radius: 5px; border: 1px solid #ccc;">
    </div>

    <div class="card">
      <h2>How it Works</h2>
      <div class="chat-preview">
        <p><span class="user">You:</span> I want a sunny beach vacation in August with a mid-range budget.</p>
        <p><span class="bot">DreamTrip AI:</span> Perfect! 🌞 How about Costa del Sol, Spain? Here’s a package with flight + hotel for 5 nights under $900.</p>
      </div>
    </div>

    <div class="card">
      <h2>Why Travelers ❤️ Us</h2>
      <div class="testimonial">“I found my honeymoon in Santorini for half the price. The AI saved us hours of research!” – Sarah G.</div>
      <div class="testimonial">“Best trip planner I’ve ever used. I was matched with a 4-star hotel in Rome in seconds.” – Daniel K.</div>
    </div>
  </div>

  <footer>
    &copy; 2025 DreamTrip AI | All rights reserved
  </footer>

</body>
</html>



