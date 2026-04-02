1) Execute o sqlite criando um banco de dados de nome lista1.sqlite. 
    **solução**
    windows+R > cmd > cd OneDrive\Desktop > sqlite3 lista.sqlite

2) Crie uma tabela com o nome de alunos. Deverá conter o campo código (inteiro), nome, telefone e 
cidade (texto).
    **solução**
    sqlite> create table alunos(codigo integer, nome text, telefone text, cidade text);

3) Use o comando .tables para verificar se a tabela foi criada
    **solução**
    .tables

4) Crie uma tabela com o nome de alunos2. Deverá conter o campo código (inteiro), nome (varchar de 
tamanho 200), telefone (varchar de tamanho 50)e cidade (varchar de tamanho 100). 
    **solução**
    sqlite> create table alunos2(codigo integer, nome varchar(200), telefone varchar(50), cidade varchar(100));

5) Crie a tabela funcionários contendo os campos nome, endereço, telefone, cidade, estado, cep, rg, cpf 
e salário. Coloque os tipos de dados necessários.
    **solução**
    create table funcionarios(nome text, endereco text, telefone text, cidade text, estado text, cep text, rg text, cpf text);

6) Saia do sqlite com o comando.
    **solução**
    .exit

7) Abra novamente no sqlite o banco lista1.sqlite. 
    **solução**
    windows+R > cmd > cd OneDrive\Desktop > sqlite3 lista.sqlite

8) Verifique se as tabelas ainda existem com o comando.
    **solução**
    .tables

9) Crie a tabela fornecedores contendo os campos nome, endereço, telefone, cidade, estado, cep, cnpj e email. Coloque os tipos de dados necessários.
    **solução**
    sqlite> create table fornecedores(nome text, endereco text, telefone text, cidade text, estado text, cep text, cnpj text, email text);

10) Crie a tabela livros contendo o campo código, nome, categoria, resumo, precocusto, precovenda.
    **solução**
    sqlite> create table livros(codigo integer, nome text, categoria text, resumo text, precocusto number, precovenda number);

11) Existe uma maneira de verificar o ESQUEMA da tabela, ou seja, sua estrutura.
    **solução**
    .schema
    CREATE TABLE alunos(codigo integer, nome text, telefone text, cidade text);
    CREATE TABLE alunos2(codigo integer, nome varchar(200), telefone varchar(50), cidade varchar(100));
    CREATE TABLE funcionarios(nome text, endereco text, telefone text, cidade text, estado text, cep text, rg text, cpf text);
    CREATE TABLE fornecedores(nome text, endereco text, telefone text, cidade text, estado text, cep text, cnpj text, email text);
    CREATE TABLE livros(codigo integer, nome text, categoria text, resumo text, precocusto number, precovenda number);

12) Crie a tabela estoque contendo o campo código, nomedoproduto, categoria, quantidade e fornecedor
    **solução**
    sqlite> create table estoque(codigo integer, nomedoproduto text, categoria text, quantidade integer, fornecedor text);

13) Crie a tabela notas contendo os campos código, nomedoaluno, bim1, bim2, bim3 e bim4 
    **solução**
    sqlite> create table notas(codigo integer, nomedoaluno text, bim1 number, bim2 number, bim3 number);

14) Crie a tabela caixa contendo os campos código, data, descrição, debito e credito.
    **solução**
    sqlite> create table caixa(codigo integer, data date, descricao text, debito number, credito number);

15) Crie a tabela contasAPagar contendo os campos código, data_conta, descrição, valor e data_pagamento.
    **solução**
    sqlite> create table contasAPagar(codigo integer, data_conta date, descricao text, valor number, data_pagamento date);

16) Crie a tabela contasAReceber contendo os campos código, data_conta, descrição, valor e data_recebimento.
    **solução**
    sqlite> create table contasAReceber(codigo integer, data_conta date, descricao text, valor number, data_recebimento date);

17) Crie a tabela filmes contendo os campos código, nome, sinopse, categoria e diretor
    **solução**
    sqlite> create table filmes(codigo integer, nome text, sinopse text, categoria text, diretor text);

18) Crie a tabela CDs contendo os campos código, nome, cantor, ano e quantidademusicas.
    **solução**
    sqlite> create table cds(codigo integer, nome text, cantor text, ano integer, quantidademusicas integer);

19) Exclua a tabela alunos. 
    **solução**
    sqlite> drop table alunos;

20) Use o comando e veja se a tabela realmente foi excluída
    **solução**
    .tables

21) Exclua a tabela livros.
    **solução**
    sqlite> drop table livros;

22) Exclua a tabela contasAPagar.
    **solução**
    sqlite> drop table contasAPagar;

23) Exclua também a tabela contasAReceber.
    **solução**
    sqlite> drop table contasAReceber;

24) Agora apague a tabela filmes.
    **solução**
    sqlite> drop table filmes;

25) Liste as tabelas e veja se a tabela alunos2 ainda existe.
    **solução**
    .tables

26) Renomeie a tabela alunos2 para super_alunos
    **solução**
    sqlite> alter table alunos2 rename to super_alunos;

27) Use o comando e veja se foi alterado o nome.
    **solução**
    .tables

28) Altere o nome da tabela estoque para produtos.
    **solução**
    sqlite> alter table estoque rename to produtos;

29) Altere o nome da tabela notas para aprovados.
    **solução**
    sqlite> alter table notas rename to aprovados;  

30) Altere o nome da tabela aprovados para notas.
    **solução**
    sqlite> alter table aprovados rename to notas;


