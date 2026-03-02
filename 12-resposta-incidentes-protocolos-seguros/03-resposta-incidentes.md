# Módulo 12 – Resposta a Incidentes e Protocolos Seguros

## Aula 3 – Resposta a Incidentes

## 📌 Lidando com Incidentes

### Processo de Resposta a Incidentes
- Política define recursos, processos e diretrizes
- Objetivo: identificar, conter, mitigar e aprender com incidentes
- Evitar danos à imagem da organização

### Etapas do processo
1. **Preparação**
2. **Identificação**
3. **Contenção**
4. **Erradicação**
5. **Recuperação**
6. **Lições Aprendidas**

### Computer Security Incident Response Team (CSIRT)
- Equipe especializada em gerenciar e coordenar resposta a incidentes
- Funções:
  - Coordenação e gerenciamento (single point-of-contact)
  - Detecção e análise (monitoramento)
  - Investigação e resposta
  - Comunicação e notificação aos stakeholders
  - Mitigação e prevenção
  - Melhoria contínua

### Times de segurança da informação

#### Purple Team
- Trabalha com Blue e Red Team
- Coordena e planeja ações conjuntas
- Compartilha informações entre equipes
- Avalia eficiência dos controles
- Promove melhoria contínua

#### White Team
- Ligado a competições de cyber security (CTFs)
- Cria cenários, desafios e ambientes de teste
- Organiza competições
- Atua como juiz

### Plano de Resposta a Incidentes (IRP)
- Contém procedimentos, contatos e recursos para categorias de incidentes
- Orienta investigadores na priorização e remediação
- Deve conter:
  - Objetivos e escopo
  - Equipe e papéis
  - Classificação e priorização
  - Fases de resposta
  - Procedimentos específicos
  - Comunicação e notificação
  - Cooperação externa
  - Testes e atualizações
  - Treinamento e conscientização

### Cyber Kill Chain Attack Framework
- Estrutura para descrever estágios de um cyber attack
- Ferramenta para pesquisa de ameaças (TTPs do adversário)
- Etapas:
  1. **Reconhecimento**
  2. **Armadilha (Weaponization)**
  3. **Entrega**
  4. **Exploração (Exploitation)**
  5. **Instalação**
  6. **Comando e Controle (C2)**
  7. **Ação (Action on Objectives)**

### Modelo Diamante de Análise de Intrusão
- The Diamond Model of Intrusion Analysis
- Análise profunda de ataques
- Quatro componentes:
  - **Adversário (Adversary)**
  - **Infraestrutura (Infrastructure)**
  - **Capacidade (Capability)**
  - **Vítima (Victim)**

### MITRE ATT&CK
- Adversarial Tactics, Techniques, and Common Knowledge
- Detalha táticas, técnicas e procedimentos (TTPs)
- Visa aprimorar defesas
- Recursos:
  - Matriz de Táticas e Técnicas
  - Táticas
  - Técnicas
  - Frameworks de Ataque
  - Detecção e prevenção
  - Treinamento e conscientização
  - Teste de Red Team
  - Análise de incidentes

### Exercícios de Resposta a Incidentes
- Atividades para otimizar processos

#### Tabletop Exercise
- Discussão teórica de cenários
- Benefícios: alinhamento, identificação de gaps

#### Walkthrough Exercise
- Passo a passo simulado
- Benefícios: validação de procedimentos

#### Simulation Exercise
- Simulação prática com ferramentas
- Benefícios: teste realista, treinamento da equipe

### Plano de Recuperação de Desastres (DRP)
- Documento com procedimentos para recuperação após desastres
- Visa retorno rápido à normalidade
- Deve conter:
  - Identificação de ativos críticos
  - Avaliação de riscos e impacto
  - Definição de objetivos de recuperação
  - Estratégias de recuperação
  - Procedimentos de recuperação
  - Alocação de recursos
  - Testes e treinamento
  - Manutenção e atualização
  - Comunicação e notificação
  - Revisão e melhoria contínua

### Plano de Continuidade de Negócios (BCP)
- Estratégias para garantir continuidade das operações
- Minimiza efeitos negativos de eventos de grande impacto
- Deve conter:
  - Identificação de funções essenciais
  - Avaliação de riscos e impactos

## 📌 Ferramentas de resposta a incidentes

### Plataformas de Registro (Logging Platforms)
- Coleta, armazenamento e análise de logs
- Tipos:
  - Syslog
  - Rsyslog
  - Syslog-ng
  - Journalctl
  - Nxlog

### Application Log Files
- Informações sobre comportamento de aplicativos, sistemas e serviços
- Tipos:
  - DNS Event Logs
  - Consultas e respostas DNS
  - Análise de padrões e anomalias
  - Solicitações de acesso
  - Detecção de atividades maliciosas
  - Monitoramento de desempenho

### Metadados
- Informações sobre outros dados
- Facilitam compreensão e gerenciamento
- Tipos:
  - Metadados de arquivo
  - Metadados da Web
  - Metadados de E-mail
  - Metadados móveis

### Prevenção de Perda de Dados (DLP)
- Estratégia e tecnologias para proteger dados sensíveis
- Protege contra ameaças internas e externas
- Etapas:
  1. Identificação de dados sensíveis
  2. Monitoramento de tráfego e atividades
  3. Detecção de conteúdo sensível
  4. Política de ação
  5. Prevenção e correção
  6. Auditoria e relatórios

### Listas de permissão e de bloqueio

#### Application Allow Lists
- Lista de aplicativos autorizados
- Funcionamento:
  - Criação da lista
  - Bloqueio de aplicativos não autorizados
  - Prevenção de execução de malware

#### Application Block Lists
- Lista de aplicativos não confiáveis ou inseguros
- Funcionamento:
  - Criação da lista
  - Impedir execução de aplicativos bloqueados
  - Prevenção de ameaças conhecidas

---

## 💡 Meus insights
- **Resposta a incidentes** não é só tecnologia, é processo. Sem preparação, o caos se instala.
- **CSIRT** é o time de elite. Ter um CSIRT bem treinado faz toda diferença.
- **Cyber Kill Chain** ajuda a entender o ataque em fases. Interromper em qualquer fase quebra a cadeia.
- **MITRE ATT&CK** é a enciclopédia de ataques. Qualquer profissional de segurança precisa conhecer.
- **Diamond Model** foca nos relacionamentos entre adversário, infra, capacidade e vítima.
- **Tabletop vs Simulation**: tabletop é barato e rápido; simulação é realista e caro. Ambos são necessários.
- **DRP vs BCP**: DRP recupera TI, BCP mantém o negócio funcionando. Andam juntos.
- **DLP** é essencial para evitar vazamento de dados. Monitora e bloqueia saída de informações sensíveis.
- **Allow Lists** são mais seguras que block lists. Só executa o que é explicitamente permitido.
- **Metadados** podem revelar mais do que parece. Um documento PDF pode conter nome do autor, data, versões anteriores.
- **Logs centralizados** são a base para investigação. Sem eles, é como investigar crime sem câmeras.