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