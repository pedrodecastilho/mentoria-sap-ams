# Documento de Especificação Funcional - Atividade 001

- ID da Demanda: AMS-MENTORIA-001
- Módulo: Cross-Module (Conceitos ERP)
- Prioridade: Alta
- Assunto: Fundamentos do Ecossistema SAP e Processos de Negócio

## Requisitos de Pesquisa

1. **O que é um ERP? Qual a diferença entre o antigo SAP ECC e o atual SAP S/4HANA (foco no banco de dados HANA)?**

Um ERP (Enterprise Resource Planning) é um software que auxilia as organizações a otimizar processos de negócios. Apresenta uma visão unificada de todas as áreas da empresa, como finanças, vendas, armazenamento, logística, recursos humanos, etc. Muitos dos processos ocorrem de maneira independente, mas impactam todo o restante. Um sistema ERP oferece módulos integrados que compartilham o mesmo banco de dados, integrando informações entre os departamentos para atender às necessidades da empresa. O SAP é um dos softwares ERP mais utilizados no mundo.

A diferença principal entre o SAP ECC e o SAP S/4HANA está na arquitetura. Enquanto o SAP ECC pode ser utilizado com diferentes bancos de dados tradicionais, como Oracle ou Microsoft SQL Server. Já o SAP S/4HANA utiliza exclusivamente com o banco de dados HANA desenvolvido pela própria SAP. Este banco de dados é _in-memory_ e de estrutura colunar, o que traz vantagens como a melhoria da performance para execução de consultas com grandes volumes de dados, permitindo leitura e processamento direto na memória. Enquanto isso, o SAP ECC possui processamento mais lento, muitas vezes executando ações em lote.

Essa característica elimina a latência e permite que o S/4HANA execute análises e transações em tempo real no mesmo sistema. O impacto dessa nova arquitetura na realidade das empresas é que o ERP permite decisões mais rápidas e baseadas em dados atualizados. Na perspectiva do usuário, o SAP S/4HANA também traz novidades. Enquanto o SAP ECC oferece a interface gráfica clássica (SAP GUI), pouco intuitiva e restrita ao desktop, o S/4HANA traz uma inteface moderna (SAP Fiori), que pode ser acessada também via web/mobile.

2. **Os Quatro Pilares (Módulos): Qual é o propósito principal dos módulos FI (Financial Accounting), MM (Materials Management), SD (Sales and Distribution) e PP (Production Planning)?**

- FI (Financial Accounting / Contabilidade Financeira): Gerencia todas as operações financeiras e contáveis da empresa. Inclui contas a pagar e a receber, razão geral, ativos fixos, e consolidação financeira.
- MM (Materials Management / Gestão de Materiais): Controla compras, estoque e materiais. Inclui requisições e pedidos de compra, recebimento de mercadorias, controle de estoque, e gestão financeira.
- SD (Sales and Distribution / Vendas e Distribuição): Gerencia processos de vendas e relacionamento com os clientes. Inclui pedidos de venda, entrega e expedição, faturamento, e precificação e crédito. 
- PP (Production Planning / Planejamento de Produção): Ajuda a planejar e controlar processos de produção e manufatura. Envolve planejamento de demanda, ordens de produção, lista de materiais, e capacidade produtiva. 

3. **Processos Integrados: Entenda e explique os conceitos de Order-to-Cash (O2C - de Vendas) e Procure-to-Pay (P2P - de Compras). Como a informação flui de um setor para o outro?**

Order to Cash é o fluxo de processamento um pedido, desde o recebimento da solicitação do cliente até o recebimento do pagamento. Isso inclui a verificação da disponibilidade, expedição e entrega, faturamento e a baixa do recebimento. Costuma envolver principalmente os módulos de SD, FI e MM. A vantagem da integração entre os módulos SAP é a otimização do processo. Por exemplo, ao criar um pedido, o SD consulta o MM para verificar se há mercadoria disponível, e quando a mercadoria é entregue ao cliente, o sistema gera um movimento de retirada de estoque no MM, atualiza o saldo de estoque e gera um lançamento contábil em FI.

Procure to Pay é o ciclo integrado de compras desde a requisição até o pagamento ao fornecedor. Através deste processo, é possível gerenciar a ordem de compra, o recebimento da mercadoria, a fatura do fornecedor e a execução do pagamento. Envolve a integração entre os módulos MM e FI. Ao fazer um pedido, o SAP o envia automaticamente para aprovação, e em seguida encaminha para o fornecedor, acompanhando o processo de entrega e o recebimento, e por fim, gerencia o processamento do pagamento. 

## Entregáveis

