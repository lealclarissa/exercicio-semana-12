# Exercício Semana 12

## Introdução a **Banco de Dados**

### Banco de dados:

- Entidades:

- Atributos:

### SGBD

Sistemas de gerenciamento de banco de dados:

- Relacionais: estruturado previamente,  
  Ex: Oracle, MySQL, PostgreSQL

- Não-relacionais: dinâmico, escalável
  Ex: MongoDB,

## MongoDB

Documento(*BSON*) -> Coleções(*Collections*) -> Banco de dados

### Principais comandos:  

```show databases```: lista todos os bancos de dados; 

```use <nomeDoNovoBancoDeDados>```: cria um banco de dados novo caso já não exista nenhum com o nome escolhido, e acessa ele;  

```db.createCollection("<nomeDaCollection>")```: cria uma *collection*; 

```db.dropDataBase()```: estando no banco de dados escolhido, removerá o mesmo por completo;  

```db.<nomeDaCollection>.find().pretty()```: retorna uma *collection* de um modo mais amigável, organizado;  

```db.<nomeDaCollection>.findOne()```: comando que retornará apenas um registro;  

```db.<nomeDaCollection>.insertOne({<atributos>})```: incluir novos registros na *collection* especificada;  

```db.<nomeDaCollection>.insertMany([ { <objetosASerInseridos> } ])```: inclui vários registros de uma única vez;  

```db.current```: aponta qual o banco de dados sendo utilizado no momento;