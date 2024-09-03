# Desing Patterns

## O que são padrões de projetos?

Design Patterns (ou padrões de projeto) são soluções típicas para problemas recorrentes no desenvolvimento de software. Eles
representam boas práticas adotadas por desenvolvedores
experientes e foram criados para facilitar a manutenção,
escalabilidade e a clareza do código.

### Cair na prova

São soluções típicas para problemas recorrentes

### Padrões segundo Alexander

Um padrão é uma regra de três partes, que
expressa uma relação entre um determinado contexto.

## Beneficios

- Reutilização de código.

  - um padrão é uma regra de três partes, que
    expressa uma relação entre um determinado contexto

- Manutenção

  - O uso de padrões facilita a
    manutenção do código, pois as
    soluções são reconhecíveis e
    compreendidas por
    desenvolvedores familiarizados
    com os padrões.

- Comunicação

  - Ao usar design patterns,
    desenvolvedores podem se
    comunicar de maneira mais
    eficiente, referindo-se a uma
    solução complexa com um
    nome simples e amplamente
    compreendido, como "Factory
    Method" ou "Observer".

- Escalabilidade e
  flexibilidade - Ajudam a criar sistemas
  facilmente estendidos ou
  modificados à medida que
  novos requisitos surgem.

## Onde não utilizar?

- Complexidade desnecessária
  - Aplicar um pattern em um problema que pode ser resolvido com uma solução mais simples pode adicionar complexidade desnecessária ao código
- Problemas mal definidos
  - Não tente forçar um padrão em um problema que não é claramente compreendido. Primeiro, compreenda completamente o problema antes de buscar uma solução padrão.
- Overengineering
  - Evite overengineering, que é a tendência de criar uma solução mais complexa do que o necessário, por aplicar padrões de design onde não são necessários. Quando você aplica uma solução muito complexa em algo simples.

## Três categorias de Patterns

- Criacionais

  - Tratam do processo de
    criação de objetos,
    promovendo a flexibilidade e
    a reutilização de código.

- Estruturais

  - Lidam com a composição
    de classes ou objetos,
    formando estruturas
    maiores de forma
    eficiente.

- Comportamentais - Lidam com a
  comunicação entre os
  objetos e com a maneira
  como eles interagem e
  suas responsabilidades.

# Padrões

## Singleton

É um padrão de design criacional que garante que uma classe tenha apenas uma única
instância e fornece um ponto global de acesso a essa instância.

## Onde ele é util

Ele é útil em situações onde é importante que apenas um objeto de uma classe seja criado,
como em gerenciadores de recursos, conexões de banco de dados ou configurações globais
de uma aplicação.

## Caracteristicas

- Única instância - Apenas uma instância da classe é
  criada durante o ciclo de vida da aplicação.
- Controle de acesso - A classe controla como e
  quando sua única instância é criada
- Ponto de acesso global - Fornece uma forma global
  de acessar essa instância única

## Abstract Factory

Padrão que permite criar famílias de objetos relacionados ou dependentes sem especificar
suas classes concretas.

## O que ele define?

Ele define uma interface para criar diferentes tipos de objetos (como botões e checkboxes),
permitindo que o cliente trabalhe com essas famílias de objetos de forma independente de
suas implementações específicas.

## Caracteristicas

- Criação de familias de objetos - Permite criar grupos de
  objetos relacionados que devem ser usados juntos.
- Independência de implementação - O cliente usa
  interfaces abstratas, sem saber quais classes
  concretas estão sendo instanciadas
- Flexibilidade - Facilita a troca entre diferentes famílias
  de objetos, como mudar a interface do usuário de
  Windows para macOS sem alterar o código cliente

## Prototype

Permite criar novos objetos copiando instâncias existentes (protótipos), ao invés de
instanciar novos objetos do zero.

## Onde ele é util?

Ele é útil quando a criação direta de um objeto é cara (em termos de tempo ou recursos) ou
quando você deseja evitar subclasses para criar diferentes instâncias.

## Caracteristicas

- Clonagem:

  - Cria novos objetos copiando
    (clonando) instâncias existentes, sem depender de
    classes concretas.

- Flexibilidade: - Permite criar objetos complexos com uma
  configuração inicial específica, evitando a repetição de
  código ou configurações

- Idependencia de implementação - Você pode criar
  novos objetos sem depender de suas classes concretas,
  utilizando cópias de protótipos existentes.

## Builder

Permite a construção de objetos complexos passo a passo. Ele separa o processo de
construção do objeto da sua representação, permitindo criar diferentes representações do
mesmo objeto.

## Caracteristicas

- Construção passo a passo
  - Permitindo criar objetos complexos em etapas, adicionando um nivel de controle sobre o processo de construção
- Seperação de precupações
  - Separa a lógica de construção do objeto (builder) de sua representação final, permitindo que o mesmo processo construa diferentes tipos de objetos
- Flexibilidade  
   - Facilita a criação de objetos com
  configurações variadas sem precisar de múltiplos
  construtores ou parâmetros opcionais.

# Problemas

Imagine que você está desenvolvendo um sistema de cassino online,
onde é necessário acessar um recurso de log centralizado para
registrar todas as operações críticas, como transações, apostas e
excpetions.

Esse recurso de log deve ser único e globalmente acessível para
garantir que todos os registros sejam armazenados de forma
consistente e que não haja múltiplas instâncias concorrendo pelos
recursos do sistema, o que poderia resultar em dados inconsistentes.

### **O padrão vai ser utilizado vai ser o Singleton**


### Segundo Problema

Imagine que você está desenvolvendo uma aplicação de interface
gráfica que precisa suportar diferentes temas visuais, como um tema
claro e um tema escuro. Cada tema possui seu próprio conjunto de
componentes de interface, como botões, caixas de texto e janelas, que
precisam ser estilizados de acordo com o tema selecionado.



Se você implementar a criação desses componentes diretamente no
código da interface, isso resultará em um código altamente acoplado,
difícil de manter e estender. Além disso, a mudança de tema se tornaria
uma tarefa complexa, pois exigiria modificações em várias partes do
código.

### **O padrão vai ser utilizado vai ser o Abstract Method**

### Terceiro Problema

Imagine que você está desenvolvendo um sistema de notificação para
uma aplicação que precisa enviar diferentes tipos de notificações para
os usuários, como e-mail, SMS e notificações push. Cada tipo de
notificação tem uma lógica de envio diferente e requer diferentes
configurações.



Se você implementasse a criação dessas notificações diretamente na
lógica do sistema, o código se tornaria rígido e difícil de manter,
especialmente quando novos tipos de notificações precisarem ser
adicionados. Além disso, a criação das instâncias estaria acoplada à
lógica da aplicação, o que não é ideal.

### **O padrão vai ser utilizado vai ser o Factory Method**
