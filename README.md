PImage img; //carga la imagen
float x=0; //controla la posición horizontal del circulo

color c1 = color(255, 0, 255); // Color arriba (magenta)
color c2 = color(0, 255, 255); // Color abajo (azul)

void setup() {
  fullScreen(); //pantalla completa
  frameRate(30); //cuadros por segundo para la animación
  noCursor(); //quita el cursor de la pantalla
  img = loadImage("KioskoLerma.JPG"); //la imagen jijiji
}

void draw() {
  background(255, 0, 100);//Color rojo rosado del estado de lerma
  image(img, 400, 50);// Mi imagen y su posición

  fill(178, 235, 242);//relleno azul cielo para la elipse
  ellipse(x, height/2, 600, 100); //hace que se mueva el circulo
  noStroke(); //sin contorno
  x+=1;
  if (x>width) {
    x=0;
  }
  textAlign(CENTER, CENTER); //alinea el texto al centro del circulo
  fill(255, 255, 255); //blanco
  textSize(30);
  text("SALA CONMEMORATIVA DE LA HISTORIA DE LERMA", x, height/2);//centro del circulo

  textAlign(CENTER, TOP); //centra el texto
  textSize(30);
  fill(0, 200, 255); //color azul cian
  text("MUSEO DE ARTE CONTEMPORANEO DE LERMA", 800,100);

  textAlign(RIGHT, BOTTOM); //Acomoda los datos hasta abajo
  textSize(25);
  fill(255,255,255); //blanco
  text("José Pedro Balmaceda Pascal", width - 10, height - 10);
  fill(255,255,255); //blanco otra vez
  text("10 al 29 de septiembre de 2024", width - 10, height - 30);
}
