# Tienda-Tecnol-gica-
Hola bienvenido al emprendimiento estamos trabajando para que sea rápido y seguro🌐   
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tienda Digital Tech</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    * { margin:0; padding:0; box-sizing:border-box; font-family:'Poppins',sans-serif; }
    body { background:#0f172a; color:white; }
    header { display:flex; justify-content:space-between; align-items:center; padding:20px 8%; background:#0b1220; position:sticky; top:0; }
    header h1 { font-weight:800; }
    header button { background:#22c55e; border:none; padding:10px 20px; border-radius:8px; font-weight:600; cursor:pointer; }

    .hero { display:flex; flex-wrap:wrap; align-items:center; justify-content:space-between; padding:80px 8%; }
    .hero-text { max-width:500px; }
    .hero-text h2 { font-size:42px; margin-bottom:20px; }
    .hero-text p { margin-bottom:30px; color:#cbd5e1; }
    .hero-text button { background:#22c55e; border:none; padding:15px 30px; border-radius:10px; font-size:16px; font-weight:600; cursor:pointer; }

    .hero-img img { width:180px; margin:10px; border-radius:20px; }

    .products { padding:80px 8%; text-align:center; }
    .products h3 { font-size:32px; margin-bottom:40px; }
    .product-grid { display:flex; flex-wrap:wrap; justify-content:center; gap:30px; }
    .card { background:#1e293b; padding:30px; border-radius:20px; width:280px; }
    .card img { width:100%; border-radius:15px; margin-bottom:20px; }
    .card h4 { margin-bottom:10px; }
    .price { font-size:22px; font-weight:700; margin:10px 0; }
    .card button { background:#22c55e; border:none; padding:10px 20px; border-radius:8px; cursor:pointer; font-weight:600; }

    .offer { background:#111827; padding:60px 8%; text-align:center; }
    .offer h3 { font-size:28px; margin-bottom:20px; }
    .timer { display:flex; justify-content:center; gap:20px; margin:20px 0; }
    .time-box { background:#22c55e; color:black; padding:20px; border-radius:15px; width:90px; }
    .time-box span { display:block; font-size:28px; font-weight:800; }

    footer { text-align:center; padding:30px; background:#0b1220; margin-top:40px; color:#94a3b8; }

    @media(max-width:768px){
      .hero { flex-direction:column; text-align:center; }
      .hero-img img { width:120px; }
    }
  </style>
</head>
<body>

<header>
  <h1>TechStore</h1>
  <button>Comprar Ahora</button>
</header>

<section class="hero">
  <div class="hero-text">
    <h2>Lo Mejor en Tecnología Digital</h2>
    <p>Descubre nuestro reloj inteligente, audífonos inalámbricos y el celular más potente del mercado.</p>
    <button>Ver Productos</button>
  </div>
  <div class="hero-img">
    <img src="https://images.unsplash.com/photo-1516574187841-cb9cc2ca948b" alt="Reloj">
    <img src="https://images.unsplash.com/photo-1518441902110-1c2c38d3b9b9" alt="Audífonos">
    <img src="https://images.unsplash.com/photo-1511707171634-5f897ff02aa9" alt="Celular">
  </div>
</section>

<section class="products">
  <h3>Nuestros Productos</h3>
  <div class="product-grid">
    <div class="card">
      <img src="https://images.unsplash.com/photo-1516574187841-cb9cc2ca948b" alt="Reloj">
      <h4>Reloj Inteligente</h4>
      <p class="price">$49</p>
      <button>Comprar</button>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1518441902110-1c2c38d3b9b9" alt="Audífonos">
      <h4>Audífonos Bluetooth</h4>
      <p class="price">$29</p>
      <button>Comprar</button>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1511707171634-5f897ff02aa9" alt="Celular">
      <h4>Smartphone Pro</h4>
      <p class="price">$399</p>
      <button>Comprar</button>
    </div>
  </div>
</section>

<section class="offer">
  <h3>🔥 Oferta Especial por Tiempo Limitado</h3>
  <div class="timer">
    <div class="time-box"><span id="hours">00</span>Horas</div>
    <div class="time-box"><span id="minutes">00</span>Min</div>
    <div class="time-box"><span id="seconds">00</span>Seg</div>
  </div>
  <button style="background:#22c55e;border:none;padding:15px 30px;border-radius:10px;font-weight:700;cursor:pointer;">Aprovechar Oferta</button>
</section>

<footer>
  © 2026 TechStore - Todos los derechos reservados
</footer>

<script>
  let countdownDate = new Date().getTime() + (24 * 60 * 60 * 1000);

  let x = setInterval(function() {
    let now = new Date().getTime();
    let distance = countdownDate - now;

    let hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    let seconds = Math.floor((distance % (1000 * 60)) / 1000);

    document.getElementById("hours").innerHTML = hours;
    document.getElementById("minutes").innerHTML = minutes;
    document.getElementById("seconds").innerHTML = seconds;

    if (distance < 0) {
      clearInterval(x);
      document.querySelector(".timer").innerHTML = "OFERTA FINALIZADA";
    }
  }, 1000);
</script>

</body>
</html>
