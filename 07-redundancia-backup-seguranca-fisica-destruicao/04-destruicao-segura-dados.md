# Aula 4 – Técnicas para Destruição Segura de Dados

## 📌 Técnicas Físicas de Destruição
- Manipulação direta dos dispositivos
- Tornam dispositivos irreparáveis
- Inviabilizam recuperação de informações

### Trituração
- Equipamentos especializados (triturador industrial)
- Reduz dispositivos a pequenos pedaços
- Para: discos rígidos, fitas, CDs/DVDs, cartões de memória

### Trituração Criptográfica
- Dados são criptografados antes da trituração
- Mesmo que alguém recupere os pedaços, dados estão ilegíveis
- Camada extra de segurança

### Perfuração
- Criar furos ou danos significativos
- Atingir áreas críticas (pratos magnéticos)
- Torna dispositivo inoperável

### Incineração
- Queima controlada em fornos especiais
- Altas temperaturas derretem e deformam componentes
- Reduz a cinzas
- Necessário controle de poluição

### Degaussing
- Desmagnetizador gera campo magnético intenso
- Para mídias magnéticas (discos rígidos, fitas, cartões)
- Partículas perdem orientação magnética
- Dados eliminados de forma irreversível
- Mídia fica inutilizável

### Desmontagem
- Separar componentes manualmente
- Discos, chips, placas de circuito
- Componentes podem ser destruídos individualmente depois

## 📌 Técnicas de Formatação e Sobrescrita

### Formatação Rápida
- Recria sistema de arquivos
- Remove referências, mas dados permanecem intactos
- Dados podem ser recuperados com ferramentas especializadas

### Formatação Completa
- Apaga sistema de arquivos
- Sobrescreve setores não alocados com zeros ou padrões
- Mais segura que rápida, mas ainda recuperável com técnicas avançadas

### Sobrescrita de Múltiplas Passagens
- Substitui dados com padrões de bits repetidas vezes
- Cada passagem usa padrão diferente
- Geralmente 3 ou mais passagens

### Sobrescrita com Padrão DoD 5220.22-M
- Padrão do Departamento de Defesa dos EUA
- **3 passagens:**
  1. Todos bits com zeros (0)
  2. Todos bits com uns (1)
  3. Padrão aleatório (0 e 1)

### Sobrescrita com Criptografia
- Dados são criptografados antes da formatação/sobrescrita
- Mesmo que recuperados, permanecem ilegíveis
- Chave de descriptografia é destruída

## 📌 Aplicativos Especializados
- **Eraser** → sobrescrita de arquivos com padrões específicos
- **DBAN (Darik's Boot and Nuke)** → bootável, sobrescreve discos inteiros
- **Secure Eraser** → opções de sobrescrita com diferentes padrões

---

## 💡 Meus insights
- Trituração é a mais garantida fisicamente. Se vira pó, não tem volta.
- Trituração criptográfica é exagero? Talvez, mas se o dado é ultrassecreto, vale.
- Perfurar disco rígido: tem que acertar os pratos. Não adianta só furar a carcaça.
- Incineração: eficaz mas problemático pro meio ambiente. Último caso.
- Degaussing: mágico. Campo magnético apaga tudo num instante. Mas mídia vira peso de papel.
- Desmontagem: trabalhoso, mas permite reciclar componentes separadamente.
- Formatação rápida: útil pra vender/doar equipamento? Não! Dados ainda estão lá.
- Formatação completa: melhor, mas ainda recuperável com laboratório forense.
- Múltiplas passagens: quanto mais passagens, mais seguro. Mas demora.
- DoD 5220.22-M: referência de segurança. Se o exército americano usa, é confiável.
- Criptografar antes: inteligente. Se o processo de sobrescrita falhar, dados ainda estão protegidos.
- DBAN: já usei. Boota, escolhe disco, e "nuke". Simples e eficaz.
- Regra de ouro: se o dado é muito sensível, destruição física + criptografia. Cinto e suspensório.