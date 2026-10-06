# Introdução:

- Aumento de desempenho nos PCs - algumas aplicações precisam de mais desempenho;
- A área da computação que lida com isso é **processamento de alto desempenho**;
- Há duas maneiras de resolver esse problema:
	- Modelos mais simples (menos precisos);
	- Arquiteturas paralelas / especiais.

# Arquiteturas paralelas:

- Obtém melhor desempenho ao usar mais unidades ativas (processadores, comumente);
- Com mais processadores, o sistema computacional fica mais complexo -> programação mais complexa;
- Processamento paralelo: várias unidades colaboram na resolução de um mesmo problema em menos tempo;
	- Os programas devem ser preparados para computadores paralelos;
	- Melhor desempenho, redução da probabilidade de falhas, aproveitamento de recursos;
	- Problemas: dependência e distribuição de dados, sincronização e áreas críticas;
	- Toda aplicação tem um número ideal de unidades ativas;
- Granulação (nível de paralelismo):
	- Fina: unidades pequenas;
	- Média: unidades médias;
	- Grossa: unidades grandes.
- 