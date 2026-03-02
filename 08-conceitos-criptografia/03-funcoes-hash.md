# Módulo 8 – Conceitos de Criptografia

## Aula 3 – Funções Hash

## 📌 Características das Funções Hash

### O que é uma função hash?
- Algoritmo que recebe dados de entrada e produz uma sequência de tamanho fixo (hash/resumo)
- Rápida de calcular e determinística (mesma entrada → mesmo hash)
- Mapeia dados de tamanho arbitrário para um valor de hash de tamanho fixo
- Representa de forma única e compacta os dados originais

### Usos
- Criptografia
- Verificação de integridade de dados
- Autenticação
- Indexação de informações
- Proteção de senhas

### Qualidades esperadas
- Deve produzir valores únicos para diferentes conjuntos de dados

## 📌 Resistência a tentativas de inversão
- Dificuldade de recuperar os dados originais a partir do valor de hash
- Deve ser computacionalmente inviável encontrar a entrada original
- Garante que, mesmo com acesso aos hashes, não se descubra a senha original
- Atacante precisaria testar combinações até encontrar colisão

## 📌 Colisões
- Ocorrem quando duas entradas diferentes produzem o mesmo valor de hash
- É indesejável, pois compromete a unicidade
- Podem ser exploradas para falsificar informações
- Funções hash de qualidade devem ter resistência a colisões

## 📌 Distribuição uniforme
- Valores de hash devem ser distribuídos de forma equilibrada no espaço de saída
- Todos os possíveis valores têm mesma probabilidade de serem gerados
- Evita agrupamentos e reduz probabilidade de colisões

## 📌 Unicidade
- Cada conjunto de dados de entrada deve produzir um hash único
- Permite identificar e distinguir conjuntos de dados
- Essencial para: armazenamento, indexação, detecção de duplicatas, verificação de integridade
- Em teoria, colisões são inevitáveis (espaço limitado), mas na prática devem ser extremamente raras
- Quanto maior o espaço de hash, menor a probabilidade de colisões

## 📌 Confusão em funções hash
- Resultado do hash altamente dependente de mudanças na entrada
- Pequenas alterações produzem valores radicalmente diferentes
- Alcançada por embaralhamento que amplifica diferenças
- Dificulta manipulação sem alterar drasticamente o hash
- Evita correlações entre entrada e saída

## 📌 Difusão em funções hash
- Espalha características dos dados de entrada por todo o valor de hash
- Qualquer mudança afeta significativamente todos os bits do hash
- Alcançada por processamento iterativo e transformações

## 📌 Paradoxo do aniversário em funções hash
- Probabilidade de colisões aumenta com o número de elementos
- Torna-se significativa quando número de entradas se aproxima da raiz quadrada do espaço de hash
- Exemplo: espaço de 10.000 valores → probabilidade alta com ~100 entradas

## 📌 Principais algoritmos

### MD5 (Message Digest Algorithm 5)
- Blocos de 512 bits
- 4 etapas: inicialização, processamento de blocos, finalização, geração do hash
- Vulnerável, colisões possíveis com ataques modernos
- Não é mais seguro para aplicações críticas

### SHA-1 (Secure Hash Algorithm 1)
- Blocos de 512 bits, hash de 160 bits
- Vulnerabilidades conhecidas desde 2005
- Inseguro para aplicações críticas

### SHA-2
- Família de algoritmos: SHA-224, SHA-256, SHA-384, SHA-512
- Números indicam tamanho do hash em bits
- Quanto maior, maior a resistência a ataques

### SHA-3
- Família: SHA3-224, SHA3-256, SHA3-384, SHA3-512
- Mais seguro que SHA-2
- Recomendado para alto nível de proteção
- Usado em autenticação, assinaturas digitais, segurança em redes

### RIPEMD-160
- Extensão do RIPEMD original, hash de 160 bits
- Alternativa ao SHA-1 e MD5
- Usado em criptografia, integridade de dados, assinaturas digitais

### BLAKE2
- Versões: Blake2b (512 bits), Blake2s (256 bits)
- Extremamente rápido, otimizado para processadores modernos
- Difusão e confusão bem equilibradas

---

## 💡 Meus insights
- **Hash não é criptografia**: criptografia pode ser revertida (com a chave), hash não. É uma via de mão única.
- **Resistência à inversão** é o que torna hash seguro para senhas. Se o banco vazar, o atacante não descobre a senha original.
- **Colisões são o fim do mundo** para uma função hash. Por isso MD5 e SHA-1 foram aposentados.
- **Paradoxo do aniversário** explica por que precisamos de hashes grandes. 128 bits já não é suficiente hoje (2^64 tentativas ~ 18 quintilhões).
- **SHA-256** é o padrão atual para segurança. Usado em blockchain, certificados SSL, etc.
- **BLAKE2** é mais rápido que SHA e tão seguro. Usado em aplicações de alta performance.
- **Salt em senhas** não foi mencionado, mas é essencial: adicionar dado aleatório antes do hash evita ataques com rainbow tables.
- **Hash + salt** + iterações (bcrypt, PBKDF2, Argon2) é o mínimo para senhas hoje.