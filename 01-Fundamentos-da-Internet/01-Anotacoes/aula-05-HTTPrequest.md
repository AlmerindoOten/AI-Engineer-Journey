- Request faz uma requisição do clinete para o server/api.
- Apps são apenas interfaces, os dados estão no servidor.
- Requests podem ser filtradas por query parameter.
- query parameter podem ser por paginação para receber menos dados de uma so vez.
- toda api tem um endereço.
- Body da request leva informações maiores e mais especificas da request que nao podem ser levadas na url, é o corpo da request: leva textos, infos
de login e etc.
- Header contem as informações de comunicação da request: quem envia, para onde vai etc.
- Body: dados de operação
- Header: dados de comunicação

- Uma Request é composta por partes, e cada uma possui uma responsabilidade específica.

Method → intenção da operação.
URL → endereço da API.
Path → recurso acessado.
Query Parameters → filtros da consulta.
Header → informações sobre a comunicação.
Body → dados da operação.
