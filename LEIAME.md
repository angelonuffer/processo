# Processo

Uma biblioteca simples para executar comandos do Node.js.

## Funções

- `nodejs({ comandos })`: Converte a lista de comandos para Node.js
- `escreva(mensagem)`: Cria um comando para exibir a `mensagem` na saída
- `saia(codigo)`: Cria um comando para encerrar o processo com `código`

Exemplo:

```
processo.nodejs({
  comandos: [
    processo.escreva("teste")
    processo.saia(0)
  ]
})
// "console.log('teste');process.exit(0)"
```

## Como Executar os Testes

Para executar os testes, você precisa:

1. Ter o Node.js 22 ou superior instalado
2. Ter o repositório angelonuffer/0 clonado
3. Executar:

```bash
node 0/código/0_node.js testes/0 node | node
```