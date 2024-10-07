# Guia de Estudo: Arquitetura de Software

## Arquitetura em Camadas

A **arquitetura em camadas** organiza um sistema de software em diferentes camadas, cada uma com uma responsabilidade específica. Esse padrão promove uma clara separação de preocupações e facilita a manutenção e escalabilidade do sistema.

### Camadas Típicas

1. **Camada de Apresentação**:
   - **Responsabilidade**: Interface com o usuário.
   - **Funções**: Exibir informações ao usuário e capturar entradas. Interage com a camada de lógica de negócios para processar dados.

2. **Camada de Lógica de Negócios**:
   - **Responsabilidade**: Implementação das regras de negócio e processamento de dados.
   - **Funções**: Processar dados recebidos da camada de apresentação e realizar operações de negócios. Interage com a camada de acesso a dados para persistência e recuperação de dados.

3. **Camada de Acesso a Dados**:
   - **Responsabilidade**: Manipulação e acesso aos dados.
   - **Funções**: Comunica-se com bancos de dados e outras fontes de dados. Fornece dados para a camada de lógica de negócios e armazena resultados.

4. **Camada de Persistência de Dados** (Opcional):
   - **Responsabilidade**: Gerenciamento de armazenamento de longo prazo.
   - **Funções**: Oferece uma interface para persistir e recuperar dados em um armazenamento persistente.

### Princípios Importantes

- **Separação de Responsabilidades**: Cada camada deve tratar de uma responsabilidade única para evitar dependências e facilitar a manutenção.
- **Interação Entre Camadas**: As camadas devem interagir apenas com as camadas adjacentes para manter a coesão e minimizar o acoplamento.

### Observação

A camada de apresentação não deve acessar diretamente a camada de dados, pois isso violaria o princípio de separação de responsabilidades e acoplamento entre camadas.

## Arquitetura Orientada a Eventos

A **arquitetura orientada a eventos (EDA)** utiliza eventos para comunicar mudanças de estado entre diferentes componentes do sistema. Esta abordagem é eficaz para sistemas que precisam de uma comunicação assíncrona e desacoplada.

### Benefícios

- **Escalabilidade**: Permite que o sistema se ajuste dinamicamente à carga de trabalho, escalando componentes de forma independente.
- **Desacoplamento**: Os componentes são desacoplados e interagem através de eventos, facilitando a adição e remoção de funcionalidades.
- **Resiliência**: A falha de um componente não afeta diretamente outros, aumentando a robustez do sistema.

### Características

- **Processamento Assíncrono**: Os eventos são processados de forma assíncrona, permitindo que o sistema continue funcionando enquanto os eventos são tratados.
- **Modelo de Pagamento por Uso**: Muitos sistemas baseados em EDA adotam um modelo de pagamento baseado no uso, que pode reduzir custos.

### Considerações

A arquitetura orientada a eventos não elimina a necessidade de servidores físicos e não implica processamento apenas em dispositivos do cliente.

## Padrão de Plugins

O **padrão de plugins** é uma abordagem que permite adicionar novas funcionalidades ao sistema sem alterar seu núcleo. Essa abordagem promove modularidade e flexibilidade.

### Benefícios

- **Extensibilidade**: Novas funcionalidades podem ser adicionadas através de módulos externos que são integrados dinamicamente ao sistema.
- **Desacoplamento**: Plugins são módulos independentes que interagem com o núcleo do sistema através de interfaces bem definidas.
- **Facilidade de Manutenção**: Permite que atualizações e modificações sejam feitas em plugins individuais sem impactar o núcleo do sistema.

### Funcionamento

- **Modularidade**: Funcionalidades são implementadas como plugins, que podem ser adicionados ou removidos conforme necessário.
- **Carregamento Dinâmico**: Plugins são carregados dinamicamente em tempo de execução, o que facilita a extensão e personalização do sistema sem precisar reinicializar o núcleo.

## Arquitetura Serverless

A **arquitetura serverless** é um estilo arquitetural onde a gestão da infraestrutura é abstraída, e os desenvolvedores focam apenas no código e na lógica de negócios. O provedor de serviços lida com a execução e escalabilidade do código.

### Benefícios

- **Escalabilidade Automática**: Adapta-se automaticamente à carga de trabalho sem intervenção manual.
- **Modelo de Pagamento por Uso**: Os custos são baseados no uso real dos recursos, o que pode reduzir despesas.
- **Redução de Overhead de Infraestrutura**: O provedor gerencia a infraestrutura, permitindo que os desenvolvedores se concentrem no desenvolvimento de funcionalidades.

### Considerações

- **Controle da Infraestrutura**: Os desenvolvedores não têm controle direto sobre a infraestrutura subjacente.
- **Dependência de Rede**: Aplicações serverless dependem fortemente da conectividade com a rede.

## Estilos Arquiteturais vs. Padrões Arquiteturais

### Estilos Arquiteturais

- **Definição**: Estilos arquiteturais são abordagens gerais para estruturar um sistema, fornecendo uma visão global da organização e interação dos componentes. Eles definem a forma como diferentes componentes e suas interações são estruturados para atender a requisitos específicos.
- **Exemplos**: Arquitetura em camadas, arquitetura orientada a eventos, microserviços.
- **Objetivo**: Definem a organização e a abordagem global para a construção e interação dos componentes do sistema.

