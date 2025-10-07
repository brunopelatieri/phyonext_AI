

::::::::::::::::::: v1 - 06/10/2025 ::::::::::::::::::

--------------------- Sub Agent FGTS Que não possui simulação ------------------
Crie uma versão do prompt sub agent AI tool credit_fgts (Sub-agente Antecipação FGTS Saque-Aniversário) que não possui a tool simulationFGTS: Executa simulação de saldo FGTS.
Nesse contexto, sem a tool simulationFGTS, não é possível fazer a simulação e, sendo assim, não há necessidade dos seguintes passos:
- PASSO 3: AUTORIZAÇÃO DE CONSULTA - Não é necessário nesse contexto sem simulação
- PASSO 4: SIMULAÇÃO - Não é necessário nesse contexto sem simulação 
- PASSO 5: RESULTADO - Não é necessário nesse contexto sem simulação 

Refaça o prompt levando em consideração as instruções acima.
Mantenha todo o resto que não está vinculado tool simulationFGTS.
Otimize o novo prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.


--------------------- Sub Agent FGTS ------------------
Analise o prompt sub agent AI tool credit_fgts (Sub-agente Antecipação FGTS Saque-Aniversário). 
O prompt sub agent AI do prompt principal persona Amanda.
Assim como foi feito com o prompt sub agent AI tool credit_clt (Sub-agente Crédito Consignado CLT).
Faça:
- Altere o nome das tools:
   - guardardadosclt para insertCLT
   - guardardados para insertFGTS
- Instrui para não solicitar novamente os dados solicitado no agente principal como o nome e CPF, procure na memória ou nos tools
- Mantenha o contexto mas otimize para trabalhar com o agent AI principal Amanda 
- Mantenha as instruções que achar melhor e conveniente para o novo contexto, porem as regras de credito FGTS não podem ser alterada
- Formato de saída em tag xml.
- Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.

--------------------- Sub Agent CLT ------------------

Analise o prompt sub agent AI tool credit_clt (Sub-agente Crédito Consignado CLT). 
O prompt sub agent AI do prompt principal persona Amanda.
Seguindo o prompt principal informado anteriormente, faça:
- Altere o nome das tools:
   - guardardadosclt para insertCLT
   - guardardados para insertFGTS
- Instrui para não solicitar novamente os dados solicitado no agente principal como o nome e CPF, procure na memória ou nos tools
- Mantenha o contexto mas otimize para trabalhar com o agent AI principal Amanda 
- Mantenha as instruções que achar melhor e conveniente para o novo contexto.
- Formato de saída em tag xml.
- Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.


::::::::::::::::::: v1 - 04/10/2025 ::::::::::::::::::

Analise o prompt e faça:

- Não altere o contexto apenas otimize e faça as mudanças solicitadas
- Não altere nada dos produtos e suas regras, estão perfeitas, se precisar, otimize.
- retire do contexto a tag <greeting> e o Auto-detecte horário. Não haverá mais cumprimento como: bom dia, boa tarde e boa noite.
- Altere a <meta>:
  - Você é uma vendedora e consultora que genuinamente quer ajudar o cliente a concluir contratação do crédito ideal para sua atual realidade de forma direta, rápida com carinha e empatia.
- Garanta que Amanda realize um atendimento que o cliente não perceba que seja uma IA.
- Otimize o prompt mas sem sacrificar a eficiência das instruções.
- Busque sempre o melhor custo-benefício em relação ao uso de tokens e eficiência na instruções.

---------------------------------
Crie uma descrição para o Think Tool Description do agent AI do n8n para que aja uma reflexão antes das repostas: 
 - Para que aumente a assertividade da IA. 
 - Evite alucinações
 - Não invente nada fora do contexto
 - Siga corretamente todas as etapas e não sai do contexto que foi designada
 - Mantenha sempre o custo/benefício na relação uso de tokens e eficiência no atendimento  


::::::::::::::::::: Prompt Inicial ::::::::::::::::::

Analise o prompt informado:

Contexto atual do prompt informado:
 - O prompt trabalha com dois tipos de crédito: credito clt e credito FGTS
 - Ele identifica qual o cliente quer e redireciona para o sub agente.
 - O prompt informado possui duas tools (n8n node sub agent IA):
    * creditodotrabalhador: executa um sub agent ia especialista em crédito consignado ao trabalhador
    * creditofgts: executa um sub agent ia especialista em crédito de antecipação FGTS

Faça:
 - Nesse novo contexto, esse prompt já recebe o crédito escolhido pelo cliente que já foi atendido por um n8n node sub agent IA anterior e cujo os dados estão na memória compartilhada.
 - Faça as alterações e as otimizações considerando esse novo contexto.
 - Altere o nome das tools:
    * creditodotrabalhador para credit_clt
    * creditofgts: para credit_fgts
    * Mantenha o contexto das tools credit_clt e credit_fgts mas otimize para o contexto atual. 
 - Dentro desse contexto, acrescente mais uma tool com o nome credit_inss que executará um sub agent ia especialista em crédito INSS que possui esses benefícios:
    * Empréstimo Consignado: É um empréstimo pessoal com taxas de juros reduzidas, cujas parcelas são descontadas diretamente da folha de pagamento do benefício
    * Cartão Benefício INSS: É um cartão de crédito que permite saques, compras e o uso do crédito para o pagamento mínimo da fatura, com descontos diretos no benefício
    * Quem pode contratar: 
        * Aposentados e pensionistas do INSS que recebem seus benefícios em conta.
        * Benefícios que podem ser elegíveis incluem aposentadoria por idade, por invalidez, por tempo de contribuição, pensão por morte, entre outros.
 -  Acrescente a tool com o nome credit_servpublic que executará um sub agent ia especialista em crédito para servidores públicos que possui esses benefícios:
    * Taxas de juros mais baixas
    * Prazos de pagamento mais longos
    * Aprovação facilitada e rápida
    * Sem necessidade de avalista ou garantia
    * Margem consignável para garantir o controle financeiro.
    * Quem pode contratar:
      * Servidores ativos
      * Aposentados
      * Pensionistas
      * Servidores públicos federais, estaduais e municipais 
 - Acrescente a tool com o nome credit_bolsafamilia que executará um sub agent ia especialista em crédito para beneficiários do Bolsa Família que possui esses requisitos: 
    * Ser beneficiário do Bolsa Família há pelo menos três meses. 
    * Receber o benefício via aplicativo Caixa Tem. 
    * Ser maior de 18 anos e titular do benefício. 
    * O valor do benefício recebido deve ser de R$ 400 ou mais.

- Acrescente a tool knowledgeDoc. Base completa com as informações de: produtos, serviços, institucionais e outras informações da empresa que oferece os serviços de crédito.
- A tool knowledgeDoc será acionado de acordo com o item: "COMO LIDAR COM OBJEÇÕES (COM EMPATIA)" quando necessitar de dados da empresa.
- Mantenha as instruções que achar melhor e conveniente para o novo contexto.
- Formato de saída em tag xml.
- Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.

