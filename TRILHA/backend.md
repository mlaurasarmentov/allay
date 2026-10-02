# Como a Web funciona:

## Web:
- Aplicações que funcionam em rede: um dispositivo conectado a outro;
1. LAN: rede local, por roteador (normalmente wi-fi);
2. WAN: maior que as redes locais, várias LANs ligadas a longa distância;
3. WWW (Internet): a rede global de computadores, um conjunto de WANs, com amplitude global;
- Conexão cliente-servidor: ligação entre um browser (comumente) e um servidor.
	- Funciona com requisição-processamento-resposta;
- FastAPI: biblioteca usada para construir servidores backend (usa Uvicorn - uma ASGI -debaixo dos panos);
	- Uvicorn serve a aplicação: é uma interface de servidor assíncrona;
- Loopback: rodando em endereço local (localhost), só o computador host consegue acessar;

## Conversa cliente-servidor:
- WEB: -> URL: endereço para comunicação com um computador na rede, também tem o
			caminho do que quer ser acessado;
		-> HTTP: protocolo que especifica como a comunicação deve ocorrer;
		-> HTML: linguagem que estrutura sites na web (HTTPS é a mesma coisa, com 
			encriptação, por isso chamamos de seguro).
- Tudo se conecta com endereços ips e um porta;
- DNS (Domain Name System): nomes para sites e patentiação de domínio, não envia dados, mas localiza o endereço pedido;
	- Na camada de rede, transforma o domínio de um site em seu endereço de servidor;

## Autenticação:
- Autenticar é logar, entrar na internet;
- Autorização é ter acesso a espaços exclusivos na internet;

# HTTP na prática:

## HTTP:
- Protocolo de transferência de textos;
- Requisição e resposta;
- Status code: retorna um código para informar sobre a requisição feita;

# APIs e REST:

## API:
- Requisição -> Backend -> Resposta;
- O backend recebe, processa e decide, nesse ínterim;
- API: interface entre o cliente e o backend;
- Endpoint: fica no fim da URL, é o caminho para a requisição;
- API liga o cliente ao backend;

## REST:
- Uma API, para ser REST, segue o padrão HATEOAS (ou seja, ela precisa transferir HTML / hypermedia);
- JSON é muito usado em tráfego de texto;

# Contratos e schema:

## Schema:
- É o contrato de como uma rota da API funcionará;
- Estabelece um entendimento sobre os dados trocados;
	- O Pydantic vem com o FastAPI, ele identifica respostas não permitidas;
	- Escreve-se o que deve ser requisitado e o que deve ser enviado;
- Model: valida a parte do banco de dados;

