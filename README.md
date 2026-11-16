# 🌿 Codex Naturae

**Cuaderno de campo** donde registro las especies que me voy encontrando por el camino — desde la rosa silvestre en un margen de sendero hasta la bacteria que aparece bajo el microscopio.

### 👉 [vthot4.github.io/cuadernodecampo](https://vthot4.github.io/cuadernodecampo/)

`https://vthot4.github.io/cuadernodecampo/`

---

## Qué es

Plantas, aves, insectos, moluscos, invertebrados marinos, hongos, algas... todo lo que llama la atención merece una ficha. La idea es simple: **observar, identificar y anotar**.

Cada ficha incluye:

- Nombre científico, autoría y nombres comunes
- Clasificación taxonómica (reino → especie)
- Descripción morfológica, ecología y distribución
- Usos y estado de conservación (badge UICN)
- Notas de campo: fecha, lugar y observaciones propias
- Galería de fotos con créditos y licencia

Además del catálogo, el sitio tiene páginas de **hábitats explorados** (bosque, pradera, humedal, costa y jardín) y una sección de **teoría** con artículos de conocimiento general.

## Diseño

Estética de cuaderno naturalista: papel crema, tinta oscura y acentos dorados.

- Responsive: pensado para móvil, tableta y escritorio
- Modo oscuro automático (`prefers-color-scheme`)
- Navegación rápida por categorías en la portada
- Respeta `prefers-reduced-motion` y tiene estilos de impresión

## Tecnología

Sitio estático construido con HTML y CSS, sin dependencias, sin JavaScript ni frameworks. Publicado con GitHub Pages.

Para verlo en local basta con servir la carpeta:

```bash
git clone https://github.com/vthot4/cuadernodecampo.git
cd cuadernodecampo
python3 -m http.server 8000
# → http://localhost:8000
```

## Categorías

Cada categoría tiene su carpeta:

| Carpeta | Contenido |
|---|---|
| `plantas/` | Plantas |
| `aves/` | Aves |
| `insectos/` | Insectos |
| `mamiferos/` | Mamíferos |
| `reptiles/` | Reptiles |
| `peces/` | Peces |
| `moluscos/` | Caracoles, bivalvos, cefalópodos |
| `invertebrados-marinos/` | Crustáceos, equinodermos, cnidarios... |
| `bacterias/` | Bacterias |
| `protozoos/` | Protozoos |
| `microalgas/` | Microalgas |
| `otros/` | Lo que no encaje en ninguna anterior (hongos, algas, rotíferos, tardígrados...) |

## Estructura del proyecto

```
├── index.html              # Página principal con el catálogo
├── _template.html          # Plantilla base para fichas de especies
├── _template_teoria.html   # Plantilla base para artículos de teoría
├── css/
│   └── style.css           # Estilos del sitio (claro y oscuro)
├── img/                    # Imágenes compartidas
├── habitats/               # Páginas de hábitats explorados
├── <categoria>/            # Fichas de especies (ej: plantas/rosa-canina.html)
│   └── img/<especie>/      # Fotos de cada especie
└── teoria/                 # Artículos de teoría y conocimiento general
    ├── botanica/
    ├── zoologia/
    ├── ecologia/
    └── microbiologia/
```

## Cómo añadir una nueva especie

1. Copiar `_template.html` en la carpeta de la categoría correspondiente
2. Renombrar el archivo con el nombre científico en minúsculas y separado por guiones (ej: `rosa-canina.html`, `parus-major.html`)
3. Rellenar los datos de la ficha: taxonomía, morfología, ecología, notas de campo y galería
4. Guardar las fotos en `categoria/img/nombre-especie/` (`principal.jpg` se usa como miniatura en la portada)
5. Añadir la especie a su sección en `index.html` (los bloques `type-section` tienen `id` por categoría) y actualizar el contador de la cabecera de sección y las estadísticas globales
6. Si es una novedad, añadirla a "Últimas Incorporaciones"

## Cómo añadir un hábitat

1. Crear un archivo HTML en `habitats/` con el nombre del hábitat en minúsculas (ej: `jardin.html`)
2. Seguir la estructura de los hábitats existentes: cabecera, descripción, especies registradas y footer
3. Añadir la tarjeta del hábitat en la sección "Hábitats Explorados" de `index.html`

## Cómo añadir un artículo de teoría

1. Copiar `_template_teoria.html` en la subcarpeta temática correspondiente dentro de `teoria/` (ej: `teoria/botanica/`)
2. Renombrar el archivo con el tema en minúsculas y separado por guiones (ej: `partes-de-una-planta.html`)
3. Rellenar las secciones: introducción, contenido y referencias
4. Añadir el enlace al artículo en la sección "Teoría" de `index.html`

## Créditos

Las fotos de cada ficha indican autoría y licencia en el pie de la galería.
