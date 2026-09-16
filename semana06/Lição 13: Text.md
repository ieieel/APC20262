#Avaliação 
// 
```javascript
var fish = createSprite(200, 200);
fish.setAnimation("fishR");

function draw() {
  background("blue");
  //Use a the correct block inside each conditional statement to make the three following movements:
  //If the user presses the right arrow key, move the fish to the right.
  if (keyWentDown("right")) {
  fish.velocityX = 4;
  }
  
  
  //If the fish gets to the right-hand side of the screen, move the fish to the left.
  if (fish.x > 400) {
    fish.velocityX = -4;
    fish.setAnimation("fishL");
  }
  
  //If the fish gets to the left-hand side of the screen, move the fish to the right.
  if (fish.x < 0) {
fish.velocityX = +4;
fish.setAnimation("fishR");
  }  

  //The fish should always be facing the same direction it's moving, so you will also need to
  //update the fish's animation inside each of the conditional statements.
  
  // Draw the fish.
  drawSprites();
}
```
Na avaliação a lição 13 eu utilizei a propriedade velocity junto com as condicionais para fazer o peixe se movimentar pela tela indo e voltando conforme ele chegasse em cada extremidade.

#Desafio
//
```javascript
var alien = createSprite(50,200);
var space = createSprite(200, 200);
space.setAnimation("space");
var flag1 = createSprite(50, 50);
flag1.setAnimation("yellow_flag");
var flag2 = createSprite(350, 50);
flag2.setAnimation("yellow_flag");
var flag3 = createSprite(350, 350);
flag3.setAnimation("yellow_flag");
var flag4 = createSprite(50, 350);
flag4.setAnimation("yellow_flag");
alien.setAnimation("alien");
  alien.depth=7;
alien.velocityX = 0;
alien.velocityY = -3;


function draw() {
  if (alien.y < 50) {
alien.velocityX = 7;
alien.velocityY = 0;
  }
  if (alien.x > 350) {
alien.velocityY = 7;
alien.velocityX = 0;
  }
  if (alien.y > 350) {
alien.velocityX = -7;
alien.velocityY = 0;
  }
  if (alien.x < 50) {
alien.velocityY = -7;
alien.velocityX = 0;

if (alien.y < 50) {
  alien.velocityX = 7;
alien.velocityY = 0;
}

  }
   
    drawSprites();
}
```
No desafio utilizei o velocity X e Y para animar o alien da lição e passei um tempo tentando descobrir como fazer ele entrar em loop (era só repetir o primeiro 'if'.
