#Avaliação
//
``` javascript
var backdrop = createSprite(200,200);
backdrop.setAnimation("sci_fi");
var dinosaur = createSprite(200, 350);
dinosaur.scale = 0.2;
dinosaur.setAnimation("tyrannosaurus");

function draw() {
  //move the dinosaur up
  dinosaur.y = dinosaur.y - 5;
if (dinosaur.y < 250) {
dinosaur.setAnimation("pterodactyl");  
}

  //if it gets to the sky, turn it into a pterodactyl

  //draw everything
  drawSprites();
}
```
Na avaliação da lição 10 foi pedido que usando a função de condição mudasse a animação quando o sprite atingisse certo ponto na tela.

#Desafio
//
1º
``` javascript
var balloon = createSprite(200, 200);
var pop= createSprite(200,200);
balloon.setAnimation("balloon");
balloon.scale = 0.1;~
pop.setAnimation("pop");
pop.visible = false;

function draw() {
  // Draw Background
  background("white");
  // Update Values
  balloon.scale = balloon.scale + 0.001;
if (balloon.scale > 0.5) {
  balloon.visible = false;
  pop.visible = true;
  }  
  // Draw Animations
  drawSprites();
}
```
2º 
``` javascript
var peixe1 = createSprite(100, 150);
var peixe2 = createSprite(300, 250);
var tartaruga = createSprite(200, 330);

var bolha1 = 80;
var bolha2 = 200;
var bolha3 = 320;

function draw() {
  background('lightblue');

  fill('darkgreen');
  rect(0, 380, 400, 120);

  fill('gray');
  ellipse(50, 420, 60, 40);
  ellipse(120, 440, 80, 50);
  ellipse(330, 430, 70, 45);

  fill('green');
  rect(70, 350, 10, 70);
  rect(90, 340, 10, 80);
  rect(300, 350, 10, 70);
  rect(320, 330, 10, 90);

  fill('pink');
  arc(200, 420, 50, 40, 180, 360);

  peixe1.setAnimation("peixeverde");
  peixe1.scale = 0.5;
  peixe1.x = peixe1.x + 2;
  peixe1.rotation = 180;

  if (peixe1.x > 420) {
    peixe1.x = 0;
  }

  peixe2.setAnimation("peixerosa");
  peixe2.scale = 0.8;
  peixe2.x = peixe2.x - 2;
  peixe2.rotation= 360;

  if (peixe2.x < -20) {
    peixe2.x = 420;
  }
  
  tartaruga.setAnimation("tartaruga");
  tartaruga.scale = 0.4;
  tartaruga.x = tartaruga.x + 1;

  if (tartaruga.x > 420) {
    tartaruga.x = -20;
  }

  noStroke();
  fill('white');

  ellipse(bolha1, 300, 15, 15);
  ellipse(bolha2, 350, 12, 12);
  ellipse(bolha3, 280, 10, 10);

  bolha1 = bolha1 - 1;
  bolha2 = bolha2 - 1;
  bolha3 = bolha3 - 1;

  if (bolha1 < 50) {
    bolha1 = 350;
  }

  if (bolha2 < 50) {
    bolha2 = 400;
  }

  if (bolha3 < 50) {
    bolha3 = 330;
  }
```
  drawSprites();
}

Na primeira parte do desafio da lição 10 foi pedido que utilizando a função de condição e a visibilidade dos sprites alterássemos a animação, já na segunda parte foi uma animação livre.  
