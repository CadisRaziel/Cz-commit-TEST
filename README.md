08/06/2020 -> Adicionamos o padrão de commit internacional com a ferramente 'cz commit'
https://github.com/commitizen/cz-cli


# "Antes de tudo lembre-se, não criaremos mais branch pelo terminal do vsCode, vamos criar todas pelo Azure !!"


## **Entendendo Historia/Task/Bug'** ->

A imagem abaixo representa uma **HISTORIA**
![hitoria2.png](/.attachments/hitoria2-765dc6a6-a00f-4f8f-ad3c-558b9b14a412.png)


A imagem abaixo representa uma **TASK** ou poderia ser um **BUG**
![task.png](/.attachments/task-1e1bc91d-663d-4c85-9c47-e61f2da912b0.png)


_Quando vamos criar branch diretamente do Azure, precisamos entender essas duas imagens !!!_

# Criando Branch no Azure, siga o passo a passo:

## 1º passo -> 
• Vá até a branch 'developT' 
• Clique nos 3 pontinhos circulado em vermelho igual da imagen
• Ele vai abrir um menu 
• A primeira opção ja é assim "+ New Branch", clique nela.
![1título.png](/.attachments/1título-ee343826-c528-479c-b7c6-64f4b29c2b4a.png)


## 2º passo -> 
• Em "Name*" voce vai colocar o que essa branch condiz (feat/docs/fix/style... conforme o cz) e o **NUMERO DA HISTORIA** conforme o exemplo na imagem...
• Em seguida no "Based on" voce vai escolher em qual Branch vai se basear, geralmente todas serão na developT....
• Em seguida no "Work items to link" voce vai colocar o **NUMERO DA HISTORIA** que esta no azure, selecione ela e ela ficará igual a imagem e de um "Create"
![branch.png](/.attachments/branch-0ca89da3-546d-4e59-b4d0-33a9a84b5d2c.png)

## 3º passo ->
• Entre no VsCode na branch "developT"
• De um git fetch e um git pull para pegar a nova branch
• Entre na nova branch criada pelo Azure e pronto.


# Utilizando o CZ pelo terminal 

## 1º passo -> 
• Faça o que tem que fazer na branch e de um 'git add .'
• Em seguida utilize o comando 'cz', ele vai abrir as possibildiades de commmit, confira na imagem
![git2.png](/.attachments/git2-9f6d9340-b519-4091-93ff-6b9610335fdf.png)
• **feat:** Um novo recurso
• **fix:** uma correção de bug
• **docs:** somente a documentação muda
• **style:** Alterações que não afetam o significado do código (espaço em branco, formatação, falta de ponto e vírgula, etc)
• **refactor:** Uma alteração de código que não corrige um bug nem adiciona um recurso
• **perf:** Uma alteração de código que melhora o desempenho
• **test:** Adicionando testes ausentes ou corrigindo testes existentes
• **build:** Alterações que afetam o sistema de compilação ou dependências externas (escopos de exemplo: gulp, broccoli, npm)
• **ci:** Alterações em nossos arquivos e scripts de configuração de CI (escopos de exemplo: Travis, Circle, BrowserStack, SauceLabs)
• **chore:** Outras alterações que não modificam src ou arquivos de teste
• **reverter:** Reverte um commit anterior

## 2º passo ->
• Suponhamos que escolhi 'style' porém podia ser qualquer outra o padrão é o mesmo pra todas !!
• What is the scope of this change (e.g. component or file name):   (press enter to skip)  
• Tradução: Qual é o escopo dessa alteração (por exemplo, componente ou nome do arquivo):(pressione enter para pular)
• ele vai nos pergunta o nome dos arquivos em que mexemos (caso nao quiser por só de um enter), eu coloquei que só alterei o arquivo 'main', _porém repare eu nao preciso por completo 'main.dart' é apenas o NOME do arquivo !!_
• depois de colocar o nome ou nao colocar aperte o ENTER
![st2.png](/.attachments/st2-8efd1a12-db08-4ca8-81b2-ecd6be73b5e3.png)

## 3º passo -> 
• Write a short, imperative tense description of the change (max 68 chars):
• Tradução: Escreva uma descrição breve e imperativa da mudança (máximo de 68 caracteres):
• Aqui colocamos um breve titulo (repare que coloquei "Remove comments")
![st3.png](/.attachments/st3-54efbc66-b8e3-459a-8b78-d8d3d4e4afa7.png)

## 4º passo -> 
• Provide a longer description of the change: (press enter to skip)  
• Tradução: Forneça uma descrição mais longa da alteração: (pressione enter para pular)
• Aqui voce coloca uma descrição do que fez !!
• Repare que eu coloquei ("removing comments from main" foi o que eu fiz no arquivo)
![st4.png](/.attachments/st4-d45652da-bb80-47fe-9362-0ab7a4e00c29.png)

## 5º passo -> 
• Are there any breaking changes ? (y/N)
• Tradução: há alguma mudança de quebra? (y/N)
• Aqui ele pergunta se isso vai ter algum conflito, caso tiver especifique ao clicar em Y
• caso voce tenha certeza que nao tenha, coloque n
• aqui eu coloquei o seguinte("two people tidying the same file" duas pessoas mexendo no mesmo arquivo então é 100% de chance de conflito)
![st5.png](/.attachments/st5-01e7b592-ef1d-466e-91df-940cf3472469.png)

## 6º passo -> 
• Does this change affect any open issues? 
• Tradução: Essa alteração afeta quaisquer problemas em aberto? (y/N)
• Aqui é a parte mais legal, pois como existe TASK criada, podemos colocar o numero dela aqui !!!
• Como na imagem la em cima o numero da task é 4134
• então nós só especificamos "task #4134" e pronto
![st6.png](/.attachments/st6-beedb8b1-240b-4d32-b4e0-4d5148457cda.png)

## 7º passo ->
• Pronto, agora voce pode dar um git push !!!
• Com isso ao abrir PR no Azure ele ja vai trazer a task e a historia !!


[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
