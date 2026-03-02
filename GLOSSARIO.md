# 📖 Glossário de Termos - Hackers do Bem (Módulos 1 a 12)

## 🎓 Módulo 1 – Princípios de Segurança da Informação

### Profissionais e Times
| Termo | Significado |
|-------|-------------|
| **CISO** | Chief Information Security Officer - líder sênior de segurança da informação |
| **DPO** | Data Protection Officer - garante privacidade de dados em conformidade com a lei |
| **Analista de Segurança** | Profissional que gerencia infraestrutura de TI e responde a incidentes |
| **Hacker Ético (Pentester)** | Profissional que invade sistemas com autorização para identificar falhas |
| **Analista de Forense Digital** | Atua em investigações com evidências digitais |
| **NOC** | Network Operations Center - monitora e mantém infraestrutura de rede |
| **SOC** | Security Operations Center - monitora, detecta e responde a ameaças |
| **CSIRT** | Computer Security Incident Response Team - equipe de resposta a incidentes |
| **Blue Team** | Time de defesa e monitoramento |
| **Red Team** | Time que simula ataques |
| **Purple Team** | Integra Blue e Red para aprimoramento contínuo |
| **White Team** | Valida resultados de testes (competições/CTFs) |

### Metodologias Ágeis
| Termo | Significado |
|-------|-------------|
| **Kanban** | Metodologia visual para controle de fluxo de trabalho |
| **XP (Extreme Programming)** | Metodologia com foco em qualidade, TDD e programação em pares |
| **Scrum** | Framework ágil com sprints, Scrum Master e Product Owner |
| **DevOps** | Integração entre desenvolvimento e operações |
| **DevSecOps** | Integração da segurança ao DevOps |

### Atores de Ameaça
| Termo | Significado |
|-------|-------------|
| **Black Hat** | Hacker malicioso que age com fins criminosos |
| **White Hat** | Hacker ético que age com autorização |
| **Gray Hat** | Atua na fronteira da legalidade, revela falhas sem autorização |
| **Blue Hat** | Contratado para testar sistemas internos |
| **Script Kiddie** | Usa ferramentas prontas sem conhecimento profundo |
| **Hacktivist** | Age por causas políticas, sociais ou ideológicas |

### Engenharia Social
| Termo | Significado |
|-------|-------------|
| **Phishing** | Mensagem fraudulenta para roubar informações |
| **Spear Phishing** | Phishing direcionado a alvos específicos |
| **Whaling** | Phishing focado em executivos de alto escalão |
| **Vishing** | Phishing por chamada telefônica |
| **Spam** | Mensagens em massa não solicitadas |
| **Hoax** | Boato ou mensagem falsa compartilhada |
| **Coleta de Credenciais** | Páginas falsas para capturar logins e senhas |
| **Campanha de Influência** | Manipulação de opiniões e percepções |

---

## 🦠 Módulo 2 – Ameaças, Malwares e Controles

### Tipos de Malware (por vetor)
| Termo | Significado |
|-------|-------------|
| **Vírus** | Malware que se anexa a arquivos e se espalha |
| **Worm** | Autônomo, se replica por redes sem hospedeiro |
| **Trojan (Cavalo de Troia)** | Disfarçado de software legítimo |
| **PUP** | Potentially Unwanted Program - programa potencialmente indesejado |

### Tipos de Malware (por propósito)
| Termo | Significado |
|-------|-------------|
| **Spyware** | Coleta informações do usuário sem consentimento |
| **Keylogger** | Registra teclas digitadas |
| **Adware** | Exibe anúncios invasivos |
| **Tracking Cookie** | Cookie que rastreia navegação |

### Tipos de Malware (por payload)
| Termo | Significado |
|-------|-------------|
| **Backdoor** | Porta dos fundos para acesso remoto |
| **RAT** | Remote Access Trojan - controle remoto |
| **Rootkit** | Esconde atividades maliciosas no sistema |
| **Ransomware** | Criptografa dados e exige resgate |
| **Cripto-Malware** | Criptografa dados sem necessariamente pedir resgate |
| **Bomba Lógica** | Ativada por gatilho específico |

### Análise de Indicadores
| Termo | Significado |
|-------|-------------|
| **Sandbox** | Ambiente isolado para executar arquivos suspeitos |
| **FIM** | File Integrity Monitoring - monitora alterações em arquivos |
| **Falso Positivo** | Alerta incorreto de ameaça |
| **Falso Negativo** | Ameaça real não detectada |

