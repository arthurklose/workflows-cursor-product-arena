# Personal OS Workflows

Workflows para captura e organização de conhecimento usando Claude Code (ou qualquer LLM com acesso a arquivos).

Cada pasta é **self-contained** — você pode copiar apenas o workflow que precisa.

## Workflows Disponíveis

| Workflow | Descrição | Trigger |
|----------|-----------|---------|
| [daily-log](./daily-log/) | Captura rápida de acontecimentos do dia | `/log [descrição]` |
| [mentoria](./mentoria/) | Processar sessões de mentoria | `/mentoria [nome]` |
| [reuniao](./reuniao/) | Processar reuniões com clientes B2B | `/reuniao [cliente]` |

## Como Usar

1. **Copie a pasta** do workflow que você quer usar
2. **Leia o README.md** da pasta para entender o workflow
3. **Copie o PROMPT.md** para o seu arquivo de instruções (CLAUDE.md, system prompt, etc.)
4. **Use o template** para criar seus arquivos de dados

## Estrutura de Cada Workflow

```
workflow-name/
├── README.md           # Documentação e como usar
├── PROMPT.md           # Instruções para o LLM (copie para seu projeto)
└── template.md         # Template dos arquivos de dados
```

## Filosofia

- **Capture first, organize later**: Registre informações rapidamente, deixe o sistema organizar
- **Self-contained workflows**: Cada workflow funciona independentemente
- **Human-readable**: Todos os dados ficam em Markdown, sem lock-in
- **LLM-agnostic**: Funciona com Claude, GPT, ou qualquer modelo com acesso a arquivos

## Requisitos

- LLM com acesso a sistema de arquivos (Claude Code, Cursor, etc.)
- Estrutura de pastas conforme os templates

## Licença

MIT - Use, modifique e compartilhe livremente.
