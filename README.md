
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PIZZERÍA MDQ</title>
<style>
body{margin:0;font-family:Arial;background:#0a0a0a;color:#fff;padding-bottom:80px}
header{text-align:center;padding:20px;background:#000}
header img{width:80px;height:80px;border-radius:50%}
header h1{color:#FFD700;margin:10px 0;font-size:28px}
header p{color:#ccc;margin:5px 0}
.menu-btns{display:flex;gap:10px;justify-content:center;padding:15px;background:#111}
.menu-btns button{padding:10px 20px;border:2px solid #e63946;background:transparent;color:#fff;border-radius:20px;font-weight:bold}
.menu-btns button.active{background:#e63946}
.categoria{padding:15px}
.categoria h2{color:#FFD700;border-bottom:2px solid #e63946;padding-bottom:5px}
.producto{background:#1a1a1a;margin:10px 0;padding:10px;border-radius:10px;display:flex;gap:10px;align-items:center}
.producto img{width:70px;height:70px;border-radius:8px;object-fit:cover}
.producto-info{flex:1}
.producto-info h3{margin:0;font-size:16px}
.producto-info p{margin:5px 0;font-size:12px;color:#aaa}
.precio{font-weight:bold;color:#FFD700}
.btn-agregar{background:#e63946;border:none;color:#fff;padding:8px 12px;border-radius:8px;font-weight:bold}
.carrito{position:fixed;bottom:0;left:0;right:0;background:#e63946;padding:15px;display:flex;justify-content:space-between;align-items:center}
.carrito button{background:#25D366;border:none;color:#fff;padding:12px 20px;border-radius:20px;font-weight:bold;font-size:16px}
</style>
</head>
<body>

<header>
<img src="https://i.imgur.com/8Km8a8a.jpg" alt="logo">
<h1>🍕 PIZZERÍA MDQ</h1>
<p>Envíos en 30min | Mar del Plata</p>
</header>

<div class="menu-btns">
<button onclick="mostrar('pizzas')" class="active">Pizzas</button>
<button onclick="mostrar('empanadas')">Empanadas</button>
<button onclick="mostrar('bebidas')">Bebidas</button>
</div>

<div id="pizzas" class="categoria">
<h2>PIZZAS</h2>
<div class="producto">
<img src="https://i.imgur.com/5oZgY8m.jpg">
<div class="producto-info">
<h3>Muzzarella</h3><p>Queso muzzarella y aceitunas</p>
<span class="precio">$12.000</span>
</div>
<button class="btn-agregar" onclick="agregar('Muzzarella',12000)">Agregar</button>
</div>

<div class="producto">
<img src="https://i.imgur.com/5oZgY8m.jpg">
<div class="producto-info">
<h3>Napolitana</h3><p>Muzzarella, tomate y ajo</p>
<span class="precio">$13.000</span>
</div>
<button class="btn-agregar" onclick="agregar('Napolitana',13000)">Agregar</button>
</div>

<div class="producto">
<img src="https://i.imgur.com/5oZgY8m.jpg">
<div class="producto-info">
<h3>Fugazzeta</h3><p>Cebolla y muzzarella</p>
<span class="precio">$14.000</span>
</div>
<button class="btn-agregar" onclick="agregar('Fugazzeta',14000)">Agregar</button>
</div>

<div class="producto">
<img src="https://i.imgur.com/5oZgY8m.jpg">
<div class="producto-info">
<h3>Jamón y Morrones</h3><p>Jamón cocido y morrones</p>
<span class="precio">$14.000</span>
</div>
<button class="btn-agregar" onclick="agregar('Jamón y Morrones',14000)">Agregar</button>
</div>
</div>

<div id="empanadas" class="categoria" style="display:none">
<h2>EMPANADAS</h2>
<div class="producto">
<img src="https://i.imgur.com/2nCt3Sbl.jpg">
<div class="producto-info">
<h3>Carne Suave x12</h3><p>Docena de empanadas de carne</p>
<span class="precio">$14.000</span>
</div>
<button class="btn-agregar" onclick="agregar('Carne Suave x12',14000)">Agregar</button>
</div>
</div>

<div id="bebidas" class="categoria" style="display:none">
<h2>BEBIDAS</h2>
<div class="producto">
<img src="https://i.imgur.com/3ZQ7yYl.jpg">
<div class="producto-info">
<h3>Coca Cola 1,5 L</h3><p>Gaseosa bien fría</p>
<span class="precio">$3.500</span>
</div>
<button class="btn-agregar" onclick="agregar('Coca Cola 1,5L',3500)">Agregar</button>
</div>
</div>

<div class="carrito">
<div>
<div>Total: $<span id="total">0</span></div>
<div id="resumen" style="font-size:12px"></div>
</div>
<button onclick="enviarWhatsApp()">WhatsApp</button>
</div>

<script>
let carrito = [];
let total = 0;
function mostrar(cat){
document.querySelectorAll('.categoria').forEach(c=>c.style.display='none');
document.getElementById(cat).style.display='block';
document.querySelectorAll('.menu-btns button').forEach(b=>b.classList.remove('active'));
event.target.classList.add('active');
}
function agregar(nombre, precio){
carrito.push({nombre, precio});
total += precio;
actualizarCarrito();
}
function actualizarCarrito(){
document.getElementById('total').innerText = total.toLocaleString();
document.getElementById('resumen').innerText = carrito.map(i=>i.nombre).join(', ');
}
function enviarWhatsApp(){
if(carrito.length==0){alert('Agregá algo al carrito');return}
let mensaje = 'Hola! Quiero pedir:%0A';
carrito.forEach(i=>{mensaje += '- '+i.nombre+' $'+i.precio.toLocaleString()+'%0A'});
mensaje += '%0ATotal: $'+total.toLocaleString();
window.open('https://wa.me/549XXXXXXXXXX?text='+mensaje,'_blank');
}
</script>
</body>
</html>