### Controles de Segurança (Categorias)
| Termo | Significado |
|-------|-------------|
| **Controle Técnico** | Implementado via software/hardware (firewall, antivírus) |
| **Controle Operacional** | Práticas diárias (políticas de senha, treinamento) |
| **Controle Gerencial** | Estratégias de longo prazo (análise de risco, BCP) |

### Controles de Segurança (Tipos Funcionais)
| Termo | Significado |
|-------|-------------|
| **Controle Preventivo** | Evita que incidentes ocorram |
| **Controle Detectivo** | Identifica incidentes em andamento |
| **Controle Corretivo** | Restaura normalidade após incidente |
| **Controle Físico** | Barreiras físicas, fechaduras, CFTV |
| **Controle Dissuasor** | Desencoraja ações maliciosas |
| **Controle de Compensação** | Alternativa quando controle principal não é viável |

### Fontes de Ameaça
| Termo | Significado |
|-------|-------------|
| **Ameaça Interna** | Origina-se dentro da organização |
| **Ameaça Externa** | Origina-se fora da organização |
| **Surface Web** | Internet indexada por buscadores |
| **Deep Web** | Conteúdo não indexado (acesso controlado) |
| **Dark Web** | Redes criptografadas com anonimato |
| **Dark Net** | Redes privadas e criptografadas |

---

## 🔍 Módulo 3 – Técnicas Utilizadas na Identificação de Ameaças

### Avaliações de Segurança
| Termo | Significado |
|-------|-------------|
| **Verificação de Vulnerabilidade** | Identificação de falhas de segurança |
| **Teste de Penetração (Pentest)** | Ataque simulado e controlado |
| **Caça a Ameaças** | Busca proativa por ameaças não detectadas |

### Varreduras
| Termo | Significado |
|-------|-------------|
| **Varredura Intrusiva (Ativa)** | Interage com o alvo, pode causar impacto |
| **Varredura Não Intrusiva (Passiva)** | Analisa evidências sem interagir |
| **Varredura Credenciada** | Usa credenciais válidas para acesso profundo |
| **Varredura Não Credenciada** | Simula visão de um invasor externo |

### Ferramentas
| Termo | Significado |
|-------|-------------|
| **Nmap** | Scanner de rede e portas |
| **OpenVAS** | Scanner de vulnerabilidades |
| **Nessus** | Scanner de vulnerabilidades comercial |
| **Burp Suite** | Testes de segurança em aplicações web |
| **Wireshark** | Analisador de pacotes |

### CVE e Reconhecimento
| Termo | Significado |
|-------|-------------|
| **CVE** | Common Vulnerabilities and Exposures - catálogo de vulnerabilidades |
| **Reconhecimento Ativo** | Interage com o alvo (ex: varredura de portas) |
| **Reconhecimento Passivo** | Coleta informações sem interagir (ex: OSINT) |

### Estratégias de Resiliência
| Termo | Significado |
|-------|-------------|
| **Gerenciamento de Configuração** | Controle de configurações de TI |
| **Gerenciamento de Ativos** | Inventário e proteção de ativos digitais |
| **Controle de Mudança** | Processo para alterações controladas |
| **RFC** | Request for Change - solicitação de mudança |
| **Hot Site** | Site de contingência totalmente configurado |
| **Warm Site** | Site parcialmente configurado |
| **Cold Site** | Site sem configuração prévia |
| **Defesa em Profundidade** | Múltiplas camadas de segurança |
| **Honeypot** | Isca para atrair e detectar invasores |
| **Honeynet** | Rede de honeypots interconectados |
| **Honeyfile** | Arquivo falso para detectar acesso não autorizado |

### Análise de Tráfego
| Termo | Significado |
|-------|-------------|
| **Ipconfig/ifconfig** | Configuração de rede (Windows/Linux) |
| **Ping** | Teste de conectividade |
| **ARP** | Address Resolution Protocol - associa IP a MAC |
| **Route** | Visualiza/gerencia rotas |
| **Tracert/traceroute** | Rastreia caminho dos pacotes |
| **Netstat** | Exibe conexões de rede |
| **nslookup/dig** | Consultas DNS |

---

## 🔐 Módulo 4 – Controles de Acesso

