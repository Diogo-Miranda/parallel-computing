**Programação estruturada:**

Vira um padrão quando é considerada uma boa prática de programação.

Problemas: Seriualização de código

*Serialização*:
- Possui ordem temporal
- É determinítica
- Fácil de codificar testar e depurar.
- Perde em paralelismo

**Programação Paralela Estruturada**:

É composta por padrões paralelos ou esquelos algorítmicos ou paralelos

- Fork-Join,
- Map,
- Reduce,
- Scan,
- Stencil etc.

Vantagem: elimina o uso explícito de threads.

a) Fork-Join:

- É o padrão mais simples
- Replica o mesmo código para várias threads trabalhadoras
- A thread mestre dispara (fork) para várias thread trabalhadoras e elas sincronizam-se quando sobra apenas a thread mestre (join).

b) Map:

- Replica uma função sobre cada elemento de um conjunto de índices (ou dados diferentes)

- Exemplo: parallel for, em que cada índice do vetor, passamos para uma thread executar, e as mapeiam em um índice do vetor.

obs: Dados devem ser independentes.

c) Reduce:

- Combina cada elemento de uma coleção de elementos, utilizando um operador, até reduzi-los em um único elemento.

d) Stencil:

- Generalização do MAP, onde cada função não acesso somente um elemtno, mas também seus vizinhos.

Obs: condições de borda

- Exemplos: convolução de imagens…

e) Scan:

- Para cada elemento computa reduções parciais de uma coleção de elementos, ou seja, para cada saída, uma redução parcial é computada até o elemento atual.
