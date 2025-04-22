<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Smart Travel Planner</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
      body {
        font-family: 'Poppins', sans-serif;
        background-color: #ffffff;
        color: #111827;
      }

      .section {
        padding: 4rem 2rem;
      }

      .glow {
        box-shadow: 0 0 20px rgba(0, 123, 255, 0.5);
      }

      .fade-in {
        animation: fadeIn 2s ease-in;
      }

      @keyframes fadeIn {
        0% { opacity: 0; transform: translateY(20px); }
        100% { opacity: 1; transform: translateY(0); }
      }

      @media (max-width: 768px) {
        .responsive-padding {
          padding: 2rem 1rem;
        }
      }
    </style>
  </head>

  <body class="bg-white text-gray-900">
    <!-- Hero section -->
    <section class="text-center section fade-in">
      <h1 class="text-4xl font-bold mb-4 text-blue-600">Plan Your Dream Trip with AI</h1>
      <p class="text-lg mb-6">Let our smart AI bot help you find the perfect vacation — fast, simple, and personalized!</p>
      <div class="max-w-md mx-auto bg-white p-6 rounded-2xl shadow-xl glow">
        <input type="email" placeholder="Enter your email" class="w-full px-4 py-2 border border-gray-300 rounded-lg mb-4" />
        <button class="w-full bg-blue-600 text-white py-2 rounded-lg hover:bg-blue-700 transition">Join Now</button>
      </div>
    </section>

    <!-- How it works -->
    <section class="section bg-gray-100 text-center fade-in">
      <h2 class="text-3xl font-semibold mb-4">How Does It Work?</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-6xl mx-auto mt-6">
        <div class="p-4 bg-white rounded-xl shadow-md hover:shadow-lg transition">
          <h3 class="font-bold text-xl mb-2 text-blue-500">Step 1</h3>
          <p>Tell the AI where and when you want to travel</p>
        </div>
        <div class="p-4 bg-white rounded-xl shadow-md hover:shadow-lg transition">
          <h3 class="font-bold text-xl mb-2 text-blue-500">Step 2</h3>
          <p>Get personalized offers and travel tips</p>
        </div>
        <div class="p-4 bg-white rounded-xl shadow-md hover:shadow-lg transition">
          <h3 class="font-bold text-xl mb-2 text-blue-500">Step 3</h3>
          <p>Book your vacation directly from the recommendations</p>
        </div>
      </div>
    </section>

    <!-- Features -->
    <section class="section text-center fade-in">
      <h2 class="text-3xl font-semibold mb-4">Why Choose Us?</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-6xl mx-auto mt-6">
        <div class="bg-blue-100 p-6 rounded-xl shadow-md">
          <h3 class="text-xl font-bold mb-2">Smart AI Bot</h3>
          <p>Our AI understands your needs and finds the best options tailored to your preferences.</p>
        </div>
        <div class="bg-blue-100 p-6 rounded-xl shadow-md">
          <h3 class="text-xl font-bold mb-2">Fast & Easy</h3>
          <p>No more endless searching. Get everything in one place — fast, easy, and reliable.</p>
        </div>
      </div>
    </section>

    <!-- City Highlights -->
    <section class="section bg-gray-100 text-center fade-in">
      <h2 class="text-3xl font-semibold mb-4">Popular Destinations</h2>
      <div class="flex flex-wrap justify-center gap-6 mt-6">
        <div class="bg-white p-4 rounded-xl shadow-md w-64">
          <h3 class="font-bold text-xl text-blue-600">Paris</h3>
          <p>Romantic city of lights and love.</p>
        </div>
        <div class="bg-white p-4 rounded-xl shadow-md w-64">
          <h3 class="font-bold text-xl text-blue-600">Tokyo</h3>
          <p>Modern vibes, ancient temples, and amazing food.</p>
        </div>
        <div class="bg-white p-4 rounded-xl shadow-md w-64">
          <h3 class="font-bold text-xl text-blue-600">New York</h3>
          <p>The city that never sleeps — full of excitement.</p>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white text-center py-6">
      <p>© 2025 Smart Travel Planner. All rights reserved.</p>
    </footer>
  </body>
</html>