### IAM
| Termo | Significado |
|-------|-------------|
| **IAM** | Identity and Access Management - gerenciamento de identidades e acessos |
| **Identificação** | Atribuição de identidade única |
| **Autenticação** | Verificação da identidade |
| **Autorização** | Determinação de permissões |
| **Contabilidade (Accounting)** | Registro e auditoria de atividades |

### Fatores de Autenticação
| Termo | Significado |
|-------|-------------|
| **Knowledge Factor** | Algo que você sabe (senha, PIN) |
| **Ownership Factor** | Algo que você tem (token, cartão) |
| **Biometric Factor** | Algo que você é (digital, face, íris) |
| **MFA** | Autenticação Multifator - uso de 2+ fatores |

### Autenticação Baseada em Conhecimento
| Termo | Significado |
|-------|-------------|
| **Autenticação Local** | Verificação no próprio dispositivo |
| **Autenticação de Rede** | Verificação em servidor central (AD, LDAP) |
| **Autenticação Remota** | Acesso via VPN, SSH |
| **SSO** | Single Sign-On - um login para múltiplos sistemas |
| **PAP** | Password Authentication Protocol - senha em texto claro |
| **CHAP** | Challenge Handshake Authentication Protocol - mais seguro que PAP |
| **MS-CHAP** | Variação Microsoft do CHAP |

### Ataques de Senha
| Termo | Significado |
|-------|-------------|
| **Ataque de Força Bruta** | Testa todas as combinações possíveis |
| **Ataque de Dicionário** | Testa palavras comuns |
| **Pulverização de Senhas** | Testa senhas comuns em várias contas |
| **Ataque Híbrido** | Combina dicionário com variações |
| **Cofre de Senhas** | Gerenciador de senhas |

### Tecnologias de Autenticação
| Termo | Significado |
|-------|-------------|
| **Smart Card** | Cartão com chip para autenticação |
| **HSM** | Hardware Security Module - módulo de segurança de hardware |
| **Token USB** | Dispositivo físico para autenticação |
| **TPM** | Trusted Platform Module - chip de segurança |
| **IEEE 802.1X** | Controle de acesso à rede |
| **RADIUS** | Remote Authentication Dial-In User Service - AAA |
| **HOTP** | HMAC-based One-Time Password - baseado em contador |
| **TOTP** | Time-based One-Time Password - baseado em tempo |
| **2FA** | Autenticação em dois fatores |

### Biometria
| Termo | Significado |
|-------|-------------|
| **FRR** | False Rejection Rate - taxa de falsa rejeição |
| **FAR** | False Acceptance Rate - taxa de falsa aceitação |
| **CER** | Crossover Error Rate - ponto de equilíbrio entre FRR e FAR |
| **Reconhecimento Facial** | Autenticação por características faciais |
| **Reconhecimento Digital** | Autenticação por impressão digital |
| **Biometria Comportamental** | Padrões de digitação, movimento do mouse |

---

## 👥 Módulo 5 – Gerenciamento de Identidades e Contas

### Políticas de Pessoal
| Termo | Significado |
|-------|-------------|
| **Onboarding** | Processo de integração de novo colaborador |
| **NDA** | Non-Disclosure Agreement - acordo de confidencialidade |
| **Offboarding** | Processo de desligamento de colaborador |
| **Separação de Funções** | Divisão de responsabilidades para evitar conflitos |
| **Menor Privilégio** | Apenas o acesso necessário para a função |
| **Rotação de Cargos** | Alternância de funções para reduzir riscos |
| **Licença Obrigatória** | Período de afastamento para auditoria independente |

### Tipos de Contas
| Termo | Significado |
|-------|-------------|
| **Conta de Convidado** | Acesso temporário e limitado |
| **Conta de Administrador/Root** | Privilégios totais no sistema |
| **Conta de Serviço** | Usada para executar serviços (Local, Network, System) |
| **Conta Compartilhada** | Usada por múltiplas pessoas (risco) |
| **Chave SSH** | Par de chaves para autenticação segura |

### Políticas de Contas
| Termo | Significado |
|-------|-------------|
| **GPO** | Group Policy Object - política de grupo (Windows) |
| **Geofencing** | Restrição de acesso por localização geográfica |
| **Auditoria de Contas** | Revisão sistemática de atividades de contas |
| **Permissões (RWX)** | Read, Write, Execute - leitura, gravação, execução |
| **Bloqueio de Conta** | Medida temporária após tentativas falhas |
| **Desabilitação de Conta** | Medida permanente |

