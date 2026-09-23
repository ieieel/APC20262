#Desafio
//
```javascript
var  player = createSprite(50,300); 
var  plataforma2 = createSprite(450, 300); 
var score = 0; 
var health = 100; 
var nuvem1 = 80; 
var nuvem2 = 210; 
var obstaculo = createSprite(450, 320); 
var premio = createSprite(450, 250); 
var jogoAtivo = true; 
 
player.setAnimation("Coelho parado"); 
player.scale = 0.5; 
plataforma2.setAnimation("chão2"); 
plataforma2.scale = 0.2; 
plataforma2.velocityX = -5; 
obstaculo.setAnimation("pedra"); 
obstaculo.scale = 0.5; 
obstaculo.velocityX = -6; 
obstaculo.setCollider("rectangle",0,0,50,50); 
premio.setAnimation("carrot"); 
premio.scale = 0.4; 
premio.velocityX = -5; 
 
function draw() { 
 
fundo(); 
nuvens(); 
sol(); 
 
pontuacao(); 
saude(); 
movimentarPlayer(); 
encostarpedra(); 
encostarplat(); 
pegarPremio();
ganharvida();
verificarGameOver(); 
telaGameOver(); 
      
  drawSprites(); 
} 
 
function movimentarPlayer() { 
 
  if (keyDown("right")) { 
    player.x = player.x + 10; 
    player.setAnimation("coelhodir"); 
  } 
 
  if (keyDown("left")) { 
    player.x = player.x - 10; 
    player.setAnimation("coelhoesq"); 
  } 
 
  if (keyWentDown("up") ) { 
    player.velocityY = -30; 
    player.setAnimation("pulando"); 
  } 
if (keyWentUp("up")) { 
  player.velocityY= 0; 
} 
 
  if (player.y < 300) { 
    player.y = player.y + 10; 
  } 
 
  if (player.y >= 300) { 
    player.y = 300; 
 
    if (!keyDown("right") && !keyDown("left")) { 
      player.setAnimation("Coelho parado"); 
    } 
  } 
} 

function fundo() { 
  background('lightblue'); 
  noStroke(); 
  fill("green"); 
  shape(0,350,400,350,400,400,0,400); 
} 

function nuvens() { 
  noStroke(); 
  fill("white"); 
 
  ellipse(nuvem1, 100, 70, 40); 
  ellipse(nuvem1 + 30, 90, 80, 50); 
  ellipse(nuvem1 + 65, 105, 70, 40); 
  rect(nuvem1, 100, 65, 30); 
   
  ellipse(nuvem2, 150, 60, 35); 
  ellipse(nuvem2 + 30, 140, 75, 45); 
  ellipse(nuvem2 + 65, 150, 65, 35); 
  rect(nuvem2, 150, 65, 30); 
 
  nuvem1 = nuvem1 - 2; 
  nuvem2 = nuvem2 - 2; 
 
  if (nuvem1 < -100) { 
    nuvem1 = 450; 
  } 
  if (nuvem2 < -100) { 
    nuvem2 = 500; 
  } 
} 

function sol() { 
  noStroke(); 
  fill("yellow"); 
  ellipse(330,80,100,100); 
 
} 

function pontuacao() { 
  fill('black'); 
  strokeWeight(5); 
  textSize(30); 
  text("Score =", 20, 50); 
  text(score, 130, 50); 
} 

function saude() { 
   fill('black'); 
  strokeWeight(5); 
  textSize(30); 
  text("Vida =", 250, 50); 
  text(health, 340, 50); 
} 

function encostarpedra() { 
  if (player.isTouching(obstaculo)) { 
    score = score - 1; 
    health = health - 10; 
    obstaculo.x = 450; 
    obstaculo.velocityX = randomNumber(-8, -2); 
  }

  if (obstaculo.x < -50) {
    obstaculo.x = 450;
    obstaculo.velocityX = randomNumber(-8, -2);
  }
}
 
function encostarplat() { 
  if (player.isTouching(plataforma2)) { 
    plataforma2.displace(player); 
  }

  if (plataforma2.x < -50) {
    plataforma2.x = 450;
    plataforma2.velocityX = -5;
  }
}

function pegarPremio() {
   if (player.isTouching(premio)) {
    score = score + 5;
    premio.x = 450;
    premio.y = randomNumber(200,280);
    premio.velocityX = randomNumber(-7,-4);
  }

  if (premio.x < -50) {
    premio.x = 450;
    premio.y = randomNumber(200,280);
    premio.velocityX = randomNumber(-7,-4);
  }
}
 
function verificarGameOver() { 
 
  if (health <= 0) { 
 
    health = 0;
    jogoAtivo = false;
 
    player.velocityY = 0; 
    plataforma2.velocityX = 0; 
    obstaculo.velocityX = 0; 
    premio.velocityX = 0; 
  } 
} 

function telaGameOver() { 

  if (jogoAtivo == false) {
    fill("black"); 
    textSize(45); 
    text("GAME OVER", 90, 180); 
 
    textSize(25); 
    text("Score final: " + score, 120, 230); 
  }
}
```
Na lição 18, sem duvida a que mais me tomou tempo e me deu dor de cabeça, eu desenvolvi um jogo do 0 utilizando todos os conceitos que eu consegui me lembrar do que eu aprendi nas outras lições.
