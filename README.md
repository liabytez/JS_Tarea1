# JS_Tarea1
Ejercicios varios de JavaScript

## Autora
Hailie Mountain

## Enunciados

### Ejercicio 1: Mostrar un mensaje al hacer clic
Crea un botón con id "btn" y un párrafo con id "resultado". Al pulsar el botón, que el párrafo muestre: "¡Hola Clase!"
 
getElementById("btn") → captura el botón
getElementById("resultado") → captura el párrafo
.addEventListener("click", function() { ... })
.innerHTML = "texto"
 

### Ejercicio 2: Cambiar el color del texto

Un párrafo con id "texto" y un botón. Al pulsar el botón, el párrafo debe ponerse en rojo usando element.style.color = "red".
const parrafo = document.getElementById("texto")
parrafo.style.color = "red"
 

### Ejercicio 3: Contador de clics

Declara una variable let contador = 0. Cada vez que se pulse el botón, el contador sube 1 y se muestra el número en pantalla. Pista: la variable debe estar fuera del evento.
let contador = 0 → declarar FUERA del evento
contador = contador + 1 → dentro del evento
resultado.innerHTML = contador
 

### Ejercicio 4: Mostrar la hora actual

Al pulsar un botón, mostrar la hora actual en un párrafo. Usa new Date().toLocaleTimeString() para obtener la hora del sistema.
const ahora = new Date()
const hora = ahora.toLocaleTimeString()
resultado.innerHTML = hora
 

### Ejercicio 5: Saludo personalizado con input

Un campo <input> con id "nombre", un botón y un párrafo. Al pulsar el botón, mostrar: "¡Hola, [nombre]!" usando lo que el usuario escribió en el input.
const input = document.getElementById("nombre")
const valor = input.value → lo que hay escrito
resultado.innerHTML = "¡Hola, " + valor + "!"
 

### Ejercicio 6: Calculadora de suma simple

Dos inputs numéricos (id "num1" y "num2") y un botón "Sumar". Al pulsar, mostrar la suma. Cuidado: input.value devuelve texto, hay que convertirlo con Number().
const a = Number(document.getElementById("num1").value)
const b = Number(document.getElementById("num2").value)
let suma = a + b
resultado.innerHTML = "La suma es: " + suma
 

### Ejercicio 7: Botón de ocultar / mostrar

Un párrafo visible y un botón "Ocultar". Al pulsar, el párrafo desaparece y el botón cambia a "Mostrar". Al volver a pulsar, el párrafo reaparece. Usa una variable let visible = true y un if / else.
let visible = true
if (visible) {
  parrafo.style.display = "none"
  boton.innerHTML = "Mostrar"
  visible = false
} else { ... }
 

### Ejercicio 8: Cambiar imagen al hacer clic

Un <img> con id "foto" mostrando una imagen inicial. Al pulsar el botón, cambia a otra imagen diferente. Usa element.src para cambiar la fuente. Puedes usar imágenes de https://picsum.photos.
const img = document.getElementById("foto")
img.src = "https://picsum.photos/200/150?random=2"  → Siempre da una imagen aleatoria
 

### Ejercicio 9: Lista de tareas sencilla

Un input de texto, un botón "Añadir" y un <ul> vacío con id "lista". Al pulsar el botón, el texto del input se añade como un nuevo <li> en la lista, y el input se vacía.
const lista = document.getElementById("lista")
const texto = input.value
lista.innerHTML = lista.innerHTML + "<li>" + texto + "</li>"
input.value = "" → vaciar el campo
 

### Ejercicio 10: Semáforo interactivo

Tres círculos de colores (rojo, naranja, verde) creados con CSS. Un botón "Siguiente". Cada vez que se pulse, el semáforo avanza al siguiente estado y se muestra el texto correspondiente ("Stop", "Atención", "Adelante"). Usa un array y una variable let estado = 0.
const estados = ["rojo", "naranja", "verde"]
const textos = ["Stop", "Atención", "Adelante"]
let estado = 0
— al pulsar:
estado = (estado + 1) % 3
resultado.innerHTML = textos[estado]
