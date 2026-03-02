# Aula 2 – Backup

## 📌 Tipos de Backup

### Backup Completo (Full)
- Cópia de todos os arquivos selecionados
- Independente de terem sido modificados ou não
- Restauração simples, mas demorado e ocupa espaço

### Backup Incremental
- Copia apenas alterações desde o último backup (completo ou incremental)
- Rápido e econômico (espaço)
- Restauração precisa de todos os incrementais desde o último full

### Backup Diferencial
- Copia todas as alterações desde o último backup completo
- Restauração precisa só do último full + último diferencial
- Ocupa mais espaço que incremental (cresce com o tempo)

### Backup Contínuo
- Cópias em tempo real, conforme dados são modificados
- Minimiza perda de dados
- Requer mais recursos (armazenamento/processamento)

### Backup Espelhado (Mirrored)
- Cópia exata em tempo real em local separado
- Alta disponibilidade
- Não protege contra exclusão acidental (reflete no espelho)

### Backup de Imagem (Image)
- Cópia exata de disco/partição inteiro (SO, apps, config, dados)
- Restaura sistema completo
- Ex: Acronis True Image, Clonezilla

### Backup em Nuvem (Cloud)
- Dados enviados para servidores remotos
- Escalável, acesso remoto, redundância geográfica
- Ex: Amazon S3, Google Cloud Storage, Azure Backup

### Backup Local
- Dispositivos físicos locais (HD externo, servidor, fita)
- Controle direto, acesso rápido

### Backup Remoto (Offsite)
- Local geograficamente separado
- Protege contra desastres locais (incêndio, inundação)

### Backup de Ponto de Verificação (Checkpoint)
- Instantâneo dos dados em momento específico
- Permite restaurar para estado anterior

## 📌 Ferramentas de Hardware para Backup
- Unidades de fita (LTO)
- Discos externos (HD, SSD)
- Bibliotecas de fita (automatizadas)
- Dispositivos de armazenamento em nuvem
- Appliances de backup (hardware + software)
- NAS (Network Attached Storage)
- VTL (Virtual Tape Library) → emula fita usando disco

## 📌 Mídias de Backup
- Fitas magnéticas (durabilidade, baixo custo/GB)
- Discos rígidos (velocidade)
- Nuvem (escalabilidade)
- Discos ópticos (CD/DVD/Blu-ray) → capacidade limitada
- SSDs (rápidos, resistentes, mais caros)

---

## 💡 Meus insights
- Full + Incremental: economiza espaço mas restauração demora. Precisa de todos os incrementais.
- Full + Diferencial: mais espaço mas restauração mais rápida (só 2 arquivos).
- Backup Contínuo: tipo Google Docs, salva automaticamente. Bom pra dados críticos.
- Backup Espelhado: RAID 1 é um exemplo. Se o disco principal queima, espelho assume.
- Backup de Imagem: formatou o PC? Restaura a imagem com tudo instalado. Economiza horas.
- Nuvem vs Local: nuvem = segurança geográfica. Local = velocidade de restauração.
- Regra 3-2-1: 3 cópias, 2 mídias diferentes, 1 offsite. Clássico e ainda vale.
- Fitas magnéticas: parece coisa antiga, mas ainda usam. Dura 30 anos se armazenado certo.
- NAS: ter um em casa com RAID 1 e backup automático é paz de espírito.
- VTL: velocidade de disco com compatibilidade de fita. Melhor dos dois mundos.
- Mais importante que fazer backup é testar restauração. Backup que não restaura não serve.