<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>💌 Para Thais</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #000;
      color: pink;
      font-family: 'Georgia', 'Times New Roman', serif;
      overflow-x: hidden;
    }
    h1 {
      text-align: center;
      margin-top: 20px;
      font-size: 2.2em;
      color: hotpink;
    }
    .container {
      display: none;
      padding: 30px;
      max-width: 800px;
      margin: auto;
      font-size: 1.3em;
      line-height: 1.8em;
      text-align: justify;
    }
    .firma {
      margin-top: 40px;
      text-align: right;
      font-weight: bold;
    }
    .teclado {
      text-align: center;
      margin-top: 50px;
    }
    .pantalla {
      background: #111;
      color: #0f0;
      padding: 10px;
      margin-bottom: 10px;
      width: 150px;
      margin: auto;
      font-family: monospace;
      font-size: 1.5em;
    }
    .boton {
      padding: 10px 20px;
      margin: 5px;
      font-size: 1.2em;
      background: #222;
      color: white;
      border: 1px solid pink;
      cursor: pointer;
    }
    .boton:hover {
      background: pink;
      color: black;
    }
    .rosa {
      display: block;
      margin: 40px auto 20px;
      width: 220px;
      border-radius: 20px;
      box-shadow: 0 0 15px pink;
    }
    .corazon {
      position: fixed;
      top: -20px;
      font-size: 20px;
      color: pink;
      animation: caer 5s linear infinite;
      user-select: none;
    }
    @keyframes caer {
      to {
        transform: translateY(100vh);
      }
    }
    iframe {
      display: block;
      margin: 30px auto 10px;
      border: none;
      border-radius: 12px;
    }
  </style>
</head>
<body>

<h1>💌 Para Thais</h1>

<div class="teclado">
  <div class="pantalla" id="pantalla">____</div>
  <div>
    <button class="boton" onclick="agregar('1')">1</button>
    <button class="boton" onclick="agregar('2')">2</button>
    <button class="boton" onclick="agregar('3')">3</button><br>
    <button class="boton" onclick="agregar('4')">4</button>
    <button class="boton" onclick="agregar('5')">5</button>
    <button class="boton" onclick="agregar('6')">6</button><br>
    <button class="boton" onclick="agregar('7')">7</button>
    <button class="boton" onclick="agregar('8')">8</button>
    <button class="boton" onclick="agregar('9')">9</button><br>
    <button class="boton" onclick="borrar()">←</button>
    <button class="boton" onclick="agregar('0')">0</button>
    <button class="boton" onclick="verificar()">✔</button>
  </div>
</div>

<div class="container" id="contenido">
  <p>Hola Thais,</p>  

  Hoy, 29 de agosto, no quería dejar pasar el día sin decirte algo.  
  No sé si este mensaje llegue a ti como una sorpresa, o como algo que esperabas sin esperarlo…  
  Pero sinceramente, necesitaba escribirlo.  

  Aunque la vida nos llevó por caminos distintos —y aunque nunca llegamos a tener algo más que lo que fue—, vos marcaste una parte muy especial de mi historia.  
  No fuimos cercanos como otros, no compartimos mil momentos ni hicimos promesas, pero hubo algo…  
  Algo real. Algo que aún hoy me acompaña.  

  No sé si alguna vez lo sentiste como yo, pero me quedé con ese amor entre las manos, sin poder entregarlo del todo.  
  No fue por falta de ganas ni de sentimientos, simplemente la vida tenía otros planes. Y aprendí a aceptarlo… aunque no fue fácil.  

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
  Fue parte de un proyecto que me dejaron en el instituto, donde estoy estudiando desarrollo de software.  
  Teníamos que crear algo en formato web… algo simple pero significativo, algo que combinara diseño con un mensaje personal. Y pensé en vos.  

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
  <div class="firma">Feliz cumpleaños, Thais. ✨<br>ATT, Maycol.i 🌹</div>

  <img class="rosa" src="https://i.pinimg.com/originals/27/0f/2b/270f2bb4f946280edfb5270506d09ef4.jpg" alt="Rosa" />

  <iframe width="100%" height="180" src="https://www.youtube.com/embed/vyUo9VjrxvI?autoplay=1&loop=1&playlist=vyUo9VjrxvI" allow="autoplay; encrypted-media"></iframe>
</div>

<script>
  let clave = "4334";
  let input = "";

  function agregar(num) {
    if (input.length < 4) {
      input += num;
      document.getElementById("pantalla").textContent = input.padEnd(4, "_");
    }
  }

  function borrar() {
    input = input.slice(0, -1);
    document.getElementById("pantalla").textContent = input.padEnd(4, "_");
  }

  function verificar() {
    if (input === clave) {
      document.querySelector(".teclado").style.display = "none";
      document.getElementById("contenido").style.display = "block";
    } else {
      input = "";
      document.getElementById("pantalla").textContent = "____";
    }
  }

  // Corazones animados
  setInterval(() => {
    const corazon = document.createElement("div");
    corazon.className = "corazon";
    corazon.style.left = Math.random() * 100 + "vw";
    corazon.style.animationDuration = 3 + Math.random() * 2 + "s";
    corazon.textContent = "💖";
    document.body.appendChild(corazon);
    setTimeout(() => corazon.remove(), 5000);
  }, 300);
</script>

</body>
</html>
