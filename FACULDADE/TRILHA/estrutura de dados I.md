estrutura de dados: a forma de guardar e de acessar informações na memória;

para arrays:
- podemos ter uma variável que define o tamanho arbitrário do array, diferente do tamanho real (aquele alocado na memória);
- o tamanho arbitrário é tudo que estamos usando do array, isso é, tudo que tem informação válida para nós;
- guardados de forma contínua;

listas em python:
- guardam ponteiros em si;
- não são guardados de forma contínua - aumentar espaço é mais barato;
- inserção: .insert(índice, valor);

string em python:
- funciona como um array de letras, cada uma em seu próprio espaço;
- tratadas como arrays: são imutáveis;

sintaxe:
- .append = adiciona-se ao último espaço;
			= é sempre no final, então, gasta menos, pois não precisamos empurrar nenhum elemento;
			= O(1) - ou seja, só gasta uma operação para resolver o problema;
- .insert = empurra tudo que tá na frente, a fim de colocar um novo elemento no início;
			= O(n) - ou seja, gasta o número de operações da lista;
- slicing = P[início; fim; passo]
	- para inverter a string, usa-se passo -1;
- pop = tira o último 

EXERCÍCIO (Leet Code - Reverse words in a string III):
1. usar um ponteiro para procurar espaços;
2. ao achar espaço, criar uma nova string até tal índice;
3. dar print em todas as strings criadas em ordem, com passo -1.

matrizes:
- representam imagens;
- em python: listas de listas;

pilhas e filas:
- pilhas: LIFO - last in, first out - funciona como uma pilha, é mais fácil tirar de cima;
- filas: FIFO - first in, first out - funciona como uma fila, é justo tirar o primeiro a entrar;

- fila encadeada: 