<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DreamTrip AI</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: linear-gradient(135deg, #00c6ff, #0072ff);
      color: white;
      overflow-x: hidden;
    }

    header {
      text-align: center;
      padding: 3rem 1rem 2rem;
      animation: slideFade 1s ease-out;
    }

    header h1 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }

    header p {
      font-size: 1.2rem;
      color: #f0f0f0;
    }

    .email-box {
      background: white;
      padding: 1.5rem;
      border-radius: 20px;
      max-width: 400px;
      margin: 2rem auto;
      text-align: center;
      box-shadow: 0 0 20px rgba(0,0,0,0.1);
      animation: popUp 1s ease-out;
    }

    .email-box h2 {
      color: #0072ff;
      margin-bottom: 1rem;
    }

    input[type="email"] {
      padding: 0.6rem;
      border: none;
      border-radius: 10px;
      width: 80%;
      margin-bottom: 1rem;
    }

    button {
      padding: 0.6rem 1.2rem;
      border: none;
      background: #0072ff;
      color: white;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #005dd1;
    }

    .features {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      padding: 3rem 1rem;
      gap: 2rem;
    }

    .card {
      background: white;
      color: #333;
      padding: 2rem;
      border-radius: 20px;
      max-width: 300px;
      text-align: center;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }

    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
    }

    .card h3 {
      margin-bottom: 1rem;
    }

    .card p {
      font-size: 0.95rem;
    }

    .section-title {
      text-align: center;
      margin-top: 4rem;
      font-size: 2rem;
      color: #fff;
      text-shadow: 2px 2px #000;
    }

    .animation-container {
      margin-top: 3rem;
      text-align: center;
      font-size: 1.4rem;
      animation: float 3s infinite ease-in-out;
    }

    .footer {
      text-align: center;
      padding: 2rem;
      background: rgba(0,0,0,0.3);
      font-size: 0.9rem;
      margin-top: 3rem;
    }

    @keyframes popUp {
      from {
        transform: scale(0.9);
        opacity: 0;
      }
      to {
        transform: scale(1);
        opacity: 1;
      }
    }

    @keyframes slideFade {
      from {
        transform: translateY(-30px);
        opacity: 0;
      }
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
    }
  </style>
</head>

<body>
  <header>
    <h1>Plan Your Dream Vacation</h1>
    <p>With the power of AI, your perfect trip is just a few clicks away.</p>
  </header>

  <section class="email-box">
    <h2>Get Started</h2>
    <input type="email" placeholder="Enter your email" />
    <br />
    <button>Start Planning</button>
  </section>

  <h2 class="section-title">Why Choose Us?</h2>
  <section class="features">
    <div class="card">
      <h3>Personalized Trips</h3>
      <p>We use smart AI to tailor your vacation to your taste, budget, and dream destinations.</p>
    </div>
    <div class="card">
      <h3>Instant Booking</h3>
      <p>Get real-time hotel & flight options based on your preferences. No more endless searching.</p>
    </div>
    <div class="card">
      <h3>One-Click Planning</h3>
      <p>Tell us what you want, and we do the rest. Easy, simple, and stress-free.</p>
    </div>
  </section>

  <div class="animation-container">
    ✈️ 🌍 Explore the World With Just One Click! 🏖️ 🗺️
  </div>

  <footer class="footer">
    &copy; 2025 DreamTrip AI. All rights reserved.
  </footer>
</body>

</html>


