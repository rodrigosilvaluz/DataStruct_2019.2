# **Curso de Estrutura de Dados 2019.2 - UNICARIOCA -  Prof: Manuel Martins Filho**

![](/home/rodrigo/git-repository/DataStruct_2019.2/tux.jpeg) 
	
### 1. Tipos de Estruturas de Dados  

**1.1 Listas Lineares**


1.1.1 ***MOTIVAÇÃO***

> Tipo de Estrutura usada na solução de problemas que envolvem conjuntos de dados
>que se relacionam mantendo uma relação de ordem.
>
>Exemplo: Agenda Telefônica

>Os elementos de uma agenda são fichas com Nomes, Endereço e Telefone , organizadas
>em ordem alfabética. 
Tomando -se o devido cuidados quando da inserção de novas fichas, ou seja, respeitando-se a ordem alafabética, pode -se facilmente acessar o dado desejado sempre que for necessário . 
Como fichas podem ser inseridas ou removidas, o tamanho da 
>agenda (n de fichas) é variavel ao longo do tempo.

1.1.2 ***CONCEITUAÇÃO***

>Lista é a estrutura que permite representar um conjunto de dados de forma a preservar a ***relação de ordem**** entre eles. Uma lista é composta de nós (registros), sendo que cada nó
>pode conter um dado primitivo ou um dado composto.

>***Ex.1 - Um lista com as taxas mensais de inflação nos ultimos 24 meses. (Dado Simples)***

>***Ex.2 - Uma lista com Nome e Matricula dos alunos de uma escola.(Dado Composto)***

>***Ex.3 - Uma lista com Nome e Salários dos deputados estaduais do estado do RJ.***


> DEFINIÇÃO: **Lista** é uma coleção ***ordenada*** de componentes do mesmo tipo .
>Tipicamente este é o tipo de registro (struct or record).

> DEFINIÇÃO FORMAL: **Lista** é um conjunto de n nós **x1,x2,...xn** organizados estruturalmente de forma a refletir as posições  relativas dos mesmos.

```
Se n > 0
   x1 é o primeiro nó
   Para 1 < k < n.
   xk é precedido pelo nó xk-1 e seguido pelo nó xk+1
    Se n=0 a lista é vazia .
```

***Representação Física***

>L = { x1,x2,x3,....,xn } -> LIsta com nós

![](/home/rodrigo/git-repository/DataStruct_2019.2/struct_node.png) 

## Principais Operações sobre Listas

>1. Acessar o k-ésimo nó da lista para obter e/ou alterar o dado nele contido
>2. Inserir um novo nó antes ou após o k-ésimo nó da lista
>3. Remover o k-ésimo nó da lista 
>4. Concatenar duas listas
>5. Determinar o número de nós de uma lista
>6. Localizar o nó que contém um dado valor


1.1.4 ***FORMAS DE REPRESENTAÇÃO***

>Exitem várias formas de representar internamente uma lista no computador. 
Obviamente a escolha da  representação mais adequada depende não só dos ***tipos de operações*** que se deseja executar sobre a lista, como também, da ***frequência*** com que estas operações serão realizadas.
>Determinadas representações são mais favoráveis a algumas operações, enquanto outras não são, no sentido de exigir  um maior esforço computacional para a sua execução.

#### As Principais formas de representação são:

- ***Por contiguidade*** (Lista Sequencial) -  **Vetor**
- ***Por encadeamento*** (Lista ligada) -  **Ponteiro**

#### Por Contiguidade:
>- Explora a sequencialidade da memória do computador
>
>- Os nós (registros) são armazenados em endereços contiguos (lado a lado)
>- Relação de ordem: se o endereço do nó xk é conhecido, o endereço do nó xk+1 pode ser determinado

***Imlementação***
>A maneira mais simples e obvia de implementar uma lista em computador é através da utilização de um vetor. Esta representação é bastante satisfatória para algumas operações e bastante ineficiente para otras. Ela é utilizada em situações em que as inclusões/exclusões são realizadas sempre no final da lista (não são necessarias inclusões/exclusões em posições intermadiárias).Apresenta-se a seguir, vantagens e desvantagens da implementação de uma lista em um vetor.

***Vantagem***

Pode -se facilmente ***alterar*** ou ***determinar*** o valor de um dado.

***Desvantagem***

1. É preciso especificar antecipadamente a dimensão máxima do vetor onde a lista vai ser implementada.

2. Inserções e remoções podem exigir considerável movimentação de dados.
***

#### Definições para Implementação em Pascal

|X1|X2|X3| ... |   
  01  02   03 DIM

   
 ***Descritores da Lista (Definem estado da lista)***
 
 >INF = 01 - **Inicio da Lista**     *Posição do primeiro nó*
 >
 >FIM = 03 - **Fim da Lista**       *Posição do ultimo nó*
 >
 >COR = 00 - **Nó Corrente da Lista**   *Percorre a Lista*
 >
 >NUM = 03 - **Quantidade de Elementos**   *Numero de nós*
 
 
 **DIM**: É a dimensão do vetor onde está a Lista
 
 >- Assim uma Lista (L) é  = Descritores + Nós (informações)
>













 
















