

# 🚀 Guía Práctica: Bootcamp Vue 3 - Portfolio Express

## 1: Daily Habit Tracker (Check-it)
**Objetivo:** Aprender reactividad básica, listas y persistencia local.

### 🛠️ Instrucciones:
1.  **Inicialización:** Crea un nuevo proyecto con `npm create vue@latest`. Selecciona solo lo básico (No Router, No Pinia por hoy).
2.  **Interfaz Base:**
    * Crea un `input` tipo texto y un botón "Añadir Hábito".
    * Usa `v-model` para capturar el texto del input en una variable reactiva (`ref`).
3.  **Listado de Hábitos:**
    * Crea un array `habitos = ref([])`.
    * Usa `v-for` para mostrar cada hábito en una lista (`<ul>`).
    * Cada elemento debe tener un `checkbox` vinculado a una propiedad `completado`.
4.  **Lógica de Control:**
    * Crea una función `agregarHabito` que valide que el input no esté vacío.
    * Crea una función `eliminarHabito` usando `.filter()` o `.splice()`.
5.  **Persistencia (LocalStorage):**
    * Usa `watch` de Vue para guardar el array en `localStorage` cada vez que cambie.
    * En el `onMounted`, carga los datos guardados para que no se borren al refrescar.

> **💡 Reto del día:** Agrega un contador que diga: "Has completado X de Y hábitos hoy".

---

## 2: Buscador de Películas (Connect Movie)
**Objetivo:** Consumo de APIs externas y manejo de estados asíncronos.

### 🛠️ Instrucciones:
1.  **Preparación:** Regístrate en [OMDb API](http://www.omdbapi.com/) para obtener una Key gratuita o usa una URL de prueba que el profesor te facilite.
2.  **Estructura de Búsqueda:**
    * Crea un campo de búsqueda que dispare una función al presionar "Enter" o hacer clic.
3.  **Llamada a la API:**
    * Instala Axios `npm install axios` o usa `fetch`.
    * Crea una función `buscarPeliculas` que reciba el término de búsqueda y actualice un array `resultados`.
4.  **Visualización de Datos:**
    * Crea un grid de "Cards" usando CSS Flexbox o Grid.
    * Muestra el póster (`v-bind:src`), el título y el año de la película.
5.  **Estados de Carga:**
    * Crea una variable `loading = ref(false)`.
    * Muestra un mensaje de "Cargando..." usando `v-if` mientras la petición está en curso.

> **💡 Reto del día:** Si la búsqueda no arroja resultados, muestra un mensaje amigable de "No se encontraron películas".


---

## 3: Coffee Shop E-Commerce
**Objetivo:** Comunicación entre componentes (Props y Emits).

### 🛠️ Instrucciones:
1.  **Componentización:**
    * Crea un componente `ProductoCard.vue` que reciba por **props** el nombre, precio e imagen del café.
    * Crea un componente `Carrito.vue` para mostrar los items seleccionados.
2.  **Evento Personalizado (Emit):**
    * En `ProductoCard`, agrega un botón "Agregar". Al hacer clic, debe emitir un evento (`$emit('add-to-cart', producto)`).
3.  **Gestión del Carrito (Padre):**
    * En el componente principal (`App.vue`), escucha el evento y añade el producto a un array `carrito`.
4.  **Cálculos Reactivos:**
    * Usa `computed` para calcular el total a pagar automáticamente cada vez que el carrito cambie.
5.  **Refinamiento:**
    * Agrega la opción de eliminar un producto del carrito desde el componente `Carrito`.

> **💡 Reto del día:** Limita la cantidad de productos: que no se puedan agregar más de 10 cafés del mismo tipo.

---

## 4: Portfolio Shell & Routing
**Objetivo:** Navegación profesional y despliegue final.

### 🛠️ Instrucciones:
1.  **Configuración de Rutas:**
    * Instala Vue Router: `npm install vue-router@4`.
    * Configura las rutas: `/habit-tracker`, `/movie-finder`, `/coffee-shop`.
2.  **Integración de Proyectos:**
    * Mueve el código de los días anteriores a componentes de tipo "View" o "Page".
3.  **Navegación (Navbar):**
    * Crea una barra de navegación superior usando `<router-link>` para moverte entre las apps sin recargar la página.
4.  **Landing Page:**
    * Crea una vista de inicio (`Home.vue`) con una breve biografía tuya y enlaces a tus redes sociales.
5.  **Despliegue (Build):**
    * Ejecuta `npm run build`.
    * Sube el proyecto a **Vercel** o **Netlify** conectando tu repositorio de GitHub.

> **💡 Reto del día:** Personaliza los colores de todo el portfolio para que tenga una identidad visual única.

---
