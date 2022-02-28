# Apuntes de HTML - @moralesvictorr

----------------
## **- Estructura basica:**
Haciendo uso de buenas practicas

```html <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="robots"  content="index,follow,translate"/> 
    <link rel="stylesheet" href="./styles/style.css">
    <title>Document</title>
</head>
<body>
    <header>
        <nav>
        </nav>
    </header>

    <main>
        <section>
            <article>
            </article>
        </section>

    </main>

    <footer>
    </footer>
</body>
</html>
```
-----------
## **- FIGURE:** Buena practica para contener etiqueta de **imagen img**:

Existe una etiqueta especifica para esto, **NO** introducir la etiqueta de imagen dentro de un div.

```html
    <figure>
        <img src="./blabla" alt="imagen de un perrito"/>
    </figure>
```
###  Además dentro de FIGURE se puede introducir otra etiqueta nueva:

**-- FIGCAPTION** Que sirve para poner la descripcion de la imagen, similar a la etique ALT de img, pero al pie de página **visible**, como si utilizaras un **div** y una etiqueta de **parrafo** para poner una descripcion al pie de imagen.
```html
 <figcaption>Raza Labrador</figcaption> 
```
------------
## **- Etiqueta de Video:**
La etiqueta video usualmente la acompañamos de "**controls**" para agregar botones y barra de reproducción.

**Tip** para video:
Usar la etiqueta "**preload**" para que el navegador precargue el video y este listo cuando lo quiera reproducir el usuario.
```html
    <video src="./blabla.mp4" controls preload="auto" ></video>
    
```
------

## **- Formularios**
### **-- FORM:** Es una buena práctica a la hora de hacer formularios, **NO** introducirlos dentro de "**div**"; porque hay una etiqueta específica para ello: "**FORM**"

### **-- LABEL:**
 Además, es buena practica usar "**label**"  para introducir el input. Label, trae una etiqueta llamada "**for**" en el que pondrás el mismo nombre que pondrás al **id** del **input**, como buena practica.
   
     for= ""

### **-- INPUT:**
**--- Type:** Usa bien la sub-etiqueta **type** (en la parte de abajo podrás ver algunos ejemplos).

**--- Placeholder:** Sirve para dentro del input poner una descripción de lo que estás solicitando al usuario.

**--- Name:** Sirve para enviar los datos

**--- Autocomplete:** Sirve para sugerir datos que el navegador ya posee del usuario. **EJEM**: Si solicitas el pais dentro de autocompletle pondrás: **autocomplete= "country". Hay etiquetas para muchos tipos de datos.**

**--- Required:** Validación desde HTML, para que el campo obligatoriamente tenga que llenarse.

    type= ""
    placeholder= ""
    name= ""
    autocomplete= ""
    required


    
```html 
    <form action="AQUI tendría que ir la url a la que envías la info">
        <label for="nombre">
            <input type="text" id="nombre" placeholder="Digita nomrbe" autocomplete="name" required/>
        </label>
    </form>
```

Los **types** de **input** a groso modo son los siguientes:

* < input type="button">
* < input type="checkbox">
* < input type="color">
* < input type="date">
* < input type="datetime-local">
* < input type="email">
* < input type="file">
* < input type="hidden">
* < input type="image">
* < input type="month">
* < input type="number">
* < input type="password">
* < input type="radio">
* < input type="range">
* < input type="reset">
* < input type="search">
* < input type="submit">
* < input type="tel">
* < input type="text">
* < input type="time">
* < input type="url">
* < input type="week">

## **--Select:** Es un ListBox desde html

### **Value:** Sirve para enviar datos.
```html
    <select name= "curso" id= "">
        <option value="opcion1">Opción 1</option>
        <option value= "opcion2">Opción 2</option>
        <option value= "opcion3">Opción 3</option>
       
    </select>
```

## **-- DataList:** Es otro ListBox desde html, pero se escribe en vez de seleccionar, se pueden capturar datos aún cuando la opción no existe, ***se usa acompañado de un input list***
id de datalist debe ser igual al del input list
```html
    <input list= "curso">
    <datalist id= "curso">
        <option value="opcion1">Opción 1</option>
        <option value= "opcion2">Opción 2</option>
        <option value= "opcion3">Opción 3</option>
       
    </datalist>
```

## **-- Botones** Se puede usar 2 tipos en formularios:

### **--- Botón "input"** Se usa exclusivamente en formularios, viene diseñado para ello

### **--- Botón "button tag"** Botón genérico personalizable

Así es como se llegaría al mismo resultado:
```html 
    <input type= "submit" value="Digita Nombre"/>
    <button  type= "submit"> Digita Nombre  </button>
```


-------

