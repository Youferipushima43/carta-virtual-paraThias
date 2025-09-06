<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Para Ti – Te Amo</title>
<style>
/* ====== Variables & Reset ====== */
:root{
  --bg:#0a0a0f;
  --panel:#0f1117;
  --panel-2:#11131b;
  --fg:#e7ecff;
  --accent:#ff2b4f;          /* heart */
  --accent-2:#ff9aa9;        /* heart light */
  --card:#fffaf0;            /* tarjeta */
  --sun-petal:#ffd74a;       /* pétalos */
  --sun-center:#6b3f14;      /* centro girasol */
  --sun-ring:#c17e2a;        /* anillo */
  --shadow:#00000030;
}
*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  font-family: ui-sans-serif,system-ui,-apple-system,Segoe UI,Roboto,Inter,Arial;
  color:var(--fg);
  background: radial-gradient(1200px 700px at 70% -10%, #e5156a20 0, transparent 60%),
              radial-gradient(900px 500px at 10% 110%, #e5156a18 0, transparent 60%),
              var(--bg);
  overflow-x:hidden;
}

/* ====== Hearts floating background ====== */
.hearts{position:fixed; inset:0; pointer-events:none; z-index:0; overflow:hidden;}
.heart{
  position:absolute; font-size:18px; opacity:.7; filter:blur(.2px);
  animation:float linear forwards; color:var(--accent);
}
@keyframes float{
  from{transform:translateY(110vh) scale(.7) rotate(0deg); opacity:.0}
  10%{opacity:.85}
  to{transform:translateY(-15vh) scale(1.1) rotate(360deg); opacity:0}
}

/* ====== Layout ====== */
.wrap{
  position:relative; z-index:1; min-height:100%;
  display:grid; place-items:center; padding:32px 16px;
}
.grid{
  width:min(1100px, 96vw);
  display:grid; gap:22px;
  grid-template-columns: 1.1fr .9fr;
}
@media (max-width:900px){
  .grid{grid-template-columns:1fr}
}

/* ====== Card ====== */
.card{
  background:linear-gradient(180deg,#fffffc 0%, #fff7df 100%);
  border-radius:24px; padding:18px; box-shadow:0 30px 80px var(--shadow);
  position:relative; overflow:hidden;
}
.card::before,
.card::after{
  content:""; position:absolute; inset:0; pointer-events:none;
  background:
    radial-gradient(600px 200px at 10% -10%, #ffd1e41c 0, transparent 60%),
    radial-gradient(220px 90px at 95% 20%, #ffd1e41c 0, transparent 60%);
}
.card-inner{
  border-radius:16px; background:var(--card);
  padding:20px; aspect-ratio:1/1; position:relative; overflow:hidden;
  box-shadow: inset 0 0 0 2px #00000010;
}
.title{
  position:absolute; inset:18px 18px auto 18px;
  text-align:center; font-weight:800; letter-spacing:.6px;
  color:#1d1a10; text-shadow:0 2px 0 #ffffff90;
  font-size: clamp(20px, 2.4vw, 30px);
}
.ribbon{
  position:absolute; width:120%; height:18px; left:-10%; top:50%;
  background:linear-gradient(90deg,#ff8aa5,#ff2b4f,#ff8aa5);
  filter:blur(14px); opacity:.12;
  transform:rotate(-8deg);
}

/* ====== Sunflowers (SVG scaled) ====== */
.sunflowers{
  position:absolute; inset:0; display:block; width:100%; height:100%;
}
svg{width:100%; height:100%}
.shadow{
  filter: drop-shadow(0 6px 10px #00000035);
}

/* ====== Code panel ====== */
.panel{
  background:linear-gradient(180deg,var(--panel) 0%, var(--panel-2) 100%);
  border-radius:22px; padding:18px 18px 14px;
  box-shadow:0 30px 80px var(--shadow);
  position:relative;
}
.panel .header{
  display:flex; align-items:center; gap:8px; padding:4px 6px 12px; opacity:.9;
  font-size:14px; color:#c7d2fe;
}
.dot{width:10px;height:10px;border-radius:50%;}
.dot.red{background:#ff6a6a}
.dot.yellow{background:#ffd166}
.dot.green{background:#61d975}
.filename{margin-left:auto; opacity:.8}
pre{margin:0; overflow:auto; padding:14px; line-height:1.5; border-radius:12px;
  background: #0b0d13; border:1px solid #ffffff10; }
code{font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace; font-size:13px;}

/* ====== Buttons / micro UI ====== */
.actions{display:flex; gap:12px; margin-top:12px}
.btn{
  border:none; border-radius:999px; padding:10px 16px; font-weight:700;
  background:linear-gradient(180deg,#ff6a8b,#ff2b4f);
  color:white; letter-spacing:.3px; cursor:pointer;
  box-shadow:0 10px 24px #ff2b4f55; transition:transform .15s ease;
}
.btn:active{transform:translateY(1px) scale(.99)}

/* ====== Sparkles ====== */
.sparkle{position:absolute; width:6px; height:6px; border-radius:50%; background:#fff;
  box-shadow:0 0 14px 4px #ffffffaa; pointer-events:none; animation:s-up .9s ease-out forwards;}
@keyframes s-up{
  from{transform:translateY(0) scale(.8); opacity:1}
  to{transform:translateY(-70px) scale(0); opacity:0}
}

/* ====== Nice entrance ====== */
.reveal{
  opacity:0; transform:translateY(12px) scale(.98);
  animation:reveal .6s cubic-bezier(.2,.9,.2,1) .1s forwards;
}
.reveal:nth-child(2){animation-delay:.2s}
@keyframes reveal{
  to{opacity:1; transform:translateY(0) scale(1)}
}
</style>
</head>
<body>

<!-- Floating hearts background -->
<div class="hearts" id="hearts"></div>

<div class="wrap">
  <div class="grid">
    <!-- ===== Left: Love card ===== -->
    <section class="card reveal">
      <div class="card-inner">
        <div class="title">PARA TI – TE AMO</div>
        <div class="ribbon"></div>

        <!-- Sunflowers SVG -->
        <div class="sunflowers">
          <svg viewBox="0 0 1000 1000" aria-label="Girasoles">
            <!-- bouquet -->
            <g class="shadow">
              <!-- stems -->
              <path d="M520 640 C520 640 520 900 520 980" stroke="#1f8a4a" stroke-width="16" fill="
              
