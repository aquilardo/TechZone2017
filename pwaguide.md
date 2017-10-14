# Guia - Workshop: Progressive Web Apps

## Preparando el Entorno

1. Instalamos Google Chrome
1. Instalamos Ligthouse, como complemento de google
1. Instalamos Git
1. Instalamos Node
1. Instalamos Atom que usaremos como editor de código

## Verificando el entorno

1. Iniciamos Git Bash
1. Verificamos que se haya instalado correctamente Node ejecutando `node --version`
1. Verficamos que se haya instalado correctamente nmp ejecutando `npm --version`
1. Iniciamos Atom
1. Iniciamos Google Chrome
1. Hacemos un recorrido sobre los paneles del **Web Developers Tools**

## Instalamos live-server
1. Ejecutamos el comando `npm install -g live-server`
1. Verificamos que se haya instalado correctamente ejecutando `liver-server --version`

## Creando el entorno de trabajo
1. Creamos una carpeta con nombre **pwatz2017** en el escritorio
1. Abrimos la carpeta con el explorador de windows y creamos dentro 3 carpetas con los siguientes nombres **images**, **css** y **js**
1. Abrir la carpeta con el editor de código **Atom**.

# Creamos nuestra PWA

## Creamos el archivo HTML `index.html` con una plantilla básica

1. Creamos el archivo HTML en la ruta raíz
1. Creamos la estructura básica del documento HTML
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>TZ 2017 by Jala - PWA</title>
  </head>
  <body>
    <h1>Mi PWA</h1>
  </body>
</html>
```
## Iniciamos el servidor y verificamos nuestra PWA

1. Desde Git Bash y con la ruta en la carpeta donde se encuentra nuestro proyecto ejecutamos el comando `live-server`
1. Ejecutamos la herramienta **Lighthouse** para verificar la evaluación que realiza entorno a los parámetros relacionados con PWA

## Añadimos algunas etiquetas meta a nuestro documento HTML
```html
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- Informa al navegador de que se trata de una PWA -->
    <meta name="mobile-web-app-capable" content="yes">
    <!-- Informa al navegador de iOS que se trata de una PWA -->
    <meta name="apple-mobile-web-app-capable" content="yes">
    <!-- Define el color del template -->
    <meta name="theme-color" content="#ff00ff">
```
Volvemos a evaluar con **Ligthouse**

## Creamos el archivo `manifest.json`

```json
{
  "short_name": "TZ 2017",
  "name": "TechZone 2017 by Jala",
  "icons": [
    {
      "src": "/images/512x512.png",
      "type": "image/png",
      "sizes": "512x512"
    },
    {
      "src": "/images/192x192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
    {
      "src": "/images/128x128.png",
      "type": "image/png",
      "sizes": "128x128"
    },
    {
      "src": "/images/small-logo.png",
      "type": "image/png",
      "sizes": "64x64"
    }
  ],
  "start_url": "/",
  "orientation": "portrait",
  "display": "standalone",
  "theme_color": "#ff00ff",
  "background_color": "#000000"
}
```
