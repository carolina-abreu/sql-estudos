1) Conte o número de editoras cadastradas
    **solução**
    SELECT count (*) "Total"
    FROM editora;

2) Calcule a média do preço de venda dos livros
    **solução**
    SELECT avg(precovenda) "Média"
    FROM livro;

3) Atualize o preço de venda do livro 1 aumentando seu valor em 7%
    **solução**
    UPDATE livro
    SET precovenda = precovenda + (precovenda * 0.07)
    WHERE id = 1;

4) Conte a quantidade de editoras de MG.
    **solução**
    SELECT COUNT (*) as "Total"
    FROM editora
    WHERE estado = "MG"
    
5) Conte o número de editoras agrupando por estado.
    **solução**
    SELECT estado, count (*) as "Total"
    FROM editora
    GROUP BY estado;    
    
6) Diminua o preço de todos os livros da editora 1 em 19%.
    **solução**
    UPDATE livro
    SET precovenda = precovenda - (precovenda * 0.19)
    WHERE editora_id = 1;

7) Qual o maior código de autor cadastrado?
    **solução**
    SELECT max (id)
    FROM autor;

8) Qual o menor código de autor cadastrado?
    **solução**
    SELECT min (id)
    FROM autor;
    
9) Conte o número de editoras, agrupando por estado e somente para estados que tenham 40 ou mais editoras.
    **solução**
    SELECT estado, count (*) as "Total"
    FROM editora
    GROUP BY estado
    HAVING count (*) >= 40; 

10) Aumente o preço de todos os livros em 7,5%
    **solução**
    UPDATE livro
    SET precovenda = precovenda + (precovenda * 0.075);

11) Exclua todas as editoras do estado DF.
    **solução**
    DELETE FROM editora
    WHERE estado = "DF";

12) Os livros podem ser vendidos em 3 parcelas sendo a primeira parcela 30% do valor do livro e a segunda e terceira sendo 35% cada. Faça um select que mostre o nome do livro juntamente com o preço dele
e os valor das parcelas.
    **solução**
    SELECT titulo, ROUND(precovenda,2),
    ROUND(precovenda*0.3,2) AS "Parcela 1",
    ROUND(precovenda*0.35,2) AS "Parcela 2",
    ROUND(precovenda*0.35,2) AS "Parcela 3"
    FROM livro;

13) Todas as editoras do DF mudaram para GO. Atualize no banco de dados por favor!
    **solução**
    UPDATE editora
    SET estado = "GO"
    WHERE estado = "DF";
    
14) Quantas editoras temos em cidades que começam pela letra M?
    **solução**
    SELECT COUNT(*)
    FROM editora
    WHERE cidade like "M%";
    
15) Altere o preço de todos os livros dando um desconto de 6% 
    **solução**
    UPDATE livro
    SET precovenda = precovenda - (precovenda * 0.06);