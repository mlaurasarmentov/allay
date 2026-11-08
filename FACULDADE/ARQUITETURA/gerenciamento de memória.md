# Introdução:
- **MMU (Unidade de gerenciamento de memória):** fica entre a CPU e a memória, tem três funções:
	- *Traduz* o endereço lógico (endereço virtual) criado pelo programa em um endereço físico, usando o Registrador Base e a tabela de páginas / de segmentos;
	- *Verifica* a proteção (se a página é válida / inválida, o tipo de acesso permitido, se houver escrita, liga dirty bit);
	- *Gera* uma interrupção se algo falhar e passa a responsabilidade para o SO;
	- Em caso de falha:
		- O SO consulta o descritor do processo;
		- Se a página estiver fora do espaço de endereçamento do processo, o processo é abortado;
		- Se é do processo mas ainda não foi carregada, é falta de página, a instrução é reexecutada.
- **TLB (Translation lookaside buffer):** é um cache de traduções, guarda os pares (pág virtual e pág física) usados mais recentes, todas as chaves são comparadas ao mesmo tempo;
	- É criada no hardware, dentro da MMU, não é uma estrutura de software;
	- Facilita a tradução;
	- O SO só a gerencia.
- **Importância da TLB para o desempenho da MMU:** armazenando os dados dos acessos mais recentes (traduções), diminui o acesso direto à memória principal. Sem a TLB, cada acesso do programa exigiria dois acessos à memória (um para a tabela, outro para o dado).

# Monoprogramação x Multiprogramação:
- Na Monoprogramação, só um programa ocupa a memória / CPU por vez;
- A Multiprogramação permite o compartilhamento de CPU por vários processos, incrementando a complexidade de comunicação entre componentes computacionais.
- Para padronizar a multiprogramação, desenvolveram-se mecanismos de gerenciamento de memória (ferramentas de alocação e de proteção).

## Máquina pura:
- Sistema sem gerenciamento de memória;
- O usuário lida diretamente com o hardware e controla totalmente a memória;
- Vantagens:
	- Mais flexibilidade;
	- Mais simplicidade;
	- Menor custo: sem software / hardware adicional.
- Desvantagens:
	- Sistema Operacional não controla interrupções (ausência de alguns serviços);
	- Não há monitor residente para processar chamadas do sistema ou erros;
- Normalmente usado em sistemas embarcados, em eletrodomésticos...

## Monitor residente:
- Divide-se a memória entre o espaço do usuário e o espaço do sistema operacional;
	- A área do SO guarda a tabela de interrupções
- Usado para **programação monousuário**:
	- **Programação monousuário:** o sistema executa somente um programa de usuário por vez, o qual usa toda a área do usuário, liberando para o próximo só no fim de sua própria execução.
	- Como os programas não compartilham memória, não há porque proteger um processo do outro;
	- Enquanto a CPU espera uma operação E/S, a CPU fica parada.
- Funcionamento:
	- SO ocupa a parte inicial da memória, com a tabela de interrupções;
	- Usuário trabalha com os endereços depois do SO, limitados pelo registrador de segurança (só aceita valores maiores que o limite do SO);
	- Na lógica do programa, o endereçamento do usuário sempre é somado ao limite;
### Relocação Estática:
- Endereços relativos viram endereços absolutos ao programa ser carregado;
- O código executável deve conter os códigos que referenciam todos os endereços (a informação de relocação).
### Relocação Dinâmica:
- Os endereços permanecem lógicos (ou seja, nunca são somados com o endereço lógico, para se tornarem endereços físicos), o **registrador base** é somado a cada acesso;
- **Registrador base / Registrador de relocação:** guarda o endereço físico em que cada programa começa. A CPU soma esse valor aos endereços lógicos gerados por programa, em tempo de execução; 
- Permite a movimentação de programas, a modificação do espaço do SO a qualquer momento e a inclusão de controladores de dispositivos;
- **Endereços lógicos:** o que o programa vê, vai de 0 até o MÁXIMO;
- **Endereços físicos:** o que o SO vê, vai de REG. BASE até REG. BASE + MÁXIMO;

