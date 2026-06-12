# sesión 09 - 12/06
# ESTADOS Y CÁMARA WEB
## ¿CÓMO CREAR UN SKETCH CON ESTADOS DIFERENTES?
### PASO 1
* Crear y definir variable estados : Al principio de tu código (fuera de las funciones), debes crear una
variable que guarde en qué pantalla nos encontramos. Empezará en 0.
* Ejemplo : let estado = 0; // 0 = Inicio, 1 = Experiencia, 2 = Final

### PASO 2 
* Configurar el lienzo (functionsetup) : Creamos el lienzo de fondo donde va a ocurrir toda la magia.

### PASO 3
* Crear la estructura del estado (function draw) : Aquí usamos un switch. Dependiendo del valor de la variable estado, el programa
dibujará una cosa u otra.

### PASO 4
* Programar visualmente cada estado (funciones propias) : Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente
para que se note el cambio.

### PASO 5
* La lógica del cambio y del reinicio : Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función mousePressed() Cada vez que hagas un clic, la variable
aumentará. Si llega a 3 (después del estado 2), volverá a 0.
* [ Ejemplo en p5.js ](https://editor.p5js.org/PoliMujica/sketches/9vHePO158)

# FORMAS DE CAMBIAR DE UN ESTADO A OTRO

#### 1.  Interacción con el teclado
1.1. Por barra espaciadora o Enter
1.2. Por teclas específicas (ej. Números):
*  Puedes hacer que la tecla 1 te lleve al inicio, la 2 a la experiencia y la 3 al final.
* [ Ejemplo en p5.js ](https://editor.p5js.org/PoliMujica/sketches/4lzOYE8KL)

#### 2.  Botones Reales
2. En lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de HTML usando la librería de p5.js. Esto es mucho más profesional para menús.
* [ Ejemplo en p5.js ](https://editor.p5js.org/PoliMujica/sketches/peTm3oGty)

#### 3. Zonas de Clic (Botones dibujados con rect o ellipse)
3. Si no quieres usar botones de HTML y prefieres dibujar tus propios botones con rect(), puedes evaluar si el mouse estaba dentro de esa caja al hacer clic.
* [ Ejemplo en p5.js ](https://editor.p5js.org/PoliMujica/sketches/iw-gjFhK8)

#### 4. Interacciones Automáticas (Por Tiempo)
4. Por Tiempo (Temporizador): Ideal para una pantalla de introducción (Splash Screen) que dura 3 segundos y pasa sola al menú.
* [ Ejemplo en p5.js ](https://editor.p5js.org/PoliMujica/sketches/_AunxbPWQ)

# CÁMARA WEB
## createCapture(VIDEO);
1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de
tu cámara web.
2. Inicializar la cámara en el function setup() utilizamos el comando especial createCapture(VIDEO) esto le pedirá permiso al navegador para encender la cámara del computador. También definimos tamaño con
captura.size(x,y); y es muy importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.
3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.
* [ Ejemplo en p5.js ](https://editor.p5js.org/PoliMujica/sketches/PhkuD7kWU)

# EJEMPLOS CÁMARA INTERACTIVA
* [ ON/OFF ](https://editor.p5js.org/PoliMujica/sketches/Xdk0YBVbQ)
* [ FILTROS ](https://editor.p5js.org/PoliMujica/sketches/sK_BYepGn)
* [ LOADPIXELS ](https://editor.p5js.org/PoliMujica/sketches/OVsazOghk)
* [ PINCEL DE PIXELES ](https://editor.p5js.org/PoliMujica/sketches/cYCPjuXft)
* [ PIXELES REACCIONAN AL VOLUMEN DEL MIC ](https://editor.p5js.org/PoliMujica/sketches/L9QBzREF3)
  
