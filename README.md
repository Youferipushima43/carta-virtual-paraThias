<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Para Thais</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: black;
      color: white;
      font-family: 'Georgia', serif;
      overflow: hidden;
    }

    .pin-container, .carta-container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .pin-box {
      background: rgba(255, 192, 203, 0.1);
      padding: 30px;
      border-radius: 20px;
      text-align: center;
    }

    .pin-box input {
      width: 100px;
      font-size: 24px;
      text-align: center;
      padding: 10px;
      border-radius: 10px;
      border: none;
      margin-bottom: 15px;
    }

    .pin-box button {
      padding: 10px 20px;
      font-size: 18px;
      background: pink;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }

    .carta {
      width: 340px;
      max-height: 90vh;
      background: #1c1c1c;
      padding: 20px;
      border-radius: 15px;
      overflow-y: auto;
      box-shadow: 0 0 15px #ff69b4;
      position: relative;
    }

    .carta p {
      font-size: 16px;
      line-height: 1.6;
      margin-bottom: 15px;
      text-align: justify;
    }

    .firma {
      margin-top: 30px;
      text-align: right;
      font-style: italic;
      font-size: 17px;
    }

    .rosa {
      text-align: center;
      margin-top: 20px;
    }

    .rosa img {
      width: 100px;
    }

    iframe {
      display: none;
    }
  </style>
</head>
<body>

<div class="pin-container" id="pinPage">
  <div class="pin-box">
    <h2>Ingresa el PIN</h2>
    <input type="password" id="pinInput" maxlength="4" />
    <br />
    <button onclick="verificarPIN()">Desbloquear</button>
  </div>
</div>

<div class="carta-container" id="cartaPage" style="display:none;">
  <div class="carta">
    <p>Hola Thais,</p>

    <p>Hoy, 29 de agosto, no quería dejar pasar el día sin decirte algo.  
    No sé si este mensaje llegue a ti como una sorpresa, o como algo que esperabas sin esperarlo…  
    Pero sinceramente, necesitaba escribirlo.</p>

    <p>Aunque la vida nos llevó por caminos distintos —y aunque nunca llegamos a tener algo más que lo que fue—, vos marcaste una parte muy especial de mi historia.  
    No fuimos cercanos como otros, no compartimos mil momentos ni hicimos promesas, pero hubo algo…  
    Algo real. Algo que aún hoy me acompaña.</p>

    <p>No sé si alguna vez lo sentiste como yo, pero me quedé con ese amor entre las manos, sin poder entregarlo del todo.  
    No fue por falta de ganas ni de sentimientos, simplemente la vida tenía otros planes. Y aprendí a aceptarlo… aunque no fue fácil.</p>

    <p>Hoy es tu cumpleaños, y más allá de todo lo que no fue, quiero desearte lo mejor de lo mejor.  
    Que este nuevo año de vida te abrace con luz, con calma, con personas que te hagan bien y momentos que te llenen el alma.  
    Que la vida te cuide, te mime y te dé todo eso que soñás en silencio. Porque sí, lo merecés.</p>

    <p>Fuiste especial para mí, aunque nunca lo dijera en voz alta. Aunque todo quedara guardado en silencios, en miradas, o en palabras que nunca se animaron a salir.  
    Y aún hoy, desde lejos, lo seguís siendo.  
    Y aunque ya no estemos en contacto, aunque no sepa nada de vos, deseo de verdad que estés bien, que seas feliz, y que te cuides mucho.</p>

    <p>Gracias por haber existido en mi vida, así, tal como fuiste.  
    Gracias por lo que dejaste en mí, sin darte cuenta.  
    Gracias por inspirar en mí sentimientos tan puros, tan reales.</p>

    <p>Y antes de terminar…  
    ¿Sabés algo curioso? Esta es la primera carta que escribo. Literalmente.  
    Fue parte de un proyecto que me dejaron en el instituto, donde estoy estudiando desarrollo de software.  
    Teníamos que crear algo en formato web… algo simple pero significativo, algo que combinara diseño con un mensaje personal. Y pensé en vos.</p>

    <p>Nunca imaginé que una tarea del instituto terminaría convirtiéndose en una carta de cumpleaños para alguien tan importante para mí.  
    Me esforcé mucho para que saliera bien. Quería que tuviera alma.  
    Y funcionó. Porque gracias a Dios, me salió bien. Y por eso estás leyendo esto ahora. Porque salió bien. Porque lo hice con el corazón.</p>

    <p>Así que, aunque suene loco, esta es mi primera "programación":  
    Una carta que te escribo en código, pero desde el corazón.  
    Y sí, el motivo, la idea, la inspiración… fuiste vos.  
    Gracias por eso también. Porque, sin saberlo, me diste el impulso para crear algo que no solo vale por su parte técnica, sino por todo lo que lleva dentro.</p>

    <p>No espero respuesta. Solo quería que lo supieras.  
    Ojalá este mensaje te abrace por dentro, te saque una sonrisa suave, o incluso una lágrima de esas que limpian el alma.  
    Donde sea que estés… que la vida te trate bonito. Siempre.</p>

    <div class="firma">Feliz cumpleaños, Thais.✨<br>ATT, Maycol.i🌹</div>

    <div class="rosa">
      <img src="A_digital_graphic_displays_a_heartfelt_letter_dedi.png" alt="Rosa" />
    </div>
  </div>
</div>

<iframe width="0" height="0" src="https://www.youtube.com/embed/U1FcG5VZ5bY?autoplay=1" frameborder="0" allow="autoplay"></iframe>

<script>
  function verificarPIN() {
    const pin = document.getElementById('pinInput').value;
    if (pin === '4334') {
      document.getElementById('pinPage').style.display = 'none';
      document.getElementById('cartaPage').style.display = 'flex';
    } else {
      alert('PIN incorrecto');
    }
  }
</script>

</body>
</html>

