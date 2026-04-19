# Seção 8 - Isso está muito fácil, quero recursos avançados!

    ## Aula 62 - 14 funções que você um dia pode precisar
        - IFNULL: não retorna valores vazios, pode ser substituido por uma frase
        SELECT titulo, IFNULL(estilo_id, "Falta Código de Estilo") FROM livro;
        - LENGTH: tamanho
        SELECT titulo 
        LENGTH (titulo) AS "Tamanho do Titulo"
        FROM livro WHERE id=1;
        - LOWER: trazer as informações em letra minúscula
        SELECT LOWER (titulo) FROM livro WHERE id=1;
        - UPPER: trazer informações em letra maiúscula
        SELECT UPPER (titulo) FROM livro WHERE id=1;
        - SUBSTR(x,y,z): extrair uma parte da informação
        SELECT SUBSTR("Curso de SQL",3,3); resultado: rso, três letras a partir da terceira posição
        - RANDOM: gera número aleatório
        SELECT titulo, substr(random(),3,3) AS codigo_inventado 
        FROM livro; resultado: gera um código inventado de 3 caracteres
        - THE REPLACE (x,y,z): substitui
        SELECT REPLACE ("Curso de SQL"," ","---"); resultado: troca o texto por ---
        - ROUND(X): arrendonda casas decimais
        SELECT titulo, precovenda FROM livro;
        SELECT titulo, ROUND(precovenda,1) FROM livro;
        - TRIM(): remove espaços do início ao fim
        SELECT TRIM ("   Curso     de      S  Q  L.   "); resultado:Curso     de      S  Q  L.
        - RTRIM(): remove espaços no final
        SELECT RTRIM ("   Curso     de      S  Q  L   ");
        resultado:   Curso     de      S  Q  L .
        - LTRIM(): remove espaços no início
        SELECT LTRIM ("   Curso     de      S  Q  L.   "); 
        resultado:Curso     de      S  Q  L.    "
        - TYPEOFF(): retorna o tipo da variável 
        SELECT TYPEOF(1); resultado: int
        SELECT TYPEOF(1.1); resultado: real
        SELECT TYPEOF(" "); resultado: text
        - DATE ('NOW'): retorna a data 
        SELECT DATE ('now');
        - SQLITE VERSION: retorna a versão do sqlite que estamos trabalhando
        SELECT SQLITE_VERSION();

    ## Aula 63 - Entendendo as transações no banco de dados
        tudo que acontece dentro de uma transsção pode ser aceito ou revertido
        exemplo: software de automação comercial, que controla clientes, estoque, fornecedores, vendas. faça uma venda com entrada + 3 parcelas
        - lança no caixa a entrada R$100
        - gera as parcelas de 3xR$50,00
        - baixa o estoque -1
        - histórico do cliente
        - fim da transação
        caso a transação dê algum erro durante o processo, tem que cancelar a transação completa e começar de novo
        - a transação começa com o begin e termina com o commit (registra a transação), ou rollback (cancela a transação e inicia novamente)

    ## Aula 64 - Um exemplo de uso de transações
        begin transaction;
        insert into autor (id,nome) values (7,"Tiago");
        rollback; (o rollback cancelou a transação e não vai inserir o autor)
        begin transaction;
        insert into autor(id,nome) values (8,"Thiago");
        commit; (o commit finaliza a transação e o autor vai ser inserido na tabela)

    ## Aula 65 - O que é um OUTER JOIN?
        -join = ligação entre as tabelas
        -inner join = traz o resultado somente quando a condição é satisfeita de ambos os lados, ou seja, não vai trazer os títulos de livros que tem o estilo vazio
        exemplo: dois jeitos de fazer 
        SELECT l.titulo, e.nome
        FROM livro l, estilo e
        WHERE e.id = l.estilo_id;
        maneira tradicional de trabalhar:
        SELECT titulo, nome
        FROM estilo INNER JOIN livro
        ON estilo.id = livro.estilo_id;
        - outer join = left outer join: mostra mesmo que esteja null
        exemplo
        SELECT titulo, nome
        FROM livro LEFT OUTER JOIN estilo
        ON estilo.id = livro.estilo_id; (traz todos os livros com estilos, mesmo livros com estilos vazios)

    ## Aula 66 - Trabalhando com TRIGGERS
        trigger: algo que acontece em determinado evento
        podem ser disparador por enventos como delete, insert, update. Executam antes ou depois do evento. Usado em tabelas de auditoria, usado para rastrear mudanças.

    ## Aula 67 -  Vamos criar uma trigger de AUDITORIA no Controle de Livros: exemplo do uso da trigger
        - registrar sempre que um novo autor for cadastrado, guardar a data
        - vamos criar a tabela auditoria
        CREATE TABLE auditoria (autor_id int, data date, acao text);
        - vamos criar a trigger de auditoria
        CREATE TRIGGER auditoria AFTER INSERT ON autor
        BEGIN
            INSERT INTO auditoria (autor_id, data, acao) 
            VALUES (new,id, datetime('now'), "Autor inserido");
        END;
        - para excluir a trigger: DROP TRIGGER 'nome da trigger';
        - trigger impacta na velocidade das operações no banco de dados;
        
    ## Aula 68 - Exercícios - Lista 9

    ## Aula 69 - Correção de exercícios
