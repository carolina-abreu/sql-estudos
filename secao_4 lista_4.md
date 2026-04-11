1) Selecione somente o nome e salário dos funcionários.
    **solução**
   SELECT nome, salario FROM funcionarios; 

2) Selecione somente o nome e telefone dos funcionários.
    **solução**
    SELECT nome, telefone FROM funcionarios;

3) Selecione somente o nome, rg e cpf dos funcionários.
    **solução**
    SELECT nome, rg,cpf FROM funcionarios;

4) Selecione somente o nome e a cidade dos funcionários.
    **solução**
    SELECT nome, cidade FROM funcionarios;

5) Insira mais um funcionário.
    **solução**
    INSERT INTO funcionarios (codigo, nome, endereco, telefone, cidade, estado, cep, rg, cpf, salario)
    VALUES
    (2, 'Roberta Juliana', 'Rua das Dores, 55', '9999-5588', 'São Paulo', 'SP', '05888-047', 'SP-567.891.22', '123.456.789-08', 4250.50)

6) Exiba todos os dados dos funcionários.
    **solução**
    SELECT * FROM funcionarios;

7) Crie a tabela fornecedores contendo os campos nome, endereço, telefone, cidade, estado, cep, cnpj e email. Coloque os tipos de dados necessários.
    **solução**
    CREATE TABLE fornecedores(nome text, endereco text, telefone text, cidade text, estado text, cep text, cnpj text, email text);

8) Insira 2 fornecedores. Código 1 e Código 2
    **solução**
    INSERT INTO fornecedores(nome, endereco, telefone, cidade, estado, cep, cnpj, email) 
    VALUES 
    ('Tech Distribuidora Ltda', 'Rua das Flores, 123', '(11) 3456-7890', 'São Paulo', 'SP', '01001-000', '12.345.678/0001-90', 'contato@techdistribuidora.com'),
    ('Alimentos Bom Sabor SA', 'Av. Brasil, 987', '(21) 2345-6789', 'Rio de Janeiro', 'RJ', '20040-002', '98.765.432/0001-10', 'vendas@bomsabor.com');

9) Selecione o nome e o telefone dos fornecedores.
    **solução**
    SELECT nome, telefone FROM fornecedores;

10) Agora iremos aprender uma opção do comando select. Nós podemos restringir o que vai ser exibido na tela. É moleza. Por exemplo se eu quiser listar somente o aluno de código 2 o comando fica assim: select * from alunos where codigo = 2; - Nós apenas adicionamos o WHERE e a CONDIÇÃO.Veja que mantivemos o * para exibir todos os campos, mas poderíamos também exibir somente o nome do aluno 2 assim: select nome from alunos where codigo = 2; - EXPERIMENTE AGORA ESSES 2 COMANDOS.
    **solução**
    SELECT * FROM alunos WHERE codigo=2;
    SELECT nome FROM alunos WHERE codigo=2;      

11) Selecione o funcionário de código 3.
    **solução**
    SELECT * FROM funcionarios WHERE codigo=3;

12) Selecione o fornecedor de código 1.
    **solução**
    Tabela fornecedores não possui coluna 'codigo'

13) Selecione o aluno de código 2.
    **solução**
    SELECT * FROM alunos WHERE codigo=2;

14) Selecione o funcionário de código 1. 
    **solução**
    SELECT * FROM funcionarios WHERE codigo=1;

15) Selecione somente o nome e salário do funcionário de código 2.
    **solução**
    SELECT nome, salario FROM funcionarios WHERE codigo = 2;

16) Selecione somente o nome a cidade do aluno de código 1.
    **solução**
    SELECT nome,cidade FROM alunos WHERE codigo=1;

17) Selecione todos os funcionários de MG.
    **solução**
    SELECT * FROM funcionarios WHERE estado='MG';

18) Selecione todos os funcionários de GO.
    **solução**
    SELECT * FROM funcionarios WHERE estado='GO';

19) Selecione todos os funcionários de SP.
    **solução**
    SELECT * FROM funcionarios WHERE estado = 'SP';

20) Insira um funcionário para SP.
    **solução**
    INSERT INTO funcionarios (codigo, nome, endereco, telefone, cidade, estado, cep, rg, cpf, salario)
    VALUES
    (6, 'Mario Rezende', 'Rua Bartira, 479', '8888-3534', 'São Paulo', 'SP', '02580-088', 'SP-132.465.88', '987.654.321-55',2575.20);
 
21) Selecione todos os funcionários de SP.
    **solução**
    SELECT * FROM funcionarios WHERE estado = 'SP';

22) Crie a tabela livros contendo o campo código, nome, categoria, resumo, precocusto, precovenda.
    **solução**
    CREATE TABLE livros(codigo int, nome text, categoria text, resumo text, precocusto number, precovenda number);

23) Verifique o esquema .schema da tabela livros.
    **solução**
    Esse comando não é valido para SQLite

24) Liste as tabelas existentes.
    **solução**
    SELECT name FROM sqlite_master WHERE type = 'table';

25) Insira 1 livro.
    **solução**
    INSERT INTO livros(codigo, nome, categoria, resumo, precocusto, precovenda)
    VALUES 
    (1, 'Excel do Básico ao Avançado', 'Educação', 'Aprenda Excel passo a passo com exemplos práticos', 30.00, 79.90),
    (2, 'Introdução à Análise de Dados', 'Tecnologia', 'Conceitos iniciais de análise de dados e ferramentas', 45.00, 99.90),
    (3, 'SQL para Iniciantes', 'Tecnologia', 'Guia completo para aprender SQL do zero', 25.00, 69.90);

26) Selecione o nome e a categoria do livro de código 1.
    **solução**
    SELECT nome,categoria FROM livros WHERE codigo=1;

27) Selecione o nome e a categoria do livro de código 3.
    **solução**
    SELECT nome,categoria FROM livros WHERE codigo=3;

28) Exclua a tabela livros.
    **solução**
    DROP TABLE livros;

29) Altere o nome da tabela aluno para estudantes.
    **solução**
    ALTER TABLE alunos RENAME TO estudantes;

30) Altere a tabela alunos inserindo o campo estado. Se estiver com dúvidas consulte a primeira lista de
exercícios
    **solução**
    ALTER TABLE estudantes ADD estado text;