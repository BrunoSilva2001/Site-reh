# Site-reh
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Amo você, minha Reh 💖</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, #ffe6f0, #fff0f5);
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
      position: relative;
    }

    h1 {
      color: #e60073;
      font-size: 3.5em;
      text-align: center;
      text-shadow: 1px 1px 2px #ffb6c1;
      animation: pulse 2s infinite;
      z-index: 2;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.1); }
      100% { transform: scale(1); }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: fall 6s infinite;
      opacity: 0.6;
      border-radius: 50%;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes fall {
      0% {
        top: -10%;
        opacity: 1;
      }
      100% {
        top: 110%;
        left: calc(100% * var(--x));
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>Amo você, minha Reh 💖</h1>

  <!-- corações caindo -->
  <script>
    for (let i = 0; i < 30; i++) {
      let heart = document.createElement("div");
      heart.classList.add("heart");
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDelay = Math.random() * 5 + "s";
      heart.style.setProperty('--x', Math.random());
      document.body.appendChild(heart);
    }
  </script>
</body>
</html>
