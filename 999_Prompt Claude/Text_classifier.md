

--------------- Text Classifier detectar INSS 10/12/2025 --------------------------

Analise o text "category" para node Text Classifier do CREDITO_INSS: 
    "Aposentado/pensionista INSS + qualquer crédito, portabilidade, refinanciamento, refin, trocar banco, juros baixos, reduzir parcela, troco, mudar banco, desconto aposentadoria.
    - Palavras-chave: INSS, aposentado, pensionista, portabilidade, refin, trocar, portar, juros baixos, reduzir
    - PRIORIDADE: Se "portabilidade|refin|trocar" + FGTS/Bolsa/CLT → CREDITO_INSS"

Após Analise, acrescente os termos novos e gere um novo com termos:
    - pré-contrato do consignado INSS
    - contexto de uso "Olá, quero fazer o meu pré-contrato do consignado INSS, pra receber primeiro quando liberar"

Verifique se possui ambiguidades nas instruções que possam causar problema de interpretações para classificar
Otimize as instruções ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade


--------------- Text Classifier detectar INSS 22/10/2025 --------------------------

Crie uma descrição para LLM que atua em "Category" para node Text Classifier do n8n classificar e detectar interesse em crédito consignado para servidores públicos municipais, estaduais e federais.
Faça um pesquisa profunda na internet para descobrir como as pessoas comuns solicitam este tipo de crédito para as financeiras via atendimento de whatsapp ou outros tipos de atendimento.
Contexto:
 - Os dados chegam via conversa de whatsapp e precisam ser classificados pelo node Text Classifier
 - Já existe as seguintes "Category" e sua descrição para model LLM no node Text Classifier do n8n:
   - ANTECIPACAO_FGTS: 
        Saque ou antecipação de FGTS. Apenas quando não há "portabilidade", "refin" ou "renovar empréstimo".
        - Palavras-chave: FGTS, saque aniversário, antecipação, liberar FGTS, Fundo Garantia
        - EXCLUSÃO: Se "portabilidade", "refin" ou "renovação" → CREDITO_INSS
   - CREDITO_DO_TRABALHADOR:
        CLT/carteira assinada sem "portabilidade" ou "refinanciamento".
        - Palavras-chave: CLT, carteira assinada, funcionário, desconto folha, empregado formal
        - EXCLUSÃO: Se "portabilidade", "refin", "trocar" → CREDITO_INSS

   - CREDITO_BOLSA_FAMILIA:
        Bolsa Família/Auxílio Brasil como base de crédito. Apenas quando não há "portabilidade" ou "trocar banco".
        - Palavras-chave: Bolsa Família, Auxílio Brasil, BF, benefício social, CadÚnico, governo programa
        - EXCLUSÃO: Se "portabilidade", "refin", "mudar banco" → CREDITO_INSS

    - CREDITO_INSS:
        Aposentado/pensionista INSS + qualquer crédito, portabilidade, refinanciamento, refin, trocar banco, juros baixos, reduzir parcela, troco, mudar banco, desconto aposentadoria.
        - Palavras-chave: INSS, aposentado, pensionista, portabilidade, refin, trocar, portar, juros baixos, reduzir
        - PRIORIDADE: Se "portabilidade|refin|trocar" + FGTS/Bolsa/CLT → CREDITO_INSS

A partir do contexto fornecido faça o mesmo com a "Category": CREDITO_SERVIDORES 
Na instrução "IMPORTANTE, refaça com as seguintes alterações:
    - Se mencionar FGTS com consignado priorize crédito INSS, portabilidade e refinanciamento (CREDITO_INSS) e se for servidores públicos da ativo ou aposentados priorize CREDITO_SERVIDORES
    - Se mencionar Bolsa familia com consignado priorize crédito INSS, portabilidade e refinanciamento (CREDITO_INSS) e se for servidores públicos da ativo ou aposentados priorize CREDITO_SERVIDORES
  
