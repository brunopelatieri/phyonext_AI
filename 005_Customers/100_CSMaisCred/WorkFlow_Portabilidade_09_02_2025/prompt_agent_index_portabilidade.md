
::::::::::::::::::: v5 - 09/02/2025 ::::::::::::::::::

Analise novamente o PROMPT — AgentIndex | CSMaisCred | Portabilidade + Refinanciamento Consignado INSS com instruções que coloquei manualmente sobre a utilização da tool  insertINSS no workflow. Coloque instrução para que quando solicitar atendimento suporte humana mais de uma vez, que seja acionado a tool suporteAtendente. Envie uma msg antes de acionar a tools suporteAtendente. Após o acionamento da tool suporteAtendente o atendimento e bloqueado na automação.

Valide toda as instruções dentro dos critérios abaixo:
    - Analise cada instrução e otimize para que sejam interpretadas de forma correta para o modelo gpt-5-mini.
    - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.

------------------------------------------------------------------------

Analise o prompt do cliente, CSMaisCred abaixo (entre aspas):
Após analise, faça:
    - Mudaremos a missão e o contexto para atendimento de portabilidade com refinanciamento de empréstimo consignado INSS
    - Manter "memory-check" memory_fallback para solicitar nome e CPF
    - Manter a tag solicitou_suporte
    - Workflow de seguir essa etapas:   
        - O senhor recebe benefício desde quanto (precisa ser igual ou anterior a 2024 - se não for mensagem de encerramento e fim - tag-> {"labels":["beneficio_2025_em_diante"]} )
        - Qual a idade do senhor? (acima de 43anos - se não for mensagem de encerramento e fim - tag-> {"labels":["abaixo_43_anos"]})
        - O senhor já possui empréstimos consignados? (Resposta precisa ser sim - se não for, mensagem de encerfamento e fim - tag-> {"labels":["não_possui_emprestimo_consignado"]} )
        - O senhor tem o extrato de empréstimos consignado? (se sim, pedir para enviar, confirmar se enviou, se enviado extrato - tag-> {"labels":["qualificados"]} e fim com suporte humano tool -> suporteAtendente , se não enviar documento extrato utilizar tag {"labels":["não_enviou_documentos","solicitou_suporte"]} e acionar a tool -> suporteAtendente )
        - Sempre enviar um mensagem utilizando o conceito "Enviar mensagem final conforme horário:" do prompt antigo.
    - O objetivo agora e Qualificar clientes de portabilidade com refinanciamento de empréstimo consignado INSS.
    - Analise cada instrução e otimize para que sejam interpretadas de forma correta para o modelo gpt-5-mini.
    - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.
