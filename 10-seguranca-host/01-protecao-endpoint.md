# Módulo 10 – Segurança no Host

## Aula 1 – Proteção do Endpoint

## 📌 Configurações e Patches

### Configuração de Linha de Base (Baseline)
- Conjunto de configurações padrão que estabelecem um estado inicial seguro e consistente
- Inclui:
  - Configurações de firewall
  - Permissões de acesso
  - Configurações de contas de usuário
  - Políticas de senha
  - Restrições de software

### Processo de configuração de linha de base
1. Identificar requisitos específicos
2. Definir Políticas da organização
3. Definição dos padrões
4. Definição das configurações para sistemas e dispositivos
- Deve ser revisada e atualizada periodicamente

### Desvio de Configuração de Linha de Base
- Situação em que configurações não estão em conformidade com a linha de base inicial
- Pode ocorrer por:
  - Alterações não autorizadas
  - Atualizações de software
  - Configurações incorretas
  - Intervenção humana
  - Atividades maliciosas

### Tecnologia da Informação Sombra (Shadow IT)
- Uso de recursos de TI por iniciativa própria, sem conformidade com normas e políticas
- Pode trazer questões de segurança e dificuldades de gerenciamento

### Gerenciamento de Patches
- Atualizações de software contendo correções
- Reduz vulnerabilidades

#### Etapas do gerenciamento de patches
1. Identificação
2. Avaliação
3. Teste
4. Implantação
5. Verificação
6. Gerenciamento de exceções

#### Soluções de mercado
- Microsoft WSUS (Windows Server Update Services)
- SCCM (System Center Configuration Manager)
- IBM BigFix
- Ivanti Patch Management
- SolarWinds Patch Manager

## 📌 Tecnologias de Proteção de Endpoint
- Soluções e práticas para garantir segurança dos dispositivos
- Visam detectar, prevenir e responder a ameaças cibernéticas

### Antimalware
- Software para proteger sistemas contra malware
- Funcionalidades:
  - Detecção de malware
  - Remoção
  - Escaneamento em tempo real
  - Atualizações de definições
  - Proteção em tempo real
  - Configurações personalizáveis

### Sistema de Detecção de Intrusão em Host (HIDS)
- Detecta atividades maliciosas no sistema operacional e aplicativos do host
- Funcionalidades:
  - Monitoramento de atividades
  - Análise de eventos
  - Detecção de intrusões
  - Alertas e notificações
  - Logs e análise forense

### Endpoint Protection Platform (EPP)
- Combina várias camadas de proteção em um único produto
- Abordagem holística para proteger endpoints e dados
- Funcionalidades:
  - Antivírus e antimalware
  - Firewall de endpoint
  - Prevenção de intrusões
  - Controle de aplicativos
  - Proteção contra ameaças avançadas
  - Gerenciamento centralizado
  - Relatórios e análise

### Endpoint Detection and Response (EDR)
- Projetado para detectar atividades maliciosas e responder a incidentes em tempo real
- Funcionalidades:
  - Coleta de dados
  - Análise e detecção
  - Resposta a incidentes
  - Investigação e análise forense
  - Inteligência e relatórios
  - Integração com outras soluções

---

## 💡 Meus insights
- **Linha de base** é o "estado de fábrica" seguro. Se um dispositivo desvia disso, algo errado aconteceu.
- **Shadow IT** é mais comum do que parece. Funcionário instala o próprio software porque o oficial é ruim. Isso cria brechas.
- **Gerenciamento de patches** é corrida contra o tempo. Vulnerabilidade divulgada = atacantes já estão testando.
- **WSUS** é útil para redes Windows, mas exige infraestrutura.
- **HIDS** é o "vigilante do host". Monitora arquivos de log, integridade de arquivos, conexões.
- **EPP** é o pacote completo: antivírus, firewall, prevenção. Solução all-in-one.
- **EDR** vai além: não só detecta, mas investiga e responde. Consegue reverter ações do malware.
- **Diferença EPP vs EDR**: EPP previne, EDR detecta e responde ao que passou. Melhor usar ambos.
- **Antimalware tradicional** já não basta. Ataques modernos exigem EDR e análise comportamental.