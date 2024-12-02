# Máscara de Rede

A **máscara de rede** é um endereço de 4 bytes (32 bits) no mesmo formato do endereço IP. Os bits **"1"** da máscara de rede representam a parte do endereço IP que identifica a **rede**, enquanto os bits **"0"** representam a parte do endereço IP que identifica o **host** dentro da rede.

## Como Funciona a Máscara de Rede

Cada parte da máscara de rede (o octeto) pode ser representada em binário, onde os bits "1" correspondem à porção do endereço IP que faz parte da rede e os bits "0" são usados para os hosts.

## Exemplo

Vamos considerar o seguinte exemplo:

- **Endereço IP:** `192.168.1.100`
- **Máscara de Sub-rede:** `255.255.255.0`

### Representação Binária

| Endereço | Binário                  | Explicação                           |
|----------|--------------------------|--------------------------------------|
| IP       | `11000000.10101000.00000001.01100100` | O endereço IP `192.168.1.100` em binário.  |
| Máscara  | `11111111.11111111.11111111.00000000` | A máscara de sub-rede `255.255.255.0` em binário. |

### Cálculo do Endereço da Rede

A operação **AND** bit a bit entre o endereço IP e a máscara de sub-rede resulta no endereço da rede.

| IP (binário)               | Máscara de Sub-rede (binário)        | Resultado (binário)                  | Endereço da Rede |
|----------------------------|-------------------------------------|--------------------------------------|------------------|
| `11000000.10101000.00000001.01100100` | `11111111.11111111.11111111.00000000` | `11000000.10101000.00000001.00000000` | `192.168.1.0`    |

O endereço da rede, após a operação AND, é `192.168.1.0`.

## Resumo

| Tipo               | Explicação                                           |
|--------------------|------------------------------------------------------|
| **Máscara de Rede** | Define quantos bits do IP pertencem à rede e quantos ao host. |
| **Bits "1"**        | Representam a parte do IP que identifica a rede.    |
| **Bits "0"**        | Representam a parte do IP que identifica o host.    |
| **Operação AND**    | A operação **AND** entre o IP e a máscara dá o endereço da rede. |

### Exemplo Final

Com o IP `192.168.1.100` e a máscara de sub-rede `255.255.255.0`, a operação **AND** resulta no endereço da rede `192.168.1.0`.
