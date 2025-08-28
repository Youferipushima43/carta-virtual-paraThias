<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Carta para Thais</title>
  <style>
    body {
      font-family: 'Georgia', serif;
      background: linear-gradient(135deg, #f8d3e6, #f9f9f9);
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }

    .container {
      width: 90%;
      max-width: 700px;
      background: #fff;
      padding: 25px;
      border-radius: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
      display: none;
      animation: fadeIn 1s ease;
    }

    .card h2 {
      text-align: center;
      color: #b30059;
    }

    .card p {
      text-align: justify;
      line-height: 1.7;
      margin: 12px 0;
      color: #333;
    }

    .pin-screen {
      text-align: center;
    }

    .pin-screen input {
      padding: 10px;
      font-size: 18px;
      border: 2px solid #b30059;
      border-radius: 8px;
      outline: none;
    }

    .pin-screen button {
      margin-top: 15px;
      padding: 10px 20px;
      font-size: 16px;
      background: #b30059;
      color: #fff;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }

    .pin-screen button:hover {
      background: #ff3385;
    }

    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }
  </style>
</head>
<body>

  <!-- Pantalla de PIN -->
  <div class="pin-screen" id="pinScreen">
    <h2>🔐 Ingresa el PIN</h2>
    <input type="password" id="pinInput" maxlength="4" placeholder="****">
    <br>
    <button onclick="checkPin()">Acceder</button>
    <p id="errorMsg" style="color:red; display:none;">PIN incorrecto ❌</p>
  </div>

  <!-- Carta -->
  <div class="container" id="cardContainer">
    <div class="card">
      <h2>Para Thais</h2>
      <p><b>Un mensaje único, desde el corazón 💌</b></p>

      <p>Hola Thais,</p>

      <p>
        Hoy, 29 de agosto, no quería dejar pasar el día sin decirte algo.
        No sé si este mensaje llegue a ti como una sorpresa, o como algo que esperabas sin esperarlo…
        Pero sinceramente, necesitaba escribirlo.
      </p>

      <p>
        Aunque la vida nos llevó por caminos distintos —y aunque nunca llegamos a tener algo más que lo que fue—,
        vos marcaste una parte muy especial de mi historia. No fuimos cercanos como otros, no compartimos mil momentos
        ni hicimos promesas, pero hubo algo… Algo real. Algo que aún hoy me acompaña.
      </p>

      <p>
        No sé si alguna vez lo sentiste como yo, pero me quedé con ese amor entre las manos, sin poder entregarlo del todo.
        No fue por falta de ganas ni de sentimientos, simplemente la vida tenía otros planes.
        Y aprendí a aceptarlo… aunque no fue fácil.
      </p>

      <p>
        Hoy es tu cumpleaños, y más allá de todo lo que no fue, quiero desearte lo mejor de lo mejor.
        Que este nuevo año de vida te abrace con luz, con calma, con personas que te hagan bien y momentos que te llenen el alma.
        Que la vida te cuide, te mime y te dé todo eso que soñás en silencio. Porque sí, lo merecés.
      </p>

      <p>
        Fuiste especial para mí, aunque nunca lo dijera en voz alta. Aunque todo quedara guardado en silencios, en miradas,
        o en palabras que nunca se animaron a salir. Y aún hoy, desde lejos, lo seguís siendo.
        Y aunque ya no estemos en contacto, aunque no sepa nada de vos, deseo de verdad que estés bien,
        que seas feliz, y que te cuides mucho.
      </p>

      <p>
        Gracias por haber existido en mi vida, así, tal como fuiste.  
        Gracias por lo que dejaste en mí, sin darte cuenta.  
        Gracias por inspirar en mí sentimientos tan puros, tan reales.
      </p>

      <p>
        Y antes de terminar… ¿Sabés algo curioso? Esta es la primera carta que escribo. Literalmente.  
        Fue parte de un proyecto que me dejaron en el instituto, donde estoy estudiando desarrollo de software.  
        Teníamos que crear algo en formato web… algo simple pero significativo, algo que combinara diseño con un mensaje personal.  
        Y pensé en vos.
      </p>

      <p>
        Nunca imaginé que una tarea del instituto terminaría convirtiéndose en una carta de cumpleaños para alguien tan importante para mí.
        Me esforcé mucho para que saliera bien. Quería que tuviera alma. Y funcionó.  
        Porque gracias a Dios, me salió bien. Y por eso estás leyendo esto ahora.  
        Porque salió bien. Porque lo hice con el corazón.
      </p>

      <p>
        Así que, aunque suene loco, esta es mi primera "programación":  
        Una carta que te escribo en código, pero desde el corazón.  
        Y sí, el motivo, la idea, la inspiración… fuiste vos.  
        Gracias por eso también. Porque, sin saberlo, me diste el impulso para crear algo que no solo vale por su parte técnica,
        sino por todo lo que lleva dentro.
      </p>

      <p>
        No espero respuesta. Solo quería que lo supieras.  
        Ojalá este mensaje te abrace por dentro, te saque una sonrisa suave, o incluso una lágrima de esas que limpian el alma.
      </p>

      <p><b>Feliz cumpleaños, Thais.</b><br>
      Donde sea que estés… que la vida te trate bonito. Siempre.</p>

      <p><i>ATT: Con cariño,</i><br>
      Maycol.i 🌹</p>
    </div>
  </div>

  <script>
    function checkPin() {
      const pin = document.getElementById("pinInput").value;
      const error = document.getElementById("errorMsg");
      if (pin === "4334") {
        document.getElementById("pinScreen").style.display = "none";
        document.getElementById("cardContainer").style.display = "block";
      } else {
        error.style.display = "block";
      }
    }
  </script>
</body>
</html>


