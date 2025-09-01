# presentacion-html 5avanzado
Exposicion
# HTML BASICO 
## 1. Introducción al HTML
###Definición:
- HTML (HyperText Markup Language) es el lenguaje de marcado que define la estructura de una página web.
- No es un lenguaje de programación, sino de marcado → organiza contenido en títulos, párrafos, imágenes, etc.

 ---
## 2. Estructura mínima de un archivo HTML y etiquetas principales 
<img width="496" height="406" alt="image" src="https://github.com/user-attachments/assets/5a1eea0c-6fad-428d-9d46-250934f9752f" />

- `<html>`: Encierra todo el documento.
- `<head>`: Contiene metadatos, título, enlaces a CSS/JS.
- `<body>`: Todo el contenido visible.

  
 ----
## 3. Formateo de texto
- `<p>`: párrafo.
- `<h1>` a `<h6>`: títulos (jerarquía).
- `<strong>`: texto en negrita (con importancia).
- `<em>`: texto en cursiva (énfasis).
- `<br>`: salto de línea.
- `<hr>`: línea horizontal.
---
## 4. Listas 
- No ordenada(`<ul>`):viñetas.
- Ordenada(`<ol>`):números
- `<li>`:cada elemento.
<img width="746" height="461" alt="image" src="https://github.com/user-attachments/assets/be505a3a-72e7-41b5-96b0-c461ef0c128a" />

## 5. Imagenes
- Se insertan con la etiqueta <img>.
- Atributos principales:
- src: ruta de la imagen.
- alt: texto alternativo (muy importante para accesibilidad y SEO).

`<img src="perro.jpg" alt="Un perro corriendo en el parque" width="300">`















# HTML Avanzado – Desarrollo Web

## 1. Elementos y Atributos Globales
Los atributos globales pueden aplicarse a la mayoría de elementos HTML.  
Algunos de los más importantes son:

- **id**: identificador único para un elemento.  
- **class**: agrupa elementos con un mismo estilo o comportamiento.  
- **style**: añade estilos CSS en línea.  
- **title**: muestra información al pasar el cursor.  
- **data-***: permite almacenar datos personalizados.  

**Ejemplo:**
```html
<p id="parrafo1" class="texto" style="color:blue;" title="Información extra" data-info="dato">
  Hola Mundo
</p>
```
## 2. Uso de `<template>` y `<slot>` para Contenido Dinámico
Los elementos `<template>` y `<slot>` permiten manejar contenido dinámico en HTML.  

- **template**: define un fragmento de contenido HTML que no se renderiza de inmediato en la página, sino que puede ser activado o clonado mediante JavaScript.  
- **slot**: se utiliza dentro de componentes web (Web Components) para permitir la inserción de contenido dinámico desde el exterior hacia el interior del componente.  

**Ejemplo con `<template>`:**
```html
<template id="miTemplate">
  <p>Texto desde el template</p>
</template>
```
### 3. Elementos Multimedia

HTML incluye soporte nativo para reproducir contenido multimedia como **audio** y **video**.  
Estos elementos ofrecen atributos que permiten controlar su comportamiento:

- **controls**: muestra botones de control como reproducir, pausar o volumen.  
- **autoplay**: inicia la reproducción automáticamente al cargar la página (con restricciones en navegadores).  
- **loop**: repite el contenido indefinidamente.  
- **muted**: comienza la reproducción en silencio.  

#### Ejemplo:

```html
<video controls>
  <source src="video.mp4" type="video/mp4">
</video>
```
### 4. Integración de SVG y Canvas

HTML proporciona dos formas principales de trabajar con gráficos:

- **SVG (Scalable Vector Graphics)**:  
  Es un lenguaje basado en **XML** que permite definir gráficos vectoriales escalables, ideales para logotipos, iconos e ilustraciones.

- **Canvas**:  
  Es un lienzo en el que se pueden dibujar gráficos dinámicos mediante **JavaScript**, útil para animaciones, videojuegos o visualización de datos.

#### Ejemplo con SVG:

```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="blue" stroke-width="2" fill="lightblue" />
</svg>
```
# 5. Formularios Avanzados

Con **HTML5**, los formularios se volvieron más potentes gracias a nuevos tipos de entrada y validaciones integradas.  
Esto mejora la experiencia del usuario y reduce la necesidad de validaciones complejas con **JavaScript**.

## Características principales

- **email**: valida automáticamente que el valor ingresado tenga formato de correo.  
- **number**: permite introducir solo números, con límites opcionales de mínimo y máximo.  
- **date**: muestra un calendario para elegir una fecha.  
- **required**: marca un campo como obligatorio antes de enviar el formulario.  
- **pattern**: permite usar expresiones regulares para validar datos específicos.  

## Ejemplo 5:

```html
<form>
  <label for="correo">Correo electrónico:</label>
  <input type="email" id="correo" required>

  <label for="edad">Edad:</label>
  <input type="number" id="edad" min="18" max="99">

  <label for="fecha">Fecha de cita:</label>
  <input type="date" id="fecha" required>

  <button type="submit">Enviar</button>
</form>
