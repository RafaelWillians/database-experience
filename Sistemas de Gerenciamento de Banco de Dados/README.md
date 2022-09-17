# Sistemas de Gerenciamento de Banco de Dados

## Abordagem de SGBDs vs. Abordagem Tradicional

Por que utilizar SGBDs?

Não faz muito sentido a própria aplicação armazenar todos os dados nela, até porque vai demandar mais armazenamento, tem a questão da segurança e disponibilidade desses dados (como que a aplicação sozinha vai administrar esses dados, torná-los seguros, confiáveis e disponíveis para todo mundo?), entre outros fatores.

Vantagens do SGBD: não precisa modificar na aplicação em si, para que a aplicação faça uma consulta de dados específica e para que a aplicação reestruture os dados. Podemos usar o SGBD para executarmos tais consultas (com SQL por exemplo) enquanto mantemos a aplicação e a estrutura dos dados como estão, evitando retrabalhos para os desenvolvedores em modificar o código da aplicação, recompilar a mesma, etc. 

Características principais:

* Abstração
* Auto-descrição
* Isolamento
* Compartilhamento
* Múltiplas visões
* Transação multiuser

## Natureza Auto-descritiva da Abordagem de Banco de Dados

Ou seja, a descrição do banco de dados em si, sua estrutura e regras.

Descrição da estrutura e constrains

DB schema: estrutura pré-definida dos dados, sem inserção dos dados.

O DBA será responsável pela estruturação do banco de dados.

Numa abordagem tradicional, os dados são persistidos e armazenados na aplicação.

Numa abordagem com SGBDs, podemos definir em separado o que são os relacionamentos (as entidades, como se relacionam), do conteúdo persistido em si (quais os dados em si, o tipo de dado).

## Isolamento Program/data e Abstração

Na abordagem tradicional, todo o tratamento dos dados estaria embarcada (embedded) na aplicação. Se precisarmos incluir um campo por exemplo, teremos que alterar a aplicação em si e isso demanda muito tempo.

Com SGBDs, separamos as coisas. O banco de dados em si vai conter a estrutura dos dados em si, como as tabelas, relacionamentos, regras, etc. e a outra parte vai conter os dados persistidos. E isso separadamente da aplicação. Se estruturarmos corretamente, a inclusão de um campo vai ser um processo muito mais suave. 

Essa característica dessa forma de trabalharmos com o SGBD, com os dados estruturados e persistidos separadamente da aplicação, é chamada de "Program-data independence".

Numa reestruturação, como por exemplo, alterarmos um campo "Nome de usuário" para se tornarem dois campos "Nome" e "Sobrenome", na abordagem tradicional eventualmente teremos que alterar a nossa aplicação. Já na abordagem com SGBDs, não interfere tanto na aplicação em si.

* Abstração - independência do programa e dados
* Transparência

## Suporte a Múltiplas Visões dos Dados

## Compartilhamento de dados e Processamento de Transações Multiusuários

## Abordagem de banco de dados - Quais são os Atores em Banco de Dados

## Workers em background - Banco de Dados

## Vantagens de Utilizar a Abordagem de SGBDs

## Ganhos em utilizar SGBDs

## Quando não usar SGBDs

