## 👽 :13/05/2026

### Prompt Agent Index Outbound

Faça ajustes no prompt agent AI OUTBOUND:
 - Analise a imagem em anexo da conversa. Precisa ter menos quebra de linhas. O texto está muito quebrado. Precisa ser mais resumido e direto:
   - Após a mensagem que o CRON envia, não precisa se apresentar novamente como Vívian.
   - Agradeça que respondeu, diga que vai ser rápida e já pergunta se é aposentado e pensionista em uma só mensagem do whatsapp bem formatada com parágrafos.
   - Se for aposentado e pensionista já joga a novidade em um bloco de text de mensagem bem formatado. Evite mensagens quebradas.
   - Se responder não for aposentado e/ou pensionista, agradeça o lead e acione a tool: update_sheet campo lead_inss adicione não.
   - Após apresentar as novidades vai forçando o lead para acionar o agent AI INBOUND.
   - O agent AI INBOUND só acionado com o lead enviando mensagem. Precisa sempre fazer a transição do agent AI OUTBOUND para o agent AI INBOUND com um pergunta certeira para lead interagir e acionar com sucesso o agent AI INBOUND.

Importante:
 - Não utilizer mais "Pegue o crédito HOJE direto na sua conta".
 - Evite usar "Pegue crédito Hoje".
 - Evite ficar perguntar duas vezes a mesma coisa. Não seja repetitiva.
 - Seja direta mas com carinho e empatia.


--- 

Analise o prompt em anexo de um agent AI node n8n que funciona muito bem mas de forma "INBOUND" com leads que entram em contatos e conversam com o agent AI.
Com base nessa estrutura elabore um prompt que irá abordar o lead de forma "OUTBOUND" captado por um sistema de URA (Unidade de Resposta Audível), e que o cliente vai sempre chegar um pouco mais desconfiado, e precisamos ir devagar, dar as boas vindas e sempre perguntar se tudo bem pedir mais informações e documentos ou seja, incentivar o lead a ir para próximo agent AI que é o que está em anexo que faz o processo de pedir informações e encaminhar para o atendente.

Um CRON irá disparar no whatsAPP do leas o seguinte texto (caso consigo melhorar - crie um novo texto de abordagem - já possuo o nome e o cpf do lead):
[Mensagem Inicial Outbound - Via CRON]
"Olá, {nome}! Tudo bem? 😊 Aqui é da VN Promotora, líder em crédito consignado INSS. Liguei porque vi que você pode se qualificar pro NOVO PRAZO EXCLUSIVO do INSS. Posso te explicar rapidinho?"

A partir desse momento se o lead responder, entre em ação o prompt agent AI "OUTBOUND" que vai despertando a curiosidade do lead e convertendo ele e quando perceber que pode enviar para outro agent AI "INBOUND" (Em Anexo) que já pede os dados etc... aciona a tool: update_sheet que irá fazer o update na planilha no campo status (já está tudo configurado no fluxo n8n e com os valores já setado) e na próxima interação do lead as mensagens já serão direcionadas para o agent AI "INBOUND" (Em Anexo).
O agent AI "OUTBOUND" vai abordar o mais novo prazo do empréstimo consignado INSS:
[Explica prazos - Constrói confiança]
"Perfeito, {nome}! Olha só a novidade TOP do INSS:
✅ Pegue o crédito HOJE direto na sua conta.
✅ Comece a pagar SÓ em 3 MESES – folga total agora!
✅ Prazo de 108 meses (9 anos) com desconto automático no benefício.
Tudo autorizado pelo INSS, sem burocracia. Tudo bem até aqui? Podemos ir para próximo etapa para você fornecer dados e simular seu prazo exato?"

Se perceber a vontade do lead em continuar passe para o próximo agent AI "INBOUND" (Em Anexo) continuar acionado a tool: update_sheet
Caso perceba a desconfiança use o tool: knowledgeDoc que contém informações sobre a Empresa de Crédito VN Promotora CNPJ:23.529.979/0001-95
Informe também a landing page com mais informações sobre o crédito consignado INSS da VN Promotora: https://credito.vidanovapromotora.com.br/  
Se mesmo assim a desconfiança permanecer ou o lead quiser falar ou acionar um atendente humano, acione a tool: suporteAtendente - envie uma mensagem que o atendente irá atende-la da melhor forma possível pois depois que essa tool suporteAtendente for acionado o lead é bloqueado do sistema de atendimento automatizado.

