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

Google Cloud Essentials: 
Passo 1 ---> GSP282 A Tour of Google Cloud Hands-on Labs https://www.cloudskillsboost.google/focuses/3495?parent=catalog
https://www.cloudskillsboost.google/focuses/2794?locale=pt_BR&parent=catalog


Username: student-04-bad0da8fa959@qwiklabs.net
Senha: zNHPcWd993y
ID Projeto: qwiklabs-gcp-03-56e87d1fe127

Passo 2 ---> GSP001 Creating a Virtual Machine https://www.cloudskillsboost.google/focuses/8585?parent=catalog
    Roteiro:
        Crie uma máquina virtual com Cloud Console;
        Crie uma máquina virtual com a gcloud linha de comando
        Implante um servidor da web e conect-o uma máquina virtual
        P2.1 --> Incia o laboratorio/Copia os dados de Username, Password, GCP Project ID/realiza o Sing in com dados copiados/Aceite os termos e não adicione opções de recurações e de avaliações gratuitas/Ativa o Cloud Shell/Apoś Ativar o Terminal Linux podemos listar o nome da conta (provisória liberada pelo Google "quiklabs-gcp-...."); depois o ID do projeto; depois o seguinte comando:
 
   Username: student-04-bad0da8fa959@qwiklabs.net
   Senha: zNHPcWd993y
   ID Projeto: qwiklabs-gcp-03-da6bf22a156e

   P2.2 --> You can list the active account name with this command: gcloud auth list 
   P2.2 --> You can list the project ID with this command: gcloud config list project
    
   P2.3 Atenção para fixar o resultado do projeto utilize o mesmo "recurso zonal" ou seja a mesma instância da máquina virtual 

Passo 3 ---> GSP093 Compute Engine: Qwik Start — Windows https://www.cloudskillsboost.google/focuses/2?locale=pt_BR&parent=catalog

   Username: student-04-bad0da8fa959@qwiklabs.net
   Senha: zNHPcWd993y
   ID Projeto: qwiklabs-gcp-04-3467cca95faf
    P3.1 --> Começar o laboratório.>Abrir Console do Google> copiado do painel "Detalhes da conexão" > clique em Menu de navegação no canto superior esquerdo, ao lado de "Google Cloud Platform". > 
    P3.2 --> Crie uma instância de máquina virtual > Menu de navegação e clique em Compute Engine > Instâncias de VM e depois clique em Criar Instância.
    p3.3 --> Na seção Configuração da máquina, para Série selecione N1
    P3.4 --> Na seção Disco de inicialização, clique em Alterar para iniciar a configuração do disco de inicialização.
    P3.5 --> Escolha Windows Server 2012 R2 Datacenter e clique em Selecionar. Não altere as outras configurações.
    P3.6 --> No Terminal liste o nome da conta ativa com o seguinte comando
    
    gcloud auth list

p3.7 --> É possível listar o ID de projeto com este comando: (tiv problema neste passo, portanto verificar documentação: https://cloud.google.com/sdk/gcloud)

     gcloud config list project
	
p3.8 -->    Teste o status da inicialização do Windows, após instalar. Para verificar se ela está pronta para uma conexão RDP, execute o seguinte comando na linha de comando do terminal do Cloud Shell:
Plugin do Chrome > Chrome RDP for Google Cloud Platform: https://chrome.google.com/webstore/detail/chrome-rdp-for-google-clo/mpbbnannobiobpnfblimoapbephgifkm

    gcloud compute instances get-serial-port-output instance-1

p3.9 --> RDP no Windows Server: Para definir uma senha e fazer login no RDP, execute o comando a seguir no terminal do Cloud Shell, substitua [instance] pela instância de VM que você criou e defina [username] como administrador.   
   
    gcloud compute reset-windows-password [instance] --zone us-central1-a --user [username]

P3.10 --> Se aparecer a pergunta Would you like to set or reset the password for [admin] (Y/n)?, responda Y.
   
   Acesso RDP
   Nome do usuário: student_04_bad0da8fa
   senha



p3.11 -->

Copie e cole com o cliente do RDP

Depois de fazer login com segurança na sua instância, você encontrará os comandos para copiar e colar no manual do laboratório.

Para colar, pressione as teclas CTRL-V (CMND-V não funcionará para usuários do Mac). Se você estiver em uma janela do Powershell, precisa clicar nela antes de usar as teclas de atalho para colar.

Se você estiver colando no PuTTY, clique com o botão direito.


Google Cloud Essentials: 
Passo 1 ---> GSP093 Compute Engine: Qwik Start - Windows  https://www.cloudskillsboost.google/focuses/2?parent=catalog aprenda no Youtube https://www.youtube.com/watch?v=EFPaP20APuw

Passo 1.1 ---> GSP093 Vamos aprender sobre Remote Desktop Protocol (RDP) 

Username: student-04-bad0da8fa959@qwiklabs.net
Senha: zNHPcWd993y
ID Projeto: qwiklabs-gcp-02-e2df2887c854

Passo 2.0 ---> GSP093 Crie uma instância de máquina virtual
Passo 2.1 ---> GSP093 Série para N1 --> Altere o Boot disk para Windows Server
Passo 2.2 ---> GSP093 Ative o Google Cloud Shell com os comandos listados acima em passos superiores
Passo 3.0 ---> GSP093 Teste o status da conexão RDP com o seguinte comando: gcloud compute instances get-serial-port-output instance-1
Nota: ao testar a conexão aperece a msg: You don't have permission to edit the permissions of the selected resource 

    gcloud compute reset-windows-password [instance] --zone us-central1-a --user [username]
gcloud compute reset-windows-password instance-1 --zone us-central1-a --user student-04-bad0da8fa959@qwiklabs.net

IP 104.196.253.181 deu erro
IP 10.128.0.2 deu erro
IP 34.135.104.212
Usuário: student_04_bad0da8fa
Usuário: admin deu erro
