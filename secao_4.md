# Seção 4 - Selecionando e extraindo informações

    ## Aula 24 - Inserindo informações
        - comandos de manipulação de dados
        - insert: comando para inserir dados nas tabelas do banco de dados

    ## Aula 25 - O comando mais badalado so SQL
        - select * from "nome da tabela": visualiza todos os dados da tabela 
        - select * from "nome da tabela" where "coluna"="dado procurado"
        
    ## Aula 26 - Mostrando só alguns campos
        - select "dado pesquisado" from "nome da tabela" where "coluna"="dado procurado"

    ## Aula 27 - Apagando coisas que não preciso
        - delete from "nome da tabela": exclui todos os registros da tabela
        - detele from "nome da tabela" where "nome da coluna"="dado que quer excluir"

    ## Aula 28 - O que é esse tal de Like?
        - select * from "nome da tabela" where "coluna" like "primeira letra%": vai mostrar todos dados que começam com a primeira letra determinada

    ## Aula 29 - Conhecendo o SQLite Studio
        - introdução ao SQLite Studio

    ## Aula 30 - Exercícios Lista 3

    ## Aula 31 - Correção dos exercícios

    ## Aula 32 - Exercícios Lista 4

    ## Aula 33 - Correção dos exercícios

    ## Aula 34 - Colocando em ordem alfabética
        SELECT * FROM 'tabela' ORDER BY 'nome da coluna'; (ordem crescente)
        SELECT * FROM 'tabela' ORDER BY 'nome da coluna' DESC; (ordem decrescente)

    ## Aula 35 - Buscando intervalos de valores
        SELECT * FROM 'tabela' WHERE codigo = 2 OR codigo = 50;
        SELECT * FROM 'tabela' WHERE codigo = 2 OR codigo = 50 OR codigo = 7;
        SELECT * FROM 'tabela' WHERE codigo in (50,2,7,900,4);
        
    ## Aula 36 - Aula importante: Controle de livros
        relacionamento de tabelas
        importância da chave primária na relação de tabelas
        chave primária: código que não se repete em uma base de dados
        chave estrangeira: campo que existe numa tabela 1 e que conecta com o codigo de uma tabela 2
        regras para tabelas: nome da tabela no singular, campo código com nome de 'id', a chave estrangeira será tabela_id

    ## Aula 37 - Exercícios Lista 5

    ## Aula 38 - Correção dos exercícios

    ## Aula 39 - Atualizando informações na tabela
        UPDATE 'tabela que vai alterar' SET 'campo=dado antigo' WHERE  'id do dado que vai alterar';