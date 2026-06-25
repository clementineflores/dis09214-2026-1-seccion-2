

# "Supremacía de minorías"
## Katalina Ludueña y Clementine Flores

### Descripción objetiva
#### ¿Qué es el proyecto?
Nuestro proyecto habla de la supremacía del hombre cis-hetero sobre las personas no hombres —mujeres, lesbianas, trans, no binaries, entre otras— es una estructura que lleva siglos operando, y que aún hoy se traduce en incomodidad, miedo e inseguridad cotidiana. Desde esa realidad que habitamos, surge casi como un acto de supervivencia la posibilidad de imaginar otra, un mundo sin esa presencia opresora, donde por un momento respirar, aliviarse, existir sin el peso constante de esa mirada.

#### ¿Qué se ve en pantalla?
En la pantalla se despliega una dualidad —o más bien, una transición— entre dos realidades que han coexistido siempre, la del hombre hetero cis y la de las personas no hombres. El primer estado aparece apagado, frío, plano. Es el punto de partida. Al presionar ENTER, algo se rompe y se transforma en un trance, un umbral. Lo que emerge es una frase que Violeta Parra pronunció en una entrevista: "Soy una hormiguita que busca bajo la tierra dónde refugiar su corazón". Las personas no hombres somos esas hormiguitas —pequeñas no por naturaleza, sino porque así se nos ha intentado hacer sentir, constantemente, por una cultura que nos reduce y nos estrecha—.
Pero la hormiga también busca. Y esa búsqueda —bajo la tierra, dónde refugiar su corazón— habla de el impulso de encontrar refugio entre nosotrxs, entre otras personas no hombres, de ser entendidxs, escuchadxs y amadxs de una manera genuina y sin condiciones ni patriarcado de por medio, a lo que al presionar ENTER otra vez, se comienza a escuchar 

#### ¿Qué elementos visuales aparecen?
*  Figuras geométricas representadas como las personas no hombres (mujeres, lesbianas, trans, no binaries, etc) y los hombres hetero cis.
*  Símbolo de hombre (supremacía cis-hetero)
*  Frase dicha por Violeta Parra "Soy una hormiguita que busca bajo la tierra dónde poder refugiar su corazón", asociando "hormigas" como esta minoría no hombre.
*  Una imagen de un símbolo masculino y otra imagen de un lirio florecido.

#### Descripción conceptual
Nuestra idea central del proyecto es demostrar la realidad actual y no actual, de cómo las personas no hombres son oprimidas. Nuestra regla de oro en el proyecto funciona de esta manera: Mientras el mouse esté presionado, persiste la supremacía y opresión, pero al soltarlo, las personas no hombres pueden florecer libremente en este mundo ideal, o conviviendo con las mismas personas no hombres. La lógica con nuestra problemática se relaciona directamente en representación desde nosotras, como personas no hombres oprimidas por la supremacía diariamente, en cómo nosotras lo hemos vivido, y en que sabemos cómo puede ser vivenciarlo desde primera fuente. 

#### Input / Output y sistema
* **Inputs:**
* `mouseX`, `mouseY` → posición del mouse.
* `keyPressed`, `key`, `keyCode`, `ENTER`, `" "` → entrada del teclado (Enter y barra espaciadora).
* `windowWidth`, `windowHeight`, `windowResized()` → tamaño y cambios de la ventana.
* `loadImage()`, `loadFont()`, `loadSound()` → archivos externos cargados (imágenes, fuente y audio).
* `random()` → generación de valores aleatorios para posición, tamaño, velocidad, color y tipo de figura.

**Outputs:**
* `ellipse()`, `rect()`, `triangle()`, `line()` → figuras dibujadas en pantalla.
* `image()` → imágenes mostradas (símbolo masculino y fondo).
* `text()` → texto e instrucciones en pantalla.
* `micancion.play()`, `micancion.stop()` → reproducción y detención del audio.
* Cambio de `estado` (`pantallaOpresion`, `pantallaInicio`, `pantallaLiberacion`) → cambio visual entre pantallas.

