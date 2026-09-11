sintaxe = int ****p //em que * sinaliza que é um ponteiro;
*p // acesso indireto, de modo que é o apelido da variável apontada.

com ponteiros, podemos fazer novas funções: teremos uma função com parâmetro de saída, ou de entrada e de saída.

assim, temos que ****p controla o valor de quem ele aponta!

ademais:

	*p tem o endereço de seu apontado (&x)
	é boa prática começar definindo o ponteiro como vazio (int *p = NULL;)
	com os ponteiros, não precisamos retronar valores em funções
	SEMPRE especificar que a função ganha um valor ponteiro (*p)
	ao terminar de usar ponteiros, pode-se anulá-los - é boa prática


