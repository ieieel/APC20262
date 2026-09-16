#Avaliação
//
``` javascript
var grass = createSprite(200,200);
grass.setAnimation("floating_grass");
var alien = createSprite(180,100);
alien.setAnimation("alien");
alien.scale = 1.3;
var robot = createSprite(300,300);
robot.setAnimation("robot");
robot.scale = 0.2;
drawSprites();
textSize(15);
fill('yellow');
text("The butterflies are too colorfull.", 10, 275);
text("Where am I going?", 250, 100);
```
A avaliação da lição 7 pedia para adicionarmos textos ao cenário já pronto, o que eu fiz nas linhas 13 e 14 mudando algumas caraterísticas do texto como tamanho e cor da letra.

#Desafio
//
``` javascript
var sprite = createSprite(200,280);

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
drawSprites();
fill('white');
stroke('black');
strokeWeight(3);
ellipse(125,170,150,100);
shape(163,213,186,226,190,197);
strokeWeight(1);
fill('black');
textSize(15);
text("It's a good day!", 70, 150, 177, 152);
```
A ultima lição contava com 4 etapas sendo a 3 apenas mudando códigos já prontos e a última criando um cenário com sprite do 0. 
