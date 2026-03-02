# Módulo 10 – Segurança no Host

## Aula 3 – Firmware Seguro

## 📌 Proteção a nível de Firmware

### Firmware
- Contém drivers e protocolos para interoperabilidade entre componentes de hardware
- Fornece interface para software de nível superior (SO) interagir com hardware
- Pode conter configurações que afetam:
  - Configurações de energia
  - Configurações de rede
  - Configurações de segurança

## 📌 Hardware Root of Trust
- Componente de hardware confiável e imutável
- Atua como base segura para inicialização e operação do sistema
- Estabelece raiz de confiança
- Garante que etapas críticas ocorram em ambiente confiável
- Projetado para resistir a ataques físicos e lógicos
- Protege contra: malware, ataques de firmware, ataques de inicialização

## 📌 Trusted Platform Module (TPM)
- Chip de hardware para recursos de segurança e criptografia
- Componente crítico do Hardware Root of Trust
- Opera independente da CPU e do SO
- Funciona mesmo com sistema desligado ou em suspensão

### Recursos e funcionalidades
- Armazenamento seguro de chaves criptográficas
- Geração de chaves criptográficas
- Operações criptográficas seguras
- Medição de integridade
- Autenticação de plataforma

## 📌 Unified Extensible Firmware Interface (UEFI)
- Especificação de firmware moderna que substituiu o BIOS
- Responsável por:
  - Inicializar o sistema
  - Configurar hardware
  - Fornecer interface entre firmware e SO

### Recursos avançados
- Inicialização mais rápida
- Suporte a discos > 2,2 TB
- Inicialização em modo protegido
- Suporte a interfaces gráficas

### Etapas
1. Inicialização do UEFI
2. Configuração do hardware
3. Inicialização do SO
4. Interface do usuário
5. Extensibilidade

## 📌 Secure Boot
- Recurso de segurança em sistemas compatíveis com UEFI
- Protege contra malware e ataques de inicialização comprometida
- Garante que apenas software confiável e autorizado seja executado durante a inicialização

### Funcionamento
- Verificação da integridade do firmware
- Verificação da integridade do carregador de inicialização
- Verificação da assinatura digital do kernel e drivers
- Chave de assinatura confiável
- Modo de usuário e configuração

## 📌 Measured Boot
- Recurso que complementa o Secure Boot
- Verifica e mede a integridade de componentes críticos durante a inicialização
- Permite detecção de alterações ou comprometimentos em:
  - Firmware
  - Bootloader
  - SO
  - Drivers

### Funcionamento
- Coleta de medidas
- Criação de cadeias de confiança
- Armazenamento seguro das medidas
- Verificação da cadeia de confiança
- Comparação de medidas
- Relatórios de integridade

## 📌 Boot Attestation
- Mecanismo que complementa o Measured Boot
- Permite que sistema forneça evidências de integridade para entidade externa confiável
- Entidades: servidor de autenticação, sistema de monitoramento

## 📌 Full Disk Encryption (FDE)
- Criptografa todos os dados armazenados em disco
- Inclui: SO, arquivos do usuário, metadados
- Impede acesso não autorizado em caso de perda/roubo

## 📌 Self-Encrypting Drives (SED)
- Unidades de armazenamento (HDD/SSD) com criptografia integrada no hardware
- Executa criptografia diretamente no hardware da unidade

### Funcionamento
- Chave de criptografia
- Autenticação
- Criptografia em tempo real
- Chave de dados
- Rápido apagamento
- Gerenciamento de chaves

## 📌 Segurança em USB Flash Drive (Pendrive)
- Medidas para proteger dados armazenados:
  - Criptografia
  - Senhas e autenticação
  - Armazenamento seguro
  - Proteção contra gravação
  - Atualizações de firmware
  - Gerenciamento adequado

---

## 💡 Meus insights
- **Firmware é invisível, mas crítico**. Se comprometido, o atacante controla a máquina antes mesmo do SO iniciar.
- **Root of Trust** é a âncora. Toda a segurança do sistema parte daí. Se quebrar, tudo que vem depois é inseguro.
- **TPM** é usado pelo Windows (BitLocker) para armazenar chaves de criptografia. Se o TPM detectar alterações no boot, bloqueia o acesso.
- **UEFI substituiu BIOS** por bons motivos: suporte a discos grandes, boot seguro, interface gráfica.
- **Secure Boot** impede rootkits de boot. Só executa código assinado por chaves confiáveis.
- **Measured Boot** vai além: registra tudo que foi executado e pode atestar para um servidor remoto.
- **Boot Attestation** é usado em ambientes corporativos. O computador "prova" que está íntegro antes de acessar a rede.
- **FDE** protege contra acesso físico. Se roubarem o notebook, os dados estão criptografados.
- **SED** é transparente: a criptografia acontece no hardware, sem perda de performance.
- **Pendrive seguro** com criptografia por hardware é essencial para dados sensíveis. Senha no dispositivo, dados protegidos mesmo se perdido.