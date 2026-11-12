# Luan Ribeiro de Brito

**Engenharia de IA aplicada · Python · Automações confiáveis**

Sou graduando em **Engenharia da Computação na Universidade Cruzeiro do Sul**, com conclusão prevista em **janeiro de 2029**, e mestre em Ciências pela UFRJ. Desenvolvo projetos próprios de software com apoio de ferramentas de IA, concentrando meu aprendizado em integração de modelos, automação e verificação de resultados.

Minha experiência anterior em análise de dados de negócio, pesquisa e treinamento orienta os problemas que escolho resolver: um fluxo precisa produzir uma entrega que outra pessoa consiga conferir, reproduzir e manter.

[Portfólio](https://luandv92.github.io) · [Todos os repositórios](https://github.com/luandv92?tab=repositories) · [LinkedIn](https://www.linkedin.com/in/luan-ribeiro-brito/) · [Contato](mailto:lrb92@hotmail.com)

## Comece por estes projetos

### [llm-cascade](https://github.com/luandv92/llm-cascade)

**Problema:** acoplar uma aplicação a um único modelo ou provedor dificulta lidar com custo e indisponibilidade.

Roteador Python com fallback entre provedores e registro de modelo e custo. O [exemplo de agentes](https://github.com/luandv92/llm-cascade/blob/main/examples/agent_workflow.py) organiza planejador, executor e revisor com contratos JSON, até três chamadas ao roteador e interrupção após uma revisão negativa.

**Confira:** [demo offline e instruções](https://github.com/luandv92/llm-cascade#readme) · [testes dos contratos](https://github.com/luandv92/llm-cascade/blob/main/tests/test_agent_workflow.py) · [CI](https://github.com/luandv92/llm-cascade/actions/workflows/ci.yml)

### [outcome-watchdog](https://github.com/luandv92/outcome-watchdog)

**Problema:** uma rotina pode terminar com sucesso e não produzir nenhuma entrega útil.

Verifica arquivos, crescimento de registros e resultados de comandos. O [exemplo de entregas de agentes](https://github.com/luandv92/outcome-watchdog/blob/master/examples/agent_outcomes.py) distingue resultado recente, ausência de novas entregas e impossibilidade de verificar.

**Confira:** [contratos e uso](https://github.com/luandv92/outcome-watchdog#readme) · [teste do exemplo](https://github.com/luandv92/outcome-watchdog/blob/master/tests/test_agent_outcomes_example.py) · [CI em Linux, macOS e Windows](https://github.com/luandv92/outcome-watchdog/actions/workflows/ci.yml)

### [wiringguard](https://github.com/luandv92/wiringguard)

**Problema:** uma proteção pode continuar importada ou citada no código, embora o fluxo tenha deixado de chamá-la.

Analisa a AST de Python para conferir chamadas obrigatórias e restringir onde determinadas operações podem ocorrer. É uma verificação estática complementar aos testes de comportamento.

**Confira:** [exemplos de regras](https://github.com/luandv92/wiringguard#readme) · [código e testes](https://github.com/luandv92/wiringguard) · [CI](https://github.com/luandv92/wiringguard/actions/workflows/ci.yml)

## Como as peças se conectam

```text
objetivo → planejamento → candidato → revisão → validação da aplicação → entrega
              llm-cascade                          ↓                    ↓
                                             wiringguard        outcome-watchdog
```

Os exemplos de agentes e monitoramento são **demonstrações separadas e reproduzíveis**. A integração em uma rede com estado persistente faz parte do [roadmap](ROADMAP.md). A demo offline usa respostas fixas; ela verifica os contratos do fluxo, sem medir a qualidade de um modelo real. Aprovação por um LLM também precisa de verificações próprias da aplicação.

O [guia de arquitetura](https://github.com/luandv92/awesome-ai-content-ops/blob/master/docs/agent-workflows.md) descreve contratos, limites e próximos passos dessa composição.

## Outros projetos do ecossistema

| Frente | Repositórios e finalidade |
|---|---|
| Qualidade de software | [silentbugs](https://github.com/luandv92/silentbugs): falhas silenciosas em scripts · [pytest-sideeffects](https://github.com/luandv92/pytest-sideeffects): alterações reais de arquivos durante testes |
| Operação de agentes de código | [cc-worktree-ops](https://github.com/luandv92/cc-worktree-ops): continuidade de sessões e integração de worktrees · [cc-cost-kit](https://github.com/luandv92/cc-cost-kit): política de modelos e visibilidade de tokens |
| Qualidade e distribuição de mídia | [media-gate](https://github.com/luandv92/media-gate): vídeo preto, silêncio e duplicação de imagens · [tiktok-direct-post](https://github.com/luandv92/tiktok-direct-post): integração com a API oficial de publicação · [video-prompt-formulas](https://github.com/luandv92/video-prompt-formulas): estruturas de prompts para vídeo |
| Integrações de negócio | [content-ops-automation-templates](https://github.com/luandv92/content-ops-automation-templates): leads, e-mails e UTMs · [stripe-hardening-kit](https://github.com/luandv92/stripe-hardening-kit): validação de integrações e referência de webhook · [honest-timer](https://github.com/luandv92/honest-timer): prazo persistente no navegador |
| Referência de arquitetura | [awesome-ai-content-ops](https://github.com/luandv92/awesome-ai-content-ops): mapa de ferramentas, padrões e limites para pipelines de conteúdo com IA |

## Próximas frentes

- **Rede de agentes e automações:** integrar execução, avaliação e evidência de entrega antes de ampliar a concorrência ou a autonomia.
- **Plataforma educativa Feira das Escolhas / Ludimapa:** evoluir o [piloto público](https://feira.storyteller-mari.com/?lang=pt-BR) e preparar uma extração pública de componentes reutilizáveis, com critérios de privacidade e acessibilidade. Resultados educacionais ainda não foram estabelecidos.

Os nomes de futuros repositórios no [roadmap](ROADMAP.md) são propostas, com critérios de conclusão explícitos. Não representam projetos já publicados.

## Formação e experiência que trago

- **Engenharia da Computação — Universidade Cruzeiro do Sul:** em andamento, conclusão prevista em janeiro de 2029.
- **Mestrado em Ciências — UFRJ:** 2018.
- **Tecnologia em Marketing — UNIGRANRIO:** 2023.
- **BAT Brasil, Trade Marketing e Key Account:** análise de dados de negócio e comunicação de insights, de 2021 a 2023.
- **UFRJ / FAPERJ:** capacitação de alunos e apoio a projetos e experimentos, de 2018 a 2021.

**Objetivo profissional:** oportunidades de estágio em AI Engineering e desenvolvimento de software com IA, com espaço para aprender, construir e validar soluções em equipe.

---

**English:** I am a Computer Engineering student, graduating in January 2029, with an MSc in Science from UFRJ and previous experience in business data analysis and research support. My open-source work focuses on LLM integration, automation reliability and verifiable outcomes. Start with **llm-cascade**, **outcome-watchdog** and **wiringguard**. Agent examples are reproducible demonstrations; the integrated agent network and educational components remain on the roadmap.
