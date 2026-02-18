# Aula 4 – Análise de Tráfego TCP/IP

## 📌 Ferramentas de linha de comando
- `ipconfig` / `ifconfig` → mostra configuração de rede
- `ping` → testa conectividade
- `arp` → mostra mapeamento IP-MAC (útil para detectar ataques man-in-the-middle)
- `traceroute` / `tracert` → mostra o caminho dos pacotes até o destino
- `netstat` → mostra portas abertas e conexões ativas
- `nslookup` / `dig` → consulta DNS

## 📌 Nmap
Scanner de rede mais popular. Identifica hosts ativos, portas abertas e serviços em execução.

## 📌 Wireshark
Captura e analisa pacotes de rede em tempo real. Mostra o que está trafegando na rede.

---

## 💡 Meus insights
- **Comandos de rede:** 
  - `ipconfig/ifconfig`: básico mas essencial. Saber o IP da máquina é o primeiro passo.
  - `ping`: testar conectividade, ver se o host tá vivo.
  - `arp -a`: vi que serve pra detectar ataque man-in-the-middle. Se aparecer MAC estranho, algo errado.
  - `traceroute/tracert`: ver o caminho que os pacotes fazem. Útil pra ver onde tá travando.
  - `netstat -an`: mostra portas abertas. Se tiver porta que não deveria, suspeita.
  - `nslookup/dig`: consultar DNS. Aprendi que dá até ver se o site foi sequestrado.

- **Nmap:** 
  - Ferramenta poderosa! `-sS` stealth, `-sV` versão do serviço, `-O` sistema operacional.
  - Quero praticar mais, decorar os comandos principais.

- **Wireshark:** 
  - Ver os pacotes passando em tempo real é fascinante.
  - Filtros como `tcp.port == 80`, `ip.addr == 192.168.1.1` ajudam a não se perder.
  - Dá pra ver requisição HTTP, DNS, até senha se não tiver criptografia (assustador!).

- **Na prática:** 
  - Ping e traceroute são os primeiros passos quando alguém fala "a internet caiu".
  - Netstat é meu aliado pra ver se tem conexão suspeita.

- **Como Purple Team:** 
  - Wireshark vai ser essencial pra analisar tráfego de ataque e ver como o invasor se move.
  - Nmap pra simular reconhecimento e ver o que a defesa detecta.

- **Curiosidade:** 
  - Aprendi que HTTP é texto puro, dá pra ler tudo. HTTPS já é criptografado. Por isso que hoje em dia tudo é HTTPS.

- **Dúvida:** 
  - No Wireshark, como filtrar só tráfego suspeito sem ter que olhar pacote por pacote?