### Soluções de Autorização
| Termo | Significado |
|-------|-------------|
| **DAC** | Discretionary Access Control - proprietário define permissões |
| **RBAC** | Role-Based Access Control - permissões por função |
| **MAC** | Mandatory Access Control - políticas definidas pelo sistema |
| **ABAC** | Attribute-Based Access Control - permissões por atributos |
| **PAM** | Privileged Access Management - gestão de contas privilegiadas |
| **LDAP** | Lightweight Directory Access Protocol - acesso a diretórios |
| **DN** | Distinguished Name - identificação única no diretório |
| **CN** | Common Name - nome comum |
| **OU** | Organizational Unit - unidade organizacional |
| **O** | Organization - organização |
| **C** | Country - país |
| **DC** | Domain Component - componente de domínio |
| **Federação** | Compartilhamento de autenticação entre organizações |
| **SAML** | Security Assertion Markup Language - XML para autenticação |
| **SOAP** | Simple Object Access Protocol - comunicação entre apps |
| **OAuth 2.0** | Protocolo de autorização |
| **OIDC** | OpenID Connect - autenticação sobre OAuth 2.0 |

---

## 🌐 Módulo 6 – Proteção Web e Desenvolvimento Seguro

| Termo | Significado |
|-------|-------------|
| **XSS** | Cross-Site Scripting - injeção de scripts maliciosos em páginas web |
| **Reflected XSS** | Código malicioso em link que é "refletido" pelo servidor |
| **Stored XSS** | Código malicioso armazenado no servidor (comentários, perfil) |
| **DOM-based XSS** | Manipulação do DOM da página sem passar pelo servidor |
| **CSP** | Content Security Policy - política que restringe execução de scripts |
| **SQLi** | SQL Injection - injeção de comandos SQL em formulários |
| **Consulta parametrizada** | Técnica que separa comando SQL dos dados do usuário |
| **XML Injection** | Inserção de dados maliciosos em documentos XML |
| **LDAP Injection** | Manipulação de consultas LDAP para acessar diretórios |
| **Directory Traversal** | Acesso a arquivos fora da área permitida (ex: ../../../etc/passwd) |
| **Command Injection** | Execução de comandos maliciosos no sistema operacional |
| **SSRF** | Server-Side Request Forgery - servidor faz requisições não autorizadas |
| **CSRF** | Cross-Site Request Forgery - usuário autenticado executa ação sem querer |
| **Token Anti-CSRF** | Valor único gerado pelo servidor para prevenir CSRF |
| **Clickjacking** | Elemento oculto sobre página legítima para enganar clique |
| **X-Frame-Options** | Cabeçalho HTTP que controla incorporação em iframes |
| **SSL Strip** | Remoção da criptografia SSL/TLS em conexões |
| **HSTS** | HTTP Strict Transport Security - força conexão HTTPS |
| **Session Hijacking** | Sequestro de sessão - invasor assume controle da sessão |
| **HttpOnly** | Flag de cookie que impede acesso via JavaScript |
| **SameSite** | Política que controla envio de cookies entre sites |
| **Replay Attack** | Retransmissão de dados válidos interceptados |
| **API Attack** | Ataque a APIs explorando falhas de segurança |
| **Rate Limiting** | Limite de taxa para evitar força bruta |
| **Menor privilégio** | Princípio de dar apenas o acesso necessário |
| **Defesa em profundidade** | Múltiplas camadas de segurança |
| **Stored Procedure** | Rotina no banco de dados que valida entrada |
| **Ofuscação** | Tornar código complexo para dificultar engenharia reversa |

---

## 💾 Módulo 7 – Redundância, Backup, Segurança Física e Destruição de Dados

