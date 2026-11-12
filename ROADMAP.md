# Roadmap do portfólio

Este documento separa o que já pode ser examinado no código das próximas extrações públicas. Os nomes de repositórios abaixo são propostas; nenhum link de repositório inexistente é apresentado como entrega.

## Base publicada

| Componente | O que já existe | Evidência |
|---|---|---|
| Roteamento de LLMs | Fallback e registro de modelo e custo; exemplo de planejador, executor e revisor com contratos JSON | [llm-cascade](https://github.com/luandv92/llm-cascade) |
| Verificação de resultados | Monitoramento de arquivos, registros e comandos; exemplo com resultados aceitos | [outcome-watchdog](https://github.com/luandv92/outcome-watchdog) |
| Proteções no código | Regras de chamadas obrigatórias por AST | [wiringguard](https://github.com/luandv92/wiringguard) |
| Arquitetura de composição | Limites dos exemplos e decisões antes de escalar | [guia de agentes](https://github.com/luandv92/awesome-ai-content-ops/blob/master/docs/agent-workflows.md) |

## 1  agent-workflow-lab

**Status: planejado.** Protótipo de integração da rede de agentes.

**Problema:** demonstrações isoladas ainda não demonstram retomada, controle de orçamento ou entrega consistente de um fluxo completo.

**Escopo inicial:** tarefa de software bem delimitada, papéis de planejamento, execução e revisão, contrato de entrada/saída e registro persistente da execução. Reutilizar o roteador e o monitor existentes.

**Critérios para publicar como demonstrável:**

- Demo offline executável a partir de um checkout limpo.
- Identificador de execução e registro separado de tentativas e entregas aceitas.
- Orçamento e limite de tentativas definidos antes da execução.
- Testes de saída malformada, revisão negativa e interrupção seguida de retomada.
- Uma repetição da mesma execução não cria outra entrega aceita.
- README com arquitetura, comandos, limites e evidências dos testes.

## 2  agent-evaluation-kit

**Status: planejado.** Avaliação independente dos fluxos de agentes.

**Problema:** um modelo aprovar outro modelo não comprova a correção ou a utilidade da resposta.

**Escopo inicial:** conjunto pequeno de tarefas versionadas, resultados esperados, verificações determinísticas quando possíveis e critérios para revisão humana.

**Critérios para publicar como demonstrável:**

- Separação explícita entre fixtures offline e avaliação com provedores reais.
- Casos de acerto, erro, recusa e saída inválida.
- Registro de versão dos dados, configuração de modelo e custo reportado.
- Relatório reproduzível, com resultados por tarefa e limites da amostra.
- Nenhuma conclusão de superioridade de modelo baseada apenas em um exemplo favorável.

## 3  family-learning-lab

**Status: planejado para extração pública.** Componentes reutilizáveis da plataforma educativa Feira das Escolhas / Ludimapa.

**Ponto de partida:** [piloto web público](https://feira.storyteller-mari.com/?lang=pt-BR) de aprendizagem em evolução. A extração pública ainda precisa ser preparada e validada; este roadmap não apresenta uma biblioteca pronta nem comprovação de eficácia educacional.

**Escopo inicial:** uma missão educativa independente, suporte a idiomas e persistência local de progresso, acompanhados de critérios de acessibilidade e privacidade.

**Critérios para publicar como demonstrável:**

- Exemplo executável com conteúdo de demonstração e instruções de instalação.
- Objetivo de aprendizagem, interação e feedback documentados.
- Nenhum dado real de criança, credencial ou conteúdo privado no repositório.
- Navegação por teclado e revisão de legibilidade em telas pequenas.
- Testes de troca de idioma e persistência local.
- Licença e origem dos conteúdos e ativos verificadas.
- Resultados de testes técnicos separados de qualquer alegação de resultado educacional.

## Ordem de execução

Começar pelo fluxo integrado de agentes, depois acrescentar avaliação independente. A extração educativa pode avançar quando o componente e sua licença estiverem definidos. Cada frente deve ganhar um repositório quando houver um exemplo útil para outra pessoa executar, e não apenas para ocupar um nome no portfólio.

Sem datas de lançamento prometidas. A promoção de **planejado** para **demonstrável** depende dos critérios acima; uso em produção e resultados com usuários exigem evidências adicionais.
