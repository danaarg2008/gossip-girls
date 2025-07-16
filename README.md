# gossip-girls 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GOSSIP GIRL - Fundas & Decoración</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #fff1f7;
      color: #444;
    }
    header {
      background: linear-gradient(90deg, #ff66b2, #ff85c1);
      color: white;
      padding: 30px 20px;
      text-align: center;
    }
    .presentacion {
      background-color: #ffe0ec;
      padding: 30px 20px;
      text-align: center;
    }
    .presentacion img {
      max-width: 300px;
      border-radius: 20px;
      margin-bottom: 20px;
    }
    .presentacion p {
      font-size: 18px;
      color: #cc0066;
      max-width: 800px;
      margin: 0 auto;
    }
    nav {
      background-color: #ffcce5;
      padding: 12px;
      text-align: center;
    }
    nav a {
      margin: 0 20px;
      text-decoration: none;
      color: #cc0066;
      font-weight: bold;
      font-size: 16px;
    }
    .container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 30px;
    }
    .producto {
      background-color: white;
      border-radius: 15px;
      box-shadow: 0 6px 15px rgba(0,0,0,0.1);
      padding: 20px;
      text-align: center;
      transition: transform 0.3s;
    }
    .producto:hover {
      transform: translateY(-5px);
    }
    .producto img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 10px;
    }
    .producto h3 {
      color: #cc0066;
      margin: 15px 0 5px;
    }
    .precio {
      color: #ff3399;
      font-size: 1.2em;
      font-weight: bold;
    }
    button {
      background-color: #ff66b2;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 8px;
      margin-top: 10px;
      cursor: pointer;
    }
    #carrito {
      background-color: #fff0f5;
      padding: 30px;
      border-top: 3px solid #ff66b2;
      text-align: center;
    }
    footer {
      background-color: #ff66b2;
      color: white;
      text-align: center;
      padding: 20px;
    }
    .footer-info {
      margin-top: 10px;
      font-size: 14px;
    }
    .social-icons img {
      width: 24px;
      margin: 0 10px;
      vertical-align: middle;
    }
   </style>
  <script>
    let carrito = [];

    function agregarAlCarrito(nombre, precio) {
      carrito.push({ nombre, precio });
      mostrarCarrito();
    }

    function mostrarCarrito() {
      let contenedor = document.getElementById('carrito-lista');
      contenedor.innerHTML = '';
      let total = 0;
      carrito.forEach((producto, index) => {
        contenedor.innerHTML += `
          <div>
            <span>${producto.nombre} - $${producto.precio}</span>
            <button onclick="eliminarDelCarrito(${index})">❌</button>
          </div>`;
        total += producto.precio;
      });
      document.getElementById('carrito-total').innerText = 'Total: $' + total;
    }

    function eliminarDelCarrito(index) {
      carrito.splice(index, 1);
      mostrarCarrito();
    }
  </script>
  </nav>
