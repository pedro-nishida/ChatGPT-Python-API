# Categorização de Produtos com OpenAI GPT-3

Este script em Python foi desenvolvido para categorizar produtos utilizando o modelo GPT-3 da OpenAI. Ele começa importando os módulos necessários: `os`, `openai` e `dotenv`.

## Função `categorizaProduto`

A função `categorizaProduto` tem como objetivo categorizar um produto fornecido. Ela recebe dois argumentos:

- `nome_do_produto`: O nome do produto a ser categorizado.
- `categorias_validas`: As categorias válidas para classificação.

Dentro da função:
- Uma string `prompt_sistema` é criada utilizando um f-string. Essa string serve como prompt para o modelo de IA, instruindo-o a categorizar o produto. Ela inclui uma lista de categorias válidas e um exemplo de como a categorização deve ser feita.
- O método `openai.ChatCompletion.create` é utilizado para gerar uma resposta do modelo GPT-3. Esse método inclui parâmetros como:
  - `model`: Especifica o modelo a ser usado, neste caso, "gpt-3.5-turbo".
  - `messages`: Uma matriz de objetos de mensagem, cada um com um "papel" e um "conteúdo". A primeira mensagem tem o papel de "sistema" e fornece o prompt para o modelo de IA. A segunda mensagem tem o papel de "usuário" e fornece o nome do produto a ser categorizado.
  - `temperature`: Controla a aleatoriedade da saída do modelo de IA. Valores mais altos aumentam a aleatoriedade.
  - `max_tokens`: Define o comprimento máximo da saída do modelo.
  - `top_p`: Controla a amostragem do núcleo, ajudando na geração de respostas diversas.
  - `frequency_penalty` e `presence_penalty`: Parâmetros que controlam a saída do modelo com base na frequência e presença de tokens, respectivamente.
- Por fim, a função imprime o conteúdo da primeira escolha da resposta do modelo. Esta saída deve representar a categorização do produto realizada pela IA.

Este script demonstra como o GPT-3 pode ser usado para automatizar a tarefa de categorização de produtos, fornecendo uma categorização com base no prompt definido pelo sistema e no nome do produto fornecido pelo usuário.

```python
# Exemplo de uso da função categorizaProduto
categorizaProduto("Nome do Produto", ["Categoria A", "Categoria B", "Categoria C"])
Certifique-se de configurar corretamente as variáveis de ambiente, incluindo a chave da API da OpenAI, antes de executar o script.