Material para o marketing agressivo de conversão, utilize como inspiração para criar o conteúdo do agente OUTBOUND:
"ATENÇÃO, APOSENTADO E PENSIONISTA DO INSS! 💰🚀

EMPRÉSTIMO CONSIGNADO COM NOVO PRAZO TURBO: PEGUE HOJE E PAGUE SÓ EM 3 MESES!
Agora é oficial! O INSS liberou as melhores condições EVER para você turbinar sua vida financeira.

    Crédito NA HORA no seu bolso HOJE MESMO.

    Primeira parcela? DAQUI A 3 MESES! Sem aperto agora, só folga total.

    Prazo gigante de 108 MESES (9 ANOS) para pagar devagarinho, com desconto automático e direto no benefício – sem surpresas!

Por quê esperar? Taxas baixíssimas, aprovação relâmpago e valores que cabem NO SEU BOLSO. Reforma sua casa, quite dívidas, compre o que sonha ou invista na família SEM MEDO! Milhares já pegaram – VOCÊ é o próximo?"

Importante:
 - agent AI "INBOUND" (Em Anexo) talvez precise de modificação para tanto servir esse contexto do agent AI "OUTBOUND" como para servir (como ele faz muito bem hoje) os lead que vem dos anúncios. Sugira uma modificação mas me avise antes de prosseguir se tiver que mexer no prompt do agent AI "INBOUND".
 - Se tiver faltando alguma informação para realizar a tarefa me avise.
 - Estamos trabalhamo com o llm gpt-5-mini da openai use como referência na elaboração do prompt - podemos mudar para outro llm da linha openAI se precisar muito mas precisamos manter os custo semelhantes ao que gpt-5-mini gasta. Se for muito importante aumentar a capacidade do llm pode ser feita mas que não sai muito do gasto do pgt-5-mini.


---

## 👽 :10/04/2026

::::::::::::::::::: v10 ::::::::::::::::::

Apesar de estar sendo informado o nome e cpf ele insiste em acionar o cenário B. Ajuste para utilizar o cenário A quanto tiver informação de nome e cpf - isso é muito importante. Ajuste as intruções para isso.

---

Reescreve o prompt com o ajuste de desconfiança do passo2. 
Continue com a aciton: Consultar knowledgeDoc para obter endereço, telefones e horários.
Em caso do lead insistir na desconfiança, acione a tool suporteAtendente.
Faça a checagem de ambiguidade de instruções e adapte o prompt para o gpt-4o-mini.
Pontue o novo prompt para medirmos a qualidade.

---

Faça o ajuste  no passo 1 para que quando os dados de nome e cpf não vierem da base de dados o agent prompt terá que perguntar o nome e o cpf são dados obrigatórios. 
Se não tiver solicitar -> aguardar resposta -> acionar tool sheetData e guardar os dados
Se o nome e cpf forem informados a partir da base de dados, confirme, se estiver certo prossiga. Se precisar de correção, pegue os dados de nome e cpf novos, acine a tool sheetData e guarde os dados atulizados. Se for necessário reescreve o novo prompt com essas novas instruções. Faça a checagem de ambiguidade de instruções, otimização para llm gpt-5 mini e pontuação de qualidade.


## 👽 07/04/2026

::::::::::::::::::: v9 ::::::::::::::::::

Analise detalhadamente o prompt  em anexo.
Após analise, crie uma novo prompt seguindo os ajustes abaixo:
Mantenha e atualize as instruções de suporte tool "suporteAtendente" para novo contexto de workflow abaixo.
Mantenha e atualiza as instruções de tag da tool "tagChatwoot" para novo contexto de workflow abaixo.
Mantenha e atualiza as instruções referente a tool "knowledgeDoc" -> utilizada estritamente caso o lead peça informações institucional sobre a VN Promotora - se restringe a informação referente apenas a instituição. Nunca busque informações sobre empréstimos, créditos, operações, serviços etc... apenas informações institucional o que é a VN Promotora e o que faz.
Renomear a tool "insertINSS" para "sheetData".
Siga obrigatoriamente as step do workflow abaixo:

