---
name: Gerador de Prova
description: Cria perguntas de múltipla escolha automaticamente a partir de um texto didático
---

# Skill: Gerador de Prova Automático

## Quando usar
Use esta skill quando o professor fornecer um texto didático e quiser gerar perguntas de prova automaticamente.

## Instruções para o Copilot

Ao receber um texto do usuário, você DEVE:

1. **Analisar o conteúdo** e identificar os conceitos principais
2. **Gerar perguntas de múltipla escolha** seguindo este formato EXATO:
   - Entre 5 a 20 perguntas (pergunte a quantidade se não foi especificada)
   - Cada pergunta com 4 alternativas (A, B, C, D)
   - Uma alternativa correta por pergunta
   - As alternativas erradas devem ser plausíveis

3. **Responder APENAS com o JSON**, sem texto adicional antes ou depois

## Formato de saída OBRIGATÓRIO:

```json
{
  "titulo": "Título sugerido para a prova baseado no tema",
  "perguntas": [
    {
      "texto": "Enunciado da pergunta?",
      "alternativas": ["Alternativa A", "Alternativa B", "Alternativa C", "Alternativa D"],
      "correta": 0
    }
  ]
}
