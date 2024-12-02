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
  - Classe A: Redes grandes (1.0.0.0 - 126.255.255.255).
  - Classe B: Redes médias (128.0.0.0 - 191.255.255.255).
  - Classe C: Redes pequenas (192.0.0.0 - 223.255.255.255).
  - Classes D e E: Usadas para multicast e pesquisas experimentais.

### IPv6 (Internet Protocol version 6)
- **Tamanho:** 128 bits, representado no formato hexadecimal, separado por dois pontos (ex.: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
- **Estrutura:**
  - **Prefixo da Rede:** Define a rede a que pertence.
  - **ID de Interface:** Identifica o dispositivo específico dentro da rede.
- **Características:**
  - Suporta um número maior de dispositivos devido ao tamanho do endereço.
  - Possui recursos nativos para segurança e mobilidade.
