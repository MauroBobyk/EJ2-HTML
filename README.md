# EJ2-HTML

## Conceptos trabajados

- **`class`**: Atributo HTML que agrupa varios elementos bajo un mismo nombre. En CSS se selecciona con un punto (`.`) y permite aplicar los mismos estilos a todos los elementos que la compartan. A diferencia de `id` (`#`), una clase puede repetirse.

- **Flexbox**: Sistema de layout moderno que permite alinear y distribuir elementos dentro de un contenedor de forma sencilla. Se activa con `display: flex`. Con `flex-direction: column` los elementos se apilan verticalmente y con `align-self` cada hijo puede decidir su propia alineación (`flex-start` = izquierda, `flex-end` = derecha, `center` = centro).

- **Selectores CSS**: Indican a qué elementos se aplican los estilos. Los principales son: universal `*` (todos los elementos), clase `.nombre`, ID `#nombre` (único) y pseudo-clases como `:hover` (cuando el mouse pasa por encima).

- **Transiciones**: Con `transition` los cambios de estilo (color, tamaño) se animan suavemente en vez de ser instantáneos. Se especifica qué propiedad animar y cuánto tarda (ej: `transition: background-color 0.3s`).

- **Navegación entre páginas**: La etiqueta `<a href="archivo.html">` convierte cualquier elemento en un enlace clickeable hacia otra página del proyecto.

---

## Google Fonts

[Google Fonts](https://fonts.google.com/) es un servicio gratuito que ofrece cientos de tipografías listas para usar en la web. En este proyecto cada página usa una fuente distinta:
### ¿Cómo se accede y se elige una fuente?

1. Entrar a **[fonts.google.com](https://fonts.google.com/)**.
2. Navegar por el catálogo o usar el buscador para encontrar una fuente.
3. Hacer clic en la fuente deseada.
4. En la página de la fuente, hacer clic en **"Get font"** (esquina superior derecha).
5. Luego ir a **"Get embed code"** para ver las opciones de inserción.
6. Elegir la pestaña **"Web"** y seleccionar la opción **`<link>`** (la primera, no `@import`).
7. Seleccionar solo los pesos que se van a usar (ej: Regular 400 y Bold 700). Cuantos más pesos se marquen, más tarda en cargar.
8. Copiar el `<link>` que aparece en el recuadro y pegarlo en el `<head>` del HTML.
### ¿Cómo se usa?

Son dos pasos:

1. **Cargar la fuente** con una etiqueta `<link>` en el `<head>` del HTML:
   ```html
   <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
   ```
   - `family=Roboto` → nombre de la fuente.
   - `wght@400;700` → pesos que se descargan (400 = normal, 700 = negrita).
   - `display=swap` → muestra texto con una fuente del sistema mientras la de Google termina de cargar (evita que la página se vea en blanco).

2. **Aplicar la fuente** con la propiedad CSS `font-family`:
   ```css
   body { font-family: 'Roboto', sans-serif; }
   ```
   El valor después de la coma (`sans-serif`, `serif`) es el *fallback*: si Google Fonts falla, el navegador usa una fuente genérica parecida.

### Fuentes usadas en cada página

| Página | Fuente | Categoría | Característica |
|--------|--------|-----------|----------------|
| `index.html` | **Roboto** | sans-serif | Limpia, moderna y muy legible. Es la fuente predeterminada de Android. |
| `pagina1.html` | **Montserrat** | sans-serif | Geométrica, con formas redondeadas. Inspirada en la señalización urbana. |
| `pagina2.html` | **Lora** | serif | Elegante, con remates curvos. Ideal para textos largos o citas. |
| `pagina3.html` | **Oswald** | sans-serif | Condensada (estrecha), fuerte y con carácter. Muy usada en titulares. |

### Categorías de fuentes

- **serif**: Tienen remates (patitas) en los extremos de las letras. Transmiten tradición y elegancia (ej: Times New Roman, Lora).
- **sans-serif**: Sin remates. Son limpias y modernas (ej: Arial, Roboto, Montserrat).
- **monospace**: Cada letra ocupa el mismo ancho. Ideales para código (ej: Courier New).
- **display / handwriting**: Decorativas o manuscritas, para usos puntuales (títulos, logos).


