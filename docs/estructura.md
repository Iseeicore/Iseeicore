# Cómo editar el perfil

El repositorio público `Iseeicore/Iseeicore` contiene el README que GitHub muestra en el perfil de `Iseeicore`.

## Carpetas

```text
README.md                   Presentación pública del perfil
assets/
  images/                   Imágenes PNG, JPG o WebP
  svg/                      SVG estáticos; incluye el banner inicial
  animations/
    pixel/                  Animaciones pixel art exportadas, por ejemplo GIF
    svg/                    SVG animados autosuficientes
design/
  source/                   Archivos originales editables y spritesheets
docs/
  estructura.md             Esta guía
```

Los archivos `.gitkeep` permiten guardar carpetas vacías en Git. Puedes retirarlos cuando añadas contenido.

## Insertar recursos

Usa rutas relativas desde el README:

```md
![Descripción de mi imagen](assets/images/mi-imagen.png)
![Descripción de mi SVG](assets/svg/mi-grafico.svg)
![Descripción de mi animación](assets/animations/pixel/mi-animacion.gif)
```

Estos nombres son ejemplos: los archivos deben existir antes de añadirlos al contenido visible. Las carpetas de animaciones están preparadas para tus futuros recursos.

## Composición del perfil

- Presentación: `personaje-rosa-azul.png` acompaña el texto sobre César.
- Stack: `sol-dorado.png` a la izquierda y `lobo-azul.png` a la derecha.
- Proyecto estrella: `samurai-cartillas.png` se reserva para Cartillas IA.
- Cierre: `principito.png` y `zorro.png`.
- Variantes disponibles: `serpiente-tinta.png`, `guerrero-mecha.png` y `cascos-mecha.png`.

Las nueve imágenes se copiaron de los archivos proporcionados, conservando sus originales sin modificaciones. El README usa seis para mantener una jerarquía clara. Las imágenes son estáticas, no animaciones.

El banner SVG inicial sigue disponible en `assets/svg/banner.svg`, pero la presentación actual usa las ilustraciones. Los textos permanecen como HTML/Markdown para facilitar su edición y lectura. La distribución usa tablas compatibles con GitHub, sin CSS personalizado.

Puedes cambiar los colores, textos y formas de `assets/svg/banner.svg` con un editor de texto. Incluye los recursos que necesites dentro del SVG: evita depender de scripts, fuentes o imágenes externas.

## Publicar cambios

Desde esta carpeta, revisa y publica solamente los archivos que quieras hacer públicos:

```powershell
git status
git add README.md assets docs design
git diff --cached
git commit -m "Actualiza el perfil"
git push
```

Comprueba el resultado en https://github.com/Iseeicore tanto en móvil como en escritorio y con los temas claro y oscuro.
