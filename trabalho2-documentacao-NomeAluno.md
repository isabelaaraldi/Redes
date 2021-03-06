# Trabalho 2: Integração de habilidades - 2022/1
**Disciplina: Redes de Computadores**

**Curso: Engenharia de Computação / Elétrica**

**Nome/RA:Isabela Araldi 1707175


## Tarefa 1:  Sub-Redes
| Sub- Rede |             IPv6 - Sub-Rede            |  IPv4 - Sub-Rede  |  IPv4 - Máscara   | IPv4 - Broadcast  |    
|:---------:|:--------------------------------------:|:-----------------:|:-----------------:|:-----------------:|
| Matriz    | 2001:DB8:ACAD:**4B**00::/64 | 200.200.75.0   | 255.255.255.192 | 200.200.75.63  |
| Filial 1  | 2001:DB8:ACAD:**4B**01::/64 | 200.200.75.64  | 255.255.255.224 | 200.200.75.95  |
| Filial 2  | 2001:DB8:ACAD:**4B**02::/64 | 200.200.75.96  | 255.255.255.224 | 200.200.75.127 |
| Filial 3  | 2001:DB8:ACAD:**4B**03::/64 | 200.200.75.128 | 255.255.255.224 | 200.200.75.159 |
| Filial 4  | 2001:DB8:ACAD:**4B**04::/64 | 200.200.75.160 | 255.255.255.224 | 200.200.75.192 |
| Filial 5  | 2001:DB8:ACAD:**4B**05::/64 | 200.200.75.192 | 255.255.255.224 | 200.200.75.223 |
| pb-vit    | 2001:DB8:ACAD:**4B**FF::0:0/112 | 200.200.75.224 | 255.255.255.252 | 200.200.75.227 |
| vit-fb    | 2001:DB8:ACAD:**4B**FF::1:0/112 | 200.200.75.228 | 255.255.255.252 | 200.200.75.231 |
| fb-ita    | 2001:DB8:ACAD:**4B**FF::2:0/112 | 200.200.75.232 | 255.255.255.252 | 200.200.75.235 |
| ita-pb    | 2001:DB8:ACAD:**4B**FF::3:0/112 | 200.200.75.236 | 255.255.255.252 | 200.200.75.239 |
| cv-ita    | 2001:DB8:ACAD:**4B**FF::4:0/112  | 200.200.75.240 | 255.255.255.252 | 200.200.75.243 |


## Tarefa 2: Endereçamento de Dispositivos
| Dispositivo           | Interface | IPv4 | IPv4 - Máscara | IPv4 - Gateway | IPv6/Prefixo | IPv6 - Gateway |
|-----------------------|-----------|------|----------------|----------------|--------------|----------------|
| PC1 | NIC    | 200.200. 75.3     | 255.255.255.192  | 200.200. 75.1 | 2001:DB8:ACAD:4B00::3/64 | 2001:DB8:ACAD:4B00::1/64  |
| PC2 | NIC    |200.200. 75.4      |  255.255.255.192         |200.200. 75.1  | 2001:DB8:ACAD:4B00::4/64 |2001:DB8:ACAD:4B00::1/64                |
| PC3 | NIC    | 200.200. 75.67     | 255.255.255.224          | 200.200. 75.65  | 2001:DB8:ACAD:4B01::3/64   | 2001:DB8:ACAD:4B01::1/64               |
| PC4 | NIC    | 200.200. 75.68     | 255.255.255.224          | 200.200. 75.65            | 2001:DB8:ACAD:4B01::4/64             |  2001:DB8:ACAD:4B01::1/64 |
| PC5 | NIC    | 200.200. 75.99     |  255.255.255.224         | 200.200. 75.97            | 2001:DB8:ACAD:4B02::3/64             |  2001:DB8:ACAD:4B02::1/64              |
| PC6 | NIC    | 200.200. 75.100     |   255.255.255.224        | 200.200. 75.97            |2001:DB8:ACAD:4B02::4/64              |2001:DB8:ACAD:4B02::1/64               |
| Switch-Matriz | SVI    | 200.200. 75.2     |255.255.255.192           |  200.200. 75.1              |              |                |
| Switch-Filial1 | SVI    | 200.200. 75.66     |255.255.255.224          |  200.200. 75.65              |              |                |
| Switch-Filial2 | SVI    | 200.200. 75.98     |255.255.255.224                | 200.200. 75.97               |              |                |
| Roteador-Pato Branco  | Fa0/0 |200.200. 75.1      |  255.255.255.224              |              |2001:DB8:ACAD:4B00::1/64      FE80::1        |                |
| Roteador-Pato Branco  | Se0/0/0 | 200.200. 75.225     |  255.255.255.252              |                |2001:DB8:ACAD:4BFF::0:1/112    EUI-64          |                |
| Roteador-Pato Branco  | Se0/0/1 |200.200. 75.238      | 255.255.255.252               |                | 2001:DB8:ACAD:4BFF::3:2/112     EUI-64        |                |
| Roteador-Fco. Beltrão | Fa0/0     | 200.200. 75.65     | 255.255.255.224               |                |2001:DB8:ACAD:4B01::1/64       FE80::1       |                |
| Roteador-Fco. Beltrão | Se0/0/0        |200.200. 75.233                | 255.255.255.252               |              | 2001:DB8:ACAD:4BFF::2:1/112    EUI-64           |
| Roteador-Fco. Beltrão | Se0/0/1 | 200.200. 75.230     |255.255.255.252                |                |  2001:DB8:ACAD:4BFF::1:2/112     EUI-64       |                |
| Roteador-Vitorino     | Se0/0/0 | 200.200. 75.229     | 255.255.255.252               |                |  2001:DB8:ACAD:4BFF::1:1/112    EUI-64        |                |
| Roteador-Vitorino     | Se0/0/1 | 200.200. 75.226     |255.255.255.252                |                | 2001:DB8:ACAD:4BFF::0:2/112       EUI-64      |                |
| Roteador-Itapejara    | Se0/0/0 | 200.200. 75.237     | 255.255.255.252               |                |  2001:DB8:ACAD:4BFF::3:1/112     EUI-64       |                |
| Roteador-Itapejara    | Se0/0/1 |  200.200. 75.234    | 255.255.255.252               |                | 2001:DB8:ACAD:4BFF::2:2/112     EUI-64        |                |
| Roteador-Itapejara    | Fa0/1   | 200.200. 75.241     |  255.255.255.252              |                | 2001:DB8:ACAD:4BFF::4:1/112     EUI-64        |                |
| Roteador-Coronel      | Fa0/0   | 200.200. 75.97     | 255.255.255.224               |                | 2001:DB8:ACAD:4B02::1/64     FE80::1        |                |
| Roteador-Coronel      | Se0/0/1 |     |                |                |              |                |
| Roteador-Coronel      | Fa0/1  |200.200. 75.242       | 255.255.255.252               |                |  2001:DB8:ACAD:4BFF::4:2/112    EUI-64        |                |

