# Site-reh
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Amo você, minha Reh 💖</title>
  <style>
    <style>
  @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    background: radial-gradient(circle at top, #fff0f5, #ffe6f0, #ffccda);
    font-family: 'Pacifico', cursive;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
    position: relative;
    padding: 1rem;
  }

  h1 {
    color: #ff4d88;
    font-size: 3em;
    text-align: center;
    text-shadow: 2px 2px 8px rgba(255, 105, 180, 0.4);
    animation: pulse 2s ease-in-out infinite;
    z-index: 2;
  }

  @keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
  }

  .heart {
    position: absolute;
    width: 20px;
    height: 20px;
    background: linear-gradient(45deg, #ff4d88, #ff99cc);
    transform: rotate(45deg);
    animation: fall 6s linear infinite;
    opacity: 0.6;
    border-radius: 50%;
  }

  .heart::before,
  .heart::after {
    content: '';
    position: absolute;
    width: 20px;
    height: 20px;
    background: inherit;
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
      transform: rotate(45deg) scale(0.8);
    }
    100% {
      top: 110%;
      left: calc(100% * var(--x));
      opacity: 0;
      transform: rotate(45deg) scale(1.2);
    }
  }

  @media (max-width: 600px) {
    h1 {
      font-size: 2em;
    }
  }
</style>

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
