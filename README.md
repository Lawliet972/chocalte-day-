<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Chocolate Day 🍫</title>

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500&family=Poppins:wght@300&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #3e2723, #6d4c41);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Poppins', sans-serif;
      overflow: hidden;
    }

    .card {
      background: #fff7f2;
      padding: 45px;
      border-radius: 22px;
      box-shadow: 0 25px 50px rgba(0,0,0,0.25);
      text-align: center;
      max-width: 420px;
      animation: fadeIn 1.8s ease;
    }

    h1 {
      font-family: 'Playfair Display', serif;
      color: #5d4037;
      margin-bottom: 12px;
    }

    p {
      color: #4e342e;
      line-height: 1.7;
      font-size: 16px;
    }

    footer {
      margin-top: 22px;
      font-size: 14px;
      color: #6d4c41;
    }

    /* Chocolate */
    .choco-container {
      cursor: pointer;
      margin-bottom: 20px;
    }

    .choco {
      font-size: 55px;
      animation: float 3s infinite ease-in-out;
    }

    #tapText {
      font-size: 14px;
      color: #6d4c41;
      margin-top: 8px;
    }

    .message {
      display: none;
      animation: fadeInUp 1.5s ease forwards;
    }

    .message.show {
      display: block;
    }

    .choco.open {
      animation: melt 1s ease forwards;
    }

    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
      100% { transform: translateY(0); }
    }

    @keyframes melt {
      0% { transform: scale(1); }
      60% { transform: scale(1.35) rotate(-6deg); }
      100% { transform: scale(1.15); }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(25px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>

<body>

  <div class="card">

    <!-- Tap Chocolate -->
    <div class="choco-container" onclick="openChocolate()">
      <div class="choco" id="choco">🍫</div>
      <p id="tapText">Tap the chocolate 🍫</p>
    </div>

    <!-- Hidden Message -->
    <div class="message" id="message">
      <h1>Happy Chocolate Day, Khushboo 🍫</h1>

      <p>
        Chocolate is sweet, comforting, and irresistible —<br>
        just like you.<br><br>

        I’m really sorry I couldn’t wake you up this morning 😔<br>
        but I hope this makes up for it a little.<br><br>

        Even though I can"t give you real chocolates today,personally <br>
        I wanted to give you something made with love.<br><br>

        No matter the distance,<br>
        you’ll always be my favorite treat. 🍫❤️<br><br>

        So tell me… 😉<br>
        <strong>which chocolate do you want?</strong>
      </p>

      <footer>
        — Forever yours, Abhishek ❤️
      </footer>
    </div>

  </div>

  <script>
    function openChocolate() {
      document.getElementById("choco").classList.add("open");
      document.getElementById("tapText").style.display = "none";
      document.getElementById("message").classList.add("show");
    }
  </script>

</body>
</html>
