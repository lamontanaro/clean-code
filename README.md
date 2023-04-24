
#  Conceptos de "Clean Code" de Robert Martin en JavaScript

"Clean Code" es un conjunto de principios y prácticas que se centran en escribir código fácil de leer, entender y mantener. A continuación, explicaré algunos de los principales conceptos y cómo aplicarlos en JavaScript:

1. **Nombres significativos de variables y funciones**
   Las variables y funciones deben tener nombres significativos que indiquen claramente su propósito y función. En lugar de nombres cortos y genéricos, utiliza nombres descriptivos y precisos. Por ejemplo, en lugar de `x`, usa `total` para una variable que almacena el total de una factura:
   
   
   ```
   // Malo
   let x = 0;

   // Bueno
   let total = 0;
   ```

2. **Funciones cortas y con una sola responsabilidad**
   Las funciones deben ser cortas y tener una sola responsabilidad. Si una función hace demasiadas cosas, es difícil de entender y mantener. En lugar de eso, descompón la función en funciones más pequeñas y especializadas. Por ejemplo, en lugar de una función larga que valida y envía un formulario, divide la función en dos partes: una que valida los campos del formulario y otra que envía el formulario:
   ```
   // Malo
   function enviarFormulario() {
     // código de validación
     // código de envío
   }

   // Bueno
   function validarFormulario() {
     // código de validación
   }

   function enviarFormulario() {
     // código de envío
   }
   ```

3. **Evitar anidación excesiva**
   La anidación excesiva hace que el código sea difícil de leer y entender. En lugar de eso, utiliza nombres significativos y crea funciones más pequeñas para evitar anidaciones profundas. Por ejemplo, en lugar de anidar muchas condicionales, puedes crear funciones que encapsulen esas condiciones:
   ```
   // Malo
   if (condicion1) {
     if (condicion2) {
       if (condicion3) {
         // hacer algo
       }
     }
   }

   // Bueno
   if (todasLasCondicionesSonVerdaderas()) {
     // hacer algo
   }
   
   func todasLasCondicionesSonVerdaderas(){
    return condition1 && condition2 && condition3
   }
   ```

4. **Escribir código legible y fácil de entender**
   El código debe ser fácil de leer y entender, incluso para personas que no han trabajado en el proyecto anteriormente. Utiliza sangrías, espacios y comentarios para mejorar la legibilidad. Por ejemplo:
   ```
   // Malo
   if(condicion==true){accion();}

   // Bueno
   if (condicion) {
     accion();
   }
   ```

5. **Usar pruebas unitarias**
   Las pruebas unitarias son fundamentales para asegurarse de que el código funciona correctamente y se puede mantener a lo largo del tiempo. Escribir pruebas unitarias ayuda a identificar errores temprano y a mantener la calidad del código a largo plazo. Por ejemplo, si tienes una función que realiza una suma, escribe pruebas unitarias para verificar que la función retorna el resultado correcto:
   ```
   // Malo
   function suma(a, b) {
     return a + b;
   }

   // Bueno
   function suma(a, b) {
     return a + b;
   }

   // Pruebas unitarias
   describe("suma", () =>
