# Desafio Técnico Frontend - Dashboard Financeiro

## 🎯 Objetivo

Olá, candidato(a)!

Este desafio foi projetado para avaliarmos suas habilidades e fundamentos em desenvolvimento frontend. Queremos entender como você estrutura um projeto, escreve código, lida com dados assíncronos e documenta seu trabalho.

O objetivo não é apenas "entregar a funcionalidade", mas demonstrar sua proficiência em boas práticas, arquitetura de software e sua capacidade de tomar decisões técnicas sólidas, independentemente da ferramenta escolhida.

## 📝 A Tarefa (Aplicação)

Você deve criar um pequeno dashboard para visualização de transações financeiras. A aplicação deverá consumir dados de uma API mock (detalhada abaixo) e exibi-los de forma clara e interativa para o usuário.

### Funcionalidades Essenciais

1.  **Listagem de Transações:**
    * Exibir uma lista com todas as transações recebidas da API.
    * Cada item da lista deve mostrar, no mínimo: a descrição, a categoria, o valor e a data da transação.
    * O valor da transação deve ser formatado como moeda local (ex: R$).
    * Transações com o tipo `expense` (despesa) devem ter seu valor exibido com uma cor distinta (ex: vermelho) e um sinal de negativo. Transações do tipo `income` (receita) devem ter outra cor (ex: verde).

2.  **Resumo Financeiro:**
    * Em um local de destaque na página (como um cabeçalho), deve haver um resumo com:
        * O total de receitas (`income`).
        * O total de despesas (`expense`).
        * O saldo total (receitas - despesas).

3.  **Filtro de Transações:**
    * Adicionar um campo de texto que permita ao usuário filtrar as transações em tempo real pela sua **descrição**.

## 📝 A Tarefa (API)

Para simplificar, você não precisará construir um backend. Recomendamos o uso do `json-server` para criar uma API REST local a partir de um arquivo `db.json`.

Crie um arquivo `db.json` na raiz do seu projeto com a seguinte estrutura de dados:

```json
{
  "transactions": [
    {
      "id": 1,
      "description": "Salário Mensal",
      "category": "Salário",
      "price": 5500.00,
      "type": "income",
      "createdAt": "2025-08-01T10:00:00Z"
    },
    {
      "id": 2,
      "description": "Aluguel",
