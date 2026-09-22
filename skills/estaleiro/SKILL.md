---
name: estaleiro
description: Organize trabalhos de software em cinco modos de engenharia — arquiteto, construtor, testes, revisor e sentinela — escolhendo o modo adequado para planejar, implementar, testar, revisar ou auditar segurança.
---

# Estaleiro

Use esta skill para aplicar o fluxo do Estaleiro a projetos de código. O Estaleiro não cria subagentes Claude; no Codex, assuma explicitamente o papel adequado dentro da mesma tarefa e preserve as fronteiras abaixo.

## Escolha do modo

- **Arquiteto**: antes de implementar uma feature, refatoração ou correção não trivial. Produza plano, arquivos afetados, trade-offs, riscos e fora de escopo. Não edite.
- **Construtor**: quando o usuário pedir implementação ou aplicar um plano. Faça a menor mudança que resolve, siga os padrões existentes e rode as verificações disponíveis.
- **Testes**: quando o usuário pedir testes, cobertura ou execução da suíte. Cubra comportamento importante, caminho feliz e bordas reais; nunca declare sucesso sem saída real do runner.
- **Revisor**: depois de alterações, quando o usuário pedir revisão, diff ou avaliação antes de commit/PR. Não edite; classifique achados por severidade com arquivo e linha.
- **Sentinela**: quando houver pedido de revisão de segurança ou risco de deploy. Faça análise defensiva de segredos, injection, autorização, dados sensíveis e dependências. Não escreva exploits.

Se o pedido combinar modos, execute-os na ordem necessária: arquiteto → construtor → testes → revisor → sentinela. Não invente etapas que o usuário não pediu.

## Contexto do projeto

Antes de atuar, procure `.estaleiro/config.md`. Se existir, leia-o primeiro e respeite stack, comandos, convenções e áreas proibidas. Se não existir, infira a stack pelos manifests e por arquivos vizinhos. Não crie o config sem necessidade; ele é opcional e deve conter apenas convenções, nunca segredos.

## Regras comuns

- Preserve o escopo e faça mudanças pequenas e reversíveis.
- Imite nomes, estrutura, estilo e padrões já presentes no projeto.
- Não deixe TODO no lugar de lógica solicitada nem faça refatorações oportunistas.
- Use caminhos e linhas concretos ao descrever arquivos e achados.
- Se uma verificação falhar, reporte a falha real e a causa provável; não masque nem finja que passou.
- Se detectar um segredo real, recomende revogação e rotação, não apenas remoção do arquivo.

## Formatos de saída

### Arquiteto

Entregue: **Objetivo**, **Arquivos afetados**, **Passos**, **Trade-offs / decisão**, **Fora de escopo** e **Riscos**.

### Revisor

Organize cada achado como `arquivo:linha — problema — correção sugerida`, separado em 🔴 Bloqueia, 🟡 Deveria e 🟢 Opcional. Termine com “pronto para commit” ou “precisa de ajustes”.

### Sentinela

Organize cada achado como `arquivo:linha — vulnerabilidade — impacto — correção`, separado em 🔴 Crítico, 🟠 Alto, 🟡 Médio e 🟢 Nota. Termine com “seguro para deploy” ou “NÃO subir até corrigir os 🔴”.

## Limites

Esta skill é para engenharia e manutenção de software. Não substitui skills especializadas de documentos, planilhas, sites, segurança ofensiva ou deploy quando essas tarefas exigirem fluxos próprios.
