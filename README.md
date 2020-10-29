# Introdução a **Banco de Dados**

[![database](./public/images/database.jpg)](https://br.freepik.com/vetores-gratis/centro-de-dados_5039056.htm#page=1&query=database&position=3)

Banco de dados é onde armazenamos dados importantes e úteis para determinados usos de maneira organizada; e para que se tenha acesso em qualquer momento, caso seja necessário buscar ou modificar informações. Isso feito de modo a proteger informações sensíveis para que somente as pessoas ou entidades autorizadas tenham acesso a esse conteúdo.

## SGBD

Sistemas de gerenciamento de banco de dados:

- **Relacionais (SQL)**: organizada em formato de tabela, planilha.Suas colunas devem estar configuradas para o tipo de valor que elas irão receber (número, string, etc), deve ser informada a relação entre elas, e são obrigatórias ou não. Bom para fazer consultas e relações entre os dados.  

  Ex: MySQL, Postgres, Microsoft SQL Server, Oracle Database.

- **Não-relacionais (NoSQL)**: dados armazenados de diversas formas, diferente de planilhas não têm uma estrutura pré-definida, por isto é muito utilizado para aplicações em tempo real. É dinâmico, escalável e permite uma grande flexibilidade.

  Ex: MongoDB, Cassandra, HBase, Redis.
---  

## MongoDB

É um sistema de gerenciamento de banco de dados não relacional do tipo documento, podendo reunir várias informações juntas num só lugar. Quando reunimos vários documentos com essas informações, temos uma coleção, já a junção de várias coleções é que forma o banco de dados. Este SGBD utiliza documentos num formato BSON que é bastante similar ao tão disseminado JSON.

Para mais informações sobre, segue a documentação:  

> https://docs.mongodb.com/manual/crud/

Documento(*BSON*) -> Coleções(*Collections*) -> Banco de dados.

Recentemente passei a utilizar o Linux (uso atualmente o Ubuntu versão 20.04) então procurei um passo a passo para a instalação do MongoDB para este caso, segue:

> https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/#verify-that-mongodb-has-started-successfully


### Principais comandos:  

```show databases```: lista todos os bancos de dados; 

```use <nomeDoNovoBancoDeDados>```: coloca um banco de dados em uso, acessa ele. E o cria, caso não exista ainda;  

```db.createCollection("<nomeDaCollection>")```: cria uma *collection*; 

```db.dropDataBase()```: estando no banco de dados escolhido, apagará o mesmo por completo;  

```db.<nomeDaCollection>.find().pretty()```: retorna uma *collection* inteira de um modo mais amigável, organizado;  

```db.<nomeDaCollection>.findOne()```: comando que retornará apenas um registro (o primeiro);  

```db.<nomeDaCollection>.insertOne({<atributos>})```: incluir novos registros na *collection* especificada;  

```db.<nomeDaCollection>.insertMany([ { <objetosASerInseridos> } ])```: inclui vários registros de uma única vez;  

```db.current```: aponta qual o banco de dados sendo utilizado no momento.