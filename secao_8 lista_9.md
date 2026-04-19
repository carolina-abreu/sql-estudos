1) Crie uma tabela de auditoria contendo os campos editora_id, data e observação
    **solução**
    CREATE TABLE auditoria (editoria_id, data date, obs text);

2) Crie uma trigger para que toda vez que seja inserido um novo registro na tabela editora seja gravado um registro na tabela auditoria com a informação “Registro inserido”
    **solução**
    CREATE TRIGGER auditoria AFTER INSERT ON editora
    BEGIN
        INSERT INTO auditoria (editora_id, data, obs)
        VALUES (new.id, datetime('now'), "Registro Inserido");
    END;

3) Crie uma trigger para que toda vez que seja excluído um registro na tabela editora seja gravado um registro na tabela auditoria com a informação “Registro excluído”
    **solução**
    CREATE TRIGGER auditoria2 AFTER DELETE ON editora
    BEGIN
        INSERT INTO auditoria(editora_id, data, obs)
        VALUES (old.id, datetime('now'), "Registro Excluído");
    END;

4) Faça um join na tabela de livros com autores mostrando o título do livro e do autor.
    **solução**
    SELECT titulo, nome
    FROM autor INNER JOIN livro
    ON autor.id = livro.autor_id;
    
5) Faça um join na tabela de livros com autores mostrando o título do livro e do autor usando agora um LEFT OUTER JOIN para mostrar inclusive os livros que não tenham autor definido.
    **solução**
    SELECT titulo, nome
    FROM livro, LEFT OUTER JOIN autor
    ON autor.id = livro.estilo_id;
    
6) Escreva um bloco de transação que exclua o livro de código 1 e insira um novo livro de código 50. Mas dê um rollback na transação.
    **solução**
    BEGIN TRANSACTION;
    DELETE FROM livro WHERE id = 1;
    INSERT INTO livro (id,titulo) VALUES (50,"Teste");
    ROLLBACK;

7) Escreva um bloco de transação que exclua o livro de código 3 e insira um novo livro de código 3. Feche a transação com Commit.
    **solução**
    BEGIN TANSACTION;
    DELETE FROM livro WHERE id = 3;
    INSERT INTO livro(id,titulo) VALUES (3,"SQL de A a Z");
    COMMIT;

8) Fazer um select no Banco e retornar os seguintes campos:
• Nome do autor em letras maiúsculas
• Nome do estilo em letras minúsculas
• As 10 primeiras letras do nome do livro
• Valor do Livro
• Valor do Livro com desconto de 7%
Atenção: Trata-se de UM ÚNICO COMANDO SELECT para retornar todos os campos acima.
    **solução**
    SELECT 
    UPPER (a.nome),
    LOWER (e.nome),
    SUBSTR (l.titulo,1,10),
    l.precovenda, 
    l.precovenda*0.93
    FROM livro l, autor a, estilo e
    WHERE a.id = l.autor_id
    AND e.id = l.estilo_id;

9) Faça um select trazendo o nome do livro, código do estilo, código do autor e código da editora. Caso algum campo desse esteja NULL mostre a mensagem SEM CADASTRO.
    **solução**
    SELECT titulo, 
        IFNULL (estilo_id, "SEM CADASTRO"),
        IFNULL (auto_id, "SEM CADASTRO"),
        IFNULL (editora_id, "SEM CADASTRO")
    FROM livro;

10) Mostre o nome das 6 primeiras editoras em ordem alfabética e em letras maiúsculas.
    **solução**
    SELECT nome
    FROM editora
    ORDER BY nome
    LIMIT 6;

11) Faça um select mostrando o nome do livro e o tamanho em caracteres do nome
    **solução**
    SELECT titulo, LENGTH (titulo)
    FROM livro;

12) Exiba a data atual
    **solução**
    SELECT DATE ('now');

13) Exiba a versão do SQLite
    **solução**
    SELECT sqlite_version();

14) Exiba o nome das editoras substituindo a letra a por X
    **solução**
    SELECT REPLACE (nome, "a", "x")
    FROM editora;