# Color Tools (Fig)

Modulo utilitario para manipulacao de cores, conversao de hex e uso de ANSI 24-bit.

## Instalar no projeto

```bash
fig install isCarlosCoder/color-tools
```

## Importar

```js
import "mod:isCarlosCoder/color-tools" color
```

## Uso basico

```js
import "mod:isCarlosCoder/color-tools" color

let red = color.rgb(255, 0, 0)
print(color.toHex(red))
print(color.paint("Alert", red))
```

## Conversao

```js
let c1 = color.fromHex("#0f0")
print(color.toHex(c1))  # #00ff00
```

## Mistura e variacoes

```js
let base = color.rgb(50, 120, 200)
let lighter = color.lighten(base, 0.3)
let darker = color.darken(base, 0.3)
```

## ANSI

```js
let teal = color.rgb(0, 180, 180)
print(color.paint("Hello", teal))
print(color.paintBg("Hi", teal))
```

## API

- `color.rgb(r, g, b)`
- `color.rgba(r, g, b, a)`
- `color.withAlpha(color, a)`
- `color.toHex(color)`
- `color.fromHex(hex)`
- `color.mix(a, b, t)`
- `color.lighten(color, amount)`
- `color.darken(color, amount)`
- `color.invert(color)`
- `color.toRgbString(color)`
- `color.toRgbaString(color)`
- `color.fgCode(color)`
- `color.bgCode(color)`
- `color.reset()`
- `color.paint(text, color)`
- `color.paintBg(text, color)`

## Rodar testes locais

Dentro do modulo:

```bash
FIG_COLOR_TOOLS_TEST=1 fig run
```
