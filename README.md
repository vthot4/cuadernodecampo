# Codex Naturae

Cuaderno de campo donde registro las especies que me voy encontrando por el camino — desde la rosa silvestre en un margen de sendero hasta la bacteria que aparece bajo el microscopio.

Plantas, aves, insectos, mamíferos, reptiles, microalgas, protozoos, bacterias... todo lo que llama la atención merece una ficha. La idea es simple: observar, identificar y anotar.

Sitio estático construido con HTML y CSS, sin dependencias ni frameworks.

## Categorías

El catálogo está organizado en las siguientes categorías, cada una con su carpeta:

- Plantas
- Aves
- Insectos
- Mamíferos
- Reptiles
- Peces
- Moluscos (caracoles, bivalvos, cefalópodos)
- Invertebrados marinos (crustáceos, equinodermos, cnidarios...)
- Bacterias
- Protozoos
- Microalgas
- Otros (para lo que no encaje en ninguna anterior)

## Estructura del proyecto

```
├── index.html              # Página principal con el catálogo
├── _template.html          # Plantilla base para fichas de especies
├── _template_teoria.html   # Plantilla base para artículos de teoría
├── css/
│   └── style.css           # Estilos del sitio
├── img/                    # Imágenes compartidas
├── habitats/               # Páginas de hábitats explorados
├── plantas/                # Fichas de plantas (ej: rosa-canina.html)
├── aves/                   # Fichas de aves (ej: passer-domesticus.html)
├── insectos/               # Fichas de insectos (ej: lasius-niger.html)
├── mamiferos/
├── reptiles/
├── peces/
├── moluscos/
├── invertebrados-marinos/
├── bacterias/
├── protozoos/
├── microalgas/
├── otros/
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
4. Añadir el enlace a la nueva ficha en la sección correspondiente de `index.html`
5. Si hay fotos, guardarlas en la carpeta de la categoría: `categoria/img/nombre-especie/`

## Cómo añadir un hábitat

1. Crear un archivo HTML en `habitats/` con el nombre del hábitat en minúsculas (ej: `jardin.html`)
2. Seguir la estructura de los hábitats existentes: cabecera, descripción, especies registradas y footer
3. Añadir la tarjeta del hábitat en la sección "Hábitats Explorados" de `index.html`

## Cómo añadir un artículo de teoría

1. Copiar `_template_teoria.html` en la subcarpeta temática correspondiente dentro de `teoria/` (ej: `teoria/botanica/`)
2. Renombrar el archivo con el tema en minúsculas y separado por guiones (ej: `partes-de-una-planta.html`)
3. Rellenar las secciones: introducción, contenido y referencias
4. Añadir el enlace al artículo en la sección "Teoría" de `index.html`
