# Seção 6 - Aprendendo COUNT, MIN, MAX e AVG
    
    ## Aula 46 - Vamos contar
        função que faz contagem 
        COUNT
        exemplo:
        SELECT COUNT (*) as "Total"
        FROM editora
        WHERE estado = "MG"

    ## Aula 47 - Tirando a média
        AVG - average (média)
        exemplo:
        SELECT AVG(precovenda) "Média"
        FROM livros;

    ## Aula 48 - Encontrando valores maiores e menores
        pode ser usado para descobrir o último id
        exemplo:
        - SELECT MAX (precovenda)
          FROM livro;
        - SELECT MIN (precovenda)
          FROM livro;
        - SELECT max (id)
          FROM editora; 

    ## Aula 49 - A cláusula group by e menores
        faz a contagem agrupada
        exemplo:
        - SELECT estado, count (*) as "Total"
          FROM editora
          GROUP BY estado; (conta quantas vezes cada estado aparece na base de dados)
        - SELECT estado, count (*) as "Total"
          FROM editora
          GROUP BY estado
          HAVING count (*) < 30 (conta quantas vezes cada estado aparece, mas mostra somente os menores que )
          
    ## Aula 50 - Exercícios Lista 7

    ## Aula 51 - Correção dos Exercícios 
