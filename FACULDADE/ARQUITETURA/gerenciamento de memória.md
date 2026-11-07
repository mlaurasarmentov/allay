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
- Usado para programação monousuário:
	- **Programação monousuário:** o sistema executa somente um programa de usuário por vez, o qual usa toda a área do usuário, liberando para o próximo só no fim de sua própria execução.
	- Como os programas não compartilham memória, não há porque proteger um processo do outro;
	- Enquanto a CPU espera uma operação E/S, a CPU fica parada.
- Funcionamento:
	- SO ocupa a parte inicial da memória, com a tabela de interrupções;
	- Usuário trabalha com os endereços depois do SO, limitados pelo registrador de segurança (só aceita valores maiores que o limite do SO);
	- Na lógica do programa, o endereçamento do usuário sempre é somado ao limite;
- Relocação: