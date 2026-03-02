# Módulo 11 – Rede Segura e Equipamentos de Segurança

## Aula 1 – Design de Rede Segura

## 📌 Princípios de Redes Seguras
- **Confidencialidade**: acesso apenas a quem tem permissão
- **Integridade**: dados não são alterados indevidamente
- **Disponibilidade**: rede e serviços acessíveis quando necessário

## 📌 Fraquezas em Redes Seguras
- Pontos únicos de falha
- Dependências complexas
- Disponibilidade acima de confidencialidade e integridade
- Falta de documentação e controle de mudanças
- Dependência exagerada na segurança perimetral

## 📌 Principais Equipamentos de Rede
- **Switch (Comutador)**: conecta dispositivos na mesma rede
- **Wireless Access Points (WAP)**: acesso sem fio
- **Roteadores**: conectam diferentes redes
- **Firewalls**: filtram tráfego com base em regras
- **Balanceadores de Carga**: distribuem tráfego entre servidores
- **Servidores DNS**: resolvem nomes de domínio

## 📌 Encaminhamento de Tráfego

### Switching (Comutação)
- Usa endereço MAC
- Opera na mesma LAN

### Roteamento
- Usa endereço IP
- Comunicação entre redes diferentes

### Internet Protocol (IP)
- Opera na camada 3 do Modelo OSI
- Pacote IP contém: dados encapsulados, IP origem, IP destino
- Padrões: IPv4 e IPv6
- Endereço IP exclusivo por dispositivo
- Controle de fragmentação

### Address Resolution Protocol (ARP)
- Opera na camada 2 (enlace)
- Associa endereços IP a endereços MAC
- ARP Request vs ARP Reply
- Para dispositivos na mesma LAN

### Segmentação de Rede
- Divisão de rede maior em sub-redes independentes
- Cada segmento é isolado
- Facilita gerenciamento de segurança e desempenho
- Permite segregação de tráfego

### Segregação de Rede
- Separação física ou lógica dos segmentos
- Técnicas: VLANs, sub-redes, firewalls
- Protege recursos críticos por isolamento

## 📌 Zonas e suas topologias
- **Zona de rede**: área que agrupa dispositivos com requisitos comuns de segurança
- Relacionada à segregação
- **Intranet**: rede interna
- **Extranet**: rede para parceiros/terceiros

### Zonas Desmilitarizadas (DMZ)
- Áreas isoladas das demais zonas
- Intermediária entre rede interna (Intranet) e externa (Internet)
- Camada adicional de segurança
- Servidores com restrição de acesso

#### Formas de implementar DMZ
- Sub-rede com DMZ
- Firewall triplamente protegido
- Host filtrado

## 📌 Considerações de Design de Redes Seguras

### Tráfego Leste-Oeste (East-West)
- Comunicação interna entre dispositivos do datacenter
- Rede interna de alta velocidade e baixa latência

### Tráfego Norte-Sul (North-South)
- Comunicação do datacenter com a rede externa
- Conexão com internet e dispositivos de borda

### Confiança Zero (Zero Trust)
- Redefine proteção de redes e sistemas
- Abandona "confiança implícita"
- Nenhum dispositivo ou usuário é confiável por padrão
- Segurança baseada em:
  - Autenticação
  - Autorização
  - Verificação contínua

---

## 💡 Meus insights
- **Princípios CIA** (Confidencialidade, Integridade, Disponibilidade) são a base. Toda decisão de segurança deve considerar esses três.
- **Ponto único de falha** é um risco enorme. Redundância é essencial em redes críticas.
- **Dependência exagerada no perímetro** é um erro. Se o atacante passar do firewall, rede interna está indefesa. Daí o Zero Trust.
- **ARP** é um protocolo antigo e inseguro. ARP spoofing é um ataque clássico de MITM.
- **Segmentação** é uma das melhores defesas. Se uma parte da rede for comprometida, o resto não é afetado.
- **VLANs** são a forma prática de segmentar sem comprar novos switches.
- **DMZ** é onde ficam servidores que precisam ser acessados da internet (web, e-mail). Se invadirem o servidor web, não acessam a rede interna.
- **Tráfego East-West** é crítico em datacenters. Um atacante que compromete um servidor pode se mover lateralmente. Microssegmentação ajuda.
- **Zero Trust** é o modelo atual. "Nunca confie, sempre verifique". Cada acesso é autenticado e autorizado individualmente.
- **Design de rede segura** é pensar em defesa em profundidade: firewalls, DMZ, segmentação, monitoramento, Zero Trust.