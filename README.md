📦 Sistema de Vendas - Database Project
🎯 Sobre o Projeto
Este projeto consiste em um banco de dados relacional completo para um sistema de vendas, desenvolvido como parte de um desafio técnico para demonstrar conhecimentos em modelagem de dados, criação de índices e desenvolvimento de stored procedures.

O sistema gerencia todo o ciclo de vendas, desde o cadastro de produtos e clientes até o acompanhamento de pedidos, entregas e controle de estoque, incluindo integração com vendedores terceiros.

🏗️ Estrutura do Banco de Dados
Principais Entidades
Cliente: Pessoas físicas e jurídicas que realizam compras

Produto: Catálogo de produtos com preços e categorias

VendedorTerceiro: Parceiros comerciais que fornecem produtos

Pedido: Registro das vendas realizadas

FormaPagamento: Métodos de pagamento aceitos

Estoque: Controle de localizações e quantidades

Entrega: Acompanhamento de envios e rastreamento

Relacionamentos Principais
Um cliente pode ter múltiplos pedidos

Um pedido contém múltiplos produtos (N para N)

Produtos podem ser fornecidos por múltiplos vendedores terceiros

Produtos podem estar em múltiplos estoques

🚀 Funcionalidades Implementadas
1. Índices Otimizados (indices.sql)
Estratégia de índices para garantir performance nas consultas mais frequentes:

sql
-- Índice para agrupamento de funcionários por departamento
CREATE INDEX idx_employees_department ON employees(department_id);

-- Índice HASH para buscas exatas por cidade
CREATE INDEX idx_departments_city_hash ON departments(city) USING HASH;
2. Stored Procedures (procedures.sql)
Procedures completas para manipulação de dados com controle de fluxo:

sp_GerenciarCliente - CRUD completo de clientes

sp_GerenciarProduto - Gestão de produtos

sp_GerenciarPedido - Controle de pedidos

sp_GerenciarEstoque - Transferência entre estoques

sp_RelatoriosGerenciais - Consultas analíticas

📊 Consultas Otimizadas
O projeto inclui consultas SQL otimizadas para:

Departamento com maior número de funcionários

Departamentos agrupados por cidade

Relação completa de empregados por departamento

Relatórios de vendas e performance

🛠️ Tecnologias Utilizadas
MySQL 8.0+ - Sistema de Gerenciamento de Banco de Dados

SQL - Linguagem de consulta estruturada

Stored Procedures - Lógica de negócios no banco de dados

Índices - B-Tree, HASH e compostos
