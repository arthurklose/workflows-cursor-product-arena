# Reunião com Cliente B2B Workflow

Processa e organiza anotações de reuniões com clientes B2B, mantendo histórico por cliente e consolidando insights.

## Por que usar?

- Histórico completo de cada cliente/projeto
- Padrões de dor e oportunidades ficam visíveis
- Próximos passos nunca se perdem
- Base para identificar upsell e expansão

## Como funciona

```
/reuniao Itaú

Subcliente: Área de Dados
Participantes: João (PO), Maria (Tech Lead)

Updates: Lançaram dashboard semana passada, 500 usuários no dia 1
Perguntas: Como medir impacto? Como priorizar backlog?
Decisões: Workshop de priorização na próxima semana
Próximos passos: Eles levantam iniciativas, eu preparo material
```

O sistema:
1. Identifica ou cria arquivo do cliente/subcliente
2. Estrutura a sessão com todas as informações
3. Atualiza o consolidado de insights

## Setup

1. Copie `PROMPT.md` para seu arquivo de instruções
2. Crie a estrutura de pastas `Knowledge/clients/`
3. Crie o arquivo de insights consolidados usando o template

## Estrutura de arquivos

```
Knowledge/
└── clients/
    ├── Itaú/
    │   ├── _overview.md
    │   └── Área de Dados.md
    ├── Ambev/
    │   ├── _overview.md
    │   └── Marketing.md
    └── clients-insights.md
```

## Output

### Arquivo do cliente
```markdown
## 📅 15/01/2026
**Participantes:** João (PO), Maria (Tech Lead)

### Updates
Lançaram dashboard semana passada, 500 usuários no dia 1

### Perguntas
- Como medir impacto?
- Como priorizar backlog?

### Decisões
- Workshop de priorização confirmado

### Próximos Passos
**Cliente:**
- [ ] Levantar lista de iniciativas

**Nós:**
- [ ] Preparar material do workshop
```

### Consolidado de insights
```markdown
## Perguntas Frequentes
- Como medir impacto? - **Itaú** (01/2026)

## Padrões de Dor
- Times sem framework de priorização

## Oportunidades
- Workshop de priorização - **Itaú** - Em andamento
```

## Dicas

- Capture participantes — útil para relacionamento
- O consolidado revela padrões entre clientes
- Revise oportunidades semanalmente
- Use para preparar propostas de expansão
