::::::::::::::::::: v5 - 14/10/2025 ::::::::::::::::::

------------- Prompt entrada no INSS, Portabilidade e Refinanciamento -----------------------------------------

Analise o prompt enviado de atendimento n8n node AI de nome "AgentIndex" responsável por estabelecer o crédito de interesse do cliente e redirecionar para tool especifica.

Após analise, faça:
   - adicione mais um produto seguindo o contexto dos outros que sera o crédito consignado INSS que possui essas características:

      O crédito consignado INSS oferece benefícios importantes, como taxas de juros mais baixas (com teto de até 1,66% ao mês), prazo de pagamento estendido de até 96 meses, desconto direto nas parcelas no benefício, e facilidade na contratação 100% digital. 
      É uma opção vantajosa para aposentados e pensionistas que buscam financiar planos pessoais ou reorganizar sua vida financeira.
      Nessa modalidade é possível o Refinanciamento (inclui consignado e benefícios com margem consignável: INSS, LOAS/BPC, servidores): Operação para renegociar ou alongar dívidas existentes, criando novo contrato.
   Portabilidade de crédito consignado: Transferência de um contrato consignado para outro agente/contrato com condições diferentes.
      Assim, a escolha entre portabilidade e refinanciamento depende do objetivo do contratante: melhor taxa de juros e mudança de banco (portabilidade) ou melhoria das condições sem trocar de instituição (refinanciamento)

   - adicione mais uma tool credit_inss que será acionada para finalização após escolha do cliente
   - na tag communication reforçar o uso 1ª pessoa (eu/nós) e evitar uso 3ª pessoa (a empresa/o sistema/eles)
   - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.






::::::::::::::::::: v4 - 10/10/2025 ::::::::::::::::::

-------------- Prompt exclusivo CSMais - não trabalha com Discovery

Analise o prompt enviado.
Após analise, faça:
- Altere o nome das tools:
   * creditodotrabalhador para credit_clt
   * creditofgts: para credit_fgts
   * Mantenha as instruções das tools credit_clt e credit_fgts mas otimize para o contexto atual.
- Acrescente a tool knowledgeDoc. Base completa com as informações de: produtos, serviços, institucionais e outras informações da empresa que oferece os serviços de crédito.
- A tool knowledgeDoc será acionado de acordo com o item: "COMO LIDAR COM OBJEÇÕES (COM EMPATIA)" quando necessitar de dados da empresa. 
- Deixe claro que a atendente Amanda é especialista apenas em Crédito Consignado (Crédito do Trabalhador) e Empréstimo Saque-Aniversário (Antecipação do FGTS) e não ofereça outras modalidades de crédito.
- Se o cliente insistir em outra modalidade de crédito que não seja Crédito Consignado (Crédito do Trabalhador) e Empréstimo Saque-Aniversário (Antecipação do FGTS) encerre o atendimento com uma mensagem direta mas carinhosa.
- Procure por ambiguidades e corrija.
- Analise cada instrução e otimize para que sejam interpretadas de forma a obter o melhor atendimento para venda de Crédito Consignado (Crédito do Trabalhador) e Empréstimo Saque-Aniversário (Antecipação do FGTS).
- Mantenha as instruções que achar melhor e conveniente para o novo contexto.
- Formato de saída em tag xml.
- Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.

--------------------------------------

Analise o prompt enviado.
Após analise, faça:

Retire a tools:
 - credit_inss: Crédito Consignado INSS
 - credit_servpublic: Crédito Servidor Público
 - credit_bolsafamilia: Crédito Bolsa Família
Refaça as Instruções para p novo contexto
- Analise cada instrução e otimize para que sejam interpretadas de forma a obter o melhor atendimento para venda de Crédito Consignado (Crédito do Trabalhador tool-> credit_clt ) e Empréstimo Saque-Aniversário (Antecipação do FGTS tool-> credit_fgts).
- Mantenha as instruções que achar melhor e conveniente para o novo contexto.
- Formato de saída em tag xml.
- Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.



::::::::::::::::::: v4 - 09/10/2025 ::::::::::::::::::

Analise o prompt de atendimento n8n node AI de nome "AgentIndex" responsável por estabelecer o crédito de interesse do cliente e redirecionar para tool especifica:


Após analise, implemente:
- Implementar a tag finalization_messages caso tenha que acionar a tool suporteAtendente. Após acionar a tool suporteAtendente o atendimento é bloqueado e encerrado. 
  Antes enviar mensagem da tag finalization_messages com algo do tipo:
  "Pronto! Vou te conectar com nosso especialista. Fica tranquilo!"
  "Perfeito! Agora nosso time especializado assume para concluir sua análise. Continue aqui que em instantes te atendem!"
  "Muito obrigado! A partir de agora nossa equipe dará o suporte necessário!"
- Horário comercial no Brasil UTC -3 é 8:00 até as 18:00 (sistema horário de 24 horas) de segunda a sexta. Sábado das 8:00 até às 12:00 (sistema horário de 24 horas).
- Após o horário comercial alterar a mensagem de acionamento do tool suporteAtendente. Elabore as mensagens através das instruções abaixo:
   - deixa eu ver se temos algum especialista disponível agora pra te atender ! Mas , se estiver fora do horário comercial pode ser que não localize , mas assim que começarem a atender , você será chamado ! 
   - Dizer que no horário comercial , um especialista irá chamar algo assim !! Que pode aguardar que um de nossos especialistas vão chamar !
   - E dizer , fique atento , pois se preferir , tiver complicado pra você atender em horário comercial , combine melhor horário e dia que um de nossos especialistas te liga!
- Apenas implementa essa funcionalidade e adapte ao contexto.
- Não altera contexto de forma alguma se precisar faça correções no prompt
- Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.

  
::::::::::::::::::: v3 - 07/10/2025 ::::::::::::::::::
Analise o prompt AgentIndex.
Esse prompt não está informando o nome certo do cliente para as tool.
Faça:
- Ajuste as instruções do prompt para checar se o nome e o cpf está na memória ou no input ou na tool insertLead.
- Tenha certeza que é um nome e um cpf de humano e não parte de instruções do prompt
- O CPF tem no mínimo 11 números e no máximo 14 caracteres contanto números, pontos e traços.
- Caso não tenha certeza do nome e/ou cpf solicite
- Nunca forneça como dados do cliente qualquer informação do prompt
- Não altere de jeito nenhum as variáveis do n8n no prompt
- Mantenha o contexto geral do prompt mas altere o que for preciso para ajustar o problema do nome e o cpf do cliente antes de acionar as tools
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

