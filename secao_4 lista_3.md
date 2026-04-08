1) Leia do primeiro ao último exercício antes de começar a resolver.
    **solução**
    NA
2) Execute o sqlite criando um banco de dados de nome lista3.sqlite.
    **solução**
    banco de dados criado utilizando a interface do SQLite Studio

3) Crie uma tabela com o nome de alunos. Deverá conter o campo código (inteiro), nome, telefone e cidade (texto).
    **solução**
    CREATE TABLE alunos(
        codigo int, 
        nome text, 
        telefone text, 
        cidade text
    );

4) Use o comando .tables para verificar se a tabela foi criada 
    **solução**
    Esse comando não é valido para SQLite

5) Crie a tabela funcionários contendo os campos código, nome, endereço, telefone, cidade, estado, cep, rg, cpf e salário. Coloque os tipos de dados necessários. 
    **solução**
    CREATE TABLE funcionarios(
        codigo int, 
        nome text, 
        endereco text, 
        telefone text, 
        cidade text, 
        estado text, 
        cep text, 
        rg text, 
        cpf text, 
        salario number
    );

6) Saia do sqlite com o comando .exit. 
    **solução**
    Esse comando não é valido para SQLite

7) Abra novamente no sqlite o banco lista3.sqlite. 
    **solução**
    NA

8) Verifique se as tabelas ainda existem com o comando .tables 
    **solução**
    Esse comando não é valido para SQLite
    
9) Agora iremos trabalhar com o comando insert para inserir um novo registro ao banco de dados. Iremos inserir um registro na tabela alunos: 1,Ana,9999-9999,Ituiutaba.
    **solução**
    INSERT INTO alunos( codigo, nome, telefone, cidade) 
    VALUES(1,'Ana', '9999-9999', 'Ituiutaba');

10) Precisamos agora verificar se o registro foi inserido corretamente. Então precisamos selecionar todos os dados da tabela alunos.
    **solução**
    SELECT * FROM alunos;

11) Insira um novo registro na tabela alunos com os seus dados. 
    **solução**
    INSERT INTO alunos(codigo, nome, telefone, cidade) 
    VALUES(2,'Carolina', '99591-9722','Curitiba');

12) Selecione os registros da tabela alunos e veja se o registro foi inserido. 
    **solução**
    SELECT * FROM alunos;

13) Ligue os cabeçalhos usando o comando .headers on 
    **solução**
    Esse comando não é valido para SQLite

14) Selecione novamente para verificar se o cabeçalho foi mostrado corretamente. 
    **solução**
    NA

15) Insira na tabela alunos o aluno José Buscapé. 
    **solução**
    INSERT INTO alunos (codigo, nome, telefone, cidade) 
    VALUES (3,'José Buscapé','8888-8888','Belo Horizonte');

16) Selecione o conteúdo da tabela e veja se foi inserido corretamente. 
    **solução**
    SELECT * FROM alunos;

17) Exibir somente o código e o nome.
    **solução**
    SELECT codigo, nome FROM alunos;
    
18) Selecione somente o nome e telefone dos alunos. 
    **solução**
    SELECT nome, telefone FROM alunos;
    
19) Selecione o nome e a cidade dos alunos 
    **solução**
    SELECT nome, cidade FROM alunos;
    
20) Selecione somente o código e o telefone dos alunos 
    **solução**
    SELECT codigo,telefone FROM alunos;

21) Insira 4 novos alunos; 
    **solução**
    INSERT INTO (codigo, nome, telefone, cidade) 
    VALUES 
    (4, 'Bruno', '7777-7777', 'São Paulo'),
    (5, 'Carla', '1111-1111', 'Rio de Janeiro'),
    (6, 'Daniel', '6666-6666', 'Vitória'),
    (7, 'Eduarda', '5555-5555', 'Florianópolis');
    
22) Selecione todos os campos da tabela alunos 
    **solução**
    SELECT * FROM alunos;

23) Selecione da tabela alunos os seguintes campos (nessa ordem): cidade, código, nome. Veja que você pode exibir os dados na ordem que quiser.
    **solução**
    SELECT cidade,codigo,nome FROM alunos;

24) Insira mais um alunos na tabela alunos. 
    **solução**
    INSERT INTO alunos (codigo, nome, telefone, cidade) VALUES (8,'Gustavo','2222-2222','Juiz de Fora');

25) Saia do sqlite, feche o terminal e abra novamente. 
    **solução**
    NA

26) Selecione os dados da tabela a alunos e veja se ainda existem. 
    **solução**
    SELECT * FROM alunos;
    
27) Adicione 1 novo funcionário. Lembre-se que é necessário usar aspas para campos TEXTO. Campos numéricos não podem ter aspas. Se o salário tiver centavos, lembre-se que deve separar os centavos com um (.) (ponto) pois a vírgula é usada para separar os valores a serem inseridos. 
    **solução**
    INSERT INTO funcionarios(codigo,nome,endereco,telefone,cidade,estado,cep,rg,cpf,salario)
    VALUES (1,'Marcelo Silva','Av Sete de Abril, 755','2222-2222','Palmeira','PR','005878-020','PR-17.985.237','157.154.687-58',2500.50);

28) Selecione os dados da tabela funcionários e veja se foi inserido corretamente. 
    **solução**
    SELECT * FROM funcionarios;
    
29) Cadastre 3 funcionários. Use código na sequência. (1,2,3,4,5 etc). 
    **solução**
    INSERT INTO funcionarios (codigo, nome, endereco, telefone, cidade, estado, cep, rg, cpf, salario)
    VALUES
    (2, 'João Marcos', 'Rua das Flores, 123', '9999-1111', 'São Paulo', 'SP', '01000-000', 'SP-123.456.78', '123.456.789-00', 3530.20),
    (3, 'Maria Oliveira', 'Av Brasil, 456', '8888-2222', 'Rio de Janeiro', 'RJ', '20000-000', 'RJ-876.543.21', '987.654.321-00', 4270.50),
    (4, 'Carlos Souza', 'Rua Central, 789', '7777-3333', 'Joinville', 'SC', '89200-000', 'SC-112.233.44', '111.222.333-44', 3985.30);   
    
30) Selecione somente o código e nome dos funcionários.  
    **solução**
    SELECT codigo,nome FROM funcionarios;