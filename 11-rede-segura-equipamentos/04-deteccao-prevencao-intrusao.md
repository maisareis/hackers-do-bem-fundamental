# Módulo 11 – Rede Segura e Equipamentos de Segurança

## Aula 4 – Sistemas de Detecção e Prevenção de Intrusão

## 📌 Sistemas de Detecção e Prevenção de Intrusão

### Network-Based Intrusion Detection Systems (NIDS)
- Operam em conjunto com HIDS
- Identificam ameaças na rede
- Características:
  - Análise de tráfego via inspeção de pacotes
  - Alertas e notificações para administradores
  - Console de monitoramento

### Host-Based Intrusion Detection Systems (HIDS)
- Detectam atividades em hosts individuais
- Características:
  - Implementação em hosts
  - Monitoramento de eventos locais
  - Diferentes níveis de detecção
  - Resposta no próprio host

### Sistemas de Prevenção de Intrusão (IPS)
- Atuação proativa na segurança
- Complementa o IDS
- Detecta, bloqueia e toma ações automaticamente

### Network-Based Intrusion Prevention Systems (NIPS)
- Opera no tráfego de toda a rede
- Características:
  - Posicionamento em pontos estratégicos
  - Análise do tráfego
  - Detecção e prevenção de intrusões
  - Resposta em tempo real

## 📌 Tipos de Detecção ou Prevenção

### Baseada em Assinaturas (Signature-based)
- Vantagens:
  - Eficiência
  - Precisão
- Desafios:
  - Dependência de atualizações constantes
  - Vulnerabilidade a ameaças desconhecidas (zero-day)

### Baseada em Anomalias (Anomaly-based)
- Identifica desvios no comportamento padrão da rede
- Características:
  1. Coleta de dados de comportamento
  2. Análise de padrões
  3. Criação de perfis
  4. Detecção de anomalias
  5. Geração de alertas
- Vantagens:
  - Detecção de ameaças desconhecidas
  - Baixa dependência de atualizações
- Desafios:
  - Falsos-positivos
  - Complexidade

## 📌 Ferramentas de Detecção ou Prevenção

### Switched Port Analyzer (SPAN) ou Mirror Port
- Funcionalidade em switches e roteadores
- Copia tráfego para monitoramento em tempo real sem interromper fluxo
- Etapas:
  1. Configuração do SPAN
  2. Cópia do tráfego
  3. Inspeção de tráfego
  4. Análise de pacotes
- Benefícios:
  - Monitoramento em tempo real
  - Busca por atividades maliciosas sem interromper operações

### Network Test Access Point (TAP)
- Dispositivo que monitora tráfego sem intervir no fluxo
- Visão ampla e precisa do tráfego em tempo real

#### TAP Passivo
- Opera de forma passiva (sem fonte de energia própria)
- Fica entre dois dispositivos de rede
- Possui portas de entrada e saída
- Funcionamento:
  - Divisão do sinal óptico ou elétrico
  - Conectividade não-invasiva

#### TAP Ativo
- Requer fonte de energia própria
- Possui portas de entrada e saída
- Copia tráfego e regenera pacotes antes de encaminhar
- Pode reconfigurar pacotes e reconstituir sinal elétrico
- Filtragem de tráfego como recurso adicional

### User and Entity Behavior Analytics (UEBA)
- Abordagem que usa algoritmos de aprendizado de máquina
- Análise comportamental para detectar atividades suspeitas
- Identifica ameaças internas e externas
- Funcionamento:
  - Coleta contínua de dados
  - Criação de perfis de comportamento
  - Aprendizado de máquina
  - Detecção de anomalias
  - Avaliação de risco
  - Geração de alertas

### Next-Generation Firewall (NGFW)
- Evolução dos firewalls tradicionais
- Características:
  - Filtragem de pacotes tradicional
  - Inspeção em camadas de aplicação
  - Prevenção de Intrusões (IPS)
  - Filtragem de conteúdo
  - Controle de aplicações
  - VPN e segurança de acesso remoto
  - Inteligência de ameaças e Machine Learning

### Filtro de Conteúdo (Content Filter)
- Monitora acessos à internet
- Características:
  - Identificação de categorias de conteúdo
  - Inspeção do tráfego
  - Análise de URLs e conteúdo
  - Correspondência com listas de categorias
  - Bloqueio ou liberação
  - Notificações e relatórios
  - Personalização de políticas

### Unified Threat Management (UTM)
- Solução integrada em um único equipamento
- Combina:
  - Firewall
  - Prevenção de Intrusões (IPS)
  - Antivírus e Antimalware
  - Filtro de conteúdo
  - Virtual Private Network (VPN)
  - Controle de aplicações
  - Análise e relatórios
  - Gerenciamento centralizado

### Secure Web Gateway (SWG)
- Protege usuários e rede de ameaças da web
- Características:
  - Roteamento de tráfego
  - Verificação e autenticação de usuários
  - Filtro de conteúdo
  - Prevenção de malware
  - Proteção contra ameaças avançadas
  - Inspeção SSL/TLS
  - Controle de aplicações
  - Relatórios e análises
  - Segurança para dispositivos remotos

---

## 💡 Meus insights
- **NIDS vs HIDS**: NIDS olha a rede, HIDS olha o host. Juntos, visão completa.
- **Signature-based** detecta o conhecido, **anomaly-based** detecta o desconhecido. Melhor usar ambos.
- **IPS** bloqueia automaticamente, **IDS** só alerta. IPS é mais arriscado (pode bloquear tráfego legítimo), mas necessário em alguns casos.
- **SPAN** é fácil de configurar, mas pode perder pacotes em alta carga. **TAP** é mais confiável.
- **TAP Passivo** não altera tráfego, ideal para forense. **TAP Ativo** regenera sinal, útil para longas distâncias.
- **UEBA** detecta comportamentos anômalos: usuário acessando dados fora do horário, transferência incomum, etc.
- **NGFW** é o firewall moderno: entende aplicações, não só portas e protocolos.
- **UTM** é o canivete suíço: tudo em um. Bom para pequenas/médias empresas.
- **SWG** é essencial para controle de acesso à web. Filtra conteúdo malicioso antes que chegue ao usuário.
- **Defesa em profundidade**: NIDS + HIDS + NGFW + UEBA + UTM/SWG. Quanto mais camadas, melhor.