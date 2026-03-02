# Módulo 12 – Resposta a Incidentes e Protocolos Seguros

## Aula 1 – Monitoramento de Redes e Redes Sem Fio

## 📌 Monitoramento de Redes

### Network Monitor
- Ferramenta para monitoramento e análise do tráfego de rede
- Etapas de funcionamento:
  - Captura de pacotes
  - Análise de pacotes
  - Filtragem de dados
  - Visualização e análise de tráfego
  - Diagnóstico de problemas
  - Registro e exportação de dados

### Logs
- Registros detalhados de ocorrências geradas por sistemas ou aplicativos
- Propósito: registrar informações para análise posterior
- Características:
  - Geração automática
  - Formato estruturado
  - Armazenamento e gerenciamento
  - Análise e monitoramento
  - Ferramentas de análise

### Syslog
- Armazena registros de eventos gerados por sistemas e aplicativos
- Classificados por instalações e severidades
- Pode ser centralizado para agilizar resposta a incidentes
- Recurso importante para segurança da rede e sistemas
- Ferramentas como SIEM utilizam Syslog

### Coleta de Logs (Log Collection)
- Essencial para monitoramento de segurança em redes
- Abordagens:
  - **Agent-based**: agente instalado no sistema
  - **Collector**: coletor centralizado
  - **Sensor**: dispositivo dedicado

### Security Information and Event Management (SIEM)
- Solução que oferece gerenciamento de eventos e informações em tempo real
- Etapas:
  1. Coleta de dados de diversas fontes
  2. Armazenamento centralizado
  3. Normalização e correlação
  4. Detecção de anomalias e ameaças
  5. Notificação e resposta
  6. Relatórios e conformidade
  7. Integração com outras ferramentas

### Agregação de Logs (Log Aggregation)
- Processo de centralização de diversos logs em um único local
- Visa facilitar monitoramento, análise e correlação
- Geralmente realizado no SIEM
- Funcionalidades:
  - Coleta de logs de diferentes fontes
  - Centralização
  - Normalização dos dados
  - Análise e correlação de eventos
  - Alertas e notificações
  - Armazenamento de longo prazo
  - Relatórios e inteligência de segurança

### User and Entity Behavior Analytics (UEBA)
- Técnica que emprega IA e aprendizado de máquina
- Pode operar junto com SIEM
- Etapas:
  1. Coleta de dados de comportamento
  2. Criação de perfil de comportamento (baseline)
  3. Detecção de anomalias
  4. Correlação de eventos
  5. Pontuação de risco
  6. Alertas e notificações
  7. Adaptação ao ambiente

### Security Orchestration, Automation, and Response (SOAR)
- Orquestração, automatização e resposta de segurança
- Combina funções em plataforma única
- Etapas:
  1. Coleta e agregação de dados
  2. Análise e correlação de eventos
  3. Automatização de tarefas
  4. Orquestração de fluxo de trabalho
  5. Integração com ferramentas de segurança
  6. Geração de relatórios e métricas

### Manipulação de arquivos (Unix-like)
- Comandos para extração de informações relevantes:
  - **Cat (Concatenate)**: exibir conteúdo de arquivos
  - **Head e Tail**: visualizar início/fim de arquivos
  - **Logger**: adicionar mensagens ao syslog
  - **Regex (Expressões regulares)**: padrões de busca
  - **Grep**: buscar texto em arquivos

## 📌 Segurança em Redes Sem Fio

### Wireless Access Point (WAP)
- Funcionamento:
  - SSID e autenticação
  - Comutação de pacotes
  - Segurança
  - Gestão e monitoramento

### Interferência de Canal Compartilhado (CCI)
- Ocorre quando dois ou mais Access Points compartilham o mesmo canal
- Gera interferência para ambas as redes
- Como ocorre:
  - Canais de frequência (divisão de faixas não licenciadas)
  - Sobreposição de canais
  - Canais não sobrepostos vs sobrepostos
  - Concorrência por largura de banda
  - Gerenciamento de canais
  - Controle de potência

### Wi-Fi Protected Access – WPA2 e WPA3

#### WPA2
- Autenticação: protocolo 802.1X/EAP
- Criptografia: padrão AES
- Modos: WPA2-PSK e WPA2-Enterprise

#### WPA3
- Autenticação individualizada (chave única por dispositivo)
- Criptografia de 192 bits (padrão SAE)
- Proteção contra ataques de força bruta
- Resistência a ataques de dicionário
- Transições de segurança
- Mais seguro que WPA2

### Wi-Fi Protected Setup (WPS)
- Recurso para configuração fácil de redes Wi-Fi seguras
- Características:
  - Dois métodos: Push Button e PIN
  - Temporização do PIN
  - Chaves de criptografia
  - Ativação e desativação
- Vulnerabilidades: força bruta de PIN, ataque de registro externo

### Engenharia Social em Wi-Fi
- **Rogue Access Point (RAP)**: ponto de acesso falso
  - Criação de rede falsa
  - Engana dispositivos
  - Captura de tráfego
  - Ataques Man-in-the-Middle
- **Evil Twin (Gêmeo Malicioso)**: cópia de rede legítima para roubo de dados

---

## 💡 Meus insights
- **Monitoramento de rede** é a base da detecção de incidentes. Sem ele, você está cego.
- **Logs são ouro** para investigação. Mas só servem se estiverem centralizados e protegidos.
- **Syslog** é o padrão antigo mas ainda muito usado. Classificar por severidade ajuda a priorizar.
- **SIEM** correlaciona eventos de múltiplas fontes. Consegue detectar ataques que isoladamente passariam despercebidos.
- **UEBA** complementa o SIEM com análise comportamental. Detecta insider threats.
- **SOAR** automatiza respostas. Se um alerta dispara, SOAR pode bloquear IP automaticamente.
- **Grep e Regex** são ferramentas essenciais para quem analisa logs manualmente.
- **WPA3** resolve falhas do WPA2, mas ainda não é universal. Em redes corporativas, WPA2-Enterprise com 802.1X ainda é comum.
- **WPS** é uma porta de entrada para ataques. Melhor desabilitar.
- **Evil Twin** é perigoso porque o usuário escolhe a rede com sinal mais forte. Sempre verificar se é a rede oficial.
- **Canais Wi-Fi**: no Brasil, canais 1, 6 e 11 são os únicos não sobrepostos em 2.4 GHz.