# Módulo 10 – Segurança no Host

## Aula 4 – Segurança em Virtualização e Nuvem

## 📌 Serviços em Nuvem

### Nuvem Pública (Public Cloud)
- Recursos compartilhados com múltiplos usuários
- Garante disponibilidade, escalabilidade e segurança
- Pagamento por uso (modelo de consumo)
- Exemplos: AWS, Microsoft Azure, Google Cloud Platform

### Nuvem Privada (Private Cloud)
- Dedicada exclusivamente a uma única organização
- Recursos provisionados e gerenciados internamente ou por terceiros
- Pode ser on-premise ou hospedada externamente
- Maior controle, segurança e personalização
- Adequada para requisitos rigorosos de conformidade

### Nuvem Híbrida (Hybrid Cloud)
- Combina nuvem pública e privada
- Dados e aplicações podem ser compartilhados entre os ambientes

### Nuvem Comunitária (Community Cloud)
- Compartilhada por várias organizações com interesses comuns
- Organizações colaboram em políticas de segurança, governança e conformidade
- Infraestrutura compartilhada
- Ambiente controlado e especializado

## 📌 Modelos de Serviço

### Software as a Service (SaaS)
- Acesso a aplicativos completos hospedados na nuvem
- Provedor gerencia software e infraestrutura
- Acesso via interface web ou cliente dedicado
- Sem necessidade de instalação local
- Exemplos: e-mail em nuvem, Salesforce, Google Workspace

### Platform as a Service (PaaS)
- Ambiente de desenvolvimento e execução de aplicativos
- Provedor fornece infraestrutura para construir, implantar e gerenciar aplicativos
- Inclui: SOs, bancos de dados, balanceamento de carga, etc.

### Infrastructure as a Service (IaaS)
- Acesso a recursos de infraestrutura: servidores virtuais, redes, armazenamento, SOs
- Provedor fornece infraestrutura física
- Usuário tem controle sobre SO, aplicativos e dados
- Exemplos: Amazon EC2, Azure Virtual Machines, Google Compute Engine

### Security as a Service (SECaaS)
- Soluções de segurança cibernética sob demanda
- Serviços:
  - Detecção e prevenção de intrusões (IDS/IPS)
  - Firewall Gerenciado
  - Proteção de endpoint
  - Gerenciamento de Vulnerabilidades
  - Análise de Segurança e SIEM
  - Gerenciamento de Identidade e Acesso (IAM)
  - Backup e recuperação de dados

### Managed Security Services Provider (MSSP)
- Provedor especializado em serviços gerenciados de segurança
- Serviços:
  - Monitoramento de Segurança
  - Detecção e Resposta a Incidentes
  - Gerenciamento de Vulnerabilidades
  - Gerenciamento de Identidade e Acesso
  - Firewall Gerenciado
  - Proteção de Endpoint
  - Análise de Segurança e SIEM

## 📌 Virtualização

### Hypervisor
- Software ou firmware que permite virtualização e execução de múltiplas VMs em um servidor físico
- Camada de abstração entre hardware físico e VMs
- Gerencia recursos do sistema

#### Tipo 1 (Bare-metal)
- Instalado diretamente no hardware físico
- Sem SO hospedeiro intermediário
- Gerencia acesso direto aos recursos físicos
- Desempenho mais eficiente
- Exemplos: VMware ESXi, Microsoft Hyper-V, Xen

#### Tipo 2 (Hosted)
- Instalado sobre um SO hospedeiro
- SO hospedeiro instalado no hardware físico
- Hypervisor é um aplicativo dentro do SO
- VMs são processos no SO hospedeiro
- Comum em computadores pessoais
- Exemplos: VMware Workstation, Oracle VirtualBox, Microsoft Virtual PC

### Virtual Desktop Infrastructure (VDI)
- Desktops virtuais executados em servidores centrais
- Acessados remotamente por usuários finais
- Abordagem centralizada para fornecimento e gerenciamento
- Acesso de qualquer dispositivo com conexão de rede

### VM Escape
- Vulnerabilidade de segurança
- Atacante escapa de uma VM e ganha acesso ao host físico
- Contorna o isolamento da virtualização
- Explora falhas no hypervisor ou implementação

### VM Sprawl
- Ocorre quando VMs são criadas e implantadas desnecessariamente
- Resulta em:
  - Desperdício de recursos
  - Dificuldades de gerenciamento
  - Aumento de custos operacionais

### Virtualização de Contêiner
- Empacota e isola aplicativos e dependências em contêineres leves
- Cada contêiner contém: bibliotecas, frameworks, arquivos de configuração

## 📌 Tecnologias de Virtualização

### Docker
- Plataforma de código aberto
- Facilita criação, implantação e execução de aplicativos em contêineres
- Empacota aplicativos e dependências em unidades isoladas (contêineres)

### Kubernetes
- Plataforma de orquestração de contêineres (código aberto, Google)
- Facilita implantação, dimensionamento e gerenciamento de aplicativos contêinerizados em produção

### Vagrant
- Ferramenta de código aberto
- Criação e gerenciamento de ambientes de desenvolvimento virtualizados
- Simplifica configuração e distribuição de VMs
- Usa arquivos de configuração simples (Vagrantfile)
- Permite gerenciamento de múltiplas VMs

---

## 💡 Meus insights
- **Nuvem pública** é prática, mas exige cuidado com dados sensíveis. Nem tudo deve ir pra lá.
- **Nuvem privada** é mais segura, mas mais cara. Vale para quem tem requisitos regulatórios pesados.
- **Híbrida** é o melhor dos dois mundos: dados sensíveis on-premise, escalabilidade na nuvem pública.
- **SaaS** é "pronto para usar". Só configure e use.
- **PaaS** é "traga seu código". O provedor cuida do resto.
- **IaaS** é "traga tudo". Você gerencia SO, aplicativos, dados. Provedor só dá a infra.
- **SECaaS** é terceirizar a segurança. Útil para quem não tem equipe especializada.
- **MSSP** é como um SOC externo. Monitoram 24/7 e respondem a incidentes.
- **Hypervisor Tipo 1** é para datacenter. Mais seguro e performático.
- **Hypervisor Tipo 2** é para testes e desenvolvimento. Mais fácil de usar.
- **VM Escape** é raro, mas quando ocorre é catastrófico. Isolamento é fundamental.
- **VM Sprawl** acontece em ambientes sem governança. Máquina criada e esquecida consumindo recursos.
- **Contêineres são mais leves que VMs**, mas o isolamento é diferente (compartilham kernel do host).
- **Docker** popularizou contêineres. "Build, ship, run anywhere".
- **Kubernetes** é o orquestrador padrão. Gerencia centenas de contêineres automaticamente.
- **Vagrant** é ótimo para desenvolvedores. Sobe ambiente idêntico ao de produção em minutos.