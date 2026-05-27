# Portfolio — Centro Municipal de Capacitación Laboral Santiago Rainero

Sitio web de una sola página (HTML/CSS/JS, sin dependencias) que unifica los dos PDFs en
un portfolio para presentar ante las autoridades del municipio. Resalta las historias de
éxito, los oficios que se dictan, los beneficios de estudiar en el Centro y la red de
emprendedores que forma parte de la comunidad.

## Estructura
```
.
├── index.html        ← el sitio completo (todo el CSS y JS está adentro)
└── assets/           ← imágenes (logos, capturas y piezas de los emprendedores)
```
No usa frameworks ni build: es 100% estático, listo para servir tal cual.

## Probar localmente
Abrí `index.html` en el navegador. (Opcional, con servidor local:)
```bash
python3 -m http.server 8000   # luego abrí http://localhost:8000
```

## Subir a GitHub
```bash
git init
git add .
git commit -m "Portfolio Centro Rainero"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
git push -u origin main
```

## Deploy en Cloudflare Pages
1. Entrá a **Cloudflare Dashboard → Workers & Pages → Create → Pages**.
2. **Connect to Git** y elegí el repositorio que acabás de subir.
3. Configuración del build:
   - **Framework preset:** `None`
   - **Build command:** *(dejar vacío)*
   - **Build output directory:** `/`  (la raíz, porque `index.html` está en la raíz)
4. **Save and Deploy**. En menos de un minuto vas a tener una URL pública
   `https://TU-PROYECTO.pages.dev` para compartir en la presentación.

> Cada `git push` a `main` vuelve a deployar automáticamente.

## Editar contenido rápido
- **Textos, números y secciones:** están en `index.html`.
- **Tarjetas de oficios:** array `disciplines` (al final, en el `<script>`).
- **Emprendedores de la comunidad:** array `emps` (mismo `<script>`); el orden es por
  cantidad de seguidores.
- **Colores de marca:** variables CSS en `:root` (paleta + acento coral).
