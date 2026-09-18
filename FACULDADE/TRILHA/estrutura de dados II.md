- tuplas: 
	- ordenadas;
	- imutáveis;
	- heterogêneas;
	- permite duplicatas.

- dicionários:
	- valores que se referem a outros valores: 
		- f = {"james": 1234}
		- f["james"] : 1234
	- chaves são usadas para acessar valores: 
		- d["key"] = value
	- há uma função (hash) que tranforma nomes (a chave) em um índice de um array, fazendo a ligaçaõ nome-número;
	- hash recebe um objeto e o transforma em um inteiro constante;
	- colisão de valores: hash retorna um valor igual para dois keys diferentes;
	- ser "hashable": o objeto tem a propriedade de, depois de passar pela função hash, sempre retornar o mesmo valor;
	- as chaves devem ser imutáveis: então, prefere-se usar, por exemplo, tuplas para chaves;
	- em teoria, a função hash deve ser injetora: por isso, fazemos soluções para quando ela não for;
	- a hash não é sobrejetora - ela não volta;
	- dicionários guardam uma imagem (valor de y, a chave) de um domínio (valor de x) da função hash - essa chave, por si, é parte do domínio que guarda a imagem do valor;
	- cada valor imagem tem um índice correspondente: é como se fossem relações transitivas! a transitividade vem da associação valor-índice do dicionário;
	- o dicionário tem, dentro de si, chave-valor;

BIG O:
- como calculamos quantas operações são usadas para realizar um algoritmo;
- a quantidade de operações varia de acordo com o número de funções e com a sua complexidade de tempo;
- quantidade de iterações
- o objetivo é sempre ir comparando com os outros casos da tabela BIG O;
- o maior valor na operação BIG O é o valor que será contado;
- usa-se complexidade de tempo e complexidade de espaço;

SETS:
- estrutura p conjuntos;
- não tem duplicatas;
- não tem ordem;
- faz operação de conjuntos;
- não usa acesso por índice;
- é mutável - por isso, não é "hashable";
	- o frozen set é imutável, portanto, é "hashable".

SINTAXE:
- criar_dicionario = {}
- criar_set = set()
- .update = atualiza o dicionário

INTERESSANTE:
- pesquisar funções de hash (sha256. sha1);
- fazer o leetcode twosum, contains duplicate;
- complexidade de espaço é mais usada em big data e em sistemas embarcados;
- LIVRO: "entendendo algoritmos" (livro dos ratinhos);