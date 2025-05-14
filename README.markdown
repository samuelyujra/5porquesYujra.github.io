# Juego de los 5 Porqués

## Descripción

El **Juego de los 5 Porqués** es una aplicación web interactiva diseñada para facilitar el análisis de causas raíz de cualquier problemática utilizando la metodología de los 5 Porqués. Esta técnica, originada en Toyota, consiste en preguntar "¿Por qué?" cinco veces de manera iterativa para identificar la causa fundamental de un problema. La aplicación permite a los usuarios ingresar respuestas, visualizar estadísticas y generar informes, promoviendo un análisis colaborativo y estructurado.

La aplicación es ideal para equipos que buscan resolver problemas de manera sistemática, ya sea en contextos empresariales, educativos o de mejora continua. Es personalizable para cualquier problemática, con una interfaz amigable y herramientas de visualización de datos.

## Características principales

- **Formulario interactivo**: Guía a los usuarios a través de cinco preguntas "Por qué" para profundizar en la causa raíz de un problema.
- **Progreso visual**: Incluye una barra de progreso que muestra el avance en los pasos del formulario.
- **Resultados y estadísticas**: Muestra el número de participantes, departamentos involucrados y puntos en común entre las respuestas.
- **Visualizaciones**: Genera una nube de palabras, gráficos de barras y circulares, y un árbol de problemas para analizar las respuestas.
- **Exportación de datos**: Permite exportar resultados en formato JSON y generar un informe en PDF.
- **Tema claro/oscuro**: Ofrece un interruptor para cambiar entre modos claro y oscuro.
- **Efectos visuales**: Incluye animaciones como confeti al enviar respuestas y un botón de "scroll to top".
- **Almacenamiento local**: Guarda las respuestas en `localStorage` para persistencia en el navegador.
- **Pestañas de navegación**: Organiza el contenido en secciones: Juego, Resultados, Dashboard y Acerca del Método.

## Cómo funciona

1. **Inicio del juego**:
   - Los usuarios acceden a la pestaña "Juego" y ven una descripción del problema a analizar.
   - Completan un formulario con su nombre, departamento/área y cinco respuestas a las preguntas "Por qué", cada una profundizando en la causa de la respuesta anterior.

2. **Progreso y validación**:
   - La barra de progreso muestra el paso actual (1 a 5).
   - Cada paso requiere completar los campos obligatorios antes de avanzar.
   - Los usuarios pueden retroceder para editar respuestas previas.

3. **Envío de respuestas**:
   - Al completar las cinco preguntas, los usuarios envían sus respuestas, desencadenando un efecto de confeti.
   - Las respuestas se almacenan en `localStorage` y se muestran en la pestaña "Resultados".

4. **Visualización de resultados**:
   - La pestaña "Resultados" muestra tarjetas con las respuestas de cada participante, estadísticas (número de participantes, departamentos y puntos en común) y una nube de palabras con términos frecuentes.
   - Los usuarios pueden eliminar respuestas individuales o exportar los datos en JSON o PDF.

5. **Dashboard**:
   - La pestaña "Dashboard" presenta gráficos de barras (categorías de causas raíz), circulares (distribución de causas) y un árbol de problemas que visualiza la relación entre el problema y las causas raíz.

6. **Acerca del Método**:
   - Explica la metodología de los 5 Porqués, su historia y beneficios, con secciones claras sobre el proceso y su aplicación.

## Tecnologías utilizadas

- **HTML5**: Estructura de la aplicación.
- **CSS3**: Estilos con diseño responsivo, animaciones y soporte para temas claro/oscuro.
- **JavaScript**: Lógica de la aplicación, incluyendo gestión del formulario, almacenamiento local y generación de visualizaciones.
- **Bibliotecas externas**:
  - **Font Awesome (v6.4.0)**: Iconos para la interfaz.
  - **Chart.js (v3.9.1)**: Gráficos de barras y circulares en el dashboard.
  - **jsPDF (v2.5.1)** y **html2canvas (v1.4.1)**: Generación de informes en PDF.
  - **canvas-confetti (v1.6.0)**: Efecto de confeti al enviar respuestas.
  - **Google Fonts (Poppins)**: Tipografía moderna y legible.

## Requisitos

- Un navegador web moderno (Chrome, Firefox, Safari, Edge, etc.).
- Conexión a internet para cargar las bibliotecas externas vía CDN (puede adaptarse para uso offline).
- No se requiere instalación de software adicional ni servidor backend, ya que utiliza `localStorage` para persistencia.

