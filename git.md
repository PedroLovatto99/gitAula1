# Um pequeno tutorial de git
---

## Enviando arquivos para o github, pela primeira vez

Para iniciar um repositório local basta rodar o seguinte comando:
```
git init
```
assim já podemos começar a gerenciadiar nossos arquivos, para vermos os arquivos que foram modificados e estão preparados para serem subidos, podemos rodar o comando
```
git status
```
assim veremos todas as modificações no código

para prepararmos todos os arquivo para enviar para o github utilizamos o seguinte comando
```
git add .
```
se quisermos adicionar apenas um, substitui-se o "." pelo caminho do arquivo

porém caso quisermos reverter o que foi feito em todos os códigos usamos o seguinte comando
```
git restore .
```
e para restaurar apenas um, substituimos o "." pelo caminho do arquivo

assim que adicionarmos os arquivos estamos preparados para enviar para o github, podemos cirar um commit, ele é criado com o seguinte comando
```
git commit -m "descrição do que contem no commit"
```
para prosseguirmos com o desenvolvimento é recomendado mudar o nome da branch para "develop", para evidar conflitos com o github, para fazermos isso rodamos o seguinte comando
```
git branch -M "develop"
```
depois disso só precisamos indicar para o git para onde ele deve enviar o código, e fazemos isso da seguinte forma
``` 
git remote add origin linkDoRepositório
```
e agora rodamos o código para enviarmos
```
git push -u origin develop
```
assim acabamos de enviar o nosso código para o github

---

## Trazendo repositórios do github

bem, para trazermos o repositório, é bem simples, basta utilizarmos o seguinte comando
```
git clone linkDoRepositório
```

---

## Branches

quando falamos de git um de seus principáis diferenciais são suas branches, que nada mais são que ramificações do código original, assim facilitando para implementar mais de uma funcionalidade ao mesmo tempo, para vermos as branches utilizamos o seguinte comando

```
git branch
```

para criarmos uma branch rodamos o seguinte comando
```
bit branch nomeDaBranch
```
assim que criada a branch será um clone da branch na qual se estava quando o comando for rodado, e também não seremos redirecionados para ela automaticamente, para fazermos isso rodamos o seguinte comando
```
git checkout nomeDaBranch
```

para subirmos essa branch basta, rodarmos o comando `git push`, e para atualizarmos a branch, basta rodarmos o comando `git pull`, porém se apenas rodarmos esse comando não irá funcionar, primeiro precismos dizer qual branch remota a branch local estaria apontando, para fazermos isso, rodamos esse comando
```
git branch -u <origin/nomeDaBranchRemota>
```

---

## Alguns links uteis
[Documentação do Git](https://git-scm.com/book/pt-br/v2)<br>
[Documentação do GitHub](https://docs.github.com/pt)
