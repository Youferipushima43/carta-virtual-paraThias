<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Mensaje Especial 💌</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      background-color: #fff0f5;
      color: #333;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .bloqueo {
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: #ffe6f0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      z-index: 9999;
    }

    .bloqueo input {
      padding: 10px;
      font-size: 18px;
      border: 1px solid #ccc;
      border-radius: 10px;
      text-align: center;
    }

    .bloqueo button {
      margin-top: 10px;
      padding: 10px 20px;
      font-size: 16px;
      background-color: #d63384;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }

    .container {
      max-width: 360px;
      padding: 20px;
      box-sizing: border-box;
      display: none;
    }

    header {
      text-align: center;
      margin-bottom: 10px;
    }

    header h1 {
      font-size: 24px;
      color: #d63384;
      margin: 10px 0 0;
    }

    header p {
      font-size: 14px;
      color: #555;
    }

    #music-section iframe {
      width: 100%;
      height: 60px;
      border: none;
      margin: 10px 0;
    }

    .message-content {
      background-color: #fff;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      font-size: 15px;
      line-height: 1.6;
      white-space: pre-line;
    }

    .firma {
      margin-top: 20px;
      text-align: right;
      font-weight: bold;
      color: #b30059;
    }

    .rosa {
      text-align: center;
      margin-top: 15px;
    }

    .rosa img {
      width: 100px;
      border-radius: 8px;
    }
  </style>
</head>
<body>

<!-- Pantalla de PIN -->
<div class="bloqueo" id="bloqueo">
  <h2>🔒 Ingresa el PIN</h2>
  <input type="password" id="pin" placeholder="Escribe el PIN..." />
  <button onclick="verificarPin()">Desbloquear</button>
</div>

<!-- Contenido real oculto -->
<div class="container" id="contenidoReal">
  <header>
    <h1>Para Thais</h1>
    <p>Un mensaje especial, solo para ti 💌</p>
  </header>

  <!-- Música automática -->
  <div id="music-section">
    <iframe src="https://archive.org/embed/anuel-aa-secreto-ft.-karol-g" allow="autoplay"></iframe>
  </div>

  <section class="message-content">
    <p>Hola Thais,</p>

Hoy, 29 de agosto, no quería dejar pasar el día sin decirte algo.  
No sé si este mensaje llegue a ti como una sorpresa, o como algo que esperabas sin esperarlo…  
Pero sinceramente, necesitaba escribirlo.  

Aunque la vida nos llevó por caminos distintos —y aunque nunca llegamos a tener algo más que lo que fue—, vos marcaste una parte muy especial de mi historia.  
No fuimos cercanos como otros, no compartimos mil momentos ni hicimos promesas, pero hubo algo…  

Algo real. Algo que aún hoy me acompaña.  

(...texto de tu carta aquí, lo dejé tal cual lo pusiste...)

    <div class="firma">Feliz cumpleaños, Thais.✨<br>ATT, Maycol.i🌹</div>
  </section>

  <div class="rosa">
    <img src="https://raw.githubusercontent.com/AnteroTeobaldo/BCodeProyectos/main/dia_novia_1_bcode/rosa_bonita.png" alt="Rosa para Thais">
  </div>
</div>

<script>
  function verificarPin() {
    const claveCorrecta = "4334";
    const pinIngresado = document.getElementById("pin").value;

    if (pinIngresado === claveCorrecta) {
      document.getElementById("bloqueo").style.display = "none";
      document.getElementById("contenidoReal").style.display = "block";
    } else {
      alert("PIN incorrecto. Intenta de nuevo.");
    }
  }
</script>

</body>
</html>


