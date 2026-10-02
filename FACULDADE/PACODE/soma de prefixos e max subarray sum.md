# Soma de prefixos:

## Uma dimensão:
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
- O vetor sum acaba com índice+1 do vetor inicial.

## Duas dimensões:
- Calcular uma sub-matriz dentro de uma matriz;
- Espaço = total - sobra1 - sobra2 + interseção;
	- `pref(l2)(c2) = prefix[l2][col1-1] - prefix[l1-1][col2] + prefix[l1-1][col1-1]

# Max subarray sum:

- Dado um array, queremos encontrar um segmento em que a soma dos intervalos é máxima;
- Checar Kadane;
- Queremos achar o valor em que prefix(l-1) é menor:
	- Por cálculo, para achar [r, l], `prefix[r] - prefix[l-1]`;
- 