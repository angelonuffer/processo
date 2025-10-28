# Processo

Uma biblioteca simples para executar comandos do Node.js.

## Estrutura

- `código/0`: Contém as funções principais
- `testes/0`: Contém os testes unitários
- `.github/workflows/IC.yml`: Configuração da Integração Contínua

## Funções

A biblioteca fornece funções principais para diferentes formatos de saída:

- `nodejs`: Gera código JavaScript para Node.js
- `wat`: Gera código WebAssembly Text format (WAT) com WASI

E funções auxiliares para criar comandos:

- `escreva`: Cria comando para escrever texto
- `saia`: Cria comando para sair com código de status

## Formatos de Saída

### Node.js
Gera código JavaScript compatível com Node.js:
```javascript
console.log('mensagem');process.exit(0)
```

### WAT (WebAssembly Text format com WASI)
Gera código WebAssembly Text format com suporte a WASI:
```wat
(module
  (import "wasi_snapshot_preview1" "fd_write" (func $fd_write (param i32 i32 i32 i32) (result i32)))
  (import "wasi_snapshot_preview1" "proc_exit" (func $proc_exit (param i32)))
  (memory 1)
  (export "memory" (memory 0))
  (export "_start" (func $_start))
  (func $_start
    ;; escreva "mensagem"
    (call $proc_exit (i32.const 0))
  )
)
```

## Como Executar os Testes

Para executar os testes, você precisa:

1. Ter o Node.js instalado
2. Ter o repositório nuffem/0 clonado
3. Executar:

```bash
node 0/0_node.js testes/0
```
