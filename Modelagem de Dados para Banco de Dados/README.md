# Modelagem de Dados para Banco de Dados

## Por que modelar?

Para compreendermos melhor o sistema, para termos uma representação visual do banco de dados. Possui foco na descrição e relacionamento dos elementos que compõem a representação do contexto (mini-mundo).

Modelagem pode ser classificada em:

* Representação;
* Modelo;
* Referência.

O que podemos modelar?

* Software;
* Dados;
* Computacional;
* Conceitual;
* Processo de negócios;
* Matemática.

E o esquema?

O esquema vai facilitar a compreensão do contexto dos dados.

Modelos de alto nível:

* Entidade-Relacionamento
* UML (Unified Modeling Language)

### Exemplo de SQL

Exemplo de criação de tabela:

```
CREATE DATABASE firstexample;
CREATE TABLE periodicos( 
          id integer, 
          nome varchar(120),
          issn integer
);
```

Exemplo de atribuição de chave primária:

```
CREATE DATABASE firstexample;
CREATE TABLE periodicos( 
          id integer, 
          nome varchar(120),
          issn integer,
         PRIMARY KEY (id)
);
```

Exemplo de atribuição de chave estrangeira:

```
CREATE TABLE periodicos( 
          id integer, 
          nome varchar(120),
          issn integer,
          id_editora integer,
         PRIMARY KEY (id),
         FOREIGN KEY (id_editora) REFERENCES editora(id)
);
```

## Desafio!

Criar duas entidades: Artigo e Pesquisador, com base no exemplo da aula.

#### Entidades

Pesquisador:
id
nome
pais
id_artigo

Artigo:
id
nome
id_periodico

#### Diagrama (feito no [Lucid](lucid.app))

![diagramaPesquisador-Artigo](Imagens\diagramaPesquisador-Artigo.png)

#### SQL

```
CREATE TABLE pesquisador( 
          id integer, 
          nome varchar(120),
          pais varchar(50),
          id_artigo integer,
         PRIMARY KEY (id),
         FOREIGN KEY (id_artigo) REFERENCES artigo(id)
);
CREATE TABLE artigo( 
          id integer, 
          nome varchar(120),
          id_periodico integer,
         PRIMARY KEY (id),
         FOREIGN KEY (id_periodico) REFERENCES periodico(id)
);
```

## [Instalação MySQL Windows](https://dev.mysql.com/downloads/mysql/)

## [Instalação PostgreSQL](https://www.postgresql.org/download/windows/)

## Explorando Comandos básicos SQL

Mostrar os bancos de dados existentes:

```
SHOW DATABASES;
```

Utilizar um banco de dados existente:

```
USE base1;
```

Mostrar todas as tabelas do banco de dados utilizado:

```
SHOW TABLES;
```

Remover banco de dados (PRE-RI-GO!):

```
DROP DATABASE base1;
```

Exemplo de criação de tabela (via terminal):

```
create table periodicos(
    -> id INT AUTO_INCREMENT PRIMARY KEY,
    -> nome_periodico VARCHAR(20),
    -> issn INT,
    -> id_editora INT
    -> );
```

Exemplo de alteração na tabela "periodicos", incluindo uma constraint para determinarmos uma chave estrangeira na tabela:

```
ALTER TABLE periodicos ADD CONSTRAINT fk_editora_periodico FOREIGN KEY (id_editora) REFERENCES editora(id);
```

Inserção de dados na tabela "editora":

```
INSERT INTO editora (nome_editora, pais) VALUES ('IEEE', 'EUA'), ('DataScienceMagazine', 'EUA');
```

Selecionar tudo da tabela editora:

```
SELECT * FROM editora;
```

