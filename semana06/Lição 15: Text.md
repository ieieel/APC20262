#Avaliação
//
```javascript
var rock = createSprite(200, 350);
rock.setAnimation("rock");
rock.velocityY =  -10;
rock.rotationSpeed = 2;

function draw() {
  background("skyblue");
  rock.velocityY = rock.velocityY + 0.2;
  // update sprites
  
  drawSprites();
}
```
Utilizei o velocityY junto com o counterpattern para fazer a pedra voltar quando ela fosse lançada para cima.

#Desafio 
//
1ª Parte
```javascript
var plane = createSprite(50, 350);
plane.setAnimation("plane");
var rock = createSprite(150, 350);
rock.setAnimation("rock");
var rockdown = createSprite(350, 100);
rockdown.setAnimation("rock_down");

// You might want to change these 
plane.velocityY = -9;
plane.velocityX = 3;

function draw() {
  background("lightblue");
  plane.velocityY = plane.velocityY + 0.2;
  
  drawSprites();
}
```
Utilizando o velocity junto com o counterpattern novamente para fazer o avião descer depois de subir.

2ª Parte
```javascript
var car = createSprite(200, 350);
car.setAnimation("car");

car.velocityY = -15;
function draw() {
  background("forestgreen");
  fill("gray");
  rect(150, 0, 100, 400);
  
   car.velocityY = car.velocityY + 0.3;
   
 if (car.velocityY < 0) {
     car.velocityY = car.velocityY + 0;
 } else { 
   car.velocityY = 0;
   }  
   
  drawSprites();
}
```
Na segunda parte continuei usando o velocity com counterpatter, mas dessa vez com um if para parar o movimento do carro e a soma quando ele chegasse a 0.

3ª parte
```javascript
var back = createSprite(200,200);
var flor = createSprite(300,300);
var abelha = createSprite(100,250);
back.setAnimation("back");
flor.setAnimation("flor");
flor.scale = 0.4;
abelha.setAnimation("abelha");
abelha.scale = 0.2;
abelha.velocityX = 5;

function draw() {
  abelha.velocityX = abelha.velocityX - 0.07;
 if (abelha.x > 275) {
    abelha.rotation = randomNumber(-5,5);
  }
   if (abelha.x < -60) {
abelha.x = 0;
abelha.velocityX = 6.5;
 abelha.velocityX = abelha.velocityX - 0.15;
   }
   
  
  drawSprites();
}
```
Na ultima parte animei uma cena de uma abelha voando em uma flor utilizando o velocity com o counterpattern para que ela voltasse quando chegasse na flor e também um if para que ela não continuasse para fora da tela e repetisse a animação.
