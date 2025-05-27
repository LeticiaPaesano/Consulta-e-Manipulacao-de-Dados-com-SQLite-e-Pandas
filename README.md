# Consulta e Manipulação de Dados com SQLite e Pandas

Este projeto demonstra como realizar a **integração entre pandas e SQLAlchemy** para criar um banco de dados SQLite em memória, realizar operações de leitura, filtragem, inserção, exclusão e atualização de dados utilizando comandos SQL e a biblioteca `pandas`.

---

## Tecnologias Utilizadas

- **Python**
- **Pandas**
- **SQLAlchemy**
- **SQLite (banco em memória)**

---

## Estrutura do Código

### 1. Importação das Bibliotecas

Importo os módulos necessários para a manipulação de dados com `pandas` e conexão com o banco de dados por meio da `SQLAlchemy`.

### 2. Criação do Banco de Dados

Crio um banco de dados em memória utilizando o seguinte comando:

```python
engine = create_engine('sqlite:///:memory:')
```

### 3. Criação da Tabela

Simulo um conjunto de dados utilizando `pandas.DataFrame` e insiro esses dados na base de dados SQLite com o método `to_sql()`. Essa abordagem permite estruturar os dados de forma tabular e transferi-los diretamente para o banco de dados em memória.

---

### 4. Leitura dos Dados

Realizo consultas SQL diretamente no banco utilizando o método `pandas.read_sql()`, o qual retorna os resultados em formato de `DataFrame`. Isso possibilita a combinação da flexibilidade das consultas SQL com a análise de dados dentro do ambiente Python.

---

### 5. Manipulação com SQL

Aplico as principais operações de SQL diretamente na conexão com o SQLite, por meio de comandos executados via `engine.connect()`:

- **Inserção de novos registros** (`INSERT INTO`)
- **Atualização de valores** (`UPDATE`)
- **Exclusão de dados** (`DELETE`)
- **Filtros com cláusulas** `WHERE`
- **Ordenações com** `ORDER BY`
- **Limitação de resultados com** `LIMIT`

Essas operações são realizadas com foco em simular um fluxo de atualização contínua em um banco relacional.

---

### 6. Atualização e Validação

Após cada operação SQL, realizo uma nova leitura da tabela para validar os efeitos das instruções executadas. Essa etapa garante o acompanhamento preciso das alterações, exibindo os dados atualizados em `DataFrame`.

---

## Objetivo

Este projeto tem como objetivo consolidar conhecimentos práticos sobre:

- Criação e manipulação de bancos SQLite com `SQLAlchemy`
- Execução de comandos SQL diretamente no ambiente `pandas`
- Integração entre análise de dados e bancos relacionais de forma eficiente e didática

## Aprendizado

Durante o desenvolvimento deste projeto, aprendi a:

- Criar um banco de dados `SQLite` em memória com `SQLAlchemy`

- Utilizar `pandas` para executar comandos SQL

- Manipular dados relacionais de forma prática, com recursos avançados de consulta

- Integrar a análise de dados tabulares com a lógica de bancos relacionais
