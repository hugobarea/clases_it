# Apuntes

- [Apuntes](#apuntes)
  - [Control structures](#control-structures)
    - [If](#if)
    - [switch/case](#switchcase)
    - [for](#for)
    - [while](#while)
  - [Grabbing elements from ID](#grabbing-elements-from-id)
    - [innerHTML, value and src](#innerhtml-value-and-src)
  - [Alerts, prompts](#alerts-prompts)
  - [Converting data types](#converting-data-types)
  - [String manipulation functions](#string-manipulation-functions)
  - [Arrays](#arrays)
  - [setTimeout and setInterval](#settimeout-and-setinterval)

## Control structures

### If

```js
if(condition1){ // this code only runs if condition is true
    statement1;
    statement2;
}

else if(condition2){
    statement1;
    statement2;
}

else{
    statement1;
    statement2;
}
```

### switch/case

```js

var n = prompt("Dame un número");

switch(n){
    case 1: // if(n == 1)
        statement1;
        break;
    
    case 2: // else if(n == 2)
        statement2;
        break;
    
    case default: // else
        statement3;
        break;
}
```

### for

```js
for (var i = 0; i < x; i++){ // i++ -> i = i + 1;
    statement1;
} 
```

### while

```js

while(condition){ // mientras que condition sea true
    statement1;
} 
```

## Grabbing elements from ID
  
```html
<p id="parrafo"></>
<img id="imagen" src="fortnite.jpeg">

<script>
    var mi_parrafo = document.getElementById('parrafo');
    var mi_imagen = document.getElementById('imagen');

    mi_parrafo.innerHTML = 'Hola Mundo';
    mi_imagen.src = 'fortnite2.jpeg';
</script>
```

### innerHTML, value and src

HTML

```html
<p id="parrafo"></p>
<input id="whatever_data"> // notice input does not have a closing tag
<img id="imagen" src="fortnite.jpeg"> // and neither do images

```

Javascript

```js
    var mi_parrafo = document.getElementById("parrafo");
    mi_parrafo.innerHTML = 'Hello World'; // <p id="parrafo">Hello World</p>

    var mi_input = document.getElementById("whatever_data").value; // will store element's value into mi_input

    var mi_imagen = document.getElementById("imagen")
    mi_imagen.src = "fortnite2.jpeg" // will change image file
```

## Alerts, prompts

```js
alert("Bienvenido a la página");
var x = prompt("Introduce un número"); // prompt returns a string
```

## Converting data types

```js
var x = "4";
var x = parseInt(x); // x = 4

var y = 4;
y.toString(); // y = "4";
```

## String manipulation functions

```js
// slice, charAt, substr

var x = "Hello World";

var y = x.slice(0,5); // "Hello" slices between first and last character non-inclusive

y = x.charAt(0) // x = "H" char at position given
y = x.charAt(5) // x = " "

y = x.substr(0, 4); // x = "Hell" takes substring from given position (0) of length 4

```

## Arrays
  
```js
// Valid and invalid arrays

var array1 = [0, 1, 2]; // same data type so valid
var array2 = [0, "1", 2]; // invalid as not same data type

// Array positions

var array3 = [1, 3, 5, 7];

var x = array3[0] // x = 1;

// Array length

var length = array3.length;

// Iterate over array

for(var i = 0; i < array.length; i++){ // runs for i = 0, 1, 2
            alert(array[i]);   
        }

```

## setTimeout and setInterval

```js
// Consider the following function:

function helloworld(){
    alert("Hello World");
}


// setTimeout

setTimeout(helloworld, 1000); // will run the function helloworld() once 1000ms after the website is loaded

// setInterval

setInterval(helloworld, 1000); // will run the function helloworld() every 1000ms


// Clearing intervals

// store the interval in a variable
var event = setInterval(helloworld, 1000);

// use the function clearInterval
event = clearInterval(helloworld);
```
