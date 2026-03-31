# Seção 3 - Criando tabelas e inserindo informações
    
    ## Aula 11 - Antes de começar
        - Como abrir o sqlite3: prompt de comando > cd OneDrive\Desktop > (vai acessar os arquivos da área de trabalho) > dir > (vai mostrar os arquivos na área de trabalho) > sqlite3 "nome do banco de dados que deve ser criado"
        - Necessário seguir esses passos, para evitar a mensagem "transient in-memory database"

    ## Aula 12 - Criando uma tabela
        - abri o sqlite3 usando o prompt de comandos, usando as instruções da aula 11, nesse caso, abrindo o sqlite3 já criando um banco de dados, utilizando o comando abaixo:
        sqlite3 aula.sqlite
        - criamos 3 tabelas no sqlite3 usando as seguintes linhas de comando:
        sqlite> create table agenda (nome text, telefone text);
        sqlite> .tables
        (resultado) agenda
        sqlite> create table alunos (matricula integer, nome text, telefone text, cidade text);
        sqlite> .tables
        (resultado) agenda  alunos
        sqlite> create table produtos (codigo integer, nome text, qtd integer);
        sqlite> .tables
        (resultado) agenda    alunos    produtos
        sqlite> .exit
        - create table é um DDL - Data Definition Language, comando SQL.

    ## Aula 13 - Inserindo informações
        - abri o sqlite usando o prompt de comandos
        windows+r > cmd > cd OneDrive\Desktop > slite3 aula.sqlite
        - .tables para visualizar as tabelas no banco de dados
        - .schema: mostra as definições da tabela (colunas, tipo das colunas)
        - insert: comando para inserir dados em uma tabela
            insert into agenda(nome,telefone) values ('Maria','99999-9999');
        - comando para mostrar o banco de dados agenda: sqlite> select * from agenda; 
        - comando para mostrar o banco de dados agenda com o cabeçalho (nome das colunas): 
            sqlite> .headers on
            sqlite> select * from agenda;

    ## Aula 14 - Entendendo os tipos de dados
        - text: texto entre aspas simples
        - varchar, varchar2 e string: também usado para textos
        - integer: números inteiros
        - number: números com casa decimal
        - single, double, real: também usado para casas decimais
        - date: usado para datas
        - boolean: para tipo de dados booleanos
        - chave primária: campo existente na tabela que torna o registro único.

    ## Aula 15 - FIQUE ATENTO! Tabelas, campos e registros

    ## Aula 16 - Excluindo uma tabela

    ## Aula 17 - Mudando o nome da tabela

    ## Aula 18 - Vamos adicionar um campo na tabela

    ## Aula 19 - Exercícios - Lista 1

    ## Aula 20 - Correção de exercícios

    ## Aula 21 - Continuação da correção

    ## Aula 22 - Exercícios - Lista 2

    ## Aula 23 - Correção dos exercícios