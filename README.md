<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dream Travel AI</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      scroll-behavior: smooth;
    }

    body {
      background: linear-gradient(to bottom, #fefefe, #e0f7fa);
      color: #333;
      line-height: 1.6;
      overflow-x: hidden;
    }

    header {
      background: linear-gradient(to right, #2196f3, #00bcd4);
      color: white;
      padding: 60px 20px;
      text-align: center;
      animation: fadeIn 2s ease;
    }

    header h1 {
      font-size: 3rem;
      margin-bottom: 10px;
    }

    section {
      padding: 60px 20px;
      text-align: center;
      animation: fadeInUp 1s ease forwards;
      opacity: 0;
    }

    section.visible {
      opacity: 1;
    }

    .features {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 30px;
      margin-top: 30px;
    }

    .card {
      background: white;
      border-radius: 12px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.1);
      padding: 25px;
      width: 280px;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 12px 24px rgba(0,0,0,0.15);
    }

    .chat-demo {
      background: #263238;
      color: #cfd8dc;
      padding: 25px;
      border-radius: 8px;
      width: 85%;
      max-width: 700px;
      margin: 0 auto;
      font-family: monospace;
      font-size: 1rem;
    }

    .testimonials {
      background: #f9f9f9;
    }

    .testimonial-card {
      background: #ffffff;
      margin: 25px auto;
      padding: 20px;
      border-left: 5px solid #009688;
      width: 70%;
      max-width: 500px;
      border-radius: 10px;
      box-shadow: 0 6px 12px rgba(0,0,0,0.05);
    }

    .cta {
      background: #00796b;
      color: white;
    }

    .cta form {
      margin-top: 20px;
    }

    .cta input {
      padding: 12px;
      width: 260px;
      border-radius: 6px;
      border: none;
      margin-right: 10px;
    }

    .cta button {
      padding: 12px 24px;
      border: none;
      background: #004d40;
      color: white;
      border-radius: 6px;
      cursor: pointer;
    }

    footer {
      background: #004d40;
      color: white;
      padding: 25px;
      text-align: center;
      font-size: 0.9rem;
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(40px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
      }
      to {
        opacity: 1;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>🌍 Dream Travel Planner</h1>
    <p>Your perfect vacation starts here, powered by AI.</p>
  </header>

  <section id="features" class="feature-section">
    <h2>🚀 Why People Love Us</h2>
    <div class="features">
      <div class="card">🌐 AI Travel Agent Available 24/7</div>
      <div class="card">💸 Find The Best Deals Instantly</div>
      <div class="card">✈️ Explore Hidden Destinations</div>
    </div>
  </section>

  <section id="ai-demo">
    <h2>🤖 Sample Chat with Our Travel AI</h2>
    <div class="chat-demo">
      <p><strong>User:</strong> I want to go to Japan in spring.</p>
      <p><strong>AI:</strong> Cherry blossom season! I found a 5-star hotel in Kyoto with a direct flight from Tel Aviv. Want to book now?</p>
    </div>
  </section>

  <section class="testimonials">
    <h2>💬 Real Stories</h2>
    <div class="testimonial-card">
      “Used this site to plan my honeymoon to Thailand. Insanely easy.” <br><span>- Avi L.</span>
    </div>
    <div class="testimonial-card">
      “Their AI literally saved me $600 on hotels!”<br><span>- Shira G.</span>
    </div>
    <div class="testimonial-card">
      “Never thought travel planning could be this fast.”<br><span>- Yossi T.</span>
    </div>
  </section>

  <section class="cta">
    <h2>📩 Ready to plan your trip?</h2>
    <form>
      <input type="email" placeholder="Enter your email" required />
      <button type="submit">Start Planning</button>
    </form>
  </section>

  <footer>
    <p>🚀 Powered by Etay's AI Travel Co. | All rights reserved © 2025</p>
  </footer>

  <script>
    // Reveal sections on scroll
    const sections = document.querySelectorAll("section");

    window.addEventListener("scroll", () => {
      const trigger = window.innerHeight * 0.85;
      sections.forEach(section => {
        const top = section.getBoundingClientRect().top;
        if (top < trigger) {
          section.classList.add("visible");
        }
      });
    });
  </script>
</body>
</html>



