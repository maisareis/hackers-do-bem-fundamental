# Módulo 11 – Rede Segura e Equipamentos de Segurança

## Aula 3 – Firewall e Proxy

## 📌 Firewall
- Barreira virtual entre rede interna e redes externas
- Filtra e bloqueia acessos não autorizados
- Previne ataques maliciosos e atividades suspeitas

## 📌 Lista de Controle de Acesso (ACL)
- Criada com base em regras para permitir ou bloquear tráfego
- Aplicada a cada pacote que passa pelo firewall
- Critérios comuns:
  - Endereços IP de origem e destino
  - Portas de origem e destino
  - Protocolos de transporte
  - Outras informações do cabeçalho

### Funcionamento
- Avaliação de pacotes sequencial
- Ordem de avaliação (primeira regra correspondente é aplicada)
- Ações: permitir, negar, encaminhar
- Regras personalizadas
- Implicit Deny (negação implícita no final)
- Sentido do fluxo (entrada/saída)

## 📌 Iptables
- Recurso do Linux para filtrar e controlar tráfego de rede
- Dividido em: Tabelas, Cadeias e Regras

### Tabelas
- **Filter**: filtragem de pacotes
- **Nat**: tradução de endereços
- **Mangle**: modificação de cabeçalhos
- **Raw**: processamento antes de outras tabelas

### Cadeias
- **INPUT**: pacotes destinados ao próprio sistema
- **OUTPUT**: pacotes gerados pelo sistema
- **FORWARD**: pacotes encaminhados

### Regras
- Determinam tratamento dos pacotes
- Podem: permitir, negar, encaminhar, alterar cabeçalho

### Fluxo de decisão
1. Verificação das regras da Tabela Raw
2. Pré-processamento da Tabela Mangle
3. Filtragem nas cadeias INPUT/OUTPUT/FORWARD
4. Verificação das regras da Tabela Nat

## 📌 Tipos de Firewall

### Firewall de Filtragem de Pacotes
- Inspeciona pacotes individualmente
- Permite ou bloqueia conforme regras
- Vantagem: eficiente em desempenho
- Limitação: não detecta tráfego malicioso disfarçado

### Firewall de Inspeção sem Estado (Stateless)
- Examina cabeçalho de cada pacote individualmente
- Vantagens: simplicidade, eficiência, resistente a DoS
- Limitações: não rastreia estado das conexões, ameaças podem passar despercebidas

### Firewall de Inspeção com Estado (Stateful)
- Mantém registro de conexões ativas em tabela de estado
- Monitora histórico de pacotes
- Decisões baseadas em contexto e histórico
- Vantagens: rastreia estado, mais eficiente na filtragem
- Limitações: consome mais recursos, pode ser mais lento

### Web Application Firewall (WAF)
- Protege aplicações web
- Analisa e filtra tráfego HTTP/HTTPS
- Funcionamento:
  - Inspeção do tráfego de entrada/saída
  - Comparação com assinaturas de ataques conhecidos
  - Bloqueio de ataques (SQLi, XSS)
  - Aprendizado e adaptação
  - Personalização de regras

### Appliance Firewall
- Solução pronta para uso (hardware dedicado)
- Recursos e configurações embutidos
- Características: hardware especializado, SO próprio, configuração simplificada, recursos avançados, escalabilidade

### Host-Based Firewall
- Software de segurança para computadores individuais
- Atua na segurança do sistema local
- Funcionamento:
  - Inspeção do tráfego local
  - Criação de regras
  - Política default
  - Ações do firewall
  - Integração com SO

## 📌 Proxy

### Forward Proxy
- Atua entre usuários da rede interna e servidores externos
- Executa troca de mensagens sem que servidor externo saiba identidade do cliente
- Benefícios: melhora desempenho (cache), protege privacidade

### Fluxo de funcionamento
1. Requisição do cliente
2. Encaminhamento da requisição
3. Resposta do servidor
4. Cache e otimização
5. Controle de acesso

### Transparent Proxy
- Cliente não percebe existência do proxy
- Interceptação automática
- Transparência para o cliente
- Controle e cache

### Non-Transparent Proxy
- Requer configuração manual no cliente
- Conscientização do cliente
- Controle e cache

### Reverse Proxy
- Atua como intermediário entre clientes externos e servidores internos
- Gerencia tráfego de entrada

### Fluxo de funcionamento
1. Requisição do cliente externo
2. Encaminhamento da requisição para servidor interno
3. Proteção dos servidores internos
4. Balanceamento de carga
5. Cache e otimização
6. **SSL Termination**: pode criptografar/descriptografar tráfego SSL/TLS

---

## 💡 Meus insights
- **ACL** é a base de todo firewall. Regras bem definidas evitam tráfego indesejado.
- **Iptables** é poderoso, mas complexo. Dominar as tabelas e cadeias é essencial para administradores Linux.
- **Stateless vs Stateful**: stateless é rápido mas cego; stateful entende o contexto. Uso combinado é comum.
- **WAF** é obrigatório para aplicações web expostas. Bloqueia SQLi, XSS e outros ataques específicos.
- **Appliance Firewall** é "liga e usa". Bom para empresas que não querem configurar do zero.
- **Host-based Firewall** é a última linha de defesa no próprio computador. Essencial para endpoints.
- **Forward Proxy** protege identidade dos usuários internos e faz cache de conteúdo (economia de banda).
- **Reverse Proxy** protege servidores internos e distribui carga. Essencial para alta disponibilidade.
- **SSL Termination** no reverse proxy alivia servidores internos do custo de criptografia.
- **Transparent Proxy** é útil para redes corporativas, usuário não precisa configurar nada.
- **Non-Transparent Proxy** dá mais controle, mas exige configuração manual (ou via PAC).
- **Defesa em profundidade**: firewall de borda + WAF + reverse proxy + host-based firewall.