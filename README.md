# Trabalhos_extras
Cenários de Teste da ULA 6-bits

A seguir estão descritos cinco cenários de teste que validam o funcionamento da ULA desenvolvida no CircuitVerse. Cada cenário cobre uma das operações principais da unidade.

Cenário 1 – Somador (sel = 11)

Entradas:

A = 000101 (5)

B = 000111 (7)

sel = 00

Resultado esperado:

Y = 000110 (12)

carry = 0

overflow = 0

zero = 0

Cenário 2 – Carry no Somador (sel = 11)

Entradas:

A = 111111 (63)

B = 000001 (1)

sel = 00

Resultado esperado:

Y = 000000 (0, pois ocorre estouro em 6 bits)

carry = 1

overflow = 0

zero = 1

Cenário 3 – Convenção (unsigned, 6 bits):
Quando sel = 00, a saída Y codifica o resultado da comparação:

Y = 000000 → A == B (usa a flag zero = 1 para indicar igualdade)

Y = 000001 → A > B

Y = 000010 → A < B
Flags: carry = 0, overflow = 0 nesse modo.
Cenário 4 – Operação OR (sel = 01)

Entradas:

A = 101010

B = 010011

sel = 10

Resultado esperado:

Y = 111011

carry = 0

overflow = 0

zero = 0

Cenário 5 – Operação AND (sel = 10)

Entradas:

A = 101010

B = 010011

sel = 11

Resultado esperado:

Y = 000010

carry = 0

overflow = 0

zero = 0

Esses cenários permitem validar todas as operações principais da ULA: adição, detecção de carry, contagem, OR bit a bit e AND bit a bit.