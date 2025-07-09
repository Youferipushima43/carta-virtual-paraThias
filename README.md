<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Para Thais - Un mensaje único</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      height: 100vh;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #fda085, #f6d365);
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      position: relative;
    }
    .container { text-align: center; color: #fff; z-index: 1; }
    .container h1 { font-size: 2.1em; margin-bottom: 10px; }
    .container p { font-size: 1.1em; margin-bottom: 30px; }
    .envelope {
      width: 200px;
      height: 130px;
      background: #f45c5c;
      position: relative;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.3s ease;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .envelope:hover { transform: scale(1.05); }
    .envelope:before {
      content: '';
      position: absolute;
      top: 0;
      width: 0;
      height: 0;
      border-left: 100px solid transparent;
      border-right: 100px solid transparent;
      border-bottom: 65px solid #ff7e7e;
      border-radius: 10px;
    }
    .heart {
      width: 30px;
      height: 30px;
      background: white;
      clip-path: polygon(50% 0%, 100% 35%, 80% 100%, 50% 75%, 20% 100%, 0% 35%);
    }
    .card {
      position: absolute;
      background: #fffefa;
      color: #222;
      padding: 30px 20px;
      width: 85vw;
      max-width: 400px;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) scale(0);
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0,0,0,0.2);
      z-index: 2;
      transition: transform 0.4s ease;
      overflow-y: auto;
      max-height: 90vh;
    }
    .card.open { transform: translate(-50%, -50%) scale(1); }
    .card h2 { color: #f45c5c; margin-bottom: 10px; }
    .card p { line-height: 1.6; margin-bottom: 1em; }
    .close-btn {
      position: absolute;
      top: 10px;
      right: 15px;
      background: #f45c5c;
      color: white;
      border: none;
      border-radius: 50%;
      width: 28px;
      height: 28px;
      font-weight: bold;
      cursor: pointer;
    }
    .background-hearts {
      position: absolute;
      width: 100%;
      height: 100%;
      background-image: url('https://i.ibb.co/FWcCKgG/heart-bg.png');
      background-repeat: repeat;
      z-index: 0;
      opacity: 0.25;
    }
    .modal {
      position: fixed;
      top: 0; left: 0;
      width: 100vw; height: 100vh;
      background: rgba(0,0,0,0.4);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 3;
    }
    .modal-content {
      background: #fff;
      padding: 25px;
      border-radius: 12px;
      text-align: center;
      max-width: 300px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    }
    .modal-content input {
      font-size: 1.5em;
      padding: 8px;
      width: 100%;
      text-align: center;
      border: none;
      border-bottom: 2px solid #f45c5c;
      margin-bottom: 20px;
    }
    .modal-content button {
      background: #f45c5c;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 8px;
      font-size: 1em;
      cursor: pointer;
    }
    .error-msg {
      color: red;
      font-size: 0.9em;
      margin-top: 10px;
      display: none;
    }
  </style>
</head>
<body>
  <div class="background-hearts"></div>

  <div id="passwordModal" class="modal">
    <div class="modal-content">
      <h2>Ingresa la contraseña</h2>
      <input type="password" id="passInput" maxlength="6">
      <button onclick="checkPassword()">Abrir</button>
      <div id="errorMsg" class="error-msg">Contraseña incorrecta</div>
    </div>
  </div>

  <div class="container" id="mainContent" style="display: none;">
    <h1>Para Thais - Un mensaje único, desde el corazón 💌</h1>
    <p>Haz clic en el sobre para tu sorpresa</p>
    <div class="envelope" onclick="openCard()">
      <div class="heart"></div>
    </div>
  </div>

  <div id="loveCard" class="card">
    <button class="close-btn" onclick="closeCard()">×</button>
    <h2>Para Thais<br><small>Un mensaje único, desde el corazón 💌</small></h2>
    <p>Hola Thais,</p>
    <p>Hoy, 29 de agosto, no quería dejar pasar el día sin decirte algo... (todo tu mensaje completo)</p>
    <p><strong>Feliz cumpleaños, Thais.</strong><br>Donde sea que estés… que la vida te trate bonito. Siempre.</p>
    <p>Con cariño,<br><strong>Maycol.i 🌹</strong></p>
  </div>

  <script>
    const PASSWORD = "4334";
    function checkPassword() {
      const input = document.getElementById('passInput').value;
      if (input === PASSWORD) {
        document.getElementById('passwordModal').style.display = 'none';
        document.getElementById('mainContent').style.display = 'block';
      } else {
        document.getElementById('errorMsg').style.display = 'block';
      }
    }
    function openCard() {
      document.getElementById('loveCard').classList.add('open');
    }
    function closeCard() {
      document.getElementById('loveCard').classList.remove('open');
    }
  </script>
</body>
</html>

