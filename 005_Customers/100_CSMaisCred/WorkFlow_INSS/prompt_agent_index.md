::::::::::::::::::: v1 - 13/01/2025 ::::::::::::::::::

Crie uma Think Tool Description para node Think Tool do node AI Agent especifico para o prompt PROMPT FINAL — OTIMIZADO

-----------------------------------------------------------------

Analise o prompt inteiro enviado em anexo.

Após analise, faça:
    - Analise cada instrução e otimize para que sejam interpretadas de forma correta para o modelo gpt-5-mini
    - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade
    - Nunca altere o contexto.
    - Nunca altere nenhuma mensagem.
    - Nunca altere os passos do workflow
    - Nunca altere as regras de memoria
    - Faças as adaptações necessária mas sem alterar as condições acima

-------------------------------------------------------------------

Apenas implemente uma instrução ao prompt para que quando o cliente informar que já forneceu as informações solicitada e nada foi encontrado na memória pela memory_check, envie a a mensagem: "Em instantes, um especialista vai falar com você aqui no WhatsApp para dar continuidade. Obrigado." e acione a tool "suporteAtendente" e encere o atendimento -> FIM 

---------------------------------------------------------------------

Apenas coloque o "PASSO 2: CONTEXTO E AUTORIZAÇÃO" no lugar do "PASSO 1: DADOS ESSENCIAIS".
O "PASSO 1: DADOS ESSENCIAIS" para o lugar do "PASSO 2: CONTEXTO E AUTORIZAÇÃO".
Faça as adaptações necessárias e não altera contexto de forma alguma. 

---------------------------------------------------------------------

Analise o prompt:

Após a analise adicione a tool "tagChatwoot".
A tool "tagChatwoot" será responsável para adicionar e categorizar os contatos atendidos nas seguintes tags:
    - qualificados: enviou nome, cpf, os documentos e desbloqueio do INSS (site app)
    - não_enviou_documentos: não enviou ou recusou enviar os documentos
    - não_desbloqueou_inss: informou que não desbloqueou ou não sabe fazer
    - solicitou_suporte: foi enviado pelo suporte acionou a tool "suporteAtendente"
    - não_interessou_desistiu: não demonstrou interesse ou desistiu
Pode categorizar de uma até 3 tags cada contato.
O formato, obrigatoriamente, precisar ser um json sempre em formato: {"labels": ["tag1", "tag2"]}
Executar a analise para categorizar as tags a cada passo do worflow.
Enviar o json sempre no formato correto para tool "tagChatwoot"



