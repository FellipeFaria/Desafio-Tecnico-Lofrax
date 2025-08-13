# Desafio Técnico Frontend - Dashboard Financeiro

## Objetivo

Olá, candidato(a)!

Este desafio foi projetado para avaliarmos suas habilidades e fundamentos em desenvolvimento frontend. Queremos entender como você estrutura um projeto, escreve código, lida com dados assíncronos e documenta seu trabalho.

O objetivo não é apenas "entregar a funcionalidade", mas demonstrar sua proficiência em boas práticas, arquitetura de software e sua capacidade de tomar decisões técnicas sólidas, independentemente da ferramenta escolhida.

##  A Tarefa (Aplicação)

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

## A Tarefa (API)

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
      "category": "Moradia",
      "price": 1200.00,
      "type": "expense",
      "createdAt": "2025-08-03T14:30:00Z"
    },
    {
      "id": 3,
      "description": "Supermercado",
      "category": "Alimentação",
      "price": 450.50,
      "type": "expense",
      "createdAt": "2025-08-05T18:45:00Z"
    },
    {
      "id": 4,
      "description": "Venda de item usado",
      "category": "Venda",
      "price": 300.00,
      "type": "income",
      "createdAt": "2025-08-06T11:00:00Z"
    },
    {
      "id": 5,
      "description": "Conta de Internet",
      "category": "Contas",
      "price": 99.90,
      "type": "expense",
      "createdAt": "2025-08-10T09:00:00Z"
    },
    {
      "id": 6,
      "description": "Restaurante",
      "category": "Lazer",
      "price": 100.10,
      "type": "expense",
      "createdAt": "2025-08-11T20:15:00Z"
    }
  ]
}
```

**Endpoint a ser consumido:**
* `GET /transactions`: Retorna a lista completa de transações.
* **Observação:** O resumo financeiro (`income`, `expense`, `total`) deverá ser **calculado no frontend** a partir da lista de transações.

## 🛠 Requisitos Técnicos

* **Linguagem/Framework:** **Você tem total liberdade para escolher a tecnologia!** Pode usar JavaScript puro, TypeScript, ou qualquer framework/biblioteca que preferir (React, Vue, Angular, Svelte, Solid, etc.). A avaliação será focada nos conceitos e fundamentos, não na ferramenta.
* **Versionamento:** O projeto deve ser versionado com **Git** e hospedado em um repositório público (GitHub, GitLab, etc.). Seu histórico de commits será avaliado.
* **Estilização:** Você também tem liberdade para escolher a abordagem de estilização: CSS puro, pré-processadores (Sass/SCSS), CSS-in-JS (Styled Components, Emotion), ou frameworks de CSS (Tailwind CSS, Bootstrap).
* **Testes:** A qualidade do software é fundamental. Escreva testes que julgar pertinentes para garantir o funcionamento da aplicação (ex: testes unitários para funções de cálculo/formatação, e testes de integração/componente para as funcionalidades principais).

## O que será Avaliado

Não existe uma "solução perfeita". Estamos interessados em ver como você aborda o problema. Seus principais pontos de avaliação serão:

1.  **Arquitetura e Estrutura do Projeto:**
    * Organização de pastas e arquivos de forma lógica e escalável.
    * Clara separação de responsabilidades (componentes, lógica de negócio, acesso a dados, etc.).

2.  **Qualidade do Código e Boas Práticas:**
    * Código limpo, legível e de fácil manutenção.
    * Uso de convenções de nomenclatura consistentes.
    * Uso de ferramentas de qualidade de código (linters, formatters) é um grande diferencial.

3.  **Modularização e Gerenciamento de Estado:**
    * Criação de componentes (ou módulos) reutilizáveis e bem definidos.
    * Escolha e implementação de uma estratégia de gerenciamento de estado que seja coerente com a complexidade da aplicação e a tecnologia escolhida.

4.  **Assincronismo e Tratamento de Erros:**
    * Como você lida com as chamadas assíncronas para a API.
    * Gerenciamento de estados de carregamento (`loading`) e erro na interface do usuário.

5.  **Testes:**
    * A relevância e a qualidade dos testes que você escreveu.
    * Demonstração de entendimento sobre o que e como testar.

6.  **Responsividade e Acessibilidade (a11y):**
    * A aplicação deve ser funcional e agradável em diferentes tamanhos de tela (mobile e desktop).
    * Uso de HTML semântico e boas práticas de acessibilidade (ex: atributos `alt` em imagens, `aria-label` em botões, contraste de cores, etc.).

7.  **Versionamento (Git):**
    * Commits atômicos e com mensagens claras e descritivas (seguindo um padrão como o [Conventional Commits](https://www.conventionalcommits.org/) é um bônus).
    * Um histórico de commits que conta a história do desenvolvimento.

8.  **Documentação (README.md):**
    * **Este é um requisito fundamental.** O `README.md` do seu projeto deve ser claro e conter:
        * Uma breve descrição do projeto.
        * A linguagem/framework utilizado.
        * Os pré-requisitos para rodar o projeto.
        * As instruções passo a passo para instalar as dependências e executar a aplicação localmente (incluindo a API mock).
        * Instruções para rodar os testes.
        * Uma breve explicação sobre as **decisões técnicas** que você tomou (ex: por que escolheu determinada abordagem de estilização, gerenciamento de estado, etc.).

## Diferenciais (Opcional)

Quer ir além? Aqui estão algumas ideias para impressionar:

* Implementar paginação ou "scroll infinito" na lista de transações.
* Adicionar funcionalidades de ordenação (por data, valor, etc.).
* Criar uma visualização gráfica simples dos dados (ex: um gráfico de pizza mostrando a proporção de despesas por categoria).
* Configurar um pipeline de Integração Contínua (CI) com GitHub Actions (ou similar) para rodar os testes e o linter automaticamente.
* Otimizações de performance (ex: virtualização da lista para grandes volumes de dados).

## Entrega

1.  Crie um repositório público no GitHub (ou serviço de sua preferência).
2.  Faça o push do seu código, garantindo que o `README.md` esteja completo.
3.  Envie o link do repositório para o recrutador.

Boa sorte e divirta-se! Estamos ansiosos para ver seu trabalho.
