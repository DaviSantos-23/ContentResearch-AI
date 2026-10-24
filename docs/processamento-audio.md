# Processamento de Áudio

## Objetivo

Permitir que o usuário envie uma solicitação por áudio pelo Telegram, sem precisar digitar o assunto.

## Fluxo funcional

1. O usuário envia um áudio.
2. O workflow identifica e processa o arquivo.
3. O componente de processamento de áudio configurado obtém o conteúdo textual ou realiza a tradução prevista.
4. O texto resultante é encaminhado à etapa de pesquisa.
5. O restante do workflow segue o fluxo normal de geração e entrega dos conteúdos.

## Considerações

A transcrição converte a fala em texto. A tradução converte o conteúdo de um idioma para outro. São operações diferentes e a documentação definitiva deve indicar qual delas é executada pelo workflow.

A qualidade do resultado pode depender da clareza da gravação, do idioma, do ruído de fundo e do serviço de processamento utilizado.

## Testes recomendados

- Áudio curto e claro.
- Áudio com ruído de fundo.
- Áudio com nomes próprios ou termos técnicos.
- Áudio em outro idioma, se houver suporte à tradução.
- Mensagem de áudio inválida ou sem conteúdo reconhecível.
