###
O Git e o Github possuem vários comandos, mas para facilitar o seu uso, dividimos em categorias.
O **Git** é o sistema de controle de versão (funciona no seu computador).
O **GitHUb** é a plataforma online onde você pode hospedar e gerenciar seus repositórios.

Abaixo, vou organizar **todos os principais comandos do Git** (com explicaçães) para você que está se desbravando nesse novo mundo.  

## 🔹Comandos Essenciais do Git

---
|**Comando**| **Função**|
:---|:---| 
|`git init`|Inicializa um novo repositório Git no diretório atual|
|`git clone <url>`|Clona um repositório remoto para sua máquina.|
|`git status`|Mostra o estado atual do repositório (arquivos modificados, staged, etc).|
|`git add <arquivo>`|Adiciona um arquivo específico para a área de staging.|
|`gitt add .`|Adiciona todos os arquivos modificados para staging.|
|`git commit -m "mensagem"`|Salva as mudanças no repositório com uma mensagem.|
|`git log`| Mostra o histórico de commits.|
|`git diff`|Mostra as diferenças entre arquivos modificados e o último commit.|
|`git remote add origin <https/ssh>`|Adiciona o repositório de destino dos commits.|
|`git push origin <branch>`|Envia suas mudanças para o repositório remoto (ex: GitHub).|
|`git pull origin <branch>`| Baixa e mescla mudanças do repositório remoto.|
|`git fetch`| Baixa as mudanças, mas não mescla automaticamente.|

---
## 🔹Trabalhando com Branches
|**Comando**|**Função**|
|:---|:---|
|`git branch`|Lista branches existentes.|
|`git branch <nome>`|Cria uma nova branch.|
|`git branch`|Troca para a branch especificada.|
|`git checkout -b <nome>`|Cria e troca para a nova branch.|
|`git switch <branch>`|(Mais novo que checkout) troca de branch.|
|`git merge <branch>`|Mescla a branch indicada com a atual.|
|`git rebase <branch>`|Reaplica commits da branch atual em cima da branch indicada.|
|`git branch -d <nome>`|Deleta uma branch local.|

---
## 🔹Gerenciamento de Arquivos
|**Comando**|**Funções**|
|:---|:---|
|`git rm <arquivo>`|Remove um arquivo do repositório e do diretório.|
|`git mv <nome_antigo> <nome_novo>`|Renomeia ou move um arquivo.|
|`git clean -f`|Remove arquivos não rastreados.|

---
## 🔹Histórico e Visualização
|**Comando**|**Funções**|
|:---|:---|
|`git log --oneline`|Mostra o histórico de commits em uma linha cada.|
|`git log --graph --oneline --all`|Mostra gráfico de branches e commits.|
|`git show <commit>`|Mostra detalhes de um commit específico.|
|`git blame <arquivo>|Mostra quem alterou cada linha do arquivo.|
|`git shortlog`|Mostra commits agrupados por autor.|

---
## 🔹Desfazer Alterações
|**Comando**|**Funções**|
|:---|:---|
|`git reset <arquivo>`|Remove arquivo do staging, mas mantém alterações locais.|
|`git reset --hard <commit>`|Volta o repositório para um commit específico (descarta mudanças).|
|`git revert <commit>`| Cria um novo commit que desfaz o commit especificado.|
|`git checkout -- <arquivo>`|Restaura arquivo modificado para o estado do último commit.|

---
## 🔹Tags (versões)
|**Comando**|**Funções**|
|:---|:---|
|`git tag`|Lista todas as tags.|
|`git tag <nome>`|Cria uma tag leve.|
|`git tag -a <nome> -m "mensagem"`|Cria uma tag anotada|
|`git push origin <tag>`|Envia uma tag para o repositório remoto.|
|`git push --tags`|Envia todas as tags locais.|

---
## 🔹Configurações do Git
|**Comando**|**Funções**|
|:---|:---|
|`git config --global user.name "seu nome"`|Define nome global do autor dos commits.|
|`git config --global user.email "seu@email.com"`|Define email global do autor dos commits.|
|`git config --list`|Lista todas as configurações atuais.|

---
## 🔹Comandos Avançados
|**Comando**|**Funções**|
|:---|:---|
|`git stash`|Salva temporariamente alterações sem commit.|
|`git stash pop`|Recupera e aplica as alterações salvas.|
|`git cherry-pick <commit>`| Aplica um commit específico em outra branch.|
|`git reflog`|Mostra histórico completo de referências (inclusive resets e reverts).|
|`git bisect`|Ajuda a encontrar commit que introduziu um bug.|
|`git submodule add <url>`|Adiciona um repositório dentro de outro.|

---
## 🔹GitHub CLI (gh)
### 
Além do Git tradicional, o GitHub tem a CLI (`gh`) para gerenciar direto pelo terminal.
|**Comando**|**Funções**|
|:---|:---|
|`gh auth login`|Conecta sua conta GitHub à CLI.|
|`gh repo create`|Cria um repositório no GitHub.|
|`gh repo clone <repo>`|Clona um repositório do GitHub.|
|`gh repo fork <repo>`|Cria um fork no GitHub.|
|`gh pr create`|Cria um Pull Request.|
|`gh pr list`|Lista PRs abertos.|
|`gh issue crate`|Cria uma issue.|
|`gh issue list`|Lista issues abertas.|
