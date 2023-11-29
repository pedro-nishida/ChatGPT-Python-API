# Identificação de Perfis de Compra

Este script em Python contém três funções principais: `carrega`, `salva` e `identifica_perfis`.

## Funcionalidades das Funções

### Função `carrega`

- Recebe um nome de arquivo como argumento.
- Tenta abrir e ler o arquivo especificado.
- Utiliza um bloco try/except para lidar com exceções IOError que podem ocorrer durante o processo, como quando o arquivo não existe.
- Se o arquivo for aberto e lido com sucesso, a função retorna o conteúdo do arquivo como uma string.

### Função `salva`

- Similar à função `carrega`, mas escreve em um arquivo em vez de ler.
- Recebe um nome de arquivo e algum conteúdo como argumentos.
- Tenta abrir o arquivo em modo de escrita e escrever o conteúdo nele.
- Utiliza um bloco try/except para lidar com exceções IOError que podem ocorrer durante o processo de escrita.

### Função `identifica_perfis`

- Recebe uma lista de compras por cliente como argumento.
- Imprime uma mensagem indicando que está iniciando a identificação de perfis.
- Define um prompt multilinha que parece ser um guia para o usuário identificar o perfil de compra de cada cliente.
- O prompt inclui um exemplo do formato de saída esperado, que é um objeto JSON contendo uma matriz de objetos de cliente, cada um com um nome e uma descrição de perfil.

## Observações Finais

O script parece ter o propósito de carregar e salvar dados de arquivos, bem como de guiar o usuário na identificação de perfis de compra para cada cliente com base em suas compras. As funções `carrega` e `salva` lidam com a manipulação de arquivos, enquanto a função `identifica_perfis` parece ser um guia para interação do usuário na definição dos perfis de compra dos clientes.

Observação adicional: Dependendo do tamanho do documento, o programa pode rodar com sucesso, dependendo da capacidade de processamento disponível na carteira na plataforma do ChatGPT.
