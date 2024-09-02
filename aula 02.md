# Microserviços

## O que é microserviços

É um estilo arquitetural que estrutura uma aplicação como um conjunto de pequenos
serviços independentes, cada um executando um processo único e comunicando-se
por meio de APIs bem definidas. Cada microserviço é desenvolvido, implantado e
escalado de forma independente, permitindo uma maior flexibilidade e agilidade no
desenvolvimento e na manutenção de software.
Os serviços são individuais. 

Tendo um API Gateway recebe todas as request em um URL e faz um proxy para o serviço especifico. Exemplo: tendo um Kong, sendo um endnest servindo como loadbalencer.

Para resolver um dos problemas de balanceamento de garga usasse um loadbalancer como o Kong.

Para fazer a conversão de um monolito e fazer a conversão para microserviçøs usamos um loadbalancer com 10% das reqs indo para o monolito e os outros 90% para o monolitos

Para utilizar microservices você usa dockers. Criando varias imagens e subir com a ajuda de um kubernets.

* Resposta da prova: escalabilidade e autonomia de times

### Como resolver o problema de muitos requests?
Serviços de mensagerias, conectando os microserviçøs

## Caracteristicas

- Desenvolvimento independente
- Desenvolvimento poliglota
- Desempenho e escalabilidade
- Descentralização

## Problemas (ou trade-offs)

- Sincronização de dados
- Complexidade do gerenciamento
- Redundacia de dados
- Problema de volta de dados
- Muitas URLs para fazer requisição 
- Latência na comunicação entre microserviços
- Consistência de dados
- Custos operacionais e segurança

# Clean Arch

Este estilo de arquitetura enfatiza a separação de preocupações
e a independência dos frameworks, interfaces de usuário, bancos
de dados e outros detalhes externos. Podemos considerar como
um avanço da onion architeture.

- Resposta da prova: Ter um nucleo de regra de negocio intacta e interface para lidar com o resto

## Caracteristicas 
- Independencias entre as camadas
- Liberdade de troca de linguagens
- Separação das responsabildiades
- Regras de negocios isoladas de frameworks


# Problemas

- Dependencia de modulos
- Lmites confusos
- Dificuldades na manutenção
- Dependencia na base de dados

# Hexagonal-Ports and Adapters

Foi proposta por Alistair Cockburn, visa criar sistemas de software que sejam altamente desacoplados e testáveis, permitindo que as partes centrais da aplicação permaneçam independentes de suas interfaces de entrada e saída.

- Resposta da prova: Ter um nucleo de regra de negocio intacta e interface para lidar com o resto

## Caracteristicas

- Sempre havera portas e adaptadores
- A comunicação do domain serão as portas e adaptadores

as duas arquiteturas resumem a terem uma regra de negocio intacta e terem interfaces para resolver as outras partes.

# Serveless

Arquitetura serverless é um modelo de computação em nuvem onde os provedores
de nuvem gerenciam a execução do código, alocando dinamicamente os recursos
necessários. 

Esse modelo permite que os desenvolvedores se concentrem mais na lógica de
negócios e menos na infraestrutura, uma vez que tudo isso é responsabilidade do
provedor de serviços de nuvem.

## Caracteristicas

- Execução sob demanda, escabilidade automática
- Custo-eficiencia, gerenciamento simplificado

### Funções como serviço (FaaS)

- AWS Lambda, Google Cloud Functions, e Azure Functions

### Backend como serviço (BaaS)

- Firebase Authentication, Firestore e Amazon S3
 
# Padroes arquitetural

São soluções recorrentes para problemas específicos de design em um contexto
arquitetural. Eles são mais específicos que estilos arquiteturais e fornecem detalhes
sobre a implementação.
Dizem como vamos utilizar no nosso codigo 

## Caracteristicas

- Solucionam problemas específicos
- Guias de implementação
- Reutilização de soluções

### Exemplos

- MVC - Model, View e Controller
  - Model 
    - Representa os dados e a lógica de negócios.
    - Gerencia o comportamento e os dados da aplicação.
  - View
    - Apresenta os dados ao usuário.
  - Controller
    - Recebe a entrada do usuário.
    - Interage com o modelo e seleciona a visão para apresentar a saída.
- Beneficios: 
     - Separação de preocupações: Facilita a manutenção e a escalabilidade.
     - Reutilização de código: Componentes podem ser reutilizados em diferentes partes da aplicação.

- Plug-ins
    - Núcleo e plug-ins ou extensões que adicionam funcionalidades. O núcleo fornece a
base e a infraestrutura, enquanto os plug-ins fornecem funcionalidades específicas.
    - Alguns locais citam como estilo arquitetural, porém partilho da visão de que ela
como solução não possui "tamanho" suficiente para ser um estilo completo, se
enquadrando como padrão que pode ser composto em estilos arquiteturais como
o Layered e Componend-based.


- Microkernell