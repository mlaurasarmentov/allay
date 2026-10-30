# Que é front?

- É a parte do sistema que roda no cliente. Conversa com o servidor e transforma em interface;
- Chegada da web: troca de dados de modo instantâneo - nada para instalar, protocolo padrão;

## Evolução da web:
- Fase estática (HTML e CSS): a página vinha pronta, cada clique recarregaria tudo;
- Fase interativa (AJAX): a página conseguia procurar por dados sem recarregar;
	- Surgimento do flash!
- Fase de componentes (REACT): react (criado pelo Facebook) - faz página em componentes, a tela vira componentes reutilizáveis;
	- Experiência de navegação scroll, só os componentes da timeline se alteram;
- Fase de renderização (Next e SSR): a renderização de páginas volta a ser responsabilidade do servidor;

CGI -> PHP / ASP -> App servers 

### Além do visual:
- UI: interface usada pelo usuário (layout, componentes...);
- UX: experiência do usuário (performance, fluxos, feedback...)
- Acessibilidade: leitura de teclado, acesso;
- Dados: dados salvos e filtrados pelo servidor;

## Designer:
- O designer precisa pensar na experiência do usuário e otimizá-la - algumas métricas comuns são cliques, tempo de espera...
	- Checar posthog;
- Jornada do usuário:
	Descobre -> Entra -> Usa -> Volta
- Experiência de espera: 
	- Loading: algo visual se mexendo;
	- Skeleton: esqueleto do layout que chegará da página;
	- Otimista: mostra a ação ao usuário antes dele ser confirmado;

## Engineer:
- Cuida da parte de fetch, stream, handle, store e context: dados chegam, são tratados, guardados e distribuídos na página;
- Estruturação de fluxos de usuário (em árvore, por exemplo), para esquematização;
- Administração de cache:
	- HTTP (cache do navegador) -> Cliente (Cache de dados) -> Invalidar (Quando jogar fora, clear Cache);
	- Stream: o cliente recebe a resposta da web pedaço por pedaço, em vez de ter a resposta inteira -> a resposta chega sempre, em chunks;
- 