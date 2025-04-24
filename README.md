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
      .feature-box {
        display: flex;
        align-items: center;
        gap: 2rem;
        padding: 2rem;
        border-radius: 1.5rem;
        background: white;
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.06);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        margin-bottom: 2rem;
      }
      .feature-box:hover {
        transform: translateY(-8px);
        box-shadow: 0 12px 30px rgba(0, 0, 0, 0.08);
      }
      .feature-icon {
        font-size: 3rem;
        color: #06b6d4;
        animation: bounce 2s infinite;
      }
      .feature-text h3 {
        font-size: 1.75rem;
        margin-bottom: 0.5rem;
        font-weight: 700;
      }
      .feature-text p {
        font-size: 1rem;
        color: #4b5563;
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
      @keyframes bounce {
        0%, 100% { transform: translateY(0); }
        50% { transform: translateY(-10px); }
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

      <div class="feature-box">
        <div class="feature-icon">🌍</div>
        <div class="feature-text">
          <h3>Explore Destinations</h3>
          <p>From hidden gems to iconic cities – we uncover the world's magic just for you.</p>
        </div>
      </div>

      <div class="feature-box">
        <div class="feature-icon">🤖</div>
        <div class="feature-text">
          <h3>AI Matching Engine</h3>
          <p>Advanced tech that truly *gets* you. Your dream trip starts with smart suggestions.</p>
        </div>
      </div>

      <div class="feature-box">
        <div class="feature-icon">✈️</div>
        <div class="feature-text">
          <h3>Live Flight Search</h3>
          <p>Real-time flights, best prices, no stress. Just pack your bags.</p>
        </div>
      </div>

      <div class="feature-box">
        <div class="feature-icon">🏨</div>
        <div class="feature-text">
          <h3>Hotels You’ll Love</h3>
          <p>We match your vibe to amazing stays – from luxury to cozy.</p>
        </div>
      </div>

      <div class="feature-box">
        <div class="feature-icon">🎉</div>
        <div class="feature-text">
          <h3>Fun & Adventure</h3>
          <p>Our engine matches your mood with unforgettable experiences.</p>
        </div>
      </div>

      <div class="feature-box">
        <div class="feature-icon">👨‍👩‍👧‍👦</div>
        <div class="feature-text">
          <h3>Perfect For Groups</h3>
          <p>Traveling with friends or family? We'll sync your plans seamlessly.</p>
        </div>
      </div>

    </section>

    <footer>
      <p>© 2025 Travel AI | Powered by curiosity and algorithms.</p>
    </footer>
  </body>
</html>


