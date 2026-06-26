# sesión 10 - 19/06
#### SONIDOS EN P5.js
## Introducción
En esta clase se aborda el uso del sonido y la síntesis de audio en **p5.js** dentro del contexto de **Creative Coding** y **Pensamiento Computacional**. Se aprenderá a cargar sonidos, reproducirlos, controlarlos y generar audio mediante síntesis utilizando la librería `p5.sound()`.

---

# Carga de sonidos en p5.js
Para trabajar con sonido en p5.js, primero es necesario cargar archivos de audio dentro del proyecto.

## Paso 1: Subir sonidos a p5.js
Para agregar archivos de audio al proyecto:

1. Hacer clic en la pequeña flecha `>` ubicada en la esquina superior izquierda del editor (debajo del botón **Play**).
2. Hacer clic en el icono `+` o el menú desplegable junto a **Files**.
3. Seleccionar **Upload file**.
4. Arrastrar o seleccionar el archivo de sonido.

### Formatos recomendados

* `.mp3`
* `.wav`

### Recomendaciones
* Utilizar nombres cortos.
* Escribir en minúsculas.
* Evitar espacios.
* Crear una carpeta llamada `ASSETS`.

---

# Declarar y precargar sonidos
## Paso 2: Declarar y precargar el sonido

Primero se crea una variable global para almacenar el sonido.

Luego se utiliza `preload()` para cargar el archivo mediante `loadSound()`.

```javascript
let sonido;

function preload() {
    sonido = loadSound("ASSETS/audio.mp3");
}
```

La función `preload()` asegura que el archivo se cargue completamente antes de ejecutar el programa.

---

# Activar el sonido

## Paso 3: Reproducir sonido

Para iniciar un sonido:

```javascript
nombreVariable.play();
```

Ejemplo:

```javascript
function setup() {
    sonido.play();
}
```

Esto hará que el sonido comience automáticamente al iniciar el sketch.

Sin embargo, es recomendable activar el sonido mediante una interacción del usuario, por ejemplo:

```javascript
function mousePressed() {
    sonido.play();
}
```

Muchos navegadores bloquean la reproducción automática por razones de seguridad.

---

# Métodos para controlar el sonido

## Reproducción

### Reproducir una vez

```javascript
nombreVariable.play();
```

### Reproducir en bucle

```javascript
nombreVariable.loop();
```

### Detener sonido

```javascript
nombreVariable.stop();
```

### Pausar sonido

```javascript
nombreVariable.pause();
```

---

## Volumen

Permite modificar el volumen:

```javascript
nombreVariable.setVolume(valor);
```

Valores posibles:

* `0.0` → silencio
* `1.0` → volumen máximo

Ejemplo:

```javascript
sonido.setVolume(0.5);
```

---

## Velocidad de reproducción

Permite modificar la velocidad:

```javascript
nombreVariable.rate(valor);
```

Ejemplos:

| Valor | Resultado          |
| ----- | ------------------ |
| `0.5` | Más lento y grave  |
| `1.0` | Normal             |
| `2.0` | Más rápido y agudo |

---

# Métodos de consulta o estado del sonido

## Verificar si está reproduciéndose

```javascript
nombreVariable.isPlaying();
```

Retorna:

```javascript
true
```

o

```javascript
false
```

---

## Verificar si está pausado

```javascript
nombreVariable.isPaused();
```

---

## Verificar si está en loop

```javascript
nombreVariable.isLooping();
```

---

## Obtener tiempo actual

```javascript
nombreVariable.currentTime();
```

Ejemplo:

```javascript
12.45
```

---

## Obtener duración total

```javascript
nombreVariable.duration();
```

Ejemplo:

```javascript
180.0
```

---

## Obtener volumen actual
```javascript
nombreVariable.getVolume();
```

Retorna un valor entre
```javascript
0.0 → 1.0
```

---

## Obtener velocidad actual
```javascript
nombreVariable.getRate();
```

Ejemplo:

```javascript
1.0
```

---

# Actividades y ejemplos

## Desafío: Radio Play/Pause
Objetivo:
Crear un sistema capaz de reproducir y pausar audio mediante botones o interacciones del usuario.

---

## Ejemplo: Beyonce Game
Ejercicio práctico basado en interacción gráfica y sonido.

---

## Ejemplo: Piano Pad
Simulación de un instrumento musical utilizando teclas.
Versiones:
* Piano sin optimizar
* Piano optimizado
* Teclado clásico

---

# Introducción a la síntesis de audio
La síntesis de audio permite generar sonidos artificialmente sin utilizar archivos previamente grabados.
La librería `p5.sound()` permite crear sintetizadores básicos.

---

# Componentes de un sintetizador básico

## 1. Oscilador (`p5.Oscillator`)
Es el componente que genera el sonido.

Tipos de ondas:

### Sine
Onda senoidal:
* Sonido suave
* Similar a una flauta

### Triangle
Onda triangular:
* Sonido intermedio

### Sawtooth
Onda diente de sierra:
* Sonido brillante
* Típico de sintetizadores de los años 80

### Square
Onda cuadrada:
* Sonido retro
* Similar a videojuegos de 8 bits

---

## 2. Frecuencia (Frequency)
Controla qué tan rápido vibra una onda.
* Mayor frecuencia → sonido agudo
* Menor frecuencia → sonido grave

Se mide en:
```text
Hertz (Hz)
```

---

## 3. Amplitud (Amplitude)

Controla el volumen percibido.

Valores:

* `0.0` → silencio
* `1.0` → máximo volumen

---

# Ejemplo de sintetizador básico

Utilizando `p5.sound()` se puede crear un sintetizador simple que permita modificar:

* Frecuencia
* Amplitud
* Tipo de onda

---

# Recursos adicionales

## Learning Synths

https://learningsynths.ableton.com/

## Playground interactivo

https://learningsynths.ableton.com/en/playground

## Tutoriales de sonido

https://www.youtube.com/playlist?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW

---

# Conclusión

El uso de sonido en p5.js permite incorporar experiencias más inmersivas e interactivas en proyectos de Creative Coding.

Mediante archivos de audio y síntesis de sonido es posible desarrollar:

* Instrumentos digitales
* Interfaces interactivas
* Juegos
* Experiencias multimedia
* Proyectos creativos

```
```

