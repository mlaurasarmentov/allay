- variável que guarda textos - é um array de elementos do tipo *char* delimitado pelo caractere nulo;
- não há exatamente o tipo string, por isso, usamos arrays;
OU SEJA, strings são ponteiros que apontam para o primeiro elemento de um array de chars;

- o caractere nulo fica sempre no fim da string;
- array pode ter mais elementos que a string: o caractere nulo pode acabar antes do fim do array;
- a string nunca será maior que o array;
- a constante string é escrita com aspas duplas;
- toda constante string fica na região de constantes;
- a função *puts*, por exemplo, recebe o início da string entre aspas - seu parâmetro;
- é boa prática, ao usar strings constantes, classificá-las como *const*;
- uma string SEMPRE deve ter (número de elementos = número de letras + 1), para termos espaço p o caractere nulo;

regiões da memória:
- stack: pilha, guarda as variáveis;
- heap;
- constantes: quando tentam ser acessadas, destroem o programa;
- código;

SINTAXE: 
- caractere nulo: \0;
- usos das strings constantes:
	- char * str = "bolo"; ou char * str; str = "bolo";
	- printf("%s\n", str); ou printf(str);
- para poder alterar strings, determina-se uma string não constante:
	- char str[] = "bolo";
- leitura de strings com somente uma palavra:
	- char nome[31] - lê uma string de tamanho 30 (elementos + nulo);
	- scanf("%s", nome); - armazena o scan no array nome;
- leitura de strings com mais de uma palavra (DO MAL):
	- gets(nome) - não limita o input do usuário, de modo que pode corromper a memória: por isso, preferimos fgets(armazenamento, limite, arquivodeorigem);
	- no fgets, em vez de ser esquecido, o enter inserido vai para a impressão, esvaziando totalmente o buffer;
	- para aparar o \n, faz-se (tamanho da string - 1) e se move - \0 para esse índice no array;