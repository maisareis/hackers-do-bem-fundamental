# Aula 2 – Políticas de Contas

## 📌 Atributos de contas
Informações associadas a cada conta:
- Nome, e-mail, departamento, cargo
- Nível de acesso, permissões
- Data de criação, último acesso

## 📌 Políticas de acesso (GPO no Windows)
- Configuram quem pode acessar o quê
- Podem ser aplicadas por site, domínio ou unidade organizacional (OU)

## 📌 Política de senhas
- **Comprimento mínimo** → quanto maior, melhor
- **Complexidade** → maiúsculas, minúsculas, números, símbolos
- **Alteração periódica** → trocar a cada X dias
- **Restrições de reutilização** → não permitir repetir senhas antigas
- **Bloqueio após tentativas falhas** → evita força bruta
- **Proibição de senhas comuns** → nada de "123456" ou "senha"

## 📌 Restrições de contas
- **Baseadas em localização** → acesso só de certos lugares
- **Geofencing** → cerca virtual, libera/bloqueia por área geográfica
- **Baseadas em horário** → acesso só em determinados períodos

## 📌 Auditoria de contas
- Revisar logs de login, acesso a recursos, alterações de permissão
- Identificar comportamentos suspeitos
- Investigação forense em caso de incidente

## 📌 Permissões de contas
- **Leitura (read)** → só ver
- **Gravação (write)** → criar e modificar
- **Execução (execute)** → rodar programas
- **Exclusão (delete)** → remover
- **Administração** → controle total

## 📌 Bloqueio e desabilitação
- **Bloqueio** → temporário, após várias tentativas de login falhas
- **Desabilitação** → permanente, quando funcionário sai ou conta não é mais necessária

---

## 💡 Meus insights
- **Atributos de conta:** Cada detalhe ajuda a controlar acesso. Saber o departamento já define quais recursos liberar.
- **GPO no Windows:** É mágico! Configura uma vez e aplica pra geral. Política de senha forte pra todo mundo de uma vez.
- **Política de senhas:** Equilíbrio difícil. Senha muito complexa o usuário anota no post-it (pior ainda).
- **Alteração periódica:** Tô vendo que tão mudando essa recomendação. Melhor senha longa e forte do que trocar toda hora e esquecer.
- **Bloqueio após tentativas:** Essencial contra força bruta. Se errar 5x, bloqueia por 30 minutos.
- **Geofencing:** Imagina, acesso só liberado se tiver no escritório. Se tentar de outro país, bloqueia na hora.
- **Restrição de horário:** Acesso só 8h-18h. Se alguém logar 3h da manhã, é suspeito.
- **Auditoria de contas:** Logs salvam! Sem registro, não tem como provar nada.
- **Permissões:** Dar execução só pra quem realmente precisa. Evita que usuário comum rode programa malicioso.
- **Bloqueio vs Desabilitação:** Bloqueio é "castigo" temporário, desabilitação é fim de linha.
- **Dúvida:** Como auditar milhões de eventos sem perder o que realmente importa? Deve ter ferramenta que correlaciona.