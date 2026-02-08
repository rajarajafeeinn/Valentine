# Valentine
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Be My Valentine 💖</title>

  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ffd6e8, #ffeef5);
      font-family: "Poppins", sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }

    .container {
      text-align: center;
      padding: 20px;
    }

    h1 {
      font-size: 2.2rem;
      margin-bottom: 20px;
      color: #ff4d88;
    }

    img {
      width: 250px;
      max-width: 80%;
      border-radius: 16px;
      margin-bottom: 25px;
    }

    .buttons {
      position: relative;
      height: 120px;
    }

    button {
      font-size: 1.1rem;
      padding: 12px 28px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: transform 0.2s ease;
    }

    #yesBtn {
      background-color: #ff4d88;
      color: white;
      margin-right: 20px;
    }

    #yesBtn:hover {
      transform: scale(1.1);
    }

    #noBtn {
      position: absolute;
      background-color: #aaa;
      color: #333;
    }

    .message {
      font-size: 1.5rem;
      color: #ff2f76;
      margin-top: 20px;
      display: none;
    }
  </style>
</head>

<body>
  <div class="container">
    <h1 id="question">Will you be my Valentine? 🥺👉👈</h1>

    <img
      id="gif"
      src="https://media.giphy.com/media/3oriO0OEd9QIDdllqo/giphy.gif"
      alt="Begging puppy"
    />

    <div class="buttons">
      <button id="yesBtn">YES 💖</button>
      <button id="noBtn">No</button>
    </div>

    <div class="message" id="message">
      YAYYYY 💕 Valentine secured 🥰
    </div>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const gif = document.getElementById("gif");
    const message = document.getElementById("message");
    const question = document.getElementById("question");

    function moveNoButton() {
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 60);

      noBtn.style.left = `${x}px`;
      noBtn.style.top = `${y}px`;
    }

    // Desktop hover
    noBtn.addEventListener("mouseenter", moveNoButton);

    // Mobile tap
    noBtn.addEventListener("touchstart", moveNoButton);

    yesBtn.addEventListener("click", () => {
      gif.src =
        "https://media.giphy.com/media/111ebonMs90YLu/giphy.gif";
      question.innerText = "HEHEHE 😌💘";
      message.style.display = "block";
    });

    // Initial random position for No button
    moveNoButton();
  </script>
</body>
</html>
