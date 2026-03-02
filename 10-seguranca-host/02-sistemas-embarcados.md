# Módulo 10 – Segurança no Host

## Aula 2 – Segurança em Sistemas Embarcados

## 📌 Sistemas Embarcados
- Projetados para executar tarefas específicas
- Integrados a um hardware específico
- Três elementos:
  - Hardware
  - Software
  - Firmware

### Capacidade de processamento
- Sistemas embarcados possuem capacidade limitada
- Motivos:
  - Restrições de recursos
  - Necessidades específicas de aplicação
  - Consumo de energia

## 📌 Controladores Lógicos para Sistemas Embarcados

### PLC (Programmable Logic Controller)
- Equipamento eletrônico digital com hardware e software próprios
- Executa instruções para implementações específicas
- Criado para controlar máquinas e processos
- Sistemas embarcados são executados em um PLC

### System on Chip (SoC)
- Dispositivos eletrônicos com funções integradas em um único chip
- Componentes:
  - Processador central (CPU)
  - Memória
  - Controladores de periféricos
  - Interfaces de comunicação
  - Acelerador gráfico
- Exemplos: Raspberry Pi, Arduino

### Field Programmable Gate Array (FPGA)
- Dispositivo eletrônico com matriz de blocos lógicos programáveis interconectados
- Usa linguagens HDL (Hardware Description Language) para definir configuração
- Contém carga dos blocos lógicos programados para executar a função

### Real-Time Operating Systems (RTOS)
- Sistema operacional para realizar tarefas em tempo real
- Recursos:
  - Priorização de tarefas
  - Agendamento de tempo real
  - Compartilhamento de recursos
  - Gerenciamento de eventos
  - Comunicação entre tarefas
- Exemplos: FreeRTOS, eCos, VxWorks, QNX, Micrium μC/OS-II

## 📌 Tecnologias de Sistemas Embarcados

### Protocolos Z-Wave e Zigbee
- Protocolos de comunicação sem fio para IoT

#### Z-Wave
- Baixa potência, curto alcance
- Faixa de frequência: 800-900 MHz
- Tecnologia de malha (mesh network)
- Dispositivos podem atuar como repetidores

#### Zigbee
- Baixa potência (LPWAN)
- Faixa de frequência: 2,4 GHz
- Tecnologia de malha
- Altamente eficiente em consumo de energia
- Suporta redes com milhares de dispositivos
- Recursos avançados de segurança

### Controller Area Network (CAN)
- Protocolo de comunicação serial usado em sistemas embarcados
- Abordagem de comunicação de multi-acesso
- Mecanismo de detecção de colisão para resolver conflitos
- Suporta velocidades de transmissão variáveis
- Amplamente usado em automóveis

### Sistemas de Controle Industrial (ICS)
- Projetados para monitorar e controlar processos industriais
- Três componentes principais:
  - Dispositivos de campo (sensores e atuadores)
  - Controladores (PLCs ou SoCs)
  - Sistemas de supervisão (SCADA)

### Supervisory Control and Data Acquisition (SCADA)
- Sistemas de controle e coleta de dados para monitorar processos industriais e infraestruturas críticas
- Componentes:
  - Unidades de coleta de dados
  - Unidade de supervisão
  - Estação de controle

### Internet das Coisas (IoT)
- Interconexão de dispositivos físicos por meio da internet
- Dispositivos coletam, processam e trocam dados com autonomia
- Etapas:
  1. Coleta de dados via sensores
  2. Processamento dos dados
  3. Conectividade entre dispositivos e com a internet

### Sistema de Automação Predial (BAS)
- Sistema computacional para gerenciamento e controle predial
- Dados coletados por sensores enviados para processamento centralizado
- Painel de controle centralizado (pode ser remoto via app/web)
- Visa eficiência energética e bem-estar dos ocupantes

### Medidores Inteligentes (Smart Meters)
- Dispositivos para medir consumo de energia elétrica, água ou gás
- Coleta de dados em tempo real e transmissão às empresas de serviços públicos
- Disponíveis também para consumidores
- Usam criptografia e autenticação
- Benefícios: detecção de falhas na rede elétrica, tarifação diferenciada

---

## 💡 Meus insights
- **Sistemas embarcados estão em todo lugar**: carros, eletrodomésticos, equipamentos médicos. Segurança deles é crítica.
- **PLC** é o cérebro da indústria. Um ataque a um PLC pode parar uma fábrica inteira.
- **SoC** como Raspberry Pi é ótimo para prototipagem, mas em produção precisa de cuidados de segurança.
- **FPGA** é programável em hardware. Poderoso, mas complexo.
- **RTOS** é diferente de Windows/Linux. Prioriza tarefas em tempo real, não multitarefa genérica.
- **Z-Wave vs Zigbee**: Z-Wave tem menos interferência (800 MHz), Zigbee mais rápido (2,4 GHz). Ambos usam mesh.
- **CAN bus** é o protocolo dos carros modernos. Atacantes podem explorar para controlar veículos.
- **ICS/SCADA** são alvos de ataques state-sponsored. Stuxnet é o exemplo mais famoso.
- **IoT** é um pesadelo de segurança se não for bem configurada. Dispositivos baratos vêm com senhas fixas e vulnerabilidades.
- **BAS** pode economizar energia, mas se invadido, pode desligar sistemas críticos de um prédio.
- **Smart meters** são ótimos para eficiência, mas geram dados detalhados de consumo (privacidade).