# Aula 1 – Gerenciamento de Identidade e Acesso (IAM)

## 📌 Os 4 processos do IAM (IAAA)
1. **Identificação** → quem é você? (usuário, ID)
2. **Autenticação** → prove que você é quem diz ser (senha, biometria)
3. **Autorização** → o que você pode fazer?
4. **Accounting** → registro do que foi feito (trilha de auditoria)

## 📌 Fatores de autenticação
- **Conhecimento (Knowledge)** → algo que você sabe (senha, PIN)
- **Posse (Ownership)** → algo que você tem (token, cartão)
- **Biometria** → algo que você é (digital, face, voz)

## 📌 Atributos de autenticação
- **Localização** → de onde você está acessando?
- **Comportamento** → como você interage com o sistema?

## 📌 MFA (Multifator)
Usar dois ou mais fatores juntos. Ex: senha + token; digital + confirmação no celular.

---

## 💡 Meus insights
- **IAAA:** Os 4 passos fazem todo sentido:
  1. **Identificação:** "Quem é você?" (usuário)
  2. **Autenticação:** "Prove que é você" (senha, biometria)
  3. **Autorização:** "O que você pode fazer?" (permissões)
  4. **Accounting:** "O que você fez?" (logs)

- **Fatores de autenticação:**
  - **Conhecimento:** senha, PIN (mais comum, mais fraco)
  - **Posse:** token, celular, smart card
  - **Biometria:** digital, face, voz (mais seguro mas caro)

- **MFA:** Usei muito sem saber o nome. Sempre que pega código no celular além da senha, é MFA!

- **Na prática:** 
  - Banco usa MFA direto: senha + token no app.
  - Se só senha, qualquer vazamento já era.

- **Como Purple Team:** 
  - Simular ataques de força bruta e ver se a autenticação aguenta.
  - Testar se o "accounting" registra tudo certinho.
