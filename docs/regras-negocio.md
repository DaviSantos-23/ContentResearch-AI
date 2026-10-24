# Regras de Negócio

## Entrada

O sistema recebe mensagens pelo Telegram e trabalha com os tipos de entrada previstos no workflow: texto e áudio.

## Pesquisa

O assunto da mensagem é utilizado para orientar a pesquisa na web com Tavily.

## Geração de conteúdo

A pesquisa fornece contexto para produzir quatro saídas distintas:

1. Conteúdo para Instagram.
2. Conteúdo para LinkedIn.
3. Conteúdo para Newsletter.
4. Conteúdo para YouTube.

As saídas devem respeitar as instruções e o formato definidos para cada canal.

## Armazenamento

Os quatro conteúdos devem ser salvos em uma pasta criada pelo sistema no Google Drive.

## Entrega

O usuário recebe pelo Telegram o link da pasta de resultados.

## Qualidade e confiabilidade

- O conteúdo gerado deve ser coerente com o assunto informado.
- A pesquisa deve ser utilizada como contexto, e não como garantia automática de veracidade.
- Informações factuais relevantes devem ser verificadas nas fontes consultadas.
- O sistema não deve apresentar informações inventadas como fatos confirmados.
- Se uma etapa falhar, o sistema não deve indicar que todos os arquivos foram gerados com sucesso.
- O link de entrega deve apontar para a pasta correta e ter permissões compatíveis com o uso pretendido.

## Segurança

Tokens, chaves de API e credenciais não devem ser incluídos no repositório público.

Os arquivos e links devem respeitar as permissões de acesso configuradas no Google Drive.
