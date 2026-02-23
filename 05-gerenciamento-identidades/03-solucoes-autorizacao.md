# Aula 3 – Soluções de Autorização

## 📌 Modelos de controle de acesso

### DAC (Discretionary Access Control)
- Proprietário do recurso decide quem acessa
- Permissões: read (r), write (w), execute (x)
- Lista de Controle de Acesso (ACL) associada a cada recurso
- **Exemplo:** Você cria um arquivo e decide quem pode ver

### RBAC (Role-Based Access Control)
- Acesso baseado em função/cargo
- Usuários herdam permissões da função
- **Exemplo:** "Gerente" pode aprovar compras, "Analista" só pode ver

### MAC (Mandatory Access Control)
- Políticas definidas pelo sistema, não pelo usuário
- Rótulos de segurança (Confidencial, Restrito, Público)
- **Exemplo:** Sistema militar, só quem tem o selo "Confidencial" acessa docs confidenciais

### ABAC (Attribute-Based Access Control)
- Acesso baseado em atributos (usuário, recurso, contexto)
- **Exemplo:** "Liberar acesso se usuário é gerente, documento é financeiro, horário comercial"

## 📌 Permissões em sistemas de arquivos (Linux/Unix)
- **r (read)** → ler arquivo/listar diretório
- **w (write)** → modificar/criar arquivos
- **x (execute)** → executar programa/acessar diretório
- **chmod** → modificar permissões
- **chown** → alterar proprietário

## 📌 PAM (Privileged Access Management)
- Gerencia contas privilegiadas (admin, root)
- Rotação automática de senhas
- Monitoramento de sessões privilegiadas
- Aprovação para acessos críticos

## 📌 Serviços de diretório
- **LDAP (Lightweight Directory Access Protocol)** → protocolo para acessar diretórios
- **X.500** → padrão de diretórios hierárquicos
- **DN (Distinguished Name)** → identificação única no diretório (ex: CN=João, OU=Vendas, O=Empresa, C=BR)

### Atributos comuns
- **CN (Common Name)** → nome comum
- **OU (Organizational Unit)** → unidade organizacional (departamento)
- **O (Organization)** → organização
- **C (Country)** → país
- **DC (Domain Component)** → componente de domínio (ex: dc=empresa, dc=com)

## 📌 Federação e protocolos
- **Federação** → compartilhar autenticação entre organizações
- **SAML (Security Assertions Markup Language)** → XML para trocar info de autenticação
- **SOAP** → protocolo para comunicação entre aplicações
- **OAuth 2.0** → autorização para aplicativos acessarem recursos em nome do usuário
- **OpenID Connect (OIDC)** → autenticação baseada em OAuth 2.0, adiciona token de identidade

---

## 💡 Meus insights
- **DAC vs RBAC vs MAC vs ABAC:**
  - DAC: "meu arquivo, minhas regras"
  - RBAC: "gerente pode, analista não"
  - MAC: "sistema decide, você obedece"
  - ABAC: "se horário comercial E local escritório E cargo gerente, libera"
- **Permissões Linux:** r (ler), w (escrever), x (executar). chmod e chown são essenciais.
- **PAM:** Contas de admin são as mais visadas. Rotacionar senha automaticamente é genial.
- **LDAP:** É tipo catálogo telefônico da empresa. Onde ficam todos os usuários e suas info.
- **DN:** CN=João, OU=Vendas, O=Empresa, C=BR. Lê de trás pra frente: Brasil, Empresa, Vendas, João.
- **Federação:** Logar com Google ou Facebook é federação! Uma conta serve pra vários sites.
- **SAML vs OAuth vs OIDC:**
  - SAML: XML, mais corporativo
  - OAuth: foco em autorização (app acessar seus dados)
  - OIDC: autenticação + autorização, mais usado em apps modernos
- **SOAP:** Parece coisa antiga, XML pesado. Hoje usam mais REST.
- **Dúvida:** ABAC parece poderoso, mas deve ser complexo de configurar. Quando vale a pena?
- **Insight:** Entender esses modelos ajuda a projetar acesso do zero. Cada cenário pede um modelo diferente.