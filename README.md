<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>DreamTrip AI - Explore the World</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: #f2f9ff;
      overflow-x: hidden;
    }

    header {
      background: linear-gradient(to right, #3f51b5, #00bcd4);
      color: white;
      padding: 60px 20px;
      text-align: center;
      font-size: 2.8em;
      animation: fadeInDown 1s ease-in-out;
    }

    @keyframes fadeInDown {
      0% { opacity: 0; transform: translateY(-50px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    .hero {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      padding: 40px 20px;
      background: white;
    }

    .hero input, .hero button {
      padding: 12px;
      margin: 10px;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 1em;
    }

    .hero button {
      background: #00bcd4;
      color: white;
      border: none;
      cursor: pointer;
      transition: background 0.3s;
    }

    .hero button:hover {
      background: #0097a7;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
      padding: 60px 30px;
      background: #e3f2fd;
    }

    .card {
      background: white;
      border-radius: 16px;
      padding: 25px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }

    .card:hover {
      transform: translateY(-10px);
      background: #f1f8ff;
    }

    .card h3 {
      color: #3f51b5;
    }

    .demo {
      background: #fff8e1;
      padding: 60px 30px;
      text-align: center;
      border-top: 4px solid #ffb300;
    }

    .demo pre {
      background: #263238;
      color: #fff;
      padding: 20px;
      border-radius: 10px;
      overflow-x: auto;
      max-width: 700px;
      margin: auto;
      text-align: left;
    }

    .features {
      background: #ffffff;
      padding: 60px 30px;
      text-align: center;
    }

    .features h2 {
      color: #00bcd4;
      margin-bottom: 30px;
    }

    .feature-box {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 30px;
    }

    .feature {
      flex: 1;
      min-width: 250px;
      max-width: 400px;
      background: #e0f7fa;
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
      transition: 0.3s;
    }

    .feature:hover {
      transform: scale(1.03);
      background: #b2ebf2;
    }

    footer {
      background: #3f51b5;
      color: white;
      text-align: center;
      padding: 40px 20px;
    }
  </style>
</head>
<body>

  <header>
    🌍 DreamTrip AI – Explore, Discover, Book
  </header>

  <section class="hero">
    <h2>Plan your dream vacation with the help of smart AI</h2>
    <input type="email" placeholder="Enter your email" />
    <button>Get Started</button>
  </section>

  <section class="grid">
    <div class="card">
      <h3>🌟 Tailored AI Recommendations</h3>
      <p>Get suggestions based on your budget, location, and dates.</p>
    </div>
    <div class="card">
      <h3>✈️ Real-time Deals</h3>
      <p>Never miss a deal on flights and hotels with instant alerts.</p>
    </div>
    <div class="card">
      <h3>🏝️ Secret Spots</h3>
      <p>Explore off-the-beaten-path locations curated by AI.</p>
    </div>
    <div class="card">
      <h3>📅 Full Itineraries</h3>
      <p>Let us plan each day of your trip based on your interests.</p>
    </div>
  </section>

  <section class="demo">
    <h2>🧠 Try Our AI Travel Assistant</h2>
    <p>Imagine what it can do for you:</p>
    <pre>
User: I'm planning a 5-day trip to Japan in October with my family.
AI: Awesome! I found a beautiful hotel in Tokyo, direct flight from Tel Aviv, and family activities nearby!
Total Package: $2,150 – want me to reserve it?
    </pre>
  </section>

  <section class="features">
    <h2>Why DreamTrip AI?</h2>
    <div class="feature-box">
      <div class="feature">
        <h3>🔒 Privacy First</h3>
        <p>We don’t share your data. Your travel info stays yours.</p>
      </div>
      <div class="feature">
        <h3>📲 Mobile Optimized</h3>
        <p>Access everything easily from any device – anywhere!</p>
      </div>
      <div class="feature">
        <h3>🌐 Multilingual Support</h3>
        <p>Available in English, Hebrew, French, Spanish & more.</p>
      </div>
    </div>
  </section>

  <footer>
    &copy; 2025 DreamTrip AI. Built with ❤️ for travelers by travelers.
  </footer>

</body>
</html>






