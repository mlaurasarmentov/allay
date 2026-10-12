# Conceitos:
1.  Processo bytecode: é o processo em que o JAVAC pré-compila o programa, procurando por erros sintáticos e por erros léxicos;
	Interpretação Just in Time: é a parte em que o programa realmente é executado - o JVM pega o bytecode e converte blocos para linguagem de máquina.
2.  A palavra reservada *static* serve para fazer um bloco que não depende de um objeto específico e, comumente, define o escopo de classe.
3.  A diferença é que, enquanto o tipo primitivo funciona como qualquer outro tipo em linguagens de programação - compacta e define como algo será guardado na memória -, a classe - tipo referenciado - tem métodos e características próprias, definidas na criação da classe.
# Codando:
1. O erro é léxico - a escrita está errada, pois, para imprimir "número", não deveria haver um "@" ao lado do nome da variável.
2. O erro é sintático - falta um último parêntesis e um ponto-vírgula no método println;
3. O erro é semântico e sintático - sempre imprimirá "Ok" e há uma chaves fechando } a mais;
4. O erro é semântico - faz-se um inteiro valor com uma atribuição string e se tenta fazer um cálculo entre string e inteiro.