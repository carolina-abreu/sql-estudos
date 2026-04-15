# Seção 5 - As tabelas também se relacionam

    ## Aula 40 - Vamos fazer nosso primeiro JOIN
        união de informação de tabelas diferentes
        se concentrar na pergunta
        onde estão as respostas?
        como elas se ligam?
        como fazer um join:
            1. escreva select com o from de todas as tabelas que precisa
            2. adicione um apelido para cada tabela
            3. faça ligações com cuidado
            4. adicione outras restrições se necessário
            exemplo: 
            SELECT l.titulo, a.nome
            FROM livro l, autor a
            WHERE a.id = l.autor_id;

    ## Aula 41 - Mais um JOIN para você entender
        exemplo: 
        SELECT l.titulo, a.nome
        FROM livro l, editora e
        WHERE e.id = l.editora_id;

    ## Aula 42 - Que tal ligarmos agora 3 tabelas?
        exemplo:
        SELECT l.titulo, a.nome, e.nome
        FROM livro l, autor a, editora e
        WHERE l.autor_id = a.id
        AND l.editora_id = e.id;

    ## Aula 43 - Além do JOIN, vamos restringir um pouco mais?
        exemplo:
         SELECT l.titulo, e.nome, e.estado
         FROM livro l, editora e
         WHERE e.id = l.editora_id
         AND e.estado = "PR"

    ## Aula 44 - Exercícios Lista 6

    ## Aula 45 - Correção dos Exercícios
