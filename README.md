<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pizzería Pepe - Pizza a la Piedra</title>
<style>
body { margin:0; font-family: Arial; background:#FFF8E7; color:#222; }
header { display:flex; justify-content:space-between; align-items:center; padding:15px; background:white; position:fixed; width:100%; top:0; z-index:10; box-sizing: border-box; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
header img { height:50px; }
.btn-pedir { background:#e63946; color:white; padding:10px 20px; border-radius:8px; text-decoration:none; font-weight:bold; }
.menu-icon { font-size:28px; cursor:pointer; color:#000; }
.show { display:block !important; }

.hero { 
  height:45vh; 
  background-size:cover; 
  background-position:center; 
  display:flex; flex-direction:column; justify-content:center; align-items:center; text-align:center; 
  margin-top:80px;
  background-color: #FFF8E7; 
  animation: cambiarFondo 12s infinite; /* AHORA ROTA SOLO */
}
.hero h1 { font-size:32px; text-shadow:2px 2px 8px rgba(0,0,0,0.7); color:white; margin:10px; }
.hero p { font-size:16px; text-shadow:2px 2px 6px rgba(0,0,0,0.7); color:white; margin:10px; }
.btn-rojo { background:#e63946; color:white; padding:15px 40px; border-radius:10px; text-decoration:none; font-weight:bold; font-size:20px; margin-top:20px; transition: 0.3s; }
.btn-rojo:hover { background-color: #c62828; transform: scale(1.05); }

#menu { padding:20px; }
#menu h1 { text-align:center; color:#000; }
.categoria { background:white; color:black; margin:20px; padding:20px; border-radius:12px; display:flex; justify-content:space-between; align-items:center; box-shadow: 0 2px 8px rgba(0,0,0,0.1); text-decoration:none; }

.producto { background:white; color:black; margin:20px; padding:15px; border-radius:12px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); display:flex; justify-content:space-between; align-items:center; gap:15px; }
.producto img { width:100px; height:100px; object-fit:cover; border-radius:10px; }
.producto-info { flex:1; }
.producto h3 { margin:5px 0; color:#000; }
.producto p { margin:5px 0; font-size:14px; }
.precio { font-weight:bold; color:#e63946; font-size:20px; }
.btn-wsp { background:#25D366; color:white; padding:10px 15px; border-radius:8px; text-decoration:none; font-weight:bold; white-space:nowrap; }

/* CONTACTO BLANCO */
#contacto { padding:40px 20px; background:white; color:#222; text-align:center; border-top: 3px solid #e63946; }
#contacto h2 { color:#e63946; }
iframe { width:100%; height:250px; border:0; border-radius:12px; margin-top:20px; }

/* ANIMACION DE LAS 3 FOTOS PARA EL FONDO */
@keyframes cambiarFondo {
 0% { 
   background-image: linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)), url('empanadas-banner.jpg'); /* FOTO NUEVA */
 }
 33% { 
   background-image: linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)), url('pizza-queso.jpg'); 
 }
 66% { 
   background-image: linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)), url('picnic.jpg'); 
 }
 100% { 
   background-image: linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)), url('empanadas-banner.jpg'); 
 }
}

/* Para celu */
@media (max-width: 768px) {
  .hero { height: 40vh; }
  .hero h1 { font-size: 1.6rem; }
}
</style>
</head>
<body>

<header>
  <img src="logo.jpg" alt="logo">
  <a href="#menu" class="btn-pedir">PEDIR AHORA</a>
  <div class="menu-icon" onclick="document.getElementById('menu-desplegable').classList.toggle('show')">☰</div>
</header>

<div id="menu-desplegable" style="display:none; background:white; position:fixed; top:80px; right:10px; padding:20px; border-radius:10px; z-index:11; box-shadow: 0 2px 10px rgba(0,0,0,0.2);">
  <a href="#seccion-pizzas" style="color:#000; display:block; padding:10px; text-decoration:none;">Pizzas</a>
  <a href="#seccion-empanadas" style="color:#000; display:block; padding:10px; text-decoration:none;">Empanadas</a>
  <a href="#seccion-bebidas" style="color:#000; display:block; padding:10px; text-decoration:none;">Bebidas</a>
  <a href="#contacto" style="color:#000; display:block; padding:10px; text-decoration:none;">Ubicación</a>
  <a href="https://wa.me/5491172441030" style="color:#e63946; display:block; padding:10px; text-decoration:none; font-weight:bold;">Pedir por WhatsApp</a>
</div>

<div class="hero" id="hero">
  <h1>Pizza a la Piedra<br>Hecha con Pasión</h1>
  <p>El mejor sabor de Mar del Plata en Pizza y Empanadas</p>
  <a href="#menu" class="btn-rojo">PEDIR AHORA</a>
</div>

<div id="menu">
  <h1>¿QUÉ TENÉS GANAS?</h1>
  <a href="#seccion-pizzas" style="text-decoration:none; color:black;"><div class="categoria"><div><h2>PIZZAS</h2><p>Clásicas y especiales</p></div><img src="pizza-queso.jpg" alt="pizza" width="120" style="border-radius:10px;"></div></a>
  <a href="#seccion-empanadas" style="text-decoration:none; color:black;"><div class="categoria"><div><h2>EMPANADAS</h2><p>Crujientes y doraditas</p></div><img src="empanada-criolla.jpg" alt="empanadas" width="120" style="border-radius:10px;"></div></a>
  <a href="#seccion-bebidas" style="text-decoration:none; color:black;"><div class="categoria"><div><h2>BEBIDAS</h2><p>Bien frías</p></div><img src="coca.jpg" alt="bebida" width="120" style="border-radius:10px;"></div></a>