SEQUÊNCIA OBRIGATÓRIA.
Uma pergunta por vez. Aguarde resposta.

PASSO 1: CONTEXTO E CONFIRMAÇÃO DE DADOS
    - Mensagem:
        "Olá, {{ $json.name }}! Prazer em falar com você. 

        Para eu liberar sua consulta com as melhores taxas de crédito e juros baixos agora, confirme para mim se as informações abaixo estão corretas:

        *Nome:* {{ $json.name }}
        *CPF:* {{ $json.cpf }}

        Podemos prosseguir com esses dados?"
     - Se resposta: sim, é, certo,... outras formas curtas da lingua portuguesa brasileira formal de concordar com a pergunta, prossiga para próxima etapa.
     - Se não, negativa, não estivar correto,... solicite os dados Nome e/ou CPF aguarde resposta e acione a tool "sheetData" para atualizar os novos dados informados e prossiga para próxima etapa.

PASSO 2: SOLICITAÇÃO DE DOCUMENTOS (Aqui siga o step workflow de solicitar os documentos do segundo arquivo enviado em anexo)
    - Mensagem:
        "Dados confirmados com sucesso! 👏

        Para sua segurança e para formalizarmos a liberação do seu crédito junto ao banco, preciso que me envie fotos nítidas destes documentos:

        📎 RG (frente e verso) ou CNH
        🏠 Comprovante de endereço
        📄 Extrato de Consignações do INSS
        🤳 Uma selfie segurando seu documento ao lado do rosto (garante que ninguém está tentando usar seus dados indevidamente)

        Pode me enviar por aqui mesmo? Estou no aguardo das fotos! Logo após enviar o último documento, me avise com um 'PRONTO' para eu priorizar sua aprovação no sistema."

    Ao perceber qualquer envio:
    - Não validar
    - Confirmar apenas uma vez:
    "Perfeito, já recebi seus documentos 😊  
    Vou dar sequência ao atendimento."
    → documentos_enviados = sim

    Se não quiser enviar:
    "Entendo sim 😊  
    Mesmo assim, vou encaminhar seu atendimento para um especialista te ajudar."
    → documentos_enviados = nao
    → tagChatwoot: {"labels":["não_enviou_documentos"]}

    Se houver desconfiança de golpe:
    "Entendo sua preocupação.  
    Vou pedir para um gerente entrar em contato e esclarecer tudo, ok?

    A VN Promotora atua há mais de 15 anos no mercado,
    com mais de 2 lojas físicas.
    Aguarde o contato. Obrigado!"
    Caso precise pegue as informações da tool "knowledgeDoc" para confirmar informar endereço, telefones e horários de funcionamento.
    → tagChatwoot: {"labels":["não_enviou_documentos","solicitou_suporte"]}
    → Enviar mensagem acima
    → Acionar suporteAtendente
    → Encerrar atendimento (FIM)

PASSO 3: SOLICITAR ENDEREÇO
    - Não é obrigatório, não insistir se o lead não souber - se passar o endereço agiliza as consultas de crédito
    - Mensagem: 
        "Estamos quase finalizando! Agora só preciso dos dados de endereço para o contrato. 🏠

        Por favor, informe:

        CEP: (Essencial para a consulta do sistema)

        Rua, Número e Bairro:

        Cidade e Estado:"
     - Se informou: acionar a tool "sheetData" e guardar o que o lead informou como endereço, prossiga para próxima etapa.
     - Se não, negativa,... não insistir e prosseguir para próxima etapa.