#### Cómo se procesan y transforman?
Las entradas se procesan mediante funciones y condiciones del programa, el movimiento del mouse (`mouseX`, `mouseY`) se transforma en la posición del símbolo masculino y en la reacción de las figuras, que cambian su trayectoria cuando el cursor se acerca; las teclas (`ENTER` y espacio) son interpretadas por `keyPressed()` para modificar el valor de `estado`, cambiar pantallas y controlar la música; el tamaño de la ventana se procesa con `windowResized()` para reajustar el canvas; los archivos cargados (`imágenes`, `fuente`, `audio`) se utilizan como recursos visuales y sonoros; y los valores aleatorios (`random()`) se transforman en atributos de las figuras como tamaño, posición, velocidad, color y forma. Todo este procesamiento genera las salidas visuales y sonoras que aparecen en pantalla.

#### Pensamiento computacional
El pensamiento computacional del proyecto se observa en la descomposición, al dividir el programa en funciones y estados (pantallaOpresion, pantallaInicio, pantallaLiberacion); en el reconocimiento de patrones, al reutilizar comportamientos similares para todas las figuras mediante la clase Figura; en la abstracción, al representar distintos objetos con atributos comunes como posición, tamaño, velocidad y color; y en el diseño de algoritmos, al establecer instrucciones paso a paso para mover, rebotar, reaccionar al mouse, cambiar estados y controlar la música.

#### Explicación del sistema de interactividad
La interactividad ocurre mediante el uso del mouse y el teclado, el cursor controla la posición del símbolo masculino y modifica el comportamiento de las figuras cercanas, mientras que las teclas Enter o espacio permiten cambiar entre las distintas pantallas y activar o detener la música. El programa procesa continuamente estas entradas y genera respuestas visuales y sonoras en tiempo real, creando una relación dinámica entre las acciones del usuario y lo que sucede en la pantalla. El sistema responde a la acción de presionar y soltar el mouse. Cuando el usuario presiona el botón del mouse, la variable opresion cambia de estado, provocando que el símbolo masculino desaparezca, que el fondo se transforme en una imagen de un lirio floreciendo y que las figuras recuperen sus colores vibrantes. 
Al soltar el mouse, el estado vuelve a la normalidad, o más bien realidad. Reaparece el símbolo masculino, el fondo vuelve a ser gris y las figuras se muestran nuevamente en tonos grises mientras continúan reaccionando a la presencia del símbolo. De esta manera, la interacción permite que el usuario altere directamente el comportamiento visual de la composición, generando un contraste entre dos estados, uno asociado a la opresión y otro asociado a la liberación. El movimiento del cursor y el clic del mouse son los mecanismos que activan estos cambios y construyen el significado de la obra.

#### Referentes
Creado por nosotros mismos, de cómo representamos personalmente la vivencia de la supremacía del hombre hetero cis.

• Diagrama de Flujo: 

