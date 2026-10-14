No exercício 1 da lista ao rodar o código eu percebi que cada parte era exibida conforme a necessidade do programa,
por exemplo, o programa começava em main e chama soma_mult, e soma_mult chama mult e o controle ia passando e depois 
retornando conforme os resultados eram retornados até voltar para main. 

No exercício 2 da lista ao rodar o código eu vi que cada tipo de variável possui ocupa um espaço diferente e que o tipo de variável
influencia diretamente no resultados que vão ser retornados em cáculos simples. Cáculos realizados com int vão retornar valores
inteiros mesmo que o resultado possua casas decimais, por exemplo.

No exercício 3 da lista eu já vi que é diferente uma variavél inicializada (int a = 42), de uma não incializada (int b, que depois
o valor de b = a + 8 é atribuido), e para que serve uma constante utilizando o código const que vai ser utilizado quando quisermos 
que uma variável não seja mudada depois da inicialização do programa por alguma atribuição. 

Ao rodar o código do execício 4, percebi que cada operador era executado conforme a necessidade do programa. Primeiro, 
o programa realizava as operações de divisão e o resto, depois incrementava o valor de x de formas diferentes, 
utilizando o pré-incremento e o pós-incremento. Em seguida, verificava uma condição para definir o valor de max e, por fim, 
modificava os bits da variável flags, ligando alguns e desligando outro conforme as operações eram executadas.

No exercício 5 eu vi que o programa seguia diferentes caminhos de execução conforme as condições estabelecidas. Na primeira 
parte, o if, o else if e o else verificavam as condições em sequência até encontrar uma verdadeira e executar o comando
correspondente. Na segunda parte, o laço for repetia as instruções enquanto a condição fosse satisfeita, utilizando o continue para 
pular algumas iterações e o break para interromper a repetição quando determinado valor fosse alcançado. Na terceira parte, 
o do-while executava as instruções antes de verificar a condição, fazendo com que o bloco fosse executado pelo menos uma vez. 
Por fim, o switch selecionava o bloco correspondente ao valor da variável, agrupando diferentes casos que compartilhavam a mesma
execução e utilizando o break para sair da estrutura.

No exercício 6 a função de fatorial chamava a si mesma com valores cada vez menores até atingir uma condição 
de parada. A partir desse ponto, os resultados começavam a retornar pelas chamadas, realizando as multiplicações necessárias até
chegar ao resultado final. Depois, na função dobra, percebi que o programa utilizava um ponteiro para receber o endereço da 
variável original, permitindo modificar seu valor diretamente na memória. Por fim, o ponteiro para função armazenava a referência
à função fatorial, possibilitando chamá-la por meio de outra variável. Assim, o exercício demonstrou como o controle pode passar
entre chamadas recursivas e como os ponteiros permitem acessar dados e funções de diferentes maneiras.

No exercício 7, depois de rodar o código vi que o programa armazenava vários valores em um array e utilizava um laço for para 
percorrer seus elementos, acessando cada posição por meio de seu índice e acumulando os valores na variável soma. Em seguida,
a função memcpy copiava os elementos do array original para outro array, permitindo modificar o primeiro elemento da cópia sem 
alterar o valor correspondente no array original. Depois, o programa acessava um elemento específico da matriz utilizando os 
índices da linha e da coluna. Por fim, percebi que os elementos da matriz eram armazenados sequencialmente na memória, linha por 
linha, permitindo percorrê-los com um ponteiro a partir do endereço do primeiro elemento.
