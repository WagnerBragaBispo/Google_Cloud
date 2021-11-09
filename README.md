# Google_Cloud
Anotações sobre o curso do Google Claud Skills Boost 2021. Iniciado em 05/11/2021


O que é o aprendizado de máquina? (AI Adventures) --> https://youtu.be/HcqpanDadyQ
Usuando dados para suas perguntas. O uso de dados para Training e as perguntas para Prediction. Dito por @YufengG canal do Goolge Cloud --> AI Adventures

Passo 1 --> Form Parsing Using Document AI

Visão geral

Como consumidores, estamos acostumados a preencher formulários para solicitar seguro, fazer reivindicações de seguro, especificar preferências de saúde, candidatar-se a empregos, retenções de impostos, etc. As empresas do outro lado dessas transações obtêm um formulário que precisam analisar e extrair pedaços específicos de dados de, e popular um banco de dados com.

Neste laboratório, você usará a solução Document AI do Google Cloud para analisar formulários em um Jupyter Notebook para que possa extrair automaticamente informações de formulários em papel digitalizados.
https://cloud.google.com/document-ai/docs/

Neste laboratório, você aprenderá a:

    Crie uma instância do Jupyter Notebook no Cloud AI Platform
    Crie uma conta de serviço para automatizar o processamento de formulários.
    Faça upload de um documento PDF para o Google Cloud Storage.
    Chame o Document AI.
    Analise a resposta usando funções de baixo nível com base no layout visual do formulário.
    Analise a resposta usando funções de alto nível com base na estrutura semântica do formulário.

O que você vai construir

Você vai analisar e usá-lo para analisar um formulário de divulgação de campanha que todas as campanhas políticas dos EUA devem arquivar. Desse formulário, você retirará o dinheiro que a campanha tem em mãos.
Configurar
Antes de clicar no botão Start Lab

Leia estas instruções. Os laboratórios são cronometrados e você não pode pausá-los. O cronômetro, que começa quando você clica em Iniciar laboratório, mostra por quanto tempo os recursos do Google Cloud ficarão disponíveis para você.

Este laboratório prático do Qwiklabs permite que você mesmo faça as atividades do laboratório em um ambiente de nuvem real, não em um ambiente de simulação ou demonstração. Ele faz isso fornecendo novas credenciais temporárias que você usa para fazer login e acessar o Google Cloud durante o laboratório.
O que você precisa

Para concluir este laboratório, você precisa de:

    Acesso a um navegador de Internet padrão (navegador Chrome recomendado).
    É hora de concluir o laboratório.

Observação: se você já tem sua conta ou projeto pessoal do Google Cloud, não o use para este laboratório.

Observação: se você estiver usando um Pixelbook, abra uma janela anônima para executar este laboratório.

Certifique-se de ler todas as instruções aqui e no Notebook Jupyter.
Implante o código em Notebooks do AI Platform

Abra este link em uma nova guia para implantar o código nos Notebooks do AI Platform. Siga o tutorial à direita para preencher os pré-requisitos necessários.
https://cloud.google.com/document-ai/docs/

Na página do AI Platform, altere o nome da instância para "formdemo".

Na seção Propriedades da instância, clique no ícone de edição (lápis) e, em seguida, role para baixo até Configuração da máquina e altere o tipo de máquina para n1-standard-2.

Clique no botão Criar.

Aguarde até que a instância do Jupyter Notebook seja criada e o notebook seja implantado. Isso levará cerca de 5 minutos.

O notebook deve abrir, mas se não, clique no link ABRIR para abri-lo.
Examinar documento

Na guia JupyterLab, clique em Editar> Limpar todas as saídas para limpar todas as células do bloco de notas.

Execute as primeiras 4 células do notebook.

    Clique em uma célula - a barra azul à esquerda mostra em qual célula você está trabalhando.
    Pressione o botão triangular executar células selecionadas ... na faixa superior ou pressione Shift + Enter para cada célula.

Essas células baixam um arquivo chamado scott_walker.pdf e usam a exibição IPython para exibir o arquivo PDF.

Clique no arquivo PDF e percorra-o para responder às duas perguntas a seguir:

Qual é o nome do comitê ao qual este formulário pertence? 





Link Google API: https://notebooks.googleapis.com
Link Google Vertex AI Workbench: https://cloud.google.com/vertex-ai/docs/workbench/user-managed?hl=pt_BR&_ga=2.111249293.-866833055.1636109651
Link Google Documentação AI: https://cloud.google.com/document-ai/docs/
Link Google Documentação Notebooks API: https://cloud.google.com/vertex-ai/docs/workbench/reference/rest?apix=true
Link Google Documentação Console do Google Cloud: https://cloud.google.com/vertex-ai/docs/workbench/user-managed/create-new?hl=pt_BR
Link Google Documentação Cloud Storage client libraries: https://cloud.google.com/storage/docs/reference/libraries?hl=pt_br
Link Tutorial # Google Cloud AI Notebook Tutorials: https://3741906741e829ae-dot-us-west1.notebooks.googleusercontent.com/lab/tree/tutorials/README.ipynb

https://www.cloudskillsboost.google/focuses/2794?locale=pt_BR&parent=catalog

