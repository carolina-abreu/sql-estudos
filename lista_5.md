1) Crie no SqliteStudio um banco de dados chamado lista5.sqlite e execute os comandos abaixo.

2) Crie uma tabela com o nome de livros contendo os campos codigo, titulo, codigo do autor, código da editora, código do estilo, sinopse e isbn.
    **solução**
    CREATE TABLE livro(id int, titulo text, autor_id int, editora_id int, estilo_id int, sinopse text, isbn text);

3) Crie uma tabela com o nome de editoras contendo o codigo, nome, cidade, estado, telefone e e-mail.
    **solução**
    CREATE TABLE editora(id int, nome text, cidade text, estado text, telefone text, email text);

4) Crie uma tabela com o nome de estilos contendo o código e o nome do estilo.
    **solução** 
    CREATE TABLE estilo(id int, nome text);

5) Crie uma tabela com o nome de autores contendo o codigo, nome, cidade, estado, telefone do autor.
    **solução**
    CREATE TABLE autor(id int, nome text, cidade text, estado text, telefone text, telefone_autor text);

6) Insira um registro na tabela livros (todos os campos)
    **solução**
    INSERT INTO livro(id, titulo, autor_id, editora_id, estilo_id,sinopse, isbn)
    VALUES(1, 'O Código das Sombras', 1,1,1, 'Um analista de dados descobre padrões misteriosos que revelam uma conspiração global.', '9781234567890');

7) Insira um registro na tabela editoras (todos os campos).
    **solução**
    INSERT INTO editora(id, nome, cidade, estado, telefone, email)
    VALUES (1, 'TechBooks Editora', 'São Paulo', 'SP', '11987654321', 'contato@techbooks.com');

8) Insira um registro na tabela estilos (todos os campos).
    **solução**
    INSERT INTO estilo(id, nome)
    VALUES (1, 'Suspense Tecnológico');

9) Insira um registro na tabela autores (todos os campos).
    **solução**
    INSERT INTO autor(id, nome, cidade, estado, telefone, telefone_autor)
    VALUES (1, 'Lucas Andrade', 'São Paulo', 'SP', '1133345566', '11999998888');

10) Altere o nome da tabela autores para autor.
    **solução**
    Criei a tabela já com nome no singular.

11) Insira na tabela livros um novo registro adicionando somente os campos codigo e nome
    **solução**
    INSERT INTO livro(id,titulo)
    VALUES (2, 'Entre Linhas e Bugs');

12) Insira 5 estilos de livros.
    **solução**
    INSERT INTO estilo(id, nome)
    VALUES 
    (2, 'Comédia'),
    (3,'Drama'),
    (4,'Ficção'),
    (5,'Suspense'),
    (6,'Romance');

13) Selecionar todos os livros do banco de dados.
    **solução**
    SELECT * FROM livro;

14) Insira 2 novos livros.
    **solução**
    INSERT INTO livro(id, titulo, autor_id, editora_id, estilo_id,sinopse, isbn)
    VALUES
    (3, 'A Última Query', 3, 2, 2, 'Um detetive utiliza SQL para desvendar crimes em uma cidade dominada pela tecnologia.', '9781234567892'),
    (4, 'Amor em Planilhas', 4, 3, 3, 'Dois colegas de trabalho se aproximam enquanto colaboram em um projeto de Excel.', '9781234567893');
    
15) Altere o nome da tabela livros autores para livro.
    **solução**
    Criei a tabela já com nome no singular.

16) DESAFIO: Selecione o nome de todos os estilos em ordem alfabética
    **solução**
    SELECT * FROM estilo ORDER BY nome;

17) DESAFIO: Selecione o nome de todos os autores em ordem alfabética inversa.
    **solução**
    SELECT * FROM autor ORDER BY nome DESC;

18) Selecione o nome e o telefone de todas as editoras.
    **solução**
    SELECT nome, telefone FROM editora;

19) Selecione o nome de todas as editoras
    **solução**

20) Selecione o nome de todas as editoras de MG
    **solução**
    SELECT nome FROM editora;

21) Selecione os estilos de livros em ordem alfabética.
    **solução**
    SELECT * FROM estilo ORDER BY nome;

22) Selecione agora em ordem alfabética inversa.
    **solução**
    SELECT * FROM estilo ORDER BY nome DESC;

23) Selecione o nome de todos os autores de SP.
    **solução**
    SELECT * FROM autor WHERE estado = 'SP';

24) Selecione o estilo de código 13
    **solução**
    SELECT * FROM estilo WHERE id=13;

25) Selecione o autor de código 8
    **solução**
    SELECT * FROM autor WHERE id=8;

26) Selecione a editora de código 10
    **solução**
    SELECT * FROM editora WHERE id=10;

27) Selecione o nome, a cidade e o estado de todas as editoras.
    **solução**
    SELECT nome,cidade,estado FROM editora;

28) Adicione 3 editoras.
    **solução**
    INSERT INTO editora(id, nome, cidade, estado, telefone, email)
    VALUES
    (2, 'Alpha Editora', 'Florianópolis', 'SC', '4833334444', 'contato@alpha.com'),
    (3, 'Beta Livros', 'Porto Alegre', 'RS', '5132221111', 'contato@betalivros.com'),
    (4, 'Gamma Publicações', 'Belo Horizonte', 'MG', '3135556666', 'contato@gamma.com');

29) Selecione o nome de todas as editoras
    **solução**
    SELECT nome FROM editora;

30) Exclua a editora de código 1
    **solução**
    DELETE FROM editora WHERE id=1;
