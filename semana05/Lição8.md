#Avaliação lição 8 
// //1) Add the draw loop block to the bottom of this program.
//2) Move any blocks that need to be inside the draw loop.


World.frameRate = 6;
var salt = createSprite(200,200);
salt.setAnimation("salt");
salt.rotation = 180;
function draw() {
  background("skyblue");
  salt.y = randomNumber(190,200);
  drawSprites();
}

A avaliação da lição 8 pedia para adicionarmos o draw loop e mudar o sprite como estava na animação, no caso usando a rotação e mudandoo frame rate para se igualar.

#Desafio
//1º 
var sprite = createSprite(200,280);


function draw() {
  background('lightblue');
fill('black');
shape(0,350,0,400,400,400,400,350);
fill('grey');
shape(0,328,0,350,400,350,400,327);
fill('white');
rect(50,370, 20, 10);
rect(100,370, 20, 10);
rect(150,370, 20, 10);
rect(200,370, 20, 10);
rect(250,370, 20, 10);
rect(300,370, 20, 10);
rect(350,370, 20, 10);
fill('blue');
shape(251,327,250,50,350,50,350,326);
fill('white');
rect(260,60,20,20);
rect(260,90,20,20);
rect(260,120,20,20);
rect(260,150,20,20);
rect(260,180,20,20);
rect(260,210,20,20);
rect(260,240,20,20);
rect(260,270,20,20);
rect(260,300,20,20);
rect(290,60,20,20);
rect(290,90,20,20);
rect(290,120,20,20);
rect(290,150,20,20);
rect(290,180,20,20);
rect(290,210,20,20);
rect(290,240,20,20);
rect(290,270,20,20);
rect(290,300,20,20);
rect(320,60,20,20);
rect(320,90,20,20);
rect(320,120,20,20);
rect(320,150,20,20);
rect(320,180,20,20);
rect(320,210,20,20);
rect(320,240,20,20);
rect(320,270,20,20);
rect(320,300,20,20);
fill('brown');
shape(100,327,100,250,110,250,110,328);
fill('green');
ellipse(104,232,80,80);
fill('yellow');
ellipse(0,0,100,100);
noStroke();
fill('white');
ellipse(75,75,50,50);
ellipse(100,75,50,50);
ellipse(130,75,50,50);
sprite.setAnimation("Pessoa");
sprite.scale = 0.3;
fill('white');
stroke('black');
strokeWeight(3);
ellipse(125,170,150,100);
shape(163,213,186,226,190,197);
strokeWeight(1);
fill('black');
textSize(15);
text("It's a good day!", 70, 150, 177, 152);
  sprite.rotation = randomNumber(0,5);
  drawSprites();
}


2º 
var sprite = createSprite(100,350);

World.frameRate = 5;
function draw() {
   background('lightblue');
fill('black');
shape(0,350,0,400,400,400,400,350);
fill('grey');
shape(0,328,0,350,400,350,400,327);
fill('white');
rect(50,370, 20, 10);
rect(100,370, 20, 10);
rect(150,370, 20, 10);
rect(200,370, 20, 10);
rect(250,370, 20, 10);
rect(300,370, 20, 10);
rect(350,370, 20, 10);
  sprite.setAnimation("Moto");
  sprite.scale = 0.5;
  sprite.x = randomNumber(0,400);
  drawSprites();
}

No desafio havia duas partes onde a primeira era para animar o sprite da cena da lição 7 utilizando o draw loop, e a segunda foi um free play.