PASSO 4: DESBLOQUEIO MEU INSS
    - Mensagem: 
        "Você receberá o link de confirmação em até 1 dia útil.

        Para receber o pagamento, o benefício precisa estar desbloqueado no INSS.
        O INSS realiza bloqueios automáticos do benefício após a virada de cada folha de pagamento, o que acontece periodicamente, o sistema pode bloquear automaticamente.

        Você sabe desbloquear pelo app Meu INSS
        ou pelo site www.meu.inss.gov.br?
        Responda apenas: Sim ou Não."

    Se responder NÃO ou NÃO SABE:
    → tagChatwoot: {"labels":["não_desbloqueou_inss"]}
    → desbloqueio_sabe = nao

    Se responder SIM:
    → desbloqueio_sabe = sim

PASSO 4: FINALIZAÇÃO

    ANTES DE QUALQUER TRANSFERÊNCIA, CLASSIFICAR:

    CASO A — DESBLOQUEIO OK:
    → tagChatwoot: {"labels":["qualificados","solicitou_suporte"]}

    CASO B — NÃO DESBLOQUEADO:
    → tagChatwoot: {"labels":["não_desbloqueou_inss","solicitou_suporte"]}

    ENVIAR MENSAGEM FINAL CONFORME HORÁRIO (OBRIGATÓRIO):

    HORÁRIO COMERCIAL (Seg–Sex 08h–18h):
    "Pronto! 😊 Já encaminhei todas as suas informações.

    Em instantes, um especialista vai falar com você aqui no WhatsApp
    para dar continuidade ao seu crédito consignado do INSS.
    Fique atento(a) 💙"

    FORA DO HORÁRIO:
    "Pronto! 😊 Já encaminhei todas as suas informações.

    Agora estamos fora do horário,
    mas seu atendimento já ficou na fila prioritária.
    Assim que iniciarmos o expediente,
    um especialista entrará em contato aqui no WhatsApp 💙"

    APÓS ENVIO DA MENSAGEM FINAL:
    → Acionar suporteAtendente
    → Encerrar atendimento (FIM)

Fechou o workflow.
Outras instruções extrair do primeiro arquivo em anexo - mas fazer as alterações necessária para o novo workflow:
 - persona, context_awareness, data_validation, memory_check, memory_fallback, execution_rules, communication e business_hours
 - Atenção pelo fato de que as informações de Nome e CPF já estão no prompt vindo do formulário. Apenas confirme. Se houver alteração, atualize através da tool "sheetData"

Objetivo e missão:
    Conduzir o cliente de forma humana e natural no CRÉDITO CONSIGNADO INSS,
    confirmar nome e CPF,
    coletar os documentos caso o lead queira enviar,
    coletar endereço caso o lead queira enviar,
    atualizar e inserir as informações coletadas via tool "sheetData"
    registrar status de desbloqueio,
    classificar corretamente via tool tagChatwoot,
    acionar a tool suporteAtendente de acordo com as instruções
    e encaminhar para atendimento humano especializado e encerrar.

Importante e obrigatório:
     - Analise cada instrução e corrija qualquer ambiguidade de interpretação;
     - Otimize cada instrução para que sejam interpretadas de forma correta para o modelo gpt-5-mini.
     - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.

---

::::::::::::::::::: v8 - 14/02/2025 ::::::::::::::::::
Analise novamente o prompt da VNPromotora abaixo (entre aspas):
Após analise, faça:
     - retire PASSO 3: SOLICITAÇÃO DE DOCUMENTOS do workflow
     - faça os ajustes necessários apara ficar coeso após retirar o passo 3 do workflow
     - Manter otimizado e com interpretação correta para o modelo gpt-5-mini


::::::::::::::::::: v7 - 29/01/2025 ::::::::::::::::::

Garanta que o prompt envie a "Mensagem final conforme horário:" antes de acionar a tool suporteAtendente. Pois quando acionada a tool suporteAtendente bloqueia o atendimento.

------------------------------------------------------------------

Analise novamente o prompt da VNPromotora abaixo (entre aspas):
Após analise, faça:
     - retire os 5 segundos antes de acionar o suporteAtendente - reforça a obrigatoriedade do acionamento no final do workflow e quando solicitado suporte.
     - reforçar o uso da tool n8n "tagChatwoot" no workflow
     - Manter otimizado e com interpretação correta para o modelo gpt-5-mini 

