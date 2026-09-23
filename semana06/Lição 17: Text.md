#Avaliação
//
```javascript
var background1 = createSprite(200,200);
background1.setAnimation("rainbow_1");
var background2 = createSprite(200,200);
background2.setAnimation("floating_grass_1");
var coin = createSprite(200,10);
coin.setAnimation("coin_gold_1");
setCoin();
var bunny = createSprite(200,350);
bunny.setAnimation("bunny1_ready_1");

var score = 0;

function draw() {
  trocarprimeirobackgr();
  
  background("white");
  
  if(keyDown("left")){
    bunny.x = bunny.x - 2;
  }
  
  if(keyDown("right")){
    bunny.x = bunny.x + 2;
  }
  
  if(coin.y > 400){
    setCoin();
  }
  if (bunny.isTouching(coin)) {
    score = score + 1;
  }
  if (bunny.isTouching(coin)) {
    setCoin();
  }
  if (coin.y > 400) {
    setCoin();
  }
  
  if (score > 9 ) {
    trocarsegundobackgr();
    
  }
  drawSprites();
  textSize(20);
  text("Score: " + score, 10, 10, 100, 100);
}

textSize(20);
  text("Score: " + score, 10, 10, 100, 100);
  drawSprites();
  
function setCoin(){
  coin.y = -50;
  coin.x = randomNumber (0,400);
coin.velocityY = randomNumber(3,10);
}
function trocarprimeirobackgr() {
  background1.visible = false;
  background2.visible = true;
}

function trocarsegundobackgr() {
  background1.visible = true;
  background2.visible = false;
}
```
Utilizando as funções eu mudei o cenário do game quando o player completasse 10 pontos. 

#Desafio
//
1ª parte
```javascript
var sun = 50;
 var grass = 400;
var moonmov = 0;
var moonstop = 0;
 function draw() {
  if(World.mouseY > 200){
     scene2();
  } else {
    scene1();
  }
}
function scene1() {
  background('lightblue');
  noStroke();
  fill("yellow");
  ellipse(sun,100, 150, 150);
  sun = sun + 10;
  if (sun > 400) {
    sun = -50;
  }
   noStroke();
    fill('green');
    ellipse(200, grass, 450,200);
}
function scene2() {
  var estrela = randomNumber(0,400);
 var estrela2 = randomNumber(0,400);

 background('black');
  noStroke();
  fill("gray");
  ellipse(moonmov,300, 150, 150);
   moonmov = moonmov + 4;
   noStroke();
   fill('green');
   ellipse(moonmov,300, 70, 70);
   moonmov = moonmov + 4;
  if (moonmov > 450) {
    moonmov = -50;
  }
  noStroke();
  fill('white');
  ellipse(estrela, estrela2, randomNumber(3,10), randomNumber(3,10));
  estrela = randomNumber(0,400);
  estrela2 = randomNumber(0,400);
   noStroke();
    fill('gray');
    ellipse(200, moonstop, 250,250);
}
```
Na primeira parte usei duas funções para animar dois cenários diferentes.
2ª
//
```javascript
var sun = 50;

function draw() {
  cena();
  sol();
  nuvem();
}

function cena() {
  background("lightblue");

  fill("green");
  ellipse(200, 400, 500, 180);

  fill("gray");
  triangle(50, 350, 200, 150, 350, 350);
}

function sol() {
  fill("yellow");
  ellipse(sun, 100, 70, 70);

  sun = sun + 2;

  if (sun > 450) {
    sun = -50;
  }
}

function nuvem() {
  fill("white");

  ellipse(100, 100, 50, 40);
  ellipse(130, 90, 70, 50);
  ellipse(160, 100, 50, 40);
}
```
Na segunda parte do desafio utilizei mais funções para montar outra cena.
