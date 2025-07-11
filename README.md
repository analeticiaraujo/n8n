# n8n
README das Automações n8n
Este README fornece uma visão geral e instruções sobre como as automações n8n neste repositório estão organizadas e como podem ser utilizadas.

O que é n8n?
n8n é uma ferramenta de automação de fluxo de trabalho de código aberto que permite conectar APIs, serviços online e bancos de dados para automatizar tarefas repetitivas. Ele usa um editor visual baseado em nós, tornando a criação de automações acessível mesmo sem conhecimento aprofundado em programação.

Estrutura do Repositório
Este repositório contém arquivos .json que representam os workflows (fluxos de trabalho) exportados do n8n. Cada arquivo JSON é uma automação completa que pode ser importada diretamente para sua instância do n8n.

nome-do-seu-workflow-1.json: Breve descrição do que este workflow faz.

nome-do-seu-workflow-2.json: Breve descrição do que este workflow faz.

olx-imoveis-scraper.json: Este workflow realiza o scraping de anúncios de imóveis da OLX (especificamente em Piracicaba) e envia alertas por e-mail para anúncios que atendem a critérios específicos (ex: "Direto com o proprietário" e publicados nas últimas 24 horas).

Como Usar as Automações
Para utilizar qualquer um dos workflows contidos neste repositório, você precisará de uma instância do n8n rodando (localmente ou em um servidor).

1. Importar um Workflow
Abra sua instância do n8n no navegador.

No painel de navegação esquerdo, clique em "Workflows".

No canto superior direito, clique em "New" e selecione "Import from JSON".

Arraste e solte o arquivo .json desejado (ou copie e cole o conteúdo do JSON) e clique em "Import".

2. Configurar Credenciais (se necessário)
Muitos workflows do n8n dependem de credenciais para se conectar a serviços externos (ex: Gmail, ScraperAPI, etc.).

Após importar o workflow, verifique os nós que requerem credenciais (eles geralmente terão um ícone de alerta ou um campo de credenciais vazio).

Clique no nó em questão e, na barra lateral de propriedades, localize a seção "Credentials".

Clique em "Create new" ou selecione uma credencial existente.

Siga as instruções para configurar a nova credencial (ex: autenticação OAuth para Gmail, inserção de API Key para ScraperAPI).

Para o workflow olx-imoveis-scraper.json:

HTTP Request (ScraperAPI): Você precisará de uma chave de API do ScraperAPI. Substitua YOUR_SCRAPERAPI_KEY na URL por sua chave real.

Gmail: Configure uma credencial OAuth2 do Gmail. Certifique-se de que a conta de e-mail usada tenha permissão para enviar e-mails.

3. Ajustar Parâmetros
Alguns workflows podem ter parâmetros específicos que você talvez queira ajustar.

Schedule Trigger: Altere a frequência ou o horário de execução.

HTTP Request: Modifique a URL para fazer scraping de outras páginas ou ajustar parâmetros da API.

Code: O código JavaScript dentro do nó "Code" pode ser editado para ajustar a lógica de filtragem, o formato do e-mail, etc.

4. Ativar o Workflow
Depois de importar e configurar o workflow, você precisa ativá-lo para que ele comece a ser executado.

No canto superior direito da tela do workflow, alterne o botão "Active" para a posição "ON".

Contribuição
Sinta-se à vontade para propor melhorias, corrigir bugs ou adicionar novos workflows. Por favor, siga as boas práticas de Git ao fazer suas contribuições.

