# Script de Categorização de Produtos com OpenAI

Este script em Python é parte de um sistema de categorização de produtos. Ele utiliza a API da OpenAI para categorizar produtos com base em seus nomes.

## Configuração e Requisitos

### Módulos Necessários
- **os**: Oferece funcionalidades dependentes do sistema operacional.
- **openai**: Biblioteca cliente em Python para a API da OpenAI.
- **dotenv**: Utilizado para carregar variáveis de ambiente a partir de um arquivo .env.

### Variáveis de Ambiente
É essencial configurar as variáveis de ambiente para garantir o funcionamento correto do script:

**Arquivo .env**: Deve estar no mesmo diretório do script e conter a chave OPENAI_API_KEY.

## Utilização

Este script interage de forma interativa com o usuário para categorizar produtos. Após configurar as variáveis de ambiente:

### Execução do Script

Execute o script em um ambiente Python.

### Interação Interativa

- O script solicita ao usuário inserir categorias válidas e nomes de produtos.
- Para cada nome de produto inserido, a função `categorizaProduto` é chamada para categorizar o produto.

## Explicação do Código

O script começa definindo a função `categorizaProduto` (não mostrada no excerto). Esta função recebe dois argumentos: `nome_do_produto` (o nome do produto) e `categorias_validas` (as categorias válidas). Dentro desta função:

- Realiza uma chamada à API da OpenAI com certos parâmetros, como `temperature`, `max_tokens`, `top_p`, `frequency_penalty` e `presence_penalty`. A resposta da chamada à API é então impressa.

Após a definição da função, o script carrega variáveis de ambiente usando `dotenv.load_dotenv()`. Isso é feito tipicamente para gerenciar de forma segura informações sensíveis, como chaves de API. A chave da API da OpenAI é então recuperada das variáveis de ambiente e configurada como `openai.api_key`.

O script entra em um modo interativo onde solicita ao usuário inserir categorias válidas e o nome do produto. Ele continua solicitando nomes de produtos em um loop até o usuário digitar "sair", momento em que encerra o loop. Para cada nome de produto inserido, chama a função `categorizaProduto` para categorizá-lo.

## Notas Importantes

- Certifique-se de que o arquivo .env esteja no diretório do script e contenha a chave `OPENAI_API_KEY` correta.
- Ajuste os parâmetros de controle para variações desejadas na saída.
- Aviso Legal: Tenha cautela com informações sensíveis como chaves de API e evite compartilhá-las publicamente.

Para mais informações e uso detalhado da API, consulte a documentação da OpenAI API.
