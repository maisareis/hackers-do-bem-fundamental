# Módulo 12 – Resposta a Incidentes e Protocolos Seguros

## Aula 4 – Forense Digital

## 📌 Conceitos de Forense Digital

### Evidência
- Registros eletrônicos coletados: dados, arquivos, logs, e-mails, imagens
- Tratamento cuidadoso e imparcial
- Preservação da integridade é essencial para aceitação pela Justiça
- Autenticidade deriva da cadeia de custódia

#### Categorias de evidência
- **Evidência direta**: comprova diretamente um fato
- **Evidência circunstancial**: cria conexão lógica entre eventos, mas não prova diretamente

### Devido processo legal (Due process)
- Proteção dos direitos individuais durante processos judiciais ou investigações
- Na Forense Digital: adotar procedimentos legais e éticos na busca de evidências
- Evitar abusos e violações de privacidade

### Retenção legal (Legal hold)
- Preservação de evidências eletrônicas relevantes
- Evita que evidências sejam destruídas, alteradas ou perdidas
- Etapas:
  - Identificação das informações
  - Notificação às partes envolvidas
  - Criação de política de retenção
- Não conformidade pode trazer sanções

### Cadeia de custódia (Chain of custody)
- Registro detalhado da evidência desde a coleta até a apresentação
- Etapas:
  - Selagem e identificação
  - Registro de transferências
  - Armazenamento seguro
  - Análises e exames
  - Registro de acesso e manipulação
  - Apresentação em Tribunal
  - Encerramento da cadeia

### Descoberta Eletrônica (E-Discovery)
- Identificação, filtragem e organização de evidências relevantes
- Cria base de dados para uso da Justiça
- Funções do E-Discovery:
  - Identificação e duplicação de arquivos e metadados
  - Busca
  - Marcadores (Tags)
  - Segurança
  - Divulgação (Disclosure)

### Entrevistas com Testemunhas
- Obter informações diretas sobre um evento
- Procedimentos:
  - **Preparação**: identificar testemunhas, criar roteiro
  - **Condução**: escolher formato, coletar informações, registrar em vídeo
  - **Preservação**: documentação completa, assinatura e consentimento
  - **Análise**: comparar com outras evidências, corroborar informações
  - **Apresentação**: depoimentos em Tribunal

### Inteligência Estratégica
- Tomada de decisão proativa baseada em pesquisa e análise de dados
- Etapas:
  - Coleta de dados: técnicos e contextuais
  - Análise: identificação de padrões, correlação
  - Geração de insights

### Contrainteligência
- Identificação e análise de táticas, técnicas e procedimentos (TTPs) de agentes maliciosos
- Visa identificar, prevenir e responder a atividades maliciosas
- Etapas:
  - Identificação de táticas do adversário
  - Coleta de informações
  - Análise de padrões
  - Análise das técnicas utilizadas (exame detalhado, avaliação de vulnerabilidades)
  - Definição de configurações de registros ativos
  - Auditoria e monitoramento
  - Resposta e ajuste de defesas

### Aquisição de dados
- Coleta de informações em meios eletrônicos de forma precisa
- Objetivo: cópia exata dos dados originais mantendo integridade
- Etapas:
  1. Identificação dos alvos
  2. Seleção das técnicas: Live Acquisition, Imagem de disco
  3. Preparação e planejamento: documentação, hardware, software
  4. Coleta de dados: cópia bit a bit
  5. Hashing e verificação
  6. Armazenamento seguro
  7. Registro completo
  8. Análise e exame

### Ordem de volatilidade
- Sequência de priorização da coleta de dados
- Visa obter evidências antes que sejam removidas
- Classificação:
  - **Dados voláteis**: perdidos ou alterados rapidamente (ex: memória RAM)
  - **Dados não voláteis**: permanecem após desligamento (ex: disco)
- Sequência de coleta:
  1. Memória RAM
  2. Cache do sistema
  3. Estado do processo
  4. Dados de disco

### Software de Forense Digital
- Ferramentas para investigar e analisar evidências digitais
- Principais:
  - **EnCase Forensic**
  - **The Forensic Toolkit (FTK)**
  - **The Sleuth Kit**
  - WinHex
  - The Volatility Framework

### Aquisição de memória de disco
- Cópia completa de dispositivo de armazenamento
- Etapas:
  - Identificação e preparação do alvo
  - Técnica de aquisição
  - Preparação e ferramentas
  - Aquisição da imagem
  - Armazenamento seguro

### Preservação e integridade da evidência
- Princípios fundamentais da forense digital
- Informações devem ser mantidas íntegras e confiáveis
- Processo inclui:
  - Cadeia de custódia
  - Coleta adequada
  - Armazenamento seguro
  - Hashing e verificação
  - Rastreamento da evidência
  - Preservação do ambiente

### Aquisição de outros dados
- Coleta em outras fontes digitais
- Inclui:
  - Aquisição de dados de rede
  - Aquisição de dados de cache
  - Artefatos e recuperação de dados
  - Aquisição de instantâneos (Snapshots)
  - Aquisição de Firmware

---

## 💡 Meus insights
- **Forense Digital** é a ciência de investigar crimes no mundo digital. Exige método e rigor.
- **Evidência direta vs circunstancial**: direta é um e-mail confessando; circunstancial é um login no horário do crime.
- **Due process** significa seguir as regras. Prova obtida ilegalmente não vale em tribunal.
- **Legal hold** impede que dados sejam destruídos. Empresas podem ser multadas se não cumprirem.
- **Cadeia de custódia** é sagrada. Qualquer falha invalida a prova.
- **E-Discovery** é usado em litígios corporativos. Milhares de e-mails e documentos precisam ser revisados.
- **Entrevistas** com testemunhas são parte da investigação. Técnicas de entrevista são importantes.
- **Contrainteligência** é o jogo de gato e rato. Entender o adversário para antecipar movimentos.
- **Ordem de volatilidade**: colete primeiro o que vai desaparecer. Memória RAM é a primeira.
- **Hashing** (SHA-256) garante que a cópia é idêntica ao original. Qualquer alteração muda o hash.
- **Ferramentas forenses** como FTK e EnCase são padrão da indústria. Saber usar é diferencial.
- **Volatility Framework** é essencial para análise de memória RAM. Malware muitas vezes só está lá.
- **Preservação**: o ambiente original deve ser mantido. Nunca investigar direto no disco original, sempre na cópia.