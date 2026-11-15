# Funcionamento geral:
- O claude code não é um chat, mas um modelo em loop, com ferramentas próprias - o modelo usa seu harness para fazer ações dentro do computador (abrir e editar documentos, trazer informações...);
- Ele trabalha em loops de **pensar -> escolher ferramenta -> agir -> analisar resultado**;
- Usa o contexto para saber o que foi feito, mas, se o armazenamento de contexto estiver cheio, ele pode resumir e compactar;
- O claude code trabalha em um terminal sempre acessível pelo aplicativo, para checagem rápida de ações;
- 