## Introdução:
- geração -> | ingestão -> transformação -> serving | -> consumo
							(armazenamento)
- Transformação: organização, limpeza e preparação;
- Serving: disponibilização;
- Armazenamento em toda etapa, para sempre haver cópias.
- abstração > sistema de armazenamento > ingredientes;

## Object Storage:
- Guarda arquivos como objetos (ou seja, com um identificador único) - parece-se com uma tabela hash! - é o espaço em que guardamos dados;
- A chave de acesso é como o caminho de um arquivo;
- Objetos podem ser qualquer tipo de arquivo - normalmente, guardam vídeos e imagens, pois armazenamento por objeto, nesse caso, é mais barato;
- Pagamento somente pelo uso - não conta a margem adicional de segurança;
- Usa diversos níveis de equipamento;
- Buckets: isola projetos;
- Particionamento de dados: quebra de dados em pastas, para instalação manual depois.

## Data Lake:
- Repositório que armazena um grande volume de dados brutos;
- É barato;
- Permite arquivos estruturados (arquivo parquet ajuda, pois armazena tipos de tabela e é open source) e não estruturados em uma única plataforma;
- Object Storage é usado como base de Data Lakes;
- Ferramentas de processamento: *pandas* (melhor com bancos de dados pequenos) e *trino* (feito para tabelas em parquet);
- Assim, o Data Lake é a junção desses componentes: object storage, formato de arquivo e engine de computador (componente que manuseia os dados) - essa abstração é uma plataforma de dados;
- Essa estrutura, normalmente, é única entre empresas;
- PARQUET:
	- Arquivo colunar: faz carregamento por coluna - permite a seleção de dados e, dessa forma, é mais barato;
	- Vários arquivos conseguem funcionar como uma só tabela;
	- Apresenta estatísticas e schemas sobre os dados que ele guarda;
	- Comprime bem os dados, mas tem tempo de descompressão;
	- Amplamente adotado pela indústria;

## Compute Engine:
- Sempre fazer configuração do ambiente;
- Código, normalmente, é considerado string, para a leitura de zeros;
- Não precisa tratar tudo, só o essencial;
- Especificar os tipos de cada coluna, para não deixar a ferramenta interpretar só - escrever sempre com os tipos pré-definidos;
- Sempre fazer perguntas sobre valores e sobre quantidade de nulos: é uma boa prática;
- Cada registro no banco de dados tem uma chave única que os enumera e os diferencia, independente de repetições em outras categorias;
- Exemplos de engines: pandas, spark, trino;
- Arquitetura medalhão:
	- dados brutos -> | bronze -> silver -> gold | -> downstream
- Empresas normalmente usam diversas ferramentas para problemas diferentes - ferramentas que, muitas vezes, não se integram bem entre si e são difíceis de deixar, em razão do preço de trocar para uma nova plataforma;
- Sempre se deve levar em questão o tempo de uso da plataforma escolhida;
- Ver diferenças entre gerenciado x self-hosted;