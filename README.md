# Projeto de Banco de Dados: E-commerce, Ordem de Serviço e Universidade

## Introdução

Este documento detalha o processo de criação de um projeto de banco de dados para três cenários distintos: E-commerce, Ordem de Serviço e Universidade. O objetivo é descrever como as entidades, relacionamentos e atributos foram definidos com base em requisitos específicos de cada contexto.

## 1. Conceitos Iniciais

Para a construção de qualquer banco de dados eficiente, é essencial o levantamento de requisitos para compreender as necessidades e particularidades do sistema. Um banco de dados relacional foi escolhido, com entidades organizadas em tabelas e relacionamentos que representam as interações entre os dados.

## 2. Estrutura do Projeto

### 2.1 Cenário E-commerce

O projeto de banco de dados para o sistema de E-commerce foi desenvolvido com as seguintes entidades e relacionamentos:

- **Fornecedor**: Armazena os dados dos fornecedores, incluindo ID, Nome e Endereço. Cada fornecedor é responsável pelo fornecimento de um ou mais produtos.
- **Produto**: Contém informações sobre cada item disponível para venda, incluindo ID, Nome, Descrição, Preço e Estoque.
- **Cliente**: Representa os usuários que podem realizar compras, com informações como ID, Nome, Documento e Endereço.
- **Pedido**: Registra cada compra feita por clientes, incluindo data do pedido e status da entrega.

Essas entidades se relacionam da seguinte forma:
- Um **Cliente** pode realizar múltiplos **Pedidos**.
- Um **Pedido** pode conter múltiplos **Produtos**, e cada produto pode estar associado a um único **Fornecedor**.

### 2.2 Cenário Ordem de Serviço

O banco de dados para o sistema de Ordem de Serviço foi modelado para permitir o acompanhamento de pedidos de suporte técnico, onde:

- **Cliente**: Representa os usuários que solicitam serviços ao departamento de helpdesk.
- **Pedido**: Criado pelo cliente, descreve o serviço solicitado e passa por uma análise antes de ser transformado em ordem de serviço.
- **Responsável**: Técnico que analisa e executa o pedido.
- **Ordem de Serviço**: Documento formal que registra as ações a serem executadas pelo técnico.

Os principais relacionamentos incluem:
- O **Cliente** pode realizar um **Pedido**.
- O **Responsável** analisa e executa o **Pedido**, que, se aprovado, é convertido em uma **Ordem de Serviço**.

### 2.3 Cenário Universidade

Este cenário envolve uma estrutura acadêmica mais complexa, com entidades que abrangem alunos, cursos e avaliações:

- **Aluno**: Inclui informações dos estudantes, que podem estar matriculados em múltiplos cursos e disciplinas.
- **Curso**: Representa cada programa oferecido pela universidade, composto por várias disciplinas.
- **Disciplina**: Matérias ministradas em cada curso, algumas das quais possuem pré-requisitos.
- **Professor**: Instrutores responsáveis por ministrar as disciplinas.
- **Avaliação**: Armazena notas e informações sobre o desempenho dos alunos.

Principais relacionamentos:
- Um **Aluno** pode estar matriculado em um ou mais **Cursos**.
- Um **Curso** possui várias **Disciplinas**, e cada disciplina é ministrada por um único **Professor**.
- As **Avaliações** registram o desempenho dos alunos nas disciplinas.

## 3. Ferramentas Utilizadas

Para a criação dos modelos, foram utilizadas as seguintes ferramentas:
- **MySQL Workbench**: Para a implementação e execução do modelo.


### 3.1 Instalando o MySQL Workbench

Para usuários que desejam instalar o MySQL Workbench, o download está disponível em [MySQL Workbench](https://dev.mysql.com/downloads/workbench/).

## 4. Modelos de Cenário

Cada um dos cenários foi representado graficamente para facilitar a visualização das entidades e seus relacionamentos:

- **E-commerce**: Relacionamento entre clientes, fornecedores, produtos e pedidos.
- **Ordem de Serviço**: Fluxo desde a solicitação do cliente até a execução da ordem de serviço.
- **Universidade**: Gerenciamento das relações entre alunos, cursos, disciplinas e professores.

## Conclusão

O desenvolvimento deste projeto de banco de dados demonstrou a importância de um planejamento cuidadoso, considerando as particularidades de cada cenário para garantir um sistema eficiente. Um banco de dados bem estruturado permite uma melhor organização e acessibilidade das informações, facilitando o uso do sistema.
