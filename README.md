<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Para Thais</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: black;
      color: pink;
      text-align: center;
      overflow: hidden;
    }
    h1 {
      margin-top: 20px;
      font-size: 2.2em;
    }
    .container {
      display: none;
      padding: 20px;
    }
    .hearts {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }
    .heart {
      position: absolute;
      width: 15px;
      height: 15px;
      background-color: pink;
      transform: rotate(45deg);
      animation: fall linear infinite;
    }
    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 15px;
      height: 15px;
      background-color: pink;
      border-radius: 50%;
    }
    .heart::before {
      top: -7.5px;
      left: 0;
    }
    .heart::after {
      left: -7.5px;
      top: 0;
    }
    @keyframes fall {
      to {
        transform: translateY(100vh) rotate(45deg);
      }
    }
    .pin-pad {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: #111;
      padding: 20px;
      border-radius: 10px;
      z-index: 2;
    }
    .pin-display {
      background: #000;
      color: pink;
      font-size: 1.5em;
      padding: 10px;
      margin-bottom: 10px;
      letter-spacing: 10px;
    }
    .pin-buttons button {
      width: 60px;
      height: 60px;
      font-size: 1.2em;
      margin: 5px;
      background: pink;
      border: none;
      border-radius: 50%;
      color: black;
      cursor: pointer;
    }
    .rose-img {
      width: 100px;
      margin: 20px auto;
      display: block;
    }
    .firma {
      font-size: 1.2em;
      margin-top: 30px;
      font-weight: bold;
    }
    p {
      white-space: pre-line;
      padding: 0 20px;
      font-size: 1.05em;
    }
    iframe {
      border: none;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>

<div class="hearts" id="hearts"></div>

<div class="pin-pad" id="pinPad">
  <div class="pin-display" id="pinDisplay">----</div>
  <div class="pin-buttons">
    <button onclick="addNumber(1)">1</button>
    <button onclick="addNumber(2)">2</button>
    <button onclick="addNumber(3)">3</button><br/>
    <button onclick="addNumber(4)">4</button>
    <button onclick="addNumber(5)">5</button>
    <button onclick="addNumber(6)">6</button><br/>
    <button onclick="addNumber(7)">7</button>
    <button onclick="addNumber(8)">8</button>
    <button onclick="addNumber(9)">9</button><br/>
    <button onclick="clearPin()">C</button>
    <button onclick="addNumber(0)">0</button>
    <button onclick="checkPin()">OK</button>
  </div>
</div>

<div class="container" id="content">
  <h1>💌 Para Thais</h1>
  <p>Un mensaje especial, solo para ti</p>

  <iframe style="border-radius:12px" 
    src="https://open.spotify.com/embed/track/0r7CVbZTWZgbTCYdfa2P31?utm_source=generator" 
    width="80%" height="80" allowfullscreen="" 
    allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" 
    loading="lazy"></iframe>

  <img src="https://i.imgur.com/yz0aFNB.png" alt="rosa" class="rose-img" />

  <p>
Hola Thais,

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

<script>
  const correctPin = "4334";
  let pin = "";

  function addNumber(n) {
    if (pin.length < 4) {
      pin += n;
      updateDisplay();
    }
  }

  function clearPin() {
    pin = "";
    updateDisplay();
  }

  function updateDisplay() {
    document.getElementById("pinDisplay").textContent =
      pin.padEnd(4, "-");
  }

  function checkPin() {
    if (pin === correctPin) {
      document.getElementById("pinPad").style.display = "none";
      document.getElementById("content").style.display = "block";
    } else {
      alert("Código incorrecto");
      clearPin();
    }
  }

  function createHearts() {
    const hearts = document.getElementById("hearts");
    for (let i = 0; i < 50; i++) {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (Math.random() * 5 + 3) + "s";
      heart.style.top = "-" + (Math.random() * 20) + "px";
      hearts.appendChild(heart);
    }
  }
  createHearts();
</script>

</body>
</html>
