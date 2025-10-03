Este repositório contém um exemplo de AdaptiveDialog, usado em Microsoft Copilot Studio para estruturar como um agente conversacional deve reagir às perguntas do usuário.

## Objetivo do diálogo:

O fluxo foi construído para responder perguntas sobre o AI Builder, ferramenta de inteligência artificial integrada à Power Platform da Microsoft.

## Fluxo principal (beginDialog):

A primeira ação é o SearchAndSummarizeContent, que pega a pergunta do usuário (System.Activity.Text) e busca informações sobre AI Builder.

Depois, há uma condição (ConditionGroup) que verifica se o usuário realmente digitou algo.

Se a entrada não estiver vazia, o sistema inicia outro diálogo (BeginDialog) específico sobre o tópico AI Builder.

Caso contrário (se não houver entrada ou não for encontrada resposta), o bot envia uma mensagem padrão de desculpa e um link para o site da Microsoft com mais informações.

## Encerramento:

Após o fluxo, sempre é enviado o aviso “Tópico de AI Builder encerrado!” para indicar o fim da interação.

### 👉 Em resumo, esse conteúdo mostra como configurar um diálogo adaptativo para:

- Interpretar a entrada do usuário.
- Buscar e resumir informações relevantes (no caso, sobre AI Builder).
- Aplicar condições para decidir a próxima ação (continuar em outro diálogo ou mostrar mensagem de fallback).
- Finalizar o tópico de forma clara.