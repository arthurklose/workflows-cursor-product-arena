# Mentoria Session - Instruções para o LLM

Adicione ao seu CLAUDE.md ou system prompt:

---

## /mentoria [nome-do-mentorado]

Processa anotações de uma sessão de mentoria.

**Inputs esperados** (usuário cola após o comando):
1. Notas manuais (Updates/Perguntas/Takes/Para-casa)
2. Anotações automáticas (Gemini, Otter, etc.)
3. Transcrição completa

**Ao receber `/mentoria [nome]`:**

### Passo 1: Identificar o mentorado
- Extrair nome do comando
- Encontrar arquivo em `Knowledge/mentorship/`
- Se não encontrar, listar opções ou perguntar

### Passo 2: Processar perguntas
- Usar notas manuais como base principal
- Vasculhar transcrição + anotações automáticas para perguntas adicionais
- Perguntas aparecem como:
  - Frases interrogativas
  - Dúvidas ("não sei como...", "qual a melhor forma...")
  - Dilemas ("devo fazer X ou Y?")

### Passo 3: Estruturar sessão
```markdown
## 📅 [DD/MM/YYYY]

### Updates
[Sintetizar atualizações do mentorado]

### Perguntas
- [Pergunta 1 sintetizada]
- [Pergunta 2 sintetizada]

### Takes
[Sintetizar insights e recomendações dadas]

### Para-casa
- [ ] [Ação combinada 1]
- [ ] [Ação combinada 2]

---
```

### Passo 4: Atualizar arquivo do mentorado
- Inserir sessão **no topo** (mais recentes primeiro)
- Manter histórico anterior intacto

### Passo 5: Atualizar consolidado de perguntas
- Ler `Knowledge/mentorship-questions-by-month.md`
- Adicionar perguntas no mês atual
- Formato: `- [Pergunta] - **[Nome]**`
- Atualizar contadores (sessões e perguntas do mês)

**Output para o usuário:**
1. Quantas perguntas encontradas (manuais + descobertas)
2. Confirmação de atualização do arquivo
3. Confirmação de atualização do consolidado

---

## Exemplo

**Usuário:**
```
/mentoria Maria Santos

Notas manuais:
Updates: Promovida para Head semana passada
Perguntas: Como montar meu time? Quanto delegar?
Takes: Comece com 1:1s para entender o time
Para-casa: Agendar 1:1s com todos

[Transcrição...]
```

**Assistente:**
Sessão processada:
- 3 perguntas encontradas (2 nas notas + 1 na transcrição)
- Atualizado: `Knowledge/mentorship/Maria Santos - Head of Product.md`
- Atualizado: `Knowledge/mentorship-questions-by-month.md` (Janeiro: 8 sessões, 15 perguntas)
