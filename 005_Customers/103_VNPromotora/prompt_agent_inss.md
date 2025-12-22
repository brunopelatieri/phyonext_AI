::::::::::::::::::: v3 - 17/12/2025 ::::::::::::::::::
Analise o prompt especialista INSS - sub agent tool credit_inss, informado.

Após analise, faça:
    - No workflow retirar o passo "TIPO DE BENEFÍCIO" e passo "TITULARIDADE"
    - Passo 3 "SITUAÇÃO ATUAL" passa a ser o primeiro passo do workflow
    - Se no caso a escolha do passo "SITUAÇÃO ATUAL" for: "Garantir meu crédito com aumento salarial de 2026", faça as perguntas abaixo:
        - "Você tem o extrato de consignações do INSS em mãos? Assim conseguimos verificar seus benefícios rapidinho 😊"
            - ação pos pergunta: Se "sim" aguarde o envio (aciona a tool insertINSS e guarde em "MARGEM - EXTRATO" ) e continue. Se "não", faça a pergunta:
        - "Caso não tenha, você pode nos enviar os dados de acesso ao aplicativo Meu INSS.
            Assim conseguimos consultar seus benefícios com mais agilidade e precisão.
            Seus dados são utilizados apenas para consulta, com total sigilo."
            - ação pós pergunta: Se informar prossiga e se informar "não" continue para a próxima pergunta
        - "Você tem proposta em andamento em outra promotora? Precisamos saber qual parcela está em portabilidade para não atrapalhar a liberação do seu crédito."
            -ação pós pergunta: Se informar que possui apenas registra na tool insertINSS e guarde em "CRÉDITO ANTERIOR" e prossiga. Se informar "não" continue
        - Coloque o passo "DESBLOQUEIO MEU INSS" nesse ponto. Após a "SITUAÇÃO ATUAL" for: "Garantir meu crédito com aumento salarial de 2026", faça as perguntas e depois das perguntas acima.
    - Ajuste os outros passo em sequência.
    - No insertINSS: 
        - TIPO BENEFICIO: sempre salva INSS, 
        - TITULARIDADE: sempre salva titular 
        -  Resposta do passo "SITUAÇÃO ATUAL" guarda como observação
    - No objetivo, faça:
        Retire "Qualificar beneficiário INSS através dos PASSOS 1, 2 e 3 (tipo benefício, titularidade, situação)"
        Retire qualquer outra qualificação. 
        Faças as perguntas com as regras acima e acione a tool Acione suporteAtendente (FIM)
        REtire: "Mas temos outras opções:

1️⃣ ⭐ **Limpa Nome** (renegocie dívidas)
2️⃣ CLT (se trabalha com carteira assinada)
3️⃣ FGTS (se tem saldo no fundo)
4️⃣ Bolsa Família (se é beneficiário)"

    - Retire todo esse processo de qualificação. Apenas colha as informações, acione a tool insertINSS (para salvar) e por fim acione a tool suporteAtendente e transfira para o humano com o máximo de informações possíveis.
    - Esse é o principal objetivo.

-------------------------------------------------------------------------------

Analise o "sub-tool agent IA" de nome "credit_inss":

Veja se precisa das seguintes ações: - Procure por ambiguidades e corrija - Analise cada instrução e otimize para que sejam interpretadas de forma correta - Não altera contexto de forma alguma, faça as alterações de instrução se precisar faça correções no prompt mas sem alterar o contexto geral do especialista credit_inss - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade. Importante: Liste o que vai fazer antes de fazer e espere meu consentimento.

--------------------------------------------------------------------------------

Apenas retire do "sub-tool agent IA" de nome "credit_inss" PASSO 1.4: DESBLOQUEIO MEU INSS e faça os ajustes

::::::::::::::::::: v1 - 11/12/2025 ::::::::::::::::::

Analise o prompt especialista INSS - sub agent tool credit_inss, informado.

Após analise, faça:
    - No workflow passo 3 acrescentar "Garantir meu crédito com a aumento salarial de 2026" 
    - Após o passo 3 incluir a pergunta "Você sabe desbloquear o seu benefício dentro do aplicativo Meu INSS ou no site oficial do INSS (www.meu.inss.gov.br).". Pergunta apenas para informar o suporte atendente. Pergunta não qualificatória apenas para informar o suporte atendente na tool suporteAtendente.
    - Acrescente no menu o produto em destaque "Limpa Nome"
    - Adicione a tool "knowledgeDoc" do vinculado ao agente index que contem informações sobre o produto em destaque "Limpa Nome" (busque informações na tool "knowledgeDoc" para passar informações ao cliente)
    - Após passar informações sobre o produto "Limpa Nome", quando solicitado, pergunta se possui interesse, em caso afirmativo, aciona a tool suporteAtendente
    - Procure por ambiguidades e corrija
    - Analise cada instrução e otimize para que sejam interpretadas de forma correta
    - Não altera contexto de forma alguma, faça as alterações de instrução se precisar faça correções no prompt mas sem alterar o contexto geral do especialista credit_inss
    - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.

-----------------------------------------------------------
Retire o "Limpa Nome" produto destaque do passo 3 e coloque em:

"Mas temos outras opções:

1️⃣ CLT (se trabalha com carteira assinada)

2️⃣ FGTS (se tem saldo no fundo)

3️⃣ Bolsa Família (se é beneficiário)"

Não altera contexto de forma alguma, faça as alterações de instrução se precisar faça correções no prompt mas sem alterar o contexto geral do especialista credit_inss

------------------------------------------------------------

Faça os ajustes:
     - Coloque o item "Garantir meu crédito com aumento salarial de 2026" em primeiro no passo 3
     - Nunca tem ajudar a pessoa que fala que não sabe fazer o passo 4: Desbloquear o objetivo.
     - Seu objetivo e receber um resposta positiva ou negativa (sim ou não)
     - Passo 4 não precisa acionar a tool insertINSS. Essa informação não é registrada na tool insertINSS
     - No passo 5 o cliente já é beneficiário do INSS e não precisa mais dessa validação. Apenas valide "Situação declarada no PASSO 3 é elegível?"
     - Coloque o Limpa nome em primeiro em "Mas temos outras opções:"
     - Retire por completo o passo 6.
     - No objetivo do prompt "Qualificar cliente através de 6 passos lineares" altere para qualificar e enviar para a tool suporteAtendente apenas os passos: 1, 2 e 3
    - Procure por ambiguidades e corrija
    - Analise cada instrução e otimize para que sejam interpretadas de forma correta
    - Faça as alterações de instrução se precisar faça correções no prompt mas sem alterar o contexto geral do especialista credit_inss
    - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.


    
    
