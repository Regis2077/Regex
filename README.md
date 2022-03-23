# Regex
Expressões regulares são padrões utilizados para selecionar combinações de caracteres em uma string. Em JavaScript, expressões regulares também são objetos. Elas podem ser utilizadas com os métodos `[exec](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/exec)` e `[test](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/test)`do objeto [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp), e com os métodos `[match](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match)`, `[replace](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace)`, [`search`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/search), e `[split](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)` do objeto `[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)`.

### Usos Regex

- Extraindo seções específicas de um arquivo de texto
- Validação de formatação de, por exemplo, e-mail ou telefone
- Análise de arquivos de texto e extração de dados para, por exemplo, gravar no banco de dados
- Substituindo os valores de um texto para limpar, reformatar ou alterar o conteúdo

## Regex-Engine

Uma expressão regular sozinha é apenas uma string. É preciso ter um software para interpretar a regex e aplicá-la no alvo. Esse software é o *Regex Engine* que existe para a maioria das plataformas de desenvolvimento, como JavaScript, C#, Python, Ruby ou PHP.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6c3ceb5d-f40e-4e83-bfa9-78889d96a0c8/Untitled.png)

## Meta chars

Existem alguns caracteres que possuem um significado especial para o regex engine. Especial significa que o regex engine não interpreta o valor literal e sim diferente. Esses caracteres são chamados de **meta caracteres**.

- `.` o "ponto" que significa qualquer char
- * o asterisco que serve para definir uma quantidade de chars, zero ou mais vezes
- `{`e `}` as chaves que servem para definir uma quantidade de caracteres específicas que é desejado encontrar

Por exemplo:

- `a{3}` letra `a` 3 vezes.
- `\d*` um digito zero ou mais vezes

## Quantifier

- `{n}` - exatamente n vezes.
- `{n,}` - no mínimo n vezes.
- `{n,m}` - no mínimo n vezes, no máximo m vezes.
- `?` - zero ou uma vez.
- * - zero ou mais vezes.
- `+` - uma ou mais vezes.

## ****Classes de Char - [ ]****

- `[A-Z]` significa de A até Z, sempre maiúscula.
- `[a-z]` significa de a até z, sempre minúscula,
- `[A-Za-z]` significa A-Z ou a-z.
- `[abc]` significa a, b ou c.
- \d - todos dos digitos [0-9]
- \s - whitespace [ \t\r\n\f]
    - `\t` é um *tab*.
    - `\r` é *carriage return*.
    - `\n` é *newline*.
    - `\f` é *form feed*.
- \w - wordchar[A-Za-z0-9_]

## Âncoras

- `\b`  *word boundary*
- `^` início da string alvo.
- `$` a o fim do alvo.
