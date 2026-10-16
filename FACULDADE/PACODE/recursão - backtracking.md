# Função recursiva:

- Uma função que chama a si mesma;
	- Caso base: um caso fixo, define o fim da recursão / do programa;
	- Caso recursivo: o caso que se repetirá;
	- Parâmetros: o que entra na função;
	- Chamada: enquanto não aparecer o caso base, a função chama a si mesma (comumente em seu return default, fora de ifs);
	- Os retornos se completam pela fila de tarefas para completar;
	- Exemplos: fatorial e fibonacci;
- É mais lenta que uma função iterativa;
- Importante para questões de força bruta;
- Pilha recursiva;
- Cuidados: 
	- Normalmente, todos os casos são salvos, de modo que gasta muita memória;
	- Deve-se prestar atenção, a fim de não fazer uma função infinita;