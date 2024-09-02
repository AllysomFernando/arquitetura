# Estilos Arquiteturas

## O que é arquitetura?

Arquitetura é basicamente a organização dos códigos. Estruturas de estruturas.

### Beneficios
 - Criar uma boa arquitetura para postegar uma decisão importante
## O que é design?

Design na parte do código é a -- verificar

-- **verificar o que é um padrão arquitetural**
# Estilos arquiteturais

São abordagens de design amplas, descrevem uma estrutura de alto nível para organizar os componentes. Elas guiam o desenvolvimento e a evolução do nosso sistema.

- Estrutura Global
- Componentes e conexões 
- Escopo amplo

## Beneficios
- Reutilização
  - Permite a reutilização de soluções testadas. Aumentando a eficiencia do desenvolvimento.

- Compreensão e Comunicação
    - Eles fornecem uma linguagem comum para descrever e discuitra a arquitetura. Facilitando a comprensão.

- Flexibilidade e Escalabilidade
    - A aplicação de estilos arquiteturais pode resultar em sistemas que são mais faceis de enteder, modificar e escalar.

- Padronização
    - Ajudam a padronizar o desenvolvimento de software em uma organização.

- Facilidade de manutenção
    - Quando bem definidos, podem facilitar a manutenção e a evoluação do sistema. Pois aplicando as regras facilita a manutenção.


# Client-Server

Paradigmas que distrubuem do servidor e client side. Ex: internet

- Thin Client vs. Fat Client
    - Em um modelo de thin client, a maior parte do proessamento e armazenamento é feita no servidor, com o cliente focando na interface.
        - Thin client é quando o front serve para apenas exibir os dados.
        - Fat client é quando o front está fazendo a parte lógica tambem, não deixando apenas para o servidor fazer essas partes mais "pesadas".
- Contextos de aplicação
    - Aplicação web e sistemas de banco de dados

Contexto logico deixando apenas para o servidor e a UI/UX para o usuário carregar.

Normalmente combinando com outros estilos arquiteturas, Componentes-based, layred e utilizando em padrões arquiteturais MVC. Quem diz que é implementado são os padrões aquiteturais

## Principais problemas

- Falha no servidor
- Somente o servidor sendo o dentetor das informações.

# Component-based

Sendo uma modularização da aplicações. Quebrando o código tendo varios modulos provendo uma necessidade especificas. Sendo aplicado no back e no front

## Principais beneficios

- Reutilização
    - Componentes bem definidos podem ser reutilizados em diferentes sistemas. Reduzindo o tempo de desenvolvimento e os custos.
- Facilidade de Manutenção
    - A modularização facilita a manutenção do código.
- Facilidade de migração de monolito para microserviços

## Exemplos de Componente-based
- Sistema de gestão empresarial (ERP)
- PLataforma de comercio eletrônico
- Sistema de gerencimento de conteudo
- Componentes em aplição web

### Monolito modular

- O monolito modular é o meio termo de microserviços e monolito, pois você modulando as "regras do monolitos" quando está escalando muito você pode fazer um microserviço. Facilitando a transformações quando vai crescendo a nossa aplicação. Facilitando a criação e o deploy. No inicio do projeto os times ainda estão aprendendo das regras de negocio. Aplicando o monolito modular deixa mais facil a transformação em microserviços

# Layred & N-tiers

## Layred
- é uma aboragem onde o sistema é organizado em camdas, cada uma com responsibilidade específicas e interações bem definidas.
    - Descvre a arquiterua em camadas com um padrão estrutural comum em aplições empresarias, dividindo a aplicação em camadas como apresentação, aplicação, domínio e infraestrutura. Um exemplo como **Presentation layer**, **Domain Layer** e **Data Source layer**. Um padrão arquitetural que aplica isso é o MVC.
- EM resumo, vai possuir uma interação com usuário, seja ela qual for, vai ser possuir um dominio e vai ter uma camada de acesso a dados.


### Qual é a divisão que o estilo arquitetural layred nos propoem
Ela nos propoem uma divisão lógica, porem a nossa tiers são separação físicas

## N-tiers
- Refere-se à separação fisica das diferentas camadas da aplicação, onde cada nível pode ser distribuido em diferentes maquinas ou servidores. Esse estilo é focado na distruição e escalabilidade do sistema
- A separação física permite que cada nível seja escalado de forma independente, aumentando a capacidade do sistema de lidar com uma maior carga de trabalho.

# Diferenças Tier & Layer
Em discussões de arquitetura de três camadas(tier), o nível é frequentemente usado de forma intercambiável e equivocadamente pela camada, como um 'nível de apresentação' ou 'nível lógico de negócios'. Não são o mesmo!

### Tier(Nivel)

- Refere-se normalmente a uma divisão física do software executada em uma infraestrutura separada das outras divisões

### Layer(Camada)
- Se refere a uma divisão lógica da sua aplicação, sendo normalmente executada em uma única infra e processos distintos. 

# Exemplo:
![Exemplo](https://media.canva.com/v2/image-resize/format:JPG/height:473/quality:92/uri:s3%3A%2F%2Fmedia-private.canva.com%2FhB8TM%2FMAGLnahB8TM%2F1%2Fp.jpg/watermark:F/width:625?csig=AAAAAAAAAAAAAAAAAAAAAGyYEw56NKEEqqruq_ECacB3NHhgYAs5lQq26bAg08Yw&exp=1722915979&osig=AAAAAAAAAAAAAAAAAAAAAMFz-RHZOO5Ktp7dQqO9Udf0UjFcowLqKBt0cVhvLa4A&signer=media-rpc&x-canva-quality=screen)

# Event-driven architeture

- É um estilo arquitetural em que os componentes do sistema através da geração e manipulação de eventso. Tendo um cara que cria um evento e outros que consomem.
- Event procucers (Publicadores)
    - Geram e emitem eventos.
- Event consumer (Assinantes)
    - Recebem e processam eventos.
- Event channel (Broker de mensagens)
    - Middleware que gerencia a distrubuição de eventos dos publicadores para os assinatantes.
- Event procesors
    - Componentes que processam eventos e podem gerar novos eventos.

## Exemplos:
 - Quando você espera algo, pode ou não acontecer. Aconteceu algo no sistema várias outras coisas devem ser notificadas.
 - Uma arquitetura orientadas a eventos

Essa arquitetura ela depende de um serviço de mensageria, para notificar todos os microserviços escutando os topico da requisição. 

# Microkernel

Estilo arquitetural que busca manter o núcleo do sistema a mais simples e reduzido possiível, delegando a maioria das funcionalidades para módulos ou serviços externos adiconados ao núcleo.

## Características

- Núcleo mínimo
    - Apenas as funcionlaidades essenciais.
- Serviços e módulos
    - Funcionalidades adicionais
- Comunicação 
    - Normalmente feita por meio de chamdaas de sistemas ou mensagems

