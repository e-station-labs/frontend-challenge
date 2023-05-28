# 🚀 Front-end Challenge

Bem-vindo(a)!

Este é o desafio Front-end!

O objetivo deste desafio é avaliar suas habilidades de programação.

Quando sua solução estiver pronta, basta responder o e-mail que recebeu com o link do seu repo aqui no Github!

Em seguida, enviaremos o feedback e as instruções dos próximos passos!

Caso tenha alguma dúvida, nós estamos disponíveis no email *marcos@e-station.io*

Bom desafio!

> ⚠️ **É importante que o seu repo esteja público, caso contrário não iremos conseguir avaliar sua resposta**

# 🧠 Contexto

O desafio será implementar um dashboard com dados de medição de energia elétrica que deverá ter as seguintes funcionalidades:
- [ ] Uma visão comparando o consumo mês a mês entre os anos de 2021 e 2022
- [ ] Uma visão exibindo apenas as medições hora a hora com base no dia, mês e ano selecionados
- [ ] Uma visão com as medições horárias da última semana
- [ ] Uma tabela com a relação de medições que permita:
  - [ ] Filtrar medições por período
  - [ ] Paginação dos resultados retornados
  - [ ] Ordenação pelos campos: Agente, Ponto, Data, Hora, Consumo Ativo (MWh) e Origem

![Protótipo](./images/dashboard.png)

### Visão: Consumo Anual

Os dados devem ser exibidos considerando o consumo completo de um determinado mês, comparando ao mesmo mês do ano anterior.

Lembre-se que, os dados disponíveis para o desafio estão fragmentados por hora, ou seja, você deverá realizar a consolidação para esse comparativo.

### Visão: Medição Horária (Por Dia)

Em nosso dashboard, o gestor pode selecionar um determinado dia, mês e ano para avaliar as medições coletadas hora a hora no intuito de verificar se estão de acordo com o esperado.

Para esse desafio, você deve considerar que o volume contratado foi de exatamente **100 MWh**, com flexibilidade de 10%, ou seja, o consumo deve ir de 90 a 110 MWh, sendo 100 MWh o consumo flat, nem abaixo e nem acima do contratado.

### Visão: Medição Histórica (Última Semana)

Assim como na anterior, você deverá exibir os valores por hora. No entanto, para essa visão, desconsidere a flexibilidade e exiba apenas os dados dos últimos 7 dias disponíveis no arquivo de dados.

### Visão: Medições

Para essa visão, você deverá criar uma tabela simples que disponha as medições.

A tabela deve permitir: Ordenação, Filtragem (por período) e Páginação. Existem + 17k registros, atente-se para questões de performance.

## 📋 Instruções ReactJS

Chegou a hora de colocar a mão na massa!

- Siga [esse protótipo](./images/dashboard.png) como referência para o que irá construir
- Utilize Next.js e Typescript
- Faça a estilização com Tailwind
- Utilize uma biblioteca de gráficos a sua escolha
- Por favor, inclua no README com as instruções de instalação do projeto
- Sinta-se livre para incluir quaisquer observações
- Para cada uma das 4 visões do dashboard, considere que será utilizada uma API específica e por isso, em cada uma delas adicione: Um estado de *loading* usando Skelethon e um estado de erro para melhorar a experiência do usuário

## Dados de API

Os dados necessários para compor o dashboard, encontram-se em um arquivo `.json` no repositório do desafio.

Mantenha o foco na construção da interface e em seus respectivos comportamentos, este é um desafio de Front-end, por isso, sinta-se a vontade para usar bibliotecas como [JSON Server](https://www.npmjs.com/package/json-server) para expor uma API fake com base no JSON disponível.

No arquivo, você encontrará medições (hora a hora) dos anos 2021 e 2022, este é um exemplo:

```json
{
    "id": "6ca9116e-1751-4b8f-b716-a3f12632d13a",
    "reference": "31/12/2022",
    "year": 2022,
    "month": 12,
    "day": 31,
    "hour": 1,
    "consumption": 107.782849,
    "agent": "E-STATION",
    "meter": "STSTSTSTSTSTST",
    "origin": "COLETA DIÁRIA",
    "intervalInMinutes": 60,
    "isEstimated": false
}
```

## ✔️ Critérios de Avaliação

Além dos requisitos levantados acima, iremos olhar para os seguintes critérios durante a correção do desafio:

- Gerenciamento de estado
- Componentização
- Responsividade
- Preocupação com usabilidade
- Preocupação com acessibilidade
- Testes de Unidade e E2E
- Padrões de código
- Padrão de commits (_Conventional_)
- Outros...

## 😎 Seria legal
- Fazer deploy na Vercel ou em outro local de sua preferência e disponibilizar um link de visualização
- Utilização de cache do Next.js
