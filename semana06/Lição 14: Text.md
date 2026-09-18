#Avaliação
//
```javascrip
// create the sprites
var horse = createSprite(200, 150);
horse.setAnimation("horse");
var rainbow = createSprite(400, 370);
rainbow.setAnimation("rainbow");
rainbow.velocityX = -5;
rainbow.velocityY = -5;
rainbow.rotateToDirection = true;

function draw() {
  // draw the background
  background("skyblue");

  // change the horse to a unicorn when the rainbow touches it
  if (rainbow.isTouching(horse)) {
    horse.setAnimation("unicorn");
  }
  
  drawSprites();
}
```
Na avaliação eu utilizei o comando "is touching" para quando o arco-íris encostasse no cavalo ele se transformasse em um unicórnio.

#Desafio 
//
1ª
```javascript
var roller = createSprite(200, 200);
roller.scale = 2;
roller.setAnimation("roller_1");
// Use .setCollider() with all 6 parameters.
roller.setCollider("rectangle", 0, 0, 30, 180,30);
roller.debug = true;
drawSprites();
```
Na primeira parte do desafio usando o comando setCollider eu mudei o formato do collider para o da figura.

2ª
```javascript
var points = 0;
var coin = createSprite(200, 100);
coin.setAnimation("coin");
var ghost = createSprite(200, 300);
ghost.setAnimation("ghost");

function draw() {
  if (ghost.isTouching(coin)) {
    points = points + 1;
    coin.x= randomNumber(0,400);
    coin.y= randomNumber(0,400);
  }
  background("lightblue");
  text("Points: " + points, 25, 25);
  if(keyDown("up")) {
    ghost.y = ghost.y - 5;
  }
  if(keyDown("down")) {
    ghost.y = ghost.y + 5;
  }
  if(keyDown("left")) {
    ghost.x = ghost.x - 5;
  }
  if(keyDown("right")) {
    ghost.x = ghost.x + 5;
  }
  drawSprites();
}
```
Na segunda parte do desafio eu usei novamente o "is touching" para fazer o programa conferir se o fantasma encostava na moeda e marcar a pontuação do jogo.

3ª
```javascript
var back = createSprite(200,200);
var sapo = createSprite(100,320);
var cogu = createSprite(450,320);
var mosca = createSprite(450,100);
back.setAnimation("background");
sapo.setAnimation("frog");
cogu.setAnimation("mushroom");
cogu.scale = 1.2;
mosca.setAnimation("fly");
mosca.velocityX = randomNumber(-10,-15);
cogu.velocityX = randomNumber(-7,-10);
drawSprites();




var score = 0;
var health = 100;

function draw() {

 if (sapo.isTouching(cogu)) {
   health = health - 10;
    
  }
   
if (sapo.isTouching(cogu)) {
  cogu.x = 450;
}
if (cogu.x < 0) {
  cogu.x = 450;
}


  if (mosca.x < 0) {
  mosca.x = 450;  
  }
  
  if (sapo.isTouching(mosca)) {
     score = score + 1;
   }

if (sapo.isTouching(mosca)) {
     mosca.x = 450;
   }
  if (keyWentDown("up")) {
    sapo.velocityY = -10;
    
    
  }
  if (keyWentUp("up")) {
    sapo.velocityY = +10;
  }
  
  if (sapo.y > 320) {
    sapo.y = 320;
  }


 if (sapo.y < 100) {
     sapo.velocityY = +10;
  }
   
  drawSprites();
  
  fill("black");
  textSize(20);
  text("Health:", 280, 30);
  text (health, 350, 30);
 
 fill("black");
  textSize(20);
  text("Score:", 30, 30);
  text (score, 90, 30);
  
  
  if (health < 0) {
    background("black");
    fill("green");
    textSize(50);
    text("Game Over!" , 40, 200);
  }
}
```
Na 3ª parte desenvolvi um jogo onde o sapo precisa pegar a mosca para marcar pontos e caso ele encoste no cogumelo ele ira perder pontos de vida. Utilizei variáveis para as animações, para a pontuação e a vida, comandos para conferir colisões, e outras coisas que eu aprendi anteriormente.