## Tarefa 3: Tabela de Roteamento
### Roteador Pato Branco
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|----------------|---------|----------|--------------------|
| 200.200. 75.228                |255.255.255.252         | 200.200. 75.226         | SE0/0/0                   |
| 200.200. 75.232                |255.255.255.252         | 200.200. 75.226         | SE0/0/0                   |
| 200.200. 75.64                |255.255.255.224         | 200.200. 75.226         | SE0/0/0                   |
| 200.200. 75.240                |255.255.255.252         | 200.200. 75.226         | SE0/0/0                   |
| 200.200. 75.96                |255.255.255.224         | 200.200. 75.226         | SE0/0/0                   |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
|2001:DB8:ACAD:4BFF::1:0/112                 | 2001:DB8:ACAD:4BFF::0:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::2:0/112                 | 2001:DB8:ACAD:4BFF::0:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4B01::/64                 | 2001:DB8:ACAD:4BFF::0:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::4:0/112                 | 2001:DB8:ACAD:4BFF::0:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4B02::/64                 | 2001:DB8:ACAD:4BFF::0:2/112         | SE0/0/0                   |

### Roteador Francisco Beltrao
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|----------------|---------|----------|--------------------|
| 200.200. 75.0                |255.255.255.192       | 200.200. 75.234         | SE0/0/0                   |
|200.200. 75.224                |255.255.255.252         | 200.200. 75.234         | SE0/0/0                   |
|200.200. 75.240               |255.255.255.252         | 200.200. 75.234         | SE0/0/0                   |
|200.200. 75.96                |255.255.255.224         | 200.200. 75.234       | SE0/0/0                   |
|200.200. 75.236                |255.255.255.252         | 200.200. 75.234         | SE0/0/0                   |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
|2001:DB8:ACAD:4B00::/64                 | 2001:DB8:ACAD:4BFF::2:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::0:0/112                 | 2001:DB8:ACAD:4BFF::2:2/112          | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::4:0/112                | 2001:DB8:ACAD:4BFF::2:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4B02::/64                 | 2001:DB8:ACAD:4BFF::2:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::3:0/112                 | 2001:DB8:ACAD:4BFF::2:2/112         | SE0/0/0                   |


