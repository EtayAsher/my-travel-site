<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Travel Site</title>
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
      }
      header {
        background: white;
        padding: 1.5rem 2rem;
        display: flex;
        justify-content: space-between;
        align-items: center;
        box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        position: sticky;
        top: 0;
        z-index: 1000;
      }
      header h1 {
        font-size: 1.5rem;
        font-weight: 800;
      }
      .main-section {
        padding: 5rem 2rem;
        max-width: 1200px;
        margin: auto;
      }
      .hero {
        text-align: center;
        padding: 6rem 2rem;
        background: linear-gradient(120deg, #3b82f6, #06b6d4);
        color: white;
        border-radius: 2rem;
        margin-bottom: 5rem;
      }
      .hero h2 {
        font-size: 3rem;
        font-weight: 800;
        margin-bottom: 1rem;
      }
      .hero p {
        font-size: 1.25rem;
      }
      .section {
        margin-bottom: 6rem;
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
    </style>
  </head>
  <body>
    <header>
      <h1>My Travel Site</h1>
      <nav>
        <!-- Future nav links -->
      </nav>
    </header>

    <section class="main-section">
      <div class="hero">
        <h2>Discover Your Next Destination</h2>
        <p>AI-powered travel planning made easy.</p>
      </div>

      <div class="section">
        <h3>Why Travel With Us</h3>
        <div class="grid">
          <div class="card">
            <h4>Smart AI Bot</h4>
            <p>Talk to our smart assistant and get custom vacation ideas.</p>
          </div>
          <div class="card">
            <h4>Live Flight Suggestions</h4>
            <p>Updated real-time offers based on your preferences.</p>
          </div>
          <div class="card">
            <h4>Hotel Booking Support</h4>
            <p>Find the best places to stay with links ready to book.</p>
          </div>
        </div>
      </div>

      <div class="section">
        <h3>Built For Explorers</h3>
        <p>Whether you love city lights or quiet nature, we tailor your adventure.</p>
      </div>
    </section>

    <footer>
      <p>© 2025 My Travel Site | Designed for dreamers & explorers</p>
    </footer>
  </body>
</html>



