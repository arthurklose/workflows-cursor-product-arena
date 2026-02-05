# Mentoria Session Workflow

Processa e organiza anotações de sessões de mentoria, mantendo histórico por mentorado e consolidando perguntas por mês.

## Por que usar?

- Estrutura consistente para todas as sessões
- Histórico completo de cada mentorado
- Consolidado de perguntas revela padrões e temas recorrentes
- Base para criar conteúdo (posts, artigos, cursos)

## Como funciona

```
/mentoria João Silva

[Cola notas manuais]
[Cola anotações do Gemini/transcrição automática]
[Cola transcrição completa]
```

O sistema:
1. Identifica o arquivo do mentorado
2. Extrai perguntas de todas as fontes
3. Estrutura a sessão no arquivo do mentorado
4. Atualiza o consolidado de perguntas do mês

## Setup

1. Copie `PROMPT.md` para seu arquivo de instruções
2. Crie a pasta `Knowledge/mentorship/`
3. Crie o arquivo de perguntas consolidadas usando o template
4. Para cada mentorado, crie um arquivo usando `template-mentee.md`

## Estrutura de arquivos

```
Knowledge/
├── mentorship/
│   ├── João Silva - PM Senior.md
│   ├── Maria Santos - Head of Product.md
│   └── ...
└── mentorship-questions-by-month.md
```

## Inputs esperados

1. **Notas manuais**: Estruturadas com Updates/Perguntas/Takes/Para-casa
2. **Anotações automáticas**: Do Gemini, Otter, ou similar
3. **Transcrição**: Completa da conversa

O sistema cruza as três fontes para não perder nenhuma pergunta.

## Output

### Arquivo do mentorado
```markdown
## 📅 15/01/2026

### Updates
[O que o mentorado compartilhou]

### Perguntas
- Como priorizar quando tudo é urgente?
- Devo aceitar a proposta de promoção?

### Takes
[Seus insights e recomendações]

### Para-casa
- [ ] Fazer exercício de priorização
- [ ] Conversar com gestor sobre expectativas
```

### Consolidado de perguntas
```markdown
## 📅 JANEIRO 2026
**5 sessões | 12 perguntas**

- Como priorizar quando tudo é urgente? - **João Silva**
- Devo aceitar a proposta de promoção? - **Maria Santos**
```

## Dicas

- Mantenha as notas manuais simples — o sistema organiza depois
- O consolidado de perguntas é ouro para criar conteúdo
- Revise mensalmente as perguntas para identificar padrões
