# Módulo 9 – Infraestrutura de Chaves Públicas e Blockchain

## Aula 2 – Certificado Digital

## 📌 Certificados digitais e seu ciclo de vida

### Conceito
- Documento eletrônico que contém informações de identificação
- Exemplos de dados: nome do titular, identidade, chave pública, período de validade, assinatura digital da AC emissora
- Pode ser para pessoa física, jurídica ou dispositivo
- Emitido por ACs confiáveis dentro de uma PKI
- Chave privada é mantida em sigilo pelo titular

### Ciclo de vida
1. **Solicitação**: enviada à AC
2. **Verificação**: identidade do solicitante é checada
3. **Emissão**: AC gera o certificado
4. **Distribuição**: certificado entregue ao titular
5. **Uso**: autenticação, criptografia, assinatura digital
6. **Renovação**: antes do vencimento
7. **Revogação**: por problemas de segurança (vai para LCR)
8. **Expiração**: após data de validade

## 📌 Tipos comuns de arquivos de certificado
- **PFX/P12 (PKCS#12)**: exporta/importa certificados + chave privada
- **P7B/PKCS#7**: armazena certificados em formato compacto (.p7b, .p7c)
- **CRL (Certificate Revocation List)**: lista de certificados revogados (binário ou Base64)
- **Keychain/Key Stores**: containers de chave (macOS, Windows)

## 📌 Tipos de certificados de servidor web

### DV (Domain Validation)
- Mais utilizado
- Validação por e-mail do domínio ou registro DNS
- Baixo custo, fácil obtenção

### OV (Organization Validation)
- Validação mais rigorosa que DV
- Verifica propriedade do domínio + existência legal da organização
- Exibe informações da organização no certificado

### EV (Extended Validation)
- Maior nível de confiança
- Exibe nome da organização na barra de endereços do navegador
- Verificações detalhadas de identidade
- Usado por instituições financeiras e e-commerce

## 📌 Outros tipos de certificados
- **Email/Usuário**: assinar e criptografar e-mails (S/MIME, PGP)
- **Assinatura de Código (Code Signing)**: para editores de software assinarem executáveis/DLLs

## 📌 Arquitetura de certificados digitais – X.509
- **Versão**: padrão X.509
- **Número de Série**: único dentro da AC
- **Algoritmo de Assinatura do Emitente**: RSA, DSA, ECDSA
- **Nome do Emitente**: identificação da AC
- **Período de Validade**: "válido de" e "válido até"
- **Nome do Sujeito**: titular do certificado
- **Chave Pública**: correspondente à chave privada do titular
- **Identificador de Algoritmo de Assinatura**
- **Extensões (opcional)**: informações adicionais
- **Assinatura Digital**: assinatura da AC (garante autenticidade e integridade)

## 📌 Atributos do nome do assunto
- **CN (Common Name)**: identificação inequívoca do titular
- **SAN (Subject Alternative Name)**: permite incluir nomes alternativos (ex: múltiplos domínios em um certificado)

---

## 💡 Meus insights
- **Ciclo de vida do certificado** é como um documento de identidade: nasce (solicitação), vive (uso), morre (expira) ou é cancelado (revogação).
- **Revogação** é crítica. Se uma chave privada vazar, o certificado precisa ser invalidado imediatamente. Daí a importância da LCR e OCSP.
- **DV vs OV vs EV**:
  - DV: só prova que você controla o domínio (básico)
  - OV: prova que existe uma organização por trás (confiança média)
  - EV: barra verde no navegador (máxima confiança)
- **SAN** é muito útil para certificados wildcard ou multi-domínio. Um único certificado cobre vários sites.
- **PFX/P12** é o formato que contém a chave privada. Deve ser protegido como um tesouro.
- **CRL** pode ficar grande. Por isso existe OCSP, que consulta online e em tempo real.
- **X.509** é o padrão universal. Todo certificado SSL que você vê no navegador segue essa estrutura.