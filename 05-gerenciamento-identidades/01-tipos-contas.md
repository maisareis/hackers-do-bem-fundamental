# Aula 1 – Tipos de Contas e Identidades

## 📌 Controles de gerenciamento de identidade
- **Identidade digital** → representada por uma conta em uma rede
- **Certificados digitais** → emitidos por uma Autoridade Certificadora (CA), contém chave pública do usuário
- **Smart Cards** → armazenam chave privada e certificado, permitem autenticação em diferentes dispositivos
- **Tokens** → prova de autenticação após login único (SSO), evita ter que logar toda hora

## 📌 Provedores de identidade (IdP)
- Serviços que fornecem contas e processam autenticação
- Podem ser locais (Active Directory) ou em nuvem (Google, Microsoft)
- **Federação** → usar uma identidade em vários sites/serviços

## 📌 Verificação de antecedentes e integração
- **Onboarding** → criar conta, atribuir permissões, entregar credenciais com segurança
- **NDA (Acordo de Confidencialidade)** → funcionário assina se comprometendo a não compartilhar info sigilosa

## 📌 Políticas de pessoal para privilégios
- **Separação de funções** → dividir tarefas críticas entre pessoas diferentes
- **Menor privilégio** → só dar acesso necessário pro trabalho
- **Rotação de cargos** → evitar dependência de uma única pessoa, compartilhar conhecimento
- **Licença obrigatória** → funcionário precisa tirar férias, período onde auditoria pode detectar fraudes

## 📌 Offboarding (saída do funcionário)
- Desativar contas e permissões
- Recuperar ativos da empresa (notebook, celular, crachá)
- Limpar dados corporativos de dispositivos pessoais
- Trocar senhas de contas compartilhadas

## 📌 Tipos de contas
- **Contas de convidado** → acesso temporário e limitado
- **Contas de administrador/root** → privilégios totais (CUIDADO!)
- **Contas de serviço** → system, local service, network service (Windows)
- **Contas compartilhadas/genéricas** → usadas por múltiplas pessoas (risco!)
- **Chaves SSH** → autenticação segura sem senha, par de chaves pública/privada

---

## 💡 Meus insights
- **Certificados digitais:** É tipo um RG virtual. A CA é quem emite e garante que é você.
- **Smart Cards:** Gostei da ideia de carregar a identidade no bolso e usar em qualquer computador.
- **Tokens SSO:** Aqueles "logar com Google" é federação! Não preciso criar conta nova em cada site.
- **Separação de funções:** Uma pessoa não pode autorizar o próprio pagamento. Óbvio, mas em sistema tem que ser configurado.
- **Menor privilégio:** Se a conta for hackeada, o estrago é limitado. Faz todo sentido.
- **Rotação de cargos:** Além de segurança, ajuda a equipe a não ficar refém de uma pessoa que sabe tudo.
- **Licença obrigatória:** Espertinho! Enquanto o funcionário tá de férias, dá pra ver se ele tava fazendo coisa errada.
- **Offboarding:** Imagina esquecer de desativar a conta e o ex-funcionário continuar acessando tudo. Pesadelo!
- **Contas compartilhadas:** Se alguém faz caquinha, não tem como saber quem foi. Evitar ao máximo.
- **Chaves SSH:** Muito mais seguro que senha, mas tem que proteger a chave privada como um tesouro.
