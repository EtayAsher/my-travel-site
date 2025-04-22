<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DreamTrip Planner</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }

    body {
      background: linear-gradient(to right, #eef2f3, #8e9eab);
      color: #333;
      overflow-x: hidden;
    }

    header {
      text-align: center;
      padding: 60px 20px 20px;
    }

    header h1 {
      font-size: 2.8em;
      font-weight: 700;
      color: #1a1a1a;
    }

    header p {
      font-size: 1.2em;
      color: #444;
      margin-top: 10px;
    }

    .email-box {
      max-width: 500px;
      margin: 30px auto;
      background: #fff;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    }

    .email-box h2 {
      text-align: center;
      margin-bottom: 20px;
      font-size: 1.6em;
      color: #1a1a1a;
    }

    input[type="email"] {
      width: 100%;
      padding: 15px;
      border: 1px solid #ccc;
      border-radius: 10px;
      font-size: 1em;
    }

    .features {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      margin: 60px 20px;
      gap: 40px;
    }

    .card {
      background: #fff;
      border-radius: 16px;
      padding: 25px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.1);
      width: 300px;
      transition: transform 0.3s ease;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card h3 {
      font-size: 1.4em;
      margin-bottom: 10px;
      color: #1a1a1a;
    }

    .card p {
      font-size: 1em;
      color: #555;
    }

    .testimonials {
      background: #f4f7f9;
      padding: 60px 20px;
      text-align: center;
    }

    .testimonials h2 {
      font-size: 2em;
      margin-bottom: 30px;
    }

    .testimonial {
      max-width: 600px;
      margin: 0 auto 30px;
      font-style: italic;
    }

    .footer {
      text-align: center;
      padding: 40px;
      background: #1a1a1a;
      color: white;
    }

  </style>
</head>
<body>
  <header>
    <h1>Your Personal AI Travel Assistant</h1>
    <p>Plan your dream vacation with ease, powered by smart recommendations and real-time data.</p>
  </header>

  <section class="email-box">
    <h2>Enter your email to get started</h2>
    <input type="email" placeholder="Enter your email here..." />
  </section>

  <section class="features">
    <div class="card">
      <h3>Personalized Recommendations</h3>
      <p>Tell us your preferences and our AI will generate a full trip plan tailored for you.</p>
    </div>
    <div class="card">
      <h3>Real-time Weather & Costs</h3>
      <p>Instant access to updated information about weather, attractions, and estimated budgets.</p>
    </div>
    <div class="card">
      <h3>Fast & Easy Booking</h3>
      <p>Get direct booking links to hotels, flights, and experiences that fit your plan.</p>
    </div>
  </section>

  <section class="testimonials">
    <h2>What People Are Saying</h2>
    <div class="testimonial">“This is by far the smartest way I’ve ever planned a trip. Everything was just perfect.” – Alex</div>
    <div class="testimonial">“I love how simple it is. Just a few questions and boom – vacation plan ready.” – Maria</div>
  </section>

  <div class="footer">
    &copy; 2025 DreamTrip AI. All rights reserved.
  </div>
</body>
</html>

