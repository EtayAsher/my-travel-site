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
      .feature-box {
        display: flex;
        align-items: center;
        gap: 1.5rem;
        padding: 2rem;
        border-radius: 1.5rem;
        background: white;
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.06);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        margin-bottom: 2rem;
        flex-wrap: wrap;
      }
      .feature-icon {
        font-size: 2.5rem;
        color: #06b6d4;
        animation: bounce 2s infinite;
        flex-shrink: 0;
      }
      .feature-text h3 {
        font-size: 1.5rem;
        margin-bottom: 0.5rem;
        font-weight: 700;
      }
      .feature-text p {
        font-size: 1rem;
        color: #4b5563;
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
      .chat-demo-floating {
        position: relative;
        background: white;
        border-radius: 1rem;
        box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
        padding: 1rem;
        width: 100%;
        max-width: 350px;
        margin: 4rem auto 0;
        animation: fadeIn 1.2s ease-in-out;
      }
      .chat-demo-floating h4 {
        text-align: center;
        font-size: 1.1rem;
        margin-bottom: 0.5rem;
      }
      .chat-bubble {
        padding: 0.75rem 1rem;
        border-radius: 1rem;
        margin-bottom: 0.5rem;
        font-size: 0.9rem;
        line-height: 1.4;
        max-width: 90%;
      }
      .user-msg {
        background: #e0f2fe;
        align-self: flex-end;
        margin-left: auto;
      }
      .bot-msg {
        background: #fef9c3;
        align-self: flex-start;
        margin-right: auto;
      }
      .chat-container {
        display: flex;
        flex-direction: column;
      }
      footer {
        background: #1f2937;
        color: white;
        padding: 3rem 2rem;
        text-align: center;
      }
      @keyframes fadeIn {
        from { opacity: 0; transform: translateY(-10px); }
        to { opacity: 1; transform: translateY(0); }
      }
      @keyframes bounce {
        0%, 100% { transform: translateY(0); }
        50% { transform: translateY(-10px); }
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
          <p>Advanced tech that truly gets you. Your dream trip starts with smart suggestions.</p>
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

      <div class="chat-demo-floating">
        <h4>Chat with Travel AI ✨</h4>
        <div class="chat-container">
          <div class="chat-bubble user-msg">I want to go on a beach trip this summer!</div>
          <div class="chat-bubble bot-msg">Great! How about the Amalfi Coast or the Greek Islands?</div>
          <div class="chat-bubble user-msg">Can you help with hotel options too?</div>
          <div class="chat-bubble bot-msg">Absolutely! I'm checking the best beachfront hotels now. 🏖️</div>
        </div>
      </div>

    </section>

    <footer>
      <p>© 2025 Travel AI | Powered by curiosity and algorithms.</p>
    </footer>
  </body>
</html>



