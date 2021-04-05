# Programming-Logic
Programming logic exercises with JavaScript and HTML.


# Conceitos e Funcionalidades

•	HTML -> Hyper Text Markup Language.

•	TAGS -> instruções para o navegador, como <h1>, <a>. Pode ou não ser fechada. Exemplo do que não é TAG: <meta>.
o	De conteúdo: possuem abertura e fechamento. Ex: h, p, etc.
o	De informação: não possuem fechamento, pois estão apenas passando uma informação. Ex: DOCTYPE, meta charset, etc.

•	Atributo - Exemplo -> href.

•	meta sharset=”UTF-8”: comando inicial necessário para evitar problemas de acentuação. UTF-8 é um dos dicionários existentes que é utilizado pela maioria dos idiomas.

•	var: variável. Para que ela seja aplicável em todas as funções, é necessário que conste fora destas.

•	Math.round: serve para arredondar o valor para cima.

•	Math.floor: serve para arredondar o valor para baixo.

•	Math.random = calcula um número aleatório.

•	Math.PI: calcula o PI.

•	Funções: devem sempre ser declaradas inicialmente (e variáveis também). Quando uma função é chamada com o (), significa que ela deve ser executada. Quando ela é chamada sem o (), significa que ela está sendo atribuída como parâmetro a outro comando.

•	Funções anônimas: quando os nomes das funções forem excluídos, elas serão anônimas. Funções anônimas não funcionam "soltas", mas podem ser atribuídas a uma variável ou propriedade/comando.

o	Função pulalinha: serve para pular linha.
•	function pulaLinha() { 
•	        document.write("<br><br>");
•	    }

o	Função mostra: foi criada para substituir o que é escrito em document.write. A inserção da palavra "frase" quer dizer que frase = qualquer coisa escrita dentro dos parenteses em mostra(), sendo que esse conteúdo atua como uma variável. Por conta disso, o comando document.write dentro da função mostra deve também conter a palavra "frase", pois ela está recebendo a variável. Ademais, pode ter função dentro de função, como foi feito aqui ao se adicionar a função pulaLinha.
•	function mostra(frase) {
•	    document.write(frase);
•	    pulaLinha();
•	}

o	Função sorteia é para sortear um número aleatório.
•	function sorteia() {
•	        return Math.round(Math.random() * 10);
•	    }

o	Função sorteiaNumeros é para devolver uma lista de segredos (no caso, números). O parâmetro dentro dela indica quantos segredos ela recebe (os quais não se repetem).
•	    function sorteiaNumeros(quantidade) {
•	
•	        var segredosX = []; // Variáveis declaradas dentro de uma função só existem naquela função.
•	        var numero = 1; // Trata-se de um contador, onde começa.
•	        
•	        while (numero <= quantidade) {
•	            var numeroAleatorio = sorteia(); // numeroAleatorio é o número escolhido.
•	            var achou = false;
•	
•	            if(numeroAleatorio !== 0) { // Esse if é apenas para tirar a possibilidade de o número lançado aleatóriamente ser 0.
•	            
•	                for(var posicao = 0; posicao < segredosX.length; posicao++) { // O for faz a busca na lista (array), que é representado pela aqui função sorteia() e verifica se o número escolhido através da variável numeroAleatorio se encontra dentro dessa lista. Em caso positivo, achou vai ser igual a true, e o looping será interrompido.
•	                    if(segredosX[posicao] == numeroAleatorio) {
•	                    achou = true;
•	                    break;
•	                    }
•	                }
•	                    if(achou == false) {
•	                    segredosX.push(numeroAleatorio); // Coloca um novo segredo dentro da lista (o array). Considerando a condicional acima, ele só vai colocar o elemento aqui, se não achar o número escolhido.
•	                    numero++; // o numero++ é para dar o looping, caso o número escolhido não seja o gerado pelo sistema e seja necessário tentar novamente.
•	                    }
•	            }
•	        }         
•	            return segredosX;
•	        }

o	Função isNAN(): determina se o valor é NaN ou não.
•	while( isNaN(idade) ) {
•	    idade = parseInt(prompt("Digite sua idade"));    
•	}

•	return: indica o que sairá da função. Ainda assim, sem a declaração mostra ele não será imprintado na tela, por isso essa declaração é importante. Antes, as funções apareciam porque a declaração mostra estava dentro da função. Sem ela dentro, é necessário que haja o return.

•	prompt: é uma função que pode ser alterada também no console do navegador (atalho: F12). Ela permite ao usuário incluir um valor. O comando prompt sempre lê o que é inserido como texto.
•	var nome = prompt("Informe seu nome.");

•	parseInt: identifica um número classificado como texto e o transforma em número (inteiro).

•	parseFloat: identifica um número classificado como texto e o transforma em número (incluindo não inteiro).

•	=: serve para atribuir algo.

•	==: igual.

•	let: igual a var.

•	&&: e.

•	||: ou.

•	!=: diferente.

•	!: “not”, reverso, negativa.

•	console.log: mostra na aba console do navegador (atalho F12) qual número randômico o PC gerou antes de você chutar um valor. Ele mostra a variável/função atuando no navegador.

•	break: para a função, quebra o looping.

•	//: serve para escrever comentários e observações que não fazem parte do código dentro do JS.

•	for: recebe a variável, bem como a condição do while e a condição que faz o "looping griar".

•	++: serve para "adicionar mais um", sem precisar escrever "+ 1". É o que se chama de "pós incremento".

