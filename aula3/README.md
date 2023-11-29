# Script de Contagem de Tokens para Uso com Modelos OpenAI

Este script em Python utiliza a biblioteca `tiktoken`, uma ferramenta para contar o número de tokens em uma string sem realizar uma chamada de API. Isso é especialmente útil ao trabalhar com os modelos da OpenAI, como o GPT-3, que cobram por token.

## Configuração e Requisitos

### Biblioteca Necessária

- `tiktoken`: Esta biblioteca é essencial para executar o script e está disponível para contar tokens em uma string sem precisar fazer uma chamada à API.

## Utilização

Este script demonstra como contar tokens em uma string e calcular o custo estimado de processamento da mesma por um modelo da OpenAI. Para utilizá-lo:

### Execução do Script

Execute o script em um ambiente Python.

### Saída Interativa

- O script utiliza a biblioteca `tiktoken` para codificar uma string em uma lista de tokens.
- Em seguida, imprime a lista de tokens e seu comprimento.
- Calcula o custo estimado da string com base no número de tokens e um custo por token assumido.

## Explicação do Código

O script começa importando a biblioteca `tiktoken`.

```python
# Importando a biblioteca tiktoken
import tiktoken

# Criação do objeto codificador
encoder = tiktoken.encoding_for_model("gpt-3.5-turbo-16k")

# Codificação da string em uma lista de tokens
input_string = "Você é um categorizador de produtos."
tokens = encoder.encode(input_string)

# Exibição da lista de tokens e seu comprimento
print("Lista de Tokens:", tokens)
print("Comprimento dos Tokens:", len(tokens))

# Cálculo do custo estimado da string com base no número de tokens
cost_per_token = 0.0015  # Custo por token (exemplo, pode não refletir o preço real)
cost = (len(tokens) * cost_per_token) / 1000  # Custo total em unidades
print("Custo Estimado:", cost)