| Termo | Significado |
|-------|-------------|
| **Redundância** | Componentes ou sistemas duplicados para evitar falhas |
| **Cluster** | Conjunto de servidores atuando como um único sistema |
| **Failover** | Transferência automática para servidor redundante |
| **Balanceador de carga** | Distribui tráfego entre múltiplos servidores |
| **Replicação** | Criação de cópias idênticas em diferentes locais |
| **RAID** | Redundant Array of Independent Disks |
| **RAID 0 (Striping)** | Divisão de dados entre discos (performance, sem tolerância a falhas) |
| **RAID 1 (Espelhamento)** | Cópia idêntica em dois ou mais discos |
| **RAID 5** | Dados + paridade distribuída (tolerância a 1 falha) |
| **RAID 6** | Dupla paridade (tolerância a 2 falhas) |
| **RAID 10 (1+0)** | Espelhamento + Striping (performance + redundância) |
| **Rsync** | Sincronização eficiente com transferência delta |
| **Replicação síncrona** | Dados replicados em tempo real |
| **Replicação assíncrona** | Dados replicados em intervalo definido |
| **Backup completo (Full)** | Cópia de todos os arquivos selecionados |
| **Backup incremental** | Cópia apenas das alterações desde o último backup |
| **Backup diferencial** | Cópia de todas as alterações desde o último full |
| **Backup contínuo** | Cópias em tempo real conforme dados são modificados |
| **Backup espelhado** | Cópia exata em tempo real em local separado |
| **Backup de imagem** | Cópia exata de disco/partição inteiro |
| **Backup em nuvem** | Dados enviados para servidores remotos |
| **Backup local** | Dispositivos físicos locais (HD externo, fita) |
| **Backup remoto (Offsite)** | Local geograficamente separado |
| **NAS** | Network Attached Storage - armazenamento conectado à rede |
| **VTL** | Virtual Tape Library - emula fita usando disco |
| **Trituração** | Redução de dispositivos a pequenos pedaços |
| **Degaussing** | Desmagnetização para destruir dados em mídias magnéticas |
| **Incineração** | Queima controlada de dispositivos |
| **Sobrescrita DoD 5220.22-M** | Padrão com 3 passagens (0, 1, aleatório) |
| **DBAN** | Darik's Boot and Nuke - ferramenta de destruição |
| **Fechadura** | Controle de acesso físico tradicional |
| **Cartão de acesso** | Dispositivo com informações codificadas |
| **Biometria** | Autenticação por características físicas únicas |
| **Torniquete** | Barreira giratória que permite passagem de uma pessoa por vez |
| **CFTV** | Circuito Fechado de TV - monitoramento por câmeras |
| **Clean Desk** | Política de mesa limpa sem documentos sensíveis |

---

## 🔑 Módulo 8 – Conceitos de Criptografia

| Termo | Significado |
|-------|-------------|
| **Criptografia** | Transformação de dados legíveis em formato ilegível |
| **Texto claro** | Dados originais legíveis |
| **Texto cifrado** | Dados após aplicação da criptografia |
| **Chave simétrica** | Mesma chave para cifrar e decifrar |
| **Chave assimétrica** | Par de chaves: pública e privada |
| **Chave pública** | Compartilhada, usada para cifrar ou verificar |
| **Chave privada** | Secreta, usada para decifrar ou assinar |
| **Cifra de fluxo** | Criptografia em fluxo contínuo (ex: XOR) |
| **Cifra de blocos** | Divisão em blocos de tamanho fixo |
| **AES** | Advanced Encryption Standard - padrão atual |
| **DES** | Data Encryption Standard - inseguro atualmente |
| **3DES** | Triple DES - aplica DES três vezes |
| **RC4** | Cifra de fluxo com problemas de segurança |
| **Blowfish** | Cifra de blocos com chave variável |
| **Twofish** | Concorrente do AES, ainda seguro |
| **RSA** | Algoritmo assimétrico baseado em fatoração |
| **ECC** | Elliptic Curve Cryptography - chaves menores, mesma segurança |
| **DSA** | Digital Signature Algorithm - focado em assinaturas |
| **ElGamal** | Baseado em Diffie-Hellman |
| **Função hash** | Algoritmo que gera resumo de tamanho fixo |
| **MD5** | Message Digest 5 - inseguro, colisões possíveis |
| **SHA-1** | Secure Hash Algorithm 1 - inseguro |
| **SHA-2** | Família SHA-224, SHA-256, SHA-384, SHA-512 |
| **SHA-3** | Versão mais recente, mais segura |
| **RIPEMD-160** | Alternativa de 160 bits |
| **BLAKE2** | Hash rápido e seguro |
| **Colisão** | Duas entradas diferentes com mesmo hash |
| **Resistência à inversão** | Dificuldade de obter entrada original a partir do hash |
| **Distribuição uniforme** | Valores de hash bem espalhados no espaço de saída |
| **Confusão** | Relação complexa entre chave e texto cifrado |
| **Difusão** | Mudança mínima na entrada causa grande mudança na saída |
| **Perfect Forward Secrecy** | Chaves de sessão passadas protegidas mesmo com comprometimento futuro |
| **Esteganografia** | Ocultação de dados em arquivos (imagem, áudio) |
| **Fragmentação** | Divisão de dados em partes antes de criptografar |

