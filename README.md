Projeto de Exibição de Vídeos com Azure CosmosDB e Azure Functions

<div style="text-align: center;">
	<img src="https://img.shields.io/badge/.NET%208-333333?style=flat&logo=.net&logoColor=white" alt=".NET 8" />
	<img src="https://img.shields.io/badge/Azure-Functions-0078D7?style=flat&logo=azure-functions&logoColor=white" alt="Azure Functions" />
	<img src="https://img.shields.io/badge/Azure-CosmosDB-0078D7?style=flat&logo=microsoft-azure&logoColor=white" alt="Azure CosmosDB" />
	<img src="https://img.shields.io/badge/Azure-Storage_Account-0078D7?style=flat&logo=microsoft-azure&logoColor=white" alt="Azure Storage Account" />
</div>

# Visão Geral

Este projeto consiste em uma solução para upload, armazenamento e exibição de vídeos e thumbnails utilizando o Azure CosmosDB, Azure Storage e Azure Functions. O sistema é dividido em backend e frontend:

Backend: Implementado em C# com Azure Functions para manipulação de uploads e consulta de dados.

Frontend: Uma página HTML simples que consome as APIs para listar e exibir vídeos.

## Tecnologias Utilizadas

	Azure Functions: Para criação das APIs de upload e exibição.

	Azure CosmosDB: Para armazenar os metadados dos vídeos.

	Azure Storage Account: Para armazenar os arquivos de vídeo e thumbnails.

	HTML e CSS: Para o frontend.

	Visual Studio e Visual Studio Code: Para desenvolvimento e execução local.

## APIs Disponíveis

	1. FnPostDatabase

		Responsável por salvar os metadados no CosmosDB.

	2. FnPostStorage

		Responsável por fazer o upload dos vídeos e thumbnails no Azure Storage.

	3. FnGetAllMovies

		Lista todos os vídeos armazenados.

	4. FnGetMovieDetail

		Retorna os detalhes de um vídeo específico com base no id.

## Configurações para Execução

	Configuração do Ambiente Azure:

		Crie uma instância do Azure CosmosDB.

		Crie uma Storage Account para armazenar os arquivos.

		Configure as Azure Functions no portal do Azure para as quatro funções descritas.

	Adicione as configurações necessárias no arquivo local.settings.json.

## Execução Local:

	Abra o projeto no Visual Studio.
	
	Configure as funções FnGetAllMovies e FnGetMovieDetail para rodarem juntas.

	Certifique-se de que as dependências do projeto estão instaladas.

	Execução do Frontend:

	Coloque o arquivo api.html na raiz do projeto.

	Utilize um servidor local para rodar a página HTML. Exemplo:

	Use a extensão Live Server no Visual Studio Code.

	Acesse http://127.0.0.1:5500/api.html.

## Como Testar

	Upload de Arquivos:

		Utilize as APIs FnPostDatabase e FnPostStorage para realizar uploads de metadados e arquivos (vídeos e thumbnails).

	Listagem e Exibição:

		Acesse a página HTML.

		Confirme que os vídeos estão sendo listados corretamente com as thumbnails e títulos.

		Clique em um card para reproduzir o vídeo.

## Observações

	Certifique-se de que os endpoints das APIs FnGetAllMovies e FnGetMovieDetail estão configurados corretamente na página HTML.

	No Visual Studio, é possível configurar o Multiple Startup Projects para rodar as duas Azure Functions ao mesmo tempo.