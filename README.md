<!DOCTYPE html><html lang="es">
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
    .container { text-align: center; color: #fff; z-index: 1; display: none; }
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
      margin: 0 auto;
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
      z-index: 2;
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
  <div class="background-hearts"></div>  <div id="passwordModal" class="modal">
    <div class="modal-content">
      <h2>Ingresa la contraseña</h2>
      <input type="password" id="passInput" maxlength="6">
      <button onclick="checkPassword()">Abrir</button>
      <div id="errorMsg" class="error-msg">Contraseña incorrecta</div>
    </div>
  </div>  <div class="container" id="mainContent">
    <h1>Para Thais - Un mensaje único, desde el corazón 💌</h1>
    <p>Haz clic en el sobre para tu sorpresa</p>
    <div class="envelope" onclick="openCard()">
      <div class="heart"></div>
    </div>
  </div>  <div id="loveCard" class="card">
    <button class="close-btn" onclick="closeCard()">×</button>
    <h2>Para Thais<br><small>Un mensaje único, desde el corazón 💌</small></h2>
    <p>Hola Thais,</p>
    <p>Hoy, 29 de agosto, no quería dejar pasar el día sin decirte algo.<br>No sé si este mensaje llegue a ti como una sorpresa, o como algo que esperabas sin esperarlo…<br>Pero sinceramente, necesitaba escribirlo.</p>
    <p>Aunque la vida nos llevó por caminos distintos —y aunque nunca llegamos a tener algo más que lo que fue—, vos marcaste una parte muy especial de mi historia. No fuimos cercanos como otros, no compartimos mil momentos ni hicimos promesas, pero hubo algo…<br>Algo real. Algo que aún hoy me acompaña.</p>
    <p>No sé si alguna vez lo sentiste como yo, pero me quedé con ese amor entre las manos, sin poder entregarlo del todo. No fue por falta de ganas ni de sentimientos, simplemente la vida tenía otros planes. Y aprendí a aceptarlo… aunque no fue fácil.</p>
    <p>Hoy es tu cumpleaños, y más allá de todo lo que no fue, quiero desearte lo mejor de lo mejor.<br>Que este nuevo año de vida te abrace con luz, con calma, con personas que te hagan bien y momentos que te llenen el alma.<br>Que la vida te cuide, te mime y te dé todo eso que soñás en silencio. Porque sí, lo merecés.</p>
    <p>Fuiste especial para mí, aunque nunca lo dijera en voz alta. Aunque todo quedara guardado en silencios, en miradas, o en palabras que nunca se animaron a salir.<br>Y aún hoy, desde lejos, lo seguís siendo.<br>Y aunque ya no estemos en contacto, aunque no sepa nada de vos, deseo de verdad que estés bien, que seas feliz, y que te cuides mucho.</p>
    <p>Gracias por haber existido en mi vida, así, tal como fuiste.<br>Gracias por lo que dejaste en mí, sin darte cuenta.<br>Gracias por inspirar en mí sentimientos tan puros, tan reales.</p>
    <p>Y antes de terminar…<br>¿Sabés algo curioso? Esta es la primera carta que escribo. Literalmente.<br>Fue parte de un proyecto que me dejaron en el instituto, donde estoy estudiando desarrollo de software. Teníamos que crear algo en formato web… algo simple pero significativo, algo que combinara diseño con un mensaje personal. Y pensé en vos.</p>
    <p>Nunca imaginé que una tarea del instituto terminaría convirtiéndose en una carta de cumpleaños para alguien tan importante para mí.<br>Me esforcé mucho para que saliera bien. Quería que tuviera alma.<br>Y funcionó. Porque gracias a Dios, me salió bien. Y por eso estás leyendo esto ahora. Porque salió bien. Porque lo hice con el corazón.</p>
    <p>Así que, aunque suene loco, esta es mi primera "programación":<br>Una carta que te escribo en código, pero desde el corazón.<br>Y sí, el motivo, la idea, la inspiración… fuiste vos.<br>Gracias por eso también. Porque, sin saberlo, me diste el impulso para crear algo que no solo vale por su parte técnica, sino por todo lo que lleva dentro.</p>
    <p>No espero respuesta. Solo quería que lo supieras.<br>Ojalá este mensaje te abrace por dentro, te saque una sonrisa suave, o incluso una lágrima de esas que limpian el alma.</p>
    <p><strong>Feliz cumpleaños, Thais.</strong><br>Donde sea que estés… que la vida te trate bonito. Siempre.</p>
    <p>Con cariño,<br><strong>Maycol.i 🌹</strong></p>
  </div>  <script>
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
  </script></body>
</html>

