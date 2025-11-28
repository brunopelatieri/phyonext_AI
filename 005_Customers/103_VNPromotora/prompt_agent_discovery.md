::::::::::::::::::: v2 - 25/11/2025 ::::::::::::::::::

Analise o prompt Agent Discovery - IA de atendimento inicial da automação n8n, abaixo:

Após analise, faça:
  - Adicionar um novo produto chamado "limpa nome" no menu com as seguintes características:
    - Limpa o nome nos principais órgãos de proteção ao crédito (SERASA, SPC, BOA VISTA) de forma totalmente jurídica, respaldada pelo artigo 42 do Código de Defesa do Consumidor (CDC). Em até 60 dias, todas as restrições nesses órgãos são retiradas!
    Garantia de 6 meses ou 1 ano: Seu nome permanecerá limpo nesses órgãos por um período de 6 a 12 meses, e seu Score será restaurado ao melhor patamar dos últimos 5 anos! Atenção: Existem dívidas que não aparecem no SERASA, SPC, BOA VISTA ou CENPROT. Mesmo com o nome limpo, elas podem impedir a aprovação de crédito. São dívidas registradas no BACEN (bancárias), CADIN (Receita Federal) e CCF (cheques sem fundo). O Limpa Nome é eficaz para restrições no SPC, SERASA e Boa Vista, e também no CENPROT (Protestos) . 
    Ao baixar os apontamentos nesses órgãos, você volta a ter acesso a crediários, lojas e operadoras que consultam apenas o SPC/SERASA. Vamos prosseguir? Saber Valores ?
    Veja qual a melhor opção pra você :

    Garantia por 6 meses

    •	Limpar nome (SPC/Serasa): 
              No Pix ou Cartão R$ 700,00 link - https://mpago.la/1UgoBLR - 

    •	Limpar nome (SPC/Serasa + Protesto): 
    No Pix ou Cartão R$ 900,00 link - https://mpago.la/12hdP82 

    Garantia por 12 meses

    •	Limpar nome (SPC/Serasa): 
      No Pix ou Cartão  R$ 1.200,00 link: https://mpago.la/1Ls84H2 - 
    •	Limpar nome (SPC/Serasa + Protesto): 
                No Pix ou Cartão  R$ 1.500,00 link: https://mpago.la/1AYPmnd 

    No Boleto as baixas  são (SPC/Serasa + Protesto):

    Garantia por 6 meses
    •	No boleto : 
    R$ 800,00 . 
    Entrada de R$ 200,00 no link : https://mpago.la/2Zpe8Bi
    E restante no boleto em até 6 x R$ 100,00 No boleto 
  - Dê foque para esse produto. Esse produto é destaque.
  - Dê a opção de enviar audio e quando for solicitado acione a tool audio_limpa_nome
  - Elimine as ambiguidades no redirecionamento da tool de crédito especialista.
  - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.



::::::::::::::::::: v1 - 06/11/2025 ::::::::::::::::::

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