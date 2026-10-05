# Introdução à álgebra de Boole:

- Usa-se a ideia da lógica tradicional, ao separar dois estados finais de uma premissa: verdadeiro ou falso;
- Circuitos lógicos usam a álgebra booleana (em expressões lógicas)E, a fim de representar esses estados;
- Expressões lógicas descrevem a ligação entre a saída e a entrada;
- As portas lógicas implementam as funções lógicas, construindo todos os sistemas;
- Com a álgebra de Boole, circuitos grandes podem ser substituídos por outros menores, sem perda de informação;
	- Essa álgebra só usa três operações: AND, OR e NOT;
	- AND: representado pela multiplicação;
	- OR: representado pela soma;
	- NOT: representada pelo traço em cima da letra;
	- Transições simultâneas em OR deixam uma reta em seu lugar (glitches ou spikes);
- Regras de avaliação:
	1. Primeiro as inversões;
	2. Parêntesis;
	3. AND;
	4. OR.

# Circuitos digitais:

- Podem ser classificados em:
	- Circuitos combinacionais: saída vem da entrada corrente - não armazena valores;
	- Circuitos sequenciais: saída vem da entrada corrente e da entrada anterior - armazena memória;

# Barramento:

- Os barramentos conectam as partes da máquina;
- Barramento é um conjunto de fios paralelos que permite a transmissão de dados, de endereços, de sinais de controle e de instruções;
- Tipos de barramento:
	- Interno ao processador: ocorre entre a ULA e os registradores;
	- Externo ao processador: ocorre entre CPU, memória e dispositivos de entrada e de saída;
	- Barramento de dados (bidirecional): transferência de dados e de instruções entre processador, memória e dispositivos entrada / saída;
	- Barramento de controle (bidirecional): sincroniza atividades do sistema;
	- Barramento de endereços (unidirecional): seleciona origem ou destino de sinais - conduz endereços;

- Controladora: contém a maior parte dos circuitos elétricos de um dispositivo - está encarregada de controlar o dispositivo e tratar seu acesso ao barramento;
	- Também pode ser responsável por acesso direto à memória;
- Interrupção: a controladora de um periférico para um programa corrente para rodar um procedimento especial - rotina de tratamento da interrupção;
- Arbitragem de barramento: decide de quem será a vez de usar o barramento da máquina, entre periféricos (dispositivos de entrada e de saída) e o processador;
	- Arbitragem centralizada: um árbitro controla a vez de acesso do barramento no dispositivo;
	- Arbitragem descentralizada: não usa árbitro - o dispositivo deve usar a linha de requisição para pedir controle, e todos os dispositivos controlam essa linha;
- Protocolo de barramento: é um conjunto de regras que definem como será feito o barramento;
- Os dispositivos ligados ao barramento podem funcionar como:
	- Mestres: são ativos no processo, comandam o barramento;
	- Escravos: são passivos no processo, seguem o barramento definido pelos mestres;
- Temporização do barramento: 
	- Barramentos síncronos: usa clock para medir o as atividades - toda tarefa de barramento gasta um ciclo de cristal, ou seja, um ciclo de clock;
		- Todo dispositivo dura o mesmo tempo de uso;
		- Nenhuma ou pouca lógica necessária;
		- Baixo custo;
	- Barramentos assíncronos: não usam clock para sincronizar informações;
		- A comunicação ocorre por *handshaking*, um processo de tempo automático;
		- Dispositivos podem ter tempos diferentes;
		- Adaptável a outras tecnologias;
		- Precisa de mais lógica;
		- Menor banda passante (quantidade de dados que pode ser distribuída em tal quantidade de tempo).