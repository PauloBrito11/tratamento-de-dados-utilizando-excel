# Tratamento de dados utilizando Excel

Conjunto de dados utilizado: https://github.com/AlexTheAnalyst/Excel-Tutorial/blob/main/Data%20Cleaning%20Excel%20Tutorial.xlsx

Objetivo: tratar um Dataset contendo o nome dos presidentes e seus vices, mantendo apenas as informações objetivamente relevantes.

---

### Estrutura primária do dataset:

| Nome da Coluna inicialmente   | Nome da coluna após a renomeação               | Significado                                                                 |
|------------------|------------------------|-----------------------------------------------------------------------------|
| Unnamed: 0       | Índice                 | Índice adicional para identificar a linha, possivelmente redundante.        |
| S.No.            | Nº Sequencial          | Número de sequência do presidente na linha do tempo dos mandatos.           |
| president        | Presidente             | Nome do presidente dos Estados Unidos.                                      |
| prior            | Cargo Anterior         | Cargo ou posição ocupada pelo presidente antes de assumir a presidência.    |
| party            | Partido                | Partido político ao qual o presidente era filiado.                          |
| vice             | Vice-presidente        | Nome do vice-presidente que serviu junto ao presidente.                     |
| salary           | Salário                | Salário anual recebido pelo presidente durante o mandato, em dólares.       |
| date updated     | Data de Atualização    | Data da última atualização das informações sobre o presidente.              |
| date created     | Data de Criação        | Data de criação do registro no banco de dados.                              |

---

### O tratamento de dados deve seguir os seguintes princípios:

- Duplicidade
- Consistência
- Completude
- Conformidade
- Integridade

---

### Problemas encontrados nesse dataset:

- A coluna de nomes está com os dados não-padronizados, alguns começam com letra maiúscula e outros com letra minúscula
- Espaços adicionais na coluna "Vice"
- Dados incorretos na coluna "Data de criação" e "Data de atualização"
- Dados duplicados

## Iniciando o processo

O primeiro passo é renomear as colunas, abaixo estão as mudanças realizadas:

[TABELA AQUI]







