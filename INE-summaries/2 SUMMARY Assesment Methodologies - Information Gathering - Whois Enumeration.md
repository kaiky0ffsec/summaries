[15/01/2026]
Alvo: http://hackersploit.org/

**O que é Whois? (abrangente)**
> WHOIS é um protocolo da pilha TCP/IP específico para consultar informações de contato e DNS sobre entidades na internet. Uma entidade na internet pode ser um nome de domínio, um endereço IP ou um AS.

O que é **Whois Enumeration?**
	São pesquisas para identificar informações sobre um determinado domínio.

## Ferramentas Kali Linux & CLI

```cpp
whois hackersploit.org
```

também é possível usar o **whois** de outra maneira:

Capturando o IP do DNS
```cpp
host hackersploit.org
```

Retorna
```cpp
has address 172.67.202.99
has address 104.21.44.180
```

Após capturar o IP, façamos um **whois**
```cpp
whois 172.67.202.99
```