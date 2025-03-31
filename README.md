Una aplicación web inspirada en el universo de Rick and Morty (Explorador Interdimensional C-137) que permite buscar personajes mediante una API pública, visualizar sus datos en tarjetas con diseño responsive, y gestionar favoritos con persistencia en localStorage. Además, cuenta con secciones adicionales como reproducción de capítulos mediante modales de video.

Enlace de Despliegue
Accedé a la aplicación en:
https://nodrickandmorty.netlify.app/

Funcionalidades
Búsqueda de Personajes:
Permite buscar personajes por nombre utilizando la API de Rick and Morty. La búsqueda muestra únicamente la cantidad de resultados especificada mediante un formulario.

Visualización de Resultados:
Los personajes se muestran en tarjetas diseñadas con TailwindCSS, donde se incluye información relevante (nombre, especie, estado, género y locación).

Gestión de Favoritos:

Agregar a Favoritos: Podés marcar personajes como favoritos.

Lista de Favoritos Persistente: Los personajes favoritos se guardan en localStorage para que no se pierdan al recargar la página.

Visualización y Eliminación: Podés ver los favoritos en un modal y eliminarlos individualmente o borrar toda la lista.

Reproducción de Capítulos:
Tres botones permiten abrir modales que reproducen distintos capítulos (videos de YouTube) seleccionados mediante un ID. Cada modal se muestra de forma centrada y reproduce el video embebido.

Notificaciones:
Se utiliza react-toastify para mostrar mensajes de éxito y error en las peticiones HTTP.

Diseño Responsive:
La interfaz se adapta a diferentes tamaños de pantalla utilizando TailwindCSS.

Tecnologías y Herramientas
React – Biblioteca para construir la interfaz de usuario.

Vite – Build tool para un desarrollo rápido.

TailwindCSS – Framework de CSS para diseño responsive y estilizado.

Fetch API – Para realizar peticiones HTTP a la API pública.

React Toastify – Para mostrar notificaciones de éxito, error y estados.

LocalStorage – Para persistir los personajes favoritos entre recargas.

YouTube IFrame API – Para embeber videos (capítulos) en modales.

Estructura del Proyecto
La estructura del proyecto está organizada de la siguiente forma:

bash
Copiar
/public
   └─ favicon.png        # Favicon y archivos públicos

/src
   ├─ assets             # Imágenes y otros recursos (ej. fondo.webp, fondo2.jpg, logo.png, etc.)

   
   ├─ components
   │     ├─ Header.jsx
   │     ├─ Footer.jsx
   │     ├─ CharacterCard.jsx
   │     ├─ CharacterList.jsx
   │     ├─ Loader.jsx
   │     ├─ FavoritesModal.jsx
   │     ├─ VideoModal.jsx
   │     └─ VideoEmbed.jsx   (si se usa, o se reemplaza por botones)

   
   ├─ Context
   │     ├─ FavoritesContext.jsx
   │     └─ (opcional ThemeContext si se usa, en este caso se forzó el tema oscuro)

   
   ├─ hooks
   │     └─ useFetchCharacters.js

   
   ├─ utils
   │     └─ api.js         # Funciones para hacer peticiones a la API

   
   ├─ App.jsx
   └─ main.jsx

   
Instalación y Ejecución
Clonar el repositorio:

bash
Copiar
git clone <URL-del-repositorio>
cd <nombre-del-proyecto>
Instalar dependencias:

bash
Copiar
npm install
Ejecutar la aplicación:

bash
Copiar
npm run dev
La aplicación se abrirá en http://localhost:5173/.

Despliegue
El proyecto está configurado para ser desplegado en Netlify o Vercel. El enlace al despliegue es https://nodrickandmorty.netlify.app/.

Buenas Prácticas y Consideraciones
HTTP y APIs REST:
Se utiliza la API nativa fetch para interactuar con la API pública de Rick and Morty, demostrando un manejo correcto de las peticiones y respuestas.

Manejo de Estados y Efectos:
Se emplean useState y useEffect para controlar el flujo de datos y renderizado, minimizando peticiones innecesarias.

Manejo de Errores:
Se implementan bloques try/catch y se utilizan notificaciones con react-toastify para informar al usuario en caso de errores.

Persistencia de Datos:
Los personajes favoritos se guardan en localStorage para asegurar que no se pierdan entre recargas.

Diseño Responsive:
TailwindCSS se utiliza para lograr un diseño adaptable a dispositivos móviles y de escritorio.

Documentación:
Este README explica la estructura y las decisiones técnicas tomadas, facilitando el mantenimiento y escalabilidad del proyecto.

Conclusión
El proyecto cumple con todos los requerimientos técnicos y funcionales planteados, aplicando buenas prácticas en el uso de HTTP, manejo de estados, asincronía, persistencia de datos y diseño responsive. Se ha implementado una experiencia de usuario completa, desde la búsqueda y visualización de personajes hasta la gestión de favoritos y la reproducción de capítulos.

¡Espero que este proyecto te sea de gran utilidad y cumpla con las expectativas!
