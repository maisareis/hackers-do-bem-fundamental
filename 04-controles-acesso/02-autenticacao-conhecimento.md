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
[adicione aqui suas observações pessoais]