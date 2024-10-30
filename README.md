# Tratamento de dados utilizando Excel

Conjunto de dados utilizado: https://github.com/AlexTheAnalyst/Excel-Tutorial/blob/main/Data%20Cleaning%20Excel%20Tutorial.xlsx

Objetivo: tratar um Dataset contendo o nome dos presidentes e seus vices, mantendo apenas as informações objetivamente relevantes.

---

### Estrutura primária do dataset:

| Nome da Coluna inicialmente   | Nome da coluna após a renomeação               | Significado                                                                 |
|------------------|------------------------|-----------------------------------------------------------------------------|
| Unnamed: 0       | Índice                 | Índice adicional para identificar a linha        |
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

1 - Colunas desnecessárias e/ou irrelevantes;

2 -  A coluna "Presidente" está com os dados não-padronizados, alguns começam com letra maiúscula e outros com letra minúscula;

3 - Espaços adicionais na coluna "Vice";

4 - Dados incorretos na coluna "Data de criação" e "Data de atualização";

5 - Dados duplicados;

6 - A coluna "Partido" possui dados inconsistentes.

7 - Arredondando a coluna salários e removendo o status "currency" para evitar possíveis problemas de exportação

## 1: Colunas desnecessárias e/ou irrelevantes

O primeiro passo é remover as colunas que são inúteis em relação ao objetivo final, desse modo, as colunas removidas serão:

| Nome da coluna              | Significado                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------|
| Cargo Anterior         | Cargo ou posição ocupada pelo presidente antes de assumir a presidência.    |
| Índice                 | Índice adicional para identificar a linha|


## 2: A coluna "Presidente" está com os dados não-padronizados, alguns começam com letra maiúscula e outros com letra minúscula;

![image](https://github.com/user-attachments/assets/bb006f48-683c-442c-9d79-ec1e6a277a0f)

Para resolver esse problema, basta utilizar a função PRI.MAIÚSCULA() ou PROPER() , resultado:

![image](https://github.com/user-attachments/assets/47de6076-72cd-4018-b063-187abdf9a251)

## 3: Espaços adicionais na coluna "Vice";

Para resolver esse problema, basta utilizar a função ARRUMAR() ou TRIM() 

![image](https://github.com/user-attachments/assets/7f8ad4be-9c02-4766-a983-9767eb40c1cd)

## 4: Dados incorretos na coluna "Data de criação" e "Data de atualização";

Os dados não estão consistentes, alguns estão em formato de "data em texto" e outros em datas puramente numéricas:

![image](https://github.com/user-attachments/assets/d7e87cd4-4e74-4628-921d-06ad364c9199)

Para resolver esse problema:

![image](https://github.com/user-attachments/assets/ad3431b4-562f-49e7-aeff-5dfa366869cc)

Dessa forma, todas as datas passam a ser "abreviadas númericas":

![image](https://github.com/user-attachments/assets/ada86f8a-0202-4900-9fc1-70211e264330)

## 5: Dados duplicados.

Para remover os dados duplicados, utilizaremos uma funcionalidade do próprio Excel chamada "Remover Duplicadas"

![image](https://github.com/user-attachments/assets/3a78ae5c-4090-4735-b518-72bfaff5f745)

![image](https://github.com/user-attachments/assets/9fa1ac5a-77e8-415a-b473-90fc9a86fcea)

## 6: A coluna partido possui dados inconsistentes

## 7: Arredondando a coluna salários e removendo o status "currency" para evitar possíveis problemas de exportação

Basta mudar a tipagem da coluna para "número" e clicar no botão abaixo:

![image](https://github.com/user-attachments/assets/df8b2445-460a-4940-a127-f7c80b65a20a)


