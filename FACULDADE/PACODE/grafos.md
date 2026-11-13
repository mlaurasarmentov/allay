# Introdução:
- Nós e arestas;
- Se todos os nós, ligados entre si, fazem uma imagem completa, eles têm um ciclo;
- Ciclos devem ser feitos por, pelo menos, mais de 2 nós;
- Um grafo pode ter mais de um ciclo;
- Árvores: são grafos com n nós e n-1 arestas;
- Grafos podem ter direções entre suas arestas: são grafos dirigidos / direcionados;
	- Para isso, transformamos as arestas em setas;
## Representações de grafos:
- Matriz de adjacências:
	- Ideal para visualização;
	- Bom para menores entradas;
	- Implementação: `vector<vector<int>> g(n, vector<int> (n));`

| X   | 0   | 1   | 2   | 3   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 1   | 1   |
| 1   | 1   | 0   | 0   | 0   |
| 2   | 1   | 0   | 0   | 0   |
| 3   | 1   | 1   | 0   | 0   |

- Lista de adjacências:
	- Bom para maiores entradas;
	- Implementação: `vector<vector<int>> g(n);`
<center>0: 2 - 3</center>
<center>1: 0</center>
<center>2: 0</center>
<center>3: 0 - 1</center>

# Algoritmos:
## DFS (Depth Firts Search):
- Percorre todos os nós alcançáveis, a partir de um nó inicial;
- Cada nó é visitado e marcado, para não ser revisitado:
	- Se ele já tiver sido visitado (checado na marcação), ele é pulado.
- DFS recursivo x DFS interativo;
	- Usa a recursão para tomar as decisões de que ramo escolher, até acabarem os ramos livres (não marcados);
	- Código recursivo:
	  `vector<bool> vis(n, false);
	  `void DFS (int no) { 
	  `vis[no] = true;
	  `for (int viz : g[no]) 
	  `{ if (vis[viz] == true) continue;
	  `DFS(viz) 
	  `}}

## BFS (Breadth First Search):
- Percorre todos os nós alcançáveis a partir de um nó inicial;
- Faz uma busca em níveis - sua diferença principal a DFS;
- A lógica de um nó ter sido visitado ou não continua;
- Funciona para reconstruir caminhos, achar o caminho mais curto...
- Usa filas para a implementação em hierarquia;
- BFS multi-source: começa o BFS com mais de uma origem, ou seja, mais de um BFS ao mesmo tempo;
- Código:
	`queue<int> q;
	`queue.push(1);
	`vis[0] = true;
	`while (!q.empty()){
		`int no = q.front();
		`q.pop();
		`for (auto viz:g[no]){
			`if (vis[viz]) continue;
			`q.push(viz);
			`vis(viz) = true;` // sem essa linha, repete-se a contagem de um nó!
		`}
		`
	`}