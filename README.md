# Ruta ITIID · PWA para nuevos estudiantes

Aplicación web progresiva (PWA) que presenta la Ingeniería en Tecnologías de la Información e Innovación Digital de la UTOM, basada en el mapa curricular vigente desde septiembre de 2024.

## Secciones
- **Inicio**: ruta de 10 cuatrimestres, modelo TSU + Ingeniería, datos clave y contacto.
- **Mapa**: las 63 materias y 2 estadías, con buscador, filtro por área, detalle de cada materia y registro de avance.
- **Tu futuro**: qué sabrás hacer al cerrar cada ciclo, perfiles laborales y herramientas.
- **Participa**: proyectos integradores, estadías y actividades extracurriculares.
- **Prepárate**: test de afinidad por área, lista de preparación y consejos.

## Requisitos PWA que cumple
- `manifest.json` con nombre, colores, íconos (incluye ícono *maskable*) y accesos directos.
- `sw.js` (service worker) que guarda la app en caché para funcionar **sin conexión**.
- Botón **Instalar app** (aparece cuando el navegador lo permite) e indicador de conexión.
- Diseño responsivo (móvil, tableta y escritorio) y modo oscuro automático.
- El avance, la lista y el resultado del test se guardan con `localStorage`.

## Cómo probarla
Un service worker solo funciona en `https://` o en `localhost`, no abriendo el archivo con doble clic.

```bash
cd dist
python -m http.server 8080
# abre http://localhost:8080
```
O con VS Code: extensión **Live Server** → clic derecho en `index.html` → *Open with Live Server*.

## Publicarla gratis
Sube el contenido de esta carpeta a **GitHub Pages**, **Netlify** (arrastrar la carpeta) o **Vercel**. Después abre la URL en el celular y elige *Instalar* / *Agregar a pantalla de inicio*.

Para verificar, en Chrome abre DevTools → **Application** (Manifest y Service Workers) o ejecuta **Lighthouse** con la categoría *PWA*.

## Estructura
```
index.html        App completa (HTML, CSS y JS)
manifest.json     Manifiesto de la PWA
sw.js             Service worker (modo sin conexión)
icons/            Íconos 192, 512 y maskable
```
