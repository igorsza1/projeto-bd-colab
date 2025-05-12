
# Projeto de Banco de Dados com SQLite

Este projeto foi desenvolvido como parte da disciplina de Modelagem de Dados, com o objetivo de praticar os conceitos de modelagem, criação de tabelas, inserção de dados, consultas SQL e uso do SQLite.

## 💻 Sobre o Projeto

Ele importa as bibliotecas sqlite3 (para interagir com o SQLite) e os (para operações de sistema, como remover arquivos). Define o nome do arquivo do banco de dados como loja.db. Verifica se o arquivo loja.db já existe e o remove para garantir que cada execução comece com um banco de dados limpo. Estabelece uma conexão com o banco de dados loja.db. Se o arquivo não existir, o SQLite o cria automaticamente.

Além da parte prática com SQL, também elaborei um diagrama ER para representar as entidades do sistema e seus relacionamentos.

## 📁 Estrutura do Projeto

- `notebook_banco_de_dados.ipynb`: notebook com toda a lógica de criação do banco, inserções e consultas.
- `README.md`: este arquivo, com um resumo do projeto.
- `modelo_conceitual.png`: imagem do diagrama ER com as entidades e relações do banco de dados.

## 📊 Tabelas Criadas

O código cria três tabelas: Clientes: Armazena informações básicas dos clientes (ID, nome, e-mail). O id é a chave primária (PRIMARY KEY). Produtos: Armazena detalhes dos produtos (ID, nome do produto, preço). O id é a chave primária. Vendas: Registra as transações de vendas (ID da venda, ID do cliente, ID do produto, quantidade e data da venda). Esta tabela possui duas chaves estrangeiras (FOREIGN KEY): id_cliente que se refere ao id da tabela Clientes e id_produto que se refere ao id da tabela Produtos. Isso estabelece um relacionamento entre as tabelas. Após a criação das tabelas, as alterações são salvas no banco de dados (conn.commit()).


## 🔍 Consultas SQL

O código realiza diversas consultas SQL para demonstrar a recuperação de dados: Consulta Simples (Clientes): Seleciona e exibe todos os registros da tabela Clientes. Consulta Simples com Condição (Produtos): Seleciona e exibe produtos cujo preço é superior a R$ 200,00. Consulta com JOIN (Vendas Detalhadas): Esta é uma consulta mais avançada. Ela une as tabelas Vendas, Clientes e Produtos para exibir informações detalhadas de cada venda, incluindo o nome do cliente e o nome do produto, além do valor total da venda (quantidade * preço unitário). Os resultados são ordenados pela data da venda. Consulta com JOIN e WHERE (Produtos de um Cliente Específico): Encontra e exibe os nomes dos produtos distintos que foram comprados por "Ana Silva", mostrando como filtrar resultados através de relações de tabela. Consulta de Agregação (Total Gasto por Cliente): Calcula e exibe o valor total gasto por cada cliente, usando as funções SUM e GROUP BY para agregar os dados de vendas por cliente. Os resultados são ordenados pelo gasto total em ordem decrescente.

## 🧠 Aprendizados

Esse exercício me ajudou a reforçar bastante o entendimento de como os dados se relacionam num banco, além de como usar JOINs para trazer informações mais completas. Também entendi melhor como modelar entidades e transformar isso em um banco funcional com chaves estrangeiras.

## 🗂️ Versão no GitHub

O projeto foi versionado manualmente no GitHub, com os arquivos `.ipynb`, `.md` e imagem do modelo conceitual.

Após cada operação de consulta (SELECT), os dados recuperados do banco de dados são iterados e impressos diretamente na tela do Google Colab, ou seja, na saída da célula de código.

## ✅ Fechamento da Conexão:

Finalmente, a conexão com o banco de dados é fechada (conn.close()). Isso é importante para liberar os recursos do sistema e garantir que todas as alterações sejam salvas de forma definitiva.

