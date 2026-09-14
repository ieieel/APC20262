#Avaliação
// var orangeFish = createSprite(400, randomNumber(0, 100));
orangeFish.setAnimation("orange_fish");
var blueFish = createSprite(250, randomNumber(0, 200));
blueFish.setAnimation("blue_fish");
var greenFish = createSprite(300, randomNumber(200, 300));
greenFish.setAnimation("green_fish");

function draw() {
  // Draw Background
  background("navy");
  
  // Update Values
  orangeFish.x = orangeFish.x - 2;
  blueFish.x = blueFish.x - 4;
  greenFish.x = greenFish.x -0.5;
  
  // Draw Animations
  drawSprites();
}

A avaliação da lição 9 solicitava para que usando o counter pattern animássemos os peixes, o azul mais rápido e o verde mais lento.

#Desafio
  //1º 
  var orangeFish = createSprite(400, randomNumber(0, 100));
orangeFish.setAnimation("orange_fish");
var blueFish = createSprite(250, randomNumber(0, 200));
blueFish.setAnimation("blue_fish");
var greenFish = createSprite(300, randomNumber(200, 300));
greenFish.setAnimation("green_fish");

function draw() {
  // Draw Background
  background("navy");
  
  // Update Values
  orangeFish.x = orangeFish.x - 2;
  orangeFish.rotation = randomNumber(-2,2);
  blueFish.x = blueFish.x - 4;
  blueFish.rotation = randomNumber(-2,2);
  greenFish.x = greenFish.x -0.5;
  greenFish.rotation = randomNumber(-2,2);
  
  // Draw Animations
  drawSprites();
}

2º
var orangeFish = createSprite(400, randomNumber(0, 100));
orangeFish.setAnimation("orange_fish");
var blueFish = createSprite(250, randomNumber(0, 200));
blueFish.setAnimation("blue_fish");
var greenFish = createSprite(300, randomNumber(200, 300));
greenFish.setAnimation("green_fish");
var bubble1 = 400; 
var bubble2 = 400; 
var bubble3 = 400; 
var bubble4 = 400; 
var bubble5 = 400; 
var bubble6 = 400; 
var bubble7 = 400;

function draw() {
  // Draw Background
  background("navy");
  
  // Update Values
  orangeFish.x = orangeFish.x - 2;
  orangeFish.rotation = randomNumber(-2,2);
  blueFish.x = blueFish.x - 4;
  blueFish.rotation = randomNumber(-2,2);
  greenFish.x = greenFish.x -0.5;
  greenFish.rotation = randomNumber(-2,2);
  
  //Draw Bubbles
  noFill();
  stroke('lightblue');
  strokeWeight(4);
  ellipse(70, bubble1,25,25);
  ellipse(130,bubble2,25,25);
  ellipse(180,bubble3, 25,25);
  ellipse(225,bubble4,25,25);  
  ellipse(290,bubble5,25,25);
  ellipse(330,bubble6,25,25);
  ellipse(370,bubble7,25,25);
  bubble1 = bubble1 - 1.5;
  bubble2 = bubble2 - 0.5;
  bubble3 = bubble3 - 2;
  bubble4 = bubble4 - 1.8;
  bubble5 = bubble5 - 1;
  bubble6 = bubble6 - 3;
  bubble7 = bubble7 - 0.8;
  
  // Draw Animations
  drawSprites();
} 

3º
var voar = 450;
var sprite1 = createSprite(50, voar);
var sprite2 = createSprite(100, voar);
var sprite3 = createSprite(150, voar);
var sprite4 = createSprite(200, voar);
var sprite5 = createSprite(250, voar);
var sprite6 = createSprite(300, voar);
var sprite7 = createSprite(350, voar);

var nuvem1 = 70;
var nuvem2 = 100;
var nuvem3 = 130;
var nuvem4 = 250;
var nuvem5 = 280;
var nuvem6 = 310;
background('lightblue');

function draw() {
background('lightblue');
noStroke();
fill('white');
ellipse(nuvem1, 150, 80, 80); 
ellipse(nuvem2, 150, 80, 80);
ellipse(nuvem3,150, 80, 80);
nuvem1 = nuvem1-1;
nuvem2 = nuvem2-1;
nuvem3 = nuvem3-1;

ellipse(nuvem4,300, 80, 80);
ellipse(nuvem5,300, 80, 80);
ellipse(nuvem6,300, 80, 80);
nuvem4 = nuvem4+0.5;
nuvem5 = nuvem5+0.5;
nuvem6 = nuvem6+0.5;

sprite1.setAnimation('Bee');
sprite1.scale = 0.2;
sprite1.rotation = 270;
sprite1.x = randomNumber(48,51);
sprite1.y = sprite1.y - 2;
sprite2.setAnimation('Bee');
sprite2.scale = 0.2;
sprite2.rotation = 270;
sprite2.x = randomNumber(98,101);
sprite2.y = sprite2.y - 4;
sprite3.setAnimation('Bee');
sprite3.scale = 0.2;
sprite3.rotation = 270;
sprite3.x = randomNumber(148,151);
sprite3.y = sprite3.y - 6;
sprite4.setAnimation('Bee');
sprite4.scale = 0.2;
sprite4.rotation = 270;
sprite4.x = randomNumber(198,201);
sprite4.y = sprite4.y - 8;
sprite5.setAnimation('Bee');
sprite5.scale = 0.2;
sprite5.rotation = 270;
sprite5.y = sprite5.y - 6;
sprite5.x = randomNumber(248,251);
sprite6.setAnimation('Bee');
sprite6.scale = 0.2;
sprite6.rotation = 270;
sprite6.y= sprite6.y - 4;
sprite6.x = randomNumber(298,301);
sprite7.setAnimation('Bee');
sprite7.scale = 0.2;
sprite7.rotation = 270;
sprite7.x = randomNumber(348,351);
sprite7.y = sprite7.y - 2;
drawSprites();  
}

O desafio de 3 partes solicitava na primeira parte que fizéssemos os peixes tremerem enquanto se movimentavam, a segunda parte para adicionarmos bolhas a cena e para fazermos essas bolhas se movimentarem, e a 3º parte para utilizarmos todo o conjunto
criando uma cena utilizando as animações aprendidas anteriormente. 
