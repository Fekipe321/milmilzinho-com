<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Te Amo Multilíngue</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: sans-serif;
      text-align: center;
      color: #333;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='60' height='60'%3E%3Ctext y='50%25' x='50%25' dominant-baseline='middle' text-anchor='middle' font-size='32'%3E%F0%9F%92%96%F0%9F%8C%B9%F0%9F%92%9B%F0%9F%92%95%3C/text%3E%3C/svg%3E");
      background-repeat: repeat;
      background-size: 80px 80px;
    }

    .container {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background-color: rgba(255,255,255,0.8);
    }

    h1 {
      font-size: 2rem;
      margin-bottom: 20px;
    }

    button {
      font-size: 3rem;
      padding: 1rem 2rem;
      border: none;
      border-radius: 10px;
      background: #ff5f5f;
      color: white;
      cursor: pointer;
      transition: 0.3s ease;
    }

    button:hover {
      background: #ff2f2f;
    }

    .message {
      margin-top: 30px;
      font-size: 1.3rem;
      max-width: 90%;
      line-height: 1.6;
    }

    .more {
      margin: 50px auto;
      max-width: 600px;
      font-size: 1.2rem;
      display: none;
      background: rgba(255, 255, 255, 0.9);
      padding: 20px;
      border-radius: 10px;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Aperte</h1>
    <button id="loveBtn">?</button>
    <div class="message" id="output"></div>
  </div>

  <div class="more" id="moreMessages">
    <h2>Mais formas de dizer "Te Amo":</h2>
    <p>
      Ninapenda wewe (Suaíli)<br>
      Volim te (Croata)<br>
      Jeg elsker dig (Dinamarquês)<br>
      Te iubesc (Romeno)<br>
      Ég elska þig (Islandês)<br>
      Seni seviyorum (Turco)<br>
      Tha gràdh agam ort (Gaélico escocês)<br>
      Ngo oi nei (Cantonês)<br>
      Mahal na mahal kita (Tagalog, com intensidade)<br>
      Inhobok (Maltês)
    </p>
  </div>

  <script>
    const btn = document.getElementById("loveBtn");
    const output = document.getElementById("output");
    const more = document.getElementById("moreMessages");

    const loveMessages = [
      "Te amo (Português)",
      "I love you (Inglês)",
      "Je t'aime (Francês)",
      "Ich liebe dich (Alemão)",
      "Ti amo (Italiano)",
      "Te quiero (Espanhol)",
      "愛してる (Japonês)",
      "사랑해요 (Coreano)",
      "Я тебя люблю (Russo)",
      "我爱你 (Chinês)",
      "Eu te amu (Crioulo Cabo-verdiano)",
      "Ani ohev otach / Ani ohevet otcha (Hebraico)",
      "Saya cinta kamu (Indonésio)",
      "Ik hou van jou (Holandês)",
      "Kocham cię (Polonês)",
      "Aloha wau ia ‘oe (Havaiano)",
      "Mahal kita (Filipino)",
      "Ek is lief vir jou (Africâner)"
    ];

    btn.addEventListener("click", () => {
      output.innerHTML = loveMessages.map(msg => `❤️ ${msg}`).join("<br>");
    });

    window.addEventListener("scroll", () => {
      if (window.scrollY > 100) {
        more.style.display = "block";
      }
    });
  </script>
</body>
</html>
