# Documento de Requisitos de Software

Este documento de requisitos tem como objetivo listar as funcionalidades e requisitos não funcionais para a criação de uma aplicação para ONGs de proteção aos animais. 

Para a organização dos requisitos, foi utilizada uma convenção de nomenclatura que segue o formato RFXYYY, onde "RF" significa "requisito funcional", "RNF" significa "requisito não funcional", "X" é a letra correspondente ao tipo de requisito, "A" para "animal", "D" para "doações e voluntariado" e "C" para "comunicação e divulgação", e "YYY" é o número sequencial do requisito. Cada requisito está acompanhado de suas respectivas entradas e pré-condições, saídas e pós-condições para facilitar a compreensão e implementação. 

*Este documento é destinado para equipe de desenvolvimento da aplicação.*

## Requisitos Funcionais

Os requisitos funcionais descrevem as funcionalidades que a aplicação deve ter para atender às necessidades dos usuários e da ONG.

<details>  
  <summary>Cadastro e busca de animais </summary>

| |[RFA001 - Cadastro de animais] |
| - | - | 
| Descrição| A aplicação deve permitir que a ONG cadastre os animais que ela está ajudando, incluindo informações como nome, idade, sexo, raça, fotos, histórico médico e outras informações relevantes.| 
| Entradas| Nome, idade, sexo, raça, fotos, histórico médico e outras informações relevantes. |
| Pré-condições| A ONG deve estar logada na aplicação |
| Saída| Confirmação do cadastro do animal na base de dados da ONG | 


| |[RFA002 - Busca de animais] |
| - | - | 
| Descrição| A aplicação deve permitir que os usuários possam buscar animais por diferentes critérios, como localização, raça, idade, sexo, entre outros.| 
| Entradas| Critérios de busca, como localização, raça, idade, sexo, entre outros. |
| Pré-condições|  |
| Saída| Lista de animais correspondentes aos critérios de busca. | 

| |[RFA003 - Adoção de animais] |
| - | - | 
| Descrição| A aplicação deve permitir que os usuários possam se candidatar a adotar um animal e que a ONG possa gerenciar essas solicitações.| 
| Entradas| Dados do usuário e do animal desejado. |
| Pré-condições| A ONG deve ter aprovado o cadastro do animal. [RFA001] |
| Saída| Confirmação do interesse na adoção e notificação à ONG. | 

| |[RFA004 - Mapa de animais] |
| - | - | 
| Descrição| A aplicação deve permitir que os usuários possam visualizar os animais em um mapa, mostrando a localização dos animais que precisam de ajuda.| 
| Entradas| Dados sobre o estado de saúde e bem-estar dos animais. |
| Pré-condições| A ONG deve estar logada na aplicação. |
| Saída| Atualização das informações na base de dados da ONG. | 

| |[RFA005 - Monitoramento de animais] |
| - | - | 
| Descrição| A aplicação deve permitir que a ONG possa monitorar o estado de saúde e bem-estar dos animais que estão sendo ajudados, para garantir que eles estejam recebendo a assistência adequada.| 
| Entradas| Dados sobre o estado de saúde e bem-estar dos animais. |
| Pré-condições| A ONG deve estar logada na aplicação. |
| Saída| Atualização das informações na base de dados da ONG. | 
  
</details>

<details>
<summary>Doaçoes e voluntariado  </summary>

| |[RFD001 - Doações online] |
| - | - | 
| Descrição| A aplicação deve permitir que as pessoas possam fazer doações online para ajudar a ONG e os animais que ela está ajudando.| 
| Entradas| Informações de doação, como valor e forma de pagamento. |
| Pré-condições|  |
| Saída| Confirmação da doação e recibo eletrônico. | 

| |[RFV002 - Voluntariado] |
| - | - | 
| Descrição| A aplicação deve permitir que as pessoas possam se candidatar a ser voluntários da ONG, oferecendo seus serviços e habilidades para ajudar os animais. |
| Entradas | Dados do usuário e informações sobre as habilidades e serviços oferecidos. |
| Pré-condições|  |
| Saída| Confirmação do interesse em ser voluntário e notificação à ONG. | 

</details>

<details>
<summary> Comunicação e divulgação </summary>


| |[RFC001 - Comunicação] |
| - | - | 
| Descrição| A aplicação deve permitir que a ONG possa se comunicar com os usuários, divulgando informações sobre os animais e as atividades da organização. |
| Entradas | Informações sobre animais e atividades da ONG. |
| Pré-condições| A ONG deve estar logada na aplicação. |
| Saída| Publicação das informações na aplicação. | 

