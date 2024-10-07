# Padrões Comportamentais

## Definição 

Os padrões comportamentais são focados em definir como os objetos iteragem e se comunicam entre si dentro de um sistema.

Eles abordam a atribuição de responsabilidades e a maneira como as classes colaboram, permitindo que o comportamento do sistema seja flexível e dinâmico sem a necessidade de modificações profundas no código.

## GoF

Segundo o livro "Design Patterns: Elements of Reusable Object-Oriented Software", os padrões comportamentais "se preocupam com algoritmos e a atribuição de responsabilidades entre objetos... não descrevem apenas padrões de objetos ou classes, mas também o padrão de comunicação entre eles.""

Esses padrões auxiliam a separar a lógica de controle do comportamento real dos objetos, facilitando a extensão e manutenção do código.


# Chain of Responsability

Permite que um pedido passe por uma cadeia de objetos potenciais, onde cada objeto tem a chance de tratar o pedido ou passá-lo adiante.

Isso promove um desacoplamento entre o remetente e os receptores, permitindo que vários objetos possam processar o pedido de forma ordenada e flexível.

# Command

Transforma uma solicitação em um objeto autônomo, qie encapsula toda a informação, necessária para executar uma ação. Isso inclui o próprio pedido, o receptor que o processará e, eventualmente, os parâmetros necessários.

O padrão permite que comandos sejam armazenados, efileirados, desfeitos ou refeitos sem a necessidade de conhecimento os detalhes sobre quem ou como a solicitação será processada.

Esse padrão promove o desaclopamento entre o objeto que faz a solicitação e os objetos que realizam a ação.


# Interpreter

Define uma forma de interpretar ou avaliar a gramática de uma linguagem, representando-a por meio de uma estrutura de classes.
Ele é útil quando você precisa interpretar ou analisar sentanças ou expressões escritas em uma linguagem particular, e cada símbolo ou expressão tem uma regra gramatical associada.

Este padrão é normalmente usado em cenários onde uma linguagem específica, um script ou expressões complexas precisam ser processados repetidamente.

# Problemas


## Primeiro Problema

Desenvolver um sistema de automação
residencial que permite aos usuários controlar
dispositivos, como lâmpadas, cortinas e
sistemas de som, por meio de comandos
emitidos por um controle remoto. 

O sistema precisa ser flexível o suficiente
para permitir que novos dispositivos sejam
adicionados no futuro, sem que o controle
remoto precise ser alterado. Além disso, os
usuários querem ter a capacidade de desfazer
uma ação, como desligar a lâmpada após tê-la
ligado acidentalmente.

**Nesse problema problema o padrão comportamental utilizado para resolver eh o padrão command**

Imagine que estamos desenvolvendo um sistema de
suporte técnico para uma empresa que oferece vários níveis
de atendimento.

## Segundo Problema

Os clientes podem ter problemas de diferentes níveis de
complexidade: simples, intermediários e complexos.

Dependendo da complexidade do problema, ele pode ser
resolvido por um atendente, um técnico de nível 1, 2 ou 3.

**Nesse problema problema o padrão comportamental utilizado para resolver eh o padrão Chain of Responsability**

## Terceiro Problema

Estamos desenvolvendo uma planilha, ela deve
suportar uma gama de expressões matemáticas pré-
definidas, como (somar, subtrair, multiplicar e dividir). 

Os usuários podem inserir expressões matemáticas
no formato de texto, como SOMA(3, 5), e a
calculadora deve interpretar e avaliar a expressão
corretamente.


**Nesse problema problema o padrão comportamental utilizado para resolver eh o padrão Interpreter**

# Iterator

Permite percorrer uma coleção de objetos (como listas, arrays, ou árvores) deforma sequencial, sem expor sua estrutura interna. O padrão separa a lógica de interação da coleção, fornecendo uma interface comum para acessar os elementos um por um, independentemente da implementação da coleção.

O objetivo de Iterator é garantir que diferentes tipos de coleções possam ser percorridos de forma uniforme, oferecedo métodos como next(), hasNext(), e currentItem() para controlar o fluxo de acesso aos elementos.

# Mediator 

Centraliza a comunicação entre objetos, evitando que eles comuniquem diretamente uns com os outros.

Isso promove o desacoplamento entre os objeto, pois, ao invés de se comunicarem diretamente, eles passam a interagir mediante um intermediário, o Mediator.

Esse padrão é útil quando há inúmeras interações complexas entre os objetos, o que poderia tornar o sistema difícial de manter e modificar.

# Memento

Permite capturar e armazenar o estado interno de um objeto em um determinado momento, sem expor os detalhes de sua implementação.

Posteriormente, esse estado pode ser restaurado, permitindo que o objeto volte a uma configuração anterior.

A principal vantagem do Memento é que ele mantém a integridade do encapsulamento do objeeto original, pois o estado armazenado não é exposto diratamente para o cliente ou outros objetos.