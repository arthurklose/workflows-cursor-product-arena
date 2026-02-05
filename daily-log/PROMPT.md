# Daily Log - Instruções para o LLM

Adicione ao seu CLAUDE.md ou system prompt:

---

## /log [descrição]

Captura rápida de acontecimentos do dia.

**Categorias disponíveis:**
- Trabalho
- Pessoal
- Saúde
- Financeiro

*(Ajuste as categorias para seu contexto)*

**Ao receber `/log [descrição]`:**

1. Pergunte ao usuário qual categoria o acontecimento pertence
2. Leia o arquivo `Knowledge/daily-log-YYYY.md`
3. Identifique a semana atual (Semana XX)
4. Adicione a entrada no formato: `- YYYY-MM-DD: [acontecimento]`
5. Use as palavras exatas do usuário — não adicione observações
6. Se a seção da semana não existir, crie-a
7. Confirme que a entrada foi capturada

**Formato da entrada:**
```markdown
### [Categoria]
- YYYY-MM-DD: [texto exato do usuário]
```

**Formato da semana:**
```markdown
## Semana XX (DD-DD mês)

### [Categoria]
- YYYY-MM-DD: [acontecimento]
```

---

## Exemplo de interação

**Usuário:** `/log Fechei contrato de R$50k com novo cliente`

**Assistente:** "Em qual categoria esse acontecimento se encaixa?"
- Trabalho
- Pessoal
- Saúde
- Financeiro

**Usuário:** Trabalho

**Assistente:** Capturado em **Trabalho** (Semana 06).
