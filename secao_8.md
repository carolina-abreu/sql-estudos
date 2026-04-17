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

    ## Aula 64 - Um exemplo de uso de transações

    ## Aula 65 - O que é um OUTER JOIN?

    ## Aula 66 - Trabalhando com TRIGGERS

    ## Aula 67 -  Vamos criar uma trigger de AUDITORIA no Controle de Livros

    ## Aula 68 - Exercícios - Lista 9

    ## Aula 69 - Correção de exercícios
