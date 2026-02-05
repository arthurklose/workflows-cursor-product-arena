# Reunião B2B - Instruções para o LLM

Adicione ao seu CLAUDE.md ou system prompt:

---

## /reuniao [nome-do-cliente]

Processa anotações de reunião com cliente B2B.

**Inputs esperados** (usuário informa após o comando):
- Cliente/SubCliente
- Participantes (opcional)
- Notas da reunião (formato livre ou estruturado)
- Transcrição (opcional)

**Ao receber `/reuniao [cliente]`:**

### Passo 1: Identificar o cliente
- Extrair nome do comando
- Verificar se existe pasta em `Knowledge/clients/[Cliente]/`
- Se houver múltiplas áreas/subclientes, perguntar qual
- Se não existir, criar estrutura

### Passo 2: Processar as notas
- Usar notas do usuário como base
- Se houver transcrição, buscar:
  - Perguntas não capturadas
  - Decisões implícitas
  - Dores/necessidades mencionadas
  - Oportunidades de expansão

### Passo 3: Estruturar sessão
```markdown
## 📅 [DD/MM/YYYY]
**Participantes:** [Se mencionado]

### Updates
[Novidades do cliente - projetos, mudanças, resultados]

### Perguntas
- [Pergunta/dúvida do cliente]

### Decisões
- [Decisão tomada na reunião]

### Próximos Passos
**Cliente:**
- [ ] [Ação do cliente]

**Nós:**
- [ ] [Nossa ação]

---
```

### Passo 4: Atualizar arquivo do cliente
- Se primeiro registro, criar arquivo com header:
```markdown
# [SubCliente/Área]
**Cliente:** [Cliente Principal]
**Contato principal:** [Se conhecido]
**Início:** [Data aproximada]

## Contexto
[Breve descrição]

## Histórico de Reuniões
```
- Inserir sessão no topo do histórico

### Passo 5: Atualizar consolidado de insights
Ler `Knowledge/clients/clients-insights.md` e atualizar:

1. **Perguntas Frequentes**: `- [Pergunta] - **[Cliente]** (MM/YYYY)`
2. **Padrões de Dor**: Identificar e agrupar dores
3. **Oportunidades**: `- [Oportunidade] - **[Cliente]** - [Status]`
4. **Feedback**: Positivo e negativo sobre produto/serviço

**Output para o usuário:**
1. Qual cliente/subcliente foi atualizado
2. Quantas perguntas/decisões/próximos passos
3. Insights adicionados ao consolidado
4. Alertas de oportunidades identificadas

---

## Exemplo

**Usuário:**
```
/reuniao Ambev

Subcliente: Marketing
Participantes: Ana (Gerente), Carlos (Analista)

Updates: Campanha de verão superou meta em 20%
Perguntas: Como escalar o processo de briefing?
Decisões: Vamos fazer POC de automação
Próximos: Eles mapeiam processo atual, eu trago opções de ferramentas
```

**Assistente:**
Reunião processada:
- Cliente: Ambev / Marketing
- 1 pergunta, 1 decisão, 2 próximos passos registrados
- Oportunidade adicionada: POC de automação
- Arquivos atualizados: `Ambev/Marketing.md`, `clients-insights.md`
