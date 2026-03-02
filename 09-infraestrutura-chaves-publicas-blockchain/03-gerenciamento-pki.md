# Módulo 9 – Infraestrutura de Chaves Públicas e Blockchain

## Aula 3 – Gerenciamento de Infraestrutura de Chaves Públicas (PKI)

## 📌 Gerenciamento de Chaves
- Administração e controle das chaves de criptografia
- Garante: confidencialidade, integridade, autenticidade

### Ciclo de vida das chaves
1. Geração
2. Solicitação e Emissão de Certificados
3. Armazenamento e Proteção
4. Renovação e Atualização
5. Revogação
6. Destruição

## 📌 Tipos de gerenciamento de chave

### Centralizado
- Armazenamento e gerenciamento a partir de um ponto central
- Servidor de chaves dedicado
- Executado pelas ACs
- Controle mais rigoroso e padronizado

### Descentralizado
- Armazenamento e gerenciamento distribuídos
- Cada entidade gera suas próprias chaves e certificados
- Maior autonomia e flexibilidade
- Dificuldades de coordenação e padronização

## 📌 Vulnerabilidades no gerenciamento de certificados
- Exposição de Chaves Privadas
- Certificados Inválidos ou Comprometidos
- Falta de Revogação de Certificados
- Falha na Renovação de Certificados
- Uso de Algoritmos e Parâmetros Obsoletos
- Falta de Monitoramento e Auditoria

## 📌 Controle de acesso a chaves – M de N
- Mecanismo para ambientes de alto risco
- **M** = número mínimo de entidades para desbloquear chaves privadas
- **N** = número total de entidades ou partes envolvidas
- Exemplo: controle **2 de 3** → duas das três entidades autorizadas participam para desbloquear

## 📌 Custódia de chaves (Key Escrow)
- Mecanismo confiável para armazenar cópia de segurança das chaves privadas
- Objetivo: recuperar chaves em caso de perda, corrupção ou comprometimento
- Terceira parte confiável pode ser AC ou agência governamental

## 📌 Gerenciamento de Certificados
- Conjunto de práticas e processos para administrar certificados digitais
- Gerencia todo o ciclo de vida e armazenamento seguro

### Geração de certificados
- Solicitação de Certificado
- Criação do Par de Chaves
- Preenchimento dos Dados do Certificado
- Assinatura Digital
- Emissão do Certificado

## 📌 Revogação de Certificados e LCR (CRL)
- Revogação ocorre quando:
  - Certificado está comprometido ou suspeito
  - Informações incorretas
  - Titular deixa de ser autorizado
- Passos:
  1. Identificação da necessidade
  2. Publicação da Lista de Certificados Revogados (CRL)
  3. Verificação da Revogação

## 📌 Online Certificate Status Protocol (OCSP)
- Protocolo para consulta online do status de revogação
- Passos:
  - Solicitação OCSP
  - Resposta OCSP
  - Validação do Certificado

## 📌 Fixação de Certificado (Certificate Pinning)
- Garante autenticidade e integridade durante a comunicação
- Etapas:
  1. Seleção de Certificados
  2. Armazenamento de Informações de Identificação
  3. Verificação de Certificados
  4. Comparação e Validação

## 📌 OpenSSL
- Biblioteca de código aberto para implementação de criptografia
- Auxilia no gerenciamento de certificados em PKI
- Funcionalidades:
  - Geração de chaves
  - Criação e assinatura de certificados
  - Criação e verificação de assinaturas digitais
  - Verificação de Certificados
  - Gerenciamento de CRLs
  - Implementação de OCSP Responders

---

## 💡 Meus insights
- **Gerenciamento de chaves é o ponto mais crítico da PKI**. De nada adianta criptografia forte se a chave for mal guardada.
- **Controle M de N** é muito usado em empresas para acesso a cofres digitais. Impede que uma única pessoa tenha poder absoluto.
- **Key Escrow** é polêmico. Governos querem ter acesso, mas isso cria backdoors que podem ser explorados por atacantes.
- **Revogação** é tão importante quanto emissão. Um certificado comprometido precisa ser invalidado rápido. OCSP é mais eficiente que baixar CRL gigantes.
- **Certificate Pinning** é usado em apps móveis para evitar MITM. O app "grava" o certificado esperado e rejeita qualquer outro.
- **OpenSSL** é a ferramenta suíça. Quem trabalha com certificados precisa conhecer os comandos básicos.
- **Vulnerabilidades** mostram que PKI não é "configure e esqueça". Monitoramento contínuo é essencial.
- **Falha na renovação** já tirou muitos sites do ar. Certificado expirado = serviço indisponível.