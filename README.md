<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Smart Travel AI</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }
    body {
      background-color: #ffffff;
      color: #333;
      overflow-x: hidden;
    }
    header {
      padding: 2rem;
      text-align: center;
      background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
      color: white;
      animation: fadeIn 2s ease-in-out;
    }
    header h1 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }
    header p {
      font-size: 1.2rem;
    }
    .email-box {
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 2rem;
    }
    .email-box input {
      padding: 1rem;
      font-size: 1rem;
      width: 250px;
      border: 2px solid #0f2027;
      border-radius: 10px 0 0 10px;
      outline: none;
    }
    .email-box button {
      padding: 1rem;
      font-size: 1rem;
      border: none;
      background-color: #0f2027;
      color: white;
      border-radius: 0 10px 10px 0;
      cursor: pointer;
      transition: 0.3s;
    }
    .email-box button:hover {
      background-color: #2c5364;
    }
    section {
      padding: 3rem 2rem;
      max-width: 1000px;
      margin: auto;
    }
    .card {
      background-color: #f9f9f9;
      border-radius: 15px;
      padding: 2rem;
      margin: 1rem 0;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      animation: slideUp 1s ease;
    }
    .card h2 {
      margin-bottom: 1rem;
      color: #0f2027;
    }
    .chat-demo {
      background-color: #e3f2fd;
      padding: 1.5rem;
      border-radius: 15px;
      margin-top: 2rem;
      animation: fadeIn 1.5s ease;
    }
    .bubble {
      background-color: #d1ecf1;
      padding: 1rem;
      margin: 0.5rem 0;
      border-radius: 10px;
      width: fit-content;
      max-width: 80%;
    }
    .bubble.user {
      background-color: #c3e6cb;
      align-self: flex-end;
      margin-left: auto;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes slideUp {
      from { transform: translateY(50px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
    @media (max-width: 600px) {
      header h1 {
        font-size: 2rem;
      }
      .email-box {
        flex-direction: column;
      }
      .email-box input,
      .email-box button {
        border-radius: 10px;
        width: 80%;
        margin: 0.3rem 0;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Smart Travel AI</h1>
    <p>Plan your dream vacation in seconds with our smart travel assistant</p>
  </header>
  <div class="email-box">
    <input type="email" placeholder="Enter your email...">
    <button>Join Now</button>
  </div>
  <section>
    <div class="card">
      <h2>What is Smart Travel AI?</h2>
      <p>Smart Travel AI helps you discover amazing destinations, flights, hotels, and experiences based on your preferences. Simply chat with our AI assistant and get personalized recommendations instantly!</p>
    </div>
    <div class="card">
      <h2>Example Conversation</h2>
      <div class="chat-demo">
        <div class="bubble user">"I want to travel to Paris this summer with a medium budget."</div>
        <div class="bubble bot">"Great! The weather in Paris in the summer is usually warm and pleasant. Here are some 4-star hotels and affordable flights departing from your location."
        </div>
      </div>
    </div>
    <div class="card">
      <h2>Top Destinations</h2>
      <p>New York, Tokyo, Miami, London, Berlin, Dubai, Venice, Sydney, Cairo, Cape Town – wherever you dream of going, we’ve got you covered.</p>
    </div>
    <div class="card">
      <h2>Why Choose Us?</h2>
      <ul>
        <li>Personalized AI-powered travel planning</li>
        <li>Fast, fun, and easy-to-use interface</li>
        <li>Tailored suggestions for your needs</li>
        <li>All in one place – hotels, flights, and experiences</li>
      </ul>
    </div>
  </section>
</body>
</html>



