::::::::::::::::::: v3- 17/12/2025 ::::::::::::::::::
Vou explicar o contexto. Temos uma atendimento feito por IA com automação n8n. No n8n existe a tool "AI Agent Tools" e nela podemos conectar uma "sub-tool agent IA" também. No nosso contexto temos a tool "AI Agent Tools" que possui o nome de "AgentIndex", segue o prompt da "AgentIndex":

Conectada no "AI Agent Tools" de nome "AgentIndex" acima, está o "sub-tool agent IA" de nome "credit_inss", segue o código xm abaixo:

-----------------------------------------------------
Apenas atualize as instruções do "AgentIndex" para que quando chegar a frase "Olá, quero fazer o meu pré-contrato do consignado INSS, pra receber primeiro quando liberar" confirme nome e cpf e envie para o "sub-tool agent IA" "credit_inss"


::::::::::::::::::: v1 - 12/112/2025 ::::::::::::::::::

Analise o prompt enviado de atendimento n8n node AI de nome "AgentIndex" responsável por estabelecer o crédito de interesse do cliente e redirecionar para tool especifica.
Após analise, faça:
     - Faça adaptações para o que o "AgentIndex" funcione perfeitamente com as novas alterações do sub-agente credit_inss
     - Em "Qual crédito te interessa?" coloque em primeiro o produto em destaque "Limpa Nome"
     - Busque informações na tool "knowledgeDoc" para passar informações ao cliente sobre o produto "Limpa Nome"
     - Após passar informações sobre o produto "Limpa Nome", quando solicitado, pergunta se possui interesse, em caso afirmativo, aciona a tool suporteAtendente
     - Procure por ambiguidades e corrija
     - Analise cada instrução e otimize para que sejam interpretadas de forma correta
     - Não altera contexto de forma alguma, faça as alterações de instrução se precisar faça correções no prompt mas sem alterar o contexto geral
     - Otimize o prompt ao máximo objetivando o melhor custo/benefício de tokens mas sem sacrificar a qualidade.