---

## 🏛️ Módulo 9 – Infraestrutura de Chaves Públicas e Blockchain

| Termo | Significado |
|-------|-------------|
| **PKI** | Public Key Infrastructure - infraestrutura de chaves públicas |
| **AC (CA)** | Autoridade Certificadora - emite e valida certificados |
| **RA** | Autoridade de Registro - verifica identidade dos solicitantes |
| **CSR** | Certificate Signing Request - solicitação de certificado |
| **Certificado digital** | Documento eletrônico com chave pública e identificação |
| **X.509** | Padrão de formato de certificados digitais |
| **CN** | Common Name - nome comum do titular |
| **SAN** | Subject Alternative Name - nomes alternativos no certificado |
| **CRL** | Certificate Revocation List - lista de certificados revogados |
| **OCSP** | Online Certificate Status Protocol - consulta online de revogação |
| **DV** | Domain Validation - validação básica de domínio |
| **OV** | Organization Validation - validação de organização |
| **EV** | Extended Validation - validação estendida (barra verde) |
| **PFX/P12** | Formato que armazena certificado + chave privada |
| **P7B/PKCS#7** | Formato para armazenar certificados |
| **Key Escrow** | Custódia de chaves por terceiro confiável |
| **Certificate Pinning** | Fixação de certificado para evitar MITM |
| **OpenSSL** | Biblioteca para criptografia e certificados |
| **Blockchain** | Registro descentralizado de transações em blocos encadeados |
| **Bloco** | Unidade que armazena transações e hash do bloco anterior |
| **Nó (Node)** | Computador que mantém cópia da blockchain |
| **Consenso** | Acordo entre nós para validar transações |
| **PoW** | Proof of Work - prova de trabalho (mineração) |
| **PoS** | Proof of Stake - prova de participação |
| **Carteira (Wallet)** | Software ou hardware para guardar chaves de criptomoedas |

---

## 🖥️ Módulo 10 – Segurança no Host

| Termo | Significado |
|-------|-------------|
| **Linha de base (Baseline)** | Configuração padrão segura |
| **Shadow IT** | Uso não autorizado de TI por funcionários |
| **Patch** | Atualização de software para corrigir vulnerabilidades |
| **WSUS** | Windows Server Update Services |
| **HIDS** | Host-based Intrusion Detection System |
| **EPP** | Endpoint Protection Platform - proteção combinada |
| **EDR** | Endpoint Detection and Response - detecção e resposta |
| **PLC** | Programmable Logic Controller - controlador industrial |
| **SoC** | System on Chip - sistema em um chip |
| **FPGA** | Field Programmable Gate Array - lógica programável |
| **RTOS** | Real-Time Operating System - sistema em tempo real |
| **Z-Wave** | Protocolo IoT de baixa potência (800-900 MHz) |
| **Zigbee** | Protocolo IoT (2,4 GHz) com tecnologia mesh |
| **CAN** | Controller Area Network - protocolo para automóveis |
| **ICS** | Industrial Control System - sistema de controle industrial |
| **SCADA** | Supervisory Control and Data Acquisition |
| **IoT** | Internet of Things - internet das coisas |
| **BAS** | Building Automation System - automação predial |
| **Smart Meter** | Medidor inteligente de consumo |
| **TPM** | Trusted Platform Module - chip de segurança |
| **UEFI** | Unified Extensible Firmware Interface - substituto do BIOS |
| **Secure Boot** | Garante que só software confiável execute na inicialização |
| **Measured Boot** | Mede e verifica integridade dos componentes |
| **Boot Attestation** | Atesta integridade para entidade externa |
| **FDE** | Full Disk Encryption - criptografia total do disco |
| **SED** | Self-Encrypting Drive - disco com criptografia integrada |

---

## 🌐 Módulo 11 – Rede Segura e Equipamentos de Segurança

