ChatGPT API Python

Bem-vindo ao repositório do projeto ChatGPT API Python! Aqui está os porgramas que eu treinei para o meu aprendizado, seguindo o curso de Inteligência Artificial da Alura!

# ChatGPT 3.5 Turbo - Assistente de Categorização de Produtos

Este script Python interage com a API da OpenAI, especificamente com o modelo GPT-3.5-turbo, para gerar respostas com base nas entradas do usuário.

## Configuração

Certifique-se de ter instalado os seguintes pacotes Python:

- `openai`: O cliente oficial para a API da OpenAI.
- `dotenv`: Para carregar variáveis de ambiente a partir do arquivo `.env`.

### Arquivo `.env`

Antes de executar o script, crie um arquivo `.env` na raiz do projeto e adicione sua chave de API da OpenAI:

```
OPENAI_API_KEY=SUA_CHAVE_API_AQUI
```

### Instalação de Dependências

Para instalar as dependências necessárias, execute:

```bash
pip install openai python-dotenv
```

## Uso

O script utiliza a API da OpenAI para criar uma sessão de chat. Ele envia duas mensagens: uma do sistema e outra do usuário.

- Mensagem do sistema:
  - **Papel**: Categorizador de produtos.
  
- Mensagem do usuário:
  - **Conteúdo**: "escova de dentes".

Os parâmetros `temperature`, `max_tokens`, `top_p`, `frequency_penalty` e `presence_penalty` controlam a aleatoriedade e o comprimento das respostas.

## Exemplo de Uso

Execute o script Python para obter a resposta gerada pela API da OpenAI com base nas mensagens fornecidas.

```bash
python chat_script.py
```

## Observações

Lembre-se de não compartilhar suas chaves de API com outras pessoas. Mantenha o arquivo `.env` seguro e fora de repositórios públicos.