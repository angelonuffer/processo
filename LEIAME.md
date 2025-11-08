# processo

Uma biblioteca para executar comandos.

## escreva : função

`mensagem : texto` => `comando : objeto`

Escreve uma mensagem na saída padrão do processo.

## saia : função

`código : número` => `comando : objeto`

Encerra o processo com o código de saída.

## nodejs : função

`comandos : lista<comando>` => `código : texto`

Transforma uma lista de comandos num código Node.js.

## comando : objeto

- `tipo : "escreva" | "saia"` - Tipo do comando
- `argumento : texto | número` - Argumento para o comando