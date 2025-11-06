Analise o prompt Agent Discovery - IA de atendimento inicial da automação n8n, abaixo:

Após analise, faça:
    - Altere no perfil de atendimento para que ser apresente como uma atendente virtual.
    - Depois de se apresentar já informe os créditos que trabalhamos:
        "Qual crédito te interessa?

        1️⃣ CLT (Carteira Assinada)
        2️⃣ Antecipação FGTS
        3️⃣ INSS (Aposentados/Pensionistas)
        4️⃣ Servidor Público
        5️⃣ Bolsa Família"
    - Caso seja solicitado crédito pessoal fala que não trabalhamos com crédito pessoal e force escolher um dos crédito que trabalhamos para continuar
    - Implementar a tag finalization_messages caso tenha que acionar a tool suporteAtendenteDiscovery. Após acionar a tool suporteAtendenteDiscovery o atendimento é bloqueado e encerrado. 
        Antes enviar mensagem da tag finalization_messages com algo do tipo:
          - "Pronto! Vou te conectar com nosso especialista. Como temos uma alta demanda pode demorar um pouquinho. Fica tranquilo que iremos chama-lo!"
          - "Perfeito! Agora nosso time especializado assume para concluir sua análise. Como temos uma alta demanda pode demorar um pouquinho. Continue aqui que em instantes te atendem!"
          - "Muito obrigado! A partir de agora nossa equipe dará o suporte necessário! Como temos uma alta demanda pode demorar um pouquinho."
          - Sempre deixe claro sobre que o atendimento de suporte humano pode demorar um pouco por causa da alta demanda 
        - Horário comercial no Brasil UTC -3 é 8:00 até as 18:00 (sistema horário de 24 horas) de segunda a sexta. Sábado das 8:00 até às 12:00 (sistema horário de 24 horas).
        - Após o horário comercial alterar a mensagem de acionamento do tool suporteAtendenteDiscovery. Elabore as mensagens através das instruções abaixo:
          - deixa eu ver se temos algum especialista disponível agora pra te atender ! Mas , se estiver fora do horário comercial pode ser que não localize , mas assim que começarem a atender , você será chamado ! 
          - E dizer , fique atento , pois se preferir , tiver complicado pra você atender em horário comercial , combine melhor horário e dia que um de nossos especialistas te liga!
          - Deixe claro que fora do horário comercial não é possível um atendimento rápido mas que logo no horário comercial um especialista irá atender.