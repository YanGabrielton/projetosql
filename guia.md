GUIA DE ESTILO SQL

1 - Nome de tabelas
Utilizar plural e minúsculo.

Exemplo:
clientes
pedidos
produtos

Motivo:
Facilita leitura e padroniza consultas em ferramentas de BI.

2 - Nome de colunas

Utilizar snake_case.

Exemplo:

id_cliente
nome_cliente
data_cadastro

Motivo:
Melhora legibilidade e evita problemas com espaços.

3 - Datas

Formato padrão utilizado:

AAAA-MM-DD

Exemplo:

2026-03-09

Motivo:
Formato padrão ISO utilizado pela maioria dos bancos de dados e ferramentas analíticas.

4 - Palavras reservadas

Utilizar sempre em MAIÚSCULO.

Exemplo:

SELECT
FROM
WHERE
JOIN

Motivo:
Diferenciar comandos SQL de nomes de colunas.
