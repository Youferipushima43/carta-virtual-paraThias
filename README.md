<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mensaje para Thais 💌</title>
  <style>
    /* reset box-sizing y evitar overflow horizontal */
    *, *::before, *::after { box-sizing: border-box; }
    html, body { margin: 0; padding: 0; overflow-x: hidden; }

    body {
      font-family: Arial, sans-serif;
      background-color: #fff0f5;
      color: #333;
      padding: 14px;
      display: flex;
      justify-content: center;
    }

    /* contenedor principal, se adapta al ancho de pantalla */
    .container {
      width: 100%;
      max-width: 720px; /* límite en desktop */
      margin: 18px 0;
      padding: 0 12px;
    }

    /* tarjeta blanca con carta */
    .message-card {
      background: #ffffff;
      border-radius: 12px;
      box-shadow: 0 6px 18px rgba(0,0,0,0.08);
      padding: 18px;
    }

    header {
      text-align: center;
      margin-bottom: 12px;
    }

    /* fuentes responsivas */
    header h1 { 
      color: #d63384;
      margin: 6px 0;
      font-weight: 700;
      font-size: clamp(20px, 5vw, 28px);
    }
    header p {
      margin: 0;
      color: #666;
      font-size: clamp(13px, 3.2vw, 16px);
    }

    /* sección de música: se asegura que el iframe nunca exceda el ancho */
    #music-section {
      width: 100%;
      margin: 12px 0;
      display: flex;
      justify-content: center;
      overflow: hidden;
    }
    #music-section iframe {
      width: 100%;
      max-width: 680px; /* no más ancho que la tarjeta */
      height: 60px;
      border: none;
      display: block;
    }

    .message-content {
      font-size: clamp(15px, 3.6vw, 16px);
      line-height: 1.7;
      color: #333;
      white-space: pre-line;
    }

    .rosa {
      text-align: center;
      margin-top: 14px;
    }
    .rosa img {
      width: 110px;
      max-width: 30%;
      min-width: 80px;
      border-radius: 8px;
    }

    /* PANTALLA DE PIN (overlay) */
    .bloqueo {
      position: fixed;
      inset: 0;
      background: rgba(255,230,240,0.98);
      z-index: 9999;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 18px;
      text-align: center;
    }
    .bloqueo .pin-box {
      width: 100%;
      max-width: 420px;
      background: #fff;
      border-radius: 10px;
      padding: 14px;
      box-shadow: 0 8px 30px rgba(0,0,0,0.08);
    }
    .bloqueo input {
      width: 100%;
      max-width: 320px;
      padding: 12px 10px;
      font-size: 18px;
      border: 1px solid #d9d9d9;
      border-radius: 8px;
      text-align: center;
      margin: 8px 0;
    }
    .bloqueo button {
      width: 100%;
      max-width: 200px;
      padding: 10px 14px;
      font-size: 16px;
      background-color: #d63384;
      color: #fff;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    .error { color: #b00020; margin-top: 8px; display: none; }

    /* ajustes para pantallas muy pequeñas */
    @media (max-width: 380px) {
      body { padding: 10px; }
      .message-card { padding: 12px; }
      #music-section iframe { height: 48px; }
      .rosa img { max-width: 36%; }
    }
  </style>
</head>
<body>

  <!-- Overlay PIN -->
  <div class="bloqueo" id="bloqueo">
    <div class="pin-box" role="dialog" aria-modal="true" aria-labelledby="pinTitle">
      <h2 id="pinTitle">🔒 Ingresa el PIN</h2>
      <input id="pin" type="password" inputmode="numeric" placeholder="Escribe el PIN..." maxlength="6" />
      <div style="display:flex; gap:8px; justify-content:center; margin-top:6px;">
        <button onclick="verificarPin()">Desbloquear</button>
      </div>
      <p id="error" class="error">PIN incorrecto. Intenta de nuevo.</p>
    </div>
  </div>

  <!-- Contenido -->
  <div class="container" id="contenidoReal" aria-hidden="true">
    <div class="message-card">
      <header>
        <h1>Para Thais</h1>
        <p>Un mensaje único, desde el corazón 💌</p>
      </header>

      <!-- música (si quieres ocultarla, ver nota debajo) -->
      <div id="music-section" aria-hidden="false">
        <iframe src="https://archive.org/embed/anuel-aa-secreto-ft.-karol-g" allow="autoplay; encrypted-media"></iframe>
      </div>

      <section class="message-content">
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

Feliz cumpleaños, Thais.
Donde sea que estés… que la vida te trate bonito. Siempre.

ATT:Con cariño,
Maycol.i 🌹
      </section>

      <div class="rosa">
        <img src="https://raw.githubusercontent.com/AnteroTeobaldo/BCodeProyectos/main/dia_novia_1_bcode/rosa_bonita.png" alt="Rosa para Thais">
      </div>
    </div>
  </div>

  <script>
    function verificarPin() {
      const claveCorrecta = "4334";
      const pinIngresado = document.getElementById("pin").value.trim();
      const error = document.getElementById("error");

      if (pinIngresado === claveCorrecta) {
        document.getElementById("bloqueo").style.display = "none";
        document.getElementById("contenidoReal").style.display = "block";
        document.getElementById("contenidoReal").setAttribute("aria-hidden", "false");
        error.style.display = "none";
      } else {
        error.style.display = "block";
      }
    }
  </script>
</body>
</html>


