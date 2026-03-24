

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