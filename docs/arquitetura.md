# Documento de Arquitetura de Software 

Este documento tem como objetivo descrever a arquitetura do software do projeto da ONG Animal, que tem como objetivo ajudar animais em situação de risco. A aplicação web permitirá que as organizações cadastrem animais que precisam de ajuda, gerenciem doações online, divulguem informações sobre os animais e suas atividades, além de permitir que usuários se candidatem a adotar animais e se candidatem a ser voluntários para ajudar na causa.

## Visão Geral da Arquitetura 

A arquitetura do software é baseada em um modelo de três camadas, que separa a interface do usuário, a lógica de negócios e o acesso a dados. A camada de interface do usuário é responsável pela interação com o usuário e exibição de informações na tela. A camada de lógica de negócios é responsável por implementar as regras de negócios, processar dados e executar operações. A camada de acesso a dados é responsável por interagir com o banco de dados e recuperar ou persistir dados.

O projeto será desenvolvido utilizando o framework React para a camada de interface do usuário e o Node.js para a camada de lógica de negócios. Para o banco de dados, será utilizado o PostgresSQL, gerenciado pelo Prisma ORM. O servidor será implantado na nuvem, usando serviços como o Heroku ou AWS.

## Camada de Interface do Usuário

A camada de interface do usuário será responsável por interagir com o usuário e exibir informações na tela. O React será utilizado para criar componentes reutilizáveis e responsivos, proporcionando uma experiência do usuário intuitiva e agradável.

Serão utilizados os princípios do design responsivo para garantir que a aplicação funcione em vários dispositivos e tamanhos de tela. Também será utilizada a biblioteca Material-UI para o estilo dos componentes.

## Camada de Lógica de Negócios

A aplicação será dividida em módulos, que terão responsabilidades distintas, como a gestão de animais, doações, voluntários, etc. Serão criados controladores e middlewares para cada módulo, responsáveis por executar as operações e validar os dados. A autenticação e autorização serão implementadas usando o JWT (JSON Web Token).

## Camada de Acesso a Dados

A camada de acesso a dados será responsável por interagir com o banco de dados e recuperar ou persistir dados. Será utilizado o Prisma ORM para mapear os modelos de dados e fornecer uma interface intuitiva e segura para interagir com o banco de dados.

O Prisma ORM permite definir modelos de dados usando a linguagem Prisma Schema e realizar operações CRUD usando o Prisma Client. Além disso, o Prisma fornece a integração com várias opções de banco de dados, incluindo PostgreSQL, MySQL e SQLite. Como o projeto tem a necessidade de armazenar informações sensíveis, como histórico médico dos animais, é importante escolher um banco de dados que ofereça segurança e escalabilidade. O PostgreSQL é uma excelente escolha nesse caso, pois oferece recursos avançados de segurança, como criptografia e autenticação de usuários, além de suportar operações de grande escala e ter uma comunidade de usuários ativa e próspera.

## Servidor 

A escolha do servidor web depende das necessidades do projeto. Para um projeto em escala média, o Node.js é uma opção popular devido à sua capacidade de lidar com solicitações em tempo real e de escalar facilmente. O uso de um servidor de aplicativos como o Nginx pode melhorar a performance e a segurança, agindo como um proxy reverso e fornecendo balanceamento de carga.

Por fim, a integração contínua e a entrega contínua são essenciais para garantir a qualidade e a estabilidade do projeto. O uso de ferramentas como Github Actions, Jenkins, Travis CI ou CircleCI para automatizar a compilação, teste e implantação do aplicativo ajudará a garantir que os problemas sejam detectados e corrigidos rapidamente.


