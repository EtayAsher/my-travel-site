<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My Travel AI</title>
  <style>
    * {
      box-sizing: border-box;
      scroll-behavior: smooth;
    }
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #fefefe, #f0f8ff);
      color: #333;
    }
    header {
      background: linear-gradient(to right, #3b82f6, #06b6d4);
      color: white;
      padding: 60px 20px;
      text-align: center;
      font-size: 2.5em;
      font-weight: bold;
      animation: fadeIn 1.5s ease-in-out;
    }
    .email-box {
      text-align: center;
      background-color: #ffffff;
      padding: 50px 20px;
    }
    .email-box input {
      padding: 12px;
      margin: 8px;
      width: 280px;
      border: 1px solid #ccc;
      border-radius: 10px;
      font-size: 1em;
    }
    .email-box button {
      padding: 12px 30px;
      background-color: #3b82f6;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-size: 1em;
      margin-top: 10px;
      transition: 0.3s;
    }
    .email-box button:hover {
      background-color: #2563eb;
    }
    .section {
      padding: 60px 20px;
      text-align: center;
    }
    .fade-in-box {
      background-color: #e0f2fe;
      border-radius: 15px;
      padding: 30px;
      margin: 40px auto;
      max-width: 800px;
      box-shadow: 0px 8px 16px rgba(0,0,0,0.1);
      animation: fadeInUp 1s ease-in-out forwards;
      opacity: 0;
    }
    .chat-box {
      background: #f9fafb;
      border: 1px solid #ccc;
      border-radius: 12px;
      max-width: 800px;
      margin: 40px auto;
      padding: 25px;
      font-family: monospace;
      text-align: left;
    }
    .chat-box .user {
      color: #3b82f6;
      font-weight: bold;
    }
    .chat-box .ai {
      color: #16a34a;
      margin-top: 8px;
    }
    .testimonial {
      font-style: italic;
      margin-top: 15px;
    }
    .feature-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
      margin-top: 60px;
    }
    .feature {
      background-color: #fef9c3;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      transform: translateY(30px);
      opacity: 0;
      animation: popUp 1s ease forwards;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); opacity: 1; }
    }
    @keyframes popUp {
      to { transform: translateY(0); opacity: 1; }
    }

    footer {
      text-align: center;
      padding: 40px 20px;
      background-color: #f1f5f9;
      color: #666;
    }
  </style>
</head>
<body>

<header>
  🌍 Plan Your Dream Vacation with AI ✈️
</header>

<div class="email-box">
  <h2>Start Planning Instantly</h2>
  <p>Get your personal AI travel planner, tailored just for you.</p>
  <input type="email" placeholder="Enter your email" />
  <input type="password" placeholder="Create a password" />
  <br />
  <button>Let's Go</button>
</div>

<div class="section">
  <div class="fade-in-box">
    <h2>✳️ What Our Travel AI Can Do</h2>
    <p>From picking your perfect destination, to booking flights and hotels, our smart AI will guide you through it all in seconds.</p>
  </div>

  <div class="chat-box">
    <div class="user">User:</div>
    <div>I want to go to Japan in spring.</div>
    <div class="ai">AI: Great choice! 🌸 It's cherry blossom season! I found a 5-star hotel in Kyoto with a direct flight from Tel Aviv. Ready to book?</div>
  </div>

  <div class="fade-in-box">
    <h2>🌟 Testimonials</h2>
    <p class="testimonial">"Booked my entire family vacation to Italy in minutes – and saved hundreds!" – Yael M.</p>
    <p class="testimonial">"The AI gave me better suggestions than my travel agent!" – Tomer S.</p>
  </div>

  <div class="feature-grid">
    <div class="feature">🏨 Finds Best Hotels Automatically</div>
    <div class="feature">🛫 Compares Live Flight Prices</div>
    <div class="feature">📆 Builds Full Travel Itinerary</div>
    <div class="feature">🧠 Powered by Smart Travel AI</div>
    <div class="feature">🌎 Personalized by Budget & Season</div>
    <div class="feature">💬 Ask Anything. Get Smart Answers.</div>
  </div>
</div>

<footer>
  © 2025 Travel AI Co. | Your smart travel partner
</footer>

<script>
  const fadeIns = document.querySelectorAll('.fade-in-box, .feature');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) entry.target.style.animationPlayState = 'running';
    });
  }, { threshold: 0.3 });

  fadeIns.forEach(el => {
    el.style.animationPlayState = 'paused';
    observer.observe(el);
  });
</script>

</body>
</html>



