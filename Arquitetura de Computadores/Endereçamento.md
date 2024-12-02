## Endereçamento em Redes

### Endereçamento Físico
O endereçamento físico identifica de forma única os dispositivos numa rede local. Exemplos incluem:
- **Ethernet:** Protocolo que utiliza endereços físicos para a comunicação em redes locais.
- **MAC Address:** Identificador único de 48 bits atribuído a cada interface de rede, usado para identificar dispositivos na camada de enlace.

### Endereçamento Lógico
O endereçamento lógico é utilizado para identificar dispositivos em redes maiores, como a Internet, permitindo comunicação entre diferentes redes.
- **IP (Internet Protocol):** Endereço lógico atribuído a cada dispositivo numa rede, podendo ser:
  - **IPv4:** Endereço de 32 bits no formato "xxx.xxx.xxx.xxx".
  - **IPv6:** Endereço de 128 bits projetado para suportar um maior número de dispositivos.

## Constituição dos Endereços IP

### IPv4 (Internet Protocol version 4)
- **Tamanho:** 32 bits, dividido em 4 octetos (grupos de 8 bits), representados no formato decimal separado por pontos (ex.: `192.168.0.1`).
- **Estrutura:**
  - **Parte da Rede:** Identifica a rede à qual o dispositivo pertence.
  - **Parte do Host:** Identifica o dispositivo específico dentro da rede.
- **Classes:**
  - **Classe A:**
    - **Intervalo:** 1.0.0.0 a 126.255.255.255.
    - **Máscara de Sub-rede:** 255.0.0.0.
    - **IPs Disponíveis:** Aproximadamente 16,7 milhões de endereços por rede (2^24).
    - **Uso:** Grandes redes, como redes de ISPs ou grandes corporações.
  - **Classe B:**
    - **Intervalo:** 128.0.0.0 a 191.255.255.255.
    - **Máscara de Sub-rede:** 255.255.0.0.
    - **IPs Disponíveis:** Aproximadamente 65.000 endereços por rede (2^16).
    - **Uso:** Redes de tamanho médio, como universidades e empresas.
  - **Classe C:**
    - **Intervalo:** 192.0.0.0 a 223.255.255.255.
    - **Máscara de Sub-rede:** 255.255.255.0.
    - **IPs Disponíveis:** Até 254 endereços por rede (2^8 - 2).
    - **Uso:** Redes pequenas, como pequenas empresas ou redes domésticas.
  - **Classes D e E:**
    - **Classe D (Multicast):** 224.0.0.0 a 239.255.255.255. Usado para comunicação de multicast.
    - **Classe E (Reservado):** 240.0.0.0 a 255.255.255.255. Reservado para uso futuro ou experimentação.

- **Uso do 0 e 255 no IPv4:**
  - **0:** Em um endereço de rede, o `0` é usado para identificar a rede em si, ou seja, é o endereço de rede que define o início de um intervalo de endereços. Exemplo: `192.168.1.0` é a rede, não um host.
  - **255:** O `255` é usado no endereço de broadcast, ou seja, é um endereço especial para enviar pacotes a todos os dispositivos de uma rede. Exemplo: `192.168.1.255` envia uma mensagem para todos os dispositivos na rede `192.168.1.0/24`.

### IPv6 (Internet Protocol version 6)
- **Tamanho:** 128 bits, representado no formato hexadecimal, separado por dois pontos (ex.: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
- **Estrutura:**
  - **Prefixo da Rede:** Define a rede a que pertence.
  - **ID de Interface:** Identifica o dispositivo específico dentro da rede.
- **Características:**
  - Suporta um número maior de dispositivos devido ao tamanho do endereço.
  - Possui recursos nativos para segurança e mobilidade.

### Classes de IP
As classes de endereços IP são definidas pela parte do endereço que corresponde à rede (ID da rede) e a parte que corresponde ao host (ID do host). A máscara de sub-rede ajuda a determinar a divisão entre essas duas partes.

- **Classe A:**
  - **Intervalo:** 1.0.0.0 a 126.255.255.255.
  - **Máscara de Sub-rede:** 255.0.0.0 (ou /8).
  - **IP da Rede:** O primeiro octeto (primeiros 8 bits) é usado para o ID da rede, e os 24 bits restantes são usados para o ID do host.
  - **IPs Disponíveis:** Aproximadamente 16,7 milhões de endereços por rede (2^24).
  - **Uso:** Grandes redes, como redes de ISPs ou grandes corporações.
  - **Exemplo:** Em `10.1.2.3`, a rede é `10.0.0.0` e o host é `1.2.3`.

- **Classe B:**
  - **Intervalo:** 128.0.0.0 a 191.255.255.255.
  - **Máscara de Sub-rede:** 255.255.0.0 (ou /16).
  - **IP da Rede:** Os primeiros 16 bits são usados para o ID da rede, e os 16 bits restantes são usados para o ID do host.
  - **IPs Disponíveis:** Aproximadamente 65.000 endereços por rede (2^16).
  - **Uso:** Redes de tamanho médio, como universidades e empresas.
  - **Exemplo:** Em `172.16.1.2`, a rede é `172.16.0.0` e o host é `1.2`.

- **Classe C:**
  - **Intervalo:** 192.0.0.0 a 223.255.255.255.
  - **Máscara de Sub-rede:** 255.255.255.0 (ou /24).
  - **IP da Rede:** Os primeiros 24 bits são usados para o ID da rede, e os 8 bits restantes são usados para o ID do host.
  - **IPs Disponíveis:** Até 254 endereços por rede (2^8 - 2).
  - **Uso:** Redes pequenas, como redes domésticas ou pequenas empresas.
  - **Exemplo:** Em `192.168.1.10`, a rede é `192.168.1.0` e o host é `10`.

- **Classes D e E:**
  - **Classe D (Multicast):**
    - **Intervalo:** 224.0.0.0 a 239.255.255.255.
    - Usado para comunicação de **multicast**, ou seja, comunicação de um único remetente para múltiplos destinatários.
  - **Classe E (Reservado):**
    - **Intervalo:** 240.0.0.0 a 255.255.255.255.
    - Reservado para **uso futuro** ou **experimentação**.

- **Uso do 0 e 255 no IPv4:**
  - **0:** Em um endereço de rede, o `0` é usado para identificar a rede em si, ou seja, é o endereço de rede que define o início de um intervalo de endereços. Exemplo: `192.168.1.0` é a rede, não um host.
  - **255:** O `255` é usado no endereço de **broadcast**, ou seja, é um endereço especial para enviar pacotes a todos os dispositivos de uma rede. Exemplo: `192.168.1.255` envia uma mensagem para todos os dispositivos na rede `192.168.1.0/24`.

### IPv6 (Internet Protocol version 6)
- **Tamanho:** 128 bits, representado no formato hexadecimal, separado por dois pontos (ex.: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
- **Estrutura:**
  - **Prefixo da Rede:** Define a rede a que pertence.
  - **ID de Interface:** Identifica o dispositivo específico dentro da rede.
- **Características:**
  - Suporta um número maior de dispositivos devido ao tamanho do endereço.
  - Possui recursos nativos para segurança e mobilidade.

