1) Abra no SQLite Studio o banco de dados com o controle de livros que desenvolvemos.
    **solução**
    NA

2) Selecione o nome e o estilo de todos os livros
    **solução**
    SELECT l.titulo, e.nome
    FROM livro l, estilo e
    WHERE e.id = l.estilo_id;
    
3) Selecione o nome e a editora de todos os livros
    **solução**
    SELECT l.titulo, e.nome
    FROM livro l, editora e
    WHERE e.id = l.editora_id;

4) Selecione o nome e o autor de todos os livros
    **solução**
    SELECT l.titulo, a.nome
    FROM livro l, autor a
    WHERE a.id = l.autor_id;

5) Selecione o nome e o estilo de todos os livros que começam por “A”
    **solução**
    SELECT l.titulo, e.nome
    FROM livro l, estilo e
    WHERE e.id = l.estilo_id
    AND l.titulo like "A%";

6) Selecione o nome e o estilo de todos os livros que cujo estilo comece por “R”
    **solução**
    SELECT l.titulo, e.nome
    FROM livro l, estilo e
    WHERE e.id = l.estilo_id
    AND e.nome like "R%";

7) Selecione o nome do autor, da editora, do estilo e do livro de todos os livros de autores cujo nome comece por D.
    **solução**
    SELECT a.nome, e.nome, es.nome, l.titulo
    FROM livro l, autor a, editora e, estilo es
    WHERE a.id = l.autor_id
    AND e.id = l.editora_id
    AND es.id = l.estilo_id;
    
8) Selecione o nome do autor, da editora, do estilo e do livro de todos os livros de editoras paulistas.
    **solução**
    SELECT a.nome, e.nome, es.nome, l.titulo
    FROM livro l, autor a, editora e, estilo es
    WHERE a.id = l.autor_id
    AND e.id = l.editora_id
    AND es.id = l.estilo_id
    AND e.estado = "SP";
    
9) Atualize o autor do livro de id 1 para autor_id 2.
    **solução**
    UPDATE livro
    SET autor_id = 2
    WHERE id=1;

10) Atualize o telefone da editora de id 3 para 44 6666-6666
    **solução**
    UPDATE editora
    SET telefone = '446666-6666'
    WHERE id = 3;
    
11) Atualize o nome do autor 1 para “Graciliano Ramos”
    **solução**
    UPDATE autor
    SET nome = 'Graciliano Ramos'
    WHERE id = 1;

12) Atualize o estilo 5 para Fantasia.
    **solução**
    UPDATE estilo
    SET nome = 'Fantasia'
    WHERE id = 5;

13) Selecione o nome do livro e do estilo de todas as editoras de SP.
    **solução**
    SELECT l.titulo, e.nome
    FROM livro l, estilo e, editora ed
    WHERE e.id = l.editora_id
    AND ed.estado = "SP";
    
14) Selecione o nome do livro e da Editora de todas as editoras de SP.
    **solução**
    SELECT l.titulo, ed.nome
    FROM livro l, editora ed
    WHERE ed.id = l.editora_id
    AND ed.estaqdo = "SP";

15) Selecione o nome do livro e do autor de em ordem alfabética por autor.
    **solução**
    SELECT l.titulo, a.nome
    FROM livro l, autor a
    WHERE a.id = l.autor_id
    ORDER BY a.nome;