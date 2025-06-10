<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Cambio Climático</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f4f7f8;
      color: #333;
      transition: background-color 0.3s, color 0.3s;
    }

    header {
      background-color: #0077b6;
      color: white;
      padding: 20px;
      text-align: center;
    }

    nav {
      background-color: #023e8a;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }

    nav a {
      color: white;
      padding: 15px 20px;
      text-decoration: none;
      display: inline-block;
    }

    nav a:hover {
      background-color: #0077b6;
    }

    section {
      padding: 30px;
      max-width: 900px;
      margin: auto;
    }

    img {
      max-width: 100%;
      height: auto;
      border-radius: 10px;
      margin-top: 10px;
    }

    .boton {
      padding: 10px 20px;
      background-color: #00b4d8;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 20px;
    }

    footer {
      background-color: #023e8a;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 40px;
    }

    .modo-oscuro {
      background-color: #1e1e1e;
      color: #e0e0e0;
    }

    .modo-oscuro header,
    .modo-oscuro footer,
    .modo-oscuro nav {
      background-color: #121212;
    }

    form input, form textarea {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    .seccion {
      display: none;
    }

    .activa {
      display: block;
    }
  </style>
</head>
<body>
  <header>
    <h1>Cambio Climático</h1>
    <p>Un sitio para informar, reflexionar y actuar</p>
  </header>

  <nav>
    <a href="#" onclick="mostrar('inicio')">Inicio</a>
    <a href="#" onclick="mostrar('about')">Sobre Nosotros</a>
    <a href="#" onclick="mostrar('soluciones')">Soluciones</a>
    <a href="#" onclick="mostrar('contacto')">Contacto</a>
    <a href="#" onclick="cambiarModo()">Modo Oscuro</a>
  </nav>

  <section id="inicio" class="seccion activa">
    <h2>Bienvenido al portal sobre el Cambio Climático</h2>
    <p>El cambio climático es una de las mayores amenazas globales. Sus causas son humanas y sus consecuencias afectan a todo el planeta.</p>
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/65/Arctic_sea_ice_2007-09-16.jpg" alt="Reducción del hielo ártico">
    <h3>Estadísticas preocupantes</h3>
    <p>La temperatura global ha aumentado más de 1°C desde la era preindustrial.</p>
    <img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Global_temperature_anomalies_1880-2020.png" alt="Temperaturas globales en aumento">
  </section>

  <section id="about" class="seccion">
    <h2>Sobre Nosotros</h2>
    <p>Soy una estudiante y embajadora STEAM comprometida con la conciencia ambiental.</p>
    <img src="https://upload.wikimedia.org/wikipedia/commons/8/8e/Solar_and_wind_power_plants_in_Germany_-_panoramio.jpg" alt="Energías renovables">
  </section>

  <section id="soluciones" class="seccion">
    <h2>Soluciones al Cambio Climático</h2>
    <ul>
      <li>Uso de energías renovables</li>
      <li>Reforestación</li>
      <li>Movilidad sostenible</li>
      <li>Consumo responsable</li>
    </ul>
    <img src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Wind_turbines_and_solar_panels_-_panoramio.jpg" alt="Energía limpia">
    <h3>Emisiones por país</h3>
    <img src="https://upload.wikimedia.org/wikipedia/commons/7/75/CO2_emissions_per_country_2014.png" alt="Emisiones de CO2 por país">
  </section>

  <section id="contacto" class="seccion">
    <h2>Contáctanos</h2>
    <form onsubmit="return validarFormulario()">
      <label>Nombre:</label>
      <input type="text" id="nombre" placeholder="Tu nombre" required />
      <label>Email:</label>
      <input type="email" id="email" placeholder="Tu correo electrónico" required />
      <label>Mensaje:</label>
      <textarea id="mensaje" placeholder="Tu mensaje" rows="5" required></textarea>
      <button type="submit" class="boton">Enviar</button>
    </form>
  </section>

  <footer>
    <p>© 2025 Conciencia Climática - Todos los derechos reservados</p>
  </footer>

  <script>
    function mostrar(seccion) {
      const secciones = document.querySelectorAll('.seccion');
      secciones.forEach(sec => sec.classList.remove('activa'));
      document.getElementById(seccion).classList.add('activa');
    }

    function cambiarModo() {
      document.body.classList.toggle('modo-oscuro');
    }

    function validarFormulario() {
      const nombre = document.getElementById('nombre').value.trim();
      const email = document.getElementById('email').value.trim();
      const mensaje = document.getElementById('mensaje').value.trim();

      if (!nombre || !email || !mensaje) {
        alert('Por favor, completa todos los campos.');
        return false;
      }

      alert('Mensaje enviado. ¡Gracias por contactarnos!');
      return false; // Evita que el formulario se envíe realmente
    }
  </script>
</body>
</html>
