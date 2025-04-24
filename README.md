<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Travel AI</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }
      body {
        font-family: 'Inter', sans-serif;
        background: #f9fafb;
        color: #1f2937;
        line-height: 1.6;
        overflow-x: hidden;
      }
      header {
        background: white;
        padding: 1.5rem 2rem;
        display: none;
      }
      .main-section {
        padding: 5rem 2rem;
        max-width: 1200px;
        margin: auto;
      }
      .hero {
        text-align: center;
        padding: 8rem 2rem;
        background: linear-gradient(120deg, #3b82f6, #06b6d4);
        color: white;
        border-radius: 2rem;
        margin-bottom: 5rem;
        animation: fadeIn 2s ease-in-out;
      }
      .hero h2 {
        font-size: 3rem;
        font-weight: 800;
        margin-bottom: 1rem;
      }
      .hero p {
        font-size: 1.25rem;
        margin-bottom: 2rem;
      }
      .email-box {
        display: flex;
        justify-content: center;
        gap: 1rem;
        margin-top: 1rem;
      }
      .email-box input {
        padding: 1rem;
        font-size: 1rem;
        border: none;
        border-radius: 0.5rem;
        width: 300px;
      }
      .email-box button {
        padding: 1rem 2rem;
        font-size: 1rem;
        background: #1f2937;
        color: white;
        border: none;
        border-radius: 0.5rem;
        cursor: pointer;
        transition: background 0.3s ease;
      }
      .email-box button:hover {
        background: #374151;
      }
      .section {
        margin-bottom: 6rem;
        opacity: 0;
        transform: translateY(50px);
        animation: fadeUp 1s ease-in-out forwards;
      }
      .section:nth-child(odd) {
        animation-delay: 0.2s;
      }
      .section:nth-child(even) {
        animation-delay: 0.5s;
      }
      .section h3 {
        font-size: 2rem;
        font-weight: 600;
        margin-bottom: 1rem;
      }
      .section p {
        max-width: 800px;
        margin-bottom: 1rem;
      }
      .grid {
        display: grid;
        gap: 2rem;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      }
      .card {
        background: white;
        padding: 2rem;
        border-radius: 1rem;
        box-shadow: 0 4px 12px rgba(0,0,0,0.06);
        transition: transform 0.3s ease;
      }
      .card:hover {
        transform: translateY(-5px);
      }
      footer {
        background: #1f2937;
        color: white;
        padding: 3rem 2rem;
        text-align: center;
      }
      @keyframes fadeUp {
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }
      @keyframes fadeIn {
        from { opacity: 0; transform: scale(0.95); }
        to { opacity: 1; transform: scale(1); }
      }
    </style>
  </head>
  <body>
    <section class="main-section">
      <div class="hero">
        <h2>Let AI Plan Your Perfect Vacation</h2>
        <p>Tailored travel plans, real-time bookings, stunning destinations.</p>
        <div class="email-box">
          <input type="email" placeholder="Enter your email" />
          <button>Get Started</button>
        </div>
      </div>

      <!-- Fake long content for scroll -->
      <div class="section">
        <h3>Explore Destinations</h3>
        <p>From the streets of Rome to the beaches of Bali, find the best places matched to your vibes.</p>
      </div>

      <div class="section">
        <h3>AI Matching Engine</h3>
        <p>We use advanced algorithms to recommend the perfect trip based on your preferences.</p>
      </div>

      <div class="section">
        <h3>Live Flight Search</h3>
        <p>Instant access to real-time flight data and booking options, updated continuously.</p>
      </div>

      <div class="section">
        <h3>Hotels You’ll Love</h3>
        <p>Our AI suggests top-rated accommodations based on your travel style.</p>
      </div>

      <div class="section">
        <h3>Activities Engine</h3>
        <p>Whether it's surfing in Portugal or skiing in the Alps, we match the fun to your soul.</p>
      </div>

      <div class="section">
        <h3>Group Travel Made Easy</h3>
        <p>Planning with friends or family? We’ll create synced itineraries in seconds.</p>
      </div>

      <div class="section">
        <h3>Why Us?</h3>
        <p>We're not just another travel website. We're your digital travel agent – smarter, faster, friendlier.</p>
      </div>
    </section>

    <footer>
      <p>© 2025 Travel AI | Powered by curiosity and algorithms.</p>
    </footer>
  </body>
</html>