</div>

<!-- PIZZAS -->
<div id="seccion-pizzas" style="padding:40px 20px; background:#FFF8E7;">
  <h2 style="text-align:center; color:#e63946; font-size:32px;">PIZZAS A ELECCIÓN</h2>
  <div class="producto"><img src="pizza-queso.jpg" alt="muzzarella"><div class="producto-info"><h3>MUZZARELLA</h3><p>Mucho queso y aceitunas</p><p class="precio">$8000</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Muzzarella%20$8000" class="btn-wsp">Pedir</a></div>
  <div class="producto"><img src="napolitana.jpg" alt="napolitana"><div class="producto-info"><h3>NAPOLITANA</h3><p>Tomate, ajo, orégano y mucho queso</p><p class="precio">$8500</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Napolitana%20$8500" class="btn-wsp">Pedir</a></div>
  <div class="producto"><img src="pizza-fugazzeta.jpg" alt="fugazzeta"><div class="producto-info"><h3>FUGAZZETA</h3><p>Cebolla, queso y orégano</p><p class="precio">$8200</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Fugazzeta%20$8200" class="btn-wsp">Pedir</a></div>
  <div class="producto"><img src="jamon-morrones.jpg" alt="jamon y morrones"><div class="producto-info"><h3>JAMÓN Y MORRONES</h3><p>Jamón cocido, morrones y queso</p><p class="precio">$8700</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Jamón%20y%20Morrones%20$8700" class="btn-wsp">Pedir</a></div>
</div>

<!-- EMPANADAS -->
<div id="seccion-empanadas" style="padding:40px 20px; background:white;">
  <h2 style="text-align:center; color:#e63946; font-size:32px;">EMPANADAS</h2>
  <div class="producto"><img src="empanada-criolla.jpg" alt="criolla"><div class="producto-info"><h3>EMPANADA CRIOLLA</h3><p>Carne cortada a cuchillo</p><p class="precio">$1000 c/u</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Empanada%20Criolla%20$1000" class="btn-wsp">Pedir</a></div>
  <div class="producto"><img src="empanada-saltena.jpg" alt="salteña"><div class="producto-info"><h3>EMPANADA SALTEÑA</h3><p>Carne, papa y huevo. Estilo norte</p><p class="precio">$1000 c/u</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Empanada%20Salteña%20$1000" class="btn-wsp">Pedir</a></div>
  <div class="producto"><img src="empanadas-doradas.jpg" alt="docena"><div class="producto-info"><h3>DOCENA HORNO</h3><p>Mezcladas: carne, pollo, jyq</p><p class="precio">$12000 la docena</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Docena%20de%20Empanadas%20$12000" class="btn-wsp">Pedir</a></div>
</div>

<!-- BEBIDAS -->
<div id="seccion-bebidas" style="padding:40px 20px; background:#FFF8E7;">
  <h2 style="text-align:center; color:#e63946; font-size:32px;">BEBIDAS BIEN FRÍAS</h2>
  <div class="producto"><img src="coca.jpg" alt="coca"><div class="producto-info"><h3>COCA-COLA 350ml</h3><p>Sabor original</p><p class="precio">$2500 c/u</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Coca-Cola%20$2500" class="btn-wsp">Pedir</a></div>
  <div class="producto"><img src="sprite.jpg" alt="sprite"><div class="producto-info"><h3>SPRITE 350ml</h3><p>Lima-limón</p><p class="precio">$2500 c/u</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Sprite%20$2500" class="btn-wsp">Pedir</a></div>
  <div class="producto"><img src="fanta.jpg" alt="fanta"><div class="producto-info"><h3>FANTA NARANJA 350ml</h3><p>Zero azúcares</p><p class="precio">$2500 c/u</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Fanta%20$2500" class="btn-wsp">Pedir</a></div>
  <div class="producto"><img src="pepsi.jpg" alt="pepsi"><div class="producto-info"><h3>PEPSI 350ml</h3><p>Clásica</p><p class="precio">$2500 c/u</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Pepsi%20$2500" class="btn-wsp">Pedir</a></div>
  <div class="producto"><img src="heladera-bebidas.jpg" alt="cerveza"><div class="producto-info"><h3>CERVEZA 473ml</h3><p>Quilmes, Brahma, Andes</p><p class="precio">$3500 c/u</p></div><a href="https://wa.me/5491172441030?text=Hola!%20Quiero%201%20Cerveza%20$3500" class="btn-wsp">Pedir</a></div>
</div>

<!-- CONTACTO -->
<div id="contacto">
  <h2>NUESTRA UBICACIÓN</h2>
  <p><b>Horario:</b> Lunes a Domingo de 19:00 a 00:00 hs</p>
  <p><b>Dirección:</b> Moreno, Buenos Aires, Argentina</p>
  <p><b>Tel:</b> 11 7244-1030</p>
  <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d26246.5!2d-58.7916!3d-34.6536!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x95bc9549f7b9b3e9%3A0x5e7b3b3b3b3b3b3b!2sMoreno%2C%20Provincia%20de%20Buenos%20Aires!5e0!3m2!1ses!2sar!4v1234567890" allowfullscreen="" loading="lazy"></iframe>
</div>

</body>
</html>
