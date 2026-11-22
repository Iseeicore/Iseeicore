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

Estos nombres son ejemplos: los archivos deben existir antes de añadirlos al contenido visible. El banner inicial es estático; las carpetas de animaciones están preparadas para tus futuros recursos.

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