</body>
</html>
  <header>
    <h1>GOSSIP GIRL</h1>
    <p>Fundas personalizadas y decoración para celulares, computadoras y tablets</p>
  </header>

  <section class="presentacion">
    <img src="logo.png" alt="Logo Gossip Girl">
    <p>Bienvenida a nuestra tienda online, donde el estilo y la protección se combinan. En GOSSIP GIRL ofrecemos fundas y accesorios únicos, diseñados con amor para que tu celular, computadora o tablet refleje tu personalidad.</p>
  </section>
  <section class="nosotras">
    <div class="texto">
      <h2>   ¿Quiénes somos?</h2>
      <p>    Somos un equipo de chicas apasionadas por la moda y la tecnología. Creamos GOSSIP GIRL con la mision de ofrecer productos únicos y personalizados que reflejen el estilo de cada persona y la vision de poder tener locales fisicos para poder llegar a mas de nuestras chicas GOSSIPS. Nos encanta combinar diseño, funcionalidad y mucho brillo en cada uno de nuestros productos. Gracias por acompañarnos en este sueño rosa 💕</p>
    </div>
  </section>

  <nav>
    <a href="#celulares">Celulares</a>
    <a href="#computadoras">Computadoras</a>
    <a href="#tablets">Tablets</a>
  </nav>

  <section class="container" id="celulares">
    <div class="producto">
      <img src="funda.png" alt="Funda glitter">
      <h3>Funda personalizada con charms</h3>
      <p class="precio">$50000</p>
      <button onclick="agregarAlCarrito('Funda personalizada con charms', 50000)">Agregar al carrito</button>
    </div>
    <div class="producto">
      <img src="fundarosa.jpeg" alt="Animal Print">
      <h3>Funda rosa anti golpes</h3>
      <p class="precio">$20000</p>
      <button onclick="agregarAlCarrito('Funda rosa anti golpes', 20000)">Agregar al carrito</button>
    </div>
    <div class="producto">
      <img src="correa.png" alt="Stickers">
      <h3>Phone strap personalizadas</h3>
      <p class="precio">$6000</p>
      <button onclick="agregarAlCarrito('Phone strap', 6000)">Agregar al carrito</button>
    </div>
    <div class="producto">
      <img src="soporteadhesivo.png" alt="Funda corazón">
      <h3>soporte de silicona (10 colores)</h3>
      <p class="precio">$5000</p>
      <button onclick="agregarAlCarrito('soporte de silicona ', 5000)">Agregar al carrito</button>
    </div>
  </section>

  <section class="container" id="computadoras">
    <div class="producto">
      <img src="stickers.jpg" alt="Stickers laptop">
      <h3>Stickers para Laptop</h3>
      <p class="precio">$3000</p>
      <button onclick="agregarAlCarrito('Stickers Laptop', 3000)">Agregar al carrito</button>
    </div>
    <div class="producto">
      <img src="fundaparacompu.jpg" alt="Funda rosa">
      <h3>Funda Rosa</h3>
      <p class="precio">$6200</p>
      <button onclick="agregarAlCarrito('Funda Rosa', 6200)">Agregar al carrito</button>
    </div>
    <div class="producto">
      <img src="mouse.png" alt="Diseño mármol">
      <h3>mouse inalambrico (5 colores)</h3>
      <p class="precio">$6000</p>
      <button onclick="agregarAlCarrito('mouse inalambrico', 6000)">Agregar al carrito</button>
    </div>
    <div class="producto">
      <img src="fundaparateclado.png" alt="Funda con bolsillos">
      <h3>Funda para teclado</h3>
      <p class="precio">$7000</p>
      <button onclick="agregarAlCarrito('Funda para teclado', 7000)">Agregar al carrito</button>
    </div>
  </section>

  <section class="container" id="tablets">
    <div class="producto">
      <img src="fundadehello.png" alt="Floral">
      <h3>funda de hello kitty para tablet</h3>
      <p class="precio">$17000</p>
      <button onclick="agregarAlCarrito('funda de hello kitty para tablet', 17000)">Agregar al carrito</button>
    </div>
    <div class="producto">
      <img src="lapiz.png" alt="Glam">
      <h3>lapiz tactil</h3>
      <p class="precio">$5000</p>
      <button onclick="agregarAlCarrito('lapiz tactil', 5000)">Agregar al carrito</button>
    </div>
    <div class="producto">
      <img src="fundarosata.png" alt="Arcoiris">
      <h3>Funda rosa para tablet</h3>
      <p class="precio">$10000</p>
      <button onclick="agregarAlCarrito('Funda rosa para tablet', 10000)">Agregar al carrito</button>
    </div>
    <div class="producto">
      <img src="fundadelapiz.png" alt="Mariposas">
      <h3>Funda para lapiz tactil (pack 2)</h3>
      <p class="precio">$5000</p>
      <button onclick="agregarAlCarrito('Funda para lapiz tactil', 5000)">Agregar al carrito</button>
    </div>
  </section>

  <section id="carrito">
    <h2>🛒 Carrito de Compras</h2>
    <div id="carrito-lista"></div>
    <p id="carrito-total">Total: $0</p>
  </section>

  <footer>
    <p>&copy; 2025 GOSSIP GIRL - Todos los derechos reservados</p>
    <div class="footer-info">
      <p>📍 Dirección: PLUMERILLO 3924, Buenos Aires, Argentina</p>
      <div class="social-icons">
        <a href="https://www.instagram.com/gossip_girls.ji/"><img src="logo2.png" alt="Instagram"></a> 
      </div>
    </div>
  </footer>
</body>
</html>
