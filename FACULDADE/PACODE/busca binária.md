## Métodos:
1. Busca linear: percorrer todo o array e verificar - O(n):
	- Inviável pela complexidade temporal;
2. Busca binária: divide para encontrar (n log n):
	- Verifica o do meio (por média aritmética);
	- Se for maior, descarta-se todos à direita. Caso contrário, descarta-se todos à esquerda (inclusive o meio achado; em vez disso, o meio virará o meio + 1);
	- No fim, ou teremos o elemento desejado ou ele não existirá no vetor (quando o limite do vetor for atingido, acabar-se-á a busca).