| Termo | Significado |
|-------|-------------|
| **Switch** | Equipamento que conecta dispositivos na mesma rede |
| **Roteador** | Equipamento que conecta redes diferentes |
| **WAP** | Wireless Access Point - ponto de acesso sem fio |
| **Firewall** | Barreira que filtra tráfego com base em regras |
| **ACL** | Access Control List - lista de regras de acesso |
| **Iptables** | Firewall do Linux baseado em tabelas e cadeias |
| **Stateless firewall** | Inspeciona pacotes individualmente |
| **Stateful firewall** | Mantém estado das conexões |
| **WAF** | Web Application Firewall - protege aplicações web |
| **DMZ** | Zona desmilitarizada - rede intermediária |
| **VLAN** | Virtual LAN - segmentação lógica da rede |
| **ARP** | Address Resolution Protocol - associa IP a MAC |
| **MAC Flooding** | Inundação da tabela MAC do switch |
| **Clonagem de MAC** | Falsificação de endereço MAC |
| **STP** | Spanning Tree Protocol - evita loops em rede |
| **BPDU Guard** | Proteção contra BPDUs em portas de acesso |
| **DHCP Snooping** | Proteção contra servidores DHCP falsos |
| **PNAC / 802.1X** | Controle de acesso baseado em porta |
| **IP Spoofing** | Falsificação de endereço IP |
| **Zero Trust** | Modelo que não confia em nada por padrão |
| **Proxy** | Intermediário entre cliente e servidor |
| **Reverse Proxy** | Proxy para servidores internos |
| **NIDS** | Network-based Intrusion Detection System |
| **NIPS** | Network-based Intrusion Prevention System |
| **SPAN/Mirror Port** | Cópia de tráfego para monitoramento |
| **TAP** | Test Access Point - dispositivo de monitoramento |
| **UEBA** | User and Entity Behavior Analytics |
| **NGFW** | Next-Generation Firewall |
| **UTM** | Unified Threat Management - solução integrada |
| **SWG** | Secure Web Gateway - proteção para acesso web |

---

## 🚨 Módulo 12 – Resposta a Incidentes e Protocolos Seguros

| Termo | Significado |
|-------|-------------|
| **Incidente** | Evento que compromete a segurança |
| **CSIRT** | Computer Security Incident Response Team |
| **IRP** | Incident Response Plan - plano de resposta |
| **Cyber Kill Chain** | Framework de 7 etapas de um ataque |
| **MITRE ATT&CK** | Base de conhecimento de táticas e técnicas |
| **Diamond Model** | Modelo de análise com 4 componentes |
| **DRP** | Disaster Recovery Plan - recuperação de desastres |
| **BCP** | Business Continuity Plan - continuidade de negócios |
| **SIEM** | Security Information and Event Management |
| **SOAR** | Security Orchestration, Automation and Response |
| **Syslog** | Protocolo para envio de logs |
| **Log aggregation** | Centralização de logs |
| **DLP** | Data Loss Prevention - prevenção de perda de dados |
| **Allow list** | Lista de aplicativos autorizados |
| **Block list** | Lista de aplicativos bloqueados |
| **DNSSEC** | DNS Security Extensions - proteção contra poisoning |
| **Domain Hijacking** | Roubo de domínio |
| **DNS Poisoning** | Envenenamento de cache DNS |
| **LDAPS** | LDAP sobre SSL/TLS |
| **NTP** | Network Time Protocol |
| **NTS** | Network Time Security |
| **SNMP** | Simple Network Management Protocol |
| **SNMPv3** | Versão segura do SNMP |
| **SSL/TLS** | Protocolos de segurança para comunicação |
| **SFTP** | SSH File Transfer Protocol |
| **FTPS** | FTP over SSL/TLS |
| **SMTPS** | SMTP sobre SSL/TLS |
| **POP3S** | POP3 sobre SSL/TLS |
| **IMAPS** | IMAP sobre SSL/TLS |
| **S/MIME** | Criptografia e assinatura de e-mails |
| **TLS VPN** | VPN baseada em TLS |
| **IPSec** | Conjunto de protocolos para segurança de IP |
| **AH** | Authentication Header - autenticação no IPSec |
| **ESP** | Encapsulating Security Payload - criptografia no IPSec |
| **SSH** | Secure Shell - acesso remoto seguro |
| **Evidência** | Registro eletrônico coletado em investigação |
| **Cadeia de custódia** | Registro detalhado da evidência |
| **E-Discovery** | Identificação e organização de evidências |
| **Ordem de volatilidade** | Prioridade de coleta de dados |
| **FTK** | Forensic Toolkit - ferramenta forense |
| **EnCase** | Ferramenta forense comercial |
| **The Sleuth Kit** | Conjunto de ferramentas forenses open source |
| **Volatility** | Framework para análise de memória RAM |