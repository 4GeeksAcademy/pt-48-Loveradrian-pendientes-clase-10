
Resumen y ejemplos de lo que encontraremos: 

Video explicativo: https://youtu.be/kVGsrqYZZxM

- assignment operartor solo asigna, no compara valores unos con otros. 
- equality operator compara los datos de ambos lados, haciendo una conversion de datos si es necesario.
- strict equality operator compara sin hacer la conversion entre los datos. 

- let myVal = 5; // asignamos el valor numero 5 a la variable myVal

- 3 == '3' //true, ya que el equality operator hace una conversion de datos entre ellos, y los compara
  3 == 2 // false, ya que aunque tambien hace la conversion, dato numerico 3 es distinto de dato numerico 2. Tambien aplicaria si fueran datos de texto '3' y '2'

- 3 === 3 // true, ya que 3 y 3 son iguales, tanto en valor como en tipo de dato.
- 3 === 7 // false, ya que aunque son el mismo tipo de dato (numerico), 3 no es igual a 7.

-forEach: 

El método forEach pasa una función para cada elemento del arreglo 
junto con los siguientes parámetros:

Valor actual (requerido) - El valor del elemento actual del arreglo
Index (opcional) - El número de índice del elemento actual
Arreglo (opcional) - El objeto del arreglo al que pertenece el elemento actual

En primer lugar, para recorrer un arreglo utilizando el método forEach, 
se necesita una función callback (o función anónima)
La función se ejecutará para cada elemento del arreglo. Debe tomar al menos un parámetro 
que represente los elementos del arreglo:

const numeros = [1, 2, 3, 4, 5];

numeros.forEach(numero => console.log(numero)); //Para cada elemento en "numeros", imprimir el elemento.

Esta funcion deberia imprimir cada elemento del array. 

-map: 

-map:
El metodo map() se utiliza para crear un nuevo array a partir de uno ya existente,
aplicando una funcion a cada uno de los elementos del array inicial. 

const numeros = [1, 2, 3, 4];
const duplicar = numeros.map(elemento => elemento * 2);
console.log(duplicar); 


-filter:

El metodo filter() toma cada elemento de un array y aplica una instrucción condicional 
en el. Si este condicional retonar true, el elemento se agrega al array final.
Si la condicion retorna false, el elemento no se envia al array final. 

const numeros = [1, 2, 3, 4];
const pares = numeros.filter(item => item % 2 === 0);
console.log(pares); // [2, 4]

-reduce: 

El metodo reduce() reduce los valores de un array a un solo valor. 
Para obtener el valor de salida, ejecuta una funcion reductora en cada elemento
del array. 

const arr = [1, 2, 3, 4]; 

arr.reduce(callback[, valorInicial])

El argumento de callback es una función que se llamará una vez por 
cada elemento del arreglo. Esta función toma cuatro argumentos, 
pero a menudo solo se usan los dos primeros.

-acumulador: el valor devuelto de la iteración anterior
-valorActual: el elemento actual del arreglo
-índice: el índice del elemento actual
-arreglo: el arreglo original en la que se llamó a reduce

El argumento valorInicial es opcional. Si se proporciona,
se utilizará como valor acumulador inicial en la primera llamada a la función callback.

const numeros = [1, 2, 3, 4];
const suma = numeros.reduce(function (resultado, elemento) {
  return resultado + elemento;
}, 0);
console.log(suma); // 10
