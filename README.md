<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Holi Shikha!</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Dancing Script', cursive;
      text-align: center;
      margin: 0;
      padding: 0;
      font-size: 24px;
    }
    .page {
      display: none;
      padding: 20px;
      min-height: 100vh;
      position: relative;
      overflow: hidden;
    }
    #page1 {
      display: block;
      background: linear-gradient(rgba(255,255,255,0.8), rgba(255,255,255,0.8)),
                  url('https://i.pinimg.com/736x/61/6b/8a/616b8a1d5a9b406b0e3e3d5a7d3a3b3d.jpg') center/cover;
    }
    #page2 {
      background: linear-gradient(rgba(255,255,255,0.8), rgba(255,255,255,0.8)),
                  url('https://img.freepik.com/free-photo/holi-color-powder-explosion_1048-7521.jpg') center/cover;
    }
    #page3 {
      background: linear-gradient(rgba(255,255,255,0.8), rgba(255,255,255,0.8)),
                  url('https://images.pexels.com/photos/2879832/pexels-photo-2879832.jpeg') center/cover;
    }
    h1 {
      color: #ff69b4;
      font-size: 48px;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
      margin: 20px 0;
    }
    button {
      padding: 15px 30px;
      font-size: 28px;
      background: linear-gradient(45deg, #ff69b4, #9400d3);
      color: white;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      margin-top: 30px;
      font-family: 'Dancing Script', cursive;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    button:hover {
      background: linear-gradient(45deg, #ff1493, #8a2be2);
    }
    .secret-box {
      background: rgba(255,255,255,0.9);
      padding: 20px;
      border-radius: 15px;
      max-width: 600px;
      margin: 20px auto;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
      position: relative;
      z-index: 1;
    }
    .colorful-text {
      background: linear-gradient(45deg, #ff69b4, #ff4500, #9400d3);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      font-weight: 700;
    }
  </style>
</head>
<body>

  <!-- Page 1: Secret Code -->
  <div id="page1" class="page">
    <div class="secret-box">
      <h1 class="colorful-text">🎨 Welcome to Your Holi Surprise! 💖</h1>
      <p>✨ Enter the secret code to continue:</p>
      <input type="text" id="secretCode" placeholder="Your Name">
      <button onclick="checkCode()">Unlock Magic 🗝️</button>
      <p id="error" style="color: #ff0000; display: none; font-size: 20px;">🚫 This is not for you! Chl Nikal😡</p>
    </div>
  </div>

  <!-- Page 2: Wishes -->
  <div id="page2" class="page">
    <div class="secret-box">
      <h1 class="colorful-text">🎉 Holi Special Wishes! 🎊</h1>
      <div style="font-size: 32px;">
        <p>🌸 May your joy bloom like Gulal! 🌸</p>
        <p>🌈 Every day be as colorful as Holi!</p>
        <p>💦 May life shower you with happiness!</p>
        <p>🎨 Create memories brighter than Holi colors!</p>
        <p>😄 Joke: Why did the color red blush?<br>It saw the other colors! 🤣</p>
        <p>🥟 Wishing you sweetness with every Gujiya!</p>
        <p>💃🕺 Dance like nobody's watching!</p>
      </div>
      <button onclick="showVideoPage()">Next ❓</button>
    </div>
  </div>

  <!-- Page 3: Video -->
  <div id="page3" class="page">
    <div class="secret-box">
      <h2 class="colorful-text">🎉 Happy Holi Dear Shikha! 🎨</h2>
      <div>
        <!-- Redirecting to YouTube Shorts video -->
        <button onclick="window.open('https://youtube.com/shorts/fUKpL_rPszE', '_blank')">Watch Holi Video 🎥</button>
      </div>
    </div>
  </div>

  <script>
    function checkCode() {
      const secretCode = document.getElementById("secretCode").value;
      if (secretCode.toLowerCase() === "shikha") {
        document.getElementById("page1").style.display = "none";
        document.getElementById("page2").style.display = "block";
      } else {
        document.getElementById("error").style.display = "block";
      }
    }

    function showVideoPage() {
      document.getElementById("page2").style.display = "none";
      document.getElementById("page3").style.display = "block";
    }
  </script>
</body>
</html>
