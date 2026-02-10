# San-valentin
Nuestra cita
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>San Valentín 💖</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      min-height: 100vh;
      margin: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    .card {
      background: white;
      width: 100%;
      max-width: 360px;
      padding: 25px 20px 40px;
      border-radius: 25px;
      box-shadow: 0 12px 30px rgba(0,0,0,0.25);
      text-align: center;
      position: relative;
    }

    h1 {
      color: #ff4d6d;
      font-size: 26px;
      margin-bottom: 25px;
    }

    p {
      font-size: 18px;
    }

    .buttons {
      margin-top: 25px;
    }

    button {
      width: 80%;
      padding: 16px;
      margin: 12px auto;
      font-size: 20px;
      border-radius: 40px;
      border: none;
      cursor: pointer;
      display: block;
      transition: transform 0.3s ease;
    }

    #yes {
      background-color: #ff4d6d;
      color: white;
    }

    #no {
      background-color: #e0e0e0;
      color: #333;
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
    }
  </style>
</head>
<body>

  <div class="card" id="card">
    <h1>¿Querés ser mi San Valentín? 💘</h1>

    <div class="buttons">
      <button id="yes">Sí 💖</button>
      <button id="no">No 😢</button>
    </div>
  </div>

  <script>
    const yesBtn = document.getElementById("yes");
    const noBtn = document.getElementById("no");
    let scale = 1;

    // Para celular: touch + mouse
    function moveNoButton() {
      const card = document.querySelector(".card");
      const cardRect = card.getBoundingClientRect();

      const x = Math.random() * (cardRect.width - noBtn.offsetWidth);
      const y = Math.random() * (cardRect.height - noBtn.offsetHeight);

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";

      scale += 0.12;
      yesBtn.style.transform = `scale(${scale})`;
    }

    noBtn.addEventListener("touchstart", moveNoButton);
    noBtn.addEventListener("mouseover", moveNoButton);

    yesBtn.addEventListener("click", () => {
      document.getElementById("card").innerHTML = `
        <h1>Vale por una cena cerca de la playa 🌊✨</h1>
        <p>Ir con algo lindo 💃🕺</p>
        <h2>NUESTRA PRIMERA CITA MI AMOOOR 💘</h2>
        <p><strong>TE AMO MI PECHOCHA ❤️</strong></p>
      `;
    });
  </script>

</body>
</html>
