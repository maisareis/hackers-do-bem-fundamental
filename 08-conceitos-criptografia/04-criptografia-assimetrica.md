# Módulo 8 – Conceitos de Criptografia

## Aula 4 – Criptografia Assimétrica

## 📌 Funcionamento da criptografia assimétrica

### Componentes – Geração do par de chaves
- Par de chaves: **chave pública** e **chave privada**
- Matematicamente relacionadas, mas inviável derivar uma da outra
- Chave pública: divulgada publicamente
- Chave privada: mantida em sigilo pelo proprietário
- Cada parte pode ter seu próprio par de chaves

### Criptografia
- Remetente usa uma das chaves (pública ou privada) para cifrar
- Função matemática aplicada à mensagem original + chave
- Resultado: mensagem cifrada
- Só pode ser descriptografada com a outra chave correspondente

### Transmissão
- Mensagem cifrada é transmitida
- Somente destinatário com a chave correspondente pode descriptografar

### Descriptografia
- Destinatário recebe mensagem cifrada
- Usa a chave correspondente para decifrar
- Recupera a mensagem original

## 📌 Criptografia assimétrica para confidencialidade

### Processo completo
1. **Bob gera par de chaves**: PubBob (pública) e PrivBob (privada)
2. **Bob compartilha PubBob** publicamente
3. **Alice cifra dados** com PubBob
4. **Alice transmite dados cifrados** para Bob
5. **Bob decifra dados** com PrivBob

## 📌 Criptografia assimétrica para assinaturas digitais

### Processo completo
1. **Alice gera par de chaves**: PubAlice (pública) e PrivAlice (privada)
2. **Alice aplica função hash** ao documento → resumo criptográfico
3. **Alice cifra resumo e documento** com PrivAlice → arquivo assinado
4. **Alice disponibiliza arquivo assinado**
5. **Bob verifica assinatura**:
   - Usa PubAlice para descriptografar → obtém documento + resumo original
   - Aplica mesma função hash ao documento
   - Compara resumo gerado com resumo original
   - Se iguais: integridade confirmada e autoria atribuída a Alice

## 📌 Desafios e considerações
- **Desempenho**: mais lenta que criptografia simétrica
- **Gerenciamento de chaves**: complexo, mas mais escalável
- **Algoritmos e padrões**: usar apenas os confiáveis
- **Criptografia híbrida**: combina assimétrica (troca de chave) + simétrica (dados)
- **Atualização e segurança**: algoritmos podem se tornar obsoletos

## 📌 Principais algoritmos

### RSA (Rivest, Shamir, Adleman)
- Mais utilizado
- Baseado na dificuldade de fatorar grandes números inteiros
- Chaves de 2048 bits ou mais (considerado seguro)
- Usos: criptografia de dados, PGP, SSH, autenticação

### DSA (Digital Signature Algorithm)
- Focado em assinaturas digitais
- Chaves de 1024 bits ou mais
- Usos: e-mail criptografado, certificados digitais (PKI), TLS/SSL

### ElGamal
- Combina criptografia de chave pública e troca de chaves Diffie-Hellman
- Chaves de 2048 bits ou mais
- Usos: e-mail criptografado, compartilhamento seguro de chaves, criptografia de arquivos

### ECC (Elliptic Curve Cryptography)
- Baseado em curvas elípticas sobre corpos finitos
- Chave de 256 bits = segurança equivalente a RSA 3072 bits
- Mais eficiente (menor chave, mesma segurança)
- Usos: TLS/SSL, smart cards, IoT

## 📌 Comparação: Simétrica x Assimétrica

| Característica | Simétrica | Assimétrica |
|----------------|-----------|-------------|
| Desempenho | Superior (mais rápida) | Inferior (mais lenta) |
| Autenticação | Não tem mecanismo | Sim (assinaturas digitais) |
| Irrefutabilidade | Não (autoria pode ser negada) | Sim (assinatura é irrefutável) |
| Distribuição de chaves | Trabalhosa (muitas chaves) | Simplificada |
| Acesso | Qualquer um com a chave | Restrito ao proprietário da chave privada |

---

## 💡 Meus insights
- **Assimétrica resolve o problema da distribuição de chaves**, mas é mais lenta. Por isso sistemas reais usam **híbrido**: assimétrica para trocar chave de sessão, simétrica para os dados.
- **RSA 2048** é o padrão hoje. 4096 para quem quer exagero de segurança.
- **ECC** é o futuro. Mesma segurança com chaves menores, ideal para dispositivos com pouca capacidade (IoT, cartões).
- **Assinatura digital** é o equivalente a um "carimbo" que prova autoria e integridade. Se o documento for alterado, a assinatura quebra.
- **Irrefutabilidade** significa que Alice não pode negar que assinou. Isso é poderoso juridicamente.
- **Diffie-Hellman** (mencionado em ElGamal) é a base para troca segura de chaves. Dois lados geram chave compartilhada sem nunca enviar a chave em si.
- **Criptografia híbrida** é o que acontece no HTTPS: assimétrica no handshake (TLS), simétrica nos dados.
- **Gerenciamento de chaves** ainda é complexo, mas menos que na simétrica. PKI (Infraestrutura de Chaves Públicas) organiza isso com certificados e autoridades certificadoras.