### Roteador Vitorino
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|----------------|---------|----------|--------------------|
| 200.200. 75.0               |255.255.255.192       | 200.200. 75.230        | SE0/0/0                   |
| 200.200. 75.64              |255.255.255.224         | 200.200. 75.230         | SE0/0/0                   |
| 200.200. 75.96                |255.255.255.224         | 200.200. 75.230       | SE0/0/0                   |
| 200.200. 75.232                |255.255.255.252         | 200.200. 75.230        | SE0/0/0                   |
| 200.200. 75.236                |255.255.255.252        | 200.200. 75.230        | SE0/0/0                   |
| 200.200. 75.240                |255.255.255.252        | 200.200. 75.230        | SE0/0/0                   |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
|2001:DB8:ACAD:4B00::/64                 | 2001:DB8:ACAD:4BFF::1:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4B01::/64                | 2001:DB8:ACAD:4BFF::1:2/112        | SE0/0/0                   |
|2001:DB8:ACAD:4B02::/64                | 2001:DB8:ACAD:4BFF::1:2/112        | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::2:0/112                | 2001:DB8:ACAD:4BFF::1:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::3:0/112               | 2001:DB8:ACAD:4BFF::1:2/112        | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::4:0/112               | 2001:DB8:ACAD:4BFF::1:2/112        | SE0/0/0                   |


### Roteador Itapejara D'Oeste
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|----------------|---------|----------|--------------------|
| 200.200. 75.0               |255.255.255.192       | 200.200. 75.238        | SE0/0/0                   |
| 200.200. 75.64              |255.255.255.224         | 200.200. 75.238         | SE0/0/0                   |
| 200.200. 75.96                |255.255.255.224         | 200.200. 75.242       | SE0/0/0                   |
| 200.200. 75.224                |255.255.255.252         | 200.200. 75.238        | SE0/0/0                   |
| 200.200. 75.228                |255.255.255.252        | 200.200. 75.238        | SE0/0/0                   |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
|2001:DB8:ACAD:4B00::/64                 | 2001:DB8:ACAD:4BFF::3:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4B01::/64                | 2001:DB8:ACAD:4BFF::3:2/112        | SE0/0/0                   |
|2001:DB8:ACAD:4B02::/64                | 2001:DB8:ACAD:4BFF::4:2/112        | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::0:0/112                | 2001:DB8:ACAD:4BFF::3:2/112         | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::1:0/112               | 2001:DB8:ACAD:4BFF::3:2/112        | SE0/0/0                   |


### Roteador Coronel Vivida
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|----------------|---------|----------|--------------------|
| 200.200. 75.0               |255.255.255.192       | 200.200. 75.241        | SE0/0/0                   |
| 200.200. 75.64              |255.255.255.224         | 200.200. 75.241         | SE0/0/0                   |
| 200.200. 75.224                |255.255.255.252         | 200.200. 75.241       | SE0/0/0                   |
| 200.200. 75.228                |255.255.255.252         | 200.200. 75.241        | SE0/0/0                   |
| 200.200. 75.232                |255.255.255.252        | 200.200. 75.241        | SE0/0/0                   |
| 200.200. 75.236                |255.255.255.252        | 200.200. 75.241        | SE0/0/0                   |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
|2001:DB8:ACAD:4B00::/64                 | 2001:DB8:ACAD:4BFF::4:1/112         | SE0/0/0                   |
|2001:DB8:ACAD:4B01::/64                | 2001:DB8:ACAD:4BFF::4:1/112        | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::0:0/112               | 2001:DB8:ACAD:4BFF::4:1/112        | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::1:0/112                | 2001:DB8:ACAD:4BFF::4:1/112         | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::2:0/112               | 2001:DB8:ACAD:4BFF::4:1/112        | SE0/0/0                   |
|2001:DB8:ACAD:4BFF::3:0/112               | 2001:DB8:ACAD:4BFF::4:1/112        | SE0/0/0                   |

## Topologia - Packet Tracer
- [ ] ![Trabalho2-Topologia-IsabelaAraldi](Trabalho2_IsabelaAraldi.pkt)


## Arquivos de Configuração dos Dispositivos Intermediários (roteadores e switches)
- [ ] ![Roteador Pato Branco](r-pb-IsabelaAraldi.txt)
- [ ] ![Roteador Francisco Beltrão](r-fb-IsabelaAraldi.txt)
- [ ] ![Roteador Vitorino](r-vit-IsabelaAraldi.txt)
- [ ] ![Roteador Itapejara D'Oeste](r-ita-IsabelaAraldi.txt)
- [ ] ![Roteador Coronel Vivida](r-cv-IsabelaAraldi.txt)
- [ ] ![Switch Pato Branco](sw-pb-IsabelaAraldi.txt)
- [ ] ![Switch Francisco Beltrão](sw-fb-IsabelaAraldi.txt)
- [ ] ![Switch Coronel Vivida](sw-cv-IsabelaAraldi.txt)


