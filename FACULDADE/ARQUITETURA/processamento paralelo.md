# Introdução:

- Aumento de desempenho nos PCs - algumas aplicações precisam de mais desempenho;
- A área da computação que lida com isso é **processamento de alto desempenho**;
- Há duas maneiras de resolver esse problema:
	- Modelos mais simples (menos precisos);
	- Arquiteturas paralelas / especiais.
	- aura
	- laura

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
	- Tempo novo de comando / Tempo velho de comando;
- Eficiência: SpeedUp / p;

# Pipeline: 

Técnica usada em processadores para executar vários estágios de instruções ao mesmo tempo;
- Ganho: tempo sem pipeline / tempo com pipeline;
- MIPS (RISC-V): exige 5 etapas:
	- 1. IF (Instruction Fetch): buscar instrução;
	- 2. ID (Instruction Decode): ler registradores;
	- 3. EX (Execution): executar instrução / calcular endereço;
	- 4. MEM (Memory Access): acessar operando;
	- 5. WB (Write Back): escrever resultado em registrador;
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
	- Estruturais: o hardware não permite a combinação de instruções no mesmo ciclo de clock (exemplo: dois acessos de memória);
	- Dados: o pipeline precisa ser interrompido enquanto um estágio está sendo concluído (solucionado por *fowarding* ou *bypassing*);
	- Controle: tomada de decisão baseada nos resultados de uma outra instrução enquanto outras estão sendo feitas (solução: bolha, instrução de desvio ou previsão - coloca-se NOPs para software, curto circuito para hardware);