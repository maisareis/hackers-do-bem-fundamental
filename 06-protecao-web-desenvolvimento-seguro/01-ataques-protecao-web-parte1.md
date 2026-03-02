# Aula 1 – Ataques e Proteção Web – Parte 1

## 📌 Análise de URL
- **Esquema (Scheme)** → http, https, ftp, mailto
- **Domínio (Host)** → endereço do servidor
- **Porta (Port)** → número da porta (ex: 8080)
- **Caminho (Path)** → local do recurso no servidor
- **Query String** → parâmetros (ex: ?id=123&nome=joao)
- **Âncora (Fragment)** → posição na página (#secao2)

## 📌 Identificação de URLs maliciosas
- Verificar domínio (typosquatting: exemp1o.com)
- Exigir HTTPS
- Examinar estrutura (URLs longas/complexas são suspeitas)
- Evitar URLs encurtadas
- Usar antivírus/anti-malware
- Verificar reputação de domínio

## 📌 HTTP Percent Encoding (URL encoding)
- Substitui caracteres especiais por % + hexadecimal
- Espaço → %20
- / → %2F
- & → %26
- Ajuda a evitar ataques (XSS, SQL injection)

## 📌 API Attacks
- **Injeção de SQL** em APIs
- **Força bruta** (tentar adivinhar senhas/tokens)
- **XSS** (scripts maliciosos)
- **Ataques de dicionário** (tentar palavras comuns)

### Autenticação em APIs
- Baseada em token (JWT)
- Credenciais (usuário/senha)
- API Key
- Certificado digital

### Autorização em APIs
- **RBAC** → por função
- **ABAC** → por atributos (hora, local, dispositivo)
- **OAuth/OAuth2** → autorização de terceiros

### Boas práticas para APIs
- Validar entrada
- Limite de taxa (rate limiting)
- Controle de acesso
- Monitoramento e registro
- Atualização regular
- Autenticação forte (OAuth 2.0)

## 📌 Replay Attacks
- Invasor intercepta e retransmite dados válidos
- **Mitigação:**
  - Tokens únicos (usar uma vez só)
  - Carimbo de data/hora
  - Controle de sessão robusto
  - Criptografia
  - Autenticação Multifator (MFA)
  - Expiração de sessão

## 📌 Session Hijacking (Sequestro de Sessão)
- Invasor assume controle da sessão do usuário
- **Técnicas:**
  - Capturar cookies de sessão
  - Predizer ID de sessão
  - Man-in-the-Middle (MitM)
  - Session Fixation
- **Proteção:**
  - Criptografia
  - MFA
  - IDs de sessão aleatórios
  - Tempo de expiração
  - Cookies seguros (Secure, HttpOnly, SameSite)

## 📌 Cross-Site Request Forgery (CSRF)
- Usuário autenticado executa ação sem querer
- **Prevenção:**
  - Token Anti-CSRF
  - SameSite cookies
  - Verificar cabeçalho Origin
  - Confirmar ações críticas

## 📌 Clickjacking
- Elemento oculto sobre página legítima
- Usuário clica sem saber em ação maliciosa
- **Prevenção:**
  - X-Frame-Options (DENY, SAMEORIGIN)
  - Frame-busting JavaScript
  - Content Security Policy (CSP)

## 📌 SSL Strip
- Remove criptografia SSL/TLS
- Intercepta e descriptografa tráfego
- **Prevenção:**
  - HTTPS estrito (redirecionar HTTP → HTTPS)
  - HSTS (HTTP Strict Transport Security)
  - Validar certificados
  - Evitar Wi-Fi público sem VPN

---

## 💡 Meus insights
- A query string é onde muita coisa acontece. Parâmetros maliciosos podem vir por ali.
- "paypa1.com" engana muita gente. Verificar domínio é essencial.
- Percent encoding é útil mas também usado pra esconder URL maliciosa. "%20" pode ser só espaço ou parte de ataque.
- API é porta de entrada pra tudo hoje. Se não proteger, é game over.
- Rate limiting é simples mas eficaz. Impede que bot faça 1 milhão de tentativas de senha.
- Token de uso único é a chave contra replay attacks. Se o token expira depois de usado, replay não funciona.
- Cookie com Secure e HttpOnly é obrigatório. Sem isso, JavaScript malicioso rouba a sessão.
- Token anti-CSRF é trabalhoso mas necessário. Imagina usuário logado transferir dinheiro sem querer.
- X-Frame-Options: DENY em páginas críticas. Não quero meu site dentro de iframe de terceiros.
- HSTS resolve SSL Strip. Navegador "aprende" que site só aceita HTTPS, mesmo se usuário digitar http://
- Muitos ataques exploram a confiança. O navegador confia no cookie, o site confia no usuário autenticado. Validar tudo é o caminho.