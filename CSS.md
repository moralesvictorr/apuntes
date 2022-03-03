# Apuntes de CSS - @moralesvictorr

----------------
## ¿Qué es CSS?
Las siglas en ingés son: Cascading Style Sheets, es decir, Hojas de Estilo en Cascada. 
En pocas palabras es un lenguaje que maneja el diseño y la presentación de una página web; funciona en conjunto con HTML.
Con CSS abarcamos opciones relativas a fuentes, colores, márgenes, líneas, altura, anchura, imágenes de fondo, entre otros.

Se les denomina hojas de estilo «en cascada» porque puedes tener varias hojas y una de ellas con las propiedades heredadas (o «en cascada») de otras.

## Estructura:
![Regla CSS](https://github.com/moralesvictorr/apuntesDesarrolloWeb/blob/master/images/CSSRegla.PNG "reglaCss") 

Básicamente usamos un selector (Son los que están detallados justo abajo), e introducimos órdenes de estilo entre llaves({ }).

## **Tipos de Selectores:**
### **- Etiquetas globales (p,a,h1,...)**
Son las etiquetas globales que ya usabamos en HTML
HTML:
```html
<p>"Soy un parrafo"</p>
```
Accedemos a ella así en CSS
```css
p{
    ...
}
```
### **- Clases (.class)**
Se implementan así en HTML:
Se usa la palabra reservada "class" dentro de la apertura de la etiqueta en HTML.
```html
<p class="parrafo">"Soy un parrafo"</p>
```
Accedemos a ella así en CSS
```css
.parrafo{
    ...
}
```
### **- ID (#id)**
Se implementan así en HTML:
Se usa la palabra reservada "id" dentro de la apertura de la etiqueta en HTML.

```html
<p id="parrafo">"Soy un parrafo"</p>
```
Accedemos a ella así en CSS
```css
#parrafo{
    ...
}
```
## ¿Las etiquetas en HTML pueden tener clase e identificador al mismo tiempo? 
La respuesta es **SI**.

## **- Selector Universal**
Este selector, accede a todos los parámetros generales por defecto.
```css
* {
    ...
}
```

## Resetear valores por defecto de padding, margin con el Selector Universal
Para que no tengamos problemas de Responsive Design (Diseño responsivo, adaptable a cualquier tipo de pantalla)
```css
* {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

```

## **- PseudoClases (:pseudoclase)**
Define el estilo de un estado especial de un elemento.

Agregar al final de la clase :nombreAccion

En HTML 

```html
<p class="parrafo">"Soy un parrafo"</p>
```
Accedemos a ella así en CSS
```css
.parrafo:hover{
    ...
}
```

**EJEM**
* :root{}

Representa elemento HTML, con la especificidad de clase 
usado para anidar variables CSS
* :active

Se activa al hacer clic down
* :visited

Cambio visual cuando se visita un enlace
* :hover

Permite cambiar el estado de un elemento cuando elmause se sobrepone sobre él
* :first-child 

 Para afectar solo al primer hijo 
 Se coloca en el padre (ul) para afectar a su primer hijo (li)
* :last-child 

 Para afectar solo al ultimo hijo
* :not  

Negar una codiciones (ignorar una condicion) 
ejemplo .clase:not(last-child)
afecto a todos menos el ultimo
* :empty 

Ayuda a detectar cuando un elemento esta vacio. 
ejemplo .class:empty{background:yellow;} 
resaltar
* :nth-child() 

tag:nth-child(2){} 
Afectara al segundo elemento

## **- PseudoElementos (::pseudoelemento)**
Define el estilo de una parte específica de un elemento.

Agregar al final de la clase ::nombreAccion

En HTML 

```html
<p class="parrafo">"Soy un parrafo"</p>
```
Accedemos a ella así en CSS
```css
.parrafo::after{
    ...
}
```
-----
## **Modelo de Caja**
Así se le llama al modelo en el que está basado en CSS, todo dentro de cajas: 
![ Modelo de Caja](https://github.com/moralesvictorr/apuntesDesarrolloWeb/blob/master/images/boxStyleCss.PNG "boxModel") 
![ Modelo de Caja Desglozado](https://github.com/moralesvictorr/apuntesDesarrolloWeb/blob/master/images/boxStyleCss2.PNG "boxModel2") 
![ Ejemplo del Margin](https://github.com/moralesvictorr/apuntesDesarrolloWeb/blob/master/images/marginExample.PNG "marginExample") 

## **HERENCIA:**

### **Inherit**
 Este es un valor por medio de una keyword que especifica que, a la propiedad que se la apliquemos debe de heredar los valores de su elemento padre. Podemos decir que la palabra Inherit significa “Usa el valor de mi padre”, si el elemento padre no tiene definido dicho valor el navegador seguirá el DOM hasta que encuentre un elemento superior que lo contenga, y en ultima instancia de no tenerlo ningún elemento superior se aplicara el valor por defecto.


### **Initial** 
Este valor pertenece a la especificación CSS3 y cuando aplicamos a una propiedad el valor initial estamos dando el valor inicial y predefinido por el navegador en cuestión.

### **Upset** 
Este valor unset es una combinación entre inherit y initial, cuando utilizamos este valor en una propiedad esta tratara de heredar el valor de su elemento padre si este esta disponible, de no ser así este valor colocará el valor de la propiedad en su valor inicial, como si usáramos inherit e initial juntos.

## **Especificidad de los Selectores en CSS**
![ Epecificidad](https://github.com/moralesvictorr/apuntesDesarrolloWeb/blob/master/images/especificidadCSS.PNG "epecificidad") 

Puedes usar estos selectores dentro de las Etiquetas de HTML para luego darle estilo a etiquetas especificas en CSS.
Ejemplo en HTML 
```html
<header class="page-header"> </header>
```
Ejemplo en CSS
```css
.page-header {
    backgroung-color: #14a4a4
}
```

* No se recomienda el uso excesivo de ID
* No se recomiendan los estilos embebidos (Tienen mayor especificidad)
* No se recomienda el uso de !important (Porque puede ocasionar problemas graves de especificidad)

## **Combinadores**
![ Combinadores](https://github.com/moralesvictorr/apuntesDesarrolloWeb/blob/master/images/Combinadores.PNG "combinadores") 

A continuación: Ejemplo CSS (Colorea todos los P que estén inmediatamente después de un H2) 
```css
h2 +p {
    color: red;
}
```
Ejemplo Gráfico:
![ CombinadoresEjem](https://github.com/moralesvictorr/apuntesDesarrolloWeb/blob/master/images/combinadoresEjem.PNG "combinadoresEjem") 

## **Medidas:**

### **1) Absolutas**
Son unidades que están completamente definidas. Esto quiere decir, que su valor no depende de otro valor de referencia. 
Puede usarse: PX(Pixeles),CM(Centímetros), MM (Milímetros), PT(Puntos), IN(Pulgadas),... Entre otros.

### **2) Relativas**
Son unidades variables. Esto quiere decir, que su valor depende del tamaño del dispositivo, y/o, del valor heredado.
Puede Usarse: **Em** (Element): Representa el valor heredado del font-size del elemento.
              **Rem** (Root Element): Representa el tamaño del font-size del elemento raiz.
              **Longitudes de porcentaje de ViewPort** : VH (1/100 Altura del ViewPort),Vw (1/100 Ancho del ViewPort), Vmin (1/100 del valor mínimo de la altura y ancho del                         ViewPort), Vmax (1/100 del valor máximo de la altura y ancho del ViewPort)
              **%** (Porcentaje)
              ... Entre otros.
              
Ejemplo de medida EM vs Rem:
---------
Ejemplo de ViewPort:
----------

Se recomienda el uso de Medidas Relativas para cumplir con Responsive Design y Mobile First; solo usar medidas absolutas en casos concretos.
              

