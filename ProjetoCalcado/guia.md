# 📏 GUIA DE ESTILO SQL

Este guia define os padrões de nomenclatura e organização utilizados no projeto de banco de dados da loja de calçados.

O objetivo é garantir:
- Padronização
- Legibilidade
- Facilidade de manutenção
- Compatibilidade com ferramentas de BI

---

# 1 - Nome de Tabelas

Utilizar sempre nomes no plural e em minúsculo.

## Exemplo:
clientes  
pedidos  
produtos  
vendas  

## Motivo:
Facilita a leitura das consultas SQL e mantém consistência no banco de dados.  
Também é um padrão amplamente utilizado em projetos profissionais e ferramentas como Power BI.

---

# 2 - Nome de Colunas

Utilizar o padrão snake_case (letras minúsculas separadas por underline).

## Exemplo:

id_cliente  
nome_cliente  
data_cadastro  
valor_total  

## Motivo:
Melhora a legibilidade e evita problemas com espaços ou caracteres especiais.  
Além disso, garante compatibilidade entre diferentes bancos de dados.

---

# 3 - Chaves Primárias

Toda tabela deve possuir uma chave primária no formato:

id_nome_da_tabela

## Exemplo:

id_cliente  
id_produto  
id_venda  

## Motivo:
Facilita identificação única dos registros e padroniza relacionamentos.

---

# 4 - Chaves Estrangeiras

Devem seguir o mesmo padrão da chave primária referenciada.

## Exemplo:

id_cliente  
id_produto  

## Motivo:
Facilita entendimento dos relacionamentos entre tabelas.

---

# 5 - Datas

Formato padrão utilizado:

AAAA-MM-DD

## Exemplo:

2026-03-09  

## Motivo:
Segue o padrão internacional ISO, evitando ambiguidades entre dia e mês.  
Compatível com MySQL, PostgreSQL e ferramentas analíticas.

---

# 6 - Valores Monetários

Utilizar o tipo:

DECIMAL(10,2)

## Exemplo:

preco DECIMAL(10,2)  
valor_total DECIMAL(10,2)  

## Motivo:
Evita erros de arredondamento comuns com FLOAT.

---

# 7 - Palavras Reservadas

Utilizar sempre em MAIÚSCULO.

## Exemplo:

SELECT  
FROM  
WHERE  
JOIN  
GROUP BY  
ORDER BY  

## Motivo:
Diferencia comandos SQL dos nomes de tabelas e colunas, melhorando a leitura.

---

# 8 - Alias em Consultas

Utilizar alias curtos e significativos.

## Exemplo:

c → clientes  
v → vendas  
p → produtos  

## Motivo:
Deixa consultas mais limpas e fáceis de entender.

---

# 9 - Organização das Queries

Sempre estruturar queries da seguinte forma:

SELECT  
FROM  
JOIN  
WHERE  
GROUP BY  
ORDER BY  

## Exemplo:

```sql
SELECT c.nome, v.valor_total
FROM vendas v
JOIN clientes c ON v.id_cliente = c.id_cliente
WHERE v.valor_total > 100
ORDER BY v.valor_total DESC;