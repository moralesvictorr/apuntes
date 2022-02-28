# Apuntes de CSS - @moralesvictorr

----------------

![Regla CSS](https://github.com/moralesvictorr/apuntesDesarrolloWeb/blob/master/images/CSSRegla.PNG "reglaCss") 

## **- Etiquetas globales (p,a,h1,...)**
En HTML 

```html
<p>"Soy un parrafo"</p>
```
Accedemos a ella así en CSS
```css
p{
    ...
}
```
## **- Clases (.class)**
En HTML 

```html
<p class="parrafo">"Soy un parrafo"</p>
```
Accedemos a ella así en CSS
```css
.parrafo{
    ...
}
```
## **- ID (#id)**
En HTML 

```html
<p id="parrafo">"Soy un parrafo"</p>
```
Accedemos a ella así en CSS
```css
#parrafo{
    ...
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
