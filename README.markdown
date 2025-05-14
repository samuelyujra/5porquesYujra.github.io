# Juego de los 5 Porqués - PIL Andina

![Game Screenshot](screenshot.png)

## Descripción

El **Juego de los 5 Porqués** es una aplicación web interactiva diseñada para PIL Andina, una empresa láctea boliviana. Este juego está basado en la técnica de los "5 Whys" para identificar la causa raíz de un problema empresarial, en este caso, **retrasos en la distribución de productos a los puntos de venta en La Paz**. La aplicación permite a los empleados ingresar sus respuestas a cinco preguntas consecutivas de "por qué", visualizar las respuestas en tarjetas dinámicas y detectar puntos en común para fomentar un debate en equipo.

### Características
- **Interfaz atractiva**: Diseño basado en tarjetas con colores inspirados en PIL Andina (azul, rojo, blanco).
- **Animaciones divertidas**: Efectos de deslizamiento, confeti al enviar respuestas y transiciones suaves.
- **Barra de progreso**: Indicadores visuales para rastrear el avance de las respuestas.
- **Resultados dinámicos**: Tarjetas con respuestas de todos los participantes y detección automática de puntos en común.
- **Diseño responsivo**: Optimizado para dispositivos móviles y de escritorio.
- **Fácil de usar**: Interfaz intuitiva con emojis y mensajes amigables para empleados de todos los niveles.

## Tecnologías utilizadas
- **HTML5**: Estructura de la aplicación.
- **CSS3**: Estilos con animaciones y diseño responsivo.
- **JavaScript**: Lógica para gestionar respuestas, detectar puntos en común y animaciones.
- **Confetti.js**: Librería para efectos de confeti (CDN: `https://cdn.jsdelivr.net/npm/canvas-confetti`).
- **Google Fonts**: Fuente Poppins para un diseño moderno.

## Instalación y despliegue en GitHub Pages

### Prerrequisitos
- Una cuenta de GitHub.
- Un repositorio en GitHub para alojar el proyecto.
- Un navegador web moderno (Chrome, Firefox, Edge, etc.).

### Pasos para subir la página a GitHub Pages
1. **Clonar o crear un repositorio**:
   - Crea un nuevo repositorio en GitHub (por ejemplo, `pil-5-whys-game`).
   - Clona el repositorio a tu máquina local:
     ```bash
     git clone https://github.com/tu-usuario/pil-5-whys-game.git
     ```

2. **Agregar el archivo principal**:
   - Copia el contenido del archivo `index.html` (proporcionado en el código anterior) en el directorio raíz del repositorio.
   - Opcionalmente, agrega una captura de pantalla (`screenshot.png`) para el README.

3. **Confirmar y subir los cambios**:
   - Agrega los archivos al repositorio:
     ```bash
     git add index.html screenshot.png
     git commit -m "Agregar Juego de los 5 Porqués"
     git push origin main
     ```

4. **Habilitar GitHub Pages**:
   - Ve a tu repositorio en GitHub.
   - Dirígete a la pestaña **Settings**.
   - Desplázate hasta la sección **Pages**.
   - En **Source**, selecciona la rama `main` y la carpeta `/ (root)`.
   - Haz clic en **Save**. GitHub generará una URL (por ejemplo, `https://tu-usuario.github.io/pil-5-whys-game/`).

5. **Acceder a la página**:
   - Una vez que GitHub Pages procese el despliegue (puede tardar unos minutos), visita la URL proporcionada para ver el juego en acción.

## Uso
1. **Abrir la aplicación**:
   - Accede a la página web a través del enlace de GitHub Pages.
   - La página mostrará el problema: **"Retrasos en la distribución de productos a los puntos de venta en La Paz"**.

2. **Ingresar respuestas**:
   - Cada participante ingresa su nombre y responde a las cinco preguntas de "por qué" en los campos correspondientes.
   - Una barra de progreso muestra el avance mientras se completan los campos.

3. **Enviar respuestas**:
   - Haz clic en el botón **"🚀 Enviar Respuestas"**. Si todos los campos están completos, aparecerá un efecto de confeti, y las respuestas se mostrarán en tarjetas.

4. **Revisar resultados**:
   - Las respuestas de todos los participantes se organizan en una cuadrícula de tarjetas.
   - Los puntos en común (respuestas repetidas) se destacan en una tarjeta roja para guiar el debate.

5. **Reiniciar el juego**:
   - Usa el botón **"🔄 Reiniciar Juego"** para limpiar todas las respuestas y empezar de nuevo.

## Ejemplo de uso
- **Participante 1 (María)**:
  - ¿Por qué 1? "Los camiones salen tarde."
  - ¿Por qué 2? "Porque la planificación de rutas es ineficiente."
  - ¿Por qué 3? "Porque no usamos software de logística."
  - ¿Por qué 4? "Porque no se invirtió en tecnología."
  - ¿Por qué 5? "Porque el presupuesto priorizó marketing."
- **Participante 2 (Juan)**:
  - ¿Por qué 1? "Los camiones salen tarde."
  - ¿Por qué 2? "Porque hay demoras en la carga."
  - ¿Por qué 3? "Porque el personal no está capacitado."
  - ¿Por qué 4? "Porque no hay programas de formación."
  - ¿Por qué 5? "Porque el presupuesto priorizó marketing."
- **Puntos en común**: "Los camiones salen tarde" y "Porque el presupuesto priorizó marketing". Estos puntos sirven como base para un debate en equipo.

## Contexto para PIL Andina
- **Problema abordado**: Retrasos en la distribución, un desafío común en Bolivia debido al tráfico en La Paz, condiciones de carreteras y limitaciones logísticas.
- **Cultura local**: La interfaz incluye emojis (🎉, 🥛) y un diseño amigable para reflejar la vibrante cultura boliviana, inspirada en eventos como Alasitas o Carnaval.
- **Accesibilidad**: El diseño es simple e intuitivo, ideal para empleados de todos los niveles en PIL Andina, desde operarios hasta gerentes.

## Personalización
Para adaptar el juego a otro problema o empresa:
1. Modifica el texto del problema en la clase `.problem-card` en `index.html`.
2. Ajusta los colores en el CSS (variables como `#003087` y `#d32f2f`) para reflejar la identidad de otra empresa.
3. Actualiza los emojis o mensajes en los labels para un tono diferente.

## Contribuciones
Si deseas contribuir:
- Crea un *fork* del repositorio.
- Implementa mejoras (por ejemplo, guardar respuestas en localStorage, agregar sonidos o exportar resultados como PDF).
- Envía un *pull request* con una descripción clara de los cambios.

## Licencia
Este proyecto está bajo la [Licencia MIT](LICENSE). Siéntete libre de usarlo y modificarlo para tus necesidades.

## Contacto
Para soporte o sugerencias, contacta a través de GitHub Issues o al correo de tu equipo en PIL Andina.

---

¡Ayuda a PIL Andina a resolver sus problemas de distribución de manera divertida y colaborativa! 🚚🥛