# Aula 2 – Autenticação por Conhecimento

## 📌 Tipos de autenticação
- **Autenticação local** → login direto no dispositivo
- **Autenticação de rede** → verifica em servidor centralizado (Active Directory)
- **Autenticação remota** → via VPN, SSH

## 📌 Windows
- **Kerberos** → protocolo moderno, seguro, usa "tickets" para autenticação
- **NTLM** → protocolo antigo, ainda suportado por compatibilidade

## 📌 Linux
- Senhas armazenadas com hash em `/etc/shadow`
- **SSH** para acesso remoto seguro
- **PAM** para flexibilidade de autenticação

## 📌 SSO (Single Sign-On)
Faz login uma vez e acessa vários sistemas sem precisar logar de novo.

## 📌 Protocolos
- **PAP** → envia senha sem criptografia (inseguro)
- **CHAP** → usa desafio-resposta (mais seguro)
- **MS-CHAP** → versão Microsoft do CHAP, melhor segurança

## 📌 Tipos de ataque a senhas
- **Força bruta** → testa todas as combinações possíveis
- **Dicionário** → testa palavras comuns
- **Híbrido** → mistura dicionário + variações (ex: senha → Senha123)
- **Pulverização** → tenta a mesma senha em muitas contas
- **Offline** → ataca o banco de dados de hashes sem interagir com o sistema

---

## 💡 Meus insights
- **Tipos de autenticação:**
  - **Local:** login direto no PC (menos seguro)
  - **Rede:** servidor centralizado valida (Active Directory)
  - **Remota:** VPN, SSH (acesso de fora)

- **Windows:**
  - **Kerberos:** moderno, usa tickets, não transmite senha. É o padrão hoje.
  - **NTLM:** legado, ainda existe por compatibilidade mas é mais fraco.

- **Linux:**
  - Senhas ficam em `/etc/shadow` com hash (não em texto puro!)
  - **SSH:** acesso remoto seguro, chave pública/privada
  - **PAM:** módulos que permitem vários métodos de autenticação

- **SSO:** Login único. Entra uma vez, acessa tudo. Prático mas perigoso: se roubarem a conta, roubaram tudo.

- **Protocolos:**
  - **PAP:** senha em texto claro (NUNCA usar!)
  - **CHAP:** desafio-resposta, mais seguro
  - **MS-CHAP:** versão Microsoft do CHAP

- **Ataques a senhas:**
  - **Força bruta:** testa todas combinações (demora)
  - **Dicionário:** testa palavras comuns (mais rápido)
  - **Híbrido:** dicionário + números/símbolos (senha → Senha123)
  - **Pulverização:** mesma senha em várias contas (evita bloqueio)
  - **Offline:** ataca o hash roubado (mais perigoso, sem limite de tentativas)

- **Na prática:** 
  - Sempre usar MFA quando possível.
  - Senha forte é longa, com símbolos, e única pra cada serviço.

- **Como Purple Team:** 
  - Testar a política de senhas: será que ela realmente protege?
  - Simular ataques de pulverização pra ver se o sistema detecta.
