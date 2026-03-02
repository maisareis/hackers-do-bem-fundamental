# Módulo 9 – Infraestrutura de Chaves Públicas e Blockchain

## Aula 1 – Autoridades Certificadoras

## 📌 Public Key Infrastructure (PKI)
- Conjunto de tecnologias, políticas e procedimentos para segurança em ambientes digitais
- Usa par de chaves: pública e privada
- Garante: autenticação, integridade, confidencialidade e não repúdio

### Chave pública
- Usada para criptografar informações ou verificar assinaturas digitais
- Derivada da chave privada

### Chave privada
- Usada para descriptografar informações criptografadas com a chave pública
- Usada para criar assinaturas digitais

## 📌 Autoridades Certificadoras (ACs)
- Responsáveis por emitir, validar e revogar certificados digitais
- Funções:
  - Garantir validade e identidade dos certificados solicitados
  - Estabelecer confiança na AC por parte dos usuários
  - Gerenciar repositórios
  - Gerenciar ciclo de vida das chaves e certificados
  - Gerar LCRs (Lista de Certificados Revogados)

## 📌 Modelos de confiança da PKI
- AC Única
- Hierárquico (com AC Intermediária)
- AC Online x AC Offline

## 📌 Tipos de ACs
- **Autoridade Certificadora de Domínio**: certificados para domínios web
- **Autoridade Certificadora de Email**: certificados para assinatura/criptografia de e-mail
- **Autoridade Certificadora de Assinatura de Código**: para assinar software
- **Autoridade Certificadora de Máquina/Computador**: identidade para dispositivos
- **Autoridade Certificadora de Dispositivo**: para dispositivos IoT, etc.
- **Autoridade Certificadora de Identidade**: vinculada a pessoas físicas/jurídicas
- **Autoridade Certificadora de Servidor**: para servidores web

## 📌 Autoridades de Registro (RA) e CSRs
- **RA**: verifica identidade dos solicitantes e coleta informações para emissão
- **CSR (Certificate Signing Request)**: documento gerado pelo solicitante com informações para criação do certificado

## 📌 Autoridades Certificadoras no Brasil – ITI
- **ITI (Instituto Nacional de Tecnologia da Informação)**:
  - Autarquia federal (iti.gov.br)
  - Mantém e executa políticas da ICP-Brasil
  - É a AC Raiz
  - Audita e fiscaliza entidades da cadeia ICP-Brasil

### Hierarquia ICP-Brasil
- AC Raiz (ITI)
- ACs Subordinadas
- ACs Autorizadas

---

## 💡 Meus insights
- **PKI é a infraestrutura que torna a internet segura**. Sem ela, não haveria HTTPS, e-mails criptografados ou assinaturas digitais confiáveis.
- **AC Raiz é a "fonte da verdade"**. Se ela for comprometida, toda a cadeia de confiança quebra.
- **ITI no Brasil** é o órgão máximo. Todo certificado ICP-Brasil confiável vem dessa raiz.
- **CSR** é como uma "solicitação de identidade". A AC recebe, valida e devolve o certificado assinado.
- **RA** faz o trabalho braçal de verificar documentos. A AC só assina.
- **Modelo hierárquico** permite delegar confiança. AC Raiz assina AC Intermediária, que assina certificados finais. Se uma intermediária cair, a raiz ainda está segura.
- **AC Offline** é usada para assinar chaves de outras ACs, mantida desconectada para segurança máxima.