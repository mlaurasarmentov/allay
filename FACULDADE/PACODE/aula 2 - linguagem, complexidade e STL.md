## Linguagem:

- Escolha de linguagem: aprender C++;
- python e java: big int (vai até 10⁴⁰);
- cabeçalho:
	- `#include <bits/stdc++.h>`
	- `using namespace std;
- Fast input e fast output:
	- `ios::sync_with_stdio(false);`
	- `cin.tie(nullptr);`
- Evitar `endl` - flush automático - ou `define endl "\n"`;

## Complexidade:

- Complexidade de tempo: o quão rápido nosso código rodará, para não passar o limite de tempo;
- Notação BigO: variável n (tamanho da entrada);
	- Exemplos: $O(n)$, $O(n²)$;
- BigO ignora constantes: $O(100n)$ = $O(n)$;
- Complexidade amortizada: código, *em média*, o qual roda em uma operação;
- Complexidade de memória: uso de memória no código;

```cardlink
url: https://usaco.guide/
title: "USACO Guide"
description: "A free collection of curated, high-quality competitive programming resources to take you from USACO Bronze to USACO Platinum and beyond. Written by top USACO Finalists, these tutorials will guide you through your competitive programming journey."
host: usaco.guide
favicon: https://usaco.guide/assets/logo-square.png
image: https://usaco.guide//assets/social-media-image.jpg
```


## Estruturas de Dados:

| Característica / Tipo |  List  |                                         Stack (pilha)                                         |                                            Queue (Fila)                                             |                                                   Vector (vetor)                                                   |
| :-------------------: | :----: | :-------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------: |
|        Termos         |   -    |                                   LIFO - last in, first out                                   |                                     FIFO - first in, first out                                      |                                                 alocação dinâmica                                                  |
|       Inserção        | $O(1)$ |                                   sempre no último - $O(1)$                                   |                                      sempre no último - $O(1)$                                      |                                     $O(1)$ no final, $O(n)$ em outros lugares                                      |
|        Acesso         | $O(n)$ |                                   sempre o último - $O(1)$                                    |                                     sempre o primeiro - $O(1)$                                      |                                                       $O(1)$                                                       |
|         Extra         |   -    |                            para declarar: `stack<tipo dos itens>`                             |                                                  -                                                  |                                                         -                                                          |
|       Comandos        |  `-`   | `P.top(vê o topo), P.pop(remove do topo), P.empty(verifica se vazio), P.push(coloca no topo)` | `F.front(vê a frente), F.pop(remove da frente), F.empty(verifica se vazio), F.push(coloca na fila)` | `V.push_back(adiciona no fim), V.pop_back(remove no fim), V[i] (para acesso), V.erase(remove), V.insert(adiciona)` |

- Monotonic stack: aplicação avançada de pilha;
- `Sort(V.begin(), V.end())` - algorítimo de ordenação híbrido;
- `Pair<tipo, tipo> P` - guarda em pares.