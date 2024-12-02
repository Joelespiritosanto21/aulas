# Endereços IP Privados

Os endereços **IP privados** são utilizados em redes internas e não são roteáveis pela Internet. Estes endereços são definidos pelo **RFC 1918** para IPv4 e estão reservados para uso em redes locais.

## Classes de Endereços IP Privados

Os endereços IP privados são atribuídos em diferentes classes, com gamas específicas de endereços. Aqui estão as classes e as gamas de endereços privados:

### Classe A (10.0.0.0 a 10.255.255.255)

| Classe A               | Gama de Endereços Privados        | Notação CIDR    | Total de Endereços |
|------------------------|-----------------------------------|-----------------|--------------------|
| **Classe A**           | 10.0.0.0 - 10.255.255.255        | 10.0.0.0/8      | 16.777.216         |

- **Descrição:** A classe A oferece uma vasta gama de endereços privados, com um total de **16.777.216** endereços possíveis.

### Classe B (172.16.0.0 a 172.31.255.255)

| Classe B               | Gama de Endereços Privados        | Notação CIDR    | Total de Endereços |
|------------------------|-----------------------------------|-----------------|--------------------|
| **Classe B**           | 172.16.0.0 - 172.31.255.255       | 172.16.0.0/12   | 1.048.576          |

- **Descrição:** A classe B fornece um intervalo menor em comparação com a classe A, com **1.048.576** endereços privados possíveis.

### Classe C (192.168.0.0 a 192.168.255.255)

| Classe C               | Gama de Endereços Privados        | Notação CIDR    | Total de Endereços |
|------------------------|-----------------------------------|-----------------|--------------------|
| **Classe C**           | 192.168.0.0 - 192.168.255.255     | 192.168.0.0/16  | 65.536             |

- **Descrição:** A classe C oferece um intervalo mais restrito, com **65.536** endereços privados possíveis, sendo a mais comum para redes domésticas e pequenas empresas.

## Resumo das Classes e Gamase de Endereços Privados

| Classe        | Intervalo de Endereço Privado     | Notação CIDR  | Total de Endereços |
|---------------|-----------------------------------|---------------|--------------------|
| **Classe A**  | 10.0.0.0 - 10.255.255.255         | 10.0.0.0/8    | 16.777.216         |
| **Classe B**  | 172.16.0.0 - 172.31.255.255       | 172.16.0.0/12 | 1.048.576          |
| **Classe C**  | 192.168.0.0 - 192.168.255.255     | 192.168.0.0/16| 65.536             |

## Conclusão

Os **endereços IP privados** são utilizados para redes internas e não são roteáveis pela Internet. A sua utilização depende da classe e da gama de endereços atribuída:

- **Classe A**: Mais adequada para grandes redes internas, com um total de 16.777.216 endereços.
- **Classe B**: Usada em redes de tamanho médio, com 1.048.576 endereços.
- **Classe C**: Ideal para redes menores, com 65.536 endereços disponíveis.
