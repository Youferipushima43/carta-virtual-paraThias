<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Para Thais 💌</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    * {
      box-sizing: border-box;
    }

    html, body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: black;
      color: white;
      height: 100%;
      overflow: hidden;
    }

    .matrix-hearts canvas {
      position: fixed;
      top: 0;
      left: 0;
      z-index: -1;
    }

    .modal {
      position: fixed;
      z-index: 999;
      left: 0; top: 0;
      width: 100vw; height: 100vh;
      background: rgba(0,0,0,0.6);
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
      animation: popin .5s ease;
      color: #e17055;
    }

    @keyframes popin {
      from {transform: scale(.7); opacity:0;}
      to {transform: scale(1); opacity:1;}
    }

    .modal-content h2 {
      font-size: 1.2em;
      margin-bottom: 20px;
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

    .card {
      max-width: 600px;
      margin: 2rem auto;
      padding: 2rem;
      background: rgba(0, 0, 0, 0.6);
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(255, 105, 180, 0.4);
      overflow-y: auto;
      max-height: 90vh;
    }

    .header {
      text-align: center;
    }

    .header h1 {
      font-size: 2em;
      color: #ff9ecb;
    }

    .header p {
      font-style: italic;
      color: #ffd1dc;
      margin-top: 0.5rem;
    }

    .music-section {
      text-align: center;
      margin: 1rem 0;
    }

    .music-section iframe {
      width: 90%;
      height: 60px;
      border-radius: 12px;
      border: none;
    }

    .message-content p {
      font-size: 1.05rem;
      line-height: 1.8;
      color: #ffd6e0;
      margin-bottom: 1rem;
      white-space: pre-line;
    }

    .firma {
      text-align: right;
      font-size: 1.1rem;
      color: #ff99c8;
      margin-top: 2rem;
    }
  </style>
</head>
<body>

<!-- Efecto Corazones -->
<div class="matrix-hearts" id="matrixHearts"></div>

<!-- Modal de contraseña -->
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

<!-- Carta oculta -->
<div id="mainContainer" style="display:none;">
  <div class="card">
    <div class="header">
      <h1>💌 Para Thais</h1>
      <p>Un mensaje especial, solo para ti</p>
    </div>

    <div class="music-section">
      <iframe src="https://archive.org/embed/anuel-aa-secreto-ft.-karol-g" allow="autoplay"></iframe>
    </div>

    <div class="message-content">
      <p>Hola Thais,</p>
      <p>
Hoy, 29 de agosto, no quería dejar pasar el día sin decirte algo.
No sé si este mensaje llegue a ti como una sorpresa, o como algo que esperabas sin esperarlo…

Pero sinceramente, necesitaba escribirlo.

Aunque la vida nos llevó por caminos distintos —y aunque nunca llegamos a tener algo más que lo que fue—, vos marcaste una parte muy especial de mi historia. No fuimos cercanos como otros, no compartimos mil momentos ni hicimos promesas, pero hubo algo…

Algo real. Algo que aún hoy me acompaña.

No sé si alguna vez lo sentiste como yo, pero me quedé con ese amor entre las manos, sin poder entregarlo del todo. No fue por falta de ganas ni de sentimientos, simplemente la vida tenía otros planes. Y aprendí a aceptarlo… aunque no fue fácil.

Hoy es tu cumpleaños, y más allá de todo lo que no fue, quiero desearte lo mejor de lo mejor.
Que este nuevo año de vida te abrace con luz, con calma, con personas que te hagan bien y momentos que te llenen el alma.
Que la vida te cuide, te mime y te dé todo eso que soñás en silencio. Porque sí, lo merecés.

Fuiste especial para mí, aunque nunca lo dijera en voz alta. Aunque todo quedara guardado en silencios, en miradas, o en palabras que nunca se animaron a salir.
Y aún hoy, desde lejos, lo seguís siendo.
Y aunque ya no estemos en contacto, aunque no sepa nada de vos, deseo de verdad que estés bien, que seas feliz, y que te cuides mucho.

Gracias por haber existido en mi vida, así, tal como fuiste.
Gracias por lo que dejaste en mí, sin darte cuenta.
Gracias por inspirar en mí sentimientos tan puros, tan reales.

Y antes de terminar…
¿Sabés algo curioso? Esta es la primera carta que escribo. Literalmente.
Fue parte de un proyecto que me dejaron en el instituto, donde estoy estudiando desarrollo de software. Teníamos que crear algo en formato web… algo simple pero significativo, algo que combinara diseño con un mensaje personal. Y pensé en vos.

Nunca imaginé que una tarea del instituto terminaría convirtiéndose en una carta de cumpleaños para alguien tan importante para mí.
Me esforcé mucho para que saliera bien. Quería que tuviera alma.
Y funcionó. Porque gracias a Dios, me salió bien. Y por eso estás leyendo esto ahora. Porque salió bien. Porque lo hice con el corazón.

Así que, aunque suene loco, esta es mi primera "programación":
Una carta que te escribo en código, pero desde el corazón.
Y sí, el motivo, la idea, la inspiración… fuiste vos.
Gracias por eso también. Porque, sin saberlo, me diste el impulso para crear algo que no solo vale por su parte técnica, sino por todo lo que lleva dentro.

No espero respuesta. Solo quería que lo supieras.
Ojalá este mensaje te abrace por dentro, te saque una sonrisa suave, o incluso una lágrima de esas que limpian el alma.

Donde sea que estés… que la vida te trate bonito. Siempre.
      </p>
      <div class="firma">Feliz cumpleaños, Thais.✨<br>ATT, Maycol.i🌹</div>
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
      document.getElementById('mainContainer').style.display = 'block';
    } else {
      document.getElementById('errorMsg').style.display = 'block';
      clearInput();
    }
  }

  // Corazones animados
  document.addEventListener('DOMContentLoaded', function () {
    const canvas = document.createElement('canvas');
    document.getElementById('matrixHearts').appendChild(canvas);
    const ctx = canvas.getContext('2d');
    canvas.height = window.innerHeight;
    canvas.width = window.innerWidth;

    const hearts = "💗💖💕💘💝".split("");
    const font_size = 18;
    const columns = canvas.width / font_size;
    const drops = Array(Math.floor(columns)).fill(1);

    function draw() {
      ctx.fillStyle = "rgba(0, 0, 0, 0.1)";
      ctx.fillRect(0, 0, canvas.width, canvas.height);
      ctx.fillStyle = "#ff69b4";
      ctx.font = font_size + "px monospace";

      for (let i = 0; i < drops.length; i++) {
        const text = hearts[Math.floor(Math.random() * hearts.length)];
        ctx.fillText(text, i * font_size, drops[i] * font_size);

        if (drops[i] * font_size > canvas.height && Math.random() > 0.975) {
          drops[i] = 0;
        }

        drops[i]++;
      }
    }

    setInterval(draw, 70);
  });
</script>

</body>
</html>