## Swapping:
- Usa o disco para transformar o monitor residente monousuário em multiusuário;
- O programa que perde a CPU é copiado no disco (*swap out*), enquanto o que ganha a CPU sai do disco e vai para a memória principal (*swap in*, é uma troca, um swap!);
- Códigos executáveis ficam no disco e vão para a memória quando são chamados;
- Permite multiprogramação com memórias pequenas;
- É lento, pois custa a troca de uma grande quantidade de dados entre disco e memória, além de que, como o disco processa lentamente, deixa um dos processos mais lento;
- Se for frequente / a memória estiver sobrecarregada, o sistema gasta mais tempo na troca que na execução, isso se chama *thrashing*.

## Partições:
- Vários programas compartilham a memória ao mesmo tempo;
- A memória é dividida pelo número existente de programas;
### Partições fixas:
- Estáticas, partições que não mudam de lugar/tamanho;
- Ou seja, a memória é dividida em partições que não são alteradas durante a execução do sistema;
- O problema é a subutilização de memória, em razão da fragmentação interna;

### Partições variáveis:
- Têm regiões dinâmicas, a memória é alocada sob demanda;
- O SO guarda informações sobre quais partes de memória estão disponíveis e sobre quais partes estão ocupadas;
- Ao terminar, o processo libera a área - porém, com o tempo, podem aparecer buracos entre endereços de processos, de modo que se forma a fragmentação externa;
- Sempre existe um conjunto de áreas livres na memória -> o conjunto é procurado e parte dele vai para um programa (se a área for maior, o restante fica livre);
- Quando o processo termina, a área é liberada;
- **Algoritmo Best-fit:** escolhe o menor buraco que cabe o processo, é bom para quando há muitos processos pequenos, para preservar grandes buracos, mas deixa fragmentos pequenos;
- **Algoritmo Worst-fit:** escolhe o maior buraco encontrado, para que a sobra continue útil, é bom para processos de tamanhos parecidos, mas desperdiça buracos grandes.

## Paginação:
- Partições variáveis, apresenta **fragmentação externa**;
- A **fragmentação externa** é resolvida dividindo a memória lógica em páginas e a memória física em frames (ambos do mesmo tamanho, definido pelo hardware);
- Cada endereço gerado pela CPU é quebrado em duas partes: um número de páginas (p) e um deslocamento (d) -> o endereço lógico é (p, d);
- A memória lógica está dividida em blocos denominados *páginas lógicas*;
- A memória física do computador está dividida em *páginas físicas / frames*;
- Ocorre fragmentação interna na última página.

# Algoritmos de susbtituição de páginas:
- FCFS / FIFO: "First Come, First Served", segue a regra de fila, o primeiro a chegar é o primeiro a sair, ou seja, sai a página que está a mais tempo na memória;
- LRU: quando há necessidade de espaço, o menos usado é descartado;
- Second Chance (Segunda Chance): FIFO com bit de referência. A página mais antiga só sai com *bit 0*; se for 1, o bit vira 0 e a página vai para o fim da fila (ganham uma "segunda chance");
- FIFO + Second Chance: segue a regra FIFO, contudo se retornar, recebe uma segunda chance, ou seja, dura mais que uma página normal;

# Geral (inspirado nas questões teóricas):
- Memória interna x Memória externa:
- Capacidade x Tamanho físico:
- Taxa de transferência de barramento:
- Hierarquia de memória:
- Nível alto x Nível baixo:
- Volátil x Não volátil:
- RAM estática x RAM dinâmica:
- Memórias semicondutoras somente leitura (ROM) e principalmente leitura:
- Célula de memória:
- "Por que usar cache?":
- "Que a cache contém?":
- Acertos e erros (*hit* e *miss*):
- As duas formas de organização:
- Localidade *temporal* x Localidade *espacial*: