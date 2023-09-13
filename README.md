# Projeto de PowerBI
Aplicação de uma administradora de condomínios hipotética para análise de
inadimplência condominial e seus impactos.

## Fontes dos dados
- [Base para os condôminos](https://www.kaggle.com/datasets/gauravduttakiit/loan-defaulter) 
- [Base para os condomínios](https://www.kaggle.com/datasets/gohyuchen/singapore-private-condo-rental)

Os demais dados foram gerados aleatoriamente com certas restrições.

## Detalhamento dos dados

- SK_ID_CURR: ID do empréstimo
- TARGET: 0 se o empréstimo foi pago em dia e 1 se o empréstimo não foi pago em dia
- CODE_GENDER: Gênero do cliente
- FLAG_OWN_CAR: Se o cliente possui carro
- FLAG_OWN_REALTY: Se o cliente possui casa
- AMT_INCOME_TOTAL: Renda total do cliente
- CNT_CHILDREN: Número de crianças do cliente
- AMT_CREDIT: Valor do empréstimo
- NAME_INCOME_TYPE: Tipo de renda do cliente
- NAME_EDUCATION_TYPE: Nível de educação do cliente
- NAME_FAMILY_STATUS: Estado civil do cliente
- FLAG_MOBIL: Se o cliente possui celular
- FLAG_PHONE: Se o cliente possui telefone em casa
- FLAG_EMAIL: Se o cliente possui email
- OCCUPATION_TYPE: Ocupação do cliente
- ORGANIZATION_TYPE: Tipo de organização do cliente

## Como utilizar o Power BI com JSON
Modifique a variável `FonteDados` no PowerQuery com o caminho da pasta que
contém o arquivo JSON.

## Como utilizar o Power BI com o Google Sheets
1. Crie uma planilha no Google Sheets com os dados que deseja utilizar
2. Compartilhe a planilha para todos.
3. Copie o link de compartilhamento e cole no Power BI, utilizando o conector
   do Planilhas Google.
4. Entre na conta do Google

| Eu fiz isso no seguinte link: `https://docs.google.com/spreadsheets/d/1vJQwZ7pnIwEPbyXEJKPxb-K2rH0GChVC8YvSePzT9gY/edit?usp=sharing`

## Como utilizar o Power BI com o SQLite
Instale o [ODBC Driver](http://www.ch-werner.de/sqliteodbc/) do SQLite e siga
as instruções de instalação:
![First step](.github/odbc.png)
![Second step](.github/powerbi.png)

| O driver que funcionou bem para mim foi o da [Devart Software](https://marketplace.visualstudio.com/items?itemName=DevartSoftware.SQLiteODBCDriver3264bit).

O campo `Data Source Name` deve ser `SQLite` para funcionar de forma mais automática.
Caso contrário você deve renomear a fonte no Power Query.