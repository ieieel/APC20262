#Avaliação
//var backdrop = createSprite(200,200);
backdrop.setAnimation("sky");
var creature = createSprite(200,250);
creature.setAnimation("creature");
creature.scale = 0.2;
function draw() {
  drawSprites();
  if (mouseDown()) {
    creature.rotation = randomNumber(-5,5);
  } else {
  fill("black");
  textSize(40);
  text("Press the mouse to shake the creature.", 20, 50, 360, 100);  
  }
}

Usando se/senão no desafio da lição 12 eu alterei o código para que o sprite se movesse quando o mouse estivesse pressionado e a instrução aparecesse na tela quando não estivesse pressionado.

#Desafio
//var foguete = createSprite(200, 300, 50, 80);
foguete.setAnimation("rocketo");
foguete.scale = 0.2;
var planeta = createSprite(100, 100, 80, 80);
planeta.setAnimation("planet");
planeta.scale = 0.5;
var estrela1 = createSprite(300, 100, 40, 40);
estrela1.setAnimation("estrelagir");
estrela1.scale = 0.3;
var presente = createSprite(200, 180, 60, 60);
presente.setAnimation("gift");

presente.visible = false;

var cliques = 0;
var lancado = false;

function draw() {

  // Fundo
  background("midnightblue");

  // Estrelas no fundo
  fill("white");
  ellipse(50, 70, 5, 5);
  ellipse(350, 60, 5, 5);
  ellipse(70, 180, 4, 4);
  ellipse(330, 250, 5, 5);
  ellipse(120, 350, 5, 5);
  ellipse(280, 330, 4, 4);

 
  planeta.rotation = planeta.rotation + 1;
  estrela1.rotation = estrela1.rotation + 2;

  if (lancado == false) {

    if (mouseWentDown("leftButton")) {
      cliques = cliques + 1;

      foguete.y = foguete.y - 5;
      foguete.rotation = randomNumber(-5, 5);
    }

    if (cliques >= 30) {
      lancado = true;

      foguete.visible = false;

      presente.visible = true;


      presente.x = 200;
      presente.y = 200;
      presente.rotation = 0;
    }
  }
  if (lancado == true) {
    presente.rotation = randomNumber(-3, 3);
  }

  drawSprites();

  fill("white");
  textSize(26);
  text("Feliz Aniversário!", 85, 40);
  if (lancado == false) {

    fill("white");
    textSize(18);
    text("Clique para lançar", 125, 390);
    text("o foguete!", 155, 415);

  }
  if (lancado == true) {

    fill("yellow");
    textSize(28);
    text("SURPRESA!", 125, 350);

    fill("white");
    textSize(18);
    text("Seu presente chegou!", 105, 380);
  }
}

No desafio que teve 5 partes, na ultima desenvolvi um cartão animado de aniversário usando condicionais, true/false e mouse input. 
