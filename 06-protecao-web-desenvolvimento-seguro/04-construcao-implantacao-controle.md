# Aula 4 – Construção, Implantação e Controle de Software

## 📌 DevSecOps
- Integra **Dev** (desenvolvimento) + **Sec** (segurança) + **Ops** (operações)
- Segurança contínua em todo ciclo de vida
- Automação de tarefas de segurança

## 📌 Automação
- Tarefas sem intervenção humana
- Provisionar recursos, adicionar contas, atribuir permissões, resposta a incidentes
- Evita erros manuais (configuração inconsistente)

## 📌 Ciclo de Vida do Desenvolvimento de Software (SDLC)

### Modelo em Cascata
- Fases sequenciais:
  1. Requisitos/Análise
  2. Design
  3. Codificação
  4. Testes
  5. Manutenção
- Dificuldade de mudar requisitos no meio

### Desenvolvimento Ágil
- Iterativo, colaborativo, entregas incrementais
- **Características:**
  - Colaboração constante
  - Iterações curtas (sprints)
  - Priorização do mais importante
  - Feedback contínuo do cliente

## 📌 Garantia de Qualidade
- **Controle de Qualidade (CQ)** → testar se sistema está livre de defeitos
- **Garantia de Qualidade (GQ)** → define o que é "qualidade" e como medir

### Práticas
- Testes funcionais, integração, unidade
- Revisões de código
- Documentação
- Auditorias e certificações

## 📌 Indicadores de Códigos Maliciosos
- Análise de comportamento suspeito
- Assinaturas de malware
- Análise de tráfego de rede

## 📌 Ataque Man-in-the-Browser
- Intercepta e manipula comunicação entre usuário e app web
- **Proteção:**
  - Criptografia
  - Autenticação Multifator (MFA)
  - Monitoramento de atividade suspeita

## 📌 Ambientes de Desenvolvimento

### 1. Desenvolvimento
- Código editado, testado localmente
- Sandbox para isolamento
- Acesso restrito à equipe

### 2. Teste/Integração
- Código de vários devs é mesclado
- Testes unitários, funcionais, integração
- Réplica do ambiente de produção

### 3. Preparação (Homologação/Pré-produção)
- Espelho da produção
- Testes de usabilidade, desempenho, carga
- Cliente valida (testes de aceitação)

### 4. Produção
- Ambiente real, usuários finais
- Disponibilidade 24/7
- Monitoramento contínuo
- Backup e recuperação de desastres

## 📌 Provisionamento
- Implantar aplicativo no ambiente de destino
- Alocar hardware, software, rede, dados
- Gerenciar versões e dependências

## 📌 Desprovisionamento
- Remover aplicativo, pacotes, configurações
- Liberar recursos não usados
- Limpar dados sensíveis

## 📌 Controle de Versão
- Sistema que identifica cada iteração do software
- **Práticas:**
  - Git, SVN (rastrear alterações)
  - Rastreabilidade (quem, quando, por que)
  - Gerenciamento de mudanças (branches, merge)
  - Documentação atualizada

---

## 💡 Meus insights
- DevSecOps: segurança não é etapa final, é desde o início. Cultura, não ferramenta.
- Automação: configurar 10 servidores manualmente é pedir pra errar. Infra como código (IaC) é caminho.
- Cascata vs Ágil: cascata funciona quando requisito é estável (ponte, avião). Ágil pra software que muda toda hora.
- Garantia de Qualidade: testar não é só achar bug, é garantir que atende o que o cliente precisa.
- Man-in-the-Browser: malware no navegador vê tudo. MFA ajuda, mas se o token também for roubado...
- Ambientes: ter desenvolvimento, teste, homologação e produção separados é essencial. Já vi dev testando direto em produção (desesperador).
- Sandbox: isolar pra não interferir no resto da máquina. Teste seguro sem quebrar nada.
- Homologação: cliente aprovar antes de ir pra produção evita surpresa. "Mas não foi isso que pedi!"
- Provisionamento: criar ambiente do zero de forma padronizada. Docker e Kubernetes ajudam muito.
- Desprovisionamento: esquecer de desativar conta de ex-funcionário é falha grave. Processo tem que existir.
- Controle de Versão: Git salvou minha vida várias vezes. "Deu merda, volta pro commit passado."
- Rastreabilidade: saber quem alterou o quê. Em incidente de segurança, isso é ouro.
- Infraestrutura como código (Terraform, Ansible) resolve. Tudo versionado, tudo replicável.