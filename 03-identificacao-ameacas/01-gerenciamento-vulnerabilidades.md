# Aula 1 – Gerenciamento de Vulnerabilidades

## 📌 Verificação de vulnerabilidades
Checar se o sistema tem falhas que podem ser exploradas.

## 📌 CVE
Banco de dados mundial de vulnerabilidades conhecidas (identificadas como CVE-ANO-NÚMERO).

## 📌 Tipos de varredura
- **Intrusiva (ativa)** → interage com o alvo, pode causar interrupção, mas é mais completa
- **Não intrusiva (passiva)** → observa sem interagir, mais segura mas menos precisa
- **Credenciada** → usa login para ver mais detalhes internos
- **Não credenciada** → visão de quem está de fora

## 📌 Cuidados com resultados
- **Falso positivo** → alarme sem real ameaça
- **Falso negativo** → ameaça real que passou despercebida **(mais perigoso!)**

---

## 💡 Meus insights
- **Varredura intrusiva vs passiva:** Intrusiva é quando você "bate na porta" pra ver se abre, passiva é quando só observa de longe. Cada uma tem seu momento certo.
- **Credenciada vs não credenciada:** Credenciada é como se fosse um funcionário testando o próprio sistema. Não credenciada é hacker de fora tentando entrar.
- **Falso negativo é o pior:** Prefiro mil alertas falsos do que um ataque passar despercebido. Falso negativo deixa a porta aberta.
- **Na prática:** Empresa grande precisa scan semanal. Pequena talvez mensal. Mas nunca deixar de fazer.
- **Dúvida:** Será que scan intrusivo pode derrubar um sistema? Preciso pesquisar isso.
- **Aprendizado:** Mais importante que achar vulnerabilidade é corrigir ela rápido. Scan sem remediação não serve de nada.
