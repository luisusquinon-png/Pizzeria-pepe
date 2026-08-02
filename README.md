
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pizzería Pepe - Pizza a la Piedra</title>
<style>
body { margin:0; font-family: Arial; background:#FFF8E7; color:#222; }
header { display:flex; justify-content:space-between; align-items:center; padding:15px; background:#000; position:fixed; width:100%; top:0; z-index:10; box-sizing: border-box; }
header img { height:50px; }
.btn-pedir { background:#e63946; color:white; padding:10px 20px; border-radius:8px; text-decoration:none; font-weight:bold; }
.menu-icon { font-size:28px; cursor:pointer; color:white; }
.show { display:block !important; }

.hero { 
  height:45vh; 
  background-size:cover; 
  background-position:center; 
  display:flex; flex-direction:column; justify-content:center; align-items:center; text-align:center; 
  margin-top:80px;
  background-color: #FFF8E7; 
  transition: background-image 1s ease-in-out;
}
.hero h1 { font-size:32px; text-shadow:2px 2px 4px rgba(0,0,0,0.7); color:white; margin:10px; }
.hero p { font-size:16px; text-shadow:2px 2px 4px rgba(0,0,0,0.7); color:white; margin:10px; }
.btn-rojo { background:#e63946; color:white; padding:15px 40px; border-radius:10px; text-decoration:none; font-weight:bold; font-size:20px; margin-top:20px; }

#menu { padding:20px; }
#menu h1 { text-align:center; color:#000; }
.categoria { background:white; color:black; margin:20px; padding:20px; border-radius:12px; display:flex; justify-content:space-between; align-items:center; box-shadow: 0 2px 8px rgba(0,0,0,0.1); text-decoration:none; }
.categoria h2 { border-bottom:3px solid #e63946; display:inline-block; margin:0 0 10px 0; }
.categoria img { width:120px; border-radius:10px; }
</style>
</head>
<body>

<header>
  <img src="logo.jpg" alt="logo">
  <a href="#menu" class="btn-pedir">PEDIR AHORA</a>
  <div class="menu-icon" onclick="document.getElementById('menu-desplegable').classList.toggle('show')">☰</div>
</header>

<div id="menu-desplegable" style="display:none; background:#000; position:fixed; top:80px; right:10px; padding:20px; border-radius:10px; z-index:11;">
  <a href="#seccion-pizzas" style="color:white; display:block; padding:10px; text-decoration:none;">Pizzas</a>
  <a href="#seccion-empanadas" style="color:white; display:block; padding:10px; text-decoration:none;">Empanadas</a>
  <a href="#seccion-bebidas" style="color:white; display:block; padding:10px; text-decoration:none;">Bebidas</a>
  <a href="https://wa.me/549223XXXXXXX" style="color:#e63946; display:block; padding:10px; text-decoration:none; font-weight:bold;">Pedir por WhatsApp</a>
</div>

<div class="hero" id="hero">
  <h1>Pizza a la Piedra<br>con Sabor MDQ</h1>
  <p>Y queda mejor con una birra bien fría</p>
  <a href="#menu" class="btn-rojo">PEDIR AHORA</a>
</div>

<div id="menu">
  <h1>¿QUÉ TENÉS GANAS?</h1>

  <a href="#seccion-pizzas" style="text-decoration:none; color:black;">
    <div class="categoria">
      <div>
        <h2>PIZZAS</h2>
        <p>Clásicas y especiales hechas en horno a leña</p>
      </div>
      <img src="napolitana.jpg" alt="pizza">
    </div>
  </a>

  <a href="#seccion-empanadas" style="text-decoration:none; color:black;">
    <div class="categoria">
      <div>
        <h2>EMPANADAS</h2>
        <p>Para picar y compartir entre todos</p>
      </div>
      <img src="empanadas.jpg" alt="empanadas">
    </div>
  </a>

  <a href="#seccion-bebidas" style="text-decoration:none; color:black;">
    <div class="categoria">
      <div>
        <h2>BEBIDAS</h2>
        <p>Frías y listas para acompañar tu pizza</p>
      </div>
      <img src="bebidas.jpg" alt="bebida">
    </div>
  </a>
</div>

<!-- SECCIONES -->
<div id="seccion-pizzas" style="padding:40px 20px; background:#FFF8E7;">
  <h2 style="text-align:center; color:#e63946; font-size:32px;">PIZZAS A ELECCIÓN</h2>
  
  <div class="categoria">
    <div>
      <h2>PIZZA NAPOLITANA</h2>
      <p>Tomate, ajo, orégano y mucho queso. Clásica italiana</p>
      <p style="font-weight:bold; color:#e63946; font-size:20px;">$8500</p>
    </div>
    <img src="napolitana.jpg" alt="napolitana">
  </div>

  <div class="categoria">
    <div>
      <h2>MUZZARELLA</h2>
      <p>La de siempre. Mucho queso y aceitunas</p>
      <p style="font-weight:bold; color:#e63946; font-size:20px;">$8000</p>
    </div>
    <img src="muzzarella.jpg" alt="muzzarella">
  </div>
</div>

<div id="seccion-empanadas" style="padding:40px 20px; background:white;">
  <h2 style="text-align:center; color:#e63946; font-size:32px;">EMPANADAS</h2>
  
  <div class="categoria">
    <div>
      <h2>EMPANADAS HORNO</h2>
      <p>Carne, pollo, jamón y queso. La docena</p>
      <p style="font-weight:bold; color:#e63946; font-size:20px;">$12000 la docena</p>
    </div>
    <img src="empanadas.jpg" alt="empanadas">
  </div>
</div>

<div id="seccion-bebidas" style="padding:40px 20px; background:#FFF8E7;">
  <h2 style="text-align:center; color:#e63946; font-size:32px;">BEBIDAS BIEN FRÍAS</h2>
  
  <div class="categoria">
    <div>
      <h2>GASEOSAS 500ml</h2>
      <p>Coca, Fanta, Sprite</p>
      <p style="font-weight:bold; color:#e63946; font-size:20px;">$2500 c/u</p>
    </div>
    <img src="bebidas.jpg" alt="bebidas">
  </div>
</div>

<script>
// CARRUSEL DE FONDO
let imagenes = ['napolitana.jpg', 'picnic.jpg', 'empanadas.jpg', 'bebidas.jpg'];
let i = 0;
let hero = document.getElementById('hero');

hero.style.backgroundImage = `linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url(${imagenes[0]})`;

setInterval(()=>{
  i = (i + 1) % imagenes.length;
  hero.style.backgroundImage = `linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url(${imagenes[i]})`;
}, 3000);
</script>

</body>
</html>
