# Gym Love — PWA instalable (Android e iPhone)

## Qué contiene
Este paquete es una **carcasa PWA** que muestra la aplicación existente `https://gym-love.streamlit.app` dentro de una ventana. No altera el `app.py`, las rutinas ni Supabase. Necesita conexión a internet para entrenar y guardar datos.

## Publicar GRATIS con GitHub Pages
1. En GitHub, crea un **repositorio nuevo PÚBLICO** llamado `gym-love-pwa` (no uses tu repositorio privado actual de Streamlit).
2. Sube los archivos de esta carpeta **a la raíz del repositorio nuevo**: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`. No es necesario subir README.
3. En Settings → Pages → Build and deployment → Deploy from a branch, selecciona `main` y `/(root)` y guarda.
4. Espera a que GitHub Pages publique `https://TU_USUARIO.github.io/gym-love-pwa/`.
5. Abre esa URL desde el celular. **Android (Chrome)**: menú ⋮ → Instalar aplicación o Añadir a pantalla principal. **iPhone (Safari)**: Compartir → Añadir a pantalla de inicio → Añadir.

## Precauciones
- **Prueba antes de usar** que puedas entrar con el PIN, iniciar/terminar un entrenamiento y que los registros aparezcan en el historial. iOS/Safari puede limitar cookies o almacenamiento de páginas dentro de iframes de otro dominio.
- Si hay problemas, usa el enlace directo de Streamlit, que seguirá funcionando. Para una PWA plenamente fiable y de mismo origen en iOS, habría que migrar el frontend o desplegar una infraestructura de proxy correctamente configurada.
- No publiques secretos, PIN, claves ni `app.py` con credenciales en este repositorio público. La PWA contiene solo recursos estáticos públicos.
- No es una app offline; el service worker almacena solo el menú contenedor, **no** los entrenamientos ni los datos.
- La PWA no cambia la app principal ni requiere actualizar su código.
