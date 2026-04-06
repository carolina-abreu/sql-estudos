1) Altere o nome da tabela caixa para dinheiro.
    **solução**
     sqlite> alter table caixa rename to dinheiro;

2) Exclua a tabela dinheiro.
     **solução**
     sqlite> drop table dinheiro;

3) Exclua a tabela notas. 
     **solução**
     sqlite> drop table notas;

4) Altere o nome da tabela super_alunos para alunos. 
     **solução**
     sqlite> alter table super_alunos rename to alunos;

5) Não gostei desse nome. Mude de alunos para estudantes. 
     **solução**
     sqlite> alter table alunos rename to estudantes;    

6) Ficou feio mesmo assim. Altere o nome de estudantes para super_estudantes. 
     **solução**
    alter table estudantes rename to super_estudantes;

7) Veja se o nome foi alterado usando o comando .tables. 
     **solução**
     .tables

8) Exclua a tabela super_estudantes.
     **solução**
     sqlite> drop table super_estudantes;

9) Agora crie novamente a tabela alunos usando o mesmo comando que usou no exercício 1. 
     **solução**
     sqlite> create table alunos (codigo integer, nome text, telefone text, cidade text);

10) Nós esquecemos que a tabela alunos precisa do campo estado! Precisamos alterar a estrutura da tabela incluindo o campo estado.
     **solução**
     sqlite> alter table alunos add estado text;     

11) Crie novamente a tabela caixa. 
     **solução**
     sqlite> create table caixa(codigo integer, data date, descricao text, debito number, credito number);

12) Adicione o campo observação do tipo text na tabela caixa. 
     **solução**
     sqlite> alter table caixa add observacao text;

13) Adicione o campo cpf na tabela alunos. 
     **solução**
     sqlite> alter table alunos add cpf text;

14) Veja a estrutura da tabela caixa 
     **solução**
     .schema

15) Adicione o campo saldo na tabela caixa. 
     **solução**
     sqlite> alter table caixa add saldo number;

16) Adicione o campo rg na tabela alunos. 
     **solução**
     sqlite> alter table alunos add rg text;    

17) Veja a estrutura da tabela alunos. 
     **solução**
     .schema

18) Altere o nome da tabela caixa para muito_dinheiro 
     **solução**
     sqlite> alter table caixa add muito_dinheiro number;    

19) Acrescente o campo cliente na tabela muito_dinheiro. 
     **solução**
     sqlite> alter table muito_dinheiro add cliente text;     

20) Adicione o campo fornecedor na tabela muito_dinheiro 
     **solução**
     sqlite> alter table muito_dinheiro add fornecedor text;

21) Mude o nome da tabela muito_dinheiro para caixa 
     **solução**
     sqlite> alter table muito_dinheiro rename to caixa;

22) Saia do sqlite. 
     **solução**
     .exit

23) Abra novamente o banco de dados lista1 no sqlite. 
     **solução**
     sqlite3 lista.sqlite

24) Veja a lista das tabelas existentes. 
     **solução**
     .tables

25) Exclua a tabela caixa 
     **solução**
     sqlite> drop table caixa;

26) Exclua a tabela alunos 
     **solução**
     sqlite> drop table alunos;

27) Insira o campo gravadora do tipo TEXT na tabela CDs 
     **solução**
     sqlite> alter table cds add gravadora text;

28) Mude o nome da tabela CDs para MeusCDs 
     **solução**
     sqlite> alter table cds rename to meuscds;

29) Mude o nome da tabela MeusCDs para NossosCDs 
     **solução**
     sqlite> alter table meuscds rename to nossoscds;     

30) Veja a estrutura da tabela NossosCDs
     **solução**
     .schema













