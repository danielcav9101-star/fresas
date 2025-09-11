<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FRESEATE - Fresas con Crema</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    html { scroll-behavior: smooth; }
  </style>
</head>
<body class="bg-pink-50 text-gray-800">

  <!-- NAVBAR -->
  <header class="bg-white shadow-md fixed w-full top-0 z-50">
    <nav class="container mx-auto flex justify-between items-center p-4">
      <h1 class="text-2xl font-bold text-pink-600 flex items-center">
        🍓 FRESEATE
      </h1>
      <ul class="flex space-x-6 font-medium">
        <li><a href="#inicio" class="hover:text-pink-500">Inicio</a></li>
        <li><a href="#productos" class="hover:text-pink-500">Productos</a></li>
        <li><a href="#info" class="hover:text-pink-500">Información</a></li>
        <li><a href="#contacto" class="hover:text-pink-500">Servicio al Cliente</a></li>
      </ul>
    </nav>
  </header>

  <!-- HERO / INICIO -->
  <section id="inicio" class="pt-24 text-center bg-gradient-to-r from-pink-200 via-white to-pink-100 py-20">
    <h2 class="text-4xl font-extrabold text-pink-700">¡Amor a la primera cucharada!</h2>
    <p class="mt-4 text-lg max-w-2xl mx-auto">
      Postres frescos, innovadores y accesibles. Fresas con crema tradicional, maracuyá y Oreo, 
      ideales para compartir con amigos, familia o tu persona especial.
    </p>
    <a href="#productos" class="mt-6 inline-block bg-pink-600 text-white px-6 py-3 rounded-full shadow hover:bg-pink-700 transition">
      Ver Productos
    </a>
  </section>

  <!-- PRODUCTOS -->
  <section id="productos" class="container mx-auto py-20 px-6">
    <h3 class="text-3xl font-bold text-center text-pink-700 mb-12">Nuestros Productos</h3>
    <div class="grid md:grid-cols-3 gap-8">
      <div class="bg-white rounded-2xl shadow p-6 text-center transform transition hover:scale-105 hover:shadow-lg">
        <h4 class="text-xl font-bold text-pink-600">Clásico</h4>
        <p class="mt-2">Fresas frescas con crema tradicional, el sabor de siempre.</p>
      </div>
      <div class="bg-white rounded-2xl shadow p-6 text-center transform transition hover:scale-105 hover:shadow-lg">
        <h4 class="text-xl font-bold text-pink-600">Maracuyá</h4>
        <p class="mt-2">Una mezcla tropical que combina lo ácido y lo dulce.</p>
      </div>
      <div class="bg-white rounded-2xl shadow p-6 text-center transform transition hover:scale-105 hover:shadow-lg">
        <h4 class="text-xl font-bold text-pink-600">Oreo</h4>
        <p class="mt-2">Perfecto para los amantes del chocolate y lo crocante.</p>
      </div>
    </div>
  </section>

  <!-- INFORMACIÓN -->
  <section id="info" class="bg-pink-100 py-20 px-6">
    <div class="container mx-auto text-center">
      <h3 class="text-3xl font-bold text-pink-700 mb-8">Sobre Nosotros</h3>
      <p class="max-w-3xl mx-auto mb-4">
        <strong>Misión:</strong> Endulzar momentos especiales con postres innovadores de fresas con crema, 
        combinando sabor, frescura y accesibilidad.
      </p>
      <p class="max-w-3xl mx-auto mb-4">
        <strong>Visión:</strong> Ser reconocidos por transformar lo sencillo en extraordinario, 
        liderando el mercado de postres frescos e innovadores.
      </p>
      <p class="max-w-3xl mx-auto">
        <strong>Ventajas:</strong> Sabores únicos (maracuyá y Oreo), precios accesibles, presentación atractiva, 
        frescura garantizada y conexión con clientes en redes sociales.
      </p>
    </div>
  </section>

  <!-- CONTACTO -->
  <section id="contacto" class="container mx-auto py-20 px-6">
    <h3 class="text-3xl font-bold text-center text-pink-700 mb-12">Servicio al Cliente</h3>
    <div class="max-w-lg mx-auto bg-white rounded-2xl shadow p-8">
      <!-- FORMULARIO FORMspree -->
      <form id="mi-form" action="https://formspree.io/f/xvgblleq" method="POST" class="space-y-4">
        <input type="text" name="nombre" placeholder="Tu nombre" class="w-full border rounded-lg p-3 focus:outline-pink-500" required>
        <input type="email" name="correo" placeholder="Tu correo" class="w-full border rounded-lg p-3 focus:outline-pink-500" required>
        <textarea name="mensaje" placeholder="Escribe tu mensaje" class="w-full border rounded-lg p-3 focus:outline-pink-500" rows="4" required></textarea>
        <button type="submit" class="w-full bg-pink-600 text-white py-3 rounded-lg hover:bg-pink-700 transition">
          Enviar
        </button>
      </form>
      <div id="estado" class="text-center mt-4"></div>

      <div class="text-center mt-6">
        <p>📍 Punto de venta: Institución Educativa Monseñor Jaime Prieto Amaya</p>
        <p>📱 Síguenos en redes: @freseate</p>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer class="bg-pink-600 text-white text-center py-6 mt-10">
    <p>&copy; 2025 FRESEATE - "Amor a la primera cucharada"</p>
  </footer>

  <!-- SCRIPT para mostrar confirmación -->
  <script>
    const form = document.getElementById("mi-form");
    const estado = document.getElementById("estado");

    form.addEventListener("submit", async (e) => {
      e.preventDefault();
      const data = new FormData(form);
      const response = await fetch(form.action, {
        method: form.method,
        body: data,
        headers: { 'Accept': 'application/json' }
      });
      if (response.ok) {
        estado.innerHTML = '<p class="text-green-600 font-semibold">✅ ¡Gracias por tu mensaje! Te responderemos pronto.</p>';
        form.reset();
      } else {
        estado.innerHTML = '<p class="text-red-600 font-semibold">❌ Hubo un error. Intenta nuevamente.</p>';
      }
    });
  </script>

</body>
</html>
<!-- PRODUCTOS -->
<section id="productos" class="container mx-auto py-20 px-6">
  <h3 class="text-3xl font-bold text-center text-pink-700 mb-12">Nuestros Productos</h3>
  
  <!-- Tarjetas de productos -->
  <div class="grid md:grid-cols-3 gap-8 mb-12">
    <div class="bg-white rounded-2xl shadow p-6 text-center transform transition hover:scale-105 hover:shadow-lg">
      <h4 class="text-xl font-bold text-pink-600">Clásico</h4>
      <p class="mt-2">Fresas frescas con crema tradicional, el sabor de siempre.</p>
    </div>
    <div class="bg-white rounded-2xl shadow p-6 text-center transform transition hover:scale-105 hover:shadow-lg">
      <h4 class="text-xl font-bold text-pink-600">Maracuyá</h4>
      <p class="mt-2">Una mezcla tropical que combina lo ácido y lo dulce.</p>
    </div>
    <div class="bg-white rounded-2xl shadow p-6 text-center transform transition hover:scale-105 hover:shadow-lg">
      <h4 class="text-xl font-bold text-pink-600">Oreo</h4>
      <p class="mt-2">Perfecto para los amantes del chocolate y lo crocante.</p>
    </div>
  </div>

  <!-- Galería de imágenes reales -->
  <h4 class="text-2xl font-bold text-center text-pink-600 mb-6">Muestras Reales</h4>
  <div class="grid md:grid-cols-2 gap-8">
    <div class="bg-white rounded-2xl shadow overflow-hidden">
      <img src="fresas.jpeg" alt="Logo Freseate" class="w-full h-72 object-contain">
      <p class="text-center p-4 text-gray-700">Etiqueta oficial del producto</p>
    </div>
    <div class="bg-white rounded-2xl shadow overflow-hidden">
      <img src="WhatsApp Image 2025-09-09 at 8.05.51 PM.jpeg" alt="Producto Freseate vaso" class="w-full h-72 object-cover">
      <p class="text-center p-4 text-gray-700">Presentación real del vaso de fresas con crema</p>
    </div>
  </div>
</section>
