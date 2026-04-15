# Seção 7 - Vamos aprender umas coisas legais

    ## Aula 52 - Criando VIEW
        visualização
        atalho para um select
        exemplo: criar uma view para o select abaixo
        SELECT a.nome, e.nome, es.nome, l.titulo, e.estado
        FROM livro l, autor a, editora e, estilo es
        WHERE a.id = l.autor_id
        AND e.id = l.editora_id
        AND es.id = l.estilo_id
        AND e.estado="SP";

        CREATE VIEW SaoPaulo AS
        SELECT a.nome, e.nome, es.nome, l.titulo, e.estado
        FROM livro l, autor a, editora e, estilo es
        WHERE a.id = l.autor_id
        AND e.id = l.editora_id
        AND es.id = l.estilo_id
        AND e.estado="SP";
        (cria uma view na barra esquerda do sqlite)

        SELECT * FROM SaoPaulo; (o resultado vai ser como se fosse o select acima)

    ## Aula 53 - Excluindo VIEW
        DROP VIEW;

    ## Aula 54 - O comando create INDEX
        index = índice
        acelera buscas em uma tabela
        exemplo:
        CREATE INDEX idx_editora ON editora(estado);

    ## Aula 55 - Testando índices com 1 milhão de registros
                
    ## Aula 56 - Excluindo índices
        DROP INDEX 'nome do índice criado';
        
    ## Aula 57 - A cláusula DISTINCT
        traz valores únicos
        exemplo:
        SELECT DISTINCT estado FROM editora; (traz a lista de estados sem repetir)

    ## Aula 58 - Usando o LIMIT
        limitar a quantidade de registros retornados em um select
        exemplo:
        SELECT * FROM editora
        LIMIT 10; (traz os primeiros 10 registros)
        SELECT * FROM livro
        ORDER BY precovenda DESC
        LIMIT 2; (vai trazer os dois livros mais caros)

    ## Aula 59 - Como posso criar subselects? O que eles comem?
        exemplo:
        SELECT l.titulo FROM livro l
        WHERE l.autor_id = (
            SELECT id FROM autor
            WHERE nome = "Dan Brown"
        );

    ## Aula 60 - Exercícios - Lista 8

    ## Aula 61 - Correção de exercícios 