• Código de p5.js (Agregado en formato MarkDown): 
```javascript
let estado = 0;

let fuente;
let simbolomasculino;
let fondo;
let micancion;

// ARRAY
let noHombres = [];

// ------------------ CLASS ------------------

class Figura {

  constructor() {

    this.x = random(width);
    this.y = random(height);

    this.size = random(width * 0.02, width * 0.06);

    this.vx = random(-width * 0.002, width * 0.002);
    this.vy = random(-height * 0.002, height * 0.002);

    this.type = random([
      "ellipse",
      "rect",
      "triangle",
      "line"
    ]);

    this.col = color(
      random(255),
      random(255),
      random(255)
    );
  }

  mover() {

    this.x += this.vx;
    this.y += this.vy;

  }

  rebotar() {

    if (this.x < 0 || this.x > width) {
      this.vx *= -1;
    }

    if (this.y < 0 || this.y > height) {
      this.vy *= -1;
    }

  }

}

// ------------------ PRELOAD ------------------

function preload() {

  simbolomasculino = loadImage("simbolo masculino.png");

  fondo = loadImage("fondo.jpeg");

  fuente = loadFont("fuente/Noto.ttf");

  micancion = loadSound("cancion/ladygaga.mp3");

}

// ------------------ SETUP ------------------

function setup() {

  createCanvas(windowWidth, windowHeight);

  textFont(fuente);

  // Se crean las 200 figuras usando la clase

  for (let i = 0; i < 200; i++) {

    noHombres.push(new Figura());

  }

}

// ------------------ DRAW ------------------

function draw() {

  switch (estado) {

    case 0:
      pantallaOpresion();
      break;

    case 1:
      pantallaInicio();
      break;

    case 2:
      pantallaLiberacion();
      break;

  }

}
// ------------------ ESTADO 0 ------------------

function pantallaOpresion() {

  background(209, 192, 178);

  let tamSimbolo = width * 0.12;

  image(
    simbolomasculino,
    mouseX,
    mouseY,
    tamSimbolo,
    tamSimbolo
  );

  // Figuras
  for (let s of noHombres) {

    // Ahora usamos los métodos de la clase
    s.mover();
    s.rebotar();

    let d = dist(
      s.x,
      s.y,
      mouseX,
      mouseY
    );

    if (d < width * 0.12) {

      if (s.x < mouseX) {
        s.x -= 3;
      } else {
        s.x += 3;
      }

      if (s.y < mouseY) {
        s.y -= 3;
      } else {
        s.y += 3;
      }

      s.x += random(-2, 2);
      s.y += random(-2, 2);

    }

    dibujarFigura(s, color(120));

  }

  // Texto

  fill(0);
  noStroke();

  textAlign(LEFT, TOP);

  textSize(width * 0.025);

  text(
    "Presiona ENTER para continuar.",
    width * 0.30,
    height * 0.10,
    width * 0.50
  );

}

// ------------------ ESTADO 1 ------------------

function pantallaInicio() {

  background(255, 250, 201);

  fill(0);

  textAlign(CENTER, CENTER);

  textSize(width * 0.035);

  text(

    "Soy una hormiguita que busca bajo la tierra\n donde poder refugiar su corazón.",

    width / 2,

    height / 2 - 60

  );

  textSize(width * 0.03);

  text(

    "- Violeta Parra -\n\nPresiona ENTER para continuar",

    width / 2,

    height / 2 + 60

  );

}
// ------------------ ESTADO 2 ------------------

function pantallaLiberacion() {

  image(fondo, 0, 0, width, height);

  for (let s of noHombres) {

    // Métodos de la clase
    s.mover();
    s.rebotar();

    dibujarFigura(s, s.col);

  }

}

// ------------------ DIBUJO DE FIGURAS ------------------

function dibujarFigura(s, c) {

  fill(c);
  noStroke();

  if (s.type === "ellipse") {

    ellipse(
      s.x,
      s.y,
      s.size
    );

  }

  else if (s.type === "rect") {

    rectMode(CENTER);

    rect(
      s.x,
      s.y,
      s.size,
      s.size
    );

  }

  else if (s.type === "triangle") {

    triangle(

      s.x,
      s.y - s.size / 2,

      s.x - s.size / 2,
      s.y + s.size / 2,

      s.x + s.size / 2,
      s.y + s.size / 2

    );

  }

  else if (s.type === "line") {

    stroke(c);

    strokeWeight(
      max(2, width * 0.002)
    );

    line(
      s.x - s.size / 2,
      s.y - s.size / 2,
      s.x + s.size / 2,
      s.y + s.size / 2
    );

    line(
      s.x + s.size / 2,
      s.y - s.size / 2,
      s.x - s.size / 2,
      s.y + s.size / 2
    );

  }

}

// ------------------ CAMBIO DE ESTADOS ------------------

function keyPressed() {

  if (key === " " || keyCode === ENTER) {

    let estadoAnterior = estado;

    estado++;

    if (estado > 2) {
      estado = 0;
    }

    // Reproduce la música solo al pasar
    // del estado 1 al estado 2

    if (
      estadoAnterior === 1 &&
      estado === 2
    ) {

      if (!micancion.isPlaying()) {
        micancion.play();
      }

    }

    // Detiene la música
    // cuando vuelve al inicio

    if (
      estado === 0 &&
      micancion.isPlaying()
    ) {

      micancion.stop();

    }

  }

}

// ------------------ RESPONSIVE ------------------

function windowResized() {

  resizeCanvas(
    windowWidth,
    windowHeight
  );

}
```


• Link al sketch en P5.js en formato EDITABLE. 
(https://editor.p5js.org/kataluduena/sketches/qvp6PsBBr) 
