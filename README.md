<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Te Amo</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: radial-gradient(#ffdee9, #b5fffc);
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      font-family: "Arial", sans-serif;
    }

    h1 {
      font-size: 4em;
      color: #ff4d6d;
      text-shadow: 2px 2px 5px #fff;
      position: absolute;
      z-index: 1;
    }

    .heart {
      position: absolute;
      font-size: 1.5em;
      animation: float 2s ease-out forwards;
      pointer-events: none;
      opacity: 0.8;
    }

    @keyframes float {
      0% {
        transform: translateY(0) scale(1);
        opacity: 1;
      }
      100% {
        transform: translateY(-200px) scale(1.5);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>Te amo ❤️</h1>

  <script>
    const frases = [
      "Te amo 💖",
      "Eres mi todo",
      "Mi vida",
      "Contigo todo 💘",
      "Siempre tú 💫",
      "Mi persona favorita",
      "Tú y yo 💞",
      "Un amor infinito"
    ];

    document.body.addEventListener("click", (e) => {
      for (let i = 0; i < 10; i++) {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.textContent = frases[Math.floor(Math.random() * frases.length)];
        heart.style.left = `${e.clientX}px`;
        heart.style.top = `${e.clientY}px`;
        heart.style.color = `hsl(${Math.random() * 360}, 80%, 60%)`;
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 2000);
      }
    });
  </script>
</body>
</html>
