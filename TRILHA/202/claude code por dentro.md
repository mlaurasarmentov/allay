# Funcionamento geral:
- O claude code não é um chat, mas um modelo em loop, com ferramentas próprias - o modelo usa seu harness para fazer ações dentro do computador (abrir e editar documentos, trazer informações...);
- Ele trabalha em loops de **pensar -> escolher ferramenta -> agir -> analisar resultado**;
- Usa o contexto para saber o que foi feito, mas, se o armazenamento de contexto estiver cheio, ele pode resumir e compactar;
- O claude code trabalha em um terminal sempre acessível pelo aplicativo, para checagem rápida de ações;
- Arquivos markdown (como CLAUDE.md) servem para dar contexto à IA sobre o que ela deve saber / como ela deve agir, com informações que não podem ser inferidas somente lendo código;
### Comandos importantes:
- `/help`: mostra os comandos disponíveis;
- `/context`: mostra como está a tabela de contexto;
- `esc`: para um comando do claude code enquanto ele roda.