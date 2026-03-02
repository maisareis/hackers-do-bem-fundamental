# Módulo 8 – Conceitos de Criptografia

## Aula 1 – Propriedades da Criptografia

## 📌 Propriedades da comunicação com criptografia

### Criptografia
- Prática de transformar informações legíveis em formato ilegível (texto cifrado)
- Objetivo: proteger confidencialidade, integridade e autenticidade
- Usa algoritmos matemáticos e chaves criptográficas

### Personagens
- **Alice**: entidade que envia mensagem de forma segura
- **Bob**: destinatário da mensagem
- **Mallory**: personagem mal-intencionado que tenta interceptar
- **Eve**: "espião" (eavesdropper)
- **Trent**: autoridade neutra e confiável
- **Oscar**: adversário avançado, hacker experiente
- **Charlie**: intermediário ou canal de comunicação
- **Carol**: parte legítima (como Alice e Bob)

## 📌 Propriedades dos algoritmos criptográficos

### Confusão
- Torna a relação entre a chave e o texto cifrado o mais complexa possível
- Alcançada por embaralhamento e dispersão das características dos dados de entrada
- Dificulta identificação de padrões pelos adversários
- Exige grande esforço computacional para quebrar a criptografia
- Garante resistência a ataques de força bruta, análise estatística e criptoanálise
- **Exemplo**: tabelas de substituição S-Box no AES

### Difusão
- Garante que qualquer alteração mínima nos dados de entrada cause mudança significativa nos dados de saída
- Propaga uma pequena modificação nos bits de entrada para vários bits diferentes no texto cifrado
- Torna a relação entre dados originais e criptografados o mais complexa possível
- Alcançada por substituições, permutações, misturas
- Distribui as propriedades estatísticas dos dados originais de forma uniforme

### Colisão
- Ocorre quando duas entradas distintas geram o mesmo resumo criptográfico
- É indesejável, pois compromete a integridade dos dados
- Se um invasor encontrar uma colisão, pode substituir dados originais por dados maliciosos sem ser detectado

## 📌 Estados dos dados
- **Dados em uso**: sendo processados na memória
- **Dados em trânsito**: trafegando na rede
- **Dados em repouso**: armazenados em disco

## 📌 Perfect Forward Secrecy (PFS)
- Garante confidencialidade mesmo que chaves de criptografia sejam comprometidas no futuro
- Chaves de sessão anteriores e futuras permanecem seguras
- Usa chaves efêmeras no estabelecimento da comunicação

## 📌 Paradoxo do Aniversário
- Probabilidade de duas ou mais pessoas em um grupo compartilharem a mesma data de aniversário
- Em 23 pessoas: 50,73% de chance
- Em 50 pessoas: ~97% de chance
- Em 70 pessoas: quase 100% de chance
- Aplicado em criptografia para ilustrar probabilidade de colisões em funções hash

## 📌 Técnicas de ocultação de dados

### Esteganografia
- Oculta informações dentro de outros tipos de arquivo sem levantar suspeitas
- Usa arquivos de mídia (imagens, áudios, vídeos) como meio para ocultar dados
- Dados são inseridos sem alterar aparência visual ou auditiva do arquivo

### Ofuscação
- Dificulta a compreensão do conteúdo por terceiros não autorizados
- Torna o código mais complexo e difícil de entender sem alterar funcionalidade
- Técnicas: renomeação de variáveis, substituição de trechos de código, inserção de instruções irrelevantes, reorganização da estrutura

### Fragmentação
- Divisão de um dado em partes menores (fragmentos) antes de aplicar criptografia
- Conteúdo original dividido em várias partes de tamanho fixo
- Dificulta reconstituição dos dados originais sem acesso a todos os fragmentos e à chave

---

## 💡 Meus insights
- **Confusão e Difusão** são os pilares da criptografia moderna. Confusão embaralha, difusão espalha. Juntas, tornam o texto cifrado irreconhecível.
- **Colisão** é o pesadelo das funções hash. Por isso algoritmos como MD5 foram aposentados.
- **PFS** é essencial para comunicações seguras. Mesmo que a chave privada do servidor vaze no futuro, as sessões passadas continuam seguras.
- **Paradoxo do Aniversário** explica por que hash de 64 bits é insuficiente hoje. Com 2^32 tentativas (~4 bilhões), a chance de colisão já é alta.
- **Esteganografia** é diferente de criptografia. Criptografia esconde o conteúdo, esteganografia esconde a existência da mensagem.
- **Ofuscação** não é segurança de verdade, mas dificulta engenharia reversa. Útil para proteger propriedade intelectual.
- **Fragmentação** + criptografia = camada extra. Se um fragmento for interceptado, sozinho não faz sentido.