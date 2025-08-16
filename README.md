# LISTA DE ATIVIDADES

### Atividade 1: Criação de um Endpoint Simples

**Objetivo:** Usando um framework web de sua preferência (como Express.js, Flask, Spring Boot, etc.), crie um endpoint de API `GET /status`. Este endpoint deve retornar uma resposta em formato JSON com o seguinte corpo:

```json
{
  "status": "OK",
  "timestamp": "2024-08-16T12:00:00.000Z"
}
```

**Observação:** O campo `timestamp` deve ser a data e hora atual no formato ISO 8601.

**O que avalia:** Conhecimento básico sobre como criar um servidor web, rotas e retornar respostas em JSON.

-----

### Atividade 2: Filtragem de Dados

**Objetivo:** Crie uma função que receba uma lista de objetos, onde cada objeto representa um usuário com as propriedades `id`, `nome` e `ativo`. A função deve retornar uma nova lista contendo apenas os usuários que estão com o status `ativo` como `true`.

**Exemplo de entrada:**

```javascript
const usuarios = [
  { id: 1, nome: 'Alice', ativo: true },
  { id: 2, nome: 'Bruno', ativo: false },
  { id: 3, nome: 'Carla', ativo: true },
  { id: 4, nome: 'Daniel', ativo: false }
];
```

**Saída esperada:**

```javascript
[
  { id: 1, nome: 'Alice', ativo: true },
  { id: 3, nome: 'Carla', ativo: true }
]
```

**O que avalia:** Manipulação de arrays/listas e objetos, além do uso de funções de filtro ou laços de repetição.

-----

### Atividade 3: Agrupamento e Agregação de Dados

**Objetivo:** Crie uma função que receba uma lista de objetos representando vendas. Cada objeto contém `produto`, `categoria` e `valor`. A função deve retornar um objeto que resume o total de vendas por categoria.

**Exemplo de entrada:**

```javascript
const vendas = [
  { produto: 'Notebook', categoria: 'Eletrônicos', valor: 1500 },
  { produto: 'Celular', categoria: 'Eletrônicos', valor: 800 },
  { produto: 'Camiseta', categoria: 'Vestuário', valor: 50 },
  { produto: 'Calça Jeans', categoria: 'Vestuário', valor: 100 },
  { produto: 'Monitor', categoria: 'Eletrônicos', valor: 600 }
];
```

**Saída esperada:**

```javascript
{
  'Eletrônicos': 2900,
  'Vestuário': 150
}
```

**O que avalia:** Manipulação avançada de arrays e objetos, uso de estruturas de dados como mapas (ou dicionários) e lógica de agregação de dados.

-----

### Atividade 4: Validador de Parênteses Balanceados

**Objetivo:** Escreva uma função que receba uma string contendo apenas os caracteres `(`, `)`, `{`, `}`, `[` e `]`, e determine se a sequência de parênteses é válida e balanceada.

**Regras:**

  * Um parêntese de abertura deve ser fechado pelo mesmo tipo de parêntese.
  * Os parênteses devem ser fechados na ordem correta.

**Exemplos:**

  * `"()"` deve retornar `true`.
  * `"()[]{}"` deve retornar `true`.
  * `"(]"` deve retornar `false`.
  * `"([)]"` deve retornar `false`.
  * `"{[]}"` deve retornar `true`.

**O que avalia:** Raciocínio algorítmico e o uso de estruturas de dados, especificamente a pilha (stack), para resolver um problema clássico.

-----

### Atividade 5: Validação de Entrada e Tratamento de Erros

**Objetivo:** Crie um endpoint `POST /usuarios` que simule o cadastro de um novo usuário. O corpo da requisição deve conter `nome`, `email` e `senha`. Implemente as seguintes regras de validação no backend:

1.  **nome:** Deve ser uma string com no mínimo 3 caracteres.
2.  **email:** Deve ser uma string em formato de e-mail válido.
3.  **senha:** Deve ser uma string com no mínimo 8 caracteres.

**Comportamento esperado:**

  * Se todos os dados forem válidos, retorne um status `201 Created` com uma mensagem de sucesso.
  * Se um ou mais campos forem inválidos, retorne um status `400 Bad Request` com um corpo de resposta JSON indicando qual campo falhou na validação e o motivo.

**Exemplo de resposta de erro para um e-mail inválido:**

```json
{
  "erro": "Dados inválidos",
  "detalhes": {
    "email": "O campo email deve ser um endereço de e-mail válido."
  }
}
```

**O que avalia:** Boas práticas de desenvolvimento, validação de dados de entrada (*input validation*), e tratamento de erros com retornos de status HTTP e mensagens claras.

-----

### Atividade 6: Consumo e Formatação de API Externa

**Objetivo:** Crie uma função ou um endpoint (ex: `GET /cep/:cep`) que receba um CEP brasileiro como parâmetro, consulte a API pública **ViaCEP** (`https://viacep.com.br/ws/SEU_CEP/json/`) e retorne um objeto formatado apenas com as informações de `logradouro`, `bairro`, `cidade` e `uf`.

**Exemplo:**

  * Se a função receber o CEP `"01001000"`.
  * Ela deve fazer uma requisição para `https://viacep.com.br/ws/01001000/json/`.
  * A API do ViaCEP retornará um objeto completo.
  * Sua função deve processar essa resposta e retornar o seguinte objeto:

<!-- end list -->

```json
{
  "logradouro": "Praça da Sé",
  "bairro": "Sé",
  "cidade": "São Paulo",
  "uf": "SP"
}
```

**O que avalia:** Habilidade de fazer requisições HTTP para serviços externos, lidar com programação assíncrona (promises, async/await) e parsear/formatar respostas JSON.
