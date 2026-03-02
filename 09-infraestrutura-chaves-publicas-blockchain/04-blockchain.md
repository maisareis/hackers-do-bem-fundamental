# Módulo 9 – Infraestrutura de Chaves Públicas e Blockchain

## Aula 4 – Blockchain

## 📌 Características do Blockchain
- Registros digitais descentralizados de transações ou eventos
- Armazena informações de forma sequencial em blocos concatenados
- Usa criptografia para interligar os blocos formando uma cadeia
- Cria identidades digitais e assinaturas digitais usando par de chaves
- Mantido por uma rede de computadores distribuídos (Nós)

## 📌 Blocos e Cadeia de Blocos
- Blocos são as unidades que integram a estrutura de dados
- Armazenam: dados de transação, timestamps e outras informações
- Interconectados entre si formando uma cadeia
- Permite rastreamento
- Garante integridade e confiabilidade

## 📌 Transações e Registros Distribuídos
- Transação: ação ou evento registrado nos blocos
- Cada Nó tem cópia completa da cadeia de blocos
- Cópias são atualizadas e sincronizadas periodicamente
- Todas as transações são compartilhadas e propagadas pela rede

## 📌 Algoritmos de Consenso
- Todos os Nós devem concordar para validar a cadeia
- Consenso sobre validade das transações para adicionar blocos
- Cada algoritmo tem características próprias

### Principais algoritmos
- **Proof of Work (PoW)**: prova de trabalho (mineração)
- **Proof of Stake (PoS)**: prova de participação
- **Delegated Proof of Stake (DPoS)**
- **Practical Byzantine Fault Tolerance (PBFT)**

## 📌 Criptografia e Segurança em Blockchain

### Criptografia assimétrica
- Chave privada: mantida em sigilo por cada participante
- Chave pública: derivada da privada, compartilhada com todos

### Função Hash
- Aplicada à transação
- Cada bloco contém o hash do bloco anterior → forma a cadeia

### Assinaturas Digitais
- Realizada com chave privada do remetente
- Verificada com chave pública correspondente

### Proteção da Privacidade
- Criptografia usando o par de chaves

## 📌 Tipos de Blockchain

### Blockchain Pública
- Descentralizada
- Participação aberta
- Transparência completa
- Transações verificadas e validadas pelos Nós
- Usa algoritmo de consenso
- Mineração
- Segurança elevada

### Blockchain Privada
- Controlada por uma organização ou grupo restrito
- Participantes precisam ser autorizados
- Acesso e permissões limitados
- Governança definida pela organização
- Consenso usa mecanismos adicionais
- Escalabilidade melhor que a pública
- Privacidade para participantes autorizados

### Blockchain de Consórcio ou Federada
- Controlada por um consórcio de organizações
- Cada organização tem um ou mais nós
- Permissões restritas aos membros do consórcio
- Modelo de governança acordado entre os membros
- Algoritmos: PBFT, PoA (Proof of Authority)
- Confiança interorganizacional
- Privacidade garantida por criptografia e compartimentalização

## 📌 Carteira de Criptomoedas
- Software ou serviço para armazenar, gerenciar e interagir com criptomoedas

### Recursos
- Chave Privada
- Chave Pública

### Tipos de carteira
- **Software**: aplicativos (mobile/desktop)
- **Hardware**: dispositivos físicos (ex: Ledger)
- **Online**: serviços web (exchanges)
- **Papel**: chaves impressas

### Segurança
- Chave privada é ponto crítico
- Recomenda-se 2FA e criptografia de dispositivo

---

## 💡 Meus insights
- **Blockchain é um livro-razão imutável e distribuído**. Uma vez que um bloco é adicionado, não pode ser alterado sem modificar todos os seguintes.
- **Hash do bloco anterior** é o que cria a "corrente". Qualquer tentativa de fraude quebra a cadeia.
- **Consenso** resolve o problema de confiança entre partes que não confiam umas nas outras. PoW gasta energia, PoS gasta participação.
- **Bitcoin usa PoW**, Ethereum migrou para PoS. PoS é mais eficiente energeticamente.
- **Blockchain pública** é como uma praça: qualquer um pode entrar e ver tudo.
- **Blockchain privada** é como um clube exclusivo: só entra quem é convidado.
- **Blockchain federada** é útil para consórcios empresariais. Vários bancos compartilhando a mesma rede, cada um com seu nó.
- **Carteira de criptomoedas não guarda moedas**, guarda chaves. As moedas estão na blockchain. Perdeu a chave, perdeu o acesso.
- **Hardware wallet** é o mais seguro para valores altos. Chave nunca sai do dispositivo.
- **Autenticação de dois fatores** é obrigatório para carteiras online.