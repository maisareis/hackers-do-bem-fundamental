# Módulo 8 – Conceitos de Criptografia

## Aula 2 – Criptografia Simétrica

## 📌 Componentes e funcionamento
- **Texto Claro (Plaintext)**: dados originais legíveis
- **Chave Simétrica (Symmetric Key)**: mesma chave usada para cifrar e decifrar
- **Cifra (Cipher)**: algoritmo que realiza a transformação
- **Texto Cifrado (Ciphertext)**: dados após aplicação da criptografia

## 📌 Cifra de Fluxo
- Transforma dados em um fluxo contínuo de caracteres cifrados
- Combina bits do texto claro com uma sequência de bits gerada pela chave (fluxo de chave)
- Usa operação lógica XOR para combinar os bits
- Rápida e eficiente em recursos computacionais
- Qualquer falha na geração do fluxo pode comprometer a segurança

## 📌 Cifra de Blocos
- Divide o texto claro em blocos de tamanho fixo
- Criptografa cada bloco independentemente
- Tamanhos comuns: 64 bits (8 bytes) ou 128 bits (16 bytes)
- Modos de operação principais:
  - **ECB (Electronic Codebook)**
  - **CBC (Cipher Block Chaining)**
  - **CTR (Counter Mode)**

## 📌 Distribuição de chaves – Problemas
- Chave secreta precisa ser compartilhada
- Número de chaves cresce exponencialmente com o número de participantes
- Escalabilidade é um desafio

## 📌 Principais algoritmos modernos

### DES (Data Encryption Standard)
- Criptografia simétrica de blocos (64 bits)
- Usa estrutura de rede Feistel com 16 rounds
- Atualmente considerado inseguro (chave curta)

### 3DES (Triple DES)
- Extensão do DES, aplica criptografia 3 vezes
- Opera em blocos de 64 bits
- Modos: ECB, CBC
- Etapas: criptografia → descriptografia → criptografia

### RC4 (Rivest Cipher 4)
- Cifra de fluxo
- Gera keystream pseudoaleatório combinado com XOR
- Duas partes: inicialização e geração do keystream
- Problemas de segurança em determinados usos

### RC6 (Rivest Cipher 6)
- Criptografia simétrica de blocos (128 bits)
- Suporta chaves de 128, 192 e 256 bits
- Considerado seguro e eficiente

### Blowfish
- Criptografia simétrica de blocos (64 bits)
- Chaves de tamanho variável (32 a 448 bits)
- Rápido e eficiente

### Twofish
- Criptografia simétrica de blocos (128 bits)
- Quatro etapas: expansão de chaves, permutação, substituição, combinação linear
- Suporta chaves de 128, 192 e 256 bits
- Altamente seguro

### AES (Advanced Encryption Standard)
- Padrão atual do NIST
- Blocos de 128 bits
- Chaves de 128, 192 e 256 bits
- Mais confiável e amplamente utilizado

---

## 💡 Meus insights
- **Cifra de fluxo** é como um cifrador de fita contínua: rápido, mas se a sequência se repetir, quebra a segurança.
- **Cifra de blocos** precisa de modos de operação para evitar padrões (ECB é inseguro porque blocos iguais viram texto cifrado igual).
- **Distribuição de chaves** é o calcanhar de Aquiles da criptografia simétrica. Como enviar a chave com segurança? Esse problema levou à criptografia assimétrica.
- **DES** foi um marco, mas hoje um computador comum quebra em horas.
- **3DES** é uma gambiarra elegante, mas lenta. Aposentado em favor do AES.
- **AES** é o padrão ouro. Usado pelo governo dos EUA, todo mundo confia.
- **RC4** já foi usado no WEP e WPA, mas hoje é evitado. Falhas de segurança conhecidas.
- **Twofish** é seguro mas pouco usado. Concorrente do AES na seleção do NIST.
- **Blowfish** é antigo mas ainda usado em aplicações específicas (ex: bcrypt).
- **Tamanho da chave importa**: 128 bits é seguro hoje, 256 é para futuro e ultraconfidenciais.