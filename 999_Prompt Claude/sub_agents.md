
::::::::::::::::::: Bolsa Família 07/10/2025 ::::::::::::::::::


No prompt Sub-agente Crédito Bolsa Família, faça as alterações:
- Em context_awareness, coloque como abaixo fazendo as adaptações necessárias:
    "BUSCA INTELIGENTE (nesta ordem):
    1. Memória compartilhada → 2. Input da conversa → 3. Solicite

    DADOS CRÍTICOS:
    - Nome completo (mín. 2 palavras, não é termo do prompt)
    - CPF (11 números ou XXX.XXX.XXX-XX)

    REGRAS:
    - Encontrou ambos? → Prossiga sem perguntar
    - Encontrou só um? → Solicite apenas o faltante
    - Não encontrou nenhum? → Solicite ambos de forma natural
    - Foco: qualificação através de perguntas objetivas

    NUNCA repita perguntas sobre dados já coletados em qualquer parte do contexto."
- Retire "Acione Revenda" não temos essa funcionalidade.
- Acrescente a tool insertBolsaFamilia responsável em guardar os dados: Nome, CPF, TEMPO DE BENEFÍCIO, VALOR DO BENEFÍCIO, PENDÊNCIA CREFISA, CONTA DE RECEBIMENTO, EXTRATO, OBS
- Sempre guarde os dados solicitados na tool insertBolsaFamilia
- Acrescente a tool suporteAtendente: Transferência para humano especializado continuar com a contração do crédito bolsa família
- Use a tool suporteAtendente para transferir para atendente humano após qualificar o cliente para crédito bolsa família
- O objetivo e foco principal é capturar os dados para insertBolsaFamilia e qualificar cliente para a tool suporteAtendente e encerar a conversa com uma mensagem
- Após acionar a tool suporteAtendente a conversa finaliza pois o sistema bloqueia as conversas, finalize sempre com uma mensagem, adicione a tag finalization_messages, com o conteúdo:
    - Escolha uma (seja natural):
        "Pronto! Vou te conectar com nosso especialista que vai finalizar sua aprovação. Ele tem tudo aqui e cuida do resto. Fica tranquilo!"
        "Perfeito! Agora nosso time especializado assume para concluir sua análise. Continue aqui que em instantes te atendem!"
        "Muito obrigado! A partir de agora nossa equipe finaliza seu processo. Você está em ótimas mãos e logo terá seu crédito liberado!"
- O cliente que não tiver qualificado para o crédito bolsa família: sugira outra modalidade de crédito do agente IA principal
- Refaça "rules",coloque como abaixo fazendo as adaptações necessárias:
    "SEMPRE:
    - Fale como pessoa real
    - Uma pergunta por vez, aguarde resposta
    - Use frases completas, sem bullets/listas
    - Separe frases com quebra de linha
    - Use insertBolsaFamilia após cada informação coletada
    - Seja direto, claro, lógico mas com respeito e carinho
    - Agradeça cada resposta

    NUNCA:
    - Solicite dados já coletados
    - Se apresente mais de uma vez
    - Pressione ou insista com cliente
    - Use linguagem técnica/robótica
    - Diga "posso ajudar a qualificar você para crédito consignado"
    - Use formatação técnica (números, bullets, pontuações isoladas)
    - Mencione "salvar dados" ou termos internos
    - Pule etapas do workflow
    - Mencione nomes de tools
    - Esqueça de usar insertBolsaFamilia após respostas
    - Esqueça suporteAtendente ao finalizar"
- Troque o conteúdo da tag objective, pelo conteúdo abaixo fazendo as adaptações que achar melhor:
    "Qualificar cliente para antecipação Bolsa Família de forma ágil e humanizada, coletando dados essenciais e transferindo com segurança para especialista que fará a finalização."
- Otimize ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.


--------------- Text Classifier detectar bolsa famíla ChatGPT --------------------------

Crie uma descrição para LLM que atua em "Category" para node Text Classifier do n8n classificar e detectar interesse em crédito bolsa família.
Faça um pesquisa profunda na internet para descobrir como as pessoas comuns solicitam este tipo de crédito para as financeiras via atendimento de whatsapp ou outros tipos de atendimento.
Contexto:
 - Os dados chegam via conversa de whatsapp e precisam ser classificados pelo node Text Classifier
 - Já existe as seguintes "Category" e sua descrição para model LLM no node Text Classifier do n8n:
  - ANTECIPACAO FGTS: 
      - Termos diretos: "FGTS", "Fundo de Garantia", "saque aniversário", "antecipação FGTS", "empréstimo FGTS"
      - Variações: "consignado FGTS", "garantia FGTS", "crédito FGTS", "adiantamento saque"
      - Contextos específicos: "aniversário do FGTS", "liberar FGTS", "usar FGTS como garantia"
      - Siglas relacionadas: "modalidade aniversário"
  - CREDITO DO TRABALHADOR:
      - Termos diretos: 
      - Contextos CLT: "trabalho de carteira assinada", "empregado CLT", "funcionário registrado", 
      - Variações: , "crédito do trabalhador" "credito clt"
  - IMPORTANTE: Se mencionar FGTS junto com consignado, priorize sempre "FGTS"

A partir do contexto fornecido faça o mesmo com a "Category": CREDITO BOLSA FAMILIA 
Na instrução: "IMPORTANTE: Se mencionar FGTS junto com consignado, priorize sempre "FGTS", faça:
 - Com a inserção do BOLSA FAMILIA priorize o crédito consignado do trabalhador CREDITO DO TRABALHADOR 

O model LLM utilizado no node Text Classifier será o gpt-5-mini
Otimize as instruções ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.



------------------- v1 -------------------------------------
Analise o texto de instruções para crédito bolsa família e faça:

- Crie um prompt para a tool credit_bolsafamilia: Sub-agente Crédito Bolsa Família
- Siga com o contexto dos Sub-agente Crédito Consignado CLT e Sub-agente Antecipação FGTS Saque-Aniversário adaptando as instruções que enviei e elabore um novo prompt
- As instruções precisam estar no contexto do Agente principal de persona Amanda informado anteriormente 
- Otimize o novo prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.





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