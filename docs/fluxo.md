# Fluxo de Execução

## 1. Recebimento da mensagem

O Telegram Trigger inicia o workflow quando o usuário envia uma mensagem.

## 2. Tratamento da entrada

O sistema verifica o tipo de entrada recebido e encaminha o conteúdo para o processamento correspondente.

- Texto: utiliza o conteúdo textual recebido.
- Áudio: executa a etapa de processamento configurada para obter o conteúdo textual necessário.

## 3. Preparação do assunto

O conteúdo é estruturado para ser utilizado na pesquisa e nas etapas seguintes.

## 4. Pesquisa na web

O Tavily é utilizado para pesquisar informações relacionadas ao assunto enviado pelo usuário.

## 5. Síntese

As informações recuperadas são organizadas e utilizadas como contexto para a geração dos conteúdos.

## 6. Geração especializada

O workflow encaminha o contexto para as etapas de criação de conteúdo para:

- Instagram;
- LinkedIn;
- Newsletter;
- YouTube.

Cada saída possui instruções próprias para o formato e a finalidade do canal.

## 7. Criação e organização dos arquivos

O sistema cria uma pasta no Google Drive e armazena os quatro conteúdos gerados.

## 8. Retorno ao usuário

Após a preparação dos resultados, o workflow envia pelo Telegram uma mensagem contendo o link da pasta criada.

## Resultado esperado

Uma mensagem de entrada produz uma pasta com quatro arquivos de conteúdo, organizados por canal e acessíveis por meio do link enviado ao usuário.

## Observação

A ordem e o comportamento de cada node devem ser conferidos no JSON exportado do workflow. Esta documentação descreve o fluxo funcional do projeto.
