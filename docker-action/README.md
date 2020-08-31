# Acción de docker Hello world

Esta acción imprime "Hello World" o "Hello" + el nombre de una persona a quien saludar en el registro.

## Entradas

### `who-to-greet`

**Obligatorio** El nombre de la persona a quien saludar. Default `"World"`.

## Outputs

### `time`

El tiempo en que lo saludamos.

## Ejemplo de uso

uses: actions/hello-world-docker-action@v1
with:
  who-to-greet: 'Mona the Octocat'