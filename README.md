# Implementação de Tabela Hash em C

Este projeto implementa uma Tabela Hash utilizando listas encadeadas para resolver colisões. O código está organizado em vários arquivos para modularidade e clareza.

## Estrutura de Dados

### `struct slot`
Cada posição da Tabela Hash é representada por um vetor de `struct slot`, que contém:
- `struct nodoHash* inicio`: Um ponteiro para o primeiro nó da lista encadeada.
- `struct nodoHash* fim`: Um ponteiro para o último nó da lista encadeada.

### `struct nodoHash`
Os nós que compõem as listas encadeadas na Tabela Hash são definidos pela estrutura `struct nodoHash`, que contém:
- `int chave`: A chave associada ao nó.
- `struct nodoHash* proximo`: Um ponteiro para o próximo nó da lista.
- `struct nodoHash* anterior`: Um ponteiro para o nó anterior da lista.

## Arquivos do Projeto

### `main.c`
Este arquivo contém a função principal do programa, que faz chamadas para várias funções de manipulação da Tabela Hash:
- `imprimirDadosAlunos()`: Exibe os dados dos alunos armazenados na Tabela Hash.
- `gerarTabelaHash()`: Inicializa e popula a Tabela Hash.
- `liberarTabelaHash()`: Libera a memória alocada para a Tabela Hash.
- `obterTamTabela()`: Obtém o tamanho da Tabela Hash.
- `operacoes()`: Gerencia as operações disponíveis para o usuário.

### `tabelaHash.c` e `tabelaHash.h`
Estes arquivos contêm a implementação das funções principais que gerenciam a Tabela Hash:
- Funções para criação, inserção, busca e remoção de elementos na Tabela Hash.
- Funções para liberar a memória alocada pela Tabela Hash.

### `operacoes.c` e `operacoes.h`
Contêm a implementação de funções auxiliares, como:
- `help()`: Exibe instruções de uso do programa.
- `obterTamTabela()`: Determina o tamanho da Tabela Hash.
- `obterComando()`: Processa os comandos do usuário.
- `operacoes()`: Executa as operações especificadas pelo usuário.

### `lista.c` e `lista.h`
Estes arquivos implementam listas encadeadas que são usadas para gerenciar colisões na Tabela Hash.

## Compilação

### Como Compilar
O projeto inclui um `Makefile` para facilitar a compilação. Para compilar o projeto, basta executar o seguinte comando no terminal:
```bash
make
```
Isso gerará o executável a partir dos arquivos fonte fornecidos.

### Como Executar
Após a compilação, execute o programa com o comando:

```bash
./exec
```
Siga as instruções exibidas para realizar as operações na Tabela Hash.

## Uso do Programa

O programa permite executar várias operações na Tabela Hash, como:

- **Inserir** novos elementos.
- **Remover** elementos existentes.
- **Buscar** por um elemento específico.
- **Exibir** os elementos armazenados na Tabela Hash.

Utilize a função `help()` para obter mais informações sobre os comandos disponíveis.

## Estrutura do Projeto

- **`main.c`**: Função principal do programa.
- **`tabelaHash.c` e `tabelaHash.h`**: Implementação da Tabela Hash.
- **`operacoes.c` e `operacoes.h`**: Funções auxiliares e de suporte.
- **`lista.c` e `lista.h`**: Implementação de listas encadeadas para a Tabela Hash.
- **`makefile`**: Script de automação para a compilação.
