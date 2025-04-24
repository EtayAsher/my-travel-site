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
        background: linear-gradient(180deg, #dbeafe, #fdf2f8);
        color: #1f2937;
        line-height: 1.6;
        overflow-x: hidden;
      }
      .banner-popup {
        position: fixed;
        top: 20px;
        right: 20px;
        background-color: #3b82f6;
        color: white;
        padding: 1rem 1.5rem;
        border-radius: 0.75rem;
        box-shadow: 0 8px 16px rgba(0,0,0,0.1);
        font-size: 0.95rem;
        z-index: 1000;
        animation: fadeIn 1s ease-in-out;
        display: flex;
        align-items: center;
        gap: 0.75rem;
        transition: opacity 0.6s ease, transform 0.6s ease;
      }
      .banner-popup.hide {
        opacity: 0;
        transform: translateY(-20px);
      }
      .banner-popup button {
        background: none;
        border: none;
        color: white;
        font-size: 1rem;
        cursor: pointer;
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
        font-size: 2.5rem;
        font-weight: 800;
        margin-bottom: 1rem;
      }
      .hero p {
        font-size: 1.2rem;
        margin-bottom: 2rem;
      }
      .email-box {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1rem;
        margin-top: 1rem;
      }
      .email-box input,
      .email-box button {
        padding: 1rem;
        font-size: 1rem;
        border: none;
        border-radius: 0.5rem;
        width: 100%;
        max-width: 350px;
      }
      .email-box button {
        background: #1f2937;
        color: white;
        cursor: pointer;
        transition: background 0.3s ease;
      }
      .email-box button:hover {
        background: #374151;
      }
      .main-section {
        padding: 5rem 2rem;
        max-width: 1200px;
        margin: auto;
      }
      .ai-expert-box {
        background: #fef3c7;
        padding: 2rem;
        border-radius: 1.5rem;
        box-shadow: 0 8px 20px rgba(0,0,0,0.05);
        margin-bottom: 3rem;
        text-align: center;
        max-width: 800px;
        margin-left: auto;
        margin-right: auto;
      }
      .ai-expert-box h3 {
        font-size: 1.75rem;
        margin-bottom: 1rem;
      }
      .ai-expert-box p {
        font-size: 1.1rem;
        color: #444;
      }
    </style>
    <script>
      window.onload = function() {
        setTimeout(function() {
          const popup = document.getElementById('popup');
          if (popup) popup.classList.add('hide');
        }, 7000);
      };
      function closePopup() {
        const popup = document.getElementById('popup');
        if (popup) popup.classList.add('hide');
      }
    </script>
  </head>
  <body>
    <div class="banner-popup" id="popup">
      <span>Smart digital travel advisor powered by AI – get personalized recommendations!</span>
      <button onclick="closePopup()">✕</button>
    </div>

    <section class="main-section">
      <div class="hero">
        <h2>Let AI Plan Your Perfect Vacation</h2>
        <p>Tailored travel plans, real-time bookings, stunning destinations.</p>
        <div class="email-box">
          <input type="email" placeholder="Enter your email" />
          <button>Get Started</button>
        </div>
      </div>

      <div class="ai-expert-box">
        <h3>What Makes Us Different?</h3>
        <p>
          Our bot doesn’t just sound smart – it’s built to specialize in tourism. Powered by AI, it simulates a conversation with a digital advisor trained specifically to help with vacations, flights, and hotels. Everything is designed with you in mind – smart, friendly, and free of overwhelm.
        </p>
      </div>
    </section>

    <footer>
      <p>© 2025 Travel AI | Powered by curiosity and algorithms.</p>
    </footer>
  </body>
</html>