Após criar a descrição do Text Classifier referente Category "CREDITO_SERVIDORES", escrevas todas as "Category" e suas respectivas descrição no novo contexto com todas as classificações:
    - ANTECIPACAO_FGTS
    - CREDITO_DO_TRABALHADOR
    - CREDITO_BOLSA_FAMILIA
    - CREDITO_INSS
    - CREDITO_SERVIDORES

Verifique se possui ambiguidades nas instruções que possam causar problema de interpretações para classificar
Otimize as instruções ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade


--------------- Text Classifier detectar INSS --------------------------

Crie uma descrição para LLM que atua em "Category" para node Text Classifier do n8n classificar e detectar interesse em crédito INSS, portabilidade e refinanciamento.
Faça um pesquisa profunda na internet para descobrir como as pessoas comuns solicitam este tipo de crédito para as financeiras via atendimento de whatsapp ou outros tipos de atendimento.
Contexto:
 - Os dados chegam via conversa de whatsapp e precisam ser classificados pelo node Text Classifier
 - Já existe as seguintes "Category" e sua descrição para model LLM no node Text Classifier do n8n:
  - ANTECIPACAO_FGTS: 
      - Termos diretos: "FGTS", "Fundo de Garantia", "saque aniversário", "antecipação FGTS", "empréstimo FGTS"
      - Variações: "consignado FGTS", "garantia FGTS", "crédito FGTS", "adiantamento saque"
      - Contextos específicos: "aniversário do FGTS", "liberar FGTS", "usar FGTS como garantia"
      - Siglas relacionadas: "modalidade aniversário"
  - CREDITO_DO_TRABALHADOR:
      - Termos diretos: 
      - Contextos CLT: "trabalho de carteira assinada", "empregado CLT", "funcionário registrado", 
      - Variações: , "crédito do trabalhador" "credito clt"
      - IMPORTANTE: Se mencionar FGTS junto com consignado, priorize sempre "CLT"
  - CREDITO_BOLSA_FAMILIA:
    - Termos diretos: "Bolsa Família", "consignado Bolsa", "empréstimo Bolsa Família", "Auxílio Brasil"
    - Variações populares: "empréstimo do benefício", "usar o benefício pra empréstimo", "crédito do auxílio", "consignado do programa", "empréstimo no auxílio"
    - Siglas: "BF", "consignado BF"
    - Contextos: "recebo Bolsa Família", "sou beneficiário", "tenho o auxílio", "cadastrado no programa", "desconta do benefício"
    - Menções indiretas: "governo me paga", "benefício social", "auxílio do governo", "CadÚnico"
    - IMPORTANTE: 
      - Se mencionar FGTS → priorize "ANTECIPACAO FGTS"
      - Se mencionar CLT/carteira assinada → priorize "CREDITO DO TRABALHADOR"
      - Bolsa Família isolado ou com "consignado genérico" → classifique "CREDITO BOLSA FAMILIA"

A partir do contexto fornecido faça o mesmo com a "Category": CREDITO_INSS 
Na instrução "IMPORTANTE, refaça com as seguintes alterações:
    - Se mencionar FGTS com consignado priorize crédito INSS, portabilidade e refinanciamento (CREDITO_INSS)
    - Se mencionar Bolsa familia com consignado priorize crédito INSS, portabilidade e refinanciamento (CREDITO_INSS)
  
Após criar a descrição do Text Classifier referente Category "CREDITO_INSS", escrevas todas as "Category" e suas respectivas descrição no novo contexto com todas as classificações:
    - ANTECIPACAO_FGTS
    - CREDITO_DO_TRABALHADOR
    - CREDITO_BOLSA_FAMILIA
    - CREDITO_INSS

Otimize as instruções ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.

:::::::::::::::::::::::::::::::::::: Bolsa Família  :::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

--------------- Text Classifier detectar bolsa família ChatGPT --------------------------

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
