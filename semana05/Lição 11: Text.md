#Avaliação
//
``` javascript
var backdrop = createSprite(200,200);
backdrop.setAnimation("rainbow");
var flyer = createSprite(200,200);
flyer.setAnimation("wing_bot");

function draw() {
  //move left when the left arrow is pressed
  if (keyDown("left")) {
    flyer.x = flyer.x - 3;
  }
  //move right when the right arrow is pressed
  if (keyDown("right")) {
    flyer.x = flyer.x + 3;
  }
  //move up when the up arrow is pressed
  if (keyDown("up")) {
    flyer.y = flyer.y - 3;
  }
  //move down when the down arrow is pressed
   if (keyDown("down")) {
    flyer.y = flyer.y + 3;
  }
  drawSprites();
} 
```
Na avaliação da lição 11 eu adicionei os códigos condicionais com o keyDown para fazer o sprite se mover pela tela de animação.

#Desafio
//
``` javascript
var peixe1 = createSprite(100, 150);
var peixe2 = createSprite(300, 250);
var tartaruga = createSprite(200, 330);

var bolha1 = 80;
var bolha2 = 200;
var bolha3 = 320;

tartaruga.setAnimation("tartaruga");
  tartaruga.scale = 0.4;
  
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

  
  if (keyDown("left")) {
    tartaruga.x = tartaruga.x - 3;
    tartaruga.setAnimation("tartarugaesq");
  }
 
  if (keyDown("right")) {
    tartaruga.x = tartaruga.x + 3;
    tartaruga.setAnimation("tartaruga");
  }
 
  if (keyDown("up")) {
    tartaruga.y = tartaruga.y - 3;
    tartaruga.setAnimation("tartarugacim");
  }
  
   if (keyDown("down")) {
    tartaruga.y = tartaruga.y + 3;
    tartaruga.setAnimation("tartarugabaix");
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

  drawSprites();
}
```
No desafio eu usei o código do aquário que eu fiz no desafio anterior e animei a tartaruga utilizando animações para cada movimento como na segunda parte do desafio e comandos de keyDown.