### Padrões Arquiteturais

- **Definição**: Padrões arquiteturais são soluções reutilizáveis e melhores práticas para problemas recorrentes dentro de um estilo arquitetural. Eles fornecem diretrizes e soluções específicas para implementar aspectos detalhados de um estilo arquitetural.
- **Exemplos**: Padrão de plugins, padrão de repositório, padrão de fachada.
- **Objetivo**: Fornecem soluções específicas e diretrizes para implementar e resolver problemas comuns dentro do contexto de um estilo arquitetural.

### Diferença Principal

- **Escopo**: Estilos arquiteturais são amplos e definem a estrutura geral do sistema, enquanto padrões arquiteturais são mais específicos e focam em soluções detalhadas dentro do escopo de um estilo arquitetural.
- **Nível de Abstração**: Estilos arquiteturais fornecem uma visão macro da organização do sistema, enquanto padrões arquiteturais fornecem uma visão micro com soluções e melhores práticas para problemas específicos.

## Estudo de Caso: Microserviços

Os **microserviços** são um estilo arquitetural onde um sistema é dividido em serviços pequenos e independentes que comunicam-se entre si. Sam Newman destaca que os principais benefícios são:

- **Independência dos Times**: Times podem trabalhar de forma independente em diferentes serviços.
- **Escalabilidade**: Serviços individuais podem ser escalados de forma independente conforme necessário.

---
# Estudo para Prova de Design Patterns

## 1. **Padrões de Projeto**

**Padrões de Projeto** são soluções comprovadas que promovem a reutilização de código, facilitam a manutenção e a comunicação entre desenvolvedores, além de melhorar a escalabilidade e a flexibilidade dos sistemas.

### **Principais Benefícios**:
- **Manutenção**: Evita a necessidade de "reinventar a roda".
- **Comunicação**: Conceitos complexos são identificados por nomes simples (ex.: Singleton, Factory).
  
## 2. **Padrão Singleton**

### **Problema**: Garantir que apenas uma instância de um objeto exista e seja acessível globalmente no sistema.

### **Aplicação**:
- Controla o acesso a recursos críticos (ex.: arquivo de configuração).
- Exemplo: Garantir que apenas um usuário autenticado por vez acesse o recurso crítico de um sistema.

### **Vantagens**:
- Mantém a consistência dos dados.
- Evita problemas de concorrência.
  
## 3. **Padrão Builder**

### **Problema**: Criação de objetos complexos com múltiplas etapas.

### **Benefícios**:
- Separação do processo de construção e a representação de um objeto.
- Permite criar diferentes representações de um objeto.

### **Aplicação**:
- Útil para objetos com muitos parâmetros opcionais ou processos de construção complexos.

### **Exemplo de Aplicação**:
- Um construtor pode ser utilizado para criar um mesmo objeto de várias formas, dependendo dos parâmetros.

## 4. **Padrão Facade**

### **Problema**: Sistemas complexos com muitas interações internas difíceis de controlar.

### **Solução**: Fornece uma interface simplificada para um conjunto de classes complexas, ocultando a complexidade interna.

### **Benefícios**:
- Facilita o uso de sistemas complexos.
- Reduz a dependência do código em subsistemas complexos.

### **Exemplo de Aplicação**:
- Um Facade pode ser usado para fornecer um ponto de acesso simples para bibliotecas ou subsistemas complexos.

## 5. **Padrão Adapter**

### **Problema**: Integração de sistemas ou classes com interfaces incompatíveis.

### **Solução**: Converte a interface de uma classe em uma interface que um cliente espera, facilitando a integração.

### **Benefícios**:
- Permite que sistemas legados se conectem a novos sistemas.
- Tradução de chamadas feitas pelos clientes para interfaces incompatíveis.

### **Exemplo de Aplicação**:
- Permitir que um sistema antigo se comunique com um novo sistema sem modificar o código original.

## 6. **Padrões Estruturais**

### **Objetivo**: Resolver problemas relacionados à composição de classes e objetos, formando estruturas maiores e mais flexíveis.

### **Principais Benefícios**:
- **Flexibilidade na Composição**: Permite organizar classes de forma mais flexível.
- **Manutenção e Extensão**: Facilita a manutenção e extensão do sistema.
- **Simplificação da Complexidade**: Simplifica a estrutura do sistema.

### **Exemplo de Aplicação**:
- O padrão **Flyweight** é um exemplo de padrão estrutural que otimiza o uso de memória ao compartilhar objetos entre contextos semelhantes.

---

## Questões para Estudo

1. **Qual o objetivo do padrão Singleton?**
   - Garantir que apenas uma instância de um objeto seja criada e compartilhada por todo o sistema.

2. **Quando utilizar o padrão Builder?**
   - Quando a criação de objetos envolve muitos parâmetros opcionais ou etapas de construção complexas.

3. **Como o padrão Facade auxilia no desenvolvimento de sistemas?**
   - Ele simplifica a interface de um subsistema complexo, facilitando o uso e manutenção.

4. **Qual o papel do padrão Adapter?**
   - Adaptar uma interface incompatível para que dois sistemas possam se comunicar.

5. **Quais os principais benefícios dos padrões estruturais?**
   - Flexibilidade na composição, simplificação da complexidade e melhoria na manutenção/extensão do sistema.