1. **Crie um post para o seu blog: Resuma o que você aprendeu sobre a diferença entre o SAP ECC e o S/4HANA, e a importância de entender os processos de negócio (O2C e P2P) como desenvolvedor.**

[Iniciando a Carreira no SAP](https://dev.to/pedrodecastilho/iniciando-a-carreira-no-sap-2bih)

2. **Faça um diagrama: Um esboço simples (pode ser no papel, Miro ou Draw.io) do fluxo de um processo Procure-to-Pay. Compartilhe em um post do LinkedIn.**

[Conhecendo processos de negócio](https://www.linkedin.com/posts/pedrodecastilho_sap-p2p-procurement-share-7457526329404682240-ndpG)

## Referências

1. FORBES. **What Is SAP ERP?** Publicado em: 11 fev. 2024. Disponível em: [https://www.forbes.com/advisor/business/what-is-sap-erp](https://www.forbes.com/advisor/business/what-is-sap-erp). Acesso em: 29 abr. 2026.
2. FORMULA SAP. **SAP GUI vs SAP Fiori: comparação**. Disponível em: [https://formulasap.com.br/sap-gui-vs-sap-fiori-comparacao](https://formulasap.com.br/sap-gui-vs-sap-fiori-comparacao). Acesso em: 29 abr. 2026.
3. GURU99. **Módulos SAP**. Disponível em: [https://www.guru99.com/pt/sap-modules.html](https://www.guru99.com/pt/sap-modules.html). Acesso em: 29 abr. 2026.
4. GURU99. **Overview of SAP MM module**. Disponível em: [https://www.guru99.com/pt/overview-of-sap-mm-module.html](https://www.guru99.com/pt/overview-of-sap-mm-module.html). Acesso em: 29 abr. 2026.
5. MINDTEK. **Diferenças entre o SAP ECC e SAP S/4HANA**. Publicado em: out. 2023. Disponível em: [https://www.mindtek.com.br/2023/10/diferencas-entre-o-sap-ecc-e-sap-s-4hana](https://www.mindtek.com.br/2023/10/diferencas-entre-o-sap-ecc-e-sap-s-4hana). Acesso em: 29 abr. 2026.
6. PEERS. **Order to Cash (O2C)**. Disponível em: [https://peers.com.br/order-to-cash/](https://peers.com.br/order-to-cash/). Acesso em: 04 maio 2026.
7. PRIME INSTITUTE. **SAP FI: o módulo financeiro integrado do sistema SAP**. Disponível em: [https://www.primeinstitute.com/noticias/sap-fi-o-modulo-financeiro-integrado-do-sistema-sap-322](https://www.primeinstitute.com/noticias/sap-fi-o-modulo-financeiro-integrado-do-sistema-sap-322). Acesso em: 29 abr. 2026.
8. SAP. **O que é ERP?** Atualizado em: 26 jan. 2026. Disponível em: [https://www.sap.com/brazil/resources/what-is-erp](https://www.sap.com/brazil/resources/what-is-erp). Acesso em: 29 abr. 2026.
9. SAP. **O que é ciclo integrado de compras?**. Disponível em: [https://www.sap.com/brazil/resources/what-is-procure-to-pay](https://www.sap.com/brazil/resources/what-is-procure-to-pay). Acesso em: 04 maio 2026.
10. SAP - ABAP documentation. **O que é o módulo SAP SD – Vendas e distribuição**. Disponível em: [https://help.sap.com/docs/SUPPORT_CONTENT/abap/3353523547.html?locale=pt-BR&state=PRODUCTION&version=1.0](https://help.sap.com/docs/SUPPORT_CONTENT/abap/3353523547.html?locale=pt-BR&state=PRODUCTION&version=1.0). Acesso em: 29 abr. 2026.
11. SAP COMMUNITY. **SAP Order to Cash (OTC) process detailed explanation with real-time example**. Disponível em: [https://community.sap.com/t5/technology-blog-posts-by-members/sap-order-to-cash-otc-process-detailed-explanation-with-real-time-example/ba-p/14066523](https://community.sap.com/t5/technology-blog-posts-by-members/sap-order-to-cash-otc-process-detailed-explanation-with-real-time-example/ba-p/14066523). Acesso em: 04 maio 2026.
12. SAPINSIDER. **SAP Procure-to-Pay**. Disponível em: [https://sapinsider.org/topic/sap-spend-management/sap-procure-to-pay/](https://sapinsider.org/topic/sap-spend-management/sap-procure-to-pay/). Acesso em: 04 maio 2026.
13. WIKIPEDIA. **SAP S/4HANA**. Disponível em: [https://en.wikipedia.org/wiki/SAP_S/4HANA](https://en.wikipedia.org/wiki/SAP_S/4HANA). Acesso em: 29 abr. 2026.
