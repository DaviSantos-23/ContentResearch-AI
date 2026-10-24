# Arquitetura do ContentResearch-AI

## Visão geral

O ContentResearch-AI é uma solução de automação desenvolvida com n8n para pesquisar informações sobre um assunto e transformá-las em conteúdos adaptados a diferentes plataformas.

A interação ocorre por meio do Telegram. O usuário envia uma mensagem de texto ou áudio, o sistema processa a entrada, realiza uma pesquisa com Tavily, gera quatro versões do conteúdo e organiza os resultados em uma pasta do Google Drive.

Ao final, o usuário recebe pelo Telegram o link para acessar os arquivos gerados.

## Componentes

### 1. Telegram

Responsável por receber a mensagem inicial e entregar o link da pasta ao usuário após o processamento.

### 2. Processamento da mensagem

Identifica e trata a entrada recebida. Para mensagens de áudio, executa a etapa de processamento de áudio configurada no workflow antes de continuar.

### 3. Tavily

Realiza a pesquisa na web relacionada ao assunto informado, fornecendo informações para a etapa de síntese e geração.

### 4. Inteligência Artificial Generativa

Processa as informações coletadas e gera conteúdos para quatro destinos: Instagram, LinkedIn, Newsletter e YouTube.

### 5. Google Drive

Recebe a pasta criada automaticamente e armazena os arquivos gerados.

### 6. n8n

Orquestra as etapas, integra os serviços e controla a execução do fluxo.

## Arquitetura lógica

Telegram → Processamento da entrada → Pesquisa Tavily → Síntese das informações → Geração dos quatro formatos → Google Drive → Retorno pelo Telegram.

## Benefícios

- Redução do trabalho manual de pesquisa e preparação de conteúdo.
- Reaproveitamento de uma pesquisa em diferentes canais.
- Padronização da produção de conteúdo.
- Organização automática dos resultados.
- Integração entre APIs e serviços externos.

## Observação

Os modelos de IA, os parâmetros e as etapas exatas de processamento dependem da configuração efetiva do workflow exportado do n8n.
