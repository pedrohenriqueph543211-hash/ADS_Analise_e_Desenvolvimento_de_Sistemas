# Trabalho — Torre de Hanói

**Disciplina:** Estrutura de Dados  
**Aluno:** Pedro Henrique Souza Mendonça 

## Parte 1 – Conceitos Gerais

**1. O que representa o problema da Torre de Hanói?**

Representa um problema clássico de recursão e manipulação de pilhas, onde se deve mover uma pilha de discos de uma haste para outra, respeitando regras específicas.

**2. Quem foi o criador da Torre de Hanói e em que ano ela foi proposta?**

Foi criada pelo matemático francês Édouard Lucas em 1883.

**3. Quais são as três regras fundamentais do jogo da Torre de Hanói?**

- Apenas um disco pode ser movido por vez.
- Cada movimento consiste em retirar o disco do topo de uma haste e colocá-lo no topo de outra haste.
- Um disco maior nunca pode ser colocado sobre um disco menor.

**4. Qual é o objetivo principal do algoritmo da Torre de Hanói?**

Mover todos os discos da haste de origem para a haste de destino, utilizando uma haste auxiliar, respeitando as regras do jogo.

**5. Qual é a fórmula que calcula o número mínimo de movimentos necessários para resolver o problema com n discos?**

M(n) = 2ⁿ - 1.

**6. Quantos movimentos são necessários para resolver o problema com 3 discos?**

2³ - 1 = 7 movimentos.

**7. Qual o tempo de complexidade do algoritmo da Torre de Hanói?**

O(2ⁿ), ou seja, complexidade exponencial.

**8. Por que o problema da Torre de Hanói é considerado um exemplo clássico de recursão?**

Porque a solução pode ser definida em termos de si mesma. Mover n discos exige mover n-1 discos duas vezes, resolvendo problemas menores com a mesma lógica.

**9. O que significa caso base em um algoritmo recursivo, e qual é o caso base na Torre de Hanói?**

Caso base é a condição que interrompe a recursão. Na Torre de Hanói, é quando n == 1, movendo o disco diretamente da origem para o destino.

**10. O que acontece com o número de movimentos totais quando se adiciona mais um disco ao problema?**

O número de movimentos dobra e soma mais um: M(n+1) = 2 × M(n) + 1.

## Parte 2 – Código Java

**11. Qual é o papel dos parâmetros origem, destino e auxiliar no método moverDiscos()?**

- origem: haste de onde os discos serão movidos.
- destino: haste para onde os discos devem ser levados.
- auxiliar: haste usada como apoio intermediário durante os movimentos.

**12. O que acontece se o caso base if (n == 1) for removido do código?**

O algoritmo entra em recursão infinita, pois não terá uma condição de parada, podendo resultar em um StackOverflowError.

**13. No trecho abaixo, o que significa a linha moverDiscos(n - 1, origem, auxiliar, destino)?**

Essa linha move os n-1 discos superiores da haste de origem para a haste auxiliar, usando a haste destino como apoio.

**14. Por que o algoritmo chama o próprio método dentro dele (recursão)?**

Porque o problema pode ser dividido em problemas menores e com a mesma lógica. Mover n discos exige resolver duas vezes o problema com n-1 discos.

**15. O que a função System.out.println() exibe em cada iteração da função recursiva?**

Exibe o movimento atual, informando qual disco está sendo movido e entre quais hastes.

**16. Como o número de chamadas recursivas está relacionado ao número de discos (n)?**

O número total de chamadas recursivas é 2ⁿ - 1, correspondendo ao número de movimentos.

**17. O que aconteceria se os parâmetros destino e auxiliar fossem trocados na primeira chamada recursiva?**

A lógica ficaria incorreta, pois os discos seriam movidos para o destino errado, prejudicando a resolução do problema.

**18. Qual é o tipo de dado utilizado para representar as hastes (A, B, C) no código?**

Normalmente são utilizados char (caractere) ou String, passados como parâmetros para identificar as hastes.

**19. No programa com contador de movimentos, qual é a finalidade da variável contador?**

Armazenar e incrementar o número de movimentos realizados, permitindo exibir a contagem total ao final da execução.

**20. Se n = 4, quantos movimentos o programa imprimirá no total?**

2⁴ - 1 = 15 movimentos.

---

**Conclusão:** A Torre de Hanói demonstra como a recursividade pode resolver problemas dividindo-os em etapas menores, respeitando as regras de movimentação dos discos.
