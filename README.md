# JavaScript-Info
# Mi_JavaScrip

Información de Interes acerca de **JavaScript**

> JavaScript es un Lenguaje de programación interpretado, orientado a objetos, débilmente tipado y dinámico que añade dinamismo e interactividad a una página Web.

# Variables

- **¿Qué es una variable y para que sirve?**

*Una Variable es un espacio en memoria donde podemos guardar información dependiendo de los tipos y estructuras de datos que soporte el lenguaje, una vez guardada podemos acudir a dicha variable a gtravés del nombre que se le haya asignado.*

- **¿Cuál es la diferencia entre declarar e inicializar una variable?**

*Declarar una variable es cuando le decimos a JavaScript que vamos a crear una variable con tal nombre. Mientras que inicializar es asignarle un valor a es variable.*

**Declarar variable:**

`let name;`
`const apellido;`

**Inicializar variable:**

`let name = "Pepito";`
`const apellido = "Perez";`

- **¿Cuál operador me permite sumar o concatenar?**

*El operador que nos permite sumar o concatenar es **+**. Este operador permite sumar números cuando los usamos con números. Pero cuando lo usamos con strings, lo que hace es unir o concatenar ambos strings.*

- **Determina el nombre y tipo de dato para almacenar en variables la siguiente información:**

1. Nombre: **string**
2. Apellido: **string**
3. Nombre de usuario en Platzi: **string**
4. Edad: **number**
5. Correo electrónico: **string**
6. Mayor de edad: **boolean**
7. Dinero ahorrado: **number**
8. Deudas: **number**

- **Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.**

```js
let nombre = "Jose Alfonso";
let apellido = "Basic";
let username = "jacarrillob";
let edad = 30;
let mail = "pepitoprueba@gmail.com";
let esMayorDeEdad = true;
let dineroAhorrado = 1000;
let deudas = 100;
```

- **Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:**

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

```js
let nombreCompleto = nombre + " " + apellido;
let dineroReal = dineroAhorrado - deudas;
```

## Funciones

- **¿Qué es una función?**

*Las funciones nos permiten encapsular (guardar) bloques de código para reutilizarlos y ejecutarlos en el futuro.  *
*Conjunto de declaraciones que realiza una tarea o calcula un valor, pero para que un procedimiento califique como una función, debe tomar alguna entrada y devolver una salida donde exista una relación obvia entre el entrada y la salida*

```js
function suma(number) {
  return number + number;
}
```
- **¿Cuándo me sirve usar una función en mi código?**

*Nos sirve cuando tenemos variables o bloques de código muy parecidos (con cambios que podrían ser parámetros y argumentos) que podemos encapsular para reutilizar más de una vez en el futuro.*

*También nos sirve para ordenar y mejorar la legibilidad de nuestro código.*

- **¿Cuál es la diferencia entre parámetros y argumentos de una función?**

*Las funciones reciben parámetros cuando las creamos. Y les enviamos argumentos cuando las ejecutamos.*

- **Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:**

```js
const name = "Joé Alfonso";
const lastname = "Carrillo";
const completeName = name + " " + lastname;
const nickname = "José";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```
```js
// Mi solución
function fullName(name, lastname) {
return name + ' ' + lastname
}

function saludar(name, lastname, nickname) {
const completeName = fullName(name, lastname)
console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
}
```

## Condicionales

- **¿Qué es un condicional?**

*Son la forma en que ejecutamos un bloque de código u otro dependien de alguna condición o validación.*

- **¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?**

*IF (else y else if), Switch
El codicional if (con else y else if) nos permite hacer validaciones completamente distintas (si así queremos) en cada validación o condional. En cambio, en el switch todos los cases se comparan con la misma variable o condición que definimos en el switch.*

- **¿Puedo combinar funciones y condicionales?**

*Sí. Las funciones pueden encapsular cualquier bloque de código, incluyendo condicionales.*

- **Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:**

```js
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos durante un año");
       break;
}
```

```js
// Mi solución

const tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion === "Basic") {
console.log("Puedes tomar casi todos los cursos durante un mes");
} else if (tipoDeSuscripcion === "Free") {
console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion === "Expert") {
console.log("Puedes tomar casi todos los cursos durante un año");
} else if (tipoDeSuscripcion === "ExpertPlus") {
console.log("Tú y alguien más pueden tomar TODOS los cursos durante un año");
} else {
console.log("No se reconoce la suscripción")
}
```

**- Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).**

```js

// Mi solución

```

## Ciclos

- **¿Qué es un ciclo?**

*La forma de ejecutar un bloque de código hasta que se cumpla cierta condición.*

- **¿Qué tipos de ciclos existen en JavaScript?**

*While, do while y for.*

- **¿Qué es un ciclo infinito y por qué es un problema?**

*Es cuando la validación de nuestros condicionales nunca se cumple y termina toteando (dañando) la aplicación (e.j. cuando el navegador ya no puede más de tanta ejecución de ese bloque de código).*

- **¿Puedo mezclar ciclos y condicionales?**

*Sí, aunque los ciclos son una especie de condionales, nada nos impide agregar más condionales dentro del ciclo.*

- ** Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:**

```js
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```

```js
// Mi solución
let i = 0;
while (i < 5) {
console.log("El valor de i es: " + i);
i++;
}
// ---------
let k = 10;
while (k >=2) {
console.log("El valor de k es: " + k);
k--;
}
```

**- Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.**

```js

// Mi solución
let sum;
while (sum !== "4") {
let resultado = prompt("Cuánto es 2 + 2");
sum = resultado;
}
```

## Listas

DEBO CONTINUAR AQUI - CLASE 7


- **¿Qué es un array?**


- **¿Qué es un objeto?**


- **¿Cuándo es mejor usar objetos o arrays?**


- **¿Puedo mezclar arrays con objetos o incluso objetos con arrays?**



- **Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.**

- ** Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).**


- **Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).**
