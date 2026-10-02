# Soma de prefixos:

- Técnica usada para calcular a soma de qualquer subarray;
- É um somatório no vetor, de i = 1 (começando de 1) até n (valor do index atual);
	- Sempre pega soma acumulada + atual;
	- exemplo: `prefix[i] = prefix[i-1] + arr[i]`;
- Pode ser usado para descobrir o somatório de valores entre índices;
	- Prefix-sum de algo - Prefix-sum do que vem antes;
	- Exemplo: `prefix[7] - prefix[2]` para conseguir o intervalo [3, 7];
- Complexidade $O(n)$ por pré-processamento, $O(1)$ para a consulta;
- Complexidade final = pré-processamento + consultas;
- Cuidado para deixar a indexação em 1: se ficar em 0, pode acabar com out-of-bound (-1) - usar n+1;
- O vetor sum acaba com índice+1 do vetor inicial;