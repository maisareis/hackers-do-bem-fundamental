# Módulo 12 – Resposta a Incidentes e Protocolos Seguros

## Aula 2 – Protocolos Seguros

## 📌 Ataques de rede e protocolos seguros

### Segurança de Porta com DHCP Snooping (DHCP Snooping Port Security)
- Recurso contra ataques de Rogue DHCP
- Garante que apenas servidores legítimos atribuam IPs
- Funcionamento:
  - Identificação de portas confiáveis e não confiáveis
  - Construção da tabela DHCP snooping
  - Verificação de pacotes DHCP subsequentes

### Domain Hijacking
- Ataque para assumir controle de um domínio
- Etapas:
  - Acesso à conta do registrante ou provedor
  - Transferência ou modificação de DNS
  - Redirecionamento de tráfego
  - Extorsão ou chantagem
  - Monitoramento e ocultação

### Domain Poisoning
- Ataque a servidores DNS redirecionando usuários para sites maliciosos
- Explora vulnerabilidades nos servidores DNS
- Etapas:
  - Identificação do alvo
  - Interceptação do tráfego DNS
  - Falsificação de respostas DNS
  - Inserção de registros falsos no cache DNS
  - Redirecionamento de tráfego
  - Exploração do redirecionamento

### DNS Security Extensions (DNSSEC)
- Camada adicional de proteção contra DNS Poisoning
- Funcionamento:
  - Assinatura digital dos registros DNS
  - Cadeia de confiança
  - Armazenamento das chaves públicas
  - Resposta DNS com assinaturas
  - Verificação das assinaturas
  - Indicação de suporte DNSSEC

### Lightweight Directory Access Protocol Secure (LDAPS)
- Usa criptografia para proteger dados durante transmissão
- Amplamente usado em ambientes corporativos
- Funcionamento:
  1. Configuração do servidor LDAP
  2. Solicitação de conexão segura
  3. Estabelecimento da conexão segura
  4. Verificação do certificado
  5. Autenticação do cliente
  6. Troca de dados criptografada

### Network Time Protocol (NTP)
- Sincroniza relógios dos dispositivos na rede
- Funcionamento:
  - Seleção de servidores NTP
  - Sincronização inicial
  - Atualização periódica

### Network Time Security (NTS)
- Extensão do NTP com camada de segurança adicional
- Transações NTP protegidas com criptografia
- Funcionamento:
  - Estabelecimento de segurança
  - Autenticação do servidor
  - Proteção contra spoofing
  - Integridade dos dados de tempo

### Simple Network Management Protocol (SNMP)
- Protocolo de gerenciamento de rede IP
- Funcionamento:
  - Agentes SNMP nos dispositivos
  - Gerenciadores SNMP
  - Management Information Base (MIB)
  - Operações: Get, Set, Trap, GetNext

#### SNMPv2
- Atualização do SNMPv1
- Novas operações: GetBulk e Inform
- Acesso a tabelas MIB
- Ainda usa Community Strings

#### SNMPv3
- Versão segura do protocolo
- Autenticação forte: MD5, SHA
- Criptografia: DES, AES
- Modelos de segurança: noAuthNoPriv, authNoPriv, authPriv
- Autenticação baseada em usuários e grupos

### Secure Sockets Layer (SSL) e Transport Layer Security (TLS)
- SSL: protocolo para conexão segura entre cliente e servidor
- TLS: evolução do SSL
  - TLS 1.1: 2006
  - TLS 1.2: 2008
  - TLS 1.3: 2018

### SSH FTP (SFTP) e FTP Over SSL (FTPS)
- Protocolos para transferência segura de arquivos

#### SFTP
- Conexão segura via SSH
- Autenticação do cliente antes da transferência
- Criptografia durante transferência
- Integração com sistema de arquivos

### SMTPS, POP3S, IMAPS e S/MIME
- Proteção para comunicações de e-mail

#### SMTPS (Secure SMTP)
- Versão segura do SMTP
- Porta TCP 465
- Envio seguro de e-mails

#### POP3S (Secure POP3)
- Versão segura do POP3
- Porta TCP 995
- Cliente baixa e-mails de forma segura

#### IMAPS (Secure IMAP)
- Versão segura do IMAP
- Porta TCP 993
- Cliente acessa e-mails no servidor de forma segura

#### S/MIME (Secure/Multipurpose Internet Mail Extensions)
- Padrão de criptografia e assinatura digital para e-mails
- Segurança com chaves públicas
- Integridade e autenticidade via assinatura digital

### Transport Layer Security Virtual Private Network (TLS VPN)
- VPN com conexão segura via TLS
- Criptografia e autenticação garantem confidencialidade, integridade e autenticidade
- Funcionamento:
  - Handshake TLS
  - Autenticação
  - Criptografia
  - Túnel VPN
  - Roteamento seguro
  - Acesso remoto e site-to-site

### Internet Protocol Security (IPSec)
- Conjunto de protocolos para proteção de comunicações na rede
- Protocolos principais:
  - **AH (Authentication Header)**: autenticação
  - **ESP (Encapsulation Security Payload)**: criptografia + autenticação

#### Modos de implementação
- **Modo Túnel**: pacote inteiro encapsulado em novo pacote IP
- **Modo Transporte**: apenas payload encapsulado com AH/ESP

### Secure Shell (SSH)
- Protocolo para conexões seguras entre dispositivos
- Funcionamento:
  - Conexão segura via criptografia
  - Autenticação: senha, chave pública, chave de host
  - Chaves criptográficas (pública/privada)
  - Criptografia de dados
  - Operações remotas seguras
  - Porta padrão: TCP 22

---

## 💡 Meus insights
- **DHCP Snooping** é essencial para evitar servidores DHCP falsos. Sem ele, atacante pode redirecionar tráfego.
- **Domain Hijacking** é um dos piores pesadelos. Perder o controle do domínio = perder o negócio.
- **DNSSEC** resolve o problema de cache poisoning, mas ainda não é amplamente adotado.
- **LDAPS** deve ser usado sempre. LDAP puro envia credenciais em texto claro.
- **NTP** parece inofensivo, mas sincronização de tempo é crítica para logs e autenticação Kerberos.
- **NTS** adiciona segurança ao NTP. Evita que atacante manipule o tempo do sistema.
- **SNMPv3** é obrigatório se você for usar SNMP. v1 e v2 são inseguros.
- **TLS 1.3** é mais rápido e seguro que versões anteriores. Remove suporte a algoritmos fracos.
- **SFTP vs FTPS**: SFTP é sobre SSH, FTPS é FTP com TLS. SFTP é mais comum hoje.
- **SMTPS/POP3S/IMAPS**: sempre usar versões seguras. E-mail sem criptografia é como cartão postal.
- **S/MIME** garante que o e-mail veio mesmo de quem diz e não foi alterado.
- **TLS VPN** é prática porque usa porta 443 (mesma do HTTPS), dificultando bloqueio.
- **IPSec** é complexo de configurar, mas é o padrão para VPNs site-to-site.
- **SSH** substituiu telnet e rlogin. Qualquer administrador de sistemas vive no SSH.