•	document.querySelector(): serve para trazer o comando do mundo HTML para o JS.

•	input.value: chama a tag input (que está no HTML) a mostrar seu valor.

•	input.value = "";: serve para limpar a caixa de texto que aparece no navegador após você colocar um valor e apertar o botão.

•	.onclick = serve para identificar que se clicou no canvas.

o	button.onclick = verifica: serve para após você colocar um valor na caixa de texto do navegador e apertar o botão, a caixa de texto voltar a ser selecionada (e piscar), não sendo necessário clicar nela novamente para digitar um novo texto/número. Ele consta no começo e depois na função pois quisemos que isso acontecesse tanto ao recarregar a página quanto ao apertar o botão.

•	.push: "empurra" algo para dentro do array (só serve para array).

•	Posição: no mundo JS, o primeiro número é sempre 0, não 1.

•	Array: se configura pelo uso de [], e geralmente o nome da variável é no plural, por comportar vários itens (que podem ser texto, número, boleano, etc.). Os valores do arrey são trazidos de acordo com sua posição dentro do [].

•	.length: retorna a quantidade de elementos que o array tem.

•	.focus(): o comando que vier na frente será o foco da parte do código que se está fazendo (exemplo: input.focus()). Ou seja, ao reiniciar o navegador, o foco do clique estará nesse elemento.

•	<canvas width="600" height="400"></canvas>: comando para desenhar algo na tela (fica fora do JS). O width e heigh podem variar de acordo com o comando que for mais eficiente.

•	Canvas: delimitação de onde se desenhará. Código padrão:
•	    var tela = document.querySelector('canvas');
•	    var pincel = tela.getContext('2d');
•	    pincel.fillStyle = 'grey';
•	    pincel.fillRect(0, 0, 600, 400);

•	tela.getContext('2d'): comando importante para 

•	No mundo JS pode-se usar '' ou "".

•	fillRect() = preenche um retângulo. Dentro são inseridas as coordenadas, considerando os eixos x (horizontal) e y (vertical).

•	fillStyle = preenche a cor. Ela não é uma função, e sim como uma variável, de forma que recebe valor.

•	Cor: a cor tem de vir antes do que as demais instruções. As cores e formas podem ser localizadas em bibliotecas de JS. Basta por exemplo jogar as palavras "canvas 2d api" no google que ele localiza uma delas, ou em "https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D". Jogar no google a expressão “cores rgb” também serve, aparece a tabela de cores HTML, que contém os códigos das cores.

•	get.Context: informa o que será inserido na tela (2D, 3D, 4D, etc).

•	/* */: retira o código entre eles da tela.

•	.beginpath(): função inicia a escrita do caminho que o desenho da forma irá percorrer.

•	.moveTo: é uma função para indicar a coordenada de onde o pincel vai iniciar.

•	.lineTo: é uma função para mover o pincel.

•	.fill(): é uma função para preencher a forma com a cor.

•	.arc: é a função que desenha o círculo. Os primeiros dois parâmetros do método arc são as coordenadas X e Y do centro do circulo. O terceiro parâmetro é o valor do raio. O quarto e quinto parâmetros definem o ângulo inicial e final do círculo.

•	API = Application Programming Interface = Interface de Programação de Aplicativos.

•	Tamanho: o programador que decide o tamanho.

•	.font: determina a fonte da letra.

•	.fillText: determina o texto a ser inserido e a sua localização no canvas.

•	.fillStroke: coloca bordas. Se a cor do stroke não for definida, ela será sempre preta. É possível definir a cor com o .strokeStyle, porém o .fillStroke também serve.

•	stroke.Stylle: determina a cor da borda.

•	stroke.Rect: determina a borda um retângulo. Dentro são inseridas as coordenadas, considerando os eixos x (horizontal) e y (vertical).

•	.pageX: mostra as coordenadas x quando se clica com o mouse no canvas.

•	.pageY: mostra as coordenadas y quando se clica com o mouse no canvas.

•	.offserLeft: serve para tirar a margem branca que fica a esquerda na tela.

•	.offsetTop: serve para tirar a margem branca que fica em cima na tela.

•	.shiftKey: pergunta se a tecla SHIFT está apertada.

•	.altKey: pergunta se a tecla ALT está apertada.

•	.oncontextmenu: serve para considerar o clique do botão direito do mouse.

•	tela.onmousemove: serve para capturar o movimento do mouse.

•	tela.onmousedown: compreende quando o botão esquerdo do mouse é apertado.

•	tela.onmouseup: compreende quando o botão esquerdo do mouse é desapertado.

•	.value: chama uma variável a mostrar seu valor.

•	Booleana: só aceita 0 ou 1, true ou false, etc. Como uma booleana só aceita duas suposições, a forma de invertê-la é colocando o equivalente a "not", que é o símbolo “!”.

•	document.onkeydown: serve para identificar qual tecla está sendo pressionada, sendo a única capaz de identificar as setas do teclado.

•	.keyCode: acessa o código da tecla pressionada.

•	.clearRect serve para limpar o retângulo.

•	setInterval: função que serve para determinar a cada quanto tempo (em milisegundos) uma função é executada, por isso ela comporta o nome de outra função e o tempo.

•	+=, -=, *=, /=: serve para repetir o item anterior após o =. Ex: “xBolinha = xBolinha + velocidadeXBolinha” pode ser escrito como “xBolinha += velocidadeXBolinha”.