## Instalación y uso

1. **Descargar el código**:
   - Clona o descarga el repositorio que contiene el archivo `index.html` y cualquier recurso adicional (como imágenes para el logotipo).

2. **Configurar la problemática**:
   - Edita el contenido del `div` con clase `problem-card` en `index.html` para definir la problemática deseada:
     ```html
     <div class="problem-card">
         <h3>Problema a Resolver:</h3>
         <p>[Inserta aquí la descripción del problema]</p>
     </div>
     ```
   - Actualiza las etiquetas `<label>` en los pasos del formulario (`data-step="2"` a `data-step="6"`) para reflejar las preguntas asociadas a la nueva problemática.

3. **Configurar el logotipo**:
   - Reemplaza la ruta del logotipo en `<img src="/api/placeholder/120/120" alt="Logo" class="logo">` con la ruta de tu imagen (por ejemplo, `images/logo.png`).

4. **Ejecutar la aplicación**:
   - Abre `index.html` en un navegador web. No se necesita un servidor local para pruebas básicas, ya que las dependencias se cargan vía CDN.

5. **Usar el juego**:
   - Navega a la pestaña "Juego" y completa el formulario.
   - Revisa los resultados en la pestaña "Resultados" o las visualizaciones en "Dashboard".
   - Exporta los datos o genera un PDF según sea necesario.

## Personalización

- **Cambiar la problemática y preguntas**:
  - Modifica el texto de la problemática y las preguntas en el HTML, como se explicó en la sección de instalación.
  - Ajusta la lista de `stopWords` en la función `generateWordCloud` (en el archivo JavaScript) para excluir palabras irrelevantes específicas de la nueva problemática:
    ```javascript
    const stopWords = ['el', 'la', 'los', 'las', 'un', 'una', 'y', 'o', 'de', 'del', 'a', 'en', 'que', 'por', 'para', 'con', 'se', 'su', /* palabras específicas */];
    ```
  - Si es necesario, mejora la lógica de categorización en `generateCharts` para adaptarla a la nueva problemática (por ejemplo, usar palabras clave en lugar de la primera palabra).

- **Estilos**:
  - Edita las variables CSS en el bloque `:root` para cambiar colores, fuentes o espaciados:
    ```css
    :root {
        --primary-color: #003087;
        --accent-color: #d32f2f;
        /* Otros colores */
    }
    ```

- **Análisis avanzado**:
  - Para mejorar la detección de puntos en común, considera integrar una biblioteca de procesamiento de lenguaje natural (como Natural.js) o un backend para análisis semántico.
  - Añade categorías predefinidas en `generateCharts` para una mejor clasificación de las respuestas.

## Limitaciones y consideraciones

- **Almacenamiento**: Los datos se guardan en `localStorage`, lo que limita la persistencia al navegador del usuario. Para entornos multiusuario, considera integrar un backend.
- **Análisis de respuestas**: La detección de puntos en común busca coincidencias exactas (después de normalización). Respuestas muy variadas pueden reducir los puntos en común identificados.
- **Categorización**: La categorización en los gráficos se basa en la primera palabra de las respuestas finales, lo que puede no ser ideal para todas las problemáticas. Ajusta la lógica según sea necesario.
- **Offline**: La aplicación depende de CDNs para las bibliotecas. Para uso offline, descarga las bibliotecas y actualiza las rutas en el HTML.
- **Seguridad**: No incluye validación avanzada de entradas. Si se integra con un backend, valida y sanitiza las entradas para evitar problemas de seguridad (como XSS).

## Qué no se usa

- **Backend**: No se requiere un servidor, ya que los datos se almacenan localmente en el navegador.
- **Base de datos**: No utiliza bases de datos externas, solo `localStorage`.
- **Autenticación**: No hay sistema de login, ya que está diseñado para uso local o grupal sin restricciones de acceso.
- **Frameworks pesados**: No usa frameworks como React o Vue.js, manteniendo la aplicación ligera con JavaScript puro.
- **Imágenes externas**: Excepto el logotipo, no se usan imágenes externas en las visualizaciones.

## Contribuciones

Si deseas contribuir:
1. Haz un fork del repositorio.
2. Crea una rama para tus cambios (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -m "Añadir nueva funcionalidad"`).
4. Envía un pull request con una descripción clara de los cambios.

## Licencia

© 2025 Juego de los 5 Porqués. Desarrollado por Samuel Yura. Todos los derechos reservados.
