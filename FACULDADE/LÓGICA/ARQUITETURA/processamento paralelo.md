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
- SpeedUp: indica o aumento de desempenho;
	- Cálculo: tempo de execução em um processador / tempo de execução em p processadores;
- Eficiência: SpeedUp / p;

# Pipeline: 

Técnica usada em processadores para executar vários estágios de instruções ao mesmo tempo;
- Ganho: tempo sem pipeline / tempo com pipeline;
- MIPS: exige 5 etapas:
	- 1. Buscar instrução;
	- Ler registradores;
	- Executar instrução / calcular endereço;
	- Acessar operando;
	- Escrever resultado em registrador;
- Ciclo único x Pipeline:
- Ciclo único:
	- Cada instrução MIPS tem cinco estágios, levando 1 ciclo de clock (tempo entre instruções);
	- O ciclo de clock deve ser igual ao *tempo total* da *instrução* mais lenta;
- Pipeline:
	- O ciclo de clock deve ser igual ao tempo de duração do *estágio* mais lento;

|               Classe               | Busca | Leitura de registadores |  ULA  | Acesso a dados | Escrita de registradores | Tempo total |
| :--------------------------------: | :---: | :---------------------: | :---: | :------------: | :----------------------: | :---------: |
|                Load                | 200ps |          100ps          | 200ps |     200ps      |          100ps           |    800ps    |
|               Store                | 200ps |          100ps          | 200ps |     200ps      |            -             |    700ps    |
| Formato R (add, sub, and, or, slt) | 200ps |          100ps          | 200ps |       -        |          100ps           |    600ps    |
|            Branch (beq)            | 200ps |          100ps          | 200ps |       -        |            -             |    500ps    |

- Pipeline Hazards (riscos): quando a próxima instrução não pode ser executada no ciclo de clock seguinte;
	- Estruturais:
	- Dados:
	- Controle: