# Aula 2 – Ataques e Proteção Web – Parte 2

## 📌 Cross-Site Scripting (XSS)
- Injeção de scripts maliciosos em páginas web

### Tipos de XSS
- **Refletido (Reflected)** → código no link, vítima clica, servidor "reflete" de volta
- **Armazenado (Stored)** → código salvo no servidor (comentários, perfil), todo mundo que acessar executa
- **DOM-based** → manipula o DOM da página, não passa pelo servidor

### Prevenção
- Validar entrada (filtragem estrita)
- Escape de saída (converter < > em &lt; &gt;)
- Content Security Policy (CSP)
- Sanitização de dados (bibliotecas como DOMPurify)
- Headers HTTP seguros (X-XSS-Protection)
- Validar origem das solicitações
- Frameworks seguros (sanitização automática)

## 📌 SQL Injection
- Inserir instruções SQL maliciosas em campos de entrada

### Como acontece
1. Identificar campo vulnerável
2. Inserir SQL malicioso (ex: ' OR 1=1 --)
3. Aplicativo executa no banco
4. Explorar resultado (acessar, modificar, excluir)

### Prevenção
- Validar entrada
- **Consultas parametrizadas** (placeholders, separa comando SQL dos dados)
- Evitar concatenação manual de SQL
- Menor privilégio no banco
- Monitoramento e auditoria

## 📌 XML Injection
- Inserir dados maliciosos em documentos XML

### Prevenção
- Validar entrada (esquemas XML)
- Filtrar caracteres especiais (<, >, &, ', ")
- Evitar concatenação direta
- Bibliotecas seguras
- Limitar privilégios

## 📌 LDAP Injection
- Manipular consultas LDAP para acessar/modificar/excluir diretórios

### Prevenção
- Consultas LDAP parametrizadas
- Filtros de pesquisa seguros
- Validar entrada
- Escape de caracteres especiais ((, ), *, \, NULL)
- Menor privilégio

## 📌 Directory Traversal (Path Traversal)
- Acessar arquivos/diretórios fora da área permitida (ex: ../../../etc/passwd)

### Prevenção
- Validar caminhos de arquivo
- Usar caminhos relativos
- Restrições de acesso
- Sanitizar caminhos (remover ../)
- Whitelist de caminhos permitidos

## 📌 Command Injection
- Executar comandos maliciosos no sistema operacional via aplicativo

### Como acontece
1. Campo de entrada usado em comando do sistema
2. Invasor injeta comando (ex: ; rm -rf /)
3. Sistema executa

### Prevenção
- Validar entrada (só alfanumérico quando possível)
- Usar funções seguras (ex: subprocess no Python com lista de args)
- Sanitizar dados
- Restrições de privilégios
- Evitar entrada livre (usar dropdowns quando possível)

## 📌 Server-Side Request Forgery (SSRF)
- Servidor faz requisições não autorizadas para recursos internos/externos

### Como acontece
1. Campo que aceita URL
2. Invasor coloca URL interna (ex: http://localhost/admin)
3. Servidor faz requisição e retorna resultado

### Prevenção
- Validar URLs (whitelist de domínios)
- Restringir saída de rede (firewall)
- Usar URLs relativas
- Monitorar logs

---

## 💡 Meus insights
- O XSS "armazenado" é o mais perigoso. Um comentário com script malicioso afeta todo mundo que visitar a página.
- CSP é política de segurança de conteúdo foda. Diz pro navegador "só aceita script desse domínio aqui".
- Consultas parametrizadas resolvem 90% do SQL Injection. O resto é validar entrada.
- Em vez de "SELECT * FROM users WHERE name = '"+nome+"'", usar "SELECT * FROM users WHERE name = ?" e passar o valor separado.
- XML Injection parece coisa antiga, mas sistemas legados ainda usam XML pra tudo.
- LDAP Injection: diretório corporativo é um alvo valioso. Imaginem vazar todos os usuários e permissões.
- Directory Traversal: ../etc/passwd é clássico. Sistemas mal configurados entregam arquivos sensíveis assim.
- Command Injection é o pior pesadelo. Se o aplicativo executa comando no sistema, invasor pode fazer QUALQUER coisa.
- SSRF é muito usado em ataques a nuvem. Servidor consegue acessar metadados internos do provedor.
- Exemplo real de SSRF no AWS: Se servidor acessar http://169.254.169.254/latest/meta-data/, pega credenciais da instância.
- Whitelist de domínios: se só pode acessar img.youtube.com e i.imgur.com, bloqueia o resto.
- Resumo: valide entrada, parametrize consultas, escape saída, menos privilégio. Esses 4 resolvem 95% dos problemas.