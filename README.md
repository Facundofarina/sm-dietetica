<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SM Dietética</title>
<style>
body{margin:0;font-family:'Inter','Segoe UI',Arial,sans-serif;background:#eef3ef;color:#1f2d1f;line-height:1.6;}
header{background:linear-gradient(135deg,#1f7a3b,#5fcf80);color:white;padding:90px 20px;text-align:center;box-shadow:0 8px 25px rgba(0,0,0,.25);}
header img{width:140px;margin-bottom:15px;}
header h1{font-size:4.2rem;letter-spacing:4px;margin:0;font-weight:800;}
header p{font-size:1.4rem;margin-top:10px;}
.container{max-width:1200px;margin:auto;padding:60px 20px;}
.section{margin-bottom:80px;}
.section h2{text-align:center;font-size:2.6rem;color:#2f8f46;margin-bottom:40px;}
.about{max-width:800px;margin:auto;text-align:center;font-size:1.2rem;}

.price-table{width:100%;border-collapse:collapse;background:white;box-shadow:0 10px 28px rgba(0,0,0,.18);border-radius:16px;overflow:hidden;}
.price-table th,.price-table td{padding:16px;text-align:center;border-bottom:1px solid #eee;font-size:1.05rem;}
.price-table th{background:#2f8f46;color:white;font-size:1.1rem;}
.price-table tr:nth-child(even){background:#f7fbf8;} .price-table tr:hover{background:#e8f5ec;}
.price-table button{background:linear-gradient(135deg,#2f8f46,#5fcf80);color:white;border:none;padding:10px 22px;border-radius:25px;cursor:pointer;font-weight:600;box-shadow:0 4px 10px rgba(0,0,0,.2);}

.open-cart{position:fixed;top:20px;right:20px;background:linear-gradient(135deg,#ffb347,#ffcc33);border:none;padding:16px 26px;border-radius:35px;font-size:1.15rem;font-weight:700;cursor:pointer;box-shadow:0 6px 18px rgba(0,0,0,.35);z-index:1001;}

.cart-panel{position:fixed;top:0;right:-380px;width:360px;height:100%;background:#ffffff;box-shadow:-10px 0 28px rgba(0,0,0,.3);padding:24px;transition:.45s ease;z-index:1000;display:flex;flex-direction:column;border-top-left-radius:20px;border-bottom-left-radius:20px;}
body.cart-open .container{margin-right:380px;transition:.45s ease;}
body.cart-open header{margin-right:380px;transition:.45s ease;}
.cart-panel.active{right:0;}
.cart-panel h2{text-align:center;color:#2f8f46;}
.cart-items{flex:1;overflow-y:auto;margin:20px 0;}
.cart-item{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px;border-bottom:1px solid #eee;padding-bottom:8px;gap:8px;}
.qty-controls button{background:#2f8f46;color:white;border:none;padding:4px 8px;border-radius:6px;margin:0 4px;cursor:pointer;}
.remove{color:red;cursor:pointer;font-weight:bold;}
.total{font-weight:bold;font-size:1.2rem;text-align:center;margin-bottom:10px;}
.send-btn{background:linear-gradient(135deg,#2f8f46,#5fcf80);color:white;border:none;padding:18px;border-radius:40px;font-size:1.25rem;font-weight:700;cursor:pointer;box-shadow:0 6px 16px rgba(0,0,0,.3);}

.whatsapp{position:fixed;bottom:25px;right:25px;background:#25d366;color:white;padding:18px 22px;border-radius:50px;font-size:1.2rem;text-decoration:none;display:flex;align-items:center;gap:10px;box-shadow:0 6px 18px rgba(0,0,0,.3);} 
.whatsapp img{width:28px;height:28px;}

footer{margin-top:100px;background:#184d2a;color:white;text-align:center;padding:40px;font-size:1.05rem;}

@media(max-width:600px){
header h1{font-size:2.5rem;}
.section h2{font-size:2rem;}
.container{padding:30px 15px;}
.price-table th,.price-table td{font-size:.9rem;padding:10px;}
.cart-panel{width:100%;}
}
</style>
</head>
<body>

<header>
<img src="unnamed.jpg" alt="Logo SM Dietética">
<h1>SM</h1>
<p>Dietética moderna • natural • saludable 🌿</p>
</header>

<div class="container">

<div class="section">
<h2>Sobre nosotros</h2>
<p class="about">En SM Dietética te acercamos productos saludables de primera calidad para que comer bien sea simple, rico y accesible.</p>
</div>

<div class="section">
<h2>Lista de precios</h2>
<table class="price-table">
<tr><th>Producto</th><th>Peso</th><th>Precio</th><th>Agregar</th></tr>
<tr><td>Bolitas choco</td><td>250g</td><td>$2800</td><td><button onclick="addItem('Bolitas choco 250g',2800)">+</button></td></tr>
<tr><td>Bolitas choco</td><td>500g</td><td>$5000</td><td><button onclick="addItem('Bolitas choco 500g',5000)">+</button></td></tr>
<tr><td>Aritos frutales</td><td>250g</td><td>$2800</td><td><button onclick="addItem('Aritos frutales 250g',2800)">+</button></td></tr>
<tr><td>Aritos frutales</td><td>500g</td><td>$5000</td><td><button onclick="addItem('Aritos frutales 500g',5000)">+</button></td></tr>
<tr><td>Copos S/A</td><td>250g</td><td>$2000</td><td><button onclick="addItem('Copos S/A 250g',2000)">+</button></td></tr>
<tr><td>Copos S/A</td><td>500g</td><td>$3700</td><td><button onclick="addItem('Copos S/A 500g',3700)">+</button></td></tr>
<tr><td>Copos C/A</td><td>250g</td><td>$2500</td><td><button onclick="addItem('Copos C/A 250g',2500)">+</button></td></tr>
<tr><td>Copos C/A</td><td>500g</td><td>$4700</td><td><button onclick="addItem('Copos C/A 500g',4700)">+</button></td></tr>
<tr><td>Mix tropical</td><td>200g</td><td>$4000</td><td><button onclick="addItem('Mix tropical 200g',4000)">+</button></td></tr>
<tr><td>Mix común</td><td>200g</td><td>$3800</td><td><button onclick="addItem('Mix común 200g',3800)">+</button></td></tr>
<tr><td>Granola crocante</td><td>250g</td><td>$2800</td><td><button onclick="addItem('Granola crocante 250g',2800)">+</button></td></tr>
<tr><td>Granola crocante</td><td>500g</td><td>$4500</td><td><button onclick="addItem('Granola crocante 500g',4500)">+</button></td></tr>
<tr><td>Granola ámbar</td><td>250g</td><td>$2000</td><td><button onclick="addItem('Granola ámbar 250g',2000)">+</button></td></tr>
<tr><td>Granola ámbar</td><td>500g</td><td>$3500</td><td><button onclick="addItem('Granola ámbar 500g',3500)">+</button></td></tr>
<tr><td>Almohadas saborizadas</td><td>250g</td><td>$3700</td><td><button onclick="addItem('Almohadas saborizadas 250g',3700)">+</button></td></tr>
<tr><td>Almohadas saborizadas</td><td>500g</td><td>$6500</td><td><button onclick="addItem('Almohadas saborizadas 500g',6500)">+</button></td></tr>
<tr><td>Mix con maní</td><td>200g</td><td>$3800</td><td><button onclick="addItem('Mix con maní 200g',3800)">+</button></td></tr>
<tr><td>Almendras</td><td>200g</td><td>$5500</td><td><button onclick="addItem('Almendras 200g',5500)">+</button></td></tr>
<tr><td>Nuez</td><td>100g</td><td>$2700</td><td><button onclick="addItem('Nuez 100g',2700)">+</button></td></tr>
<tr><td>Girasol entero</td><td>250g</td><td>$1800</td><td><button onclick="addItem('Girasol entero 250g',1800)">+</button></td></tr>
<tr><td>Girasol pelado</td><td>200g</td><td>$2000</td><td><button onclick="addItem('Girasol pelado 200g',2000)">+</button></td></tr>
<tr><td>Orégano</td><td>100g</td><td>$1500</td><td><button onclick="addItem('Orégano 100g',1500)">+</button></td></tr>
<tr><td>Adobo</td><td>100g</td><td>$1000</td><td><button onclick="addItem('Adobo 100g',1000)">+</button></td></tr>
<tr><td>Pimienta blanca</td><td>100g</td><td>$1500</td><td><button onclick="addItem('Pimienta blanca 100g',1500)">+</button></td></tr>
<tr><td>Provenzal</td><td>100g</td><td>$1500</td><td><button onclick="addItem('Provenzal 100g',1500)">+</button></td></tr>
<tr><td>Pimentón</td><td>100g</td><td>$1500</td><td><button onclick="addItem('Pimentón 100g',1500)">+</button></td></tr>
<tr><td>Aceite de coco neutro</td><td>200g</td><td>$4500</td><td><button onclick="addItem('Aceite de coco neutro 200g',4500)">+</button></td></tr>
</table>
</div>

</div>

<button class="open-cart" onclick="toggleCart()">🛒 Ver pedido</button>

<div class="cart-panel" id="cartPanel">
<h2>Tu pedido</h2>
<div class="cart-items" id="cartList"></div>
<div class="total" id="totalPrice">Total: $0</div>
<button class="send-btn" onclick="sendWhatsApp()">Enviar pedido</button>
</div>

<a class="whatsapp" href="https://wa.me/541133144362" target="_blank">
<img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg"> Contactanos
</a>

<footer>
<p>© 2026 SM Dietética</p>
</footer>

<script>
let cart = [];

function addItem(name, price){
  const found = cart.find(i => i.name === name);
  if(found){
    found.qty += 1;
  } else {
    cart.push({name, price, qty:1});
  }
  renderCart();
  // abrir carrito automáticamente y correr contenido
  document.getElementById('cartPanel').classList.add('active');
  document.body.classList.add('cart-open');
}

function changeQty(index, delta){
  cart[index].qty += delta;
  if(cart[index].qty <= 0){
    cart.splice(index,1);
  }
  renderCart();
}

function removeItem(index){
  cart.splice(index,1);
  renderCart();
}

function toggleCart(){
  const panel = document.getElementById('cartPanel');
  panel.classList.toggle('active');
  document.body.classList.toggle('cart-open');}

function renderCart(){
  const list = document.getElementById('cartList');
  list.innerHTML = '';
  let total = 0;

  cart.forEach((item,index)=>{
    const div = document.createElement('div');
    div.className = 'cart-item';

    div.innerHTML = `
      <div>${item.name}<br>$${item.price}</div>
      <div class="qty-controls">
        <button onclick="changeQty(${index},-1)">-</button>
        ${item.qty}
        <button onclick="changeQty(${index},1)">+</button>
      </div>
      <span class="remove" onclick="removeItem(${index})">✖</span>
    `;

    list.appendChild(div);
    total += item.price * item.qty;
  });

  document.getElementById('totalPrice').textContent = 'Total: $' + total;
}

function sendWhatsApp(){
  if(cart.length === 0){
    alert('Agregá productos primero');
    return;
  }

  let msg = 'Hola! Quiero hacer este pedido:%0A';
  let total = 0;

  cart.forEach(item => {
    msg += `${item.qty} x ${item.name} - $${item.price * item.qty}%0A`;
    total += item.price * item.qty;
  });

  msg += `%0ATotal: $${total}`;

  window.location.href = 'https://wa.me/541133144362?text=' + msg;
}

// Simple tests (console)
function runTests(){
  cart = [];
  addItem('Test',100);
  addItem('Test',100);
  console.assert(cart.length===1,'Should merge same product');
  console.assert(cart[0].qty===2,'Quantity should be 2');
  changeQty(0,-1);
  console.assert(cart[0].qty===1,'Quantity should decrease');
  removeItem(0);
  console.assert(cart.length===0,'Cart should be empty');
  console.log('Tests OK');
}
// runTests();
</script>

</body>
</html>
