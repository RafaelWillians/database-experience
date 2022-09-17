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

Table Views

Como múltiplos usuários terão acesso aos dados, temos que ter alguma forma para controlarmos como os usuários terão esse acesso. Tanto teremos múltiplos usuários, como usuários diferentes a um mesmo dado. Perspectivas distintas, de um mesmo contexto.

As Views nos permitem, a partir das queries, agregar informações de tabelas diferentes a uma tabela única para termos uma visão específica dos dados no banco. Como por exemplo, reunirmos os alunos inscritos em uma escola e quais cursos ou disciplinas cada aluno está cursando. Os Joins nas queries (SQL) por exemplo, nos trazem essas views do banco.

## Compartilhamento de dados e Processamento de Transações Multiusuários

Dificilmente teremos um sistema single-user. E precisamos controlar de alguma forma esse acesso de múltiplos usuários diferentes e simultâneos. O mecanismo que irá administrar isso é o Concurrency Control.

Se um usuário acessa um dado, precisamos administrar esses dados para que, caso houver alteração neste dado por outro usuário, essa alteração seja fixada e não ocorra inconsistência nesses dados. Se alguém reserva um assento por exemplo, outros usuários precisam ter esse retorno do assento ocupado e precisamos impedir para que o mesmo assento seja ocupado por mais de 1 pessoa. 

OLTP - Online Transaction Processing

Voltado para operações em tempo real, em que precisamos ter todo o controle das transações em tempo real e o processamento dessas transações. Para quando precisamos de performance, para uma transação do início ao fim.

* App multiuser
* Gerenciador: transações concorrentes

Execução sem interferência

* Isolamento
* Atomicidade (É 8 ou 80! Ou vai ou racha!)

Transaction-driven

* Ambiente Operacional
* Processamento de dados



![oltp-olap](/Imagens\oltp-olap.png)

OLAP = Online Analytical Processing

ETL = Extract, Transform and Load

## Abordagem de banco de dados - Quais são os Atores em Banco de Dados

Atores podem ser uma ou um conjunto de pessoas, dispositivos, aplicações, etc. Em uma grande organização, pode ser um grupo muito grande de pessoas, sistemas complexos, entre outros.

Exemplos de Atores: usuários finais, administrador, designer.

### Atores - Designer

* Identificar dados e requisitos;
* Representação e Estrutura;
* Fase preliminar.

### Atores - Administrador

* Gerencia recursos como base de dados, SGBD, softwares adicionais, DBA staff;
* Orquestração;
* Autorização de acesso.

### Atores - Usuários finais

* Acesso > Querying (updates, reports)
* Categorizados como:
  * Casuais (acessos ocasionais, diferentes informações, uso de APIs)
  * Ingênuos (considerável porção, canned transactions, erro: raro)
  * Sofisticados (cientistas, engenheiros, analistas, utilizam queries)
  * Standalone (pessoa com um DB pessoal, só ele acessa o banco de dados)

Quem programa as canned transactions? Os engenheiros de software.

### Atores - Engenheiros de Software

* Análise de Sistema;
* Desenvolvimento da aplicação (ou APIs);
* Teste e documentação da aplicação.

## Workers em background - Banco de Dados

Fora do contexto de BD:

* Designer do sistema de SGBD
* Pessoal de operação e manutenção
* Implementação do sistema de SGBD
* Desenvolvedores de ferramentas

O SGBD tem o papel de disponibilizar os dados aos usuários.

## Vantagens de Utilizar a Abordagem de SGBDs

* Abstração;
* Auto-descrição;
* Isolamento;
* Compartilhamento;
* Múltiplas visões;
* Transação multiuser;

Além destas tem também:

* Controle de Redundância;

O modelo tradicional, quando deixamos os dados embarcados na aplicação, resulta em updates desnecessários, desperdício de tempo e dinheiro, redundância e inconsistência nos dados. 

Há também o conceito de Desnormalização, em que em alguns casos, há necessidade de redundância nos dados.

* Restrição de acesso (é utilizado um subsistema secundário);
* Storage - provê persistência;
* Storage - provê estrutura;
* Backup e Recovery;
* Estrutura de armazenamento e técnicas de busca (queries, caching, buffering, indexação);
* Provendo interface multiuser (mobile apps, Natural Language Interface, Query language, Forms & command codes, Programming language interface, Menu-driven);
* Representação de relações complexas (variedade de dados interrelacionados);
* Integridade de dados (definição e imposição, integridade de referência, regras de domínio, asserções, integridade referencial, triggers, dependências funcionais).

## Ganhos em utilizar SGBDs

- Padronização;
- Redução de tempo no desenvolvimento da aplicação;
- Flexibilidade.

Requisitos > Desenvolver > Testar > Aprimorar

- Disponibilidade de info atualizadas;
- Economia com escalabilidade.

## Quando não usar SGBDs

Temos de balancear o custo-benefício com o custo de overhead.

Quanto ao custo:

- Investimento inicial;
- Generelidade na definição e processamento;
- Segurança, controle de concorrência, recovery, funções de integridade.

### Quando não usar?

* Apps rigorosas, real-time;
* Acesso unário;
* BD simples (zero mudanças);
* Embedded systems (sistemas embarcados, como robôs, dispositivos diversos);
* Real World (AutoCAD, Dispositivo de Redes voltados (para comutação de pacotes), GIS Systems (sistemas de geo-localização)).
