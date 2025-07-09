<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Carta para Thaiss</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Íconos de Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css" integrity="sha512-sVLZgxFka0EzYxfG2q7k+MuWwYPmbgG9WLyfG1BZfQYf8Lf1RuYqH12UbhxCE0x4Mea9KDvTo1n4+UkecU2zEA==" crossorigin="anonymous" referrerpolicy="no-referrer" />
  <style>
    body {
      margin: 0;
      padding: 40px 20px;
      background: linear-gradient(135deg, #f6d365 0%, #fda085 100%);
      font-family: 'Arial', sans-serif;
      color: #333;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }

    .card {
      background: white;
      border-radius: 20px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.2);
      padding: 40px 30px;
      max-width: 600px;
      width: 100%;
      text-align: center;
      animation: fadeIn 1.2s ease;
    }

    h1 {
      color: #ff5e62;
      font-size: 28px;
      margin-bottom: 20px;
    }

    p {
      font-size: 18px;
      line-height: 1.6;
    }

    .signature {
      margin-top: 40px;
      font-style: italic;
      color: #555;
      font-size: 16px;
    }

    .heart {
      font-size: 30px;
      color: red;
      margin-top: 30px;
      animation: beat 1.5s infinite;
    }

    @keyframes beat {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Querida Thaiss</h1>
    <p>
      Aunque ya no hablemos ni sepamos nada el uno del otro,<br>
      quiero que sepas que aún te amo.<br><br>
      No hay día que no piense en ti y en todo lo que vivimos.<br><br>
      Esta carta no busca cambiar las cosas,<br>
      solo quería expresarte lo que siento<br>
      y desearte lo mejor siempre.
    </p>
    <div class="signature">
      Con cariño,<br>
      Maycol
    </div>
    <div class="heart">
      <i class="fas fa-heart"></i>
    </div>
  </div>
</body>
</html>