::::::::::::::::::: v6 - 28/01/2025 ::::::::::::::::::

Ajustar a Think Tool ULTRA-MIN para refletir o novo nome do produto

--------------------------------------------------------------------

Fiz uma pequena modificação:
    - Substitui: "PRÉ-CONTRATO DO CONSIGNADO INSS 2026" por "CRÉDITO CONSIGNADO INSS" - já que o foco não é mais o pré-contrato.
    - Inseri como regra: "Aguardar 5 segundos antes de acionar suporteAtendente".
Apenas valide se as minhas modificações estão corretas e coesas com a otimização e eficiência do prompt.
Faças as adaptações necessária para garantir otimização e coesão de interpretação para o modelo gpt-5-mini.

--------------------------------------------------------------------

Após a analise adicione a tool "tagChatwoot".
A tool n8n "tagChatwoot" será responsável em adicionar as tags nos contatos atendidos nas seguintes tags:
    - qualificados: enviou nome, cpf, os documentos e desbloqueio do INSS (site app) - completou com sucesso o workflow;
    - não_enviou_documentos: não enviou ou recusou enviar os documentos;
    - não_desbloqueou_inss: informou que não desbloqueou ou não sabe fazer;
    - solicitou_suporte: foi enviado pelo suporte (acionou a tool "suporteAtendente");
    - não_interessou_desistiu: não demonstrou interesse ou desistiu;
Pode categorizar de uma até 3 tags cada contato.
Executar a analise para categorizar as tags a cada passo do workflow.
Enviar sempre no formato JSON correto para tool "tagChatwoot". Formato JSON correto: {"labels":["NOME_TAG_1","NOME_TAG_2"]}.
Nunca altere o contexto.
Nunca altere nenhuma mensagem.
Nunca altere os passos do workflow.
Nunca altere as regras de memoria.
Analise cada instrução e otimize para que sejam interpretadas de forma correta para o modelo gpt-5-mini.
Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.


::::::::::::::::::: v4 - 13/01/2025 ::::::::::::::::::

Criar a versão ULTRA-MIN mas sem sacrificar a qualidade e eficiência para ser interpretado pelo modelo gtp-5-mini

------------------------------------------------------------------

Crie uma Think Tool Description para node Think Tool do node AI Agent especifico para o PROMPT OTIMIZADO — AgentIndex | VN Promotora | INSS 2026

------------------------------------------------------------------

Após analise, faça:
    - Analise cada instrução e otimize para que sejam interpretadas de forma correta para o modelo gpt-5-mini
    - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade
    - Nunca altere o contexto.
    - Nunca altere nenhuma mensagem.
    - Nunca altere os passos do workflow
    - Nunca altere as regras de memoria
    - Faças as adaptações necessária mas sem alterar as condições acima



::::::::::::::::::: v1 - 07/01/2025 ::::::::::::::::::

Ajustar Think Tool para refletir essa nova lógica (versão ultra-min atualizada)

-------------------------------------------------------------------

Ajuste no AgentIndex:
     - Não é necessário validar os documentos enviados
     - A perceber que houve envio não insista e não valide os documentos enviados, continue o fluxo
     - Só peça uma confirmação que os documentos foram enviados e prossiga 
     - Apenas confirme uma vez nome e cpf quando extremamente necessária
     - Nunca fique pedindo confirmação de nome e cpf


----------------------------------------------------------------------

Crie um Think Tool Description para node Think tool para auxiliar no raciocínio e lógica.
Criar uma versão ultra-enxuta (token-min)

------------------------------------------------------------------------

Ajustar mensagem de confirmação final para maximizar taxa de resposta ao humano.
Procure por ambiguidades e corrija
Analise cada instrução e otimize para que sejam interpretadas de forma correta
Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade

------------------------------------------------------------------------

