VOCÊ PODE ORDENAR ARRAYS SEM COMPARAÇÕES (magia - ordenação por contagem):
- soma quantas vezes cada número aparece;
- soma com o anterior;
- faz checagem.

falhas desse algoritmo: 
- não suporta números negativos;
- não suporta números quebrados;
- não suporta intervalos __muito__ grandes, para não fazer arrays enormes - ou seja, usaria muita memória!

	__ARITMÉTICA DE PONTEIROS:__
- soma e subtração com inteiros ou entre ponteiros;
	- entre ponteiro e número: o resultado é um novo endereço de memória;
	- entre ponteiros: o[[arrays]] resultado é um inteiro.
- fator de escala: nós fazemos nossa aritmética de acordo com o tamanho da variável usada (para descobrirmos esse tamanho, colocamos um sizeof);
	- exemplo: se usarmos int e somarmos 1, nós estamos passando 4 bytes!
- lembre-se: usamos hexadecimal, ou seja, depois de 16, vamos ao próximo caractere;
	- exemplo: e10 + 7 = f1
- o resultado da subtração de dois endereços é quantas variáveis do tipo apontado cabem entre tais endereços;

- [] é um operador de aridade 2, ou seja, 1 operador com 2 operandos!
- logo, temos que ar = ponteiro, isso é, um endereço de memória / i = inteiro, de modo que: ar[i];
- i[ar] = ar[i], pois i[ar] = * (ar + i) = ar[i];

- nós podemos retornar um array de uma função usando o parâmetro static;

- const = faz variáveis constantes, portanto, não são alteráveis;
- diferença entre const e constante simbólica:
	- constante simbólica NÃO tem endereço de memória, ou seja, não é apontável, enquanto uma variável const é apontável.
- const com ponteiros:
	- caso 1: ponteiro constante (int * const p);
	- caso 2: ponteiro para uma constante (int const * p);
	- caso 3 : ponteiro constante para uma constante (int const * const p);
- constantes não aceitam entrar em ponteiros normais, para não poderem ter seus valores alterados;
- dessarte, podemos criar arrays protegidos, porque eles não poderão ser modificados por nossas funções.

- overflow de memória = tentamos colocar mais elementos que o possível em um array!
	- exemplo: 4 elementos em um array que somente suporta 3.

