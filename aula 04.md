# Design Patterns

Padrões estruturais

## Padrão estrutural

São descritas como soluções para problemas relacionados à composição de classes e objets para formar estruturas maiores e mais flexíveis.

Esses padrões ajudam a organizar e otimizar o design de sistemas de software. facilitando como os componentes interagem e se conectam.

### Principais benefícios;

- Flexibilidade na composição de objetos
- Desacomplamento
- Manuteção e extensão
- Simplificação de complexidade

### "Strucutral patterns deal with object composition, creatgin relations between objects to from larger structures. These patterns help ensure that if one part of a system changes, the entire system does not need to change simplify the design by decoupling components, making the system more flexible and easier to maintain" - Gamma et al., 1995

## Adapter

Permite que interfaces incompatíveis trabalhem juntas. Ele converte a interface de uma classe em outra intreface esperada pelos clientes.

Assim, o Adapter atua como um intermediário que traduz as chamadas feitas pelo cliente para a interface da classe que não é compatível.

**Usado quando** é necessário integrar sistemas legados com novos sistemas ou quando se deseja adaptar uma API para uma nova interface.

**Esse design resolve esse problema:** Imagine que você está fazendo um intercambio
para o Reino Unido, chegando lá com seu laptop,
você descobre que o padrão de tomada é
diferente. 


Seu carregador foi projetado para funcionar com
uma tomada de dois pinos (padrão BR), mas lá são
utilizadas tomadas de três pinos (padrão UK). 

Para resolver esse problema sem a necessidade de
modificar o design do carregador ou da tomada,
você pode usar um adaptador de tomada que faz a
conversão entre esses dois padrões.


## Bridge

Desacopla uma abstração da sua implementação, permitindo que ambas evoluam independentemente.

**É usado** quando você quer seperar uma abstração (a ideia principal ou conceito) de sua implementação concreta (a forma como o conceito é realizado). Isso é útil para evitar que mudanças em uma parte da estrutura (como uma classe) causem impacto na outra parte.

## Composite

Permite que você trate objetos individuais e composições de objetos de forma uniforme.

Isso é útil quando você tem uma estrutura hierárquica de objetos, como uma árvore, onde cada nó pode ser um objeto simples ou um grupo de objetos.

**Usado quando** precisar representar hierarquias de objetos, como estruturas de diretórios de arquivos ou interfaces gráficas complexas.

**Esse design pattern resolve esse problema:**

- Desejamos criar um sistema que precisa lidar com a estrutura de um sistema de arquivos, onde há pastas que podem conter arquivos e outras pastas.

Cada pasta pode ter um número arbitrário de subpastas e
arquivos, mas tanto os arquivos quanto as pastas podem ser
tratados como "componentes" do sistema de arquivos,
permitindo operações como exibir o conteúdo ou calcular o
tamanho total.

## Decorator

Permite adicionar resposabilidade a um objeto dinamicamente, sem alterar o código da classe original. Ele usa um conjunto de classes de decoração que envolvem o objeto original, adicionado funcionalidades adicionais. **Utilizado** para adicionar funcionalidades a objetos de maneira flexível e extensível, como adicionar estilos de janela em um sistema de GUI.

## FACADE

Fornece uma interface simplificada para um conjunto de interfaces em um subsistema complexo. Em outras palavras, o Facade **atua como** uma "fachada" oculta a complexidade de um sistema, oferecendo uma maneira mais fácil e direta para os clientes interagirem com ele.

## FLYWEIGTH

Visa reduzir o uso de memória e melhorar o desempenho ao compartilhar objetos semlhantes em vez de criar novos objetos para cada instância.

Ele é especialmente útil quando você precisa lidar com excesso de objetos que possuem características semelhantes.

## PROXY

Fornece um substituto ou intermediário para outro objeto. Ele age como um "representante" do objeto real, controlado o acesso a ele e podendo adicionar funcionalidades extras, como controle de acesso, atraso na criação ou manipulação adicional.

**Usando para** adicionar funcionalidades como controle de acesso, cache, ou outras operções intermediárias.