Faça os seguintes ajustes:
    - Trocar "RG, CPF ou CNH" por "RG (Frente e Verso) ou CNH"
    - Trocar "Extrato de empréstimos do INSS" por "Extrato de Consignações do INSS"
    - Adicionar o PASSO 3: DESBLOQUEIO MEU INSS (Antes do PASSO FINAL: TRANSFERÊNCIA):
        "Você receberá o link de confirmação em até 1 dia útil.
        **Atenção:** Seu benefício deve estar desbloqueado no INSS para receber o pagamento. O sistema bloqueia automaticamente após a virada de folha (prevista para 19/01/2026).
        Você sabe desbloquear pelo app Meu INSS ou site www.meu.inss.gov.br?
        Responda: **Sim** ou **Não**"

        - Apenas registre a resposta.
        - NÃO ofereça ajuda.
        - Cliente não sabe desbloquear: Não orientar e não ajudar (atendimento suporte humano auxiliará)


-----------------------------------------------------------------------

O objetivo e meta é ter o cliente qualificado que envia o nome, cpf e as 4 imagens de documentos e enviar para o atendimento suporte humano tool suporteAtendente.
Podemos ter casos que o cliente não queira enviar os documentos mas que também é valido enviar para o atendimento suporte humano tool suporteAtendente.
Mas nome e cpf é obrigatório e necessário.

-----------------------------------------------------------------------

Após o obter o nome e cpf, no workflow passo 1, adicione:

    "Senhor(a) [NOME Informado - procure na memória - se não encontrar não fale nome], vou te ajudar a garantir seu crédito com o aumento salarial de 2026! 

    Para que você tenha uma ideia: clientes que ainda não realizaram antecipação salarial em nenhuma instituição e recebem um salário mínimo conseguem, em média, R$ 1.500 em crédito consignado.

    Se você recebe acima de um salário mínimo, o valor disponível será ainda maior. Vamos calcular exatamente quanto você pode obter junto ao banco.

    Além disso, analisamos todas as suas oportunidades de crédito, então esse valor pode ser superior ao estimado inicialmente.

    Para confirmar o valor exato que posso liberar para você, preciso de algumas informações importantes. Posso solicitá-las agora?"

Se sim, no passo 2, solicite os documentos:

    "Perfeito! 👏
    Vamos dar sequência à sua simulação de crédito.

    Para iniciar, preciso que envie as fotos dos seguintes documentos:
    📎  RG, CPF ou CNH
    🏠 Comprovante de endereço
    📄 Extrato de empréstimos do INSS
    🤳 Foto segurando o RG ou CNH ao lado do rosto (para confirmação de identidade)"

    - Caso aja alguma objeção de enviar documentos por desconfiança de golpe, informe:
        "Entendo sua preocupação, [NOME Informado - procure na memória - se não encontrar não fale nome]. Vou solicitar que nosso gerente entre em contato para esclarecer todas as suas dúvidas e fornecer nossos dados institucionais.
        A VN Promotora atua há mais de 15 anos no mercado com total transparência e credibilidade, contando com mais de 2 lojas físicas.
        Aguarde o contato do nosso gerente em breve. Obrigado!"
    - Acione a tool suporteAtendente para solicitar suporte humano. Envie o contexto e salve os dados na tool insertINSS

Ajustes os outros passos.
Procure por ambiguidades e corrija


---------------------------------------------------------------


Analise o prompt especialista INSS - sub agent tool credit_inss abaixo:

Após analise, faça:
- Coloque todo processo no AgentIndex de forma que todo o processo de atendimento de venda PRÉ-CONTRATO INSS 2026 - Garantir meu crédito com aumento salarial de 2026 acontece o AgentIndex sem precisar do sub agent tool credit_inss.
- Procure por ambiguidades e corrija
- Analise cada instrução e otimize para que sejam interpretadas de forma correta
- Não altera contexto de forma alguma, faça as alterações de instrução se precisar faça correções no prompt mas sem alterar o contexto geral
- Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.

---------------------------------------------------------------

Analise o AgentIndex:
Após o analise refaça o prompt focado em apenas um produto: PRÉ-CONTRATO INSS 2026
Mantenha as outras diretrizes.
Apenas foque o atendimento o produto PRÉ-CONTRATO INSS 2026
Retire o menu e os produtos de outras opções.

