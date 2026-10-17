- Cardinalidade: associação de componentes entre tabelas;
swagger -> fastAPI (com pydantic) -> SQLalchemy -> postgreSQL <- dbeaver (IDE de banco)
- ORM: em vez de fazer consultas diretamente com SQL, faz-se com classes;
- Bancos de dados só rodam em contâineres;
- Contâineres rodam em cima de linux e usam a funcionalidade do kernel de seu próprio linux, mas reaproveitando o sistema do seu computador - só roda o que você colocar nele;
- Porta: indica onde um processo roda no computador;