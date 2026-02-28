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

