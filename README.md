Git - Projeto Fase 1
================================================

Comandos GIT


**O git possui 4 áreas de trabalho:**
*1. O diretório .git que é o repositório contendo todos os arquivos versionados;*
*2. Working Area que é um snapshot do .git dentro de um determinado momento no tempo;*
*3. Stage que é um local temporário que armazena a referência para arquivos a serem versionados antes de serem commitados;*
*4. Stash que também é um local temporário que pode armazenar e esconder arquivos que estão no Stage.*

**Criando um repositório local**
>cd meuprojeto
>git init

**Para visualizar o status e confirmar se foi criado o repositório local**
>git status

**Adicionando arquivo.txt**
>git add arquivo.txt 

**Para adicionar apenas o arquivot.txt**
>git add arquivo.txt 

**Caso tenha mais de um arquivo e queira adicionar todos ao mesmo tempo**
>git add .

**Voltar ao estágio anterior do add**
>git reset HEAD arquivo.txt

**Commit - Apenas arquivos no Stage podem ser commitados**
>git commit -m "mensagem de commit"

**Adicionando e comitando ao mesmo tempo**
>git commit -a -m "mensagem de commit"

**Para voltar o commit para versões anteriores**

*Voltar um commit*
>git reset HEAD~1

*Voltar dois commit*
>git reset HEAD~2


**Volta um commit e mantém os últimos arquivos no Stage**
>git reset HEAD~1 --soft

**Volta um commit e excluindo o arquivo, deixando no estágio anterior**
>git reset HEAD~1 --hard

**Visualizando os logs (lista os commits)**
>git log

**Exibe o que foi mudado, diferença entre um arquivo e outro**
>git log -p

**Exibe os 2 últimos commits**
>git log -p -2

**Mostra o que foi modificado em cada commit**
>git log --stat


**Exibe commits dos últimos 2 dias até o momento atual**
>git log --since=2.days

**Cria um branch contendo os mesmos commits do branch de origem**
>git checkout -b novobranch 

**Exibe em que branch você está**
>git branch

**Volta para o branch master**
>git checkout master

**Inserindo o branch criado no branch master**

*Entre como branch master*
>git merge novobranch


**Apagando um branch**
>git branch -D novobranch

**Exibe branchs remotos**
>git branch -a

**Apagando arquivos**
>git rm arquivo.txt

**Deletando todos os aquivos removidos ao mesmo tempo**
>git ls-files --deleted | xargs git rm

**Ignorando arquivos**

*Crie um arquivo chamado .gitignore*
*Digite o caminho da(s) pasta(s) ou arquivo(s) a ser ignorado, sendo um arquivo por linha*


**Criando um clone do github**
>git clone (url do arquivo)

**Fazendo um clone de outros branchs**
>git checkout -b (nome do branch) origin/ (nome do branch)

**Trazendo, puxando as alterações feitas por outros usuários**
>git pull origin master

**Sincronizando tudo que está no repositório remoto**
>git pull

**Enviando o(s) projeto(s), arquivo(s) para o repositório - github**
>git push origin

**Enviando um branch para o repositório - github**
>git push origin (nome do branch)

**Criando tags**
>git tag (versão da tag) 

**Listando tags**
>git tag -l

**Enviando a tag para o repositório - github**
>git push origin master --tags

**Removendo as tags criadas**

*Removendo tag localmente*
>git tag -d 0.1.0

*Removendo tag no repositório remoto*
>git push origin :refs/tags/0.1.0

**Criando um repositório local**

*Crie uma pasta e entre nela*
>git init --bare

*Saia da pasta*
>git checkout master 
>git push local

