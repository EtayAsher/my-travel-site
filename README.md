<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Travel Site</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Montserrat', sans-serif;
      background-color: #ffffff;
      overflow-x: hidden;
    }

    header {
      text-align: center;
      padding: 4rem 1rem 2rem;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      color: #fff;
      animation: fadeIn 1s ease-in;
    }

    header h1 {
      font-size: 3rem;
      margin-bottom: 0.5rem;
    }

    header p {
      font-size: 1.2rem;
    }

    .email-signup {
      display: flex;
      justify-content: center;
      margin-top: 2rem;
      flex-wrap: wrap;
    }

    .email-signup input {
      padding: 1rem;
      font-size: 1rem;
      border: 2px solid #ff6f61;
      border-radius: 8px 0 0 8px;
      outline: none;
      width: 300px;
    }

    .email-signup button {
      padding: 1rem 2rem;
      font-size: 1rem;
      border: none;
      background-color: #ff6f61;
      color: white;
      border-radius: 0 8px 8px 0;
      cursor: pointer;
    }

    .features {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      margin: 4rem 2rem;
      gap: 2rem;
      animation: fadeIn 2s ease-in;
    }

    .feature-box {
      background: #f7f7f7;
      border-radius: 20px;
      padding: 2rem;
      width: 300px;
      text-align: center;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }

    .feature-box:hover {
      transform: scale(1.05);
    }

    .feature-box h3 {
      color: #ff6f61;
    }

    .cities-section {
      background: linear-gradient(to right, #ffecd2, #fcb69f);
      padding: 4rem 1rem;
      animation: slideIn 1s ease-in-out;
    }

    .cities-section h2 {
      text-align: center;
      margin-bottom: 2rem;
    }

    .city-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.5rem;
      padding: 0 2rem;
    }

    .city-card {
      background: white;
      padding: 1rem;
      border-radius: 15px;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
      text-align: center;
    }

    .city-card h4 {
      margin-bottom: 0.5rem;
    }

    .footer {
      text-align: center;
      padding: 2rem;
      background: #222;
      color: white;
      font-size: 0.9rem;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes slideIn {
      from { transform: translateY(50px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
  </style>
</head>

<body>
  <header>
    <h1>Plan Your Dream Vacation</h1>
    <p>AI-powered travel suggestions tailored just for you</p>
    <div class="email-signup">
      <input type="email" placeholder="Enter your email" />
      <button>Get Started</button>
    </div>
  </header>

  <section class="features">
    <div class="feature-box">
      <h3>🌍 Smart AI Planning</h3>
      <p>Get personalized travel recommendations based on your preferences.</p>
    </div>
    <div class="feature-box">
      <h3>✈️ Real-Time Flights</h3>
      <p>See updated flight deals for your chosen destinations.</p>
    </div>
    <div class="feature-box">
      <h3>🏨 Hotels & Packages</h3>
      <p>Get matched with hotels that fit your budget and style.</p>
    </div>
    <div class="feature-box">
      <h3>🎯 Save Time</h3>
      <p>Let our AI do the search. You enjoy the trip.</p>
    </div>
  </section>

  <section class="cities-section">
    <h2>Popular Destinations</h2>
    <div class="city-grid">
      <div class="city-card">
        <h4>New York</h4>
        <p>The city that never sleeps. Explore culture, shopping, and nightlife.</p>
      </div>
      <div class="city-card">
        <h4>Paris</h4>
        <p>Romantic getaways, art, and unforgettable food.</p>
      </div>
      <div class="city-card">
        <h4>Tokyo</h4>
        <p>Modern meets tradition. Discover a unique travel experience.</p>
      </div>
      <div class="city-card">
        <h4>Rome</h4>
        <p>History, architecture, and Italian charm everywhere you go.</p>
      </div>
    </div>
  </section>

  <footer class="footer">
    &copy; 2025 My Travel Site | Powered by AI & Passion for Travel ✈️🌍
  </footer>
</body>

</html>



