<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Carta para Thaiss</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
  <style>
    body {
      background: linear-gradient(135deg, #f6d365 0%, #fda085 100%);
      font-family: 'Segoe UI', Arial, sans-serif;
      margin: 0;
      padding: 0;
      min-height: 100vh;
      box-sizing: border-box;
    }
    .container {
      max-width: 600px;
      margin: 50px auto 0 auto;
      background: #fffefa;
      border-radius: 18px;
      box-shadow: 0 8px 36px rgba(238, 183, 158, 0.27), 0 2px 6px #ffecd2;
      border: 3.5px solid #ffb980;
      padding: 0 0 20px 0;
      position: relative;
      overflow: hidden;
    }
    .header {
      background: linear-gradient(90deg, #ffe3c0 0%, #eeb79e 100%);
      padding: 32px 0 18px 0;
      border-radius: 18px 18px 0 0;
      text-align: center;
      box-shadow: 0 2px 10px #ffd1a099;
      margin-bottom: 0;
    }
    .header h1 {
      margin: 0;
      font-size: 2.2em;
      color: #e17055;
      letter-spacing: 1px;
      text-shadow: 0 2px 10px #fffecd, 0 2px 12px #ffe3c088;
      font-weight: bold;
    }
    .header p {
      margin: 8px 0 0 0;
      color: #8d5524;
      font-size: 1.06em;
    }
    .music-section {
      width: 100%;
      text-align: center;
      margin-top: 20px;
      margin-bottom: 16px;
      display: none;
    }
    .music-section iframe {
      width: 98%;
      max-width: 500px;
      height: 60px;
      border: none;
      border-radius: 10px;
    }
    .message-section {
      padding: 18px 30px 0 30px;
    }
    .message-section h2 {
      color: #e17055;
      font-size: 1.42em;
      margin-bottom: 12px;
      letter-spacing: 1px;
      font-weight: bold;
      text-shadow: 0 2px 6px #ffd1a022;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .message-content p {
      color: #444;
      font-size: 1.14em;
      line-height: 1.7;
      text-align: left;
      white-space: pre-line;
      margin-bottom: 15px;
    }
    .firma {
      text-align: right;
      font-size: 1.1em;
      margin-bottom: 0;
      color: #d35400;
      margin-right: 10px;
      margin-top: 10px;
    }
    .modal {
      position: fixed;
      z-index: 999;
      left: 0; top: 0; width: 100vw; height: 100vh;
      background: rgba(60,30,30,0.17);
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .modal-content {
      background: #fffbea;
      border-radius: 25px;
      padding: 34px 24px 24px 24px;
      box-shadow: 0 8px 32px rgba(48, 26, 10, 0.23);
      min-width: 320px;
      display: flex;
      flex-direction: column;
      align-items: center;
      border: 2.5px solid #ffb980;
      animation: popin .5s cubic-bezier(.17,.67,.83,.67);
    }
    @keyframes popin {
      from {transform: scale(.7); opacity:0;}
      to {transform: scale(1); opacity:1;}
    }
    .modal-content h2 {
      font-size: 1.23em;
      margin-bottom: 20px;
      color: #e17055;
      letter-spacing: 1px;
    }
    #passInput {
      width: 120px;
      font-size: 1.7em;
      letter-spacing: 12px;
      text-align: center;
      border: none;
      border-bottom: 2.5px solid #e17055;
      background: transparent;
      margin-bottom: 18px;
      outline: none;
      color: #e17055;
      font-weight: bold;
      padding: 6px 0;
    }
    .calc-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: center;
      margin-bottom: 10px;
    }
    .calc-btn {
      width: 48px;
      height: 48px;
      border: none;
      border-radius: 13px;
      background: linear-gradient(180deg, #ffd6b2 0%, #feb47b 100%);
      color: #d35400;
      font-size: 1.23em;
      font-weight: bold;
      cursor: pointer;
    }
    .calc-btn:active {
      transform: scale(0.97);
    }
    .calc-btn.special {
      background: linear-gradient(180deg, #fff0f0 0%, #f8bfbf 100%);
      color: #e17055;
    }
    #errorMsg {
      color: #e74c3c;
      font-size: 1em;
      margin-top: 4px;
      display: none;
      font-weight: 500;
      letter-spacing: .5px;
    }
    @media (max-width: 650px) {
      .container { max-width: 99vw; margin-top: 18vw; padding: 0 0 12vw 0; }
      .message-section { padding: 5vw 3vw 0 3vw; }
      .music-section iframe { width: 98vw !important; }
    }
  </style>
</head>
<body>
  <div id="passwordModal" class="modal">
    <form class="modal-content" onsubmit="event.preventDefault(); checkPassword();">
      <h2>Ingresa la contraseña</h2>
      <input type="password" id="passInput" maxlength="8" readonly autocomplete="off" />
      <div class="calc-buttons">
        <button type="button" class="calc-btn" onclick="addNumber('1')">1</button>
        <button type="button" class="calc-btn" onclick="addNumber('2')">2</button>
        <button type="button" class="calc-btn" onclick="addNumber('3')">3</button>
        <button type="button" class="calc-btn" onclick="addNumber('4')">4</button>
        <button type="button" class="calc-btn" onclick="addNumber('5')">5</button>
        <button type="button" class="calc-btn" onclick="addNumber('6')">6</button>
        <button type="button" class="calc-btn" onclick="addNumber('7')">7</button>
        <button type="button" class="calc-btn" onclick="addNumber('8')">8</button>
        <button type="button" class="calc-btn" onclick="addNumber('9')">9</button>
        <button type="button" class="calc-btn special" onclick="clearInput()">Borrar</button>
        <button type="button" class="calc-btn" onclick="addNumber('0')">0</button>
        <button type="submit" class="calc-btn special">OK</button>
      </div>
      <p id="errorMsg">Contraseña incorrecta</p>
    </form>
  </div>

  <div id="mainContainer" class="container" style="display:none;">
    <div class="header">
      <h1><i class="fa-solid fa-envelope-open-heart"></i> Para Thais</h1>
      <p>Un mensaje especial, solo para ti 💌</p>
    </div>
    <div id="music-section" class="music-section">
      <iframe src="https://archive.org/embed/anuel-aa-secreto-ft.-karol-g" allow="autoplay"></iframe>
    </div>
    <section class="message-section">
      <h2><i class="fas fa-heart"></i> Mi Mensaje Para Ti</h2>
      <div class="message-content">
        <p>Hola Thais,</p>
        <p>
Hoy, 29 de agosto, no podía dejar pasar este día sin escribirte. Aunque la distancia —y quizás el silencio—.  
Cumplís un año más de vida, y espero de corazón que llegue cargado de luz, salud, momentos que te llenen el alma y personas que te recuerden lo increíble que sos.  
Aunque ya no esté cerca, aunque nuestras palabras hayan dejado de cruzarse como antes, lo que fuiste y lo que significaste no se borra.  
Fuiste importante, lo sos, y lo serás de alguna forma siempre.

Te deseo lo mejor de lo mejor, no solo hoy, sino cada día que el mundo tenga la suerte de tenerte en él.  
Que la vida te abrace con lo que merecés y que sigas creciendo, brillando y alcanzando todo lo que te propongas.

Gracias por haber sido parte de mi vida, y por todo lo que dejaste en mí.  
Hoy, desde lejos, te mando un abrazo silencioso pero real, deseando que seas feliz, sinceramente.
        </p>
        <div class="firma">Feliz cumpleaños, Thais.✨<br>ATT, Maycol.i🌹</div>
      </div>
    </section>
  </div>

  <script>
    const CORRECT_PASSWORD = "4334";
    function addNumber(num) {
      const input = document.getElementById('passInput');
      if (input.value.length < input.maxLength) {
        input.value += num;
      }
      document.getElementById('errorMsg').style.display = 'none';
    }
    function clearInput() {
      document.getElementById('passInput').value = '';
      document.getElementById('errorMsg').style.display = 'none';
    }
    function checkPassword() {
      const value = document.getElementById('passInput').value;
      if (value === CORRECT_PASSWORD) {
        document.getElementById('passwordModal').style.display = 'none';
        document.getElementById('mainContainer').style.display = 'block';
        document.getElementById('music-section').style.display = 'block';
      } else {
        document.getElementById('errorMsg').style.display = 'block';
        clearInput();
      }
    }
    window.onload = () => {
      document.getElementById('mainContainer').style.display = 'none';
      document.getElementById('music-section').style.display = 'none';
      document.getElementById('passInput').focus();
    };
  </script>
</body>
</html>
      
 
