# Aula 3 – Estratégias de Resiliência

## 📌 Gerenciamento de Configuração
Saber exatamente como cada componente da TI está configurado e manter isso documentado.

## 📌 Gerenciamento de Ativos
Inventariar todos os dispositivos, sistemas e dados da organização.

## 📌 Controle de Mudanças
Antes de alterar qualquer coisa, registrar o pedido (RFC), avaliar o impacto e ter um plano de reversão.

## 📌 Resiliência de site
- 🔥 **Hot site** → cópia em tempo real, ativa imediatamente
- 🌡️ **Warm site** → parcialmente configurado, leva algum tempo
- ❄️ **Cold site** → estrutura vazia, leva mais tempo para ativar

## 📌 Defesa em profundidade
Várias camadas de segurança. Se uma falhar, as outras ainda protegem.

## 📌 Estratégias de engano
- **Honeypot** → sistema armadilha para atrair atacantes
- **Honeynet** → rede de honeypots
- **Honeyfile** → arquivo falso para detectar acesso não autorizado

---

## 💡 Meus insights
- **Gerenciamento de Configuração:** Se não sei o que tem na rede, não posso proteger. Inventário atualizado é básico mas muita empresa falha nisso.
- **Controle de Mudanças:** Toda mudança precisa de plano de reversão. Já vi sistema parar por causa de atualização sem teste. Aprendi que "testar antes" não é frescura.
- **Hot/Warm/Cold site:**
  - **Hot site:** caro mas necessário pra sistema crítico (banco, hospital)
  - **Warm site:** meio termo
  - **Cold site:** mais barato, mas demora dias pra ativar
- **Defesa em profundidade:** Camadas e mais camadas. Se uma falha, a outra segura. É tipo roupa em dia frio - várias camadas.
- **Honeypot:** Adorei a ideia! Deixar um sistema falso pra atrair atacante enquanto ele perde tempo ali, a gente detecta e bloqueia.
- **Honeynet:** Vários honeypots juntos, uma rede inteira de engano.
- **Honeyfile:** Arquivo falso tipo "senhas.txt" que dispara alarme se alguém abrir. Genial!
- **Como Purple Team:** Quero aprender a configurar honeypots e honeynets pra estudar como atacantes pensam e agem.
- **Aprendizado:** O plano não é "se nunca vai cair", é "quando cair, a gente levanta rápido".
- **Dúvida:** Honeypot pode ser usado contra a gente se o atacante descobrir que é falso?
