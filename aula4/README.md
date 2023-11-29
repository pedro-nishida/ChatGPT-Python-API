# Análise de Comportamento de Compra de Clientes com GPT-3.5-turbo

Este script em Python faz parte de um programa maior que utiliza o modelo GPT-3.5-turbo da OpenAI para analisar o comportamento de compra de clientes.

## Setup e Requisitos

### Módulos Necessários

- `os`: Fornece funcionalidades dependentes do sistema operacional.
- `openai`: Biblioteca cliente em Python para a API da OpenAI.
- `dotenv`: Utilizado para carregar variáveis de ambiente a partir de um arquivo `.env`.
- `tiktoken`: Ferramenta para contar o número de tokens em uma string sem fazer uma chamada de API.

## Funcionalidades do Script

### Funcionalidades Principais

#### Contagem de Tokens:

- Utiliza a biblioteca `tiktoken` para contar o número de tokens em uma string.
- Usa a função `encoding_for_model` para obter o tokenizer apropriado para o modelo "gpt-3.5-turbo".

#### Carregamento de Dados:

- Define a função `carrega` para carregar dados de um arquivo.
- Abre o arquivo em modo de leitura e lê seu conteúdo.
- Trata exceções caso o arquivo não possa ser aberto.

#### Configuração de Variáveis de Ambiente:

- Utiliza o `dotenv` para carregar variáveis de ambiente de um arquivo `.env`.
- Recupera a chave da API da OpenAI com `os.getenv` e a atribui a `openai.api_key`.

#### Preparação para Chamada à API:

- Define prompts para o modelo de AI, como `prompt_sistema` e `prompt_usuario`.
- Converte os prompts combinados em uma lista de tokens usando o codificador (tokenizer).
- Calcula e imprime o número de tokens.

#### Preparação para Chamada à API:

- Define um tamanho esperado de saída em tokens.
- Verifica se o número de tokens no prompt é maior ou igual ao limite máximo de tokens do modelo menos o tamanho esperado de saída.
- Se a condição for verdadeira, define o modelo como "gpt-3.5-turbo-16k".

### Observações Finais

O script termina abruptamente, indicando que o restante do código provavelmente trata a chamada real à API da OpenAI e o processamento da saída do modelo.

Este script serve como uma parte integrante de um sistema maior que visa analisar o comportamento de compra de clientes utilizando o poder do modelo GPT-3.5-turbo da OpenAI.

## Licença

Este projeto está licenciado sob a [Licença MIT](https://opensource.org/licenses/MIT).
