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
      overflow-x: hidden;
    }

    header {
      background: linear-gradient(120deg, #74ebd5, #ACB6E5);
      color: #fff;
      text-align: center;
      padding: 70px 20px 50px;
    }

    header h1 {
      font-size: 42px;
      margin-bottom: 10px;
    }

    header p {
      font-size: 20px;
    }

    .email-section {
      text-align: center;
      margin-top: 50px;
      animation: fadeIn 2s ease-in-out;
    }

    .email-box {
      background-color: #fff;
      padding: 30px;
      border-radius: 14px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.1);
      display: inline-block;
      margin-top: 20px;
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

    .section {
      max-width: 1100px;
      margin: 80px auto;
      padding: 0 20px;
    }

    .bubble-box {
      background-color: #ffffff;
      padding: 25px;
      border-radius: 14px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.1);
      max-width: 700px;
      margin: 40px auto;
      animation: slideIn 1.5s ease-in-out;
    }

    .bubble {
      max-width: 90%;
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

    .card-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
      margin-top: 80px;
    }

    .card {
      background-color: #ffffff;
      border-radius: 14px;
      padding: 25px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.06);
      transform: translateY(50px);
      opacity: 0;
      transition: all 0.8s ease;
    }

    .card.visible {
      transform: translateY(0);
      opacity: 1;
    }

    .card h3 {
      margin-bottom: 12px;
      color: #2c3e50;
    }

    .card p {
      color: #555;
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

    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    @keyframes slideIn {
      from {
        opacity: 0;
        transform: translateY(40px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 600px) {
      header h1 { font-size: 30px; }
      .email-box { width: 90%; }
    }
  </style>
</head>
<body>

  <header>
    <h1>DreamTrip AI</h1>
    <p>Your smart travel assistant. No stress, just flights & fun.</p>
  </header>

  <div class="email-section">
    <div class="email-box">
      <h3>Start planning your trip:</h3>
      <input type="email" placeholder="Your email">
      <input type="password" placeholder="Create a password">
      <button>Let’s Go!</button>
    </div>
  </div>

  <div class="section bubble-box">
    <div class="bubble user"><strong>You:</strong> I want to go to New York in summer</div>
    <div class="bubble ai"><strong>AI:</strong> Amazing! Here’s a direct flight + 3-night hotel combo in Manhattan 👇</div>
  </div>

  <div class="section card-grid">
    <div class="card"><h3>Real-time Deals</h3><p>Daily updated vacation ideas based on your preferences.</p></div>
    <div class="card"><h3>Smart Matching</h3><p>AI finds the best flight + hotel bundles for your budget.</p></div>
    <div class="card"><h3>Ask Anything</h3><p>“Where to go in winter?” The AI will surprise you.</p></div>
    <div class="card"><h3>Save Time</h3><p>No more 5 tabs open. AI does the comparison for you.</p></div>
  </div>

  <div class="testimonial">
    <h2>Traveler Feedback</h2>
    <p>“This felt like talking to a real agent. Fast, helpful, perfect results. Booked my honeymoon in 10 mins!”</p>
  </div>

  <div class="footer">
    &copy; 2025 DreamTrip AI | Powered by imagination, not robots 🤫
  </div>

  <script>
    const cards = document.querySelectorAll('.card');
    const options = {
      threshold: 0.1
    };

    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, options);

    cards.forEach(card => {
      observer.observe(card);
    });
  </script>

</body>
</html>


