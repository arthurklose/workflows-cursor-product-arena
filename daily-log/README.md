# Daily Log Workflow

Captura rápida de acontecimentos do dia — fechamentos, reuniões, marcos, feedbacks, aprendizados.

## Por que usar?

- Registro acontece no momento, não no fim da semana
- Organização automática por categoria e semana
- Base para gerar weekly wins e retrospectivas

## Como funciona

```
/log após lançar a feature XXXX, aumentamos xx% o engajamento
```

O sistema:
1. Pergunta a categoria
2. Adiciona entrada no arquivo de log com timestamp
3. Organiza na semana correta

## Setup

1. Copie `PROMPT.md` para seu arquivo de instruções (CLAUDE.md ou similar)
2. Crie o arquivo de log usando `template.md` como base
3. Ajuste as categorias no PROMPT.md para seu contexto

## Categorias (exemplo)

- **Trabalho**: Projetos, entregas, reuniões
- **Pessoal**: Família, relacionamentos
- **Saúde**: Exercícios, consultas, hábitos
- **Financeiro**: Investimentos, receitas, despesas

## Estrutura do arquivo de log

```markdown
## Semana XX (DD-DD mês)

### [Categoria]
- YYYY-MM-DD: [acontecimento]
- YYYY-MM-DD: [acontecimento]

### [Outra Categoria]
- YYYY-MM-DD: [acontecimento]
```

## Dicas

- Capture no momento — não espere o fim do dia
- Seja específico: "Fechei uma parceria de R$xxx.xxx com empresa XXXX" > "Fechei contrato"
- Use `/log` várias vezes ao dia se necessário
- Combine com workflow de weekly-wins para gerar resumos
