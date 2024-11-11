# Normalização de Bases de Dados

A **normalização** é um processo essencial na modelagem de bases de dados relacionais, que visa organizar os dados de forma eficiente, evitando redundâncias e inconsistências. Este conceito foi introduzido por **Edgar Codd** na década de 1970, como parte da sua teoria dos modelos relacionais. A normalização divide os dados em várias tabelas para garantir que cada tabela contenha informações semanticamente coerentes, sem duplicação desnecessária.

## Contributo de Edgar Codd

Edgar Codd foi um matemático e informático britânico, responsável pela introdução da teoria dos modelos relacionais. A sua obra *"A Relational Model of Data"* (1970) propôs uma forma de organizar dados em tabelas inter-relacionadas, visando evitar a redundância de informações e facilitar as consultas. A normalização é um dos pilares da sua teoria.

## Conceitos-chave

### 1. Regras de Normalização
As regras de normalização, também conhecidas como **formas normais**, são princípios que devem ser seguidos para garantir uma estrutura de dados eficiente e sem redundâncias. As formas normais mais comuns incluem:

- **1ª Forma Normal (1NF)**: Todos os atributos devem ser atômicos e a tabela não pode conter grupos repetitivos.
- **2ª Forma Normal (2NF)**: A tabela deve estar em 1NF e não pode haver dependências parciais (atributos não-chave devem depender totalmente da chave primária).
- **3ª Forma Normal (3NF)**: A tabela deve estar em 2NF e não pode haver dependências transitivas (atributos não-chave não podem depender uns dos outros).

### 2. Dependências Funcionais
As **dependências funcionais** referem-se à relação entre atributos em que um atributo (ou um conjunto de atributos) determina outro. Por exemplo, se o número de identificação de um funcionário é conhecido, podemos determinar o nome desse funcionário.

### 3. Tabelas
As **tabelas** são as unidades principais de armazenamento de dados em um banco de dados relacional. Cada tabela é composta por linhas (tuplas) e colunas (atributos).

### 4. Atributos
Os **atributos** são as colunas das tabelas, representando as características dos dados. Por exemplo, em uma tabela de clientes, os atributos podem ser **nome**, **endereço**, **telefone**, etc.

### 5. Desnormalização
A **desnormalização** é o processo de introduzir redundâncias de dados para melhorar o desempenho em consultas específicas. Embora a normalização elimine redundâncias, a desnormalização pode ser necessária quando a performance de leitura é mais importante que a eficiência de armazenamento.

## Exemplos de Normalização

### Exemplo de Tabela Não Normalizada

| ID  | Nome    | Endereço        | Cidade | Código Postal |
|-----|---------|-----------------|--------|---------------|
| 1   | João    | Rua A, 123      | Lisboa | 1000-001      |
| 2   | Maria   | Rua B, 456      | Porto  | 2000-002      |
| 3   | João    | Rua A, 123      | Lisboa | 1000-001      |

Nesta tabela, os dados de João são repetidos, gerando redundância.

### Exemplo de Normalização (1ª Forma Normal)

| ID  | Nome    | Endereço        | Cidade | Código Postal |
|-----|---------|-----------------|--------|---------------|
| 1   | João    | Rua A, 123      | Lisboa | 1000-001      |
| 2   | Maria   | Rua B, 456      | Porto  | 2000-002      |

Aqui, removemos a duplicação de dados e a tabela está em **1ª Forma Normal**.

### Exemplo de Normalização (2ª Forma Normal)

**Tabela 1:**

| ID  | Nome    | Endereço        |
|-----|---------|-----------------|
| 1   | João    | Rua A, 123      |
| 2   | Maria   | Rua B, 456      |

**Tabela 2:**

| Cidade | Código Postal |
|--------|---------------|
| Lisboa | 1000-001      |
| Porto  | 2000-002      |

Aqui, os dados são divididos em duas tabelas para eliminar dependências parciais, com base na **2ª Forma Normal**.

### Exemplo de Desnormalização

| ID  | Nome    | Endereço        | Cidade | Código Postal |
|-----|---------|-----------------|--------|---------------|
| 1   | João    | Rua A, 123      | Lisboa | 1000-001      |
| 2   | Maria   | Rua B, 456      | Porto  | 2000-002      |
| 3   | João    | Rua A, 123      | Lisboa | 1000-001      |

Na **desnormalização**, a redundância é introduzida para otimizar o desempenho de leitura.

## Conclusão

A **normalização** é um processo crucial para garantir a integridade e eficiência dos dados em um banco de dados relacional. O trabalho de Edgar Codd revolucionou a forma como os dados são armazenados e manipulados. No entanto, em situações onde a performance é crítica, a **desnormalização** pode ser uma estratégia útil.

---

## Referências

- **Codd, E. F.** (1970). A Relational Model of Data for Large Shared Data Banks.
