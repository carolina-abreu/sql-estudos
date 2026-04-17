1) Faça um select somente de 10 editoras de GO
    **solução**
    SELECT * FROM editora
    WHERE estado = "GO"
    LIMIT 10;

2) Exiba o nome das editoras em ordem inversa e retorne as 3 primeiras
    **solução**
   SELECT nome FROM editora
   ORDER BY nome DESC
   LIMIT 3;

3) Exiba todos os estados que temos editoras cadastradas
    **solução**
   SELECT DISTINCT estado FROM editora;

4) Crie uma view para o select que você fez no exercício 1 com o nome de GOIAS.
    **solução**
    CREATE VIEW Goias AS
    SELECT * FROM editora
    WHERE estado = "GO";

5) Crie uma view para o select que você fez no exercício 3 com o nome de ESTADOS.
    **solução**
   CREATE VIEW Estados AS 
   SELECT DISTINCT estado FROM editora;

6) Crie um índice para o estado na tabela Editora
    **solução**
    CREATE INDES indice_estado ON editora(
        estado
    );
   
7) Crie um índice para o nome do autor.
    **solução**
    CREATE INDEX indice_autor ON autor(
        nome
    );

8) Utilize subselect e exclua todos os livros da editora XPTO
    **solução**
    DELETE FROM livro
    WHERE editora_id = (
        SELECT id
        FROM editora
        WHERE nome="XPTO"
    );
   
9) Utilize subselect e exclua todos os livros do autor José Buscapé
    **solução**
   DELETE FROM livro
    WHERE editora_id = (
        SELECT id
        FROM autor
        WHERE nome="José Buscapé"
    );

10) Exclua a view GOIAS
    **solução**
    DROP VIEW Goias;

11) Exclua o índice da tabela Editora
    **solução**
   DROP INDEX indice_estado;

12) Exclua a view Estados
    **solução**
    DROP VIEW Estados;
   
13) Exiba em ordem alfabética as editoras e mostre as 7 primeiras (somente o nome).
    **solução**
   SELECT nom FROM editora
   ORDER BY nome 
   LIMIT 7;

14) Exclua o índice da tabela autor
    **solução**
   DROP INDEX indice_autor;

15) Crie um índice para o nome do livro
    **solução**
   CREATE INDEX indice_titulo on livro (titulo);