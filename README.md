<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Tienda de Dropshipping - Productos Ganadores</title>
  <script src="https://cdn.tailwindcss.com "></script>
  <style>
    .hover\:scale-105:hover {
      transform: scale(1.05);
    }
    .line-clamp-2 {
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
    }
  </style>
</head>
<body class="bg-gray-50 text-gray-900 font-sans">

  <!-- Header -->
  <header class="bg-white shadow-sm sticky top-0 z-50">
    <div class="container mx-auto px-4 py-4">
      <div class="flex items-center justify-between">
        <div class="flex items-center space-x-2">
          <svg class="w-10 h-10 text-indigo-600" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          <h1 class="text-xl font-bold text-gray-900">DropshipGanadores</h1>
        </div>

        <!-- Mobile Menu Button -->
        <button id="menuToggle" class="md:hidden text-gray-600">
          <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </button>
      </div>

      <!-- Mobile Menu -->
      <div id="mobileMenu" class="hidden mt-4 pb-4 overflow-x-auto">
        <div class="flex space-x-4">
          <button onclick="setCategory('all')" class="whitespace-nowrap text-sm font-medium capitalize text-indigo-600 border-b-2 border-indigo-600 pb-1">Todos los Productos</button>
          <button onclick="setCategory('hogar')" class="whitespace-nowrap text-sm font-medium capitalize text-gray-600 hover:text-indigo-600">Hogar</button>
          <button onclick="setCategory('decoracion')" class="whitespace-nowrap text-sm font-medium capitalize text-gray-600 hover:text-indigo-600">Decoración</button>
          <button onclick="setCategory('oficina')" class="whitespace-nowrap text-sm font-medium capitalize text-gray-600 hover:text-indigo-600">Oficina</button>
          <button onclick="setCategory('salud')" class="whitespace-nowrap text-sm font-medium capitalize text-gray-600 hover:text-indigo-600">Salud</button>
          <button onclick="setCategory('accesorios')" class="whitespace-nowrap text-sm font-medium capitalize text-gray-600 hover:text-indigo-600">Accesorios</button>
          <button onclick="setCategory('ropa')" class="whitespace-nowrap text-sm font-medium capitalize text-gray-600 hover:text-indigo-600">Ropa</button>
        </div>
      </div>
    </div>
  </header>

  <!-- Hero Section with Image -->
  <section class="relative bg-gradient-to-r from-indigo-600 to-purple-600 text-white overflow-hidden">
    <img 
      src="https://picsum.photos/seed/dropshipping/1200/400 " 
      alt="Productos ganadores de dropshipping" 
      class="absolute inset-0 w-full h-full object-cover opacity-20"
    />
    <div class="container mx-auto px-4 py-16 relative z-10">
      <div class="max-w-3xl">
        <h2 class="text-4xl md:text-5xl font-bold mb-6 leading-tight">
          Encuentra los Productos Ganadores de Dropshipping
        </h2>
        <p class="text-xl md:text-2xl mb-8 max-w-3xl opacity-90">
          Descubre productos con alto potencial de ventas y márgenes rentables para tu negocio online.
        </p>
        <div class="flex flex-col sm:flex-row gap-4">
          <button class="bg-white text-indigo-600 px-8 py-3 rounded-lg font-semibold text-lg shadow-lg hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
            Ver Productos Destacados
          </button>
          <button class="border-2 border-white px-8 py-3 rounded-lg font-semibold text-lg hover:bg-white hover:bg-opacity-10 transition duration-300">
            Suscríbete al Boletín
          </button>
        </div>
      </div>
    </div>
  </section>

  <!-- Main Content -->
  <main class="container mx-auto px-4 py-12">
    <!-- Stats Banner -->
    <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-12">
      <div class="bg-white p-6 rounded-xl shadow-md text-center transform transition duration-300 hover:scale-105">
        <div class="text-3xl font-bold text-indigo-600">+1500</div>
        <div class="text-gray-600">Productos Analizados</div>
      </div>
      <div class="bg-white p-6 rounded-xl shadow-md text-center transform transition duration-300 hover:scale-105">
        <div class="text-3xl font-bold text-indigo-600">+85%</div>
        <div class="text-gray-600">Tasa de Conversión</div>
      </div>
      <div class="bg-white p-6 rounded-xl shadow-md text-center transform transition duration-300 hover:scale-105">
        <div class="text-3xl font-bold text-indigo-600">$10M+</div>
        <div class="text-gray-600">Ventas Totales</div>
      </div>
      <div class="bg-white p-6 rounded-xl shadow-md text-center transform transition duration-300 hover:scale-105">
        <div class="text-3xl font-bold text-indigo-600">+5000</div>
        <div class="text-gray-600">Usuarios Activos</div>
      </div>
    </div>

    <!-- Products Grid -->
    <div class="mb-12">
      <h2 class="text-3xl font-bold text-gray-900 mb-8">Productos Ganadores</h2>
      <input 
        type="text" 
        id="searchInput"
        placeholder="Buscar productos..."
        class="w-full pl-10 pr-4 py-2 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-indigo-500 mb-6"
      />
      <div id="productsGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
        <!-- Los productos se insertarán dinámicamente aquí -->
      </div>
    </div>
  </main>

  <!-- Footer -->
  <footer class="bg-gray-900 text-gray-300 py-12">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
        <div>
          <div class="flex items-center space-x-2 mb-4">
            <svg class="w-8 h-8 text-indigo-500" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              <path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              <path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            <h3 class="text-xl font-bold text-white">DropshipGanadores</h3>
          </div>
          <p class="mb-4">
            Tu plataforma número 1 para encontrar productos ganadores para tu negocio de dropshipping.
          </p>
        </div>
        <div>
          <h4 class="text-lg font-semibold text-white mb-4">Productos</h4>
          <ul class="space-y-2">
            <li><a href="#" class="hover:text-white transition duration-300">Productos Ganadores</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Nuevos Productos</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Más Vendidos</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Categorías Populares</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Análisis de Mercado</a></li>
          </ul>
        </div>
        <div>
          <h4 class="text-lg font-semibold text-white mb-4">Recursos</h4>
          <ul class="space-y-2">
            <li><a href="#" class="hover:text-white transition duration-300">Guía para Empezar</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Tips de Marketing</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Casos de Éxito</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Blog de Dropshipping</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Webinars Gratuitos</a></li>
          </ul>
        </div>
        <div>
          <h4 class="text-lg font-semibold text-white mb-4">Empresa</h4>
          <ul class="space-y-2">
            <li><a href="#" class="hover:text-white transition duration-300">Sobre Nosotros</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Contáctanos</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Términos y Condiciones</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Política de Privacidad</a></li>
            <li><a href="#" class="hover:text-white transition duration-300">Centro de Ayuda</a></li>
          </ul>
        </div>
      </div>
      <div class="border-t border-gray-800 mt-12 pt-8 text-sm text-gray-400 text-center">
        <p>© <span id="year"></span> DropshipGanadores. Todos los derechos reservados.</p>
      </div>
    </div>
  </footer>

  <!-- Script JS -->
  <script>
    const products = [
      { id: 1, name: "Lámpara de Luz Nocturna LED con Sensor de Movimiento", category: "hogar", price: 24.99, salePrice: 17.99, rating: 4.8, reviews: 1245, image: "https://picsum.photos/id/1062/400/400 ", isNew: true, bestSeller: true },
      { id: 2, name: "Reloj de Pared Silencioso con Diseño Moderno", category: "decoracion", price: 39.99, salePrice: 29.99, rating: 4.6, reviews: 890, image: "https://picsum.photos/id/1061/400/400 ", isNew: false, bestSeller: true },
      { id: 3, name: "Organizador de Cableado con Diseño Inteligente", category: "oficina", price: 14.99, salePrice: 9.99, rating: 4.7, reviews: 678, image: "https://picsum.photos/id/1059/400/400 ", isNew: true, bestSeller: false },
      { id: 4, name: "Set de 3 Cepillos de Dientes Eléctricos Recargables", category: "salud", price: 89.99, salePrice: 59.99, rating: 4.9, reviews: 1567, image: "https://picsum.photos/id/1057/400/400 ", isNew: false, bestSeller: true },
      { id: 5, name: "Mochila Antirrobo con Puerto USB Integrado", category: "accesorios", price: 49.99, salePrice: 34.99, rating: 4.7, reviews: 1023, image: "https://picsum.photos/id/1055/400/400 ", isNew: true, bestSeller: false },
      { id: 6, name: "Alfombra Absorbente de Agua para Baño o Cocina", category: "hogar", price: 19.99, salePrice: 14.99, rating: 4.6, reviews: 789, image: "https://picsum.photos/id/1053/400/400 ", isNew: false, bestSeller: true },
      { id: 7, name: "Cortavientos Reflectante Unisex para Correr", category: "ropa", price: 34.99, salePrice: 24.99, rating: 4.5, reviews: 567, image: "https://picsum.photos/id/1051/400/400 ", isNew: true, bestSeller: false },
      { id: 8, name: "Soporte Magnético para Teléfono en el Auto", category: "accesorios", price: 24.99, salePrice: 17.99, rating: 4.8, reviews: 987, image: "https://picsum.photos/id/1049/400/400 ", isNew: false, bestSeller: true }
    ];

    let selectedCategory = 'all';
    let searchTerm = '';

    function setCategory(category) {
      selectedCategory = category;
      renderProducts();
    }

    function setSearchTerm() {
      const input = document.getElementById('searchInput');
      searchTerm = input.value;
      renderProducts();
    }

    document.getElementById('searchInput').addEventListener('input', setSearchTerm);

    function renderProducts() {
      const container = document.getElementById('productsGrid');
      container.innerHTML = '';

      const filteredProducts = products.filter(product => {
        const matchesCategory = selectedCategory === 'all' || product.category === selectedCategory;
        const matchesSearch = product.name.toLowerCase().includes(searchTerm.toLowerCase());
        return matchesCategory && matchesSearch;
      });

      if (filteredProducts.length === 0) {
        container.innerHTML = `
          <div class="col-span-full text-center py-16">
            <svg class="w-16 h-16 text-gray-400 mx-auto mb-4" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M9.172 16.758L4.243 11.828L11.314 4.757L16.243 9.687L9.172 16.758Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              <path d="M14.828 20.172L19.757 15.242L12.686 8.172L7.757 13.102L14.828 20.172Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            <h3 class="text-xl font-medium text-gray-700 mb-2">No se encontraron productos</h3>
            <p class="text-gray-500 mb-4">Intenta ajustar tus filtros o términos de búsqueda</p>
            <button onclick="resetFilters()" class="px-4 py-2 bg-indigo-600 text-white rounded-lg hover:bg-indigo-700 transition duration-300">
              Restablecer filtros
            </button>
          </div>`;
        return;
      }

      filteredProducts.forEach(product => {
        const div = document.createElement('div');
        div.className = "bg-white rounded-xl shadow-lg overflow-hidden transform transition duration-300 hover:shadow-xl hover:-translate-y-1";
        div.innerHTML = `
          <div class="relative">
            <img src="${product.image}" alt="${product.name}" class="w-full h-64 object-cover"/>
            ${product.isNew ? `<span class="absolute top-3 left-3 bg-green-500 text-white text-xs font-bold px-2 py-1 rounded-full">Nuevo</span>` : ''}
            ${product.bestSeller ? `<span class="absolute top-3 right-3 bg-yellow-500 text-white text-xs font-bold px-2 py-1 rounded-full">Más Vendido</span>` : ''}
          </div>
          <div class="p-5">
            <div class="flex justify-between items-start mb-2">
              <h3 class="font-semibold text-gray-900 line-clamp-2 h-12">${product.name}</h3>
              <div class="flex items-center">
                <svg class="w-4 h-4 text-yellow-400" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                  <path d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z" />
                </svg>
                <span class="ml-1 text-sm text-gray-700">${product.rating}</span>
              </div>
            </div>
            <p class="text-sm text-gray-500 mb-4">${product.reviews} reseñas</p>
            <div class="flex justify-between items-center">
              <div>
                <span class="text-lg font-bold text-indigo-600">${product.salePrice.toFixed(2)}</span>
                <span class="text-sm text-gray-500 line-through ml-2">${product.price.toFixed(2)}</span>
              </div>
              <button class="bg-indigo-600 hover:bg-indigo-700 text-white px-4 py-2 rounded-lg transition duration-300 text-sm font-medium flex items-center">
                <svg class="w-4 h-4 mr-1" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M3 3H5L5.4 5M5.4 5H21L17 13H7M5.4 5L7 13M7 13L4.707 15.293C4.077 15.923 4.523 17 5.414 17H17M17 17C16.4696 17 15.9609 17.2107 15.5858 17.5858C15.2107 17.9609 15 18.4696 15 19C15 19.5304 15.2107 20.0391 15.5858 20.4142C15.9609 20.7893 16.4696 21 17 21C17.5304 21 18.0391 20.7893 18.4142 20.4142C18.7893 20.0391 19 19.5304 19 19C19 18.4696 18.7893 17.9609 18.4142 17.5858C18.0391 17.2107 17.5304 17 17 17Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
                Añadir al carrito
              </button>
            </div>
          </div>
        `;
        container.appendChild(div);
      });
    }

    function resetFilters() {
      selectedCategory = 'all';
      searchTerm = '';
      document.getElementById('searchInput').value = '';
      renderProducts();
    }

    function toggleMenu() {
      const menu = document.getElementById('mobileMenu');
      menu.classList.toggle('hidden');
    }

    // Event Listeners
    document.getElementById('menuToggle').addEventListener('click', toggleMenu);

    document.getElementById('year').textContent = new Date().getFullYear();

    // Initial Render
    renderProducts();
  </script>
</body>
</html>
