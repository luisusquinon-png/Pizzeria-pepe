
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pizzería MDQ</title>
<style>
body { margin:0; font-family: Arial; background:#111; color:white; }
header { display:flex; justify-content:space-between; align-items:center; padding:15px; background:#000; position:fixed; width:100%; top:0; z-index:10; }
header img { height:50px; }
.btn-pedir { background:#e63946; color:white; padding:10px 20px; border-radius:8px; text-decoration:none; font-weight:bold; }
.menu-icon { font-size:28px; cursor:pointer; }

.hero { height:70vh; background-size:cover; background-position:center; display:flex; flex-direction:column; justify-content:center; align-items:center; text-align:center; margin-top:80px; }
.hero h1 { font-size:40px; text-shadow:2px 2px 4px black; }
.hero p { font-size:18px; text-shadow:2px 2px 4px black; }
.btn-rojo { background:#e63946; color:white; padding:15px 40px; border-radius:10px; text-decoration:none; font-weight:bold; font-size:20px; margin-top:20px; }

.categoria { background:white; color:black; margin:20px; padding:20px; border-radius:12px; display:flex; justify-content:space-between; align-items:center; }
.categoria h2 { border-bottom:3px solid #e63946; display:inline-block; }
.categoria img { width:150px; border-radius:10px; }
</style>
</head>
<body>

<header>
  <img src="logo.jpg" alt="logo">
  <a href="#menu" class="btn-pedir">PEDIR AHORA</a>
  <div class="menu-icon">☰</div>
</header>

<div class="hero" id="hero">
  <h1>Pizza a la Piedra<br>con Sabor MDQ</h1>
  <p>Y queda mejor con una birra bien fría</p>
  <a href="#menu" class="btn-rojo">PEDIR AHORA</a>
</div>

<div id="menu" style="padding:20px; background:#f2f2f2;">
  <h1 style="text-align:center; color:#000;">¿QUÉ TENÉS GANAS?</h1>

  <div class="categoria">
    <div>
      <h2>PIZZA NAPOLITANA</h2>
      <p>Tomate, ajo, orégano y queso. Clásica italiana</p>
      <p style="font-weight:bold; color:#e63946;">$8500</p>
    </div>
    <img src="napolitana.jpg" alt="napolitana">
  </div>

  <div class="categoria">
    <div>
      <h2>MUZZARELLA</h2>
      <p>La de siempre. Mucho queso y aceitunas</p>
      <p style="font-weight:bold; color:#e63946;">$8000</p>
    </div>
    <img src="muzzarella.jpg" alt="muzzarella">
  </div>

  <div class="categoria">
    <div>
      <h2>BEBIDAS</h2>
      <p>Gaseosas, agua y birras bien frías</p>
      <p style="font-weight:bold; color:#e63946;">$2500</p>
    </div>
    <img src="cocacola.jpg" alt="bebida">
  </div>
</div>

<script>
// CARRUSEL DE FONDO
let imagenes = ['pizza.jpg', 'cocacola.jpg', 'logo.jpg'];
let i = 0;
setInterval(()=>{
  document.getElementById('hero').style.backgroundImage = `linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url(${imagenes[i]})`;
  i = (i + 1) % imagenes.length;
}, 3000); // cambia cada 3 segundos
</script>

</body>
</html>
