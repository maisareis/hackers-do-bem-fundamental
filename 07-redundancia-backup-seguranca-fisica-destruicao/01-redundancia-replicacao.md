# Aula 1 – Redundância e Replicação

## 📌 Redundância
- Componentes ou sistemas duplicados
- Evita perda de dados ou interrupção

### Disponibilidade Contínua
- Cluster de servidores: se um falha, outro assume
- Ex: site de e-commerce com vários servidores web

### Tolerância a Falhas
- Se um componente falha, outros assumem
- Reduz impacto de falhas únicas

### Recuperação Rápida
- Failover automático
- Balanceador de carga detecta falha e redireciona

### Proteção contra Desastres
- Backup em local geograficamente separado
- Data center externo, nuvem

### Melhoria da Escalabilidade
- Adicionar mais servidores conforme demanda
- Distribuir carga de trabalho

## 📌 Replicação
- Criar cópias idênticas em diferentes locais
- Garante disponibilidade e resiliência
- Pode ser de dados, sistemas, servidores

## 📌 RAID (Redundant Array of Independent Disks)

### Implementação
- **Via software** → SO gerencia, mais flexível, usa CPU
- **Via hardware** → controladora dedicada, mais performance, mais caro

### Níveis de RAID
| Nível | Nome | Como funciona | Vantagem | Desvantagem |
|-------|------|---------------|----------|-------------|
| **RAID 0** | Striping | Divide dados entre discos | Performance | Sem tolerância a falhas |
| **RAID 1** | Espelhamento | Cópia idêntica em 2+ discos | Redundância | Capacidade pela metade |
| **RAID 5** | Striping com paridade | Dados + paridade distribuída | Equilíbrio | 1 disco de paridade |
| **RAID 6** | Dupla paridade | Dados + 2 paridades | Tolerância a 2 falhas | Mínimo 4 discos |
| **RAID 10 (1+0)** | Espelhamento + Striping | Primeiro espelha, depois striping | Performance + redundância | Precisa de 4+ discos |
| **RAID 01 (0+1)** | Striping + Espelhamento | Primeiro striping, depois espelha | Performance + redundância | Menos comum |

## 📌 Rsync (Remote Synchronization)
- Sincronização eficiente de arquivos
- **Transferência delta** → só envia partes modificadas

### Funcionamento
1. Compara arquivos (tamanho, timestamp, checksum)
2. Transfere apenas blocos modificados (deltas)
3. Reconstrói arquivo no destino

## 📌 Replicação Síncrona
- Dados replicados em tempo real
- Gravação só conclui quando réplica confirma
- Consistência total, mas pode afetar performance
- Ex: Oracle Data Guard

## 📌 Replicação Assíncrona
- Dados replicados em intervalo definido
- Gravação conclui mais rápido
- Pequeno atraso na sincronização (aceitável)
- Ideal para recuperação de desastres

## 📌 Replicação em Nuvem
- **Síncrona** → tempo real entre regiões (Amazon S3 Replication)
- **Assíncrona** → intervalos definidos (Azure Geo-Replication)
- **Híbrida** → combina os dois conforme necessidade

---

## 💡 Meus insights
- Redundância não é só ter backup, é ter disponível na hora. Cluster com failover automático é o sonho.
- RAID 0 é rápido mas arriscado. Se um disco morre, perde tudo. Uso só pra dados temporários.
- RAID 1 é simples e seguro. Dois discos idênticos, se um falha, o outro tá lá.
- RAID 5 é bom equilíbrio. Paridade distribuída, aproveita melhor os discos.
- RAID 6 é seguro contra falha dupla. Em arrays grandes, dois discos falharem é possível.
- RAID 10 é o melhor dos dois mundos. Performance do 0, segurança do 1. Meu favorito.
- Rsync é genial. Enviar arquivo de 1GB que mudou 1KB? Rsync manda só o KB.
- Replicação síncrona: garantia de consistência, mas latência alta. Bom pra dados críticos.
- Replicação assíncrona: pode perder últimas transações se der pau, mas performance melhor.
- Replicação em nuvem: dados replicados em continentes diferentes. Desastre natural num lugar, dados seguros no outro.
- Escolha do RAID depende do uso. Banco de dados: RAID 10. Arquivos: RAID 5 ou 6.