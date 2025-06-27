<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Carta para Thaiss</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    html, body {
      height: 100%;
      margin: 0;
      padding: 0;
      background: radial-gradient(circle, #ffe3c0 0%, #eeb79e 100%);
      font-family: 'Segoe UI', Arial, sans-serif;
      overflow: hidden;
      width: 100vw;
    }
    .main-title {
      margin-top: 24px;
      margin-bottom: 12px;
      font-size: 2.2em;
      font-weight: bold;
      color: #e17055;
      letter-spacing: 1px;
      text-shadow: 0 2px 10px #ffecd2bb, 0 2px 12px #ffe3c088;
      text-align: center;
      width: 100vw;
      z-index: 2;
      position: relative;
    }
    .modal {
      position: fixed;
      z-index: 10;
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
      min-height: 240px;
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
      transition: border-color .2s;
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
      margin: 2px 0;
      box-shadow: 0 2px 8px rgba(255,184,128,0.13), 0 1px 2px #fff4;
      transition: background .2s, transform .09s;
      cursor: pointer;
      outline: none;
      user-select: none;
    }
    .calc-btn:active {
      background: linear-gradient(180deg, #feb47b 0%, #ffd6b2 100%);
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
    .carta-virtual {
      background: #fffefa;
      border: 3.5px solid #ffb980;
      border-radius: 18px;
      box-shadow: 0 8px 36px rgba(100, 60, 20, 0.13), 0 2px 6px #ffecd2;
      width: 540px;
      max-width: 93vw;
      min-width: 310px;
      height: 1098px; /* 10 cm menos que antes */
      max-height: none;
      min-height: 420px;
      margin: 0 auto;
      position: fixed;
      left: 50%; top: 52%;
      transform: translate(-50%, -50%);
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: stretch;
      z-index: 3;
      animation: cartaReveal .9s cubic-bezier(.17,.67,.83,.67);
    }
    @keyframes cartaReveal {
      from { transform: translate(-50%, 60px) scale(.93); opacity:0; }
      to { transform: translate(-50%, -50%) scale(1); opacity:1; }
    }
    .carta-music {
      width: 100%;
      text-align: center;
      margin-top: 25px;
      margin-bottom: 2px;
    }
    .carta-music iframe {
      width: 98%;
      min-width: 180px;
      max-width: 500px;
      height: 60px;
      border: none;
    }
    .carta-header {
      text-align: left;
      margin: 16px 0 10px 36px;
    }
    .carta-title {
      font-size: 2em;
      font-weight: bold;
      color: #e17055;
      margin-bottom: 4px;
      letter-spacing: .5px;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .carta-title .emoji {
      font-size: 1em;
    }
    .carta-scroll {
      flex: 1 1 auto;
      overflow-y: auto;
      padding: 0 36px 0 36px;
      margin-bottom: 8px;
    }
    .carta-body {
      color: #444;
      font-size: 1.14em;
      line-height: 1.7;
      text-align: left;
      white-space: pre-line;
      margin-bottom: 16px;
      margin-top: 0;
    }
    .carta-firma {
      text-align: right;
      font-size: 1.1em;
      margin-bottom: 30px;
      color: #d35400;
      margin-right: 36px;
    }
    .carta-virtual::before, .carta-virtual::after {
      content: '';
      position: absolute;
      width: 44px; height: 44px;
      background: url('https://cdn-icons-png.flaticon.com/512/616/616494.png') no-repeat center/60%;
      opacity: .11;
      pointer-events: none;
    }
    .carta-virtual::before {
      top: 8px; left: 8px; transform: rotate(-12deg);
    }
    .carta-virtual::after {
      bottom: 8px; right: 8px; transform: rotate(8deg);
    }
    .carta-scroll::-webkit-scrollbar {
      width: 8px;
    }
    .carta-scroll::-webkit-scrollbar-thumb {
      background: #ffe3c0;
      border-radius: 6px;
    }
    @media (max-width: 600px) {
      .main-title {
        font-size: 1.15em;
        margin-top: 12px;
        margin-bottom: 4px;
      }
      .carta-virtual {
        width: 98vw;
        min-width: 0;
        max-width: 99vw;
        height: 160vw;
        min-height: 290px;
        left: 50%; top: 53%;
        transform: translate(-50%, -50%);
      }
      .carta-title {
        font-size: 1.31em;
      }
      .carta-header {
        margin-left: 10px;
      }
      .carta-firma {
        font-size: 1em;
        margin-right: 10px;
        margin-bottom: 14px;
      }
      .carta-music iframe {
        width: 98vw !important;
      }
      .carta-scroll {
        padding: 0 10px 0 14px;
      }
    }
    #music-frame {
      display: none;
    }
  </style>
</head>
<body>
  <div class="main-title">UN MENSAJE ESPECIAL PARA TI</div>
  <!-- MODAL DE CONTRASEÑA CON CALCULADORA -->
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
  <!-- CARTA VIRTUAL -->
  <div id="carta" class="carta-virtual" style="display:none;">
    <!-- Música arriba de la carta -->
    <div id="music-frame" class="carta-music">
      <iframe src="https://archive.org/embed/anuel-aa-secreto-ft.-karol-g" width="500" height="60" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" allowfullscreen></iframe>
    </div>
    <!-- Cabecera de la carta -->
    <div class="carta-header">
      <div class="carta-title">
        Para Thais <span class="emoji">💌</span>
      </div>
    </div>
    <!-- Contenido de la carta con scroll interno -->
    <div class="carta-scroll">
      <div class="carta-body">
Hola Thais,

Hoy, 29 de agosto, no podía dejar pasar este día sin escribirte. Aunque la distancia —y quizás el silencio pero bueno—

Cumplís un año más de vida, y espero de corazón que llegue cargado de luz, salud, momentos que te llenen el alma y personas que te recuerden lo increíble que sos. Aunque ya no esté cerca, aunque nuestras palabras hayan dejado de cruzarse como antes, lo que fuiste y lo que significaste no se borra. Fuiste importante, lo sos, y lo serás de alguna forma siempre.

Te deseo lo mejor de lo mejor, no solo hoy, sino cada día que el mundo tenga la suerte de tenerte en él. Que la vida te abrace con lo que merecés y que sigas creciendo, brillando y alcanzando todo lo que te propongas.

Gracias por haber sido parte de mi vida, y por todo lo que dejaste en mí. Hoy, desde lejos, te mando un abrazo silencioso pero real, deseando que seas feliz, sinceramente.

Feliz cumpleaños, Thais.✨

ATT, Maycol.i🌹 
      </div>
    </div>
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
        document.getElementById('carta').style.display = 'flex';
        document.getElementById('music-frame').style.display = 'block';
      } else {
        document.getElementById('errorMsg').style.display = 'block';
        clearInput();
      }
    }
    document.getElementById('passInput').addEventListener('keydown', function(e){
      if(e.key === 'Enter'){ checkPassword(); }
    });
    window.onload = () => {
      document.getElementById('carta').style.display = 'none';
      document.getElementById('music-frame').style.display = 'none';
    };
  </script>
</body>
</html>
