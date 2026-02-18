# Aula 4 – Autenticação por Biometria

## 📌 O que é?
Biometria usa características físicas ou comportamentais únicas para identificar alguém.

## 📌 Métricas de avaliação
- **FAR** → taxa de falsa aceitação (aceita alguém que não deveria)
- **FRR** → taxa de falsa rejeição (nega acesso a quem deveria ter)
- **CER/EER** → ponto de equilíbrio entre FAR e FRR. Quanto menor, melhor o sistema.

## 📌 Tipos

### 🖐️ Impressão digital
- Muito usado em smartphones e controle de acesso
- Sensor captura as cristas do dedo e cria um modelo matemático
- Vulnerável a moldes falsos

### 😊 Reconhecimento facial
- Analisa proporções do rosto, distância entre olhos, formato do nariz...
- Usado em smartphones, controle de acesso e vigilância
- Taxa de erro um pouco maior, pode ser enganado por fotos

### ⌨️ Biometria comportamental
- Analisa o jeito que você digita, usa o mouse, segura o celular...
- Usada para autenticação contínua (verifica durante o uso, não só no login)
- Útil para detectar quando outra pessoa assumiu o dispositivo

---

## 💡 Meus insights
- **O que é:** Usar características físicas ou comportamentais únicas pra identificar alguém.

- **Métricas importantes:**
  - **FAR (False Acceptance Rate):** Aceitar quem não deveria. É o PIOR erro!
  - **FRR (False Rejection Rate):** Negar acesso a quem deveria ter. Frustrante mas menos grave.
  - **CER/EER:** Ponto de equilíbrio entre FAR e FRR. Quanto menor, melhor o sistema.
  - **Aprendizado:** 
  - Biometria é prática mas não é infalível. Por isso MFA é tão importante.

- **Tipos de biometria:**

  - 🖐️ **Impressão digital:** A mais comum. Rápida, barata. Dá pra enganar com molde de silicone?
  
  - 😊 **Facial:** Usa proporções do rosto, distância entre olhos, formato do nariz. Câmeras 3D dificultam enganar com foto.
  
  - 👁️ **Íris:** Muito precisa, difícil de falsificar. Usada em lugares de alta segurança.
  
  - 🗣️ **Voz:** Analisa tom, cadência. Dá pra enganar com gravação?
  
  - ⌨️ **Comportamental:** Jeito de digitar, mexer o mouse. Autenticação contínua (fica verificando durante o uso).

- **Na prática:** 
  - Celular já usa facial e digital. É rápido e prático.
  - Lugares que exigem segurança alta (bancos, data center) usam íris ou veia da palma.

- **Como Purple Team:** 
  - Testar se a biometria pode ser enganada (spoofing).
  - Ver se o sistema tem fallback quando a biometria falha.
