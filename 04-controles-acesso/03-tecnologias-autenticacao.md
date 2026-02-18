# Aula 3 – Tecnologias de Autenticação

## 📌 Smart Card
Cartão com chip que autentica via PIN + posse do cartão.

## 📌 HSM (Hardware Security Module)
Dispositivo físico para armazenar chaves criptográficas com segurança.

## 📌 IEEE 802.1X
Protocolo de controle de acesso à rede. Antes de entrar na rede, o dispositivo precisa se autenticar.

## 📌 RADIUS
Servidor que centraliza autenticação, autorização e contabilidade (AAA) para redes. Muito usado em Wi-Fi corporativo e VPN.

## 📌 Chaves de token
- **HOTP** → código gerado por contador (válido até ser usado)
- **TOTP** → código gerado por tempo (muda a cada 30 segundos, ex: Google Authenticator)

## 📌 Verificação em 2 etapas (2FA)
Senha + código no celular (ou outro fator). Mesmo que a senha vaze, o acesso ainda é protegido.

---

## 💡 Meus insights
- **Smart Card:** Cartão com chip + PIN. É algo que você tem + algo que você sabe. Muito usado em empresas grandes.

- **HSM (Hardware Security Module):** Dispositivo físico que guarda chaves criptográficas. Não dá pra acessar as chaves, só usar elas. Banco usa isso.

- **IEEE 802.1X:** Antes de entrar na rede, o dispositivo precisa se autenticar. Muito usado em Wi-Fi corporativo.

- **RADIUS:** Servidor central que cuida de autenticação, autorização e contabilidade (AAA). Wi-Fi, VPN, tudo pode usar RADIUS.

- **Tokens:**
  - **HOTP:** código baseado em contador (só muda quando usa)
  - **TOTP:** código baseado em tempo (muda a cada 30s). É o Google Authenticator!

- **2FA (Verificação em duas etapas):** Senha + código. Mesmo que a senha vaze, o código protege. Melhor coisa que inventaram.

- **Na prática:** 
  - Já usei TOTP sem saber o nome. App do banco, Google Authenticator… é isso!
  - Wi-Fi de empresa pede 802.1X, por isso que às vezes não conecta sem configuração.

- **Como Purple Team:** 
  - Testar se o RADIUS tá bem configurado, se alguém consegue burlar.
  - Simular perda de token e ver como a recuperação é feita.
