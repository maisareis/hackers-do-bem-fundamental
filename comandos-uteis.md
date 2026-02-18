# 🛠️ Comandos Úteis

## 🔹 Redes (Windows/Linux)
| Comando | Função |
|---------|--------|
| `ipconfig` (Windows) | Mostra configuração de rede |
| `ifconfig` (Linux) | Mostra configuração de rede |
| `ping` | Testa conectividade |
| `arp -a` | Mostra tabela ARP (mapeamento IP-MAC) |
| `tracert` (Windows) | Mostra caminho dos pacotes |
| `traceroute` (Linux) | Mostra caminho dos pacotes |
| `netstat -an` | Mostra portas abertas e conexões |
| `nslookup` | Consulta DNS |
| `dig` | Consulta DNS (mais detalhado) |

## 🔹 Nmap
`nmap 192.168.1.1` - Scan básico  
`nmap -sV 192.168.1.1` - Detecção de versão de serviços  
`nmap -p- 192.168.1.1` - Scan de todas as portas  
`nmap -O 192.168.1.1` - Detecção de sistema operacional  
`nmap 192.168.1.0/24` - Scan de rede inteira  
`nmap -sS 192.168.1.1` - Scan silencioso (SYN stealth)

## 🔹 Wireshark
**Atalhos:** `Ctrl+K` (configurar captura), `Ctrl+E` (iniciar/parar), `Ctrl+F` (buscar)  
**Filtros:** `tcp.port == 80`, `ip.addr == 192.168.1.1`, `http`, `dns`, `tcp`, `udp`

## 🔹 Linux
`systemctl status ssh` - Status do serviço  
`systemctl start ssh` - Iniciar serviço  
`systemctl stop ssh` - Parar serviço  
`systemctl enable ssh` - Habilitar na inicialização  
`systemctl disable ssh` - Desabilitar na inicialização  
`chmod 755 arquivo` - Permissão rwxr-xr-x  
`chmod 644 arquivo` - Permissão rw-r--r--  
`chown usuario:grupo arquivo` - Alterar dono/grupo  
`ps aux` - Listar processos  
`top` / `htop` - Monitorar processos  
`kill -9 PID` - Matar processo  
`ifconfig` - Configuração de rede  
`iwconfig` - Configuração wireless  
`ss -tuln` - Portas abertas

## 🔹 Windows
`net user` - Listar usuários  
`net user usuario senha /add` - Criar usuário  
`net localgroup administradores usuario /add` - Adicionar a admin  
`net user usuario /delete` - Deletar usuário  
`netsh advfirewall show allprofiles` - Ver firewall  
`netsh advfirewall set allprofiles state on` - Ativar firewall  
`netsh advfirewall set allprofiles state off` - Desativar firewall  
`systeminfo` - Informações do sistema  
`msinfo32` - Informações detalhadas  
`ipconfig /all` - Configuração completa de rede  
`ping -t 8.8.8.8` - Ping contínuo  
`tracert google.com` - Rota até o destino  
`pathping google.com` - Diagnóstico de rota  
`nslookup google.com` - Consulta DNS

## 🔹 Troubleshooting Rápido
`ping 8.8.8.8` - Testa conexão com internet  
`ping 192.168.1.1` - Testa conexão com gateway  
`tracert google.com` - Verifica onde está travando  
`netstat -an | findstr :80` (Windows) - Ver porta 80  
`netstat -an | grep :80` (Linux) - Ver porta 80  
`nmap -p 80 localhost` - Testa porta específica  
`nslookup google.com 8.8.8.8` - Usa DNS do Google  
`ipconfig /flushdns` (Windows) - Limpa cache DNS

## 🔹 Dicas de Segurança
- 🔒 Sempre use `ssh` em vez de `telnet`
- 🔒 Prefira `scp` ou `sftp` em vez de `ftp`
- 🔒 No Wireshark, use filtros para não se perder nos pacotes
- 🔒 No nmap, scans muito agressivos podem ser detectados por IDS/IPS
- 🔒 Mantenha seus sistemas atualizados (`sudo apt update && sudo apt upgrade` no Linux)

> 💡 **Lembrete:** A prática leva à perfeição! Teste esses comandos em laboratório antes de usar em produção.