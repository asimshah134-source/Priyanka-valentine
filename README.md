<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Valentine Priyanka 💕</title>

  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      text-align: center;
      max-width: 380px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
      animation: fadeIn 2s ease;
    }

    h1 {
      font-family: 'Pacifico', cursive;
      color: #ff4d6d;
      font-size: 2.3rem;
      margin-bottom: 10px;
    }

    p {
      font-size: 1rem;
      color: #555;
      margin-bottom: 20px;
      line-height: 1.6;
    }

    button {
      background: #ff4d6d;
      border: none;
      color: white;
      padding: 12px 28px;
      font-size: 1rem;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #e63e5c;
      transform: scale(1.05);
    }

    .hidden {
      display: none;
    }

    .hearts span {
      position: absolute;
      bottom: -50px;
      font-size: 20px;
      animation: floatUp 6s infinite;
      opacity: 0.8;
    }

    @keyframes floatUp {
      0% { transform: translateY(0); opacity: 0; }
      50% { opacity: 1; }
      100% { transform: translateY(-120vh); opacity: 0; }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Priyanka Oberoi 💖</h1>
    <p>
      From the moment you entered my life,<br>
      everything started feeling warmer, happier, and more meaningful 🌹
    </p>

    <button onclick="showLove()">Tap for a Surprise 💝</button>

    <p id="finalMessage" class="hidden">
      Priyanka, will you be my Valentine? 💕<br><br>
      Today, tomorrow, and always ❤️
    </p>
  </div>

  <div class="hearts"></div>

  <script>
    function showLove() {
      document.getElementById("finalMessage").classList.remove("hidden");
      createHearts();
    }

    function createHearts() {
      const heartsContainer = document.querySelector(".hearts");
      for (let i = 0; i < 25; i++) {
        const heart = document.createElement("span");
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
        heartsContainer.appendChild(heart);

        setTimeout(() => {
          heart.remove();
        }, 6000);
      }
    }
  </script>

</body>
</html>