| |[RFC002 - Compartilhamento nas redes sociais] |
| - | - | 
| Descrição| A aplicação deve permitir que os usuários possam compartilhar informações sobre os animais nas redes sociais, como Facebook, Instagram e Twitter, para ajudar a divulgar os animais que precisam de ajuda. |
| Entradas | Informações sobre animais e atividades da ONG. |
| Pré-condições|  |
| Saída| Publicação das informações nas redes sociais selecionadas pelo usuário. | 

| |[RFC003 - Criação de grupos de apoio] |
| - | - | 
| Descrição| A aplicação deve permitir que os usuários possam criar grupos de apoio para ajudar a ONG na divulgação dos animais que precisam de ajuda, compartilhando informações e fotos nas redes sociais. |
| Entradas | Informações sobre animais e atividades da ONG. |
| Pré-condições |  |
| Saída| Criação de um grupo de apoio para ajudar na divulgação das informações. | 

| |[RFC004 - Histórico de adoções] |
| - | - | 
| Descrição| A aplicação deve permitir que os usuários possam criar grupos de apoio para ajudar a ONG na divulgação dos animais que precisam de ajuda, compartilhando informações e fotos nas redes sociais. |
| Entradas | Dados sobre as adoções realizadas pela ONG. |
| Pré-condições | A ONG deve estar logada na aplicação. |
| Saída| Acesso ao histórico de adoções realizadas pela ONG. | 

| |[RFC005 - Agenda de eventos] |
| - | - | 
| Descrição| A aplicação deve permitir que a ONG possa divulgar seus eventos, como feiras de adoção, campanhas de vacinação e outros eventos relacionados. |
| Entradas | Informações sobre eventos, como data, hora e descrição. |
| Pré-condições | A ONG deve estar logada na aplicação. |
| Saída| Publicação do evento na aplicação. | 

 </details>

## Requisitos Não Funcionais 

Os requisitos não funcionais descrevem as características da aplicação que não estão diretamente relacionadas com as funcionalidades, mas que são importantes para garantir sua qualidade, usabilidade, segurança, desempenho e outros aspectos.

<details>
  <summary> Confira os requisitos </summary>

| |[RNF001 - Acesso restrito a informações sensíveis] |
| - | - | 
| Descrição| A aplicação deve permitir que os usuários possam criar grupos de apoio para ajudar a ONG na divulgação dos animais que precisam de ajuda, compartilhando informações e fotos nas redes sociais. |
| Entradas |  |
| Pré-condições |  |
| Saída|  | 

| |[RNF002 - Feedback dos usuários] |
| - | - | 
| Descrição| A aplicação deve permitir que os usuários possam enviar feedback sobre a experiência de uso da aplicação, para que a ONG possa avaliar a efetividade da aplicação e fazer melhorias necessárias. |
| Entradas | Feedback sobre a experiência de uso da aplicação. |
| Pré-condições |  |
| Saída| Análise do feedback e possíveis melhorias na aplicação. | 

| |[RNF003 - Histórico de doações] |
| - | - | 
| Descrição|  |
| Entradas |  |
| Pré-condições |  |
| Saída|  | 

| |[RNF004 - Performance] |
| - | - | 
| Descrição| A aplicação deve ter uma boa performance, com carregamento rápido e fácil navegação.  |
| Entradas |  |
| Pré-condições |  |
| Saída|  | 

| |[RNF004 - Disponibilidade] |
| - | - | 
| Descrição| A aplicação deve estar disponível 24 horas por dia, 7 dias por semana. |
| Entradas |  |
| Pré-condições |  |
| Saída|  | 

| |[RNF005 - Usabilidade] |
| - | - | 
| Descrição| A aplicação deve ser fácil de usar, com uma interface intuitiva e amigável para os usuários. |
| Entradas |  |
| Pré-condições |  |
| Saída|  | 

| |[RNF006 - Multilinguismo] |
| - | - | 
| Descrição| A aplicação deve permitir a tradução para diferentes idiomas para alcançar um público mais amplo. |
| Entradas |  |
| Pré-condições |  |
| Saída|  | 

| |[RNF007 - Escalabilidade] |
| - | - | 
| Descrição| A aplicação deve ser escalável para lidar com um grande volume de usuários e informações. |
| Entradas |  |
| Pré-condições |  |
| Saída|  | 

| |[RNF008 - Compatibilidade] |
| - | - | 
| Descrição| A aplicação deve ser compatível com diferentes dispositivos e navegadores. |
| Entradas |  |
| Pré-condições |  |
| Saída|  | 


| |[RNF009 - Manutenção] |
| - | - | 
| Descrição| A plicação deve ser facilmente mantida e atualizada pela equipe responsável. |
| Entradas |  |
| Pré-condições |  |
| Saída|  | 
  
 </details>
