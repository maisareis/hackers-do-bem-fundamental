# Aula 3 – Codificação Segura e Automação

## 📌 Princípios de Codificação Segura
- **Menor privilégio** → só o necessário pra funcionar
- **Defesa em profundidade** → várias camadas de segurança
- **Autenticação e autorização** → confirmar identidade e controlar acesso

## 📌 Validação de Entrada e Codificação de Saída
- Validar todo dado de entrada (evitar injeção)
- Normalizar e codificar saída (evitar XSS)

## 📌 Cookies Seguros e Cabeçalhos de Resposta
- **Secure** → cookie só via HTTPS
- **HttpOnly** → JavaScript não acessa cookie (protege contra XSS)
- **SameSite** → controla envio entre sites

## 📌 Melhores Práticas
- Usar HTTPS sempre
- Autenticação forte (MFA)
- Controle de acesso rigoroso
- Gerenciamento de sessão seguro

## 📌 Reuso de Código
- Avaliar bibliotecas de terceiros (segurança, comunidade ativa)
- Auditar código-fonte
- Versionamento controlado
- SDKs: mínimo privilégio, atualizações regulares

## 📌 Stored Procedures
- Rotinas no banco de dados
- Validam entrada, controlam acesso
- Previnem SQL Injection
- Podem prevenir negação de serviço (limites de tempo/recurso)

## 📌 Ferramentas de Verificação
- **Análise estática** → examina código fonte (encontra SQLi, XSS)
- **Análise dinâmica** → testa em execução
- **Scanners de vulnerabilidade** → componentes de terceiros

## 📌 Código Inacessível e Código Morto
- Código inacessível: controle de acesso impede uso não autorizado
- Código morto: partes não usadas, devem ser removidas (reduz superfície de ataque)

## 📌 Ofuscação e Camuflagem
- **Ofuscação** → dificulta engenharia reversa
- **Camuflagem** → proteger info sensível (chaves, senhas)

## 📌 Criptografia e Hashing
- **Criptografia** → proteger dados em trânsito/repouso
- **Hashing** → integridade, senhas com salt (evitar rainbow tables)

## 📌 Automação com Scripting

### Python
- Backup de arquivos, manipulação de dados, extração de logs

```python
import shutil

origem = '/caminho/para/a/pasta/origem'
destino = '/caminho/para/a/pasta/destino'

shutil.copytree(origem, destino)
```

### PowerShell
- Gerenciamento de usuários, instalação em massa, coleta de informações

```powershell
$processos = Get-Process
foreach ($processo in $processos) {
    Write-Host "Nome do processo: $($processo.Name), ID do processo: $($processo.Id)"
}
```

### Vantagens da Automação
- Eficiência
- Escalabilidade
- Padronização
- Monitoramento e reação em tempo real
- Redução de erros humanos

## 📌 Controle de Execução
- Garantir que apenas programas e processos autorizados sejam executados

### Técnicas
- **Lista de Permissões (Whitelisting)** → só programas autorizados
- **Lista de Bloqueios (Blacklisting)** → bloquear conhecidos (menos seguro)
- **Assinatura de código** → verificar autenticidade e integridade
- **Políticas do Sistema Operacional** → controle de acesso
- **Máquinas virtuais e contêineres** → isolar execução

### Práticas Seguras
- Atualização regular de software
- Uso de antivírus e antimalware
- Restrições de conta de usuário
- Políticas de Grupo (Group Policies)
- Monitoramento de integridade de arquivos

---

## 💡 Meus insights
- Menor privilégio: se a conta for comprometida, o estrago é mínimo. Faz todo sentido.
- HttpOnly é essencial contra XSS. Se cookie não é acessível por JS, roubo de sessão fica mais difícil.
- Reuso de código: usar biblioteca pronta é bom, mas tem que confiar. Auditoria é importante.
- Stored procedures: banco faz a validação, não só o app. Camada extra de segurança.
- Análise estática: ferramentas como SonarQube acham boas vulnerabilidades antes de ir pra produção.
- Código morto: todo sistema legado tem. Revisar e limpar reduz risco.
- Ofuscação não é segurança de verdade, mas dificulta. Como colocar placa falsa em carro de fuga.
- Hashing com salt: mesma senha gera hash diferente. Rainbow table não adianta.
- Python vs PowerShell: Python mais universal, PowerShell manda no Windows. Saber os dois é diferencial.
- Automação: tarefa repetitiva é candidata a automação. Backup todo dia às 2h? Script resolve.
- Whitelisting é mais seguro mas dá trabalho. Blacklisting é reativo, sempre atrás do malware novo.
- Assinatura de código: se o executável foi modificado, assinatura quebra. Dá pra confiar.
- Controle de execução + autenticação + criptografia = defesa em profundidade.