# Módulo 11 – Rede Segura e Equipamentos de Segurança

## Aula 2 – Segurança em Encaminhamento de Tráfego

## 📌 Ataques Man-in-the-Middle de Camada 2
- Invasor age na comunicação entre dois dispositivos
- Intercepta mensagens trocadas
- Controla todo o fluxo

### Clonagem de MAC
- Técnica de falsificação do endereço MAC
- Visa obter autenticação na rede para acessar recursos restritos
- Etapas:
  1. Observação do alvo
  2. Identificação do alvo
  3. Coleta do endereço MAC
  4. Configuração do MAC clonado
  5. Conexão à rede

### Inundação de MAC (MAC Flooding)
- Sobrecarrega a tabela de endereços MAC do switch com informações falsas
- Etapas:
  1. Identificação do switch e porta
  2. Criação de pacotes falsos
  3. Envio dos pacotes falsos
  4. Comportamento anômalo do switch (modo "failopen" – age como hub)

## 📌 Spanning Tree Protocol (STP)
- Protocolo para evitar loops de caminho em redes com redundância
- Fornece redundância e disponibilidade usando bloqueios inteligentes

### Funcionamento
1. Eleição da Bridge Raiz (Root Bridge)
2. Cálculo dos caminhos mais curtos
3. Escolha das portas designadas e bloqueadas
4. Atualizações contínuas com BPDUs
5. Tempo de convergência

### Versões aprimoradas
- **RSTP (Rapid Spanning Tree Protocol)** – convergência mais rápida
- **MSTP (Multiple Spanning Tree Protocol)** – múltiplas instâncias STP

## 📌 Bridge Protocol Data Unit (BPDU) Guard
- Medida de segurança para switches
- Aplicada em portas de acesso (não tronco)
- Bloqueia porta se receber BPDU (indicando possível loop ou ataque)
- Porta pode ser recuperada automaticamente após configuração

## 📌 Filtragem de Endereços MAC (MAC Filtering)
- Técnica que verifica se dispositivo tem permissão para acessar a rede
- Apenas MACs autorizados se conectam

### Funcionamento
1. Coleta dos endereços MAC autorizados
2. Configuração no roteador ou switch
3. Escolha do modo de filtragem (permitir/negar)
4. Autenticação dos dispositivos
5. Limitações: MAC pode ser falsificado (spoofing)

## 📌 DHCP Snooping
- DHCP: protocolo para obtenção automática de endereços IP
- DHCP Snooping protege contra servidores DHCP falsos (Rogue DHCP)

### Funcionamento
- Identifica portas confiáveis e não confiáveis
- Constrói tabela DHCP snooping
- Verifica pacotes DHCP subsequentes
- Permite apenas servidores legítimos

## 📌 Port-based Network Access Control (PNAC)
- Controle de acesso baseado nas portas físicas do switch
- Padrão IEEE 802.1X

### Funcionamento
1. Identificação dos dispositivos e portas
2. Definição das políticas de acesso
3. Configuração no switch
4. Métodos de autenticação
5. Verificação do acesso
6. Monitoramento e manutenção

## 📌 IP Spoofing
- Técnica onde remetente usa IP falso para esconder identidade
- Frequentemente usado em ataques DDoS

### Funcionamento
1. Identificação do alvo
2. Captura do tráfego de rede
3. Escolha do endereço IP falsificado
4. Criação do pacote forjado
5. Envio dos pacotes falsificados
6. Consequências: ataques de reflexão, amplificação, bypass de ACLs

---

## 💡 Meus insights
- **Ataques de Camada 2** são perigosos porque ocorrem dentro da rede local. Switches precisam de proteções específicas.
- **MAC Flooding** força o switch a agir como hub, permitindo que atacante veja todo tráfego. Port security ajuda a prevenir.
- **STP** é essencial para redes com redundância, mas pode ser atacado. BPDU Guard protege portas de acesso.
- **DHCP Snooping** é obrigatório em redes corporativas para evitar Rogue DHCP. Um servidor DHCP falso pode redirecionar tráfego.
- **802.1X** é o padrão para controle de acesso por porta. Usuário só acessa rede após autenticar.
- **IP Spoofing** é difícil de prevenir na borda da rede, mas filtros de ingresso/egresso ajudam.
- **Filtragem MAC** é frágil sozinha. Combinar com 802.1X e DHCP Snooping é melhor.
- **Defesa em profundidade** na camada 2: Port Security, DHCP Snooping, BPDU Guard, 802.1X, VLANs.