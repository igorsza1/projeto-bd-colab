
# Projeto de Banco de Dados com SQLite

Este projeto foi desenvolvido como parte da disciplina de Modelagem de Dados, com o objetivo de praticar os conceitos de modelagem, criação de tabelas, inserção de dados, consultas SQL e uso do SQLite.

## 💻 Sobre o Projeto

A proposta foi construir um banco de dados simples, mas funcional, utilizando o SQLite e integrando várias tabelas relacionadas. O foco foi simular um cenário de vendas, com clientes, itens, compras, fornecedores, promoções e estoque.

Além da parte prática com SQL, também elaborei um diagrama ER para representar as entidades do sistema e seus relacionamentos.

## 📁 Estrutura do Projeto

- `notebook_banco_de_dados.ipynb`: notebook com toda a lógica de criação do banco, inserções e consultas.
- `README.md`: este arquivo, com um resumo do projeto.
- `modelo_conceitual.png`: imagem do diagrama ER com as entidades e relações do banco de dados.

## 📊 Tabelas Criadas

1. **clientes**
   - id (PK)
   - nome
   - idade

2. **itens**
   - id (PK)
   - descricao
   - quantidade
   - precocompra

3. **compras**
   - idcompra (PK)
   - idCliente (FK)
   - idItem (FK)
   - quantidade
   - precovenda

4. **fornecedores**
   - id (PK)
   - nome
   - contato

5. **estoques**
   - idItem (PK, FK)
   - quantidade_estoque

6. **promocoes**
   - id (PK)
   - descricao
   - desconto
   - validade

## 🔍 Consultas SQL

No notebook, executei diversas consultas como:

- Seleção simples de dados
- JOINs entre tabelas
- Filtros com WHERE e ORDER BY
- Agrupamento com GROUP BY e HAVING
- Atualizações e exclusões de dados
- Geração de relatórios detalhados

## 🧠 Aprendizados

Esse exercício me ajudou a reforçar bastante o entendimento de como os dados se relacionam num banco, além de como usar JOINs para trazer informações mais completas. Também entendi melhor como modelar entidades e transformar isso em um banco funcional com chaves estrangeiras.

## 🗂️ Versão no GitHub

O projeto foi versionado manualmente no GitHub, com os arquivos `.ipynb`, `.md` e imagem do modelo conceitual.