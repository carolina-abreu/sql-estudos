1) Leia do primeiro ao último exercício antes de começar a resolver.
    **solução**

2) Execute o sqlite criando um banco de dados de nome lista3.sqlite.
    **solução**
    
3) Crie uma tabela com o nome de alunos. Deverá conter o campo código (inteiro), nome, telefone e cidade (texto). Vou te ajudar nessa: CREATE TABLE alunos (codigo int, nome text, telefone text, cidade text);
    **solução**
    
4) Use o comando .tables para verificar se a tabela foi criada 
    **solução**
    
5) Crie a tabela funcionários contendo os campos código, nome, endereço, telefone, cidade, estado, cep, rg, cpf e salário. Coloque os tipos de dados necessários. 
    **solução**
    
6) Saia do sqlite com o comando .exit. 
    **solução**
    
7) Abra novamente no sqlite o banco lista3.sqlite. 
    **solução**
    
8) Verifique se as tabelas ainda existem com o comando .tables 
    **solução**
    
9) Agora iremos trabalhar com o comando insert para inserir um novo registro ao banco de dados. Apenas para você lembrar o funcionamento dele iremos inserir um registro na tabela alunos: insert into alunos (código, nome, telefone, cidade) values (1,’Ana’,’9999-9999’,’Ituiutaba’); - Faça esse comando agora. 
    **solução**
    
10) Precisamos agora verificar se o registro foi inserido corretamente. Então precisamos selecionar todos os dados da tabela alunos. Use o comando select desse jeito: select * from alunos; (lembre-se que o * aqui nesse caso significa todos os campos, ou seja, irá mostrar nome, endereço, código, etc). 
    **solução**
    
11) Insira um novo registro na tabela alunos com os seus dados. 
    **solução**
    
12) Selecione os registros da tabela alunos e veja se o registro foi inserido. 
    **solução**
    
13) Ligue os cabeçalhos usando o comando .headers on 
    **solução**
    
14) Selecione novamente para verificar se o cabeçalho foi mostrado corretamente. 
    **solução**
    
15) Insira na tabela alunos o aluno José Buscapé. 
    **solução**
    
16) Selecione o conteúdo da tabela e veja se foi inserido corretamente. 
    **solução**
    
17) Agora você vai aprender um novo recurso do comando select. Você pode escolher os CAMPOS que deseja que sejam exibidos. Por exemplo, se eu quiser exibir somente o código e o nome devo usar o comando assim: select codigo,nome from alunos; - Faça isso agora! 
    **solução**
    
18) Selecione somente o nome e telefone dos alunos. 
    **solução**
    
19) Selecione o nome e a cidade dos alunos 
    **solução**
    
20) Selecione somente o código e o telefone dos alunos 
    **solução**
    
21) Insira 4 novos alunos; 
    **solução**
    
22) Selecione todos os campos da tabela alunos 
    **solução**
    
23) Selecione da tabela alunos os seguintes campos (nessa ordem): cidade, código, nome. Veja que você pode exibir os dados na ordem que quiser.
    **solução**
    
24) Insira mais um alunos na tabela alunos. 
    **solução**
    
25) Saia do sqlite, feche o terminal e abra novamente. 
    **solução**
    
26) Selecione os dados da tabela a alunos e veja se ainda existem. 
    **solução**
    
27) Adicione 1 novo funcionário. Lembre-se que é necessário usar aspas para campos TEXTO. Campos numéricos não podem ter aspas. Se o salário tiver centavos, lembre-se que deve separar os centavos com um (.) (ponto) pois a vírgula é usada para separar os valores a serem inseridos. 
    **solução**
    
28) Selecione os dados da tabela funcionários e veja se foi inserido corretamente. 
    **solução**
    
29) Cadastre 3 funcionários. Use código na sequência. (1,2,3,4,5 etc). 
    **solução**
    
30) Selecione somente o código e nome dos funcionários.  
    **solução**
    


