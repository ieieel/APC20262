#Avaliação
```javascript
// create sprites
var giraffe = createSprite(50, 50);
giraffe.setAnimation("giraffe");
giraffe.velocityX = 3;
var hippo = createSprite(50, 150);
hippo.setAnimation("hippo");
hippo.velocityX = 3;
var rabbit = createSprite(50, 250);
rabbit.setAnimation("rabbit");
rabbit.velocityX = 3;
var snake = createSprite(50, 350);
snake.setAnimation("snake");
snake.velocityX = 3;
var parrot = createSprite(350, 50);
parrot.setAnimation("parrot");
parrot.velocityX = -3;
var elephant = createSprite(350, 150);
elephant.setAnimation("elephant");
elephant.velocityX = -3;
var monkey = createSprite(350, 250);
monkey.setAnimation("monkey");
monkey.velocityX = -3;
var pig = createSprite(350, 350);
pig.setAnimation("pig");
pig.velocityX = -3;


function draw() {
  background("lightblue");
  drawSprites();
  giraffe.bounce(parrot);
  hippo.displace(elephant);
  rabbit.collide(monkey);
  snake.bounceOff(pig);
}
```
Na avaliação da lição 16 eu utilizei os 4 tipos de locomoção aprendidos nas partes anteriores da lição.

#Desafio
//
```javascript
var player = createSprite(200, 100);
player.setAnimation("fly_bot");
player.scale = 0.8;
var obstacle = createSprite (-50,randomNumber(0,400));
obstacle.setAnimation("pedra");
obstacle.scale = 0.8;
obstacle.velocityX = 5;
var obstacle2 = createSprite(randomNumber(0,400),-50);
obstacle2.setAnimation("pedra2");
obstacle2.scale = 0.8;
obstacle2.velocityY = 5;
var moeda = createSprite(50,100);
moeda.setAnimation("coin");
moeda.scale = 0.4;
var score = 0; 

 
  
function draw() {
  background("lightblue");
 
  fill('black');
  strokeWeight(5);
  textSize(30);
  text("Score =", 50, 50);
  
  text(score, 170, 50);
  
    if (player.isTouching(moeda)) {
    score = score + 1; 
  }
  
  if (obstacle.x > 400) {
    obstacle.x = -50;
  obstacle.y = randomNumber (0,400);
  }
  if (obstacle2.y > 400) {
    obstacle2.y = -50;
    obstacle2.x = randomNumber (0,400);
  }
  player.velocityY = player.velocityY + 0.15;
  if (keyWentDown("up")) {
    player.velocityY = - 5;
  }
  
  if (keyWentDown("left")) {
    player.velocityX = - 5;
  }
  
  if (keyWentDown("right")) {
    player.velocityX = 5;
  }
  
  if (player.isTouching(moeda)) {
    moeda.x = randomNumber(0,400);
    moeda.y = randomNumber(0,400);
  }
  
  if (player.isTouching(obstacle)) {
    obstacle.displace(player);
  }
  if (player.isTouching(obstacle2)) {
    obstacle.displace(player);
  }
  
  drawSprites();
  
  if (player.x < -50 || player.x > 450 || player.y < -50 || player.y > 450) {
    background("black");
    textSize(50);
    fill("green");
    text("Game Over!", 50, 200);
    
    
  
    
}
}
```
Na parte final do desafio eu desenvolvi um minigame utilizando os conceitos de mobilidade aprendidos nas lições anteriores e na própria lição 16.
