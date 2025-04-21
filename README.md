<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Travel Site</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }
    body, html {
      height: 100%;
      overflow-x: hidden;
    }
    .background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-size: cover;
      background-position: center;
      z-index: -1;
      animation: backgroundChange 40s infinite;
    }

    @keyframes backgroundChange {
      0% { background-image: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e'); }
      25% { background-image: url('https://images.unsplash.com/photo-1549924231-f129b911e442'); }
      50% { background-image: url('https://images.unsplash.com/photo-1528909514045-2fa4ac7a08ba'); }
      75% { background-image: url('https://images.unsplash.com/photo-1505761671935-60b3a7427bad'); }
      100% { background-image: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e'); }
    }

    .email-box {
      position: absolute;
      top: 20%;
      left: 50%;
      transform: translateX(-50%);
      background-color: rgba(255, 255, 255, 0.85);
      padding: 20px;
      border-radius: 10px;
      text-align: center;
      max-width: 300px;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
    }

    .email-box h2 {
      font-size: 20px;
      margin-bottom: 10px;
    }

    .email-box input {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 5px;
      border: 1px solid #ccc;
    }

    .email-box button {
      padding: 10px 20px;
      background-color: #28a745;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .flyer {
      position: fixed;
      bottom: 30px;
      right: 30px;
      background-color: #4CAF50;
      color: white;
      padding: 20px;
      border-radius: 15px;
      font-weight: bold;
      animation: flyIn 1.5s ease-in-out forwards;
      display: none;
    }

    @keyframes flyIn {
      from { transform: translateX(200%); }
      to { transform: translateX(0); }
    }

    .section {
      padding: 100px 20px;
      text-align: center;
      background: rgba(255, 255, 255, 0.7);
    }

    .cards {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 30px;
    }

    .card {
      width: 200px;
      height: 250px;
      background-color: white;
      border-radius: 15px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
      overflow: hidden;
      transition: transform 0.3s;
    }

    .card:hover {
      transform: scale(1.05);
    }

    .card img {
      width: 100%;
      height: 150px;
      object-fit: cover;
    }

    .card h3 {
      padding: 10px;
      font-size: 16px;
    }

    .icon {
      font-size: 30px;
      margin-top: 20px;
      animation: floatIcon 2s infinite ease-in-out;
    }

    @keyframes floatIcon {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
  </style>
  <script>
    window.addEventListener('scroll', () => {
      const flyer = document.querySelector('.flyer');
      if (window.scrollY > 100) {
        flyer.style.display = 'block';
      }
    });
  </script>
</head>
<body>
  <div class="background"></div>
  <div class="email-box">
    <h2>Plan Your Dream Vacation!</h2>
    <input type="email" placeholder="Enter your email">
    <br>
    <input type="password" placeholder="Enter password">
    <br>
    <button>Join Now</button>
  </div>

  <div class="flyer">
    Hey! Need help planning your perfect vacation?
  </div>

  <div class="section">
    <h1>Explore the World With Us!</h1>
    <div class="icon">✈️</div>
    <p>From sunny beaches to iconic cities, we help you plan the ultimate getaway.</p>

    <div class="cards">
      <div class="card">
        <img src="https://source.unsplash.com/200x150/?newyork" alt="New York">
        <h3>New York</h3>
      </div>
      <div class="card">
        <img src="https://source.unsplash.com/200x150/?paris" alt="Paris">
        <h3>Paris</h3>
      </div>
      <div class="card">
        <img src="https://source.unsplash.com/200x150/?tokyo" alt="Tokyo">
        <h3>Tokyo</h3>
      </div>
      <div class="card">
        <img src="https://source.unsplash.com/200x150/?venice" alt="Venice">
        <h3>Venice</h3>
      </div>
      <div class="card">
        <img src="https://source.unsplash.com/200x150/?australia" alt="Australia">
        <h3>Australia</h3>
      </div>
      <div class="card">
        <img src="https://source.unsplash.com/200x150/?egypt" alt="Egypt">
        <h3>Egypt</h3>
      </div>
    </div>
  </div>
</body>
</html>


