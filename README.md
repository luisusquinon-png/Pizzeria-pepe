
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Don Hernancios - Menú Online</title>
  <style>
    *{margin:0;padding:0;box-sizing:border-box;font-family:Arial,sans-serif}
    body{background:#0a0a0a;color:#fff;padding-bottom:80px}
    header{position:sticky;top:0;background:#000;padding:15px;text-align:center;z-index:10;border-bottom:2px solid #d32f2f}
    header img{width:80px;height:80px;border-radius:50%;object-fit:cover;margin-bottom:5px}
    header h1{font-size:1.5em;color:#ffeb3b}
    header p{font-size:0.9em;color:#ccc}
    .categorias{display:flex;gap:10px;overflow-x:auto;padding:10px;background:#111;position:sticky;top:110px;z-index:9}
    .cat-btn{background:#222;border:1px solid #d32f2f;color:#fff;padding:8px 15px;border-radius:20px;white-space:nowrap;font-size:0.9em}
    .cat-btn.active{background:#d32f2f}
    .seccion{padding:20px 15px;display:none} /* Ocultas por defecto */
    .seccion.activa{display:block} /* Solo se muestra la activa */
    .seccion h2{color:#ffeb3b;margin-bottom:15px;font-size:1.3em;border-bottom:2px solid #d32f2f;padding-bottom:5px}
    .producto{background:#1a1a1a;border-radius:12px;padding:12px;margin-bottom:12px;display:flex;gap:12px;border:1px solid #333}
    .producto img{width:80px;height:80px;border-radius:8px;object-fit:cover}
    .info{flex:1}
    .info h3{font-size:1.1em;margin-bottom:3px}
    .info p{font-size:0.85em;color:#aaa;margin-bottom:5px}
    .precio{color:#4caf50;font-weight:bold;font-size:1.2em}
    .barra-pedido{position:fixed;bottom:0;left:0;right:0;background:#d32f2f;padding:12px;display:flex;justify-content:space-between;align-items:center}
    .btn-wpp{background:#25D366;color:#fff;padding:12px 20px;border-radius:25px;text-decoration:none;font-weight:bold;font-size:1em}
  </style>
</head>
<body>
  <header>
    <img src="https://images.unsplash.com/photo-1555396273-367ea4eb4db5?w=200" alt="logo">
    <h1>🍕 PIZZERÍA MDQ</h1>
    <p>Envíos en 30min | Mar del Plata</p>
  </header>

  <div class="categorias">
    <button class="cat-btn active" onclick="mostrar('pizzas')">Pizzas</button>
    <button class="cat-btn" onclick="mostrar('empanadas')">Empanadas</button>
    <button class="cat-btn" onclick="mostrar('bebidas')">Bebidas</button>
  </div>

  <div id="pizzas" class="seccion activa">
    <h2>PIZZAS</h2>
    <div class="producto">
      <img src="https://images.unsplash.com/photo-1574071318508-1cdbab80d002?w=200" alt="muzzarella">
      <div class="info"><h3>Muzzarella</h3><p>Salsa, muzzarella y orégano</p><p class="precio">$13.500</p></div>
    </div>
    <div class="producto">
      <img src="https://images.unsplash.com/photo-1628840042765-356cda07504e?w=200" alt="napo">
      <div class="info"><h3>Napolitana</h3><p>Tomate, ajo, muzzarella y albahaca</p><p class="precio">$15.000</p></div>
    </div>
  </div>

  <div id="empanadas" class="seccion">
    <h2>EMPANADAS</h2>
    <div class="producto">
      <img src="https://images.unsplash.com/photo-1613564834361-90e7c9c76bcb?w=200" alt="empanada">
      <div class="info"><h3>Carne Suave x12</h3><p>Docena de empanadas de carne</p><p class="precio">$14.000</p></div>
    </div>
  </div>

  <div id="bebidas" class="seccion">
    <h2>BEBIDAS</h2>
    <div class="producto">
      <img src="https://images.unsplash.com/photo-1553456558-aff63285bdd1?w=200" alt="coca">
      <div class="info"><h3>Coca Cola 1.5L</h3><p>Gaseosa bien fría</p><p class="precio">$3.500</p></div>
    </div>
  </div>

  <div class="barra-pedido">
    <span><b>Hace tu pedido</b></span>
    <a href="https://wa.me/5492230000000?text=Hola! Quiero hacer un pedido" class="btn-wpp">WhatsApp</a>
  </div>

<script>
function mostrar(id){
  document.querySelectorAll('.seccion').forEach(s=>s.classList.remove('activa'));
  document.querySelectorAll('.cat-btn').forEach(b=>b.classList.remove('active'));
  document.getElementById(id).classList.add('activa');
  event.target.classList.add('active');
}
</script>
</body>
</html>
