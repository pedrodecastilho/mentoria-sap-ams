# Documento de Especificação Funcional - Atividade 002

- ID da Demanda: AMS-MENTORIA-002
- Módulo: Cross-Module (Conceitos ERP)
- Prioridade: Alta
- Assunto: Contextualização do Ecossistema SAP do Ponto de Vista Funcional

## Pesquisa Conceitual

1. **O que é um mandante (client) no SAP e por que ele existe?**

O mandante é o nível máximo na hierarquia de dados no SAP. Ele é usado para separar dados, configurações e usuários. Na prática, o mandante é um campo chave existente nas tabelas do banco de dados do SAP. Funciona como um "ambiente isolado" dentro do mesmo sistema físico.

O principal objetivo é segmentar os dados, permitindo múltiplas organizações no mesmo sistema físico, evitando instalar sistemas separados ou duplicação de administração e infraestrutura. Também permite a divisão de ambientes como desenvolvimento, teste e produção, e personalizações específicas para atender às necessidades de cada empresa.

2. **O que diferencia uma transação de um programa no SAP?**

Uma transação é um código que funciona como um atalho de navegação para alguma funcionalidade no SAP.  Já um programa é um código desenvolvido em linguagem ABAP que executa a lógica por trás dessa funcionalidade.

3. **O que é o conceito de documento no SAP — por que quase tudo no SAP gera um documento?**

Um documento representa uma transação de negócio, e registra toda a operação para manter a rastreabilidade e garantir auditoria.  Todo evento gera um documento que não pode ser facilmente alterado, garantindo a segurança do sistema.

Um processo registrado em um módulo pode disparar lançamentos em outros. Por exemplo, a entrada de mercadoria no módulo MM pode gerar um documento de material, e em seguida, um documento contábil no módulo FI.

## Exploração do Sistema

**Acesse o SE11 e explore as tabelas abaixo. Para cada uma, anote: o que ela armazena, quais são os 3 campos que você acha mais importantes e por quê.**

- **KNA1**: Tabela de cadastro de clientes.
  - KUNNR: É o número que identifica o registro do cliente;
  - NAME1: Registra o nome do cliente que é o mais visível no sistema;
  - LAND1: Registra o país do cliente que define as regras de impostos.

- **LFA1**: Tabela de dados de fornecedores.
  - LIFNR: É o número que identifica o registro do fornecedor;
  - NAME1: Registra o nome do fornecedor que é o mais visível no sistema;
  - LAND1: Registra o país do fornecedor que afeta regras de impostos.

- **MARA**: Tabela de dados de materiais.
  - MATNR: É o número que identifica o registro do material;
  - MTART: Registra o tipo do material e define regras de uso;
  - MBRSH: Registra o setor industrial e influencia na sua classificação.

- **VBAK**: Tabela de cabeçalho de documentos de vendas.
  - VBELN: É o número que identifica o documento e auxilia na localização;
  - AUART: Registra o tipo de documento de vendas, ou seja, define a natureza comercial do documento;
  - VKORG: Registra a organização de vendas, ou seja, a unidade responsável por vender materiais e serviços.

- **BKPF**: Tabela de cabeçalho do documento contábil.
  - BUKRS: Registra em qual empresa o documento foi lançado;
  - BELNR: Identifica o número do documento contábil e faz a ligação com as tabelas de itens;
  - GJAHR: Indica o exercício fiscal do documento para a apuração contábil.

## Desafio de Integração

**Com base na exploração do sistema, como o pedido se liga ao cadastro completo desse cliente?**

O cliente 1005 está registrado na tabela KNA1. O pedido de venda foi criado para este cliente, e registrado na tabela VBAK. O campo que liga as duas tabelas é o KUNNR. Na tabela KNA1 ele é chave primária, que identifica o registro. Já na tabela VBAK ele é chave estrangeira, que faz referência a um cliente específico naquele documento de venda.

## Referências

1. CLEVERENCE. **SAP tutorial: mastering SAP step by step**. Disponível em: [https://www.cleverence.com/articles/sistemas-erp-pt/sap-tutorial-mastering-sap-step-by-step-8293746/](https://www.cleverence.com/articles/sistemas-erp-pt/sap-tutorial-mastering-sap-step-by-step-8293746/). Acesso em: 19 maio 2026.
2. PRIME INSTITUTE. **Cómo encontrar el código de transacción de un programa en SAP de forma fácil**. Disponível em: [https://www.primeinstitute.com/preguntas/como-encontrar-o-codigo-de-transacao-de-um-programa-no-sap-de-forma-facil-3394](https://www.primeinstitute.com/preguntas/como-encontrar-o-codigo-de-transacao-de-um-programa-no-sap-de-forma-facil-3394). Acesso em: 19 maio 2026.
3. PRIME INSTITUTE. **Guía para crear transacciones en SAP: tipos y pasos**. Disponível em: [https://www.primeinstitute.com/preguntas/guia-para-criar-transacoes-no-sap-tipos-e-passos-5082](https://www.primeinstitute.com/preguntas/guia-para-criar-transacoes-no-sap-tipos-e-passos-5082). Acesso em: 19 maio 2026.
4. SAP. **Criar transações**. Disponível em: [https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE_UPA/931938cf67364678b896bac72a28bc3d/3e46d953189a424de10000000a174cb4.html?locale=pt-BR](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE_UPA/931938cf67364678b896bac72a28bc3d/3e46d953189a424de10000000a174cb4.html?locale=pt-BR). Acesso em: 19 maio 2026.
5. SAP. **Transações no SAP**. Disponível em: [https://help.sap.com/doc/saphelp_snc70/7.0/en-US/5d/a9463c288dbc5de10000000a11402f/content.htm](https://help.sap.com/doc/saphelp_snc70/7.0/en-US/5d/a9463c288dbc5de10000000a11402f/content.htm). Acesso em: 19 maio 2026.
6. SAP. **Aplicativos e transações SAP S/4HANA Cloud**. Disponível em: [https://help.sap.com/docs/SAP_S4HANA_CLOUD/32da8359c8ee4e8b8e8c5e15cacba5aa/b19bce0a4e5f4256b101ed2be62fa94b.html?locale=pt-BR](https://help.sap.com/docs/SAP_S4HANA_CLOUD/32da8359c8ee4e8b8e8c5e15cacba5aa/b19bce0a4e5f4256b101ed2be62fa94b.html?locale=pt-BR). Acesso em: 19 maio 2026.
