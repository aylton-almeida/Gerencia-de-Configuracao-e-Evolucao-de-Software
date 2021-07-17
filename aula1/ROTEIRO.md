# Aula 1 - Roteiro

Durante essa disciplina iremos desenvolver uma aplicação, essa sendo uma **API REST** utilizando **Typescript**, com o objetivo de passar por todos os pontos referenciados pela gerência de configuração de uma aplicação.

Também usaremos outra aplicação desenvolvida em **NextJS** a fim de visualizar e inserir dados da nossa **API**.

Para realização desse objetivo esse roteiro mostrará como fazer a **configuração de um computador** a fim de prepara-lo para as possíveis tarefas que serão realizadas. Também serão mostrados os primeiros passos para **executar as aplicações** com que trabalharemos.

Existem dois videos de apoio para essa aula:

- [**Configuração de um VM Windows:**](https://1drv.ms/v/s!Au3pZz4ON4ATmuEZJ4ksiheelHn0rA?e=ZflF6K)
- [**Configuração de um computador**](https://1drv.ms/v/!Au3pZz4ON4ATmuJEsVDnLl-SQrM-TA?e=XZiv8h)

## Configuração do NodeJS

O **NodeJS** é um _runtime_ de Javascript, sendo ele responsável por interpretar aplicações em JS a fim de roda-las em um servidor, por exemplo. Nesse curso a usaremos para executar nossas aplicações Web e APi. Para fazer a instalação do Node basta seguir os seguintes passos:

1. Acesse o **link** de download em seu [site oficial](https://nodejs.org/en/)  
   ![NodeJs Download Page](images/node/nodejs-site.png)

2. Ná página selecione a versão desejada. O Recomendado é utilizar a **última versão estável** (LTS), sendo essa a **14.17.3** no dia de escrita deste roteiro.  
   ![Download LTS Version](images/node/download-lts.png)

3. A seguir, execute o arquivo baixado e siga o fluxo de instalação normal, marcando apenas o _checkbox_ referente aos **termos de serviço**  
   ![Node installation step 1](images/node/install-1.png)
   ![Node installation step 2](images/node/install-2.png)
   ![Node installation step 3](images/node/install-3.png)
   ![Node installation step 4](images/node/install-4.png)
   ![Node installation step 5](images/node/install-5.png)
   ![Node installation step 6](images/node/install-6.png)
   ![Node installation step 7](images/node/install-7.png)
   ![Node installation step 8](images/node/install-8.png)

4. Para **verificar sua instalação** abra uma janela do terminal e execute os comandos `npm --version` e `node --version`. O comando **node** será utilizado para execução das aplicações, enquanto o **npm** é o gerenciador de pacotes para bibliotecas Javascript. Os seguintes _outputs_ deveria ser vistos, mostrando a versão instalada de ambos comandos.  
   ![Node version check](images/node/version-check.png)

## Configuração de Git

O **Git** é o gerenciador de versões mais utilizado no mundo, de forma que com ele podemos criar novas versões de nossas aplicações, assim como gerenciar versões já criadas. Sua instalação também é bem simples.

1. Acesso o **link** de download em seu [site oficial](https://git-scm.com/downloads), selecione seu **sistema operacional** e clique no botão de **download**  
   ![Git download Page](images/git/git-download.jpg)
   ![Git download Page](images/git/git-downloaded.png)

2. Após feito o download execute o arquivo e siga as instruções de instalação. Não é necessário alterar **nenhuma** das opções selecionadas.  
   ![Git installation step 1](images/git/install-1.png)
   ![Git installation step 2](images/git/install-2.png)
   ![Git installation step 3](images/git/install-3.png)
   ![Git installation step 4](images/git/install-4.png)
   ![Git installation step 5](images/git/install-5.png)
   ![Git installation step 6](images/git/install-6.png)
   ![Git installation step 7](images/git/install-7.png)

3. Para **verificar sua instalação** abra uma janela do terminal e execute o comando `git --version` e verifique a versão do **git** que foi instalada.

   ![Git version check](images/git/version-check.png)

## Configuração do VSCode

O **Visual Studio Code** é um editor de código fonte extremamente popular, tendo um grande foco no desenvolvimento de **Javascript** e **Typescript**. Ele será utilizado nos exemplos mostrados durante as aulas, sendo que a seguir mostrarei como instalá-lo.

1. Acesso o **link** de download em seu [site oficial](https://code.visualstudio.com/Download) e selecione o link de download referente ao seu **sistema operacional**  
   ![VSCode download Page](images/vscode/download-page.png)
   ![VSCode download Page](images/vscode/downloaded-page.png)

2. Após feito o download execute o arquivo e siga as instruções de instalação conforme as imagens abaixo.  
   ![VSCode installation step 1](images/vscode/install-1.png)
   ![VSCode installation step 2](images/vscode/install-2.png)
   ![VSCode installation step 3](images/vscode/install-3.png)
   ![VSCode installation step 4](images/vscode/install-4.png)
   ![VSCode installation step 5](images/vscode/install-5.png)
   ![VSCode installation step 6](images/vscode/install-6.png)
   ![VSCode installation step 7](images/vscode/install-7.png)

3. Ao finalizar a instalação, uma nova janela do **VSCode** deve se abrir.  
   ![VSCode window](images/vscode/new-window.png)

4. Na página inicial existe um simples tutorial explicando algumas das **funcionalidades básicas** da aplicação. Porém por enquanto iremos para o **painel de extensões**.  
   ![Extensions panel](images/vscode/extensions-panel.png)

5. No painel procuraremos pela extensão **Gitlens**, ela adiciona funcionalidades extras relacionadas ao **Git** ao VSCode. Por enquanto basta instalá-la.  
   ![Gitlens](images/vscode/gitlens.png)

## Executando a API e o App Web

Como mencionado, durante nossas aulas práticas usaremos duas aplicações como base para aplicação do que formos aprendendo. Dessa forma utilizaremos uma **API** e um **Site** em **Typescript**, que utilizam respectivamente **ExpressJS** e **NextJS** em sua construção. Ambas aplicações podem ser encontradas no formato `.zip` (api.zip e web.zip) nesta mesma pasta. Inicialmente descomprima-as e siga os passo a seguir, nos quais mostrarei como executar ambas aplicações.

1. Apos descomprimir ambas as pastas, rode o comando `npm install` dentro de cada uma delas, de forma a instalar as **bibliotecas** necessárias para executa-las.  
   ![NPM installing](images/apps/npm-installing.png)
   ![NPM installed](images/apps/npm-installed.png)

2. Tendo instalado as dependências, crie um arquivo `.env` em cada pasta. Coloque respectivamente na **API** e no **Site** as seguintes variáveis:

   ```.env
      # API
      NODE_ENV=development
      APP_PORT=5000

      # Web
      NEXT_PUBLIC_API_URL=http://localhost:5000
   ```

3. Por fim, basta executar ambas aplicações rodando o comando `npm run dev` para cada uma delas.  
   ![API running](images/apps/api-running.png)
   ![Web running](images/apps/web-running.png)

4. Sua aplicação deveria estar rodando na port **3000**, logo basta acessa <http://localhost:3000> e usar o site  
   ![App running](images/apps/running-app.png)
