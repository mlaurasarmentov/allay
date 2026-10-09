# Revisão:

- Front:
	- Interação de usuário;
	- Visualização;
	- Design;
	- Requisições;
	- Hospedado na web, mas usa o poder de processamento local;
	- Front -> Autenticação -> API.
- Back:
	- Deixa a aplicação segura e a faz funcionar;

# Sobre memória:

- Em vez de usar memória RAM, você usa uma memória mais lenta, mas maior;
- Durabilidade, 
- Aumenta a escalabilidade;
- Pode ser usado por várias máquinas ao mesmo tempo;
- Por que não arquivos?
	- Salva, mas não escala;
	- Busca lenta: precisa ler o arquivo inteiro;
	- Dados repetidos;
	- Não permite escrita concomitante - apaga uma das requisições;

# Que é um banco de dados?

- Guarda, *organiza* e entrega dados rápido, sempre que é requisitado;
- Fácil de encontrar informações;
- Ajuda a mexer nos dados e a controlar quem acessa (princípio do mínimo acesso);
- Faz autenticação;
## Que são dados?
- Estruturados: formato fixo (linhas e colunas);
- Semiestruturados: tem estrutura, mas cada registro pode ter campos diferentes (pode ter tipos diferentes por registo);
- Não estruturados: sem organização e sem formato definido - o banco guarda, mas não entende o conteúdo;
### Dados relacionais:
- Tabelas: cada tabela tem nome único, linhas e colunas;
- Dados relacionados: 
