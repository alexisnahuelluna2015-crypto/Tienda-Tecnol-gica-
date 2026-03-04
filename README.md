# Tienda-Tecnol-gica-
Hola bienvenido al emprendimiento estamos trabajando para que sea rápido y seguro🌐

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TechStore Premium</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    *{margin:0;padding:0;box-sizing:border-box;font-family:'Inter',sans-serif}
    body{background:#000;color:#fff}
    header{display:flex;justify-content:space-between;align-items:center;padding:25px 8%;position:fixed;width:100%;background:rgba(0,0,0,0.7);backdrop-filter:blur(10px);z-index:1000}
    header h1{font-weight:800;letter-spacing:1px}
    header a{color:#fff;text-decoration:none;font-weight:500;margin-left:25px}
    
    .hero{height:100vh;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;padding:0 20px;background:linear-gradient(180deg,#000 60%,#111)}
    .hero h2{font-size:48px;font-weight:800;margin-bottom:20px}
    .hero p{color:#aaa;max-width:600px;margin-bottom:40px}
    .btn{background:#fff;color:#000;padding:15px 40px;border-radius:50px;font-weight:600;text-decoration:none;transition:0.3s}
    .btn:hover{background:#ddd}

    .products{padding:120px 8%;background:#111;text-align:center}
    .products h3{font-size:36px;margin-bottom:60px}
    .grid{display:flex;flex-wrap:wrap;justify-content:center;gap:40px}
    .card{background:#000;border:1px solid #222;padding:40px;border-radius:30px;width:300px;transition:0.4s}
    .card:hover{transform:translateY(-10px);border:1px solid #444}
    .card img{width:100%;border-radius:20px;margin-bottom:25px}
    .card h4{font-size:20px;margin-bottom:10px}
    .price{font-size:26px;font-weight:700;margin:15px 0}

    .offer{padding:100px 8%;text-align:center;background:#000}
    .offer h3{font-size:30px;margin-bottom:20px}
    .timer{display:flex;justify-content:center;gap:25px;margin:40px 0}
    .time-box{border:1px solid #333;padding:25px;border-radius:20px;width:100px}
    .time-box span{display:block;font-size:32px;font-weight:800}

    footer{padding:40px;text-align:center;background:#111;color:#666}

    @media(max-width:768px){
      .hero h2{font-size:34px}
      .grid{flex-direction:column;align-items:center}
    }
  </style>
</head>
<body>

<header>
  <h1>TECHSTORE</h1>
  <div>
    <a href="#productos">Productos</a>
    <a href="#oferta">Oferta</a>
  </div>
</header>

<section class="hero">
  <h2>Tecnología que Define el Futuro</h2>
  <p>Reloj inteligente, audífonos inalámbricos y smartphone premium con diseño elegante y potencia máxima.</p>
  <a href="#productos" class="btn">Explorar Productos</a>
</section>

<section class="products" id="productos">
  <h3>Productos Destacados</h3>
  <div class="grid">
    <div class="card">
      <img src="https://images.unsplash.com/photo-1516574187841-cb9cc2ca948b" alt="Reloj">
      <h4>Reloj Inteligente Pro</h4>
      <p class="price">$49</p>
      <a href="#" class="btn">Comprar</a>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1518441902110-1c2c38d3b9b9" alt="Audífonos">
      <h4>Audífonos Wireless X</h4>
      <p class="price">$29</p>
      <a href="#" class="btn">Comprar</a>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1511707171634-5f897ff02aa9" alt="Celular">
      <h4>Smartphone Ultra</h4>
      <p class="price">$399</p>
      <a href="#" class="btn">Comprar</a>
    </div>
  </div>
</section>

<section class="offer" id="oferta">
  <h3>Oferta Exclusiva por Tiempo Limitado</h3>
  <div class="timer">
    <div class="time-box"><span id="hours">00</span>Horas</div>
    <div class="time-box"><span id="minutes">00</span>Min</div>
    <div class="time-box"><span id="seconds">00</span>Seg</div>
  </div>
  <a href="#" class="btn">Aprovechar Oferta</a>
</section>

<footer>
  © 2026 TechStore Premium
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
