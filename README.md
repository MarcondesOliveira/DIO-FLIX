Projeto de Exibi��o de V�deos com Azure CosmosDB e Azure Functions

<div style="text-align: center;">
	<img src="https://img.shields.io/badge/.NET%208-333333?style=flat&logo=.net&logoColor=white" alt=".NET 8" />
	<img src="https://img.shields.io/badge/Azure-Functions-0078D7?style=flat&logo=azure-functions&logoColor=white" alt="Azure Functions" />
	<img src="https://img.shields.io/badge/Azure-CosmosDB-0078D7?style=flat&logo=microsoft-azure&logoColor=white" alt="Azure CosmosDB" />
	<img src="https://img.shields.io/badge/Azure-Storage_Account-0078D7?style=flat&logo=microsoft-azure&logoColor=white" alt="Azure Storage Account" />
</div>

# Vis�o Geral

Este projeto consiste em uma solu��o para upload, armazenamento e exibi��o de v�deos e thumbnails utilizando o Azure CosmosDB, Azure Storage e Azure Functions. O sistema � dividido em backend e frontend:

Backend: Implementado em C# com Azure Functions para manipula��o de uploads e consulta de dados.

Frontend: Uma p�gina HTML simples que consome as APIs para listar e exibir v�deos.

## Tecnologias Utilizadas

	Azure Functions: Para cria��o das APIs de upload e exibi��o.

	Azure CosmosDB: Para armazenar os metadados dos v�deos.

	Azure Storage Account: Para armazenar os arquivos de v�deo e thumbnails.

	HTML e CSS: Para o frontend.

	Visual Studio e Visual Studio Code: Para desenvolvimento e execu��o local.

## APIs Dispon�veis

	1. FnPostDatabase

		Respons�vel por salvar os metadados no CosmosDB.

	2. FnPostStorage

		Respons�vel por fazer o upload dos v�deos e thumbnails no Azure Storage.

	3. FnGetAllMovies

		Lista todos os v�deos armazenados.

	4. FnGetMovieDetail

		Retorna os detalhes de um v�deo espec�fico com base no id.

## Configura��es para Execu��o

	Configura��o do Ambiente Azure:

		Crie uma inst�ncia do Azure CosmosDB.

		Crie uma Storage Account para armazenar os arquivos.

		Configure as Azure Functions no portal do Azure para as quatro fun��es descritas.

	Adicione as configura��es necess�rias no arquivo local.settings.json.

## Execu��o Local:

	Abra o projeto no Visual Studio.
	
	Configure as fun��es FnGetAllMovies e FnGetMovieDetail para rodarem juntas.

	Certifique-se de que as depend�ncias do projeto est�o instaladas.

	Execu��o do Frontend:

	Coloque o arquivo api.html na raiz do projeto.

	Utilize um servidor local para rodar a p�gina HTML. Exemplo:

	Use a extens�o Live Server no Visual Studio Code.

	Acesse http://127.0.0.1:5500/api.html.

## Como Testar

	Upload de Arquivos:

		Utilize as APIs FnPostDatabase e FnPostStorage para realizar uploads de metadados e arquivos (v�deos e thumbnails).

	Listagem e Exibi��o:

		Acesse a p�gina HTML.

		Confirme que os v�deos est�o sendo listados corretamente com as thumbnails e t�tulos.

		Clique em um card para reproduzir o v�deo.

## Observa��es

	Certifique-se de que os endpoints das APIs FnGetAllMovies e FnGetMovieDetail est�o configurados corretamente na p�gina HTML.

	No Visual Studio, � poss�vel configurar o Multiple Startup Projects para rodar as duas Azure Functions ao mesmo